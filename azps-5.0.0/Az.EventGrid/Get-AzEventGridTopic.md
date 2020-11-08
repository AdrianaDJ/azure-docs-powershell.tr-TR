---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277464"
---
# <span data-ttu-id="d5586-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="d5586-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="d5586-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5586-102">SYNOPSIS</span></span>
<span data-ttu-id="d5586-103">Bir olay Kılavuzu konusunun ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay Kılavuzu konularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d5586-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="d5586-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5586-104">SYNTAX</span></span>

### <span data-ttu-id="d5586-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d5586-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5586-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5586-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5586-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5586-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5586-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5586-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5586-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5586-109">DESCRIPTION</span></span>
<span data-ttu-id="d5586-110">Get-AzEventGridTopic cmdlet 'i, belirli bir olay Kılavuzu konusunun ayrıntılarını veya geçerli Azure aboneliğindeki tüm olay Kılavuzu konularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d5586-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="d5586-111">Konu adı sağlanmışsa, tek bir olay Kılavuzu konusunun ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="d5586-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="d5586-112">Konu adı sağlanmadıysa, konu listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="d5586-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="d5586-113">Bu listede döndürülen öğelerin sayısı üst parametre tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="d5586-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="d5586-114">Üst değer belirtilmemişse veya $null, liste tüm konular öğelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="d5586-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="d5586-115">Aksi takdirde, en çok listede döndürülecek en fazla öğe sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5586-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="d5586-116">Daha fazla konu varsa daha fazla konu varsa, sonraki çağrıda konuların sonraki sayfasını almak için sonraki çağrıda kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d5586-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="d5586-117">Son olarak, ODataQuery parametresi arama sonuçlarının filtrelenmesini gerçekleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d5586-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="d5586-118">Filtreleme sorgusu yalnızca Name özelliğini kullanarak OData söz dizimini takip eder.</span><span class="sxs-lookup"><span data-stu-id="d5586-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="d5586-119">Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="d5586-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="d5586-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5586-120">EXAMPLES</span></span>

### <span data-ttu-id="d5586-121">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d5586-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="d5586-122">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="d5586-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d5586-123">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d5586-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="d5586-124">\` \` Myresourcegroupname kaynak grubundaki Konu1 olay Kılavuzu konusunun ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="d5586-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d5586-125">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d5586-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="d5586-126">Sayfalandırmadan myresourcegroupname kaynak grubundaki tüm olay Kılavuzu konularını listeleyin \` \` .</span><span class="sxs-lookup"><span data-stu-id="d5586-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="d5586-127">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="d5586-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="d5586-128">\`$OdataFilter sorgusunu karşılayan myresourcegroupname kaynak grubundaki ilk 10 olay Kılavuzu konularını (varsa) listeleyin \` .</span><span class="sxs-lookup"><span data-stu-id="d5586-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d5586-129">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="d5586-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d5586-130">Konuların sonraki sayfaları alabilmek için kullanıcının Get-AzEventGridTopic yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="d5586-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d5586-131">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="d5586-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="d5586-132">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="d5586-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="d5586-133">Abonedeki tüm olay Kılavuzu konularını sayfalandırmadan listeleyin.</span><span class="sxs-lookup"><span data-stu-id="d5586-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="d5586-134">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="d5586-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="d5586-135">Abonelikte $odataFilter sorgusunu karşılayan ilk 10 olay Kılavuzu (varsa) konularını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="d5586-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d5586-136">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="d5586-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d5586-137">Konuların sonraki sayfaları alabilmek için kullanıcının Get-AzEventGridTopic yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="d5586-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d5586-138">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="d5586-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="d5586-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5586-139">PARAMETERS</span></span>

### <span data-ttu-id="d5586-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5586-140">-DefaultProfile</span></span>
<span data-ttu-id="d5586-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d5586-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5586-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5586-142">-Name</span></span>
<span data-ttu-id="d5586-143">EventGrid konu adı.</span><span class="sxs-lookup"><span data-stu-id="d5586-143">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5586-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="d5586-144">-NextLink</span></span>
<span data-ttu-id="d5586-145">Gönderilecek kaynakların sonraki sayfasının bağlantısı.</span><span class="sxs-lookup"><span data-stu-id="d5586-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="d5586-146">Bu değer, daha fazla kaynak sorgulanmaya devam edildiğinde ilk Get-AzEventGrid cmdlet çağrısıyla elde edilir.</span><span class="sxs-lookup"><span data-stu-id="d5586-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="d5586-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d5586-147">-ODataQuery</span></span>
<span data-ttu-id="d5586-148">Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu.</span><span class="sxs-lookup"><span data-stu-id="d5586-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="d5586-149">Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="d5586-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5586-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5586-150">-ResourceGroupName</span></span>
<span data-ttu-id="d5586-151">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d5586-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5586-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d5586-152">-ResourceId</span></span>
<span data-ttu-id="d5586-153">Olay Kılavuzu konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="d5586-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d5586-154">-Üst</span><span class="sxs-lookup"><span data-stu-id="d5586-154">-Top</span></span>
<span data-ttu-id="d5586-155">Elde edilecek kaynak sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="d5586-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="d5586-156">Geçerli değer 1 ile 100 arasındadır.</span><span class="sxs-lookup"><span data-stu-id="d5586-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="d5586-157">En üst değer belirtildiyse ve daha fazla sonuç hala kullanılabiliyorsa, sonuç, NextLink 'de Sorgulanacak sonraki sayfanın bağlantısını içerecektir.</span><span class="sxs-lookup"><span data-stu-id="d5586-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="d5586-158">En üst değer belirtilmezse, tüm kaynak listesi bir kerede geri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="d5586-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5586-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5586-159">CommonParameters</span></span>
<span data-ttu-id="d5586-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5586-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5586-161">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d5586-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5586-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5586-162">INPUTS</span></span>

### <span data-ttu-id="d5586-163">System. String</span><span class="sxs-lookup"><span data-stu-id="d5586-163">System.String</span></span>

### <span data-ttu-id="d5586-164">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d5586-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d5586-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5586-165">OUTPUTS</span></span>

### <span data-ttu-id="d5586-166">Microsoft. Azure. Commands. EventGrid. modeller. PSTopic</span><span class="sxs-lookup"><span data-stu-id="d5586-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="d5586-167">Microsoft. Azure. Commands. EventGrid. modeller. Pstopiclistınstance</span><span class="sxs-lookup"><span data-stu-id="d5586-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="d5586-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5586-168">NOTES</span></span>

## <span data-ttu-id="d5586-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5586-169">RELATED LINKS</span></span>
