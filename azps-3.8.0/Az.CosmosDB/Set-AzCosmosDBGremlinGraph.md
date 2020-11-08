---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104438"
---
# <span data-ttu-id="fbf69-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="fbf69-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="fbf69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbf69-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf69-103">CosmosDB Gremlın grafiğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fbf69-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="fbf69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbf69-104">SYNTAX</span></span>

### <span data-ttu-id="fbf69-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fbf69-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf69-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbf69-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbf69-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbf69-107">DESCRIPTION</span></span>
<span data-ttu-id="fbf69-108">**Set-AzCosmosDBGremlinGraph** cmdlet 'ı Cosmosdb Gremlın grafiğini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fbf69-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="fbf69-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbf69-109">EXAMPLES</span></span>

### <span data-ttu-id="fbf69-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fbf69-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="fbf69-111">Kaynak nesnesi ındexingpolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts _etag içerir.</span><span class="sxs-lookup"><span data-stu-id="fbf69-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="fbf69-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbf69-112">PARAMETERS</span></span>

### <span data-ttu-id="fbf69-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fbf69-113">-AccountName</span></span>
<span data-ttu-id="fbf69-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="fbf69-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fbf69-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbf69-115">-Confirm</span></span>
<span data-ttu-id="fbf69-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbf69-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fbf69-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="fbf69-118">PSConflictResolutionPolicy türünde ConflictResolutionPolicy nesnesi, kapsayıcının ConflictResolutionPolicy olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="fbf69-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="fbf69-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="fbf69-120">Şu değerlere sahip olabilir: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="fbf69-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="fbf69-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="fbf69-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="fbf69-122">Tür Lastwriterwıns olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="fbf69-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="fbf69-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="fbf69-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="fbf69-124">Türü özel olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="fbf69-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="fbf69-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbf69-125">-DatabaseName</span></span>
<span data-ttu-id="fbf69-126">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="fbf69-126">Database name.</span></span>

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

### <span data-ttu-id="fbf69-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf69-127">-DefaultProfile</span></span>
<span data-ttu-id="fbf69-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fbf69-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbf69-129">-Indexingpolicy</span><span class="sxs-lookup"><span data-stu-id="fbf69-129">-IndexingPolicy</span></span>
<span data-ttu-id="fbf69-130">Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy türündeki Dizin Ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fbf69-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbf69-131">-InputObject</span></span>
<span data-ttu-id="fbf69-132">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fbf69-132">Gremlin Database object.</span></span>

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

### <span data-ttu-id="fbf69-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="fbf69-133">-Name</span></span>
<span data-ttu-id="fbf69-134">Gremlın grafik adı.</span><span class="sxs-lookup"><span data-stu-id="fbf69-134">Gremlin Graph Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-135">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="fbf69-135">-PartitionKeyKind</span></span>
<span data-ttu-id="fbf69-136">Bölümlemek için kullanılan algoritma türü.</span><span class="sxs-lookup"><span data-stu-id="fbf69-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="fbf69-137">Olası değerler: ' hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="fbf69-137">Possible values include: 'Hash', 'Range'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="fbf69-138">-PartitionKeyPath</span></span>
<span data-ttu-id="fbf69-139">Bölüm anahtarı yolu, örneğin, '/adres/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="fbf69-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-140">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="fbf69-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="fbf69-141">Bölüm anahtarı tanımının sürümü</span><span class="sxs-lookup"><span data-stu-id="fbf69-141">The version of the partition key definition</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf69-142">-ResourceGroupName</span></span>
<span data-ttu-id="fbf69-143">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fbf69-143">Name of resource group.</span></span>

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

### <span data-ttu-id="fbf69-144">-Üretim</span><span class="sxs-lookup"><span data-stu-id="fbf69-144">-Throughput</span></span>
<span data-ttu-id="fbf69-145">Gremlın grafiğinin (RU/s) miktarı.</span><span class="sxs-lookup"><span data-stu-id="fbf69-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="fbf69-146">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="fbf69-146">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-147">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="fbf69-147">-TtlInSeconds</span></span>
<span data-ttu-id="fbf69-148">Varsayılan TTL (saniye).</span><span class="sxs-lookup"><span data-stu-id="fbf69-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="fbf69-149">Değer eksik veya-1 olarak ayarlanmışsa, öğelerin süresi dolmasın.</span><span class="sxs-lookup"><span data-stu-id="fbf69-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="fbf69-150">Değer n olarak ayarlanırsa, son değiştirilme saatinden sonraki öğelerin süresi n saniye dolacak.</span><span class="sxs-lookup"><span data-stu-id="fbf69-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="fbf69-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="fbf69-152">Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy türünde UniqueKeyPolicy nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fbf69-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbf69-153">-WhatIf</span></span>
<span data-ttu-id="fbf69-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbf69-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbf69-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbf69-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf69-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf69-156">CommonParameters</span></span>
<span data-ttu-id="fbf69-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbf69-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf69-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fbf69-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf69-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbf69-159">INPUTS</span></span>

### <span data-ttu-id="fbf69-160">Microsoft. Azure. Commands. CosmosDB. modeller. Psındexingpolicy</span><span class="sxs-lookup"><span data-stu-id="fbf69-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="fbf69-161">Microsoft. Azure. Commands. CosmosDB. modeller. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="fbf69-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="fbf69-162">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fbf69-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="fbf69-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbf69-163">OUTPUTS</span></span>

### <span data-ttu-id="fbf69-164">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="fbf69-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="fbf69-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbf69-165">NOTES</span></span>

## <span data-ttu-id="fbf69-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbf69-166">RELATED LINKS</span></span>
