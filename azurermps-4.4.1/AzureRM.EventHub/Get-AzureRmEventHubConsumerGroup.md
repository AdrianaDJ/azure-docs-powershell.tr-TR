---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594714"
---
# <span data-ttu-id="097f3-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="097f3-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="097f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="097f3-102">SYNOPSIS</span></span>
<span data-ttu-id="097f3-103">Belirli bir olay hub tüketici grubunun ayrıntılarını alır veya bir olay hub 'ındaki tüketici gruplarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="097f3-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="097f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="097f3-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="097f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="097f3-105">DESCRIPTION</span></span>
<span data-ttu-id="097f3-106">Get-AzureRmEventHubConsumerGroup cmdlet 'i, belirtilen bir olay hub tüketici grubunun ayrıntılarını veya belirli bir olay hub 'ındaki tüketici gruplarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="097f3-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="097f3-107">Tüketici grubunun adı sağlanmışsa, tek bir tüketici grubu ayrıntılarının ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="097f3-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="097f3-108">Tüketici grubunun adı sağlanmadıysa, belirtilen olay hub 'ındaki tüketici gruplarının listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="097f3-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="097f3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="097f3-109">EXAMPLES</span></span>

### <span data-ttu-id="097f3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="097f3-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="097f3-111">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla Adynamespacename ad alanında bulunan Olay Hub myeventhubname myconsumergroupname adlı \` Tüketici grubunu alır \` .</span><span class="sxs-lookup"><span data-stu-id="097f3-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="097f3-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="097f3-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="097f3-113">\` \` \` \` Myresourcegroupname kaynak grubuyla Mynamespacename ad alanında bulunan Olay Hub myeventhubname içindeki tüketici \` gruplarının bir listesini alır \` .</span><span class="sxs-lookup"><span data-stu-id="097f3-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="097f3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="097f3-114">PARAMETERS</span></span>

### <span data-ttu-id="097f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="097f3-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="097f3-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097f3-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="097f3-117">-EventHub</span></span>
<span data-ttu-id="097f3-118">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="097f3-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097f3-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="097f3-119">-Name</span></span>
<span data-ttu-id="097f3-120">ConsumerGroup adı.</span><span class="sxs-lookup"><span data-stu-id="097f3-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097f3-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="097f3-121">-Namespace</span></span>
<span data-ttu-id="097f3-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="097f3-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="097f3-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="097f3-123">INPUTS</span></span>

### <span data-ttu-id="097f3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="097f3-124">System.String</span></span>

## <span data-ttu-id="097f3-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="097f3-125">OUTPUTS</span></span>

### <span data-ttu-id="097f3-126">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub., Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="097f3-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="097f3-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="097f3-127">NOTES</span></span>

## <span data-ttu-id="097f3-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="097f3-128">RELATED LINKS</span></span>

