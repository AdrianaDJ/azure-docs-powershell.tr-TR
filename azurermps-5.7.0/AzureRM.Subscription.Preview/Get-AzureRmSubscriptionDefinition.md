---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/get-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 8f9cfda051542327fdb6175da081c99e6b8b6b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587389"
---
# <span data-ttu-id="3345e-101">Get-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="3345e-101">Get-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="3345e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3345e-102">SYNOPSIS</span></span>
<span data-ttu-id="3345e-103">Abonelik tanımı alın.</span><span class="sxs-lookup"><span data-stu-id="3345e-103">Get a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3345e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3345e-104">SYNTAX</span></span>

### <span data-ttu-id="3345e-105">Abonelik tanımlarını alın.</span><span class="sxs-lookup"><span data-stu-id="3345e-105">Get subscription definitions.</span></span>
```
Get-AzureRmSubscriptionDefinition
```

## <span data-ttu-id="3345e-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3345e-106">EXAMPLES</span></span>

### <span data-ttu-id="3345e-107">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3345e-107">Example 1</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition

Name                    : MyProdSubscription1
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyProdSubscription1
OfferType               : MS-AZR-0017P

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="3345e-108">Tüm abonelik tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="3345e-108">Gets all subscription definitions.</span></span>

### <span data-ttu-id="3345e-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3345e-109">Example 2</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition -Name MyProdSubscription2

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="3345e-110">MyProdSubscription2 adında bir abonelik tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="3345e-110">Gets a subscription definition with the name MyProdSubscription2.</span></span>

## <span data-ttu-id="3345e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3345e-111">PARAMETERS</span></span>

### <span data-ttu-id="3345e-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="3345e-112">-Name</span></span>
<span data-ttu-id="3345e-113">Alınacak abonelik tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="3345e-113">The name of the subscription definition to retrieve.</span></span>

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

### <span data-ttu-id="3345e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3345e-114">CommonParameters</span></span>
<span data-ttu-id="3345e-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3345e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3345e-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3345e-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3345e-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3345e-117">INPUTS</span></span>

### <span data-ttu-id="3345e-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3345e-118">None</span></span>

## <span data-ttu-id="3345e-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3345e-119">OUTPUTS</span></span>

### <span data-ttu-id="3345e-120">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. SubscriptionDefinition. modeller. PSSubscriptionDefinition, Microsoft. Azure. Commands. SubscriptionDefinition, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3345e-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition, Microsoft.Azure.Commands.SubscriptionDefinition, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3345e-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3345e-121">NOTES</span></span>

## <span data-ttu-id="3345e-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3345e-122">RELATED LINKS</span></span>

