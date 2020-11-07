---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 54753001be0a754cf9416e1b2ec53fd81647d8d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763217"
---
# <span data-ttu-id="478fb-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="478fb-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="478fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="478fb-102">SYNOPSIS</span></span>
<span data-ttu-id="478fb-103">Belirtilen hizmet veri yolu konusu için abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="478fb-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="478fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="478fb-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="478fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="478fb-105">DESCRIPTION</span></span>
<span data-ttu-id="478fb-106">**Yeni-AzureRmServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu konusuna yeni bir abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="478fb-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="478fb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="478fb-107">EXAMPLES</span></span>

### <span data-ttu-id="478fb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="478fb-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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
<span data-ttu-id="478fb-109">`SB-TopicSubscription-Example1`Belirtilen hizmet veri yolu konusu için aboneliği oluşturur `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="478fb-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="478fb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="478fb-110">PARAMETERS</span></span>

### <span data-ttu-id="478fb-111">-Autodeleteonıdle</span><span class="sxs-lookup"><span data-stu-id="478fb-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="478fb-112">Aboneliğin otomatik olarak silineceği zaman [yayılımı](https://msdn.microsoft.com/library/system.timespan.aspx) boşta kalma aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="478fb-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="478fb-113">En az süre 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="478fb-113">The minimum duration is 5 minutes.</span></span>


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

### <span data-ttu-id="478fb-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="478fb-114">-Confirm</span></span>
<span data-ttu-id="478fb-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="478fb-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478fb-116">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="478fb-116">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="478fb-117">Bir aboneliğin filtre değerlendirme özel durumları üzerinde atılacak mektup desteğinin bulunup bulunmadığını belirten değer.</span><span class="sxs-lookup"><span data-stu-id="478fb-117">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="478fb-118">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="478fb-118">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="478fb-119">Ileti süre sonu</span><span class="sxs-lookup"><span data-stu-id="478fb-119">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="478fb-120">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="478fb-120">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="478fb-121">Canlı değer için TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="478fb-121">Timespan to live value.</span></span>
<span data-ttu-id="478fb-122">Bu, iletinin kullanım süresi dolduğunda, iletinin hizmet veri yoluna gönderildiği tarihten sonraki süredir.</span><span class="sxs-lookup"><span data-stu-id="478fb-122">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="478fb-123">Bu, bir iletide TimeToLive ayarlanmamışsa kullanılan varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="478fb-123">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="478fb-124">Standart = TimeSpan. Max ve Basic = 14 Dyas</span><span class="sxs-lookup"><span data-stu-id="478fb-124">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="478fb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478fb-125">-DefaultProfile</span></span>
<span data-ttu-id="478fb-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="478fb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="478fb-127">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="478fb-127">-EnableBatchedOperations</span></span>
<span data-ttu-id="478fb-128">Toplu Işlemleri etkinleştir-sunucu tarafı toplu işlemlerinin etkinleştirilip etkinleştirilmediğini belirten değer</span><span class="sxs-lookup"><span data-stu-id="478fb-128">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="478fb-129">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="478fb-129">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="478fb-130">Atılacak iletiyi iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="478fb-130">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="478fb-131">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="478fb-131">-ForwardTo</span></span>
<span data-ttu-id="478fb-132">İletileri iletmek için sıra/konu adı</span><span class="sxs-lookup"><span data-stu-id="478fb-132">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="478fb-133">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="478fb-133">-LockDuration</span></span>
<span data-ttu-id="478fb-134">Kilitleme süresi</span><span class="sxs-lookup"><span data-stu-id="478fb-134">Lock Duration</span></span>

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

### <span data-ttu-id="478fb-135">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="478fb-135">-MaxDeliveryCount</span></span>
<span data-ttu-id="478fb-136">MaxDeliveryCount-en fazla teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="478fb-136">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="478fb-137">Bu numaradan sonra otomatik olarak bir ileti verilir.</span><span class="sxs-lookup"><span data-stu-id="478fb-137">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="478fb-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="478fb-138">-Name</span></span>
<span data-ttu-id="478fb-139">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="478fb-139">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="478fb-140">-Namespace</span><span class="sxs-lookup"><span data-stu-id="478fb-140">-Namespace</span></span>
<span data-ttu-id="478fb-141">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="478fb-141">Namespace Name</span></span>

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

### <span data-ttu-id="478fb-142">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="478fb-142">-RequiresSession</span></span>
<span data-ttu-id="478fb-143">RequiresSession-bu sıranın yinelenen algılama gerektirip gerektirmediğini belirten değer.</span><span class="sxs-lookup"><span data-stu-id="478fb-143">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="478fb-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478fb-144">-ResourceGroupName</span></span>
<span data-ttu-id="478fb-145">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="478fb-145">The name of the resource group</span></span>

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

### <span data-ttu-id="478fb-146">-Konu</span><span class="sxs-lookup"><span data-stu-id="478fb-146">-Topic</span></span>
<span data-ttu-id="478fb-147">Konu adı</span><span class="sxs-lookup"><span data-stu-id="478fb-147">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="478fb-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478fb-148">-WhatIf</span></span>
<span data-ttu-id="478fb-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="478fb-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="478fb-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="478fb-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478fb-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478fb-151">CommonParameters</span></span>
<span data-ttu-id="478fb-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="478fb-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="478fb-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478fb-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478fb-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="478fb-154">INPUTS</span></span>

### <span data-ttu-id="478fb-155">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="478fb-155">-ResourceGroup</span></span>
 <span data-ttu-id="478fb-156">System. String</span><span class="sxs-lookup"><span data-stu-id="478fb-156">System.String</span></span>
 

### <span data-ttu-id="478fb-157">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="478fb-157">-NamespaceName</span></span>
 <span data-ttu-id="478fb-158">System. String</span><span class="sxs-lookup"><span data-stu-id="478fb-158">System.String</span></span>
 

### <span data-ttu-id="478fb-159">-TopicName</span><span class="sxs-lookup"><span data-stu-id="478fb-159">-TopicName</span></span>
 <span data-ttu-id="478fb-160">System. String</span><span class="sxs-lookup"><span data-stu-id="478fb-160">System.String</span></span>
 

### <span data-ttu-id="478fb-161">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="478fb-161">-SubscriptionName</span></span>
 <span data-ttu-id="478fb-162">System. String</span><span class="sxs-lookup"><span data-stu-id="478fb-162">System.String</span></span>


## <span data-ttu-id="478fb-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="478fb-163">OUTPUTS</span></span>

### <span data-ttu-id="478fb-164">Microsoft. Azure. Commands. ServiceBus. model. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="478fb-164">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>


## <span data-ttu-id="478fb-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="478fb-165">NOTES</span></span>

## <span data-ttu-id="478fb-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="478fb-166">RELATED LINKS</span></span>
