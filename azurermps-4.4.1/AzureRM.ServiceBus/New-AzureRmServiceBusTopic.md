---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: 099088bb560606990baa4f1774d8f46c5f68f04b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589117"
---
# <span data-ttu-id="63a2b-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="63a2b-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="63a2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="63a2b-103">Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="63a2b-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63a2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63a2b-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-EnableSubscriptionPartitioning <Boolean>]
 [-FilteringMessagesBeforePublishing <Boolean>] [-IsAnonymousAccessible <Boolean>] [-IsExpress <Boolean>]
 [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>] [-SupportOrdering <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63a2b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="63a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="63a2b-106">**Yeni-AzureRmServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="63a2b-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="63a2b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63a2b-107">EXAMPLES</span></span>

### <span data-ttu-id="63a2b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63a2b-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="63a2b-109">`SB-Topic_exampl1`Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu konusu oluşturur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="63a2b-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="63a2b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63a2b-110">PARAMETERS</span></span>

### <span data-ttu-id="63a2b-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="63a2b-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="63a2b-112">Konunun otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="63a2b-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="63a2b-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="63a2b-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="63a2b-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="63a2b-115">İleti hizmet veri yoluna gönderildiğinde, iletinin süresinin dolacağını belirten süreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="63a2b-116">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="63a2b-116">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="63a2b-117">Yinelenen saptama geçmişinin süresini tanımlayan [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) yapısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-117">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="63a2b-118">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="63a2b-118">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="63a2b-119">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="63a2b-119">-EnableBatchedOperations</span></span>
<span data-ttu-id="63a2b-120">Sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-120">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="63a2b-121">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="63a2b-121">-EnableExpress</span></span>
<span data-ttu-id="63a2b-122">Hızlı varlıkların etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-122">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="63a2b-123">Bir hızlı kuyruk, kalıcı depolama birimine yazmadan önce geçici olarak bellekte bir ileti tutar.</span><span class="sxs-lookup"><span data-stu-id="63a2b-123">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="63a2b-124">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="63a2b-124">-EnablePartitioning</span></span>
<span data-ttu-id="63a2b-125">Konunun birden çok ileti aracıları genelinde bölümlenmesi gerekip gerekmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-125">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="63a2b-126">-Enablesubscriptionbölümlendirme</span><span class="sxs-lookup"><span data-stu-id="63a2b-126">-EnableSubscriptionPartitioning</span></span>
<span data-ttu-id="63a2b-127">Abonelik bölümlemeyi etkinleştirip etkinleştirmeyeceğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="63a2b-127">Specifies whether to enable subscription partitioning.</span></span>

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

### <span data-ttu-id="63a2b-128">-Filteringiletibefoyeniden yayımlama</span><span class="sxs-lookup"><span data-stu-id="63a2b-128">-FilteringMessagesBeforePublishing</span></span>
<span data-ttu-id="63a2b-129">Yayımlamadan önce iletilerde filtreleme özelliğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-129">Indicates whether filtering is enabled for messages before publishing.</span></span>

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

### <span data-ttu-id="63a2b-130">-Isanonymouserişilebilirlik</span><span class="sxs-lookup"><span data-stu-id="63a2b-130">-IsAnonymousAccessible</span></span>
<span data-ttu-id="63a2b-131">İletinin anonim erişime izin verip vermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-131">Indicates whether the message allows anonymous access.</span></span>

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

### <span data-ttu-id="63a2b-132">-IsExpress</span><span class="sxs-lookup"><span data-stu-id="63a2b-132">-IsExpress</span></span>
<span data-ttu-id="63a2b-133">Konunun hızlı etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-133">Indicates whether the topic is express enabled.</span></span>

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

### <span data-ttu-id="63a2b-134">-Maxsizeınmega</span><span class="sxs-lookup"><span data-stu-id="63a2b-134">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="63a2b-135">Konu için ayrılan belleğin boyutu olan megabayt cinsinden en büyük boyut.</span><span class="sxs-lookup"><span data-stu-id="63a2b-135">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="63a2b-136">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="63a2b-136">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="63a2b-137">Konunun çoğaltma algılaması gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-137">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="63a2b-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="63a2b-138">-SizeInBytes</span></span>
<span data-ttu-id="63a2b-139">Başlığın bayt cinsinden boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="63a2b-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="63a2b-140">-SupportOrdering</span></span>
<span data-ttu-id="63a2b-141">Konunun sıralamayı destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="63a2b-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="63a2b-142">-Confirm</span></span>
<span data-ttu-id="63a2b-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63a2b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63a2b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63a2b-144">-WhatIf</span></span>
<span data-ttu-id="63a2b-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63a2b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63a2b-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63a2b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63a2b-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a2b-147">-DefaultProfile</span></span>
<span data-ttu-id="63a2b-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63a2b-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63a2b-149">-Ad</span><span class="sxs-lookup"><span data-stu-id="63a2b-149">-Name</span></span>
<span data-ttu-id="63a2b-150">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="63a2b-150">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63a2b-151">-Namespace</span><span class="sxs-lookup"><span data-stu-id="63a2b-151">-Namespace</span></span>
<span data-ttu-id="63a2b-152">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="63a2b-152">Namespace Name.</span></span>

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

### <span data-ttu-id="63a2b-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63a2b-153">-ResourceGroupName</span></span>
<span data-ttu-id="63a2b-154">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="63a2b-154">The name of the resource group</span></span>

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

### <span data-ttu-id="63a2b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a2b-155">CommonParameters</span></span>
<span data-ttu-id="63a2b-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63a2b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a2b-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63a2b-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a2b-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63a2b-158">INPUTS</span></span>

### <span data-ttu-id="63a2b-159">System. String</span><span class="sxs-lookup"><span data-stu-id="63a2b-159">System.String</span></span>
<span data-ttu-id="63a2b-160">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="63a2b-160">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="63a2b-161">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="63a2b-161">-ResourceGroup</span></span>
 <span data-ttu-id="63a2b-162">System. String</span><span class="sxs-lookup"><span data-stu-id="63a2b-162">System.String</span></span>

### <span data-ttu-id="63a2b-163">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="63a2b-163">-NamespaceName</span></span>
 <span data-ttu-id="63a2b-164">System. String</span><span class="sxs-lookup"><span data-stu-id="63a2b-164">System.String</span></span>

### <span data-ttu-id="63a2b-165">-TopicName</span><span class="sxs-lookup"><span data-stu-id="63a2b-165">-TopicName</span></span>
 <span data-ttu-id="63a2b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="63a2b-166">System.String</span></span>

### <span data-ttu-id="63a2b-167">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="63a2b-167">-EnablePartitioning</span></span>
 <span data-ttu-id="63a2b-168">System. Boolean.</span><span class="sxs-lookup"><span data-stu-id="63a2b-168">System.Boolean?</span></span>

## <span data-ttu-id="63a2b-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63a2b-169">OUTPUTS</span></span>

### <span data-ttu-id="63a2b-170">Microsoft. Azure. Commands. ServiceBus. model. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="63a2b-170">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="63a2b-171">Ad: SB-Topic_exampl1 konum: Batı ABD kimliği:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 tür: Microsoft. ServiceBus/topic AccessedAt: Autodeleteonıdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:42 har CountDetails: DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: enablebatchedoperations: true Enableexpress: false Enablebölümlendirme: true Enablesubscriptionbölümlendirme: false Esexpress: false Maxsizeınmega: 16384 requiresduplicatedetection: false (yanlış): 0 1/20/2017 3:16:43</span><span class="sxs-lookup"><span data-stu-id="63a2b-171">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:42 AM CountDetails                        : DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="63a2b-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63a2b-172">NOTES</span></span>

## <span data-ttu-id="63a2b-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63a2b-173">RELATED LINKS</span></span>

