---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763218"
---
# <span data-ttu-id="dec95-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="dec95-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="dec95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dec95-102">SYNOPSIS</span></span>
<span data-ttu-id="dec95-103">Belirtilen hizmet veri yolu ad alanında hizmet veri yolu kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dec95-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dec95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dec95-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dec95-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dec95-105">DESCRIPTION</span></span>
<span data-ttu-id="dec95-106">**Yeni-AzureRmServiceBusQueue** cmdlet 'i, belirtilen hizmet veri yolu ad boşluğunda bir hizmet veri yolu kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dec95-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="dec95-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dec95-107">EXAMPLES</span></span>

### <span data-ttu-id="dec95-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dec95-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="dec95-109">`SB-Queue_exampl1`Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu kuyruğu oluşturur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="dec95-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="dec95-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dec95-110">PARAMETERS</span></span>

### <span data-ttu-id="dec95-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="dec95-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="dec95-112">Sıranın otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec95-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="dec95-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="dec95-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="dec95-114">-Confirm</span></span>
<span data-ttu-id="dec95-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dec95-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dec95-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="dec95-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="dec95-117">Ileti süre sonu</span><span class="sxs-lookup"><span data-stu-id="dec95-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="dec95-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="dec95-119">Canlı değer için TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="dec95-119">Timespan to live value.</span></span>
<span data-ttu-id="dec95-120">Bu, iletinin kullanım süresi dolduğunda, iletinin hizmet veri yoluna gönderildiği tarihten sonraki süredir.</span><span class="sxs-lookup"><span data-stu-id="dec95-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="dec95-121">Bu, bir iletide TimeToLive ayarlanmamışsa kullanılan varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="dec95-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="dec95-122">Standart = TimeSpan. Max ve Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="dec95-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec95-123">-DefaultProfile</span></span>
<span data-ttu-id="dec95-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dec95-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dec95-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="dec95-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="dec95-126">Yinelenen saptama geçmişinin süresini tanımlayan bir [TimeSpan değeri](https://msdn.microsoft.com/library/system.timespan.aspx) yineleme algılama geçmişi zamanı penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dec95-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="dec95-127">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="dec95-127">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="dec95-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="dec95-129">Toplu Işlemleri etkinleştir-sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini belirten değer</span><span class="sxs-lookup"><span data-stu-id="dec95-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="dec95-130">-EnableExpress</span></span>
<span data-ttu-id="dec95-131">Enablehızlı-hızlı varlıkların etkinleştirilip etkinleştirilmediğini belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="dec95-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="dec95-132">Bir hızlı kuyruk, kalıcı depolama birimine yazmadan önce geçici olarak bellekte bir ileti tutar.</span><span class="sxs-lookup"><span data-stu-id="dec95-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-133">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="dec95-133">-EnablePartitioning</span></span>
<span data-ttu-id="dec95-134">Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="dec95-134">EnablePartitioning</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="dec95-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="dec95-136">Atılacak iletiyi iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="dec95-136">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-137">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="dec95-137">-ForwardTo</span></span>
<span data-ttu-id="dec95-138">İletileri iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="dec95-138">Queue/Topic name to forward the messages</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-139">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="dec95-139">-LockDuration</span></span>
<span data-ttu-id="dec95-140">Kilitleme süresi</span><span class="sxs-lookup"><span data-stu-id="dec95-140">Lock Duration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="dec95-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="dec95-142">MaxDeliveryCount-en fazla teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="dec95-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="dec95-143">Bu numaradan sonra otomatik olarak bir ileti verilir.</span><span class="sxs-lookup"><span data-stu-id="dec95-143">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-144">-Maxsizeınmega</span><span class="sxs-lookup"><span data-stu-id="dec95-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="dec95-145">Maxsizeınmegabaytlık-sıra için ayrılan belleğin megabayt cinsinden megabayt cinsinden en büyük boyutu.</span><span class="sxs-lookup"><span data-stu-id="dec95-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="dec95-146">-MessageCount</span></span>
<span data-ttu-id="dec95-147">MessageCount-kuyruktaki iletilerin sayısı</span><span class="sxs-lookup"><span data-stu-id="dec95-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="dec95-148">-Name</span></span>
<span data-ttu-id="dec95-149">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="dec95-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-150">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dec95-150">-Namespace</span></span>
<span data-ttu-id="dec95-151">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="dec95-151">Namespace Name</span></span>

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

### <span data-ttu-id="dec95-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="dec95-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="dec95-153">RequiresDuplicateDetection-sıranın oturum kavramını destekleyip desteklemediğini belirten bir değer</span><span class="sxs-lookup"><span data-stu-id="dec95-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="dec95-154">-RequiresSession</span></span>
<span data-ttu-id="dec95-155">RequiresSession-bu sıranın yinelenen öğe algılaması gerektirip gerektirmediğini belirten değer</span><span class="sxs-lookup"><span data-stu-id="dec95-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec95-156">-ResourceGroupName</span></span>
<span data-ttu-id="dec95-157">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="dec95-157">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="dec95-158">-SizeInBytes</span></span>
<span data-ttu-id="dec95-159">SizeInBytes-baytların bayt cinsinden boyutu</span><span class="sxs-lookup"><span data-stu-id="dec95-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec95-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dec95-160">-WhatIf</span></span>
<span data-ttu-id="dec95-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dec95-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dec95-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dec95-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dec95-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec95-163">CommonParameters</span></span>
<span data-ttu-id="dec95-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dec95-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dec95-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec95-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec95-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dec95-166">INPUTS</span></span>

### <span data-ttu-id="dec95-167">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dec95-167">-ResourceGroup</span></span>
 <span data-ttu-id="dec95-168">System. String</span><span class="sxs-lookup"><span data-stu-id="dec95-168">System.String</span></span>

### <span data-ttu-id="dec95-169">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="dec95-169">-NamespaceName</span></span>
 <span data-ttu-id="dec95-170">System. String</span><span class="sxs-lookup"><span data-stu-id="dec95-170">System.String</span></span>

### <span data-ttu-id="dec95-171">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="dec95-171">-QueueName</span></span>
 <span data-ttu-id="dec95-172">System. String</span><span class="sxs-lookup"><span data-stu-id="dec95-172">System.String</span></span>

### <span data-ttu-id="dec95-173">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="dec95-173">-EnablePartitioning</span></span>
 <span data-ttu-id="dec95-174">System. Boolean.</span><span class="sxs-lookup"><span data-stu-id="dec95-174">System.Boolean?</span></span>


## <span data-ttu-id="dec95-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dec95-175">OUTPUTS</span></span>

### <span data-ttu-id="dec95-176">Microsoft. Azure. Commands. ServiceBus. modeller. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="dec95-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="dec95-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dec95-177">NOTES</span></span>

## <span data-ttu-id="dec95-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dec95-178">RELATED LINKS</span></span>
