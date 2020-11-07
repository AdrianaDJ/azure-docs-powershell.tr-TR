---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: a79afdbba1293c3340e499387b5df745d8b76228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762838"
---
# <span data-ttu-id="61a74-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="61a74-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="61a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61a74-102">SYNOPSIS</span></span>
<span data-ttu-id="61a74-103">Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61a74-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61a74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61a74-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61a74-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61a74-105">DESCRIPTION</span></span>
<span data-ttu-id="61a74-106">**Yeni-AzureRmServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61a74-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="61a74-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61a74-107">EXAMPLES</span></span>

### <span data-ttu-id="61a74-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="61a74-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:42 AM
CountDetails                        : 
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM

```
<span data-ttu-id="61a74-109">`SB-Topic_exampl1`Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu konusu oluşturur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="61a74-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="61a74-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61a74-110">PARAMETERS</span></span>

### <span data-ttu-id="61a74-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="61a74-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="61a74-112">Konunun otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61a74-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="61a74-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="61a74-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="61a74-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="61a74-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="61a74-115">İleti hizmet veri yoluna gönderildiğinde, iletinin süresinin dolacağını belirten süreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="61a74-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="61a74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a74-116">-DefaultProfile</span></span>
<span data-ttu-id="61a74-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61a74-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61a74-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="61a74-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="61a74-119">Yinelenen saptama geçmişinin süresini tanımlayan [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) yapısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61a74-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="61a74-120">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="61a74-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="61a74-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="61a74-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="61a74-122">Sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61a74-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="61a74-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="61a74-123">-EnableExpress</span></span>
<span data-ttu-id="61a74-124">Hızlı varlıkların etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61a74-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="61a74-125">Bir hızlı kuyruk, kalıcı depolama birimine yazmadan önce geçici olarak bellekte bir ileti tutar.</span><span class="sxs-lookup"><span data-stu-id="61a74-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="61a74-126">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="61a74-126">-EnablePartitioning</span></span>
<span data-ttu-id="61a74-127">Konunun birden çok ileti aracıları genelinde bölümlenmesi gerekip gerekmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61a74-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61a74-128">-Maxsizeınmega</span><span class="sxs-lookup"><span data-stu-id="61a74-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="61a74-129">Konu için ayrılan belleğin boyutu olan megabayt cinsinden en büyük boyut.</span><span class="sxs-lookup"><span data-stu-id="61a74-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="61a74-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="61a74-130">-Name</span></span>
<span data-ttu-id="61a74-131">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="61a74-131">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61a74-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="61a74-132">-Namespace</span></span>
<span data-ttu-id="61a74-133">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="61a74-133">Namespace Name.</span></span>

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

### <span data-ttu-id="61a74-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="61a74-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="61a74-135">Konunun çoğaltma algılaması gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61a74-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="61a74-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a74-136">-ResourceGroupName</span></span>
<span data-ttu-id="61a74-137">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="61a74-137">The name of the resource group</span></span>

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

### <span data-ttu-id="61a74-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="61a74-138">-SizeInBytes</span></span>
<span data-ttu-id="61a74-139">Başlığın bayt cinsinden boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61a74-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="61a74-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="61a74-140">-SupportOrdering</span></span>
<span data-ttu-id="61a74-141">Konunun sıralamayı destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61a74-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="61a74-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="61a74-142">-Confirm</span></span>
<span data-ttu-id="61a74-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61a74-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a74-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a74-144">-WhatIf</span></span>
<span data-ttu-id="61a74-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61a74-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a74-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61a74-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61a74-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a74-147">CommonParameters</span></span>
<span data-ttu-id="61a74-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61a74-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a74-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a74-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a74-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61a74-150">INPUTS</span></span>

### <span data-ttu-id="61a74-151">System. String</span><span class="sxs-lookup"><span data-stu-id="61a74-151">System.String</span></span>
<span data-ttu-id="61a74-152">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="61a74-152">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="61a74-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="61a74-153">-ResourceGroup</span></span>
 <span data-ttu-id="61a74-154">System. String</span><span class="sxs-lookup"><span data-stu-id="61a74-154">System.String</span></span>

### <span data-ttu-id="61a74-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="61a74-155">-NamespaceName</span></span>
 <span data-ttu-id="61a74-156">System. String</span><span class="sxs-lookup"><span data-stu-id="61a74-156">System.String</span></span>

### <span data-ttu-id="61a74-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="61a74-157">-TopicName</span></span>
 <span data-ttu-id="61a74-158">System. String</span><span class="sxs-lookup"><span data-stu-id="61a74-158">System.String</span></span>

### <span data-ttu-id="61a74-159">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="61a74-159">-EnablePartitioning</span></span>
 <span data-ttu-id="61a74-160">System. Boolean.</span><span class="sxs-lookup"><span data-stu-id="61a74-160">System.Boolean?</span></span>

## <span data-ttu-id="61a74-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61a74-161">OUTPUTS</span></span>

### <span data-ttu-id="61a74-162">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="61a74-162">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="61a74-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61a74-163">NOTES</span></span>

## <span data-ttu-id="61a74-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61a74-164">RELATED LINKS</span></span>

