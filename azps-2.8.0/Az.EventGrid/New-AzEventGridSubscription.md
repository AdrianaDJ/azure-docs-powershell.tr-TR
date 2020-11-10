---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 5aa5089520663d6679df44eae19bcfd322bbaff7
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395365"
---
# <span data-ttu-id="f3cff-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f3cff-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="f3cff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3cff-102">SYNOPSIS</span></span>
<span data-ttu-id="f3cff-103">Bir konuya, Azure kaynağına, Azure aboneliğine veya kaynak grubuna yeni bir Azure olay Kılavuzu olay aboneliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3cff-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="f3cff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3cff-104">SYNTAX</span></span>

### <span data-ttu-id="f3cff-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f3cff-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cff-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3cff-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cff-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3cff-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cff-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3cff-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cff-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3cff-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cff-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3cff-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3cff-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3cff-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3cff-112">EtkiAlanıA</span><span class="sxs-lookup"><span data-stu-id="f3cff-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3cff-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3cff-113">DESCRIPTION</span></span>
<span data-ttu-id="f3cff-114">Azure olay kılavuzu konusuna, desteklenen Azure kaynağına, Azure aboneliğine veya kaynak grubuna yeni bir etkinlik aboneliği oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f3cff-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="f3cff-115">Seçili Azure aboneliğine bir etkinlik aboneliği oluşturmak için olay aboneliği adını ve hedef uç noktasını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f3cff-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="f3cff-116">Bir kaynak grubuna olay aboneliği oluşturmak için, olay aboneliği adına ve hedef uç noktasına ek olarak kaynak grubu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f3cff-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="f3cff-117">Bir Azure olay kılavuzu konusuna olay aboneliği oluşturmak için, konu adını da belirtin.</span><span class="sxs-lookup"><span data-stu-id="f3cff-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="f3cff-118">Desteklenen bir Azure kaynağına olay aboneliği oluşturmak için, kaynağın tam kaynak KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="f3cff-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="f3cff-119">Desteklenen türlerin listesini görüntülemek için Get-AzEventGridTopicType cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f3cff-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="f3cff-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3cff-120">EXAMPLES</span></span>

### <span data-ttu-id="f3cff-121">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f3cff-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="f3cff-122">\` \` \` \` \` \` Web kancası hedef uç noktasına sahip Myresourcegroupname kaynak grubundaki bir Azure olay kılavuzu konusuna konu1 yeni bir etkinlik aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="f3cff-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="f3cff-123">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="f3cff-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="f3cff-124">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f3cff-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="f3cff-125">\` \` \` \` Web kancası hedef uç noktasıyla myresourcegroupname kaynak grubuna yeni bir olay aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="f3cff-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="f3cff-126">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="f3cff-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="f3cff-127">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="f3cff-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="f3cff-128">\` \` Seçili Azure aboneliğine Web kancası hedef uç noktasıyla yeni bir etkinlik aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="f3cff-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="f3cff-129">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="f3cff-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="f3cff-130">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="f3cff-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="f3cff-131">\` \` Seçili Azure aboneliğine Web kancası hedef uç noktasıyla yeni bir etkinlik aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="f3cff-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="f3cff-132">Bu olay aboneliği, olay türleri ve konu için ek filtreler belirtir ve yalnızca bu filtrelerle eşleşen olaylar hedef uç noktasına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="f3cff-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="f3cff-133">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="f3cff-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="f3cff-134">\` \` Seçili Azure aboneliği için, belirtilen olay hub 'ındaki olaylar için hedef olarak yeni bir etkinlik aboneliği EventSubscription1 oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3cff-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="f3cff-135">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="f3cff-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="f3cff-136">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="f3cff-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="f3cff-137">\` \` Belirtilen Web kancası hedef uç noktasına sahip bir EventHub ad alanına yeni bir etkinlik aboneliği EventSubscription1 oluşturur `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="f3cff-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="f3cff-138">Bu olay aboneliği varsayılan filtreleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="f3cff-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="f3cff-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3cff-139">PARAMETERS</span></span>

### <span data-ttu-id="f3cff-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="f3cff-140">-AdvancedFilter</span></span>
<span data-ttu-id="f3cff-141">Özniteliğe dayalı filtreleme için kullanılan birden çok Hashtable değerinin dizisini belirten gelişmiş filtre.</span><span class="sxs-lookup"><span data-stu-id="f3cff-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="f3cff-142">Her Hashtable değerinde aşağıdaki tuşlar-değer bilgileri: Işlem, anahtar ve değer veya değerler vardır.</span><span class="sxs-lookup"><span data-stu-id="f3cff-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="f3cff-143">İşleç aşağıdaki değerlerden biri olabilir: Numberın, Numbernotın, NumberLessThan, NumberGreaterThan, Numberlessiboiyals, NumberGreaterThanOrEquals, BoolEquals, Stringın, Stringnotın, StringEndsWith veya StringContains.</span><span class="sxs-lookup"><span data-stu-id="f3cff-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="f3cff-144">Anahtar, Gelişmiş filtreleme ilkelerinin uygulandığı yük özelliğini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f3cff-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="f3cff-145">Son olarak, değer veya değerler eşleştirilecek değeri veya değerleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f3cff-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="f3cff-146">Bu, ilgili türün veya bir değer dizisinin tek bir değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="f3cff-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="f3cff-147">Gelişmiş filtre parametrelerinin bir örneği olarak: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), burada $AdvFilter 1 = @ {operator = "Numberın"; Key = "Data. anahtar"; Değerler = @ (1, 2)} ve $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "Subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="f3cff-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-148">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3cff-148">-DeadLetterEndpoint</span></span>
<span data-ttu-id="f3cff-149">Teslim edilemeyen olayları depolamak için kullanılan uç nokta.</span><span class="sxs-lookup"><span data-stu-id="f3cff-149">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="f3cff-150">Depolama blob kapsayıcısının Azure Kaynak KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="f3cff-150">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="f3cff-151">Örneğin:/Subscriptions/[SubscriptionID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[Kapsayıcıadı].</span><span class="sxs-lookup"><span data-stu-id="f3cff-151">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3cff-152">-DefaultProfile</span></span>
<span data-ttu-id="f3cff-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f3cff-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3cff-154">-Domainınputobject</span><span class="sxs-lookup"><span data-stu-id="f3cff-154">-DomainInputObject</span></span>
<span data-ttu-id="f3cff-155">Olay Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="f3cff-155">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-156">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="f3cff-156">-DomainName</span></span>
<span data-ttu-id="f3cff-157">Olay aboneliğinin oluşturulması gereken olay Kılavuzu etki alanının adı.</span><span class="sxs-lookup"><span data-stu-id="f3cff-157">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-158">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="f3cff-158">-DomainTopicInputObject</span></span>
<span data-ttu-id="f3cff-159">EventGrid etki alanı konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f3cff-159">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-160">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="f3cff-160">-DomainTopicName</span></span>
<span data-ttu-id="f3cff-161">Olay aboneliğinin oluşturulması gereken etki alanı konusunun adı.</span><span class="sxs-lookup"><span data-stu-id="f3cff-161">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-162">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="f3cff-162">-Endpoint</span></span>
<span data-ttu-id="f3cff-163">Olay aboneliği hedef uç noktası.</span><span class="sxs-lookup"><span data-stu-id="f3cff-163">Event subscription destination endpoint.</span></span>
<span data-ttu-id="f3cff-164">Bu bir Web kancası URL 'si veya bir EventHub, depolama kuyruğu, hybridconnection veya servicebusqueue 'un Azure Resource ID 'si olabilir.</span><span class="sxs-lookup"><span data-stu-id="f3cff-164">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="f3cff-165">Örneğin, karma bağlantının kaynak KIMLIĞI şu şekilde olur:/Subscriptions/[Azure abonelik KIMLIĞI]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="f3cff-165">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="f3cff-166">Herhangi bir olay Kılavuzu cmdlet 'i yürütmeden önce hedef uç noktasının oluşturulması ve kullanılabilir olması beklenir.</span><span class="sxs-lookup"><span data-stu-id="f3cff-166">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-167">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="f3cff-167">-EndpointType</span></span>
<span data-ttu-id="f3cff-168">Uç nokta türü.</span><span class="sxs-lookup"><span data-stu-id="f3cff-168">Endpoint Type.</span></span>
<span data-ttu-id="f3cff-169">Bu, Web kancası, eventhub, storagequeue, hybridconnection veya servicebusqueue olabilir.</span><span class="sxs-lookup"><span data-stu-id="f3cff-169">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="f3cff-170">Varsayılan değer, Web kancası.</span><span class="sxs-lookup"><span data-stu-id="f3cff-170">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-171">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f3cff-171">-EventSubscriptionName</span></span>
<span data-ttu-id="f3cff-172">Olay aboneliğinin adı</span><span class="sxs-lookup"><span data-stu-id="f3cff-172">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-173">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="f3cff-173">-EventTtl</span></span>
<span data-ttu-id="f3cff-174">Olay teslimatı için dakika cinsinden süre.</span><span class="sxs-lookup"><span data-stu-id="f3cff-174">The time in minutes for the event delivery.</span></span> <span data-ttu-id="f3cff-175">Bu değer 1 ile 1440 arasında olmalıdır</span><span class="sxs-lookup"><span data-stu-id="f3cff-175">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-176">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="f3cff-176">-ExpirationDate</span></span>
<span data-ttu-id="f3cff-177">Hangi olay aboneliğinin devre dışı bırakılabilecek olay aboneliğinin süre sonu tarihini belirler.</span><span class="sxs-lookup"><span data-stu-id="f3cff-177">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-178">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="f3cff-178">-IncludedEventType</span></span>
<span data-ttu-id="f3cff-179">İçerilecek olay türlerinin listesini belirten filtre. Belirtilmezse, tüm olay türleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="f3cff-179">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3cff-180">-InputObject</span></span>
<span data-ttu-id="f3cff-181">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f3cff-181">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="f3cff-182">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f3cff-182">-Label</span></span>
<span data-ttu-id="f3cff-183">Olay aboneliği için Etiketler</span><span class="sxs-lookup"><span data-stu-id="f3cff-183">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-184">-Max, Yattempt</span><span class="sxs-lookup"><span data-stu-id="f3cff-184">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="f3cff-185">Olayı teslim etmek için en fazla deneme sayısı.</span><span class="sxs-lookup"><span data-stu-id="f3cff-185">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="f3cff-186">Bu değer 1 ile 30 arasında olmalıdır</span><span class="sxs-lookup"><span data-stu-id="f3cff-186">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-187">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3cff-187">-ResourceGroupName</span></span>
<span data-ttu-id="f3cff-188">Konunun kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f3cff-188">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-189">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f3cff-189">-ResourceId</span></span>
<span data-ttu-id="f3cff-190">Olay aboneliğinin oluşturulması gereken kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="f3cff-190">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="f3cff-191">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="f3cff-191">-SubjectBeginsWith</span></span>
<span data-ttu-id="f3cff-192">Yalnızca belirtilen konu önekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="f3cff-192">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="f3cff-193">Belirtilmezse, tüm konu önekleri olan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="f3cff-193">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-194">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="f3cff-194">-SubjectCaseSensitive</span></span>
<span data-ttu-id="f3cff-195">Konu alanının hassas bir şekilde karşılaştırılacağını belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="f3cff-195">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="f3cff-196">Belirtilmemişse, konu büyük/küçük harfe duyarlı olmayan şekilde karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="f3cff-196">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="f3cff-197">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="f3cff-197">-SubjectEndsWith</span></span>
<span data-ttu-id="f3cff-198">Yalnızca belirtilen konu sonekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="f3cff-198">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="f3cff-199">Belirtilmezse, tüm konu sonekleri bulunan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="f3cff-199">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cff-200">-TopicName</span><span class="sxs-lookup"><span data-stu-id="f3cff-200">-TopicName</span></span>
<span data-ttu-id="f3cff-201">Olay aboneliğinin oluşturulması gereken konunun adı.</span><span class="sxs-lookup"><span data-stu-id="f3cff-201">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="f3cff-202">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3cff-202">-Confirm</span></span>
<span data-ttu-id="f3cff-203">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3cff-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3cff-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3cff-204">-WhatIf</span></span>
<span data-ttu-id="f3cff-205">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3cff-205">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3cff-206">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3cff-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3cff-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3cff-207">CommonParameters</span></span>
<span data-ttu-id="f3cff-208">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3cff-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3cff-209">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3cff-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3cff-210">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3cff-210">INPUTS</span></span>

### <span data-ttu-id="f3cff-211">System. String</span><span class="sxs-lookup"><span data-stu-id="f3cff-211">System.String</span></span>

### <span data-ttu-id="f3cff-212">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="f3cff-212">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="f3cff-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="f3cff-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="f3cff-214">Microsoft.Azure.Commands.EventGrid.Models.PSDOmainkonu başlığı</span><span class="sxs-lookup"><span data-stu-id="f3cff-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="f3cff-215">System. String []</span><span class="sxs-lookup"><span data-stu-id="f3cff-215">System.String[]</span></span>

### <span data-ttu-id="f3cff-216">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f3cff-216">System.Int32</span></span>

## <span data-ttu-id="f3cff-217">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3cff-217">OUTPUTS</span></span>

### <span data-ttu-id="f3cff-218">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="f3cff-218">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="f3cff-219">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3cff-219">NOTES</span></span>

## <span data-ttu-id="f3cff-220">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3cff-220">RELATED LINKS</span></span>
