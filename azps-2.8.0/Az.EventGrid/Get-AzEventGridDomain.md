---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: cde1a3274c8fe8372c8b45a729d33d9dce04e998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752021"
---
# <span data-ttu-id="181c1-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="181c1-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="181c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="181c1-102">SYNOPSIS</span></span>
<span data-ttu-id="181c1-103">Bir olay Kılavuzu etki alanının ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay Kılavuzu etki alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="181c1-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="181c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="181c1-104">SYNTAX</span></span>

### <span data-ttu-id="181c1-105">ResourceGroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="181c1-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="181c1-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="181c1-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="181c1-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="181c1-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="181c1-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="181c1-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181c1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="181c1-109">DESCRIPTION</span></span>
<span data-ttu-id="181c1-110">Get-AzEventGridDomain cmdlet 'i, belirtilen bir olay Kılavuzu etki alanının veya geçerli Azure aboneliğindeki tüm olay Kılavuzu etki alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="181c1-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="181c1-111">Etki alanı adı sağlanmışsa, tek bir olay Kılavuzu etki alanının ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="181c1-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="181c1-112">Etki alanı adı sağlanmazsa, etki alanı listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="181c1-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="181c1-113">Bu listede döndürülen öğelerin sayısı üst parametre tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="181c1-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="181c1-114">Üst değer belirtilmemişse veya $null, listede aynı anda döndürülen tüm etki alanı öğeleri yer alır.</span><span class="sxs-lookup"><span data-stu-id="181c1-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="181c1-115">Aksi takdirde, en çok listede döndürülecek en fazla öğe sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="181c1-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="181c1-116">Daha fazla etki alanı varsa, sonraki çağrıda etki alanlarının sonraki sayfasını almak için NextLink 'teki değer kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="181c1-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="181c1-117">Son olarak, ODataQuery parametresi arama sonuçlarının filtrelenmesini gerçekleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="181c1-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="181c1-118">Filtreleme sorgusu yalnızca Name özelliğini kullanarak OData söz dizimini takip eder.</span><span class="sxs-lookup"><span data-stu-id="181c1-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="181c1-119">Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="181c1-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="181c1-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="181c1-120">EXAMPLES</span></span>

### <span data-ttu-id="181c1-121">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="181c1-121">Example 1</span></span>

<span data-ttu-id="181c1-122">\` \` Myresourcegroupname kaynak grubundaki domain1 etki alanı ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="181c1-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="181c1-123">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="181c1-123">Example 2</span></span>

<span data-ttu-id="181c1-124">\` \` \` RESOURCEID seçeneğini kullanarak myresourcegroupname kaynak grubundaki domain1 etki alanı ayrıntılarını alır \` .</span><span class="sxs-lookup"><span data-stu-id="181c1-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="181c1-125">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="181c1-125">Example 3</span></span>

<span data-ttu-id="181c1-126">Tüm olay Kılavuzu etki alanlarını \` sayfalandırmadan Listele myresourcegroupname \`</span><span class="sxs-lookup"><span data-stu-id="181c1-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="181c1-127">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="181c1-127">Example 4</span></span>

<span data-ttu-id="181c1-128">\` \` Bir kerede $odataFilter sorgulama 10 etki alanlarını sağlayan myresourcegroupname kaynak grubundaki olay Kılavuzu etki alanlarını (varsa) listeleyin.</span><span class="sxs-lookup"><span data-stu-id="181c1-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="181c1-129">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="181c1-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="181c1-130">Etki alanları için sonraki sayfaları alabilmeniz için kullanıcının Get-AzEventGridDomain yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="181c1-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="181c1-131">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="181c1-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="181c1-132">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="181c1-132">Example 5</span></span>

<span data-ttu-id="181c1-133">Azure aboneliğindeki tüm olay Kılavuzu etki alanlarını sayfalandırmadan listeleme (tüm etki alanları tek bir atıya döndürülüyor)</span><span class="sxs-lookup"><span data-stu-id="181c1-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="181c1-134">Örnek 6</span><span class="sxs-lookup"><span data-stu-id="181c1-134">Example 6</span></span>

<span data-ttu-id="181c1-135">Azure aboneliğindeki olay Kılavuzu etki alanlarını (varsa), bir kerede $odataFilter sorgu 20 etki alanını karşılayan şekilde listeleyin.</span><span class="sxs-lookup"><span data-stu-id="181c1-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="181c1-136">Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz.</span><span class="sxs-lookup"><span data-stu-id="181c1-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="181c1-137">Etki alanları için sonraki sayfaları alabilmeniz için kullanıcının Get-AzEventGridDomain yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı.</span><span class="sxs-lookup"><span data-stu-id="181c1-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="181c1-138">Çağrı yapıldığında arayan durur. NextLink $null olur.</span><span class="sxs-lookup"><span data-stu-id="181c1-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="181c1-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="181c1-139">PARAMETERS</span></span>

### <span data-ttu-id="181c1-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181c1-140">-DefaultProfile</span></span>
<span data-ttu-id="181c1-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="181c1-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="181c1-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="181c1-142">-Name</span></span>
<span data-ttu-id="181c1-143">EventGrid etki alanı adı.</span><span class="sxs-lookup"><span data-stu-id="181c1-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181c1-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="181c1-144">-NextLink</span></span>
<span data-ttu-id="181c1-145">Gönderilecek kaynakların sonraki sayfasının bağlantısı.</span><span class="sxs-lookup"><span data-stu-id="181c1-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="181c1-146">Bu değer, daha fazla kaynak sorgulanmaya devam edildiğinde ilk Get-AzEventGrid cmdlet çağrısıyla elde edilir.</span><span class="sxs-lookup"><span data-stu-id="181c1-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181c1-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="181c1-147">-ODataQuery</span></span>
<span data-ttu-id="181c1-148">Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu.</span><span class="sxs-lookup"><span data-stu-id="181c1-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="181c1-149">Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.</span><span class="sxs-lookup"><span data-stu-id="181c1-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181c1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="181c1-150">-ResourceGroupName</span></span>
<span data-ttu-id="181c1-151">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="181c1-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181c1-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="181c1-152">-ResourceId</span></span>
<span data-ttu-id="181c1-153">Olay Kılavuzu etki alanını temsil eden kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="181c1-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="181c1-154">-Üst</span><span class="sxs-lookup"><span data-stu-id="181c1-154">-Top</span></span>
<span data-ttu-id="181c1-155">Elde edilecek kaynak sayısı üst sınırı.</span><span class="sxs-lookup"><span data-stu-id="181c1-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="181c1-156">Geçerli değer 1 ile 100 arasındadır.</span><span class="sxs-lookup"><span data-stu-id="181c1-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="181c1-157">En üst değer belirtildiyse ve daha fazla sonuç hala kullanılabiliyorsa, sonuç, NextLink 'de Sorgulanacak sonraki sayfanın bağlantısını içerecektir.</span><span class="sxs-lookup"><span data-stu-id="181c1-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="181c1-158">En üst değer belirtilmezse, tüm kaynak listesi bir kerede geri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="181c1-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181c1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181c1-159">CommonParameters</span></span>
<span data-ttu-id="181c1-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="181c1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181c1-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181c1-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181c1-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="181c1-162">INPUTS</span></span>

### <span data-ttu-id="181c1-163">System. String</span><span class="sxs-lookup"><span data-stu-id="181c1-163">System.String</span></span>

## <span data-ttu-id="181c1-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="181c1-164">OUTPUTS</span></span>

### <span data-ttu-id="181c1-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="181c1-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="181c1-166">Microsoft.Azure.Commands.EventGrid.Models.PSDOmainlistınstance</span><span class="sxs-lookup"><span data-stu-id="181c1-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="181c1-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="181c1-167">NOTES</span></span>

## <span data-ttu-id="181c1-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="181c1-168">RELATED LINKS</span></span>
