---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587784"
---
# <span data-ttu-id="e8195-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="e8195-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="e8195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8195-102">SYNOPSIS</span></span>
<span data-ttu-id="e8195-103">Belirtilen hizmet veri yolu ad alanında hizmet veri yolu kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8195-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8195-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8195-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8195-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8195-105">DESCRIPTION</span></span>
<span data-ttu-id="e8195-106">**Yeni-AzureRmServiceBusQueue** cmdlet 'i, belirtilen hizmet veri yolu ad boşluğunda bir hizmet veri yolu kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8195-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e8195-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8195-107">EXAMPLES</span></span>

### <span data-ttu-id="e8195-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e8195-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="e8195-109">`SB-Queue_exampl1`Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu kuyruğu oluşturur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e8195-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="e8195-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8195-110">PARAMETERS</span></span>

### <span data-ttu-id="e8195-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="e8195-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="e8195-112">Sıranın otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="e8195-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="e8195-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="e8195-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="e8195-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="e8195-115">İletilerin süre bitime durumunda olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="e8195-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="e8195-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="e8195-117">Varsayılan ileti ömrünü (TTL) belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="e8195-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="e8195-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="e8195-119">Yinelenen saptama geçmişinin süresini tanımlayan bir [TimeSpan değeri](https://msdn.microsoft.com/library/system.timespan.aspx) yineleme algılama geçmişi zamanı penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="e8195-120">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="e8195-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="e8195-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="e8195-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="e8195-122">Sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="e8195-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="e8195-123">-EnableExpress</span></span>
<span data-ttu-id="e8195-124">Hızlı varlıkların etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="e8195-125">Bir hızlı kuyruk, kalıcı depolama birimine yazmadan önce geçici olarak bellekte bir ileti tutar.</span><span class="sxs-lookup"><span data-stu-id="e8195-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="e8195-126">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="e8195-126">-EnablePartitioning</span></span>
<span data-ttu-id="e8195-127">Enablebölümlendirme özelliğinin etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8195-128">-Isanonymouserişilebilirlik</span><span class="sxs-lookup"><span data-stu-id="e8195-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="e8195-129">İletinin anonim olarak erişilebilir olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="e8195-130">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="e8195-130">-LockDuration</span></span>
<span data-ttu-id="e8195-131">Kilitleme süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="e8195-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="e8195-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="e8195-133">En fazla teslim sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="e8195-134">Bu numaradan sonra otomatik olarak bir ileti verilir.</span><span class="sxs-lookup"><span data-stu-id="e8195-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="e8195-135">-Maxsizeınmega</span><span class="sxs-lookup"><span data-stu-id="e8195-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="e8195-136">Sıra için ayrılan belleğin megabayt cinsinden megabayt cinsinden en büyük boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="e8195-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="e8195-137">-MessageCount</span></span>
<span data-ttu-id="e8195-138">Kuyruktaki iletilerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="e8195-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="e8195-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="e8195-140">Kuyruğun yinelenen saptamayı gerektirip gerektirmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="e8195-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="e8195-141">-RequiresSession</span></span>
<span data-ttu-id="e8195-142">Bu sıranın oturumları destekleyip desteklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8195-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="e8195-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="e8195-143">-SizeInBytes</span></span>
<span data-ttu-id="e8195-144">Sıranın bayt cinsinden boyutu.</span><span class="sxs-lookup"><span data-stu-id="e8195-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="e8195-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8195-145">-Confirm</span></span>
<span data-ttu-id="e8195-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8195-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8195-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8195-147">-WhatIf</span></span>
<span data-ttu-id="e8195-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8195-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8195-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8195-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8195-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8195-150">-DefaultProfile</span></span>
<span data-ttu-id="e8195-151">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8195-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8195-152">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8195-152">-Name</span></span>
<span data-ttu-id="e8195-153">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="e8195-153">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8195-154">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e8195-154">-Namespace</span></span>
<span data-ttu-id="e8195-155">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e8195-155">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8195-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8195-156">-ResourceGroupName</span></span>
<span data-ttu-id="e8195-157">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="e8195-157">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8195-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8195-158">CommonParameters</span></span>
<span data-ttu-id="e8195-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8195-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8195-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8195-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8195-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8195-161">INPUTS</span></span>

### <span data-ttu-id="e8195-162">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8195-162">-ResourceGroup</span></span>
 <span data-ttu-id="e8195-163">System. String</span><span class="sxs-lookup"><span data-stu-id="e8195-163">System.String</span></span>

### <span data-ttu-id="e8195-164">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e8195-164">-NamespaceName</span></span>
 <span data-ttu-id="e8195-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e8195-165">System.String</span></span>

### <span data-ttu-id="e8195-166">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="e8195-166">-QueueName</span></span>
 <span data-ttu-id="e8195-167">System. String</span><span class="sxs-lookup"><span data-stu-id="e8195-167">System.String</span></span>

### <span data-ttu-id="e8195-168">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="e8195-168">-EnablePartitioning</span></span>
 <span data-ttu-id="e8195-169">System. Boolean.</span><span class="sxs-lookup"><span data-stu-id="e8195-169">System.Boolean?</span></span>

## <span data-ttu-id="e8195-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8195-170">OUTPUTS</span></span>

### <span data-ttu-id="e8195-171">Microsoft. Azure. Commands. ServiceBus. model. QueueAttributes</span><span class="sxs-lookup"><span data-stu-id="e8195-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="e8195-172">Ad: SB-Queue_exampl1 konum: Batı US LockDuration: AccessedAt: Autodeleteonıdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:36: DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true DeadLetteringOnMessageExpiration: false EnableExpress: false Enablebölümlendirme: true ısanonymouseriþin: false MaxDeliveryCount: Maxsizeınmega: 16384 messagecount: CountDetails 1/20/2017 2:51:37</span><span class="sxs-lookup"><span data-stu-id="e8195-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="e8195-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8195-173">NOTES</span></span>

## <span data-ttu-id="e8195-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8195-174">RELATED LINKS</span></span>

