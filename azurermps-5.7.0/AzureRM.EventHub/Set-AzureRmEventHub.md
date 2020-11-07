---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
ms.openlocfilehash: 4de16b04151daa1c3e64dc6ea93b171c38fdb96a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590490"
---
# <span data-ttu-id="21d28-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="21d28-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="21d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21d28-102">SYNOPSIS</span></span>
<span data-ttu-id="21d28-103">Belirtilen olay hub 'ını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="21d28-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21d28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21d28-104">SYNTAX</span></span>

### <span data-ttu-id="21d28-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="21d28-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21d28-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="21d28-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21d28-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="21d28-107">DESCRIPTION</span></span>
<span data-ttu-id="21d28-108">Set-AzureRmEventHub cmdlet 'i belirtilen olay hub 'ının özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="21d28-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="21d28-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21d28-109">EXAMPLES</span></span>

### <span data-ttu-id="21d28-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21d28-110">Example 1</span></span>
<span data-ttu-id="21d28-111">Eventhub 'ı yakalama açıklaması özellikleriyle güncelleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="21d28-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 



```
PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
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

<span data-ttu-id="21d28-112">\`MyCreatedEventHub nesnesiyle gösterilen olay hub myeventhubname 'i güncelleştirir \` \` \` , ileti bekletme süresini 4 gün olarak ayarlar, bölüm sayısını 2 ve captureaçıklama özelliklerine ayarlar</span><span class="sxs-lookup"><span data-stu-id="21d28-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="21d28-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="21d28-113">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="21d28-114">\`MyCreatedEventHub nesnesiyle temsil edilen olay hub myeventhubname 'i güncelleştirir \` \` \` , ileti bekletme süresini 4 güne ve bölüm sayısını da 2 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="21d28-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="21d28-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21d28-115">PARAMETERS</span></span>

### <span data-ttu-id="21d28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d28-116">-DefaultProfile</span></span>
<span data-ttu-id="21d28-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21d28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d28-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21d28-118">-InputObject</span></span>
<span data-ttu-id="21d28-119">EventHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="21d28-119">EventHub object</span></span>

```yaml
Type: PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d28-120">-Messageretentionındays</span><span class="sxs-lookup"><span data-stu-id="21d28-120">-messageRetentionInDays</span></span>
<span data-ttu-id="21d28-121">Gün Içinde Eventhub Ileti tutma</span><span class="sxs-lookup"><span data-stu-id="21d28-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="21d28-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="21d28-122">-Name</span></span>
<span data-ttu-id="21d28-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="21d28-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d28-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="21d28-124">-Namespace</span></span>
<span data-ttu-id="21d28-125">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="21d28-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d28-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="21d28-126">-partitionCount</span></span>
<span data-ttu-id="21d28-127">Eventhub bölüm sayısı</span><span class="sxs-lookup"><span data-stu-id="21d28-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="21d28-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d28-128">-ResourceGroupName</span></span>
<span data-ttu-id="21d28-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="21d28-129">Resource Group Name</span></span>

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

### <span data-ttu-id="21d28-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="21d28-130">-Confirm</span></span>
<span data-ttu-id="21d28-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21d28-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d28-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21d28-132">-WhatIf</span></span>
<span data-ttu-id="21d28-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="21d28-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21d28-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="21d28-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d28-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d28-135">CommonParameters</span></span>
<span data-ttu-id="21d28-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21d28-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="21d28-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d28-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d28-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21d28-138">INPUTS</span></span>

### <span data-ttu-id="21d28-139">System. String</span><span class="sxs-lookup"><span data-stu-id="21d28-139">System.String</span></span>
<span data-ttu-id="21d28-140">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="21d28-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="21d28-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21d28-141">OUTPUTS</span></span>

### <span data-ttu-id="21d28-142">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="21d28-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="21d28-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21d28-143">NOTES</span></span>

## <span data-ttu-id="21d28-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21d28-144">RELATED LINKS</span></span>