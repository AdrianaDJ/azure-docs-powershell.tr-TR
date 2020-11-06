---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592224"
---
# <span data-ttu-id="74534-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="74534-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="74534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74534-102">SYNOPSIS</span></span>
<span data-ttu-id="74534-103">Belirtilen olay hub 'ı tüketici grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="74534-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74534-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74534-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="74534-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74534-105">DESCRIPTION</span></span>
<span data-ttu-id="74534-106">Remove-AzureRmEventHubConsumerGroup cmdlet 'i, verilen olay hub 'ından belirtilen tüketici grubunu kaldırır ve siler.</span><span class="sxs-lookup"><span data-stu-id="74534-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="74534-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74534-107">EXAMPLES</span></span>

### <span data-ttu-id="74534-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="74534-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="74534-109">\`Myconsumergroupname adlı tüketici grubunu, \` kapsam dışı \` \` olarak \` mynamespacename \` ad alanına siler.</span><span class="sxs-lookup"><span data-stu-id="74534-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="74534-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74534-110">PARAMETERS</span></span>

### <span data-ttu-id="74534-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74534-111">-ResourceGroupName</span></span>
<span data-ttu-id="74534-112">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="74534-112">Resource group name.</span></span>

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

### <span data-ttu-id="74534-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="74534-113">-Confirm</span></span>
<span data-ttu-id="74534-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74534-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74534-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74534-115">-WhatIf</span></span>
<span data-ttu-id="74534-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74534-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74534-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74534-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74534-118">-EventHub</span><span class="sxs-lookup"><span data-stu-id="74534-118">-EventHub</span></span>
<span data-ttu-id="74534-119">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="74534-119">EventHub Name.</span></span>

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

### <span data-ttu-id="74534-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="74534-120">-Name</span></span>
<span data-ttu-id="74534-121">ConsumerGroup adı.</span><span class="sxs-lookup"><span data-stu-id="74534-121">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74534-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="74534-122">-Namespace</span></span>
<span data-ttu-id="74534-123">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="74534-123">Namespace Name.</span></span>

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

## <span data-ttu-id="74534-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74534-124">INPUTS</span></span>

### <span data-ttu-id="74534-125">System. String</span><span class="sxs-lookup"><span data-stu-id="74534-125">System.String</span></span>

## <span data-ttu-id="74534-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74534-126">OUTPUTS</span></span>

### <span data-ttu-id="74534-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="74534-127">System.Object</span></span>

## <span data-ttu-id="74534-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74534-128">NOTES</span></span>

## <span data-ttu-id="74534-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74534-129">RELATED LINKS</span></span>

