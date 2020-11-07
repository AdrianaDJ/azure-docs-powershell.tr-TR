---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: 2b1f3c0cd30b9f0ebc67a0b11f5b42a35b7e3394
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935857"
---
# <span data-ttu-id="5e6d3-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="5e6d3-101">Set-AzEventHub</span></span>

## <span data-ttu-id="5e6d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5e6d3-103">Belirtilen olay hub 'ını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="5e6d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e6d3-104">SYNTAX</span></span>

### <span data-ttu-id="5e6d3-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5e6d3-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e6d3-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="5e6d3-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e6d3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e6d3-107">DESCRIPTION</span></span>
<span data-ttu-id="5e6d3-108">Set-AzEventHub cmdlet 'i belirtilen olay hub 'ının özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="5e6d3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e6d3-109">EXAMPLES</span></span>

### <span data-ttu-id="5e6d3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e6d3-110">Example 1</span></span>
<span data-ttu-id="5e6d3-111">Eventhub 'ı yakalama açıklaması özellikleriyle güncelleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="5e6d3-112">\`MyCreatedEventHub nesnesiyle gösterilen olay hub myeventhubname 'i güncelleştirir \` \` \` , ileti bekletme süresini 4 gün olarak ayarlar, bölüm sayısını 2 ve captureaçıklama özelliklerine ayarlar</span><span class="sxs-lookup"><span data-stu-id="5e6d3-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="5e6d3-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5e6d3-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="5e6d3-114">\`MyCreatedEventHub nesnesiyle temsil edilen olay hub myeventhubname 'i güncelleştirir \` \` \` , ileti bekletme süresini 4 güne ve bölüm sayısını da 2 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="5e6d3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e6d3-115">PARAMETERS</span></span>

### <span data-ttu-id="5e6d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e6d3-116">-DefaultProfile</span></span>
<span data-ttu-id="5e6d3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e6d3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e6d3-118">-InputObject</span></span>
<span data-ttu-id="5e6d3-119">EventHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="5e6d3-119">EventHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6d3-120">-Messageretentionındays</span><span class="sxs-lookup"><span data-stu-id="5e6d3-120">-messageRetentionInDays</span></span>
<span data-ttu-id="5e6d3-121">Gün Içinde Eventhub Ileti tutma</span><span class="sxs-lookup"><span data-stu-id="5e6d3-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6d3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e6d3-122">-Name</span></span>
<span data-ttu-id="5e6d3-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="5e6d3-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6d3-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e6d3-124">-Namespace</span></span>
<span data-ttu-id="5e6d3-125">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="5e6d3-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6d3-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="5e6d3-126">-partitionCount</span></span>
<span data-ttu-id="5e6d3-127">Eventhub bölüm sayısı</span><span class="sxs-lookup"><span data-stu-id="5e6d3-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6d3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e6d3-128">-ResourceGroupName</span></span>
<span data-ttu-id="5e6d3-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5e6d3-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6d3-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e6d3-130">-Confirm</span></span>
<span data-ttu-id="5e6d3-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e6d3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e6d3-132">-WhatIf</span></span>
<span data-ttu-id="5e6d3-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e6d3-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e6d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e6d3-135">CommonParameters</span></span>
<span data-ttu-id="5e6d3-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e6d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e6d3-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e6d3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e6d3-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e6d3-138">INPUTS</span></span>

### <span data-ttu-id="5e6d3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5e6d3-139">System.String</span></span>

### <span data-ttu-id="5e6d3-140">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="5e6d3-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="5e6d3-141">System. Nullable ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5e6d3-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5e6d3-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e6d3-142">OUTPUTS</span></span>

### <span data-ttu-id="5e6d3-143">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="5e6d3-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="5e6d3-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e6d3-144">NOTES</span></span>

## <span data-ttu-id="5e6d3-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e6d3-145">RELATED LINKS</span></span>
