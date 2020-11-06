---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 74921cb6ccfc77e2c45d734316cb2a67817c7ede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587234"
---
# <span data-ttu-id="c0e3d-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="c0e3d-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="c0e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e3d-103">Yeni bir olay hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0e3d-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0e3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0e3d-104">SYNTAX</span></span>

### <span data-ttu-id="c0e3d-105">EventhubPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0e3d-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e3d-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0e3d-106">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0e3d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0e3d-107">DESCRIPTION</span></span>
<span data-ttu-id="c0e3d-108">New-AzureRmEventHub cmdlet 'i yeni bir Azure Olay Hub 'ı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c0e3d-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="c0e3d-109">Yakalama açıklaması özellikleriyle Eventhub oluşturmak için aşağıdaki adımları izleyin (örnekler 2).</span><span class="sxs-lookup"><span data-stu-id="c0e3d-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="c0e3d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0e3d-110">EXAMPLES</span></span>

### <span data-ttu-id="c0e3d-111">Örnek 1-yeni EventHub oluşturma</span><span class="sxs-lookup"><span data-stu-id="c0e3d-111">Example 1  - Create new EventHub</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="c0e3d-112">\` \` \` WestUS \` konumunda, myresourcegroupname kaynak grubuyla birlikte, 3 günlük ileti bekletme dönemi ve iki bölümlü, myeventhubname adlı bir \` Olay Hub 'ı oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="c0e3d-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c0e3d-113">Örnek 2 ' CaptureDescription ' ile Eventhub güncelleme</span><span class="sxs-lookup"><span data-stu-id="c0e3d-113">Example 2 Update Eventhub with 'CaptureDescription'</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

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

<span data-ttu-id="c0e3d-114">\` \` \` WestUS \` konumunda, myresourcegroupname kaynak grubuyla birlikte, 3 günlük ileti bekletme dönemi, 2 bölüm ve Capturedescription özellikleri içeren bir \` Olay Hub 'ı oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="c0e3d-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c0e3d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0e3d-115">PARAMETERS</span></span>

### <span data-ttu-id="c0e3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e3d-116">-DefaultProfile</span></span>
<span data-ttu-id="c0e3d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0e3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0e3d-118">-InputObject</span></span>
<span data-ttu-id="c0e3d-119">EventHub giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="c0e3d-119">EventHub Input object</span></span>

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

### <span data-ttu-id="c0e3d-120">-Messageretentionındays</span><span class="sxs-lookup"><span data-stu-id="c0e3d-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="c0e3d-121">Gün Içinde Eventhub Ileti tutma</span><span class="sxs-lookup"><span data-stu-id="c0e3d-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="c0e3d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0e3d-122">-Name</span></span>
<span data-ttu-id="c0e3d-123">Eventhub adı</span><span class="sxs-lookup"><span data-stu-id="c0e3d-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e3d-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c0e3d-124">-Namespace</span></span>
<span data-ttu-id="c0e3d-125">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="c0e3d-125">Namespace Name</span></span>

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

### <span data-ttu-id="c0e3d-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="c0e3d-126">-PartitionCount</span></span>
<span data-ttu-id="c0e3d-127">Eventhub bölüm sayısı</span><span class="sxs-lookup"><span data-stu-id="c0e3d-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="c0e3d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e3d-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0e3d-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c0e3d-129">Resource Group Name</span></span>

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

### <span data-ttu-id="c0e3d-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0e3d-130">-Confirm</span></span>
<span data-ttu-id="c0e3d-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0e3d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e3d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e3d-132">-WhatIf</span></span>
<span data-ttu-id="c0e3d-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0e3d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e3d-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0e3d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e3d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e3d-135">CommonParameters</span></span>
<span data-ttu-id="c0e3d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0e3d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e3d-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e3d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e3d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0e3d-138">INPUTS</span></span>

### <span data-ttu-id="c0e3d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c0e3d-139">System.String</span></span>

### <span data-ttu-id="c0e3d-140">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="c0e3d-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="c0e3d-141">System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c0e3d-141">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c0e3d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0e3d-142">OUTPUTS</span></span>

### <span data-ttu-id="c0e3d-143">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="c0e3d-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="c0e3d-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0e3d-144">NOTES</span></span>

## <span data-ttu-id="c0e3d-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0e3d-145">RELATED LINKS</span></span>
