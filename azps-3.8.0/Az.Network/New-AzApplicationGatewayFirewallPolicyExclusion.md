---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicyexclusion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyExclusion.md
ms.openlocfilehash: e5ad76625a171e1fd12fc583c6ad8acf593ed817
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104817"
---
# <span data-ttu-id="12f3a-101">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="12f3a-101">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="12f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="12f3a-103">Güvenlik Duvarı Ilkesinde dışlama oluşturur</span><span class="sxs-lookup"><span data-stu-id="12f3a-103">Creates an exclusion on the Firewall Policy</span></span>

## <span data-ttu-id="12f3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12f3a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable <String> -SelectorMatchOperator <String>
 -Selector <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12f3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="12f3a-106">**New-Azapplicationgatewayfirewallpolicydışlaması** cmdlet 'i güvenlik duvarı ilkesi için yeni bir dışlama kuralı listesi.</span><span class="sxs-lookup"><span data-stu-id="12f3a-106">The **New-AzApplicationGatewayFirewallPolicyExclusion** cmdlet a new exclusion rule list for firewall policy.</span></span>

## <span data-ttu-id="12f3a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="12f3a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="12f3a-108">Example 1</span></span>
```powershell
PS C:\> $exclusionEntry = New-AzApplicationGatewayFirewallPolicyExclusion -MatchVariable "RequestHeaderNames" -SelectorMatchOperator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="12f3a-109">Bu komut, Ertheadernames ve WITH xyz adlı ad ve dosya adı</span><span class="sxs-lookup"><span data-stu-id="12f3a-109">This command creates a new exclusion-entry for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="12f3a-110">Dışlama girişi $exclusionEntry kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="12f3a-110">The exclusion entry is saved in $exclusionEntry.</span></span>

## <span data-ttu-id="12f3a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12f3a-111">PARAMETERS</span></span>

### <span data-ttu-id="12f3a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f3a-112">-DefaultProfile</span></span>
<span data-ttu-id="12f3a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12f3a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f3a-114">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="12f3a-114">-MatchVariable</span></span>
<span data-ttu-id="12f3a-115">Dışlanacak değişken.</span><span class="sxs-lookup"><span data-stu-id="12f3a-115">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestHeaderNames, RequestCookieNames, RequestArgNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f3a-116">-Seçici</span><span class="sxs-lookup"><span data-stu-id="12f3a-116">-Selector</span></span>
<span data-ttu-id="12f3a-117">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12f3a-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="12f3a-118">-SelectorMatchOperator</span><span class="sxs-lookup"><span data-stu-id="12f3a-118">-SelectorMatchOperator</span></span>
<span data-ttu-id="12f3a-119">Değişken bir koleksiyon olduğunda, bu dışlama koleksiyonundaki hangi öğelerin uygulanacağını belirtmek için seçici üzerinde işlem yapın.</span><span class="sxs-lookup"><span data-stu-id="12f3a-119">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Equals, Contains, StartsWith, EndsWith, EqualsAny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f3a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f3a-120">CommonParameters</span></span>
<span data-ttu-id="12f3a-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12f3a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f3a-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="12f3a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f3a-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12f3a-123">INPUTS</span></span>

### <span data-ttu-id="12f3a-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="12f3a-124">None</span></span>

## <span data-ttu-id="12f3a-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12f3a-125">OUTPUTS</span></span>

### <span data-ttu-id="12f3a-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="12f3a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion</span></span>

## <span data-ttu-id="12f3a-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12f3a-127">NOTES</span></span>

## <span data-ttu-id="12f3a-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12f3a-128">RELATED LINKS</span></span>
