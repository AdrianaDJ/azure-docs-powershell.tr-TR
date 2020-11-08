---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107888"
---
# <span data-ttu-id="6ec12-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="6ec12-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="6ec12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec12-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec12-103">Teslim kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ec12-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="6ec12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ec12-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ec12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ec12-105">DESCRIPTION</span></span>
<span data-ttu-id="6ec12-106">**New-AzCdnDeliveryRule** CMDLET 'i CDN uç noktası oluşturma için bir teslim kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ec12-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="6ec12-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ec12-107">EXAMPLES</span></span>

### <span data-ttu-id="6ec12-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ec12-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="6ec12-109">Basit bir kural oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6ec12-109">Create a simple rule.</span></span>

## <span data-ttu-id="6ec12-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ec12-110">PARAMETERS</span></span>

### <span data-ttu-id="6ec12-111">-Eylem</span><span class="sxs-lookup"><span data-stu-id="6ec12-111">-Action</span></span>
<span data-ttu-id="6ec12-112">Kuralın tüm koşulları tatmin edildiğinde yürütülen eylemlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="6ec12-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec12-113">-Koşul</span><span class="sxs-lookup"><span data-stu-id="6ec12-113">-Condition</span></span>
<span data-ttu-id="6ec12-114">Yürütülecek eylemler için eşleşmesi gereken koşulların listesi.</span><span class="sxs-lookup"><span data-stu-id="6ec12-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec12-115">-DefaultProfile</span></span>
<span data-ttu-id="6ec12-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ec12-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ec12-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ec12-117">-Name</span></span>
<span data-ttu-id="6ec12-118">Kuralın adı</span><span class="sxs-lookup"><span data-stu-id="6ec12-118">Name of the rule</span></span>

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

### <span data-ttu-id="6ec12-119">-Düzen</span><span class="sxs-lookup"><span data-stu-id="6ec12-119">-Order</span></span>
<span data-ttu-id="6ec12-120">Kuralın sırası</span><span class="sxs-lookup"><span data-stu-id="6ec12-120">Order of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec12-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec12-121">CommonParameters</span></span>
<span data-ttu-id="6ec12-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ec12-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec12-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6ec12-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec12-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ec12-124">INPUTS</span></span>

### <span data-ttu-id="6ec12-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6ec12-125">None</span></span>

## <span data-ttu-id="6ec12-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ec12-126">OUTPUTS</span></span>

### <span data-ttu-id="6ec12-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="6ec12-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="6ec12-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ec12-128">NOTES</span></span>

## <span data-ttu-id="6ec12-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ec12-129">RELATED LINKS</span></span>
