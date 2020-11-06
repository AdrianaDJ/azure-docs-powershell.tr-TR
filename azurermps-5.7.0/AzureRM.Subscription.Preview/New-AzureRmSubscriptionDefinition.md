---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592857"
---
# <span data-ttu-id="022a6-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="022a6-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="022a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="022a6-102">SYNOPSIS</span></span>
<span data-ttu-id="022a6-103">Abonelik tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="022a6-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="022a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="022a6-104">SYNTAX</span></span>

### <span data-ttu-id="022a6-105">Abonelik tanımı oluştur</span><span class="sxs-lookup"><span data-stu-id="022a6-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="022a6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="022a6-106">DESCRIPTION</span></span>
<span data-ttu-id="022a6-107">**Yeni-AzureRmSubscriptionDefinition** cmdlet 'i abonelik tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="022a6-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="022a6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="022a6-108">EXAMPLES</span></span>

### <span data-ttu-id="022a6-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="022a6-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="022a6-110">Varsayılan abonelik görünen adıyla bir abonelik tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="022a6-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="022a6-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="022a6-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="022a6-112">Özel bir abonelik görünen adıyla bir abonelik tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="022a6-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="022a6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="022a6-113">PARAMETERS</span></span>

### <span data-ttu-id="022a6-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="022a6-114">-Name</span></span>
<span data-ttu-id="022a6-115">Oluşturulacak abonelik tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="022a6-115">The name of the subscription definition to create.</span></span>

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

### <span data-ttu-id="022a6-116">-OfferType</span><span class="sxs-lookup"><span data-stu-id="022a6-116">-OfferType</span></span>
<span data-ttu-id="022a6-117">Temel alınan abonelik oluşturulurken kullanılacak teklifin türü.</span><span class="sxs-lookup"><span data-stu-id="022a6-117">The type of offer to use when creating the underlying subscription.</span></span>

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

### <span data-ttu-id="022a6-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="022a6-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="022a6-119">Abonelik tanımının temel aldığı aboneliğini oluştururken kullanılacak görünen ad.</span><span class="sxs-lookup"><span data-stu-id="022a6-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="022a6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="022a6-120">CommonParameters</span></span>
<span data-ttu-id="022a6-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="022a6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="022a6-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="022a6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="022a6-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="022a6-123">INPUTS</span></span>

### <span data-ttu-id="022a6-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="022a6-124">None</span></span>

## <span data-ttu-id="022a6-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="022a6-125">OUTPUTS</span></span>

### <span data-ttu-id="022a6-126">Microsoft. Azure. Commands. SubscriptionDefinition. modeller. PSSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="022a6-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="022a6-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="022a6-127">NOTES</span></span>

## <span data-ttu-id="022a6-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="022a6-128">RELATED LINKS</span></span>

