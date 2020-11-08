---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267253"
---
# <span data-ttu-id="dabf4-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="dabf4-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="dabf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dabf4-102">SYNOPSIS</span></span>
<span data-ttu-id="dabf4-103">Teslim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dabf4-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="dabf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dabf4-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dabf4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dabf4-105">DESCRIPTION</span></span>
<span data-ttu-id="dabf4-106">**New-AzCdnDeliveryPolicy** CMDLET 'i CDN uç noktası oluşturma için bir teslim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dabf4-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="dabf4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dabf4-107">EXAMPLES</span></span>

### <span data-ttu-id="dabf4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dabf4-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="dabf4-109">Örnek teslim ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dabf4-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="dabf4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dabf4-110">PARAMETERS</span></span>

### <span data-ttu-id="dabf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabf4-111">-DefaultProfile</span></span>
<span data-ttu-id="dabf4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dabf4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dabf4-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="dabf4-113">-Description</span></span>
<span data-ttu-id="dabf4-114">İlkenin açıklaması</span><span class="sxs-lookup"><span data-stu-id="dabf4-114">Description of the policy</span></span>

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

### <span data-ttu-id="dabf4-115">-Kural</span><span class="sxs-lookup"><span data-stu-id="dabf4-115">-Rule</span></span>
<span data-ttu-id="dabf4-116">DeliveryRules listesi.</span><span class="sxs-lookup"><span data-stu-id="dabf4-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabf4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabf4-117">CommonParameters</span></span>
<span data-ttu-id="dabf4-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dabf4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabf4-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dabf4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabf4-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dabf4-120">INPUTS</span></span>

### <span data-ttu-id="dabf4-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dabf4-121">None</span></span>

## <span data-ttu-id="dabf4-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dabf4-122">OUTPUTS</span></span>

### <span data-ttu-id="dabf4-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="dabf4-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="dabf4-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dabf4-124">NOTES</span></span>

## <span data-ttu-id="dabf4-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dabf4-125">RELATED LINKS</span></span>
