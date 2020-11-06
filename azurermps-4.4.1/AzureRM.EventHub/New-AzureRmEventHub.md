---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594709"
---
# <span data-ttu-id="3bba2-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="3bba2-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="3bba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bba2-102">SYNOPSIS</span></span>
<span data-ttu-id="3bba2-103">Yeni bir olay hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bba2-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bba2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3bba2-104">SYNTAX</span></span>

### <span data-ttu-id="3bba2-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3bba2-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3bba2-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="3bba2-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3bba2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3bba2-107">DESCRIPTION</span></span>
<span data-ttu-id="3bba2-108">New-AzureRmEventHub cmdlet 'i yeni bir Azure Olay Hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bba2-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="3bba2-109">Yakalama açıklaması özellikleriyle Eventhub oluşturmak için aşağıdaki adımları izleyin (örnekler 2).</span><span class="sxs-lookup"><span data-stu-id="3bba2-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="3bba2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3bba2-110">EXAMPLES</span></span>

### <span data-ttu-id="3bba2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3bba2-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="3bba2-112">\` \` \` WestUS \` konumunda, myresourcegroupname kaynak grubuyla birlikte, 3 günlük ileti bekletme dönemi ve iki bölümlü, myeventhubname adlı bir \` Olay Hub 'ı oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="3bba2-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3bba2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3bba2-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

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

<span data-ttu-id="3bba2-114">\` \` \` WestUS \` konumunda, myresourcegroupname kaynak grubuyla birlikte, 3 günlük ileti bekletme dönemi, 2 bölüm ve Capturedescription özellikleri içeren bir \` Olay Hub 'ı oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="3bba2-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3bba2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3bba2-115">PARAMETERS</span></span>

### <span data-ttu-id="3bba2-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="3bba2-116">-Location</span></span>
<span data-ttu-id="3bba2-117">Ad alanı coğrafi konumu.</span><span class="sxs-lookup"><span data-stu-id="3bba2-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bba2-118">-Messageretentionındays</span><span class="sxs-lookup"><span data-stu-id="3bba2-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="3bba2-119">Gün içinde Olay Hub 'Ları ileti tutma süresi.</span><span class="sxs-lookup"><span data-stu-id="3bba2-119">Event Hubs message retention time in days.</span></span>

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

### <span data-ttu-id="3bba2-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="3bba2-120">-PartitionCount</span></span>
<span data-ttu-id="3bba2-121">Olay Hub 'ındaki bölüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="3bba2-121">Number of partitions in the Event Hub.</span></span>

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

### <span data-ttu-id="3bba2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bba2-122">-ResourceGroupName</span></span>
<span data-ttu-id="3bba2-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3bba2-123">Resource group name.</span></span>

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

### <span data-ttu-id="3bba2-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="3bba2-124">-Confirm</span></span>
<span data-ttu-id="3bba2-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3bba2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bba2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bba2-126">-WhatIf</span></span>
<span data-ttu-id="3bba2-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3bba2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bba2-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3bba2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bba2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bba2-129">-InputObject</span></span>
<span data-ttu-id="3bba2-130">EventHub giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3bba2-130">EventHub Input object.</span></span>

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

### <span data-ttu-id="3bba2-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="3bba2-131">-Name</span></span>
<span data-ttu-id="3bba2-132">Eventhub adı.</span><span class="sxs-lookup"><span data-stu-id="3bba2-132">Eventhub Name.</span></span>

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

### <span data-ttu-id="3bba2-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3bba2-133">-Namespace</span></span>
<span data-ttu-id="3bba2-134">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="3bba2-134">Namespace Name.</span></span>

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

## <span data-ttu-id="3bba2-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3bba2-135">INPUTS</span></span>

### <span data-ttu-id="3bba2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3bba2-136">System.String</span></span>

## <span data-ttu-id="3bba2-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3bba2-137">OUTPUTS</span></span>

### <span data-ttu-id="3bba2-138">Microsoft. Azure. Commands. EventHub. modeller. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3bba2-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="3bba2-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3bba2-139">NOTES</span></span>

## <span data-ttu-id="3bba2-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3bba2-140">RELATED LINKS</span></span>

