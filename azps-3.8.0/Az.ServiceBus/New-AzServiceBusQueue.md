---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: a555e269fd02cb02d420426fed99888b19214f52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096790"
---
# <span data-ttu-id="84ac7-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="84ac7-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="84ac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="84ac7-103">Belirtilen hizmet veri yolu ad alanında hizmet veri yolu kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84ac7-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="84ac7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84ac7-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84ac7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84ac7-105">DESCRIPTION</span></span>
<span data-ttu-id="84ac7-106">**New-AzServiceBusQueue** cmdlet 'i, belirtilen hizmet veri yolu ad boşluğunda bir hizmet veri yolu kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84ac7-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="84ac7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84ac7-107">EXAMPLES</span></span>

### <span data-ttu-id="84ac7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="84ac7-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="84ac7-109">`SB-Queue_example1`Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu kuyruğu oluşturur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="84ac7-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="84ac7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84ac7-110">PARAMETERS</span></span>

### <span data-ttu-id="84ac7-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="84ac7-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="84ac7-112">Sıranın otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84ac7-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="84ac7-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="84ac7-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="84ac7-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="84ac7-115">Ileti süre sonu</span><span class="sxs-lookup"><span data-stu-id="84ac7-115">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="84ac7-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="84ac7-117">Canlı değer için TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="84ac7-117">Timespan to live value.</span></span>
<span data-ttu-id="84ac7-118">Bu, iletinin kullanım süresi dolduğunda, iletinin hizmet veri yoluna gönderildiği tarihten sonraki süredir.</span><span class="sxs-lookup"><span data-stu-id="84ac7-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="84ac7-119">Bu, bir iletide TimeToLive ayarlanmamışsa kullanılan varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="84ac7-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="84ac7-120">Standart = TimeSpan. Max ve BASIC = 14 gün için</span><span class="sxs-lookup"><span data-stu-id="84ac7-120">For Standard = Timespan.Max and Basic = 14 days</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ac7-121">-DefaultProfile</span></span>
<span data-ttu-id="84ac7-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84ac7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84ac7-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="84ac7-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="84ac7-124">Yinelenen saptama geçmişinin süresini tanımlayan bir [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) değeri yineleme algılama geçmişi zamanı penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84ac7-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="84ac7-125">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="84ac7-125">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="84ac7-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="84ac7-127">Toplu Işlemleri etkinleştir-sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini belirten değer</span><span class="sxs-lookup"><span data-stu-id="84ac7-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="84ac7-128">-EnableExpress</span></span>
<span data-ttu-id="84ac7-129">Enablehızlı-hızlı varlıkların etkinleştirilip etkinleştirilmediğini belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="84ac7-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="84ac7-130">Bir hızlı kuyruk, kalıcı depolama birimine yazmadan önce geçici olarak bellekte bir ileti tutar.</span><span class="sxs-lookup"><span data-stu-id="84ac7-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-131">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="84ac7-131">-EnablePartitioning</span></span>
<span data-ttu-id="84ac7-132">Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="84ac7-132">EnablePartitioning</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="84ac7-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="84ac7-134">Atılacak iletiyi iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="84ac7-134">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="84ac7-135">-ForwardTo</span></span>
<span data-ttu-id="84ac7-136">İletileri iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="84ac7-136">Queue/Topic name to forward the messages</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="84ac7-137">-LockDuration</span></span>
<span data-ttu-id="84ac7-138">Kilitleme süresi</span><span class="sxs-lookup"><span data-stu-id="84ac7-138">Lock Duration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="84ac7-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="84ac7-140">MaxDeliveryCount-en fazla teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="84ac7-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="84ac7-141">Bu numaradan sonra otomatik olarak bir ileti verilir.</span><span class="sxs-lookup"><span data-stu-id="84ac7-141">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-142">-Maxsizeınmega</span><span class="sxs-lookup"><span data-stu-id="84ac7-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="84ac7-143">Maxsizeınmegabaytlık-sıra için ayrılan belleğin megabayt cinsinden megabayt cinsinden en büyük boyutu. Varsayılan 1024 ' dır.</span><span class="sxs-lookup"><span data-stu-id="84ac7-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="84ac7-144">Standart SKU için maks 5120 ve Premium SKU için 81920, Izin verilen değerler: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="84ac7-144">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-145">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="84ac7-145">-MessageCount</span></span>
<span data-ttu-id="84ac7-146">MessageCount-kuyruktaki iletilerin sayısı</span><span class="sxs-lookup"><span data-stu-id="84ac7-146">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="84ac7-147">-Name</span></span>
<span data-ttu-id="84ac7-148">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="84ac7-148">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-149">-Namespace</span><span class="sxs-lookup"><span data-stu-id="84ac7-149">-Namespace</span></span>
<span data-ttu-id="84ac7-150">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="84ac7-150">Namespace Name</span></span>

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

### <span data-ttu-id="84ac7-151">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="84ac7-151">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="84ac7-152">RequiresDuplicateDetection-sıranın oturum kavramını destekleyip desteklemediğini belirten bir değer</span><span class="sxs-lookup"><span data-stu-id="84ac7-152">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-153">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="84ac7-153">-RequiresSession</span></span>
<span data-ttu-id="84ac7-154">RequiresSession-bu sıranın oturumları kullandığını belirten değer</span><span class="sxs-lookup"><span data-stu-id="84ac7-154">RequiresSession - the value indicating if this queue uses sessions</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84ac7-155">-ResourceGroupName</span></span>
<span data-ttu-id="84ac7-156">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="84ac7-156">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-157">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="84ac7-157">-SizeInBytes</span></span>
<span data-ttu-id="84ac7-158">SizeInBytes-baytların bayt cinsinden boyutu</span><span class="sxs-lookup"><span data-stu-id="84ac7-158">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84ac7-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="84ac7-159">-Confirm</span></span>
<span data-ttu-id="84ac7-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84ac7-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84ac7-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84ac7-161">-WhatIf</span></span>
<span data-ttu-id="84ac7-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84ac7-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84ac7-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84ac7-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84ac7-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ac7-164">CommonParameters</span></span>
<span data-ttu-id="84ac7-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84ac7-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ac7-166">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84ac7-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ac7-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84ac7-167">INPUTS</span></span>

### <span data-ttu-id="84ac7-168">System. String</span><span class="sxs-lookup"><span data-stu-id="84ac7-168">System.String</span></span>

### <span data-ttu-id="84ac7-169">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="84ac7-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84ac7-170">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="84ac7-170">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84ac7-171">System. Nullable ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="84ac7-171">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="84ac7-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84ac7-172">OUTPUTS</span></span>

### <span data-ttu-id="84ac7-173">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="84ac7-173">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="84ac7-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84ac7-174">NOTES</span></span>

## <span data-ttu-id="84ac7-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84ac7-175">RELATED LINKS</span></span>
