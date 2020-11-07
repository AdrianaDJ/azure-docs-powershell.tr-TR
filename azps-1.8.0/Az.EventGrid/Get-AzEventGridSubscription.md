---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760880"
---
# <span data-ttu-id="1232a-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1232a-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="1232a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1232a-102">SYNOPSIS</span></span>
<span data-ttu-id="1232a-103">Bir olay aboneliğinin ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1232a-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="1232a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1232a-104">SYNTAX</span></span>

### <span data-ttu-id="1232a-105">EventSubscriptionTopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1232a-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1232a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1232a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1232a-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1232a-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1232a-108">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1232a-108">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1232a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1232a-109">DESCRIPTION</span></span>
<span data-ttu-id="1232a-110">Get-AzEventGridSubscription cmdlet 'i, belirli bir olay Kılavuzu aboneliğinin ayrıntılarını veya geçerli Azure aboneliğindeki veya kaynak grubundaki tüm olay Kılavuzu aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1232a-110">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="1232a-111">Olay aboneliği adı sağlanmışsa, tek bir olay Kılavuzu aboneliğinin ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="1232a-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="1232a-112">Olay aboneliği adı sağlanmazsa, tüm olay abonelikleri listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="1232a-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="1232a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1232a-113">EXAMPLES</span></span>

### <span data-ttu-id="1232a-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1232a-114">Example 1</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="1232a-115">\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 EventSubscription1 için oluşturulan olay \` aboneliği ayrıntılarını alır \` .</span><span class="sxs-lookup"><span data-stu-id="1232a-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1232a-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1232a-116">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="1232a-117">\` \` \` \` \` \` Web kancası tabanlı bir olay aboneliği olan tam uç nokta URL 'si de dahil olmak üzere, myresourcegroupname kaynak grubundaki konu konu1 için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="1232a-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="1232a-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1232a-118">Example 3</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="1232a-119">\` \` Myresourcegroupname kaynak grubunda konu konu1 için oluşturulan tüm olay aboneliklerinin bir listesini alın \` \` .</span><span class="sxs-lookup"><span data-stu-id="1232a-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1232a-120">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="1232a-120">Example 4</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="1232a-121">\` \` Myresourcegroupname kaynak grubu için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="1232a-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1232a-122">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="1232a-122">Example 5</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="1232a-123">\` \` Seçili Azure aboneliği için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="1232a-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="1232a-124">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="1232a-124">Example 6</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="1232a-125">Myresourcegroupname kaynak grubu altında oluşturulan tüm genel olay aboneliklerinin listesini alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="1232a-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1232a-126">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="1232a-126">Example 7</span></span>
```
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="1232a-127">Seçili Azure aboneliği altında oluşturulan tüm genel olay aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1232a-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="1232a-128">Örnek 8</span><span class="sxs-lookup"><span data-stu-id="1232a-128">Example 8</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="1232a-129">\` \` Belirtilen konum westus2 kaynak grubu altında oluşturulan tüm bölgesel olay aboneliklerinin listesini alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="1232a-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="1232a-130">Örnek 9</span><span class="sxs-lookup"><span data-stu-id="1232a-130">Example 9</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="1232a-131">Belirtilen EventHub ad alanı için oluşturulan tüm olay abonelikleri listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1232a-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="1232a-132">Örnek 10</span><span class="sxs-lookup"><span data-stu-id="1232a-132">Example 10</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="1232a-133">Belirtilen konu türü (EventHub ad alanları) için oluşturulan tüm olay aboneliklerinin listesini belirtilen konumda alır.</span><span class="sxs-lookup"><span data-stu-id="1232a-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="1232a-134">Örnek 11</span><span class="sxs-lookup"><span data-stu-id="1232a-134">Example 11</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="1232a-135">Belirli bir kaynak grubu için oluşturulan tüm olay aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="1232a-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="1232a-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1232a-136">PARAMETERS</span></span>

### <span data-ttu-id="1232a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1232a-137">-DefaultProfile</span></span>
<span data-ttu-id="1232a-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1232a-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1232a-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1232a-139">-EventSubscriptionName</span></span>
<span data-ttu-id="1232a-140">Olay aboneliğinin adı</span><span class="sxs-lookup"><span data-stu-id="1232a-140">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1232a-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="1232a-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="1232a-142">Olay aboneliği hedefinin tam uç nokta URL 'sini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1232a-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1232a-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1232a-143">-InputObject</span></span>
<span data-ttu-id="1232a-144">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1232a-144">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="1232a-145">-Konum</span><span class="sxs-lookup"><span data-stu-id="1232a-145">-Location</span></span>
<span data-ttu-id="1232a-146">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="1232a-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1232a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1232a-147">-ResourceGroupName</span></span>
<span data-ttu-id="1232a-148">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1232a-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1232a-149">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1232a-149">-ResourceId</span></span>
<span data-ttu-id="1232a-150">Olay aboneliklerinin oluşturulduğu kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="1232a-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1232a-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="1232a-151">-TopicName</span></span>
<span data-ttu-id="1232a-152">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="1232a-152">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1232a-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="1232a-153">-TopicTypeName</span></span>
<span data-ttu-id="1232a-154">TopicType adı</span><span class="sxs-lookup"><span data-stu-id="1232a-154">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1232a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1232a-155">CommonParameters</span></span>
<span data-ttu-id="1232a-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1232a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1232a-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1232a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1232a-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1232a-158">INPUTS</span></span>

### <span data-ttu-id="1232a-159">System. String</span><span class="sxs-lookup"><span data-stu-id="1232a-159">System.String</span></span>

### <span data-ttu-id="1232a-160">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="1232a-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="1232a-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1232a-161">OUTPUTS</span></span>

### <span data-ttu-id="1232a-162">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="1232a-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="1232a-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1232a-163">NOTES</span></span>

## <span data-ttu-id="1232a-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1232a-164">RELATED LINKS</span></span>
