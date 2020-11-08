---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlindexingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIndexingPolicy.md
ms.openlocfilehash: cb8ecea538273adf9db14168a3b60d5679536cda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103630"
---
# <span data-ttu-id="6f5ac-101">New-AzCosmosDBSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="6f5ac-101">New-AzCosmosDBSqlIndexingPolicy</span></span>

## <span data-ttu-id="6f5ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f5ac-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5ac-103">Yeni bir CosmosDB SQL ındexingpolicy nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6f5ac-103">Creates a new CosmosDB Sql IndexingPolicy object.</span></span>

## <span data-ttu-id="6f5ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f5ac-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlIndexingPolicy [-IncludedPath <PSIncludedPath[]>] [-SpatialSpec <PSSpatialSpec[]>]
 [-CompositePath <PSCompositePath[][]>] [-ExcludedPath <String[]>] [-Automatic <Boolean>]
 [-IndexingMode <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f5ac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f5ac-105">DESCRIPTION</span></span>
<span data-ttu-id="6f5ac-106">**New-AzCosmosDBSqlIndexingPolicy** cmdlet 'ı PSSqlIndexingPolicy türünde yeni bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6f5ac-106">The **New-AzCosmosDBSqlIndexingPolicy** cmdlet creates a new object of type PSSqlIndexingPolicy.</span></span>

## <span data-ttu-id="6f5ac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f5ac-107">EXAMPLES</span></span>

### <span data-ttu-id="6f5ac-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6f5ac-108">Example 1</span></span>
```powershell
PS C:\> $ipath1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $ipath2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
PS C:\> $IncludedPath = New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $ipath1, $ipath2
PS C:\>  $SpatialSpec = New-AzCosmosDBSqlSpatialSpec -Path  "/mySpatialPath/*" -Type  "Point", "LineString", "Polygon", "MultiPolygon"
PS C:\> $cp1 = New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending
PS C:\>  $cp2 = New-AzCosmosDBSqlCompositePath -Path "/aberc" -Order Descending
PS C:\> $compositePath = (($cp1, $cp2), ($cp2, $cp1))
PS C:\> New-AzCosmosDBSqlIndexingPolicy -IncludedPath $IncludedPath -SpatialSpec $SpatialSpec -CompositePath $compositePath -ExcludedPath "/myPathToNotIndex/*" -Automatic 1 -IndexingMode Consistent

Automatic        : True
IndexingMode     : Consistent
IncludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath}
ExcludedPaths    : {Microsoft.Azure.Commands.CosmosDB.Models.PSExcludedPath}
CompositeIndexes : {Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath,
                   Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath}
SpatialIndexes   : {Microsoft.Azure.Commands.CosmosDB.Models.PSSpatialSpec}
```

## <span data-ttu-id="6f5ac-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f5ac-109">PARAMETERS</span></span>

### <span data-ttu-id="6f5ac-110">-Otomatik</span><span class="sxs-lookup"><span data-stu-id="6f5ac-110">-Automatic</span></span>
<span data-ttu-id="6f5ac-111">Boole, Dizin ilkesinin otomatik olup olmadığını belirtecek şekilde</span><span class="sxs-lookup"><span data-stu-id="6f5ac-111">Bool to indicate if the indexing policy is automatic</span></span>

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

### <span data-ttu-id="6f5ac-112">-CompositePath</span><span class="sxs-lookup"><span data-stu-id="6f5ac-112">-CompositePath</span></span>
<span data-ttu-id="6f5ac-113">Microsoft. Azure. Commands. CosmosDB. PSCompositePath türünde nesneler dizisi dizisi</span><span class="sxs-lookup"><span data-stu-id="6f5ac-113">Array of array of objects of type Microsoft.Azure.Commands.CosmosDB.PSCompositePath</span></span>

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

### <span data-ttu-id="6f5ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5ac-114">-DefaultProfile</span></span>
<span data-ttu-id="6f5ac-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f5ac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f5ac-116">-Excludedyolu</span><span class="sxs-lookup"><span data-stu-id="6f5ac-116">-ExcludedPath</span></span>
<span data-ttu-id="6f5ac-117">ExcludedPath içeren dizeler dizisi (Azure Cosmos DB hizmetinde dışlanacak bir JSON belgesi içindeki bir yol belirtir.)  öðelerinin.</span><span class="sxs-lookup"><span data-stu-id="6f5ac-117">Array of strings containing excludedPath(Specifies a path within a JSON document to be excluded in the Azure Cosmos DB service.)  elements.</span></span>

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

### <span data-ttu-id="6f5ac-118">-Includedyol</span><span class="sxs-lookup"><span data-stu-id="6f5ac-118">-IncludedPath</span></span>
<span data-ttu-id="6f5ac-119">Includedpath içeren dizeler dizisi (Azure Cosmos DB hizmeti.) öğelerine eklenecek bir JSON belgesi içindeki bir yol belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f5ac-119">Array of strings containing includedPath (Specifies a path within a JSON document to be included in the Azure Cosmos DB service.) elements.</span></span>

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

### <span data-ttu-id="6f5ac-120">-Indexingmode</span><span class="sxs-lookup"><span data-stu-id="6f5ac-120">-IndexingMode</span></span>
<span data-ttu-id="6f5ac-121">Dizin oluşturma modunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f5ac-121">indicates the indexing mode.</span></span>
<span data-ttu-id="6f5ac-122">Olası değerler: ' tutarlı ', ' Lazy ', ' none '</span><span class="sxs-lookup"><span data-stu-id="6f5ac-122">Possible values include: 'Consistent', 'Lazy', 'None'</span></span>

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

### <span data-ttu-id="6f5ac-123">-SpatialSpec</span><span class="sxs-lookup"><span data-stu-id="6f5ac-123">-SpatialSpec</span></span>
<span data-ttu-id="6f5ac-124">Microsoft. Azure. Commands. CosmosDB. Psshaalspec türünde nesneler dizisi</span><span class="sxs-lookup"><span data-stu-id="6f5ac-124">Array of objects of type Microsoft.Azure.Commands.CosmosDB.PSSpatialSpec</span></span>

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

### <span data-ttu-id="6f5ac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5ac-125">CommonParameters</span></span>
<span data-ttu-id="6f5ac-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f5ac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5ac-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6f5ac-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5ac-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f5ac-128">INPUTS</span></span>

### <span data-ttu-id="6f5ac-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6f5ac-129">None</span></span>

## <span data-ttu-id="6f5ac-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f5ac-130">OUTPUTS</span></span>

### <span data-ttu-id="6f5ac-131">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="6f5ac-131">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

## <span data-ttu-id="6f5ac-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f5ac-132">NOTES</span></span>

## <span data-ttu-id="6f5ac-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f5ac-133">RELATED LINKS</span></span>
