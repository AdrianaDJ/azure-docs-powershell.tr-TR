---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592221"
---
# <span data-ttu-id="571b4-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="571b4-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="571b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="571b4-102">SYNOPSIS</span></span>
<span data-ttu-id="571b4-103">Belirtilen olay hub 'ını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="571b4-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="571b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="571b4-104">SYNTAX</span></span>

### <span data-ttu-id="571b4-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="571b4-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="571b4-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="571b4-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="571b4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="571b4-107">DESCRIPTION</span></span>
<span data-ttu-id="571b4-108">Set-AzureRmEventHub cmdlet 'i belirtilen olay hub 'ının özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="571b4-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="571b4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="571b4-109">EXAMPLES</span></span>

### <span data-ttu-id="571b4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="571b4-110">Example 1</span></span>
<span data-ttu-id="571b4-111">Eventhub 'ı yakalama açıklaması özellikleriyle güncelleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="571b4-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="571b4-112">\`MyCreatedEventHub nesnesiyle gösterilen olay hub myeventhubname 'i güncelleştirir \` \` \` , ileti bekletme süresini 4 gün olarak ayarlar, bölüm sayısını 2 ve captureaçıklama özelliklerine ayarlar</span><span class="sxs-lookup"><span data-stu-id="571b4-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="571b4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="571b4-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="571b4-114">\`MyCreatedEventHub nesnesiyle temsil edilen olay hub myeventhubname 'i güncelleştirir \` \` \` , ileti bekletme süresini 4 güne ve bölüm sayısını da 2 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="571b4-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="571b4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="571b4-115">PARAMETERS</span></span>

### <span data-ttu-id="571b4-116">-Messageretentionındays</span><span class="sxs-lookup"><span data-stu-id="571b4-116">-messageRetentionInDays</span></span>
<span data-ttu-id="571b4-117">Gün içinde olay merkezi ileti saklama süresi.</span><span class="sxs-lookup"><span data-stu-id="571b4-117">Event Hub message retention period, in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="571b4-118">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="571b4-118">-partitionCount</span></span>
<span data-ttu-id="571b4-119">Bu olay hub 'ındaki bölüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="571b4-119">Number of partitions on this Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="571b4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="571b4-120">-ResourceGroupName</span></span>
<span data-ttu-id="571b4-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="571b4-121">Resource group name.</span></span>

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

### <span data-ttu-id="571b4-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="571b4-122">-Confirm</span></span>
<span data-ttu-id="571b4-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="571b4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="571b4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="571b4-124">-WhatIf</span></span>
<span data-ttu-id="571b4-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="571b4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="571b4-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="571b4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="571b4-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="571b4-127">-InputObject</span></span>
<span data-ttu-id="571b4-128">EventHub nesnesi.</span><span class="sxs-lookup"><span data-stu-id="571b4-128">EventHub object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="571b4-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="571b4-129">-Name</span></span>
<span data-ttu-id="571b4-130">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="571b4-130">Namespace Name.</span></span>

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

### <span data-ttu-id="571b4-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="571b4-131">-Namespace</span></span>
<span data-ttu-id="571b4-132">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="571b4-132">Namespace Name.</span></span>

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

## <span data-ttu-id="571b4-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="571b4-133">INPUTS</span></span>

### <span data-ttu-id="571b4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="571b4-134">System.String</span></span>

## <span data-ttu-id="571b4-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="571b4-135">OUTPUTS</span></span>

### <span data-ttu-id="571b4-136">Microsoft. Azure. Commands. EventHub. modeller. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="571b4-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="571b4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="571b4-137">NOTES</span></span>

## <span data-ttu-id="571b4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="571b4-138">RELATED LINKS</span></span>

