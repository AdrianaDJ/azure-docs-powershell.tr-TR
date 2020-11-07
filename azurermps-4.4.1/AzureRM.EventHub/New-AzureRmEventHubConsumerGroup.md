---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764855"
---
# <span data-ttu-id="d7db2-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d7db2-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="d7db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7db2-102">SYNOPSIS</span></span>
<span data-ttu-id="d7db2-103">Belirtilen olay hub 'ı için yeni bir tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7db2-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7db2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7db2-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d7db2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7db2-105">DESCRIPTION</span></span>
<span data-ttu-id="d7db2-106">New-AzureRmEventHubConsumerGroup cmdlet 'i belirtilen olay hub 'ı için yeni bir tüketici grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7db2-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="d7db2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7db2-107">EXAMPLES</span></span>

### <span data-ttu-id="d7db2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d7db2-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="d7db2-109">\` \` \` \` \` \` Myresourcegroupname kaynak grubuyla, mynamespacename ad alanı kapsamındaki Olay Hub myeventhubname ile tüketici \` \` grubu 'nu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7db2-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d7db2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7db2-110">PARAMETERS</span></span>

### <span data-ttu-id="d7db2-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7db2-111">-ResourceGroupName</span></span>
<span data-ttu-id="d7db2-112">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d7db2-112">Resource group name.</span></span>

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

### <span data-ttu-id="d7db2-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="d7db2-113">-UserMetadata</span></span>
<span data-ttu-id="d7db2-114">Tüketici grubu için Kullanıcı meta verileri.</span><span class="sxs-lookup"><span data-stu-id="d7db2-114">User metadata for the consumer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7db2-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7db2-115">-Confirm</span></span>
<span data-ttu-id="d7db2-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7db2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7db2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7db2-117">-WhatIf</span></span>
<span data-ttu-id="d7db2-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7db2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7db2-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7db2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7db2-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d7db2-120">-EventHub</span></span>
<span data-ttu-id="d7db2-121">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="d7db2-121">EventHub Name.</span></span>

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

### <span data-ttu-id="d7db2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7db2-122">-Name</span></span>
<span data-ttu-id="d7db2-123">ConsumerGroup adı.</span><span class="sxs-lookup"><span data-stu-id="d7db2-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="d7db2-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d7db2-124">-Namespace</span></span>
<span data-ttu-id="d7db2-125">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d7db2-125">Namespace Name.</span></span>

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

## <span data-ttu-id="d7db2-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7db2-126">INPUTS</span></span>

### <span data-ttu-id="d7db2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d7db2-127">System.String</span></span>

## <span data-ttu-id="d7db2-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7db2-128">OUTPUTS</span></span>

### <span data-ttu-id="d7db2-129">Microsoft. Azure. Commands. EventHub. model. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="d7db2-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="d7db2-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7db2-130">NOTES</span></span>

## <span data-ttu-id="d7db2-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7db2-131">RELATED LINKS</span></span>

