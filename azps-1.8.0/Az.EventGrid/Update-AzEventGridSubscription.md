---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: a5aee2c8df132a4218ece171453e04d1224f7adc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760862"
---
# <span data-ttu-id="e8647-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e8647-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="e8647-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8647-102">SYNOPSIS</span></span>
<span data-ttu-id="e8647-103">Olay Kılavuzu olay aboneliğinin özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e8647-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="e8647-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8647-104">SYNTAX</span></span>

### <span data-ttu-id="e8647-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8647-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8647-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8647-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8647-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8647-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8647-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8647-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8647-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8647-109">DESCRIPTION</span></span>
<span data-ttu-id="e8647-110">Olay Kılavuzu olay aboneliğinin özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e8647-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="e8647-111">Bu, var olan bir olay aboneliğinin filtresini, hedefini veya etiketlerini güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e8647-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="e8647-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8647-112">EXAMPLES</span></span>

### <span data-ttu-id="e8647-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e8647-113">Example 1</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="e8647-114">\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 \` \` ES1\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="e8647-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="e8647-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e8647-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="e8647-116">\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 \` \` ES1\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="e8647-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="e8647-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e8647-117">Example 3</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="e8647-118">\` \` Yeni uç nokta olarak, EventHub ad alanı ContosoNamespace için olay aboneliği ES1 özelliklerini \` https://requestb.in/1kxxoui1\ ve yeni subjectendswith \` jpg olarak güncelleştirir\`</span><span class="sxs-lookup"><span data-stu-id="e8647-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="e8647-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="e8647-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="e8647-120">\` \` \` Yeni Etiketler $Labels myresourcegroupname kaynak grubu için olay aboneliği ES1 özelliklerini güncelleştirir \` .</span><span class="sxs-lookup"><span data-stu-id="e8647-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="e8647-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8647-121">PARAMETERS</span></span>

### <span data-ttu-id="e8647-122">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8647-122">-DeadLetterEndpoint</span></span>
<span data-ttu-id="e8647-123">Teslim edilemeyen olayları depolamak için kullanılan uç nokta.</span><span class="sxs-lookup"><span data-stu-id="e8647-123">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="e8647-124">Depolama blob kapsayıcısının Azure Kaynak KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="e8647-124">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="e8647-125">Örneğin:/Subscriptions/[SubscriptionID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[Kapsayıcıadı].</span><span class="sxs-lookup"><span data-stu-id="e8647-125">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="e8647-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8647-126">-DefaultProfile</span></span>
<span data-ttu-id="e8647-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8647-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8647-128">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="e8647-128">-Endpoint</span></span>
<span data-ttu-id="e8647-129">Olay aboneliği hedef uç noktası.</span><span class="sxs-lookup"><span data-stu-id="e8647-129">Event subscription destination endpoint.</span></span>
<span data-ttu-id="e8647-130">Bu bir Web kancası URL 'SI veya bir EventHub, depolama sırası veya hybridconnection 'un Azure Kaynak KIMLIĞI olabilir.</span><span class="sxs-lookup"><span data-stu-id="e8647-130">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="e8647-131">Örneğin, karma bağlantının kaynak KIMLIĞI şu şekilde olur:/Subscriptions/[Azure abonelik KIMLIĞI]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="e8647-131">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="e8647-132">Herhangi bir olay Kılavuzu cmdlet 'i yürütmeden önce hedef uç noktasının oluşturulması ve kullanılabilir olması beklenir.</span><span class="sxs-lookup"><span data-stu-id="e8647-132">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="e8647-133">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="e8647-133">-EndpointType</span></span>
<span data-ttu-id="e8647-134">Uç nokta türü.</span><span class="sxs-lookup"><span data-stu-id="e8647-134">Endpoint Type.</span></span>
<span data-ttu-id="e8647-135">Bu, Web kancası, eventhub, storagequeue veya hybridconnection olabilir.</span><span class="sxs-lookup"><span data-stu-id="e8647-135">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="e8647-136">Varsayılan değer, Web kancası.</span><span class="sxs-lookup"><span data-stu-id="e8647-136">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8647-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e8647-137">-EventSubscriptionName</span></span>
<span data-ttu-id="e8647-138">Olay aboneliğinin adı</span><span class="sxs-lookup"><span data-stu-id="e8647-138">The name of the event subscription</span></span>

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

### <span data-ttu-id="e8647-139">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="e8647-139">-EventTtl</span></span>
<span data-ttu-id="e8647-140">Olay teslimatı için dakika cinsinden süre.</span><span class="sxs-lookup"><span data-stu-id="e8647-140">The time in minutes for the event delivery.</span></span> <span data-ttu-id="e8647-141">Bu değer 1 ile 1440 arasında olmalıdır</span><span class="sxs-lookup"><span data-stu-id="e8647-141">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="e8647-142">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="e8647-142">-IncludedEventType</span></span>
<span data-ttu-id="e8647-143">İçerilecek olay türlerinin listesini belirten filtre. Belirtilmezse, tüm olay türleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="e8647-143">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="e8647-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8647-144">-InputObject</span></span>
<span data-ttu-id="e8647-145">EventGridSubscription nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e8647-145">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="e8647-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e8647-146">-Label</span></span>
<span data-ttu-id="e8647-147">Olay aboneliği için Etiketler</span><span class="sxs-lookup"><span data-stu-id="e8647-147">Labels for the event subscription</span></span>

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

### <span data-ttu-id="e8647-148">-Max, Yattempt</span><span class="sxs-lookup"><span data-stu-id="e8647-148">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="e8647-149">Olayı teslim etmek için en fazla deneme sayısı.</span><span class="sxs-lookup"><span data-stu-id="e8647-149">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="e8647-150">Bu değer 1 ile 30 arasında olmalıdır</span><span class="sxs-lookup"><span data-stu-id="e8647-150">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="e8647-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8647-151">-ResourceGroupName</span></span>
<span data-ttu-id="e8647-152">Konunun kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e8647-152">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8647-153">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8647-153">-ResourceId</span></span>
<span data-ttu-id="e8647-154">Olay aboneliğinin oluşturulduğu kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="e8647-154">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="e8647-155">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="e8647-155">-SubjectBeginsWith</span></span>
<span data-ttu-id="e8647-156">Yalnızca belirtilen konu önekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="e8647-156">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="e8647-157">Belirtilmezse, tüm konu önekleri olan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="e8647-157">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="e8647-158">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="e8647-158">-SubjectEndsWith</span></span>
<span data-ttu-id="e8647-159">Yalnızca belirtilen konu sonekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="e8647-159">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="e8647-160">Belirtilmezse, tüm konu sonekleri bulunan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="e8647-160">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="e8647-161">-TopicName</span><span class="sxs-lookup"><span data-stu-id="e8647-161">-TopicName</span></span>
<span data-ttu-id="e8647-162">Olay aboneliğinin oluşturulması gereken konunun adı.</span><span class="sxs-lookup"><span data-stu-id="e8647-162">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="e8647-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8647-163">-Confirm</span></span>
<span data-ttu-id="e8647-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8647-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8647-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8647-165">-WhatIf</span></span>
<span data-ttu-id="e8647-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8647-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8647-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8647-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8647-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8647-168">CommonParameters</span></span>
<span data-ttu-id="e8647-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8647-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8647-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8647-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8647-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8647-171">INPUTS</span></span>

### <span data-ttu-id="e8647-172">System. String</span><span class="sxs-lookup"><span data-stu-id="e8647-172">System.String</span></span>

### <span data-ttu-id="e8647-173">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="e8647-173">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="e8647-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8647-174">OUTPUTS</span></span>

### <span data-ttu-id="e8647-175">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="e8647-175">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="e8647-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8647-176">NOTES</span></span>

## <span data-ttu-id="e8647-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8647-177">RELATED LINKS</span></span>
