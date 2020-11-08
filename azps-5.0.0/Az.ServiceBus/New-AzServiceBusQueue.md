---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: 16a7de817250170cf39a02200cee67c028249e1f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279377"
---
# <span data-ttu-id="b8352-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="b8352-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="b8352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8352-102">SYNOPSIS</span></span>
<span data-ttu-id="b8352-103">Belirtilen hizmet veri yolu ad alanında hizmet veri yolu kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8352-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b8352-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8352-104">SYNTAX</span></span>

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

## <span data-ttu-id="b8352-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8352-105">DESCRIPTION</span></span>
<span data-ttu-id="b8352-106">**New-AzServiceBusQueue** cmdlet 'i, belirtilen hizmet veri yolu ad boşluğunda bir hizmet veri yolu kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8352-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b8352-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8352-107">EXAMPLES</span></span>

### <span data-ttu-id="b8352-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b8352-108">Example 1</span></span>
```powershell
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

<span data-ttu-id="b8352-109">`SB-Queue_example1`Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu kuyruğu oluşturur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="b8352-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="b8352-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b8352-110">Example 2</span></span>

<span data-ttu-id="b8352-111">Belirtilen hizmet veri yolu ad alanında hizmet veri yolu kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8352-111">Creates a Service Bus queue in the specified Service Bus namespace.</span></span> <span data-ttu-id="b8352-112">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="b8352-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzServiceBusQueue -EnablePartitioning $true -MaxSizeInMegabytes <Int64> -Name SB-Queue_example1 -Namespace SB-Example1 -ResourceGroupName Default-ServiceBus-WestUS
```

## <span data-ttu-id="b8352-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8352-113">PARAMETERS</span></span>

### <span data-ttu-id="b8352-114">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="b8352-114">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="b8352-115">Sıranın otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8352-115">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="b8352-116">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="b8352-116">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="b8352-117">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="b8352-117">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="b8352-118">Ileti süre sonu</span><span class="sxs-lookup"><span data-stu-id="b8352-118">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="b8352-119">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b8352-119">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="b8352-120">Canlı değer için TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="b8352-120">Timespan to live value.</span></span>
<span data-ttu-id="b8352-121">Bu, iletinin kullanım süresi dolduğunda, iletinin hizmet veri yoluna gönderildiği tarihten sonraki süredir.</span><span class="sxs-lookup"><span data-stu-id="b8352-121">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="b8352-122">Bu, bir iletide TimeToLive ayarlanmamışsa kullanılan varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="b8352-122">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="b8352-123">Standart = TimeSpan. Max ve BASIC = 14 gün için</span><span class="sxs-lookup"><span data-stu-id="b8352-123">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="b8352-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8352-124">-DefaultProfile</span></span>
<span data-ttu-id="b8352-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8352-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8352-126">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="b8352-126">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="b8352-127">Yinelenen saptama geçmişinin süresini tanımlayan bir [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) değeri yineleme algılama geçmişi zamanı penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8352-127">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) value that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="b8352-128">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="b8352-128">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="b8352-129">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="b8352-129">-EnableBatchedOperations</span></span>
<span data-ttu-id="b8352-130">Toplu Işlemleri etkinleştir-sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini belirten değer</span><span class="sxs-lookup"><span data-stu-id="b8352-130">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="b8352-131">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="b8352-131">-EnableExpress</span></span>
<span data-ttu-id="b8352-132">Enablehızlı-hızlı varlıkların etkinleştirilip etkinleştirilmediğini belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="b8352-132">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="b8352-133">Bir hızlı kuyruk, kalıcı depolama birimine yazmadan önce geçici olarak bellekte bir ileti tutar.</span><span class="sxs-lookup"><span data-stu-id="b8352-133">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="b8352-134">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="b8352-134">-EnablePartitioning</span></span>
<span data-ttu-id="b8352-135">Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="b8352-135">EnablePartitioning</span></span>

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

### <span data-ttu-id="b8352-136">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="b8352-136">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="b8352-137">Atılacak iletiyi iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="b8352-137">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="b8352-138">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="b8352-138">-ForwardTo</span></span>
<span data-ttu-id="b8352-139">İletileri iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="b8352-139">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="b8352-140">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="b8352-140">-LockDuration</span></span>
<span data-ttu-id="b8352-141">Kilitleme süresi</span><span class="sxs-lookup"><span data-stu-id="b8352-141">Lock Duration</span></span>

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

### <span data-ttu-id="b8352-142">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="b8352-142">-MaxDeliveryCount</span></span>
<span data-ttu-id="b8352-143">MaxDeliveryCount-en fazla teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="b8352-143">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="b8352-144">Bu numaradan sonra otomatik olarak bir ileti verilir.</span><span class="sxs-lookup"><span data-stu-id="b8352-144">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="b8352-145">-Maxsizeınmega</span><span class="sxs-lookup"><span data-stu-id="b8352-145">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="b8352-146">Maxsizeınmegabaytlık-sıra için ayrılan belleğin megabayt cinsinden megabayt cinsinden en büyük boyutu. Varsayılan 1024 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b8352-146">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.Default is 1024.</span></span> <span data-ttu-id="b8352-147">Standart SKU için maks 5120 ve Premium SKU için 81920, Izin verilen değerler: 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span><span class="sxs-lookup"><span data-stu-id="b8352-147">Max for Standard SKU is 5120 and for Premium SKU is 81920, Allowed values : 1024, 2048, 3072, 4096, 5120, 10240, 20480, 40960, 81920</span></span>

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

### <span data-ttu-id="b8352-148">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="b8352-148">-MessageCount</span></span>
<span data-ttu-id="b8352-149">MessageCount-kuyruktaki iletilerin sayısı</span><span class="sxs-lookup"><span data-stu-id="b8352-149">MessageCount - the number of messages in the queue</span></span>

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

### <span data-ttu-id="b8352-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8352-150">-Name</span></span>
<span data-ttu-id="b8352-151">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="b8352-151">Queue Name</span></span>

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

### <span data-ttu-id="b8352-152">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8352-152">-Namespace</span></span>
<span data-ttu-id="b8352-153">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="b8352-153">Namespace Name</span></span>

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

### <span data-ttu-id="b8352-154">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="b8352-154">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="b8352-155">RequiresDuplicateDetection-sıranın oturum kavramını destekleyip desteklemediğini belirten bir değer</span><span class="sxs-lookup"><span data-stu-id="b8352-155">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

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

### <span data-ttu-id="b8352-156">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="b8352-156">-RequiresSession</span></span>
<span data-ttu-id="b8352-157">RequiresSession-bu sıranın oturumları kullandığını belirten değer</span><span class="sxs-lookup"><span data-stu-id="b8352-157">RequiresSession - the value indicating if this queue uses sessions</span></span>

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

### <span data-ttu-id="b8352-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8352-158">-ResourceGroupName</span></span>
<span data-ttu-id="b8352-159">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b8352-159">The name of the resource group</span></span>

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

### <span data-ttu-id="b8352-160">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="b8352-160">-SizeInBytes</span></span>
<span data-ttu-id="b8352-161">SizeInBytes-baytların bayt cinsinden boyutu</span><span class="sxs-lookup"><span data-stu-id="b8352-161">SizeInBytes - the size of the queue in bytes</span></span>

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

### <span data-ttu-id="b8352-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8352-162">-Confirm</span></span>
<span data-ttu-id="b8352-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8352-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8352-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8352-164">-WhatIf</span></span>
<span data-ttu-id="b8352-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8352-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8352-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8352-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8352-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8352-167">CommonParameters</span></span>
<span data-ttu-id="b8352-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8352-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8352-169">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8352-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8352-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8352-170">INPUTS</span></span>

### <span data-ttu-id="b8352-171">System. String</span><span class="sxs-lookup"><span data-stu-id="b8352-171">System.String</span></span>

### <span data-ttu-id="b8352-172">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8352-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8352-173">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8352-173">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8352-174">System. Nullable ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8352-174">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b8352-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8352-175">OUTPUTS</span></span>

### <span data-ttu-id="b8352-176">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="b8352-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="b8352-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8352-177">NOTES</span></span>

## <span data-ttu-id="b8352-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8352-178">RELATED LINKS</span></span>
