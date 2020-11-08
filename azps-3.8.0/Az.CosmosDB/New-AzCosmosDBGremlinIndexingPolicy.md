---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinIndexingPolicy.md
ms.openlocfilehash: 10a928be0827f280d7fe00a1307535dbad6eda1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097562"
---
# <span data-ttu-id="676d5-101">New-AzCosmosDBGremlinIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="676d5-101">New-AzCosmosDBGremlinIndexingPolicy</span></span>

## <span data-ttu-id="676d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="676d5-102">SYNOPSIS</span></span>
<span data-ttu-id="676d5-103">Yeni bir CosmosDB ındexingpolicy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="676d5-103">Creates a new CosmosDB IndexingPolicy object.</span></span>

## <span data-ttu-id="676d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="676d5-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="676d5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="676d5-105">DESCRIPTION</span></span>
<span data-ttu-id="676d5-106">**New-Azcosmosdbgremlinındexingpolicy** cmdlet 'ı Psındexingpolicy türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="676d5-106">The **New-AzCosmosDBGremlinIndexingPolicy** cmdlet creates a new object of type PSIndexingPolicy.</span></span>

## <span data-ttu-id="676d5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="676d5-107">EXAMPLES</span></span>

### <span data-ttu-id="676d5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="676d5-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $ipath2 = New-AzCosmosDBGremlinIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\>> $IncludedPath = New-AzCosmosDBGremlinIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>>  $SpatialSpec = New-AzCosmosDBGremlinSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\>> $cp1 = New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending
PS C:\>>  $cp2 = New-AzCosmosDBGremlinCompositePath -Path "/aberc" -Order Descending
PS C:\>> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\>> New-AzCosmosDBGremlinIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent


Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

<span data-ttu-id="676d5-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="676d5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="676d5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="676d5-110">PARAMETERS</span></span>

### <span data-ttu-id="676d5-111">-Otomatik</span><span class="sxs-lookup"><span data-stu-id="676d5-111">-Automatic</span></span>
<span data-ttu-id="676d5-112">Boole, Dizin ilkesinin otomatik olup olmadığını belirtecek şekilde</span><span class="sxs-lookup"><span data-stu-id="676d5-112">Bool to indicate if the indexing policy is automatic</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676d5-113">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="676d5-113">-CompositePath</span></span>
<span data-ttu-id="676d5-114">Microsoft. Azure. Commands. CosmosDB. PSCompositePath türünde nesneler dizisi dizisi</span><span class="sxs-lookup"><span data-stu-id="676d5-114">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

```yaml
Type: PSCompositePath[][]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="676d5-115">-DefaultProfile</span></span>
<span data-ttu-id="676d5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="676d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676d5-117">-Excludedyolu</span><span class="sxs-lookup"><span data-stu-id="676d5-117">-ExcludedPath</span></span>
<span data-ttu-id="676d5-118">ExcludedPath içeren dizeler dizisi (Azure Cosmos DB hizmetinde dışlanacak bir JSON belgesi içindeki bir yol belirtir.)  öðelerinin.</span><span class="sxs-lookup"><span data-stu-id="676d5-118">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="676d5-119">-Includedyol</span><span class="sxs-lookup"><span data-stu-id="676d5-119">-IncludedPath</span></span>
<span data-ttu-id="676d5-120">Includedpath içeren dizeler dizisi (Azure Cosmos DB hizmeti.) öğelerine eklenecek bir JSON belgesi içindeki bir yol belirtir.</span><span class="sxs-lookup"><span data-stu-id="676d5-120">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

```yaml
Type: PSIncludedPath[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676d5-121">-Indexingmode</span><span class="sxs-lookup"><span data-stu-id="676d5-121">-IndexingMode</span></span>
<span data-ttu-id="676d5-122">Dizin oluşturma modunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="676d5-122">Indicates the indexing mode.</span></span>
<span data-ttu-id="676d5-123">Olası değerler: ' tutarlı ', ' Lazy ', ' none '</span><span class="sxs-lookup"><span data-stu-id="676d5-123">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="676d5-124">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="676d5-124">-SpatialSpec</span></span>
<span data-ttu-id="676d5-125">Microsoft. Azure. Commands. CosmosDB. Psshaalspec türünde nesneler dizisi</span><span class="sxs-lookup"><span data-stu-id="676d5-125">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

```yaml
Type: PSSpatialSpec[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="676d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="676d5-126">CommonParameters</span></span>
<span data-ttu-id="676d5-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="676d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="676d5-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="676d5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="676d5-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="676d5-129">INPUTS</span></span>

### <span data-ttu-id="676d5-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="676d5-130">None</span></span>

## <span data-ttu-id="676d5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="676d5-131">OUTPUTS</span></span>

### <span data-ttu-id="676d5-132">Microsoft. Azure. Commands. CosmosDB. modeller. Psındexingpolicy</span><span class="sxs-lookup"><span data-stu-id="676d5-132">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

## <span data-ttu-id="676d5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="676d5-133">NOTES</span></span>

## <span data-ttu-id="676d5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="676d5-134">RELATED LINKS</span></span>