---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107670"
---
# <span data-ttu-id="cbb3b-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="cbb3b-101">Search-AzGraph</span></span>

## <span data-ttu-id="cbb3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbb3b-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb3b-103">Azure Resource Manager tarafından yönetilen kaynakları sorgular.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="cbb3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbb3b-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbb3b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbb3b-105">DESCRIPTION</span></span>
<span data-ttu-id="cbb3b-106">Sorgu söz dizimi hakkında daha fazla bilgi edinin: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="cbb3b-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="cbb3b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbb3b-107">EXAMPLES</span></span>

### <span data-ttu-id="cbb3b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cbb3b-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="cbb3b-109">Basit kaynaklar kaynak alanlarının alt kümesini isteyen sorgu.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="cbb3b-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="cbb3b-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="cbb3b-111">Alan seçimi, filtreleme ve özetleme özelliklerine sahip kaynaklar üzerinde karmaşık bir sorgu.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="cbb3b-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="cbb3b-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="cbb3b-113">Yönetilen diskleri kullanmayan ve abonelik görünen adlarını içeren tüm sanal makineleri sağlayan bir sorgu.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="cbb3b-114">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="cbb3b-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="cbb3b-115">Kiracının ve abonelik görünen adlarının kaynak sayısını görüntüleyen bir sorgu.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="cbb3b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbb3b-116">PARAMETERS</span></span>

### <span data-ttu-id="cbb3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbb3b-117">-DefaultProfile</span></span>
<span data-ttu-id="cbb3b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbb3b-119">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="cbb3b-119">-Query</span></span>
<span data-ttu-id="cbb3b-120">Kaynak Grafiği sorgusu.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-120">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbb3b-121">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="cbb3b-121">-Subscription</span></span>
<span data-ttu-id="cbb3b-122">Sorgu çalıştırmada kullanılacak abonelikler.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="cbb3b-123">-Atla</span><span class="sxs-lookup"><span data-stu-id="cbb3b-123">-Skip</span></span>
<span data-ttu-id="cbb3b-124">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="cbb3b-125">-Önce</span><span class="sxs-lookup"><span data-stu-id="cbb3b-125">-First</span></span>
<span data-ttu-id="cbb3b-126">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-126">The maximum number of objects to return.</span></span> <span data-ttu-id="cbb3b-127">İzin verilen değerler: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="cbb3b-128">Varsayılan değer 100 ' dır.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-128">Default value is 100.</span></span>

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

### <span data-ttu-id="cbb3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb3b-129">CommonParameters</span></span>
<span data-ttu-id="cbb3b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbb3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb3b-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbb3b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb3b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbb3b-132">INPUTS</span></span>

### <span data-ttu-id="cbb3b-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cbb3b-133">None</span></span>

## <span data-ttu-id="cbb3b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbb3b-134">OUTPUTS</span></span>

### <span data-ttu-id="cbb3b-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="cbb3b-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cbb3b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbb3b-136">NOTES</span></span>

## <span data-ttu-id="cbb3b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbb3b-137">RELATED LINKS</span></span>
