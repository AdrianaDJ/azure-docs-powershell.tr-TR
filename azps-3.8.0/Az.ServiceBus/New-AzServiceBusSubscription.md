---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096786"
---
# <span data-ttu-id="455b9-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="455b9-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="455b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="455b9-102">SYNOPSIS</span></span>
<span data-ttu-id="455b9-103">Belirtilen hizmet veri yolu konusu için abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="455b9-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="455b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="455b9-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="455b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="455b9-105">DESCRIPTION</span></span>
<span data-ttu-id="455b9-106">**New-AzServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu konusuna yeni bir abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="455b9-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="455b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="455b9-107">EXAMPLES</span></span>

### <span data-ttu-id="455b9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="455b9-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="455b9-109">`SB-TopicSubscription-Example1`Belirtilen hizmet veri yolu konusu için aboneliği oluşturur `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="455b9-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="455b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="455b9-110">PARAMETERS</span></span>

### <span data-ttu-id="455b9-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="455b9-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="455b9-112">Aboneliğin otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="455b9-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="455b9-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="455b9-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="455b9-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="455b9-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="455b9-115">Bir aboneliğin filtre değerlendirme özel durumları üzerinde atılacak mektup desteğinin bulunup bulunmadığını belirten değer.</span><span class="sxs-lookup"><span data-stu-id="455b9-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="455b9-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="455b9-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="455b9-117">Ileti süre sonu</span><span class="sxs-lookup"><span data-stu-id="455b9-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="455b9-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="455b9-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="455b9-119">Canlı değer için TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="455b9-119">Timespan to live value.</span></span>
<span data-ttu-id="455b9-120">Bu, iletinin kullanım süresi dolduğunda, iletinin hizmet veri yoluna gönderildiği tarihten sonraki süredir.</span><span class="sxs-lookup"><span data-stu-id="455b9-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="455b9-121">Bu, bir iletide TimeToLive ayarlanmamışsa kullanılan varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="455b9-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="455b9-122">Standart = TimeSpan. Max ve BASIC = 14 gün için</span><span class="sxs-lookup"><span data-stu-id="455b9-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="455b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="455b9-123">-DefaultProfile</span></span>
<span data-ttu-id="455b9-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="455b9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="455b9-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="455b9-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="455b9-126">Toplu Işlemleri etkinleştir-sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini belirten değer</span><span class="sxs-lookup"><span data-stu-id="455b9-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="455b9-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="455b9-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="455b9-128">Atılacak iletiyi iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="455b9-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="455b9-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="455b9-129">-ForwardTo</span></span>
<span data-ttu-id="455b9-130">İletileri iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="455b9-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="455b9-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="455b9-131">-LockDuration</span></span>
<span data-ttu-id="455b9-132">Kilitleme süresi</span><span class="sxs-lookup"><span data-stu-id="455b9-132">Lock Duration</span></span>

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

### <span data-ttu-id="455b9-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="455b9-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="455b9-134">MaxDeliveryCount-en fazla teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="455b9-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="455b9-135">Bu numaradan sonra otomatik olarak bir ileti verilir.</span><span class="sxs-lookup"><span data-stu-id="455b9-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="455b9-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="455b9-136">-Name</span></span>
<span data-ttu-id="455b9-137">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="455b9-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455b9-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="455b9-138">-Namespace</span></span>
<span data-ttu-id="455b9-139">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="455b9-139">Namespace Name</span></span>

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

### <span data-ttu-id="455b9-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="455b9-140">-RequiresSession</span></span>
<span data-ttu-id="455b9-141">RequiresSession-bu sıranın yinelenen algılama gerektirip gerektirmediğini belirten değer.</span><span class="sxs-lookup"><span data-stu-id="455b9-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="455b9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="455b9-142">-ResourceGroupName</span></span>
<span data-ttu-id="455b9-143">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="455b9-143">The name of the resource group</span></span>

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

### <span data-ttu-id="455b9-144">-Konu</span><span class="sxs-lookup"><span data-stu-id="455b9-144">-Topic</span></span>
<span data-ttu-id="455b9-145">Konu adı</span><span class="sxs-lookup"><span data-stu-id="455b9-145">Topic Name</span></span>

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

### <span data-ttu-id="455b9-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="455b9-146">-Confirm</span></span>
<span data-ttu-id="455b9-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="455b9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="455b9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="455b9-148">-WhatIf</span></span>
<span data-ttu-id="455b9-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="455b9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="455b9-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="455b9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="455b9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455b9-151">CommonParameters</span></span>
<span data-ttu-id="455b9-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="455b9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455b9-153">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="455b9-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455b9-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="455b9-154">INPUTS</span></span>

### <span data-ttu-id="455b9-155">System. String</span><span class="sxs-lookup"><span data-stu-id="455b9-155">System.String</span></span>

### <span data-ttu-id="455b9-156">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="455b9-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="455b9-157">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="455b9-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="455b9-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="455b9-158">OUTPUTS</span></span>

### <span data-ttu-id="455b9-159">Microsoft. Azure. Commands. ServiceBus. model. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="455b9-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="455b9-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="455b9-160">NOTES</span></span>

## <span data-ttu-id="455b9-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="455b9-161">RELATED LINKS</span></span>
