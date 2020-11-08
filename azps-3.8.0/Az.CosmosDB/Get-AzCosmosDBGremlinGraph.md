---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104122"
---
# <span data-ttu-id="bda41-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="bda41-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="bda41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bda41-102">SYNOPSIS</span></span>
<span data-ttu-id="bda41-103">CosmosDB Gremlın grafiğini alır.</span><span class="sxs-lookup"><span data-stu-id="bda41-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="bda41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bda41-104">SYNTAX</span></span>

### <span data-ttu-id="bda41-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bda41-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="bda41-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bda41-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bda41-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bda41-107">DESCRIPTION</span></span>
<span data-ttu-id="bda41-108">**Get-AzCosmosDBGremlinGraph** cmdlet 'ı Cosmosdb Gremlın grafik özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="bda41-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="bda41-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bda41-109">EXAMPLES</span></span>

### <span data-ttu-id="bda41-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bda41-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="bda41-111">Kaynak nesnesi ındexingpolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts _etag içerir.</span><span class="sxs-lookup"><span data-stu-id="bda41-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="bda41-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bda41-112">PARAMETERS</span></span>

### <span data-ttu-id="bda41-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bda41-113">-AccountName</span></span>
<span data-ttu-id="bda41-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="bda41-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda41-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bda41-115">-DatabaseName</span></span>
<span data-ttu-id="bda41-116">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="bda41-116">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda41-117">-DefaultProfile</span></span>
<span data-ttu-id="bda41-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bda41-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bda41-119">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="bda41-119">-Detailed</span></span>
<span data-ttu-id="bda41-120">Sağlanmışsa, cmdlet, ilgili üretilen iş değerini içeren Gremlın grafiğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="bda41-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda41-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bda41-121">-InputObject</span></span>
<span data-ttu-id="bda41-122">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bda41-122">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bda41-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="bda41-123">-Name</span></span>
<span data-ttu-id="bda41-124">Gremlın grafik adı.</span><span class="sxs-lookup"><span data-stu-id="bda41-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="bda41-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda41-125">-ResourceGroupName</span></span>
<span data-ttu-id="bda41-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bda41-126">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda41-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda41-127">CommonParameters</span></span>
<span data-ttu-id="bda41-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bda41-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda41-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bda41-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda41-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bda41-130">INPUTS</span></span>

### <span data-ttu-id="bda41-131">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bda41-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="bda41-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bda41-132">OUTPUTS</span></span>

### <span data-ttu-id="bda41-133">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="bda41-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="bda41-134">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bda41-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bda41-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bda41-135">NOTES</span></span>

## <span data-ttu-id="bda41-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bda41-136">RELATED LINKS</span></span>
