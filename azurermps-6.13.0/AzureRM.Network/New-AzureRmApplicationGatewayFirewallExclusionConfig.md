---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 570e2df066f9e56b7926bf2d0926c484a0654977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591359"
---
# <span data-ttu-id="e3de7-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="e3de7-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="e3de7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3de7-102">SYNOPSIS</span></span>
<span data-ttu-id="e3de7-103">Uygulama ağ geçidi için yeni bir dışlama kuralı listesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="e3de7-103">Creates a new exclusion rule list for application gateway waf</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3de7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3de7-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3de7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3de7-105">DESCRIPTION</span></span>
<span data-ttu-id="e3de7-106">**New-AzureRmApplicationGatewayFirewallExclusionConfig** cmdlet 'i, Application Gateway WAF için yeni bir dışlama kuralı listesi.</span><span class="sxs-lookup"><span data-stu-id="e3de7-106">The **New-AzureRmApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="e3de7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3de7-107">EXAMPLES</span></span>

### <span data-ttu-id="e3de7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e3de7-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="e3de7-109">Bu komut, Ertheadernames ve WITH xyz adlı ad ve işleç adındaki işleç adlı değişken için yeni bir dışlama kuralı listesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3de7-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="e3de7-110">Dışlama listesi yapılandırması $exclusion 1 ' de kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="e3de7-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="e3de7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3de7-111">PARAMETERS</span></span>

### <span data-ttu-id="e3de7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3de7-112">-DefaultProfile</span></span>
<span data-ttu-id="e3de7-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3de7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3de7-114">-İşleç</span><span class="sxs-lookup"><span data-stu-id="e3de7-114">-Operator</span></span>
<span data-ttu-id="e3de7-115">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için seçici üzerinde işlem yapın.</span><span class="sxs-lookup"><span data-stu-id="e3de7-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="e3de7-116">-Seçici</span><span class="sxs-lookup"><span data-stu-id="e3de7-116">-Selector</span></span>
<span data-ttu-id="e3de7-117">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e3de7-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="e3de7-118">Değişkenli</span><span class="sxs-lookup"><span data-stu-id="e3de7-118">-Variable</span></span>
<span data-ttu-id="e3de7-119">Dışlanacak değişken.</span><span class="sxs-lookup"><span data-stu-id="e3de7-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="e3de7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3de7-120">CommonParameters</span></span>
<span data-ttu-id="e3de7-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3de7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3de7-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3de7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3de7-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3de7-123">INPUTS</span></span>

### <span data-ttu-id="e3de7-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e3de7-124">None</span></span>

## <span data-ttu-id="e3de7-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3de7-125">OUTPUTS</span></span>

### <span data-ttu-id="e3de7-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="e3de7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="e3de7-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3de7-127">NOTES</span></span>

## <span data-ttu-id="e3de7-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3de7-128">RELATED LINKS</span></span>
