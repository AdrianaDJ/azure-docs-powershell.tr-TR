---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 1c0391fa266e498c717bc4eb43bd92ab93be508f
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395195"
---
# <span data-ttu-id="86c96-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="86c96-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="86c96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86c96-102">SYNOPSIS</span></span>
<span data-ttu-id="86c96-103">Bir konuya, Azure kaynağına, Azure aboneliğine veya kaynak grubuna yeni bir Azure olay Kılavuzu olay aboneliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86c96-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="86c96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86c96-104">SYNTAX</span></span>

### <span data-ttu-id="86c96-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="86c96-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c96-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c96-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c96-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c96-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86c96-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="86c96-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c96-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="86c96-109">DESCRIPTION</span></span>
<span data-ttu-id="86c96-110">Azure olay kılavuzu konusuna, desteklenen Azure kaynağına, Azure aboneliğine veya kaynak grubuna yeni bir etkinlik aboneliği oluşturun.</span><span class="sxs-lookup"><span data-stu-id="86c96-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="86c96-111">Seçili Azure aboneliğine bir etkinlik aboneliği oluşturmak için olay aboneliği adını ve hedef uç noktasını belirtin.</span><span class="sxs-lookup"><span data-stu-id="86c96-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="86c96-112">Bir kaynak grubuna olay aboneliği oluşturmak için, olay aboneliği adına ve hedef uç noktasına ek olarak kaynak grubu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="86c96-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="86c96-113">Bir Azure olay kılavuzu konusuna olay aboneliği oluşturmak için, konu adını da belirtin.</span><span class="sxs-lookup"><span data-stu-id="86c96-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="86c96-114">Desteklenen bir Azure kaynağına olay aboneliği oluşturmak için, kaynağın tam kaynak KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="86c96-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="86c96-115">Desteklenen türlerin listesini görüntülemek için Get-AzEventGridTopicType cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="86c96-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="86c96-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86c96-116">EXAMPLES</span></span>

### <span data-ttu-id="86c96-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="86c96-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="86c96-118">\` \` \` \` \` \` Web kancası hedef uç noktasına sahip Myresourcegroupname kaynak grubundaki bir Azure olay kılavuzu konusuna konu1 yeni bir etkinlik aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86c96-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86c96-119">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="86c96-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="86c96-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="86c96-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="86c96-121">\` \` \` \` Web kancası hedef uç noktasıyla myresourcegroupname kaynak grubuna yeni bir olay aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86c96-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86c96-122">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="86c96-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="86c96-123">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="86c96-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="86c96-124">\` \` Seçili Azure aboneliğine Web kancası hedef uç noktasıyla yeni bir etkinlik aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86c96-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86c96-125">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="86c96-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="86c96-126">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="86c96-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="86c96-127">\` \` Seçili Azure aboneliğine Web kancası hedef uç noktasıyla yeni bir etkinlik aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86c96-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86c96-128">Bu olay aboneliği, olay türleri ve konu için ek filtreler belirtir ve yalnızca bu filtrelerle eşleşen olaylar hedef uç noktasına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="86c96-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="86c96-129">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="86c96-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="86c96-130">\` \` Seçili Azure aboneliği için, belirtilen olay hub 'ındaki olaylar için hedef olarak yeni bir etkinlik aboneliği EventSubscription1 oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86c96-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="86c96-131">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="86c96-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="86c96-132">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="86c96-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="86c96-133">\` \` Belirtilen Web kancası hedef uç noktasına sahip bir EventHub ad alanına yeni bir etkinlik aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="86c96-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="86c96-134">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="86c96-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="86c96-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86c96-135">PARAMETERS</span></span>

### <span data-ttu-id="86c96-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="86c96-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="86c96-137">Teslim edilemeyen olayları depolamak için kullanılan uç nokta.</span><span class="sxs-lookup"><span data-stu-id="86c96-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="86c96-138">Depolama blob kapsayıcısının Azure Kaynak KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="86c96-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="86c96-139">Örneğin:/Subscriptions/[SubscriptionID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[Kapsayıcıadı].</span><span class="sxs-lookup"><span data-stu-id="86c96-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c96-140">-DefaultProfile</span></span>
<span data-ttu-id="86c96-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="86c96-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86c96-142">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="86c96-142">-Endpoint</span></span>
<span data-ttu-id="86c96-143">Olay aboneliği hedef uç noktası.</span><span class="sxs-lookup"><span data-stu-id="86c96-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="86c96-144">Bu bir Web kancası URL 'SI veya bir EventHub, depolama sırası veya hybridconnection 'un Azure Kaynak KIMLIĞI olabilir.</span><span class="sxs-lookup"><span data-stu-id="86c96-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="86c96-145">Örneğin, karma bağlantının kaynak KIMLIĞI şu şekilde olur:/Subscriptions/[Azure abonelik KIMLIĞI]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="86c96-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="86c96-146">Herhangi bir olay Kılavuzu cmdlet 'i yürütmeden önce hedef uç noktasının oluşturulması ve kullanılabilir olması beklenir.</span><span class="sxs-lookup"><span data-stu-id="86c96-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="86c96-147">-EndpointType</span></span>
<span data-ttu-id="86c96-148">Uç nokta türü.</span><span class="sxs-lookup"><span data-stu-id="86c96-148">Endpoint Type.</span></span>
<span data-ttu-id="86c96-149">Bu, Web kancası, eventhub, storagequeue veya hybridconnection olabilir.</span><span class="sxs-lookup"><span data-stu-id="86c96-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="86c96-150">Varsayılan değer, Web kancası.</span><span class="sxs-lookup"><span data-stu-id="86c96-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="86c96-151">-EventSubscriptionName</span></span>
<span data-ttu-id="86c96-152">Olay aboneliğinin adı</span><span class="sxs-lookup"><span data-stu-id="86c96-152">The name of the event subscription</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="86c96-153">-EventTtl</span></span>
<span data-ttu-id="86c96-154">Olay teslimatı için dakika cinsinden süre.</span><span class="sxs-lookup"><span data-stu-id="86c96-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="86c96-155">Bu değer 1 ile 1440 arasında olmalıdır</span><span class="sxs-lookup"><span data-stu-id="86c96-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="86c96-156">-IncludedEventType</span></span>
<span data-ttu-id="86c96-157">İçerilecek olay türlerinin listesini belirten filtre. Belirtilmezse, tüm olay türleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="86c96-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86c96-158">-InputObject</span></span>
<span data-ttu-id="86c96-159">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="86c96-159">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-160">Etiketli</span><span class="sxs-lookup"><span data-stu-id="86c96-160">-Label</span></span>
<span data-ttu-id="86c96-161">Olay aboneliği için Etiketler</span><span class="sxs-lookup"><span data-stu-id="86c96-161">Labels for the event subscription</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-162">-Max, Yattempt</span><span class="sxs-lookup"><span data-stu-id="86c96-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="86c96-163">Olayı teslim etmek için en fazla deneme sayısı.</span><span class="sxs-lookup"><span data-stu-id="86c96-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="86c96-164">Bu değer 1 ile 30 arasında olmalıdır</span><span class="sxs-lookup"><span data-stu-id="86c96-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c96-165">-ResourceGroupName</span></span>
<span data-ttu-id="86c96-166">Konunun kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="86c96-166">The resource group of the topic.</span></span>

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

### <span data-ttu-id="86c96-167">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="86c96-167">-ResourceId</span></span>
<span data-ttu-id="86c96-168">Olay aboneliğinin oluşturulması gereken kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="86c96-168">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="86c96-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="86c96-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="86c96-170">Yalnızca belirtilen konu önekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="86c96-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="86c96-171">Belirtilmezse, tüm konu önekleri olan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="86c96-171">If not specified, events with all subject prefixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-172">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="86c96-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="86c96-173">Konu alanının hassas bir şekilde karşılaştırılacağını belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="86c96-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="86c96-174">Belirtilmemişse, konu büyük/küçük harfe duyarlı olmayan şekilde karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="86c96-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="86c96-175">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="86c96-175">-SubjectEndsWith</span></span>
<span data-ttu-id="86c96-176">Yalnızca belirtilen konu sonekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="86c96-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="86c96-177">Belirtilmezse, tüm konu sonekleri bulunan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="86c96-177">If not specified, events with all subject suffixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c96-178">-TopicName</span><span class="sxs-lookup"><span data-stu-id="86c96-178">-TopicName</span></span>
<span data-ttu-id="86c96-179">Olay aboneliğinin oluşturulması gereken konunun adı.</span><span class="sxs-lookup"><span data-stu-id="86c96-179">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="86c96-180">-Onay</span><span class="sxs-lookup"><span data-stu-id="86c96-180">-Confirm</span></span>
<span data-ttu-id="86c96-181">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="86c96-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86c96-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c96-182">-WhatIf</span></span>
<span data-ttu-id="86c96-183">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86c96-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86c96-184">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="86c96-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86c96-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c96-185">CommonParameters</span></span>
<span data-ttu-id="86c96-186">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86c96-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c96-187">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c96-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c96-188">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86c96-188">INPUTS</span></span>

### <span data-ttu-id="86c96-189">System. String</span><span class="sxs-lookup"><span data-stu-id="86c96-189">System.String</span></span>

### <span data-ttu-id="86c96-190">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="86c96-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="86c96-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="86c96-191">System.String[]</span></span>

## <span data-ttu-id="86c96-192">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86c96-192">OUTPUTS</span></span>

### <span data-ttu-id="86c96-193">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="86c96-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="86c96-194">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86c96-194">NOTES</span></span>

## <span data-ttu-id="86c96-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86c96-195">RELATED LINKS</span></span>
