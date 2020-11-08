---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267722"
---
# <span data-ttu-id="54fba-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="54fba-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="54fba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54fba-102">SYNOPSIS</span></span>
<span data-ttu-id="54fba-103">Bir olay aboneliğinin ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="54fba-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="54fba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54fba-104">SYNTAX</span></span>

### <span data-ttu-id="54fba-105">EventSubscriptionTopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54fba-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54fba-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fba-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54fba-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fba-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54fba-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fba-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54fba-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fba-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54fba-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fba-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54fba-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fba-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54fba-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fba-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54fba-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="54fba-113">DESCRIPTION</span></span>
<span data-ttu-id="54fba-114">Get-AzEventGridSubscription cmdlet 'i, belirli bir olay Kılavuzu aboneliğinin ayrıntılarını veya geçerli Azure aboneliğindeki veya kaynak grubundaki tüm olay Kılavuzu aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="54fba-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="54fba-115">Olay aboneliği adı sağlanmışsa, tek bir olay Kılavuzu aboneliğinin ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="54fba-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="54fba-116">Olay aboneliği adı sağlanmazsa, tüm olay abonelikleri listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="54fba-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="54fba-117">Bu listede döndürülen öğelerin sayısı üst parametre tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="54fba-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="54fba-118">Üst değer belirtilmemişse veya $null, liste tüm olay aboneliği öğelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="54fba-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="54fba-119">Aksi takdirde, en çok listede döndürülecek en fazla öğe sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fba-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="54fba-120">Daha fazla etkinlik hala kullanılabilirse, sonraki çağrıda, bir sonraki olay abonelikleri sayfasını elde etmek için NextLink 'teki değer kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="54fba-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="54fba-121">Son olarak, ODataQuery parametresi arama sonuçlarının filtrelenmesini gerçekleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="54fba-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="54fba-122">Filtreleme sorgusu yalnızca Name özelliğini kullanarak OData söz dizimini takip eder.</span><span class="sxs-lookup"><span data-stu-id="54fba-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="54fba-123">Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="54fba-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="54fba-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54fba-124">EXAMPLES</span></span>

### <span data-ttu-id="54fba-125">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="54fba-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="54fba-126">\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 EventSubscription1 için oluşturulan olay \` aboneliği ayrıntılarını alır \` .</span><span class="sxs-lookup"><span data-stu-id="54fba-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="54fba-127">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="54fba-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="54fba-128">\` \` \` \` \` \` Web kancası tabanlı bir olay aboneliği olan tam uç nokta URL 'si de dahil olmak üzere, myresourcegroupname kaynak grubundaki konu konu1 için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="54fba-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="54fba-129">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="54fba-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="54fba-130">\` \` \` Sayfalandırmadan myresourcegroupname kaynak grubundaki konu1 konu için oluşturulan tüm olay aboneliklerinin listesini edinin \` .</span><span class="sxs-lookup"><span data-stu-id="54fba-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="54fba-131">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="54fba-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="54fba-132">\` \` \` $OdataFilter sorgusunu karşılayan myresourcegroupname kaynak grubundaki konu konu1 için oluşturulmuş ilk 10 olay aboneliğini (varsa) listeleyin \` .</span><span class="sxs-lookup"><span data-stu-id="54fba-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="54fba-133">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="54fba-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="54fba-134">Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="54fba-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="54fba-135">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="54fba-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="54fba-136">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="54fba-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="54fba-137">\` \` Myresourcegroupname kaynak grubu için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="54fba-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="54fba-138">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="54fba-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="54fba-139">\` \` Seçili Azure aboneliği için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="54fba-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="54fba-140">Örnek 7</span><span class="sxs-lookup"><span data-stu-id="54fba-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="54fba-141">Sayfalandırmadan myresourcegroupname kaynak grubu altında oluşturulan tüm genel olay aboneliklerinin listesini alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="54fba-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="54fba-142">Örnek 8</span><span class="sxs-lookup"><span data-stu-id="54fba-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="54fba-143">\`$OdataFilter sorgusunu karşılayan myresourcegroupname kaynak grubu altında oluşturulmuş ilk 5 olay aboneliğini listeleyin \` .</span><span class="sxs-lookup"><span data-stu-id="54fba-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="54fba-144">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="54fba-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="54fba-145">Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="54fba-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="54fba-146">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="54fba-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="54fba-147">Örnek 9</span><span class="sxs-lookup"><span data-stu-id="54fba-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="54fba-148">Seçili Azure aboneliği altında, sayfalandırmadan oluşturulan tüm genel olay aboneliklerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="54fba-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="54fba-149">Örnek 10</span><span class="sxs-lookup"><span data-stu-id="54fba-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="54fba-150">Seçili Azure aboneliği altında, $odataFilter sorgusunu karşılayan ilk 15 genel etkinlik aboneliğini (varsa) listeleyin.</span><span class="sxs-lookup"><span data-stu-id="54fba-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="54fba-151">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="54fba-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="54fba-152">Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="54fba-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="54fba-153">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="54fba-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="54fba-154">Örnek 11</span><span class="sxs-lookup"><span data-stu-id="54fba-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="54fba-155">\` \` Westus2 belirtilen konumunda, sayfalandırmadan belirtilen myresourcegroupname kaynak grubu altında oluşturulan tüm bölgesel olay aboneliklerinin listesini alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="54fba-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="54fba-156">Örnek 12</span><span class="sxs-lookup"><span data-stu-id="54fba-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="54fba-157">Belirtilen konumdaki myresourcegroupname kaynak grubu altında oluşturulmuş ilk 15 bölgesel etkinlik aboneliğini (varsa), \` \` \` \` $odataFilter sorgusunu karşılayan westus2.</span><span class="sxs-lookup"><span data-stu-id="54fba-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="54fba-158">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="54fba-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="54fba-159">Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="54fba-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="54fba-160">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="54fba-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="54fba-161">Örnek 13</span><span class="sxs-lookup"><span data-stu-id="54fba-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="54fba-162">Belirtilen EventHub ad alanı için oluşturulan tüm olay aboneliklerinin listesini sayfalandırmadan alır.</span><span class="sxs-lookup"><span data-stu-id="54fba-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="54fba-163">Örnek 14</span><span class="sxs-lookup"><span data-stu-id="54fba-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="54fba-164">$OdataFilter sorgusunu karşılayan belirtilen EventHub ad alanı için oluşturulmuş ilk 25 olay aboneliğini (varsa) listeleyin.</span><span class="sxs-lookup"><span data-stu-id="54fba-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="54fba-165">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="54fba-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="54fba-166">Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="54fba-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="54fba-167">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="54fba-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="54fba-168">Örnek 15</span><span class="sxs-lookup"><span data-stu-id="54fba-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="54fba-169">Belirtilen konu türü (EventHub ad alanları) için oluşturulan tüm olay aboneliklerinin listesini sayfalandırmadan belirtilen konumda alır.</span><span class="sxs-lookup"><span data-stu-id="54fba-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="54fba-170">Örnek 16</span><span class="sxs-lookup"><span data-stu-id="54fba-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="54fba-171">Belirtilen konum türü (EventHub ad alanları) için oluşturulmuş ilk 15 olay aboneliğini, $odataFilter sorgusunu karşılayan belirtilen konumda listeleyin.</span><span class="sxs-lookup"><span data-stu-id="54fba-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="54fba-172">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="54fba-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="54fba-173">Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="54fba-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="54fba-174">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="54fba-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="54fba-175">Örnek 17</span><span class="sxs-lookup"><span data-stu-id="54fba-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="54fba-176">Belirli bir kaynak grubu için oluşturulan tüm olay aboneliklerinin listesini sayfalandırmadan alır.</span><span class="sxs-lookup"><span data-stu-id="54fba-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="54fba-177">Örnek 18</span><span class="sxs-lookup"><span data-stu-id="54fba-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="54fba-178">$OdataFilter sorgusunu karşılayan belirli bir kaynak grubu için oluşturulmuş ilk 100 olay aboneliğini (varsa) listeleyin.</span><span class="sxs-lookup"><span data-stu-id="54fba-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="54fba-179">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="54fba-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="54fba-180">Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="54fba-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="54fba-181">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="54fba-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="54fba-182">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54fba-182">PARAMETERS</span></span>

### <span data-ttu-id="54fba-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fba-183">-DefaultProfile</span></span>
<span data-ttu-id="54fba-184">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="54fba-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54fba-185">-Domainınputobject</span><span class="sxs-lookup"><span data-stu-id="54fba-185">-DomainInputObject</span></span>
<span data-ttu-id="54fba-186">Olay Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="54fba-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="54fba-187">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="54fba-187">-DomainName</span></span>
<span data-ttu-id="54fba-188">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="54fba-188">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="54fba-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="54fba-190">EventGrid etki alanı konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="54fba-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="54fba-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="54fba-191">-DomainTopicName</span></span>
<span data-ttu-id="54fba-192">EventGrid etki alanı konu adı.</span><span class="sxs-lookup"><span data-stu-id="54fba-192">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="54fba-193">-EventSubscriptionName</span></span>
<span data-ttu-id="54fba-194">Olay aboneliğinin adı</span><span class="sxs-lookup"><span data-stu-id="54fba-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="54fba-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="54fba-196">Olay aboneliği hedefinin tam uç nokta URL 'sini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="54fba-196">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54fba-197">-InputObject</span></span>
<span data-ttu-id="54fba-198">EventGrid konu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="54fba-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="54fba-199">-Konum</span><span class="sxs-lookup"><span data-stu-id="54fba-199">-Location</span></span>
<span data-ttu-id="54fba-200">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="54fba-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="54fba-201">-NextLink</span></span>
<span data-ttu-id="54fba-202">Gönderilecek kaynakların sonraki sayfasının bağlantısı.</span><span class="sxs-lookup"><span data-stu-id="54fba-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="54fba-203">Bu değer, daha fazla kaynak sorgulanmaya devam edildiğinde ilk Get-AzEventGrid cmdlet çağrısıyla elde edilir.</span><span class="sxs-lookup"><span data-stu-id="54fba-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="54fba-204">-ODataQuery</span></span>
<span data-ttu-id="54fba-205">Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu.</span><span class="sxs-lookup"><span data-stu-id="54fba-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="54fba-206">Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="54fba-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fba-207">-ResourceGroupName</span></span>
<span data-ttu-id="54fba-208">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="54fba-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-209">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="54fba-209">-ResourceId</span></span>
<span data-ttu-id="54fba-210">Olay aboneliklerinin oluşturulduğu kaynağın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="54fba-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="54fba-211">-Üst</span><span class="sxs-lookup"><span data-stu-id="54fba-211">-Top</span></span>
<span data-ttu-id="54fba-212">Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu.</span><span class="sxs-lookup"><span data-stu-id="54fba-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="54fba-213">Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="54fba-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="54fba-214">-TopicName</span></span>
<span data-ttu-id="54fba-215">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="54fba-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="54fba-216">-TopicTypeName</span></span>
<span data-ttu-id="54fba-217">TopicType adı</span><span class="sxs-lookup"><span data-stu-id="54fba-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fba-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fba-218">CommonParameters</span></span>
<span data-ttu-id="54fba-219">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54fba-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fba-220">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="54fba-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fba-221">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54fba-221">INPUTS</span></span>

### <span data-ttu-id="54fba-222">System. String</span><span class="sxs-lookup"><span data-stu-id="54fba-222">System.String</span></span>

### <span data-ttu-id="54fba-223">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="54fba-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="54fba-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="54fba-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="54fba-225">Microsoft.Azure.Commands.EventGrid.Models.PSDOmainkonu başlığı</span><span class="sxs-lookup"><span data-stu-id="54fba-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="54fba-226">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="54fba-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="54fba-227">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54fba-227">OUTPUTS</span></span>

### <span data-ttu-id="54fba-228">Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="54fba-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="54fba-229">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54fba-229">NOTES</span></span>

## <span data-ttu-id="54fba-230">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54fba-230">RELATED LINKS</span></span>
