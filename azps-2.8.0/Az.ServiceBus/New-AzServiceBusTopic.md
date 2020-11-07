---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
ms.openlocfilehash: 8fe78fff4d297233ee322b58c426099f160b2990
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932465"
---
# <span data-ttu-id="aec75-101">New-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="aec75-101">New-AzServiceBusTopic</span></span>

## <span data-ttu-id="aec75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aec75-102">SYNOPSIS</span></span>
<span data-ttu-id="aec75-103">Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aec75-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

## <span data-ttu-id="aec75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aec75-104">SYNTAX</span></span>

```
New-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aec75-105">DESCRIPTION</span></span>
<span data-ttu-id="aec75-106">**New-AzServiceBusTopic** cmdlet 'i, belirtilen hizmet veri yolu ad boşluğunda yeni bir Service Bus konusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aec75-106">The **New-AzServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="aec75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aec75-107">EXAMPLES</span></span>

### <span data-ttu-id="aec75-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aec75-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="aec75-109">`SB-Topic_exampl1`Belirtilen hizmet veri yolu ad boşluğunda yeni bir hizmet veri yolu konusu oluşturur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="aec75-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="aec75-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aec75-110">PARAMETERS</span></span>

### <span data-ttu-id="aec75-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="aec75-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="aec75-112">Konunun otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aec75-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="aec75-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="aec75-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="aec75-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="aec75-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="aec75-115">İleti hizmet veri yoluna gönderildiğinde, iletinin süresinin dolacağını belirten süreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="aec75-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="aec75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec75-116">-DefaultProfile</span></span>
<span data-ttu-id="aec75-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aec75-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aec75-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="aec75-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="aec75-119">Yinelenen saptama geçmişinin süresini tanımlayan [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) yapısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aec75-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="aec75-120">Varsayılan değer 10 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="aec75-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="aec75-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="aec75-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="aec75-122">Sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="aec75-122">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="aec75-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="aec75-123">-EnableExpress</span></span>
<span data-ttu-id="aec75-124">Hızlı varlıkların etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="aec75-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="aec75-125">Bir hızlı kuyruk, kalıcı depolama birimine yazmadan önce geçici olarak bellekte bir ileti tutar.</span><span class="sxs-lookup"><span data-stu-id="aec75-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="aec75-126">-Enablebölümlendirme</span><span class="sxs-lookup"><span data-stu-id="aec75-126">-EnablePartitioning</span></span>
<span data-ttu-id="aec75-127">Konunun birden çok ileti aracıları genelinde bölümlenmesi gerekip gerekmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aec75-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="aec75-128">-Maxsizeınmega</span><span class="sxs-lookup"><span data-stu-id="aec75-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="aec75-129">Konu için ayrılan belleğin boyutu olan megabayt cinsinden en büyük boyut.</span><span class="sxs-lookup"><span data-stu-id="aec75-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="aec75-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="aec75-130">-Name</span></span>
<span data-ttu-id="aec75-131">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="aec75-131">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec75-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aec75-132">-Namespace</span></span>
<span data-ttu-id="aec75-133">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="aec75-133">Namespace Name.</span></span>

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

### <span data-ttu-id="aec75-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="aec75-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="aec75-135">Konunun çoğaltma algılaması gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="aec75-135">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="aec75-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec75-136">-ResourceGroupName</span></span>
<span data-ttu-id="aec75-137">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="aec75-137">The name of the resource group</span></span>

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

### <span data-ttu-id="aec75-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="aec75-138">-SizeInBytes</span></span>
<span data-ttu-id="aec75-139">Başlığın bayt cinsinden boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aec75-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="aec75-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="aec75-140">-SupportOrdering</span></span>
<span data-ttu-id="aec75-141">Konunun sıralamayı destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="aec75-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="aec75-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="aec75-142">-Confirm</span></span>
<span data-ttu-id="aec75-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aec75-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec75-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec75-144">-WhatIf</span></span>
<span data-ttu-id="aec75-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aec75-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec75-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aec75-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec75-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec75-147">CommonParameters</span></span>
<span data-ttu-id="aec75-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aec75-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec75-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec75-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec75-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aec75-150">INPUTS</span></span>

### <span data-ttu-id="aec75-151">System. String</span><span class="sxs-lookup"><span data-stu-id="aec75-151">System.String</span></span>

### <span data-ttu-id="aec75-152">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="aec75-152">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="aec75-153">System. Nullable ' 1 [[System. Int64, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="aec75-153">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aec75-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aec75-154">OUTPUTS</span></span>

### <span data-ttu-id="aec75-155">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="aec75-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="aec75-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aec75-156">NOTES</span></span>

## <span data-ttu-id="aec75-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aec75-157">RELATED LINKS</span></span>
