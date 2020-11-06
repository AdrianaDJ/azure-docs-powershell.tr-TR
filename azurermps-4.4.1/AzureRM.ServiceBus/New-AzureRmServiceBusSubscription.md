---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590627"
---
# <span data-ttu-id="72074-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="72074-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="72074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72074-102">SYNOPSIS</span></span>
<span data-ttu-id="72074-103">Belirtilen hizmet veri yolu konusu için abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72074-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72074-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72074-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72074-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72074-105">DESCRIPTION</span></span>
<span data-ttu-id="72074-106">**Yeni-AzureRmServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu konusuna yeni bir abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72074-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="72074-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72074-107">EXAMPLES</span></span>

### <span data-ttu-id="72074-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="72074-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="72074-109">`SB-TopicSubscription-Example1`Belirtilen hizmet veri yolu konusu için aboneliği oluşturur `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="72074-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="72074-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72074-110">PARAMETERS</span></span>

### <span data-ttu-id="72074-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="72074-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="72074-112">Aboneliğin otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72074-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="72074-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="72074-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="72074-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="72074-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="72074-115">Aboneliğin filtre değerlendirme özel durumları üzerinde eski harf desteği olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72074-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="72074-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="72074-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="72074-117">Bir iletinin süresi dolduğunda aboneliğin sahipsiz destek olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72074-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="72074-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="72074-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="72074-119">Sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="72074-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="72074-120">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="72074-120">-IsReadOnly</span></span>
<span data-ttu-id="72074-121">Varlık açıklamasının salt okunur olup olmadığını gösterir</span><span class="sxs-lookup"><span data-stu-id="72074-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="72074-122">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="72074-122">-LockDuration</span></span>
<span data-ttu-id="72074-123">Aboneliğin süresini kilitleme süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72074-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="72074-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="72074-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="72074-125">Maksimum teslimatlar sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72074-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="72074-126">Bu numaradan sonra otomatik olarak bir ileti verilir.</span><span class="sxs-lookup"><span data-stu-id="72074-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="72074-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="72074-127">-RequiresSession</span></span>
<span data-ttu-id="72074-128">Bir aboneliğin oturum kavramını destekleyip desteklemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72074-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="72074-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="72074-129">-Confirm</span></span>
<span data-ttu-id="72074-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72074-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72074-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72074-131">-WhatIf</span></span>
<span data-ttu-id="72074-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72074-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72074-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72074-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72074-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="72074-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="72074-135">Canlı değer için TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="72074-135">Timespan to live value.</span></span> <span data-ttu-id="72074-136">Bu, iletinin kullanım süresi dolduğunda, iletinin hizmet veri yoluna gönderildiği tarihten sonraki süredir.</span><span class="sxs-lookup"><span data-stu-id="72074-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="72074-137">Bu, bir iletide TimeToLive ayarlanmamışsa kullanılan varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="72074-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="72074-138">Standart = TimeSpan. Max ve Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="72074-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="72074-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72074-139">-DefaultProfile</span></span>
<span data-ttu-id="72074-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72074-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72074-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="72074-141">-Name</span></span>
<span data-ttu-id="72074-142">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="72074-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72074-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="72074-143">-Namespace</span></span>
<span data-ttu-id="72074-144">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="72074-144">Namespace Name.</span></span>

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

### <span data-ttu-id="72074-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72074-145">-ResourceGroupName</span></span>
<span data-ttu-id="72074-146">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="72074-146">The name of the resource group</span></span>

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

### <span data-ttu-id="72074-147">-Konu</span><span class="sxs-lookup"><span data-stu-id="72074-147">-Topic</span></span>
<span data-ttu-id="72074-148">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="72074-148">Topic Name.</span></span>

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

### <span data-ttu-id="72074-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72074-149">CommonParameters</span></span>
<span data-ttu-id="72074-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72074-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72074-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72074-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72074-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72074-152">INPUTS</span></span>

### <span data-ttu-id="72074-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72074-153">-ResourceGroup</span></span>
 <span data-ttu-id="72074-154">System. String</span><span class="sxs-lookup"><span data-stu-id="72074-154">System.String</span></span>
 

### <span data-ttu-id="72074-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="72074-155">-NamespaceName</span></span>
 <span data-ttu-id="72074-156">System. String</span><span class="sxs-lookup"><span data-stu-id="72074-156">System.String</span></span>
 

### <span data-ttu-id="72074-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="72074-157">-TopicName</span></span>
 <span data-ttu-id="72074-158">System. String</span><span class="sxs-lookup"><span data-stu-id="72074-158">System.String</span></span>
 

### <span data-ttu-id="72074-159">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="72074-159">-SubscriptionName</span></span>
 <span data-ttu-id="72074-160">System. String</span><span class="sxs-lookup"><span data-stu-id="72074-160">System.String</span></span>

## <span data-ttu-id="72074-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72074-161">OUTPUTS</span></span>

### <span data-ttu-id="72074-162">Microsoft. Azure. Commands. ServiceBus. model. Subscriptionöznitelikleri</span><span class="sxs-lookup"><span data-stu-id="72074-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="72074-163">Ad: SB-TopicSubscription-example1 konumu: Batı US AccessedAt: 1/20/2017 3:18:54 har Autodeleteıdle: 10675199.02:48:05.4775807 CountDetails: Microsoft. Azure. Management. ServiceBus. modeller. MessageCountDetails CreatedAt: 1/20/2017 3:18:52 ısdefaultmessagetimetolive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: true DeadLetteringOnMessageExpiration: false EnableBatchedOperations: true EntityAvailabilityStatus:. 1/20/2017 3:18:54 00:01:00</span><span class="sxs-lookup"><span data-stu-id="72074-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="72074-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72074-164">NOTES</span></span>

## <span data-ttu-id="72074-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72074-165">RELATED LINKS</span></span>

