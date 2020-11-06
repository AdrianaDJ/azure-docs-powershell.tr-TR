---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: 7a6f7833a2b123a4f0235d331952b1403316df37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589794"
---
# <span data-ttu-id="6bba6-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6bba6-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="6bba6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bba6-102">SYNOPSIS</span></span>
<span data-ttu-id="6bba6-103">Olay Kılavuzu olay aboneliğinin özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6bba6-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bba6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bba6-104">SYNTAX</span></span>

### <span data-ttu-id="6bba6-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6bba6-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bba6-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bba6-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bba6-107">Eventsubscriptionınputobjectset</span><span class="sxs-lookup"><span data-stu-id="6bba6-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bba6-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bba6-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bba6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bba6-109">DESCRIPTION</span></span>
<span data-ttu-id="6bba6-110">Olay Kılavuzu olay aboneliğinin özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6bba6-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="6bba6-111">Bu, var olan bir olay aboneliğinin filtresini, hedefini veya etiketlerini güncelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6bba6-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="6bba6-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bba6-112">EXAMPLES</span></span>

### <span data-ttu-id="6bba6-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6bba6-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="6bba6-114">\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 \` \` ES1\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="6bba6-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="6bba6-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6bba6-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="6bba6-116">\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 \` \` ES1\`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="6bba6-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="6bba6-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="6bba6-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="6bba6-118">\` \` Yeni uç nokta olarak, EventHub ad alanı ContosoNamespace için olay aboneliği ES1 özelliklerini \` https://requestb.in/1kxxoui1\ ve yeni subjectendswith \` jpg olarak güncelleştirir\`</span><span class="sxs-lookup"><span data-stu-id="6bba6-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="6bba6-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="6bba6-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="6bba6-120">\` \` \` Yeni Etiketler $Labels myresourcegroupname kaynak grubu için olay aboneliği ES1 özelliklerini güncelleştirir \` .</span><span class="sxs-lookup"><span data-stu-id="6bba6-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="6bba6-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bba6-121">PARAMETERS</span></span>

### <span data-ttu-id="6bba6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bba6-122">-DefaultProfile</span></span>
<span data-ttu-id="6bba6-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bba6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bba6-124">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="6bba6-124">-Endpoint</span></span>
<span data-ttu-id="6bba6-125">Olay aboneliği hedef uç noktası.</span><span class="sxs-lookup"><span data-stu-id="6bba6-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="6bba6-126">Bu, bir EventHub Web kancası URL 'SI veya Azure Resource ID olabilir.</span><span class="sxs-lookup"><span data-stu-id="6bba6-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="6bba6-127">-EndpointType</span></span>
<span data-ttu-id="6bba6-128">Uç nokta türü.</span><span class="sxs-lookup"><span data-stu-id="6bba6-128">Endpoint Type.</span></span>
<span data-ttu-id="6bba6-129">Bu, Web kancası veya eventhub olabilir</span><span class="sxs-lookup"><span data-stu-id="6bba6-129">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6bba6-130">-EventSubscriptionName</span></span>
<span data-ttu-id="6bba6-131">Olay aboneliğinin adı</span><span class="sxs-lookup"><span data-stu-id="6bba6-131">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="6bba6-132">-IncludedEventType</span></span>
<span data-ttu-id="6bba6-133">İçerilecek olay türlerinin listesini belirten filtre. Belirtilmezse, tüm olay türleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="6bba6-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bba6-134">-InputObject</span></span>
<span data-ttu-id="6bba6-135">EventGridSubscription nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6bba6-135">EventGridSubscription object.</span></span>

```yaml
Type: PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6bba6-136">-Label</span></span>
<span data-ttu-id="6bba6-137">Olay aboneliği için Etiketler</span><span class="sxs-lookup"><span data-stu-id="6bba6-137">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bba6-138">-ResourceGroupName</span></span>
<span data-ttu-id="6bba6-139">Konunun kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="6bba6-139">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6bba6-140">-ResourceId</span></span>
<span data-ttu-id="6bba6-141">Olay aboneliğinin oluşturulduğu kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6bba6-141">The identifier of the resource to which the event subscription was created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="6bba6-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="6bba6-143">Yalnızca belirtilen konu önekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="6bba6-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="6bba6-144">Belirtilmezse, tüm konu önekleri olan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="6bba6-144">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="6bba6-145">-SubjectEndsWith</span></span>
<span data-ttu-id="6bba6-146">Yalnızca belirtilen konu sonekiyle eşleşen olayların dahil edileceğini belirten filtre.</span><span class="sxs-lookup"><span data-stu-id="6bba6-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="6bba6-147">Belirtilmezse, tüm konu sonekleri bulunan olaylar dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="6bba6-147">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-148">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6bba6-148">-TopicName</span></span>
<span data-ttu-id="6bba6-149">Olay aboneliğinin oluşturulması gereken konunun adı.</span><span class="sxs-lookup"><span data-stu-id="6bba6-149">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bba6-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bba6-150">-Confirm</span></span>
<span data-ttu-id="6bba6-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bba6-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bba6-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bba6-152">-WhatIf</span></span>
<span data-ttu-id="6bba6-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bba6-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bba6-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bba6-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bba6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bba6-155">CommonParameters</span></span>
<span data-ttu-id="6bba6-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bba6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bba6-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bba6-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bba6-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bba6-158">INPUTS</span></span>

### <span data-ttu-id="6bba6-159">System. String</span><span class="sxs-lookup"><span data-stu-id="6bba6-159">System.String</span></span>
<span data-ttu-id="6bba6-160">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription System. String []</span><span class="sxs-lookup"><span data-stu-id="6bba6-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.String[]</span></span>

## <span data-ttu-id="6bba6-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bba6-161">OUTPUTS</span></span>

### <span data-ttu-id="6bba6-162">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="6bba6-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="6bba6-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bba6-163">NOTES</span></span>

## <span data-ttu-id="6bba6-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bba6-164">RELATED LINKS</span></span>

