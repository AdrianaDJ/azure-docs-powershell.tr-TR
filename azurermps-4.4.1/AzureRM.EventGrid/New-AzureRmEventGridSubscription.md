---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: ed2855571ccd3ce10a8a41fd72f5e14fde7bba16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594731"
---
# <span data-ttu-id="2ac04-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2ac04-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="2ac04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac04-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac04-103">Bir konuya, Azure kaynağına, Azure aboneliğine veya kaynak grubuna yeni bir Azure olay Kılavuzu olay aboneliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2ac04-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ac04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ac04-104">SYNTAX</span></span>

### <span data-ttu-id="2ac04-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ac04-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac04-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ac04-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac04-107">Eventsubscriptionınputobjectset</span><span class="sxs-lookup"><span data-stu-id="2ac04-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ac04-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ac04-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac04-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ac04-109">DESCRIPTION</span></span>
<span data-ttu-id="2ac04-110">Azure olay kılavuzu konusuna, desteklenen Azure kaynağına, Azure aboneliğine veya kaynak grubuna yeni bir etkinlik aboneliği oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2ac04-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="2ac04-111">Seçili Azure aboneliğine bir etkinlik aboneliği oluşturmak için olay aboneliği adını ve hedef uç noktasını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2ac04-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="2ac04-112">Bir kaynak grubuna olay aboneliği oluşturmak için, olay aboneliği adına ve hedef uç noktasına ek olarak kaynak grubu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2ac04-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="2ac04-113">Bir Azure olay kılavuzu konusuna olay aboneliği oluşturmak için, konu adını da belirtin.</span><span class="sxs-lookup"><span data-stu-id="2ac04-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="2ac04-114">Desteklenen bir Azure kaynağına olay aboneliği oluşturmak için, kaynağın tam kaynak KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="2ac04-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="2ac04-115">Desteklenen türlerin listesini görüntülemek için Get-AzureRmEventGridTopicType cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2ac04-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="2ac04-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ac04-116">EXAMPLES</span></span>

### <span data-ttu-id="2ac04-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ac04-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2ac04-118">\` \` \` \` \` \` Web kancası hedef uç noktasına sahip Myresourcegroupname kaynak grubundaki bir Azure olay kılavuzu konusuna konu1 yeni bir etkinlik aboneliği EventSubscription1 oluşturur https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="2ac04-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="2ac04-119">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="2ac04-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="2ac04-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2ac04-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2ac04-121">\` \` \` \` Web kancası hedef uç noktasıyla myresourcegroupname kaynak grubuna yeni bir olay aboneliği EventSubscription1 oluşturur https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="2ac04-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="2ac04-122">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="2ac04-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="2ac04-123">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2ac04-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2ac04-124">\` \` Seçili Azure aboneliğine Web kancası hedef uç noktasıyla yeni bir etkinlik aboneliği EventSubscription1 oluşturur https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="2ac04-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="2ac04-125">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="2ac04-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="2ac04-126">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="2ac04-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="2ac04-127">\` \` Seçili Azure aboneliğine Web kancası hedef uç noktasıyla yeni bir etkinlik aboneliği EventSubscription1 oluşturur https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="2ac04-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="2ac04-128">Bu olay aboneliği, olay türleri ve konu için ek filtreler belirtir ve yalnızca bu filtrelerle eşleşen olaylar hedef uç noktasına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2ac04-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="2ac04-129">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="2ac04-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="2ac04-130">\` \` Seçili Azure aboneliği için, belirtilen olay hub 'ındaki olaylar için hedef olarak yeni bir etkinlik aboneliği EventSubscription1 oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2ac04-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="2ac04-131">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="2ac04-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="2ac04-132">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="2ac04-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2ac04-133">\` \` Belirtilen webhhtamam hedef uç noktasına sahip bir EventHub ad alanına yeni bir etkinlik aboneliği EventSubscription1 oluşturur https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="2ac04-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="2ac04-134">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="2ac04-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="2ac04-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ac04-135">PARAMETERS</span></span>

### <span data-ttu-id="2ac04-136">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="2ac04-136">-Endpoint</span></span>
<span data-ttu-id="2ac04-137">Olay aboneliği hedef uç noktası.</span><span class="sxs-lookup"><span data-stu-id="2ac04-137">Event subscription destination endpoint.</span></span>
<span data-ttu-id="2ac04-138">Bu, bir EventHub Web kancası URL 'SI veya Azure Resource ID olabilir.</span><span class="sxs-lookup"><span data-stu-id="2ac04-138">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-139">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="2ac04-139">-EndpointType</span></span>
<span data-ttu-id="2ac04-140">Uç nokta türü.</span><span class="sxs-lookup"><span data-stu-id="2ac04-140">Endpoint Type.</span></span>
<span data-ttu-id="2ac04-141">Bu, Web kancası veya eventhub olabilir</span><span class="sxs-lookup"><span data-stu-id="2ac04-141">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 
Accepted values: webhook, eventhub, webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-142">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2ac04-142">-EventSubscriptionName</span></span>
<span data-ttu-id="2ac04-143">Olay aboneliğinin adı</span><span class="sxs-lookup"><span data-stu-id="2ac04-143">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-144">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="2ac04-144">-IncludedEventType</span></span>
<span data-ttu-id="2ac04-145">İçerilecek olay türlerinin listesini belirten filtre. Belirtilmezse, tüm olay türleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="2ac04-145">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac04-146">-InputObject</span></span>
<span data-ttu-id="2ac04-147">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2ac04-147">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2ac04-148">-Label</span></span>
<span data-ttu-id="2ac04-149">Olay aboneliği için Etiketler</span><span class="sxs-lookup"><span data-stu-id="2ac04-149">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac04-150">-ResourceGroupName</span></span>
<span data-ttu-id="2ac04-151">Konunun kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="2ac04-151">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ac04-152">-ResourceId</span></span>
<span data-ttu-id="2ac04-153">Olay aboneliğinin oluşturulması gereken kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="2ac04-153">The identifier of the resource to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-154">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="2ac04-154">-SubjectBeginsWith</span></span>
<span data-ttu-id="2ac04-155">Yalnızca belirtilen konu önekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="2ac04-155">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="2ac04-156">Belirtilmezse, tüm konu önekleri olan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="2ac04-156">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-157">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="2ac04-157">-SubjectCaseSensitive</span></span>
<span data-ttu-id="2ac04-158">Konu alanının hassas bir şekilde karşılaştırılacağını belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="2ac04-158">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="2ac04-159">Belirtilmemişse, konu büyük/küçük harfe duyarlı olmayan şekilde karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="2ac04-159">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="2ac04-160">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="2ac04-160">-SubjectEndsWith</span></span>
<span data-ttu-id="2ac04-161">Yalnızca belirtilen konu sonekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="2ac04-161">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="2ac04-162">Belirtilmezse, tüm konu sonekleri bulunan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="2ac04-162">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-163">-TopicName</span><span class="sxs-lookup"><span data-stu-id="2ac04-163">-TopicName</span></span>
<span data-ttu-id="2ac04-164">Olay aboneliğinin oluşturulması gereken konunun adı.</span><span class="sxs-lookup"><span data-stu-id="2ac04-164">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac04-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ac04-165">-Confirm</span></span>
<span data-ttu-id="2ac04-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ac04-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ac04-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac04-167">-WhatIf</span></span>
<span data-ttu-id="2ac04-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ac04-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac04-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ac04-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ac04-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac04-170">-DefaultProfile</span></span>
<span data-ttu-id="2ac04-171">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ac04-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ac04-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac04-172">CommonParameters</span></span>
<span data-ttu-id="2ac04-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ac04-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac04-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac04-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac04-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ac04-175">INPUTS</span></span>

### <span data-ttu-id="2ac04-176">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac04-176">System.String</span></span>
<span data-ttu-id="2ac04-177">Microsoft. Azure. Commands. EventGrid. modeller. Pstopıc System. Management. Automation. SwitchParameter System. String []</span><span class="sxs-lookup"><span data-stu-id="2ac04-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic System.Management.Automation.SwitchParameter System.String[]</span></span>

## <span data-ttu-id="2ac04-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ac04-178">OUTPUTS</span></span>

### <span data-ttu-id="2ac04-179">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="2ac04-179">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="2ac04-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ac04-180">NOTES</span></span>

## <span data-ttu-id="2ac04-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ac04-181">RELATED LINKS</span></span>

