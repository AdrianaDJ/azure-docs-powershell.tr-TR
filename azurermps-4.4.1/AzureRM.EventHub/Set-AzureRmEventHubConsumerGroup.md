---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c871036c6f3113bd40e17fb5bbc201fa6297573c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593132"
---
# <span data-ttu-id="26bf3-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="26bf3-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="26bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="26bf3-103">Belirtilen olay hub 'ı tüketici grubunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="26bf3-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26bf3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26bf3-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="26bf3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="26bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="26bf3-106">Set-AzureRmEventHubConsumerGroup cmdlet 'i belirtilen olay hub 'ı tüketici grubuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="26bf3-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="26bf3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="26bf3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="26bf3-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="26bf3-109">Tüketici grubunun Kullanıcı meta verilerini \` myconsumergroupname \` "test" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="26bf3-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="26bf3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26bf3-110">PARAMETERS</span></span>

### <span data-ttu-id="26bf3-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26bf3-111">-ResourceGroupName</span></span>
<span data-ttu-id="26bf3-112">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="26bf3-112">Resource group name.</span></span>

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

### <span data-ttu-id="26bf3-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="26bf3-113">-UserMetadata</span></span>
<span data-ttu-id="26bf3-114">Tüketici grubu için Kullanıcı meta verileri (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="26bf3-114">User metadata for the consumer group (optional).</span></span>

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

### <span data-ttu-id="26bf3-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="26bf3-115">-Confirm</span></span>
<span data-ttu-id="26bf3-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26bf3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26bf3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26bf3-117">-WhatIf</span></span>
<span data-ttu-id="26bf3-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26bf3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26bf3-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26bf3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26bf3-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="26bf3-120">-EventHub</span></span>
<span data-ttu-id="26bf3-121">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="26bf3-121">EventHub Name.</span></span>

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

### <span data-ttu-id="26bf3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="26bf3-122">-Name</span></span>
<span data-ttu-id="26bf3-123">ConsumerGroup adı.</span><span class="sxs-lookup"><span data-stu-id="26bf3-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="26bf3-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="26bf3-124">-Namespace</span></span>
<span data-ttu-id="26bf3-125">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="26bf3-125">Namespace Name.</span></span>

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

## <span data-ttu-id="26bf3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26bf3-126">INPUTS</span></span>

### <span data-ttu-id="26bf3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="26bf3-127">System.String</span></span>

## <span data-ttu-id="26bf3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26bf3-128">OUTPUTS</span></span>

### <span data-ttu-id="26bf3-129">Microsoft. Azure. Commands. EventHub. model. ConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="26bf3-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="26bf3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26bf3-130">NOTES</span></span>

## <span data-ttu-id="26bf3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26bf3-131">RELATED LINKS</span></span>

