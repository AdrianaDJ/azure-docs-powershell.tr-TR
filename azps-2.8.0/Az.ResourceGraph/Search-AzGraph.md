---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: 5a9a47ff6f4a329d3e48ec54df85ade3be5ae84d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932609"
---
# <span data-ttu-id="548b0-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="548b0-101">Search-AzGraph</span></span>

## <span data-ttu-id="548b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="548b0-102">SYNOPSIS</span></span>
<span data-ttu-id="548b0-103">Azure Resource Manager tarafından yönetilen kaynakları sorgular.</span><span class="sxs-lookup"><span data-stu-id="548b0-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="548b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="548b0-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="548b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="548b0-105">DESCRIPTION</span></span>
<span data-ttu-id="548b0-106">Sorgu söz dizimi hakkında daha fazla bilgi edinin: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="548b0-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="548b0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="548b0-107">EXAMPLES</span></span>

### <span data-ttu-id="548b0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="548b0-108">Example 1</span></span>
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

<span data-ttu-id="548b0-109">Basit kaynaklar kaynak alanlarının alt kümesini isteyen sorgu.</span><span class="sxs-lookup"><span data-stu-id="548b0-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="548b0-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="548b0-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="548b0-111">Alan seçimi, filtreleme ve özetleme özelliklerine sahip kaynaklar üzerinde karmaşık bir sorgu.</span><span class="sxs-lookup"><span data-stu-id="548b0-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="548b0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="548b0-112">PARAMETERS</span></span>

### <span data-ttu-id="548b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548b0-113">-DefaultProfile</span></span>
<span data-ttu-id="548b0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="548b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="548b0-115">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="548b0-115">-Query</span></span>
<span data-ttu-id="548b0-116">Kaynak Grafiği sorgusu.</span><span class="sxs-lookup"><span data-stu-id="548b0-116">Resource Graph query.</span></span>

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

### <span data-ttu-id="548b0-117">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="548b0-117">-Subscription</span></span>
<span data-ttu-id="548b0-118">Sorgu çalıştırmada kullanılacak abonelikler.</span><span class="sxs-lookup"><span data-stu-id="548b0-118">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="548b0-119">-Atla</span><span class="sxs-lookup"><span data-stu-id="548b0-119">-Skip</span></span>
<span data-ttu-id="548b0-120">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="548b0-120">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="548b0-121">-Önce</span><span class="sxs-lookup"><span data-stu-id="548b0-121">-First</span></span>
<span data-ttu-id="548b0-122">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="548b0-122">The maximum number of objects to return.</span></span> <span data-ttu-id="548b0-123">İzin verilen değerler: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="548b0-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="548b0-124">Varsayılan değer 100 ' dır.</span><span class="sxs-lookup"><span data-stu-id="548b0-124">Default value is 100.</span></span>

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

### <span data-ttu-id="548b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548b0-125">CommonParameters</span></span>
<span data-ttu-id="548b0-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="548b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548b0-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548b0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548b0-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="548b0-128">INPUTS</span></span>

### <span data-ttu-id="548b0-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="548b0-129">None</span></span>

## <span data-ttu-id="548b0-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="548b0-130">OUTPUTS</span></span>

### <span data-ttu-id="548b0-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="548b0-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="548b0-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="548b0-132">NOTES</span></span>

## <span data-ttu-id="548b0-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="548b0-133">RELATED LINKS</span></span>
