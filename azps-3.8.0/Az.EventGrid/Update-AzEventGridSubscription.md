---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: d4967dd45cc420035a4be60736389729d019fd45
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096408"
---
# <span data-ttu-id="33551-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="33551-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="33551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33551-102">SYNOPSIS</span></span>
<span data-ttu-id="33551-103">Olay Kılavuzu olay aboneliğinin özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="33551-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="33551-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33551-104">SYNTAX</span></span>

### <span data-ttu-id="33551-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="33551-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33551-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="33551-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33551-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33551-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33551-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="33551-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33551-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="33551-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33551-110">EtkiAlanıA</span><span class="sxs-lookup"><span data-stu-id="33551-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33551-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="33551-111">DESCRIPTION</span></span>
<span data-ttu-id="33551-112">Olay Kılavuzu olay aboneliğinin özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="33551-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="33551-113">Bu, var olan bir olay aboneliğinin filtresini, hedefini veya etiketlerini güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="33551-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="33551-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33551-114">EXAMPLES</span></span>

### <span data-ttu-id="33551-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="33551-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="33551-116">\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 \` \` ES1\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="33551-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="33551-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="33551-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="33551-118">\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 \` \` ES1\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="33551-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="33551-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="33551-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="33551-120">\` \` Yeni uç nokta olarak, EventHub ad alanı ContosoNamespace için olay aboneliği ES1 özelliklerini \` https://requestb.in/1kxxoui1\ ve yeni subjectendswith \` jpg olarak güncelleştirir\`</span><span class="sxs-lookup"><span data-stu-id="33551-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="33551-121">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="33551-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="33551-122">\` \` \` Yeni Etiketler $Labels myresourcegroupname kaynak grubu için olay aboneliği ES1 özelliklerini güncelleştirir \` .</span><span class="sxs-lookup"><span data-stu-id="33551-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="33551-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33551-123">PARAMETERS</span></span>

### <span data-ttu-id="33551-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="33551-124">-AdvancedFilter</span></span>
<span data-ttu-id="33551-125">Özniteliğe dayalı filtreleme için kullanılan birden çok Hashtable değerinin dizisini belirten gelişmiş filtre.</span><span class="sxs-lookup"><span data-stu-id="33551-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="33551-126">Her Hashtable değerinde aşağıdaki tuşlar-değer bilgileri: Işlem, anahtar ve değer veya değerler vardır.</span><span class="sxs-lookup"><span data-stu-id="33551-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="33551-127">İşleç aşağıdaki değerlerden biri olabilir: Numberın, Numbernotın, NumberLessThan, NumberGreaterThan, Numberlessiboiyals, NumberGreaterThanOrEquals, BoolEquals, Stringın, Stringnotın, StringEndsWith veya StringContains.</span><span class="sxs-lookup"><span data-stu-id="33551-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="33551-128">Anahtar, Gelişmiş filtreleme ilkelerinin uygulandığı yük özelliğini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="33551-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="33551-129">Son olarak, değer veya değerler eşleştirilecek değeri veya değerleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="33551-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="33551-130">Bu, ilgili türün veya bir değer dizisinin tek bir değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="33551-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="33551-131">Gelişmiş filtre parametrelerinin bir örneği olarak: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), burada $AdvFilter 1 = @ {operator = "Numberın"; Key = "Data. anahtar"; Değerler = @ (1, 2)} ve $AdvFilter 2 = @ {operator = "StringBringsWith"; Key = "Subject"; Values = @ ("SubjectPrefix1", "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="33551-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="33551-132">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="33551-132">-DeadLetterEndpoint</span></span>
<span data-ttu-id="33551-133">Teslim edilemeyen olayları depolamak için kullanılan uç nokta.</span><span class="sxs-lookup"><span data-stu-id="33551-133">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="33551-134">Depolama blob kapsayıcısının Azure Kaynak KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="33551-134">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="33551-135">Örneğin:/Subscriptions/[SubscriptionID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[Kapsayıcıadı].</span><span class="sxs-lookup"><span data-stu-id="33551-135">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33551-136">-DefaultProfile</span></span>
<span data-ttu-id="33551-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33551-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33551-138">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="33551-138">-DomainName</span></span>
<span data-ttu-id="33551-139">Olay aboneliğinin oluşturulması gereken etki alanının adı.</span><span class="sxs-lookup"><span data-stu-id="33551-139">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33551-140">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="33551-140">-DomainTopicName</span></span>
<span data-ttu-id="33551-141">Olay aboneliğinin oluşturulması gereken etki alanı konusunun adı.</span><span class="sxs-lookup"><span data-stu-id="33551-141">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33551-142">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="33551-142">-Endpoint</span></span>
<span data-ttu-id="33551-143">Olay aboneliği hedef uç noktası.</span><span class="sxs-lookup"><span data-stu-id="33551-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="33551-144">Bu bir Web kancası URL 'si veya bir EventHub, depolama kuyruğu, hybridconnection veya servicebusqueue 'un Azure Resource ID 'si olabilir.</span><span class="sxs-lookup"><span data-stu-id="33551-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="33551-145">Örneğin, karma bağlantının kaynak KIMLIĞI şu şekilde olur:/Subscriptions/[Azure abonelik KIMLIĞI]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="33551-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="33551-146">Herhangi bir olay Kılavuzu cmdlet 'i yürütmeden önce hedef uç noktasının oluşturulması ve kullanılabilir olması beklenir.</span><span class="sxs-lookup"><span data-stu-id="33551-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="33551-147">-EndpointType</span></span>
<span data-ttu-id="33551-148">Uç nokta türü.</span><span class="sxs-lookup"><span data-stu-id="33551-148">Endpoint Type.</span></span>
<span data-ttu-id="33551-149">Bu, Web kancası, eventhub, storagequeue, hybridconnection veya servicebusqueue olabilir.</span><span class="sxs-lookup"><span data-stu-id="33551-149">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="33551-150">Varsayılan değer, Web kancası.</span><span class="sxs-lookup"><span data-stu-id="33551-150">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="33551-151">-EventSubscriptionName</span></span>
<span data-ttu-id="33551-152">Olay aboneliğinin adı</span><span class="sxs-lookup"><span data-stu-id="33551-152">The name of the event subscription</span></span>

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

### <span data-ttu-id="33551-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="33551-153">-EventTtl</span></span>
<span data-ttu-id="33551-154">Olay teslimatı için dakika cinsinden süre.</span><span class="sxs-lookup"><span data-stu-id="33551-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="33551-155">Bu değer 1 ile 1440 arasında olmalıdır</span><span class="sxs-lookup"><span data-stu-id="33551-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-156">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="33551-156">-ExpirationDate</span></span>
<span data-ttu-id="33551-157">Hangi olay aboneliğinin devre dışı bırakılabilecek olay aboneliğinin süre sonu tarihini belirler.</span><span class="sxs-lookup"><span data-stu-id="33551-157">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="33551-158">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="33551-158">-IncludedEventType</span></span>
<span data-ttu-id="33551-159">İçerilecek olay türlerinin listesini belirten filtre. Belirtilmezse, tüm olay türleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="33551-159">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-160">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33551-160">-InputObject</span></span>
<span data-ttu-id="33551-161">EventGridSubscription nesnesi.</span><span class="sxs-lookup"><span data-stu-id="33551-161">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33551-162">Etiketli</span><span class="sxs-lookup"><span data-stu-id="33551-162">-Label</span></span>
<span data-ttu-id="33551-163">Olay aboneliği için Etiketler</span><span class="sxs-lookup"><span data-stu-id="33551-163">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-164">-Max, Yattempt</span><span class="sxs-lookup"><span data-stu-id="33551-164">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="33551-165">Olayı teslim etmek için en fazla deneme sayısı.</span><span class="sxs-lookup"><span data-stu-id="33551-165">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="33551-166">Bu değer 1 ile 30 arasında olmalıdır</span><span class="sxs-lookup"><span data-stu-id="33551-166">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33551-167">-ResourceGroupName</span></span>
<span data-ttu-id="33551-168">Konunun kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="33551-168">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33551-169">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="33551-169">-ResourceId</span></span>
<span data-ttu-id="33551-170">Olay aboneliğinin oluşturulduğu kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="33551-170">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="33551-171">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="33551-171">-SubjectBeginsWith</span></span>
<span data-ttu-id="33551-172">Yalnızca belirtilen konu önekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="33551-172">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="33551-173">Belirtilmezse, tüm konu önekleri olan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="33551-173">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-174">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="33551-174">-SubjectEndsWith</span></span>
<span data-ttu-id="33551-175">Yalnızca belirtilen konu sonekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="33551-175">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="33551-176">Belirtilmezse, tüm konu sonekleri bulunan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="33551-176">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33551-177">-TopicName</span><span class="sxs-lookup"><span data-stu-id="33551-177">-TopicName</span></span>
<span data-ttu-id="33551-178">Olay aboneliğinin oluşturulması gereken konunun adı.</span><span class="sxs-lookup"><span data-stu-id="33551-178">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33551-179">-Onay</span><span class="sxs-lookup"><span data-stu-id="33551-179">-Confirm</span></span>
<span data-ttu-id="33551-180">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="33551-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33551-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33551-181">-WhatIf</span></span>
<span data-ttu-id="33551-182">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="33551-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33551-183">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="33551-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33551-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33551-184">CommonParameters</span></span>
<span data-ttu-id="33551-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33551-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33551-186">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33551-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33551-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33551-187">INPUTS</span></span>

### <span data-ttu-id="33551-188">System. String</span><span class="sxs-lookup"><span data-stu-id="33551-188">System.String</span></span>

### <span data-ttu-id="33551-189">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="33551-189">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="33551-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33551-190">OUTPUTS</span></span>

### <span data-ttu-id="33551-191">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="33551-191">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="33551-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33551-192">NOTES</span></span>

## <span data-ttu-id="33551-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33551-193">RELATED LINKS</span></span>
