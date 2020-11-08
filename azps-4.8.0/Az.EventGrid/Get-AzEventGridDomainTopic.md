---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273603"
---
# <span data-ttu-id="d13e9-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d13e9-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="d13e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d13e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d13e9-103">Bir olay Kılavuzu etki alanı konusunun ayrıntılarını alır veya geçerli Azure aboneliğindeki belirli bir olay Kılavuzu etki alanı altındaki tüm olay Kılavuzu etki alanı konularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d13e9-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="d13e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d13e9-104">SYNTAX</span></span>

### <span data-ttu-id="d13e9-105">DomainTopicNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d13e9-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d13e9-106">Resourceıddomaintopicparameterset</span><span class="sxs-lookup"><span data-stu-id="d13e9-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d13e9-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="d13e9-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d13e9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d13e9-108">DESCRIPTION</span></span>
<span data-ttu-id="d13e9-109">Get-AzEventGridDomainTopic cmdlet 'i, belirli bir olay Kılavuzu etki alanı konusunun ayrıntılarını veya geçerli Azure aboneliğindeki belirli bir etki alanının altındaki tüm olay Kılavuzu etki alanı konularının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d13e9-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="d13e9-110">Etki alanı konu adı sağlanmışsa, tek bir olay Kılavuzu etki alanı konusunun ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="d13e9-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="d13e9-111">Etki alanı konu adı sağlanmadıysa, belirtilen etki alanı adı altındaki etki alanı konularının listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="d13e9-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="d13e9-112">Bu listede döndürülen öğelerin sayısı üst parametre tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="d13e9-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="d13e9-113">Üst değer belirtilmemişse veya $null, liste tüm etki alanı konuları öğelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="d13e9-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="d13e9-114">Aksi takdirde, en çok listede döndürülecek en fazla öğe sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d13e9-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="d13e9-115">Daha fazla etki alanı konusu hala kullanılabiliyorsa, sonraki çağrıda, etki alanı konularının sonraki sayfasını elde etmek için, NextLink 'teki değer kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d13e9-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="d13e9-116">Son olarak, ODataQuery parametresi arama sonuçlarının filtrelenmesini gerçekleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d13e9-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="d13e9-117">Filtreleme sorgusu yalnızca Name özelliğini kullanarak OData söz dizimini takip eder.</span><span class="sxs-lookup"><span data-stu-id="d13e9-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="d13e9-118">Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="d13e9-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="d13e9-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d13e9-119">EXAMPLES</span></span>

### <span data-ttu-id="d13e9-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d13e9-120">Example 1</span></span>

<span data-ttu-id="d13e9-121">\` \` \` \` Myresourcegroupname kaynak grubundaki DomainTopic1 etki alanı domain1 altındaki olay \` Kılavuzu etki alanı konusunun ayrıntılarını alır \` .</span><span class="sxs-lookup"><span data-stu-id="d13e9-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="d13e9-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d13e9-122">Example 2</span></span>

<span data-ttu-id="d13e9-123">\` \` \` \` \` RESOURCEID seçeneğini kullanarak myresourcegroupname kaynak grubundaki DomainTopic1 etki alanı konu başlığı altındaki olay Kılavuzu etki alanı konusunun ayrıntılarını \` .</span><span class="sxs-lookup"><span data-stu-id="d13e9-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="d13e9-124">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d13e9-124">Example 3</span></span>

<span data-ttu-id="d13e9-125">\` \` \` Sayfalama olmadan myresourcegroupname kaynak grubunda domain1 \` (tüm sonuçlar tek bir görüntü içinde döndürülür)</span><span class="sxs-lookup"><span data-stu-id="d13e9-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="d13e9-126">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="d13e9-126">Example 4</span></span>

<span data-ttu-id="d13e9-127">Tüm olay Kılavuzu etki alanı domain1 'in altındaki \` \` \` myresourcegroupname kaynak grubundaki \` tüm olay Kılavuzu etki alanı başlıklarını listeleme</span><span class="sxs-lookup"><span data-stu-id="d13e9-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="d13e9-128">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="d13e9-128">Example 5</span></span>

<span data-ttu-id="d13e9-129">$OdataFilter etki alanı domain1 'in altındaki etki alanı altında, \` \` \` \` bir kerede 10 etki alanı</span><span class="sxs-lookup"><span data-stu-id="d13e9-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="d13e9-130">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="d13e9-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d13e9-131">Etki alanı konularının sonraki sayfaları alabilmek için, kullanıcının Get-AzEventGridDomainTopic yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="d13e9-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d13e9-132">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="d13e9-132">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## <span data-ttu-id="d13e9-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d13e9-133">PARAMETERS</span></span>

### <span data-ttu-id="d13e9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13e9-134">-DefaultProfile</span></span>
<span data-ttu-id="d13e9-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d13e9-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d13e9-136">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="d13e9-136">-DomainName</span></span>
<span data-ttu-id="d13e9-137">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d13e9-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13e9-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="d13e9-138">-Name</span></span>
<span data-ttu-id="d13e9-139">EventGrid etki alanı konu adı.</span><span class="sxs-lookup"><span data-stu-id="d13e9-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13e9-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="d13e9-140">-NextLink</span></span>
<span data-ttu-id="d13e9-141">Gönderilecek kaynakların sonraki sayfasının bağlantısı.</span><span class="sxs-lookup"><span data-stu-id="d13e9-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="d13e9-142">Bu değer, daha fazla kaynak sorgulanmaya devam edildiğinde ilk Get-AzEventGrid cmdlet çağrısıyla elde edilir.</span><span class="sxs-lookup"><span data-stu-id="d13e9-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="d13e9-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d13e9-143">-ODataQuery</span></span>
<span data-ttu-id="d13e9-144">Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu.</span><span class="sxs-lookup"><span data-stu-id="d13e9-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="d13e9-145">Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="d13e9-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13e9-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d13e9-146">-ResourceGroupName</span></span>
<span data-ttu-id="d13e9-147">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d13e9-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13e9-148">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d13e9-148">-ResourceId</span></span>
<span data-ttu-id="d13e9-149">Olay Kılavuzu etki alanı veya kılavuz etki alanı konusunu temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="d13e9-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13e9-150">-Üst</span><span class="sxs-lookup"><span data-stu-id="d13e9-150">-Top</span></span>
<span data-ttu-id="d13e9-151">Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu.</span><span class="sxs-lookup"><span data-stu-id="d13e9-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="d13e9-152">Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="d13e9-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13e9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13e9-153">CommonParameters</span></span>
<span data-ttu-id="d13e9-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d13e9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13e9-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d13e9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13e9-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d13e9-156">INPUTS</span></span>

### <span data-ttu-id="d13e9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="d13e9-157">System.String</span></span>

### <span data-ttu-id="d13e9-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d13e9-158">System.Int32</span></span>

## <span data-ttu-id="d13e9-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d13e9-159">OUTPUTS</span></span>

### <span data-ttu-id="d13e9-160">Microsoft.Azure.Commands.EventGrid.Models.PSDOmainkonu başlığı</span><span class="sxs-lookup"><span data-stu-id="d13e9-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="d13e9-161">Microsoft.Azure.Commands.EventGrid.Models.PSDOmaintopiclistınstance</span><span class="sxs-lookup"><span data-stu-id="d13e9-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="d13e9-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d13e9-162">NOTES</span></span>

## <span data-ttu-id="d13e9-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d13e9-163">RELATED LINKS</span></span>
