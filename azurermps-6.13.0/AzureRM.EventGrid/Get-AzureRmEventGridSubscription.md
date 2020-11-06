---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 3117433c677330eba4585d45337c44658225ee0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590944"
---
# <span data-ttu-id="c5f2d-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="c5f2d-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="c5f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f2d-103">Bir olay aboneliğinin ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5f2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5f2d-104">SYNTAX</span></span>

### <span data-ttu-id="c5f2d-105">EventSubscriptionTopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5f2d-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5f2d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5f2d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5f2d-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5f2d-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5f2d-108">Eventsubscriptionınputobjectset</span><span class="sxs-lookup"><span data-stu-id="c5f2d-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5f2d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5f2d-109">DESCRIPTION</span></span>
<span data-ttu-id="c5f2d-110">Get-AzureRmEventGridSubscription cmdlet 'i, belirli bir olay Kılavuzu aboneliğinin ayrıntılarını veya geçerli Azure aboneliğindeki veya kaynak grubundaki tüm olay Kılavuzu aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="c5f2d-111">Olay aboneliği adı sağlanmışsa, tek bir olay Kılavuzu aboneliğinin ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="c5f2d-112">Olay aboneliği adı sağlanmazsa, tüm olay abonelikleri listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="c5f2d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5f2d-113">EXAMPLES</span></span>

### <span data-ttu-id="c5f2d-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c5f2d-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c5f2d-115">\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 EventSubscription1 için oluşturulan olay \` aboneliği ayrıntılarını alır \` .</span><span class="sxs-lookup"><span data-stu-id="c5f2d-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c5f2d-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c5f2d-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="c5f2d-117">\` \` \` \` \` \` Web kancası tabanlı bir olay aboneliği olan tam uç nokta URL 'si de dahil olmak üzere, myresourcegroupname kaynak grubundaki konu konu1 için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="c5f2d-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c5f2d-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="c5f2d-119">\` \` Myresourcegroupname kaynak grubunda konu konu1 için oluşturulan tüm olay aboneliklerinin bir listesini alın \` \` .</span><span class="sxs-lookup"><span data-stu-id="c5f2d-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c5f2d-120">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="c5f2d-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c5f2d-121">\` \` Myresourcegroupname kaynak grubu için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="c5f2d-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c5f2d-122">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="c5f2d-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="c5f2d-123">\` \` Seçili Azure aboneliği için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="c5f2d-124">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="c5f2d-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="c5f2d-125">Myresourcegroupname kaynak grubu altında oluşturulan tüm genel olay aboneliklerinin listesini alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="c5f2d-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c5f2d-126">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="c5f2d-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="c5f2d-127">Seçili Azure aboneliği altında oluşturulan tüm genel olay aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="c5f2d-128">Örnek 8</span><span class="sxs-lookup"><span data-stu-id="c5f2d-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="c5f2d-129">\` \` Belirtilen konum westus2 kaynak grubu altında oluşturulan tüm bölgesel olay aboneliklerinin listesini alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="c5f2d-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="c5f2d-130">Örnek 9</span><span class="sxs-lookup"><span data-stu-id="c5f2d-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="c5f2d-131">Belirtilen EventHub ad alanı için oluşturulan tüm olay abonelikleri listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="c5f2d-132">Örnek 10</span><span class="sxs-lookup"><span data-stu-id="c5f2d-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="c5f2d-133">Belirtilen konu türü (EventHub ad alanları) için oluşturulan tüm olay aboneliklerinin listesini belirtilen konumda alır.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="c5f2d-134">Örnek 11</span><span class="sxs-lookup"><span data-stu-id="c5f2d-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="c5f2d-135">Belirli bir kaynak grubu için oluşturulan tüm olay aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="c5f2d-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5f2d-136">PARAMETERS</span></span>

### <span data-ttu-id="c5f2d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f2d-137">-DefaultProfile</span></span>
<span data-ttu-id="c5f2d-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c5f2d-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5f2d-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c5f2d-139">-EventSubscriptionName</span></span>
<span data-ttu-id="c5f2d-140">Olay aboneliğinin adı</span><span class="sxs-lookup"><span data-stu-id="c5f2d-140">The name of the event subscription</span></span>

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

### <span data-ttu-id="c5f2d-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="c5f2d-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="c5f2d-142">Olay aboneliği hedefinin tam uç nokta URL 'sini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-142">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="c5f2d-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5f2d-143">-InputObject</span></span>
<span data-ttu-id="c5f2d-144">EventGrid olay aboneliği nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-144">EventGrid Event Subscription object.</span></span>

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

### <span data-ttu-id="c5f2d-145">-Konum</span><span class="sxs-lookup"><span data-stu-id="c5f2d-145">-Location</span></span>
<span data-ttu-id="c5f2d-146">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="c5f2d-146">Location</span></span>

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

### <span data-ttu-id="c5f2d-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5f2d-147">-ResourceGroupName</span></span>
<span data-ttu-id="c5f2d-148">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="c5f2d-149">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c5f2d-149">-ResourceId</span></span>
<span data-ttu-id="c5f2d-150">Olay aboneliklerinin oluşturulduğu kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-150">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="c5f2d-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="c5f2d-151">-TopicName</span></span>
<span data-ttu-id="c5f2d-152">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-152">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c5f2d-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="c5f2d-153">-TopicTypeName</span></span>
<span data-ttu-id="c5f2d-154">TopicType adı</span><span class="sxs-lookup"><span data-stu-id="c5f2d-154">TopicType name</span></span>

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

### <span data-ttu-id="c5f2d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f2d-155">CommonParameters</span></span>
<span data-ttu-id="c5f2d-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5f2d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f2d-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5f2d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f2d-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5f2d-158">INPUTS</span></span>

### <span data-ttu-id="c5f2d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="c5f2d-159">System.String</span></span>

### <span data-ttu-id="c5f2d-160">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="c5f2d-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="c5f2d-161">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5f2d-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c5f2d-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5f2d-162">OUTPUTS</span></span>

### <span data-ttu-id="c5f2d-163">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="c5f2d-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="c5f2d-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5f2d-164">NOTES</span></span>

## <span data-ttu-id="c5f2d-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5f2d-165">RELATED LINKS</span></span>
