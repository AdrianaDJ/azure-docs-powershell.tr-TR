---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 2ed5d3345730e631b3f7668ca4b05f3decc04f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933230"
---
# <span data-ttu-id="7b835-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="7b835-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="7b835-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b835-102">SYNOPSIS</span></span>
<span data-ttu-id="7b835-103">Belirtilen hizmet veri yolu konusu için abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b835-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="7b835-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b835-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b835-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b835-105">DESCRIPTION</span></span>
<span data-ttu-id="7b835-106">**New-AzServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu konusuna yeni bir abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7b835-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="7b835-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b835-107">EXAMPLES</span></span>

### <span data-ttu-id="7b835-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7b835-108">Example 1</span></span>
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

<span data-ttu-id="7b835-109">`SB-TopicSubscription-Example1`Belirtilen hizmet veri yolu konusu için aboneliği oluşturur `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="7b835-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="7b835-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b835-110">PARAMETERS</span></span>

### <span data-ttu-id="7b835-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="7b835-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="7b835-112">Aboneliğin otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b835-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="7b835-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="7b835-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="7b835-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="7b835-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="7b835-115">Bir aboneliğin filtre değerlendirme özel durumları üzerinde atılacak mektup desteğinin bulunup bulunmadığını belirten değer.</span><span class="sxs-lookup"><span data-stu-id="7b835-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="7b835-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="7b835-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="7b835-117">Ileti süre sonu</span><span class="sxs-lookup"><span data-stu-id="7b835-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="7b835-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="7b835-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="7b835-119">Canlı değer için TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="7b835-119">Timespan to live value.</span></span>
<span data-ttu-id="7b835-120">Bu, iletinin kullanım süresi dolduğunda, iletinin hizmet veri yoluna gönderildiği tarihten sonraki süredir.</span><span class="sxs-lookup"><span data-stu-id="7b835-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="7b835-121">Bu, bir iletide TimeToLive ayarlanmamışsa kullanılan varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="7b835-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="7b835-122">Standart = TimeSpan. Max ve BASIC = 14 gün için</span><span class="sxs-lookup"><span data-stu-id="7b835-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="7b835-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b835-123">-DefaultProfile</span></span>
<span data-ttu-id="7b835-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b835-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b835-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="7b835-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="7b835-126">Toplu Işlemleri etkinleştir-sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini belirten değer</span><span class="sxs-lookup"><span data-stu-id="7b835-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="7b835-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="7b835-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="7b835-128">Atılacak iletiyi iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="7b835-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="7b835-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="7b835-129">-ForwardTo</span></span>
<span data-ttu-id="7b835-130">İletileri iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="7b835-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="7b835-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="7b835-131">-LockDuration</span></span>
<span data-ttu-id="7b835-132">Kilitleme süresi</span><span class="sxs-lookup"><span data-stu-id="7b835-132">Lock Duration</span></span>

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

### <span data-ttu-id="7b835-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="7b835-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="7b835-134">MaxDeliveryCount-en fazla teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="7b835-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="7b835-135">Bu numaradan sonra otomatik olarak bir ileti verilir.</span><span class="sxs-lookup"><span data-stu-id="7b835-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="7b835-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="7b835-136">-Name</span></span>
<span data-ttu-id="7b835-137">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="7b835-137">Subscription Name</span></span>

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

### <span data-ttu-id="7b835-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7b835-138">-Namespace</span></span>
<span data-ttu-id="7b835-139">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="7b835-139">Namespace Name</span></span>

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

### <span data-ttu-id="7b835-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="7b835-140">-RequiresSession</span></span>
<span data-ttu-id="7b835-141">RequiresSession-bu sıranın yinelenen algılama gerektirip gerektirmediğini belirten değer.</span><span class="sxs-lookup"><span data-stu-id="7b835-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="7b835-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b835-142">-ResourceGroupName</span></span>
<span data-ttu-id="7b835-143">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="7b835-143">The name of the resource group</span></span>

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

### <span data-ttu-id="7b835-144">-Konu</span><span class="sxs-lookup"><span data-stu-id="7b835-144">-Topic</span></span>
<span data-ttu-id="7b835-145">Konu adı</span><span class="sxs-lookup"><span data-stu-id="7b835-145">Topic Name</span></span>

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

### <span data-ttu-id="7b835-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b835-146">-Confirm</span></span>
<span data-ttu-id="7b835-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b835-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b835-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b835-148">-WhatIf</span></span>
<span data-ttu-id="7b835-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b835-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b835-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b835-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b835-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b835-151">CommonParameters</span></span>
<span data-ttu-id="7b835-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b835-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b835-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b835-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b835-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b835-154">INPUTS</span></span>

### <span data-ttu-id="7b835-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7b835-155">System.String</span></span>

### <span data-ttu-id="7b835-156">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="7b835-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7b835-157">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="7b835-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7b835-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b835-158">OUTPUTS</span></span>

### <span data-ttu-id="7b835-159">Microsoft. Azure. Commands. ServiceBus. model. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="7b835-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="7b835-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b835-160">NOTES</span></span>

## <span data-ttu-id="7b835-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b835-161">RELATED LINKS</span></span>