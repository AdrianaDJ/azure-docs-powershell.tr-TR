---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321558"
---
# <span data-ttu-id="1d261-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="1d261-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="1d261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d261-102">SYNOPSIS</span></span>
<span data-ttu-id="1d261-103">Yeni bir CosmosDB Gremlın grafiği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d261-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1d261-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d261-104">SYNTAX</span></span>

### <span data-ttu-id="1d261-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1d261-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d261-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d261-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d261-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d261-107">DESCRIPTION</span></span>
<span data-ttu-id="1d261-108">Yeni bir CosmosDB Gremlın grafiği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d261-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="1d261-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d261-109">EXAMPLES</span></span>

### <span data-ttu-id="1d261-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1d261-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="1d261-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d261-111">PARAMETERS</span></span>

### <span data-ttu-id="1d261-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d261-112">-AccountName</span></span>
<span data-ttu-id="1d261-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="1d261-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d261-114">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="1d261-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1d261-115">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="1d261-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1d261-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d261-116">-Confirm</span></span>
<span data-ttu-id="1d261-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d261-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d261-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1d261-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="1d261-119">PSConflictResolutionPolicy türünde ConflictResolutionPolicy nesnesi, kapsayıcının ConflictResolutionPolicy olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1d261-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="1d261-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="1d261-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="1d261-121">Şu değerlere sahip olabilir: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="1d261-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="1d261-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="1d261-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="1d261-123">Tür Lastwriterwıns olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="1d261-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="1d261-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="1d261-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="1d261-125">Türü özel olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="1d261-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="1d261-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d261-126">-DatabaseName</span></span>
<span data-ttu-id="1d261-127">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="1d261-127">Database name.</span></span>

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

### <span data-ttu-id="1d261-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d261-128">-DefaultProfile</span></span>
<span data-ttu-id="1d261-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d261-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d261-130">-Indexingpolicy</span><span class="sxs-lookup"><span data-stu-id="1d261-130">-IndexingPolicy</span></span>
<span data-ttu-id="1d261-131">Microsoft. Azure. Commands. CosmosDB. Psındexingpolicy türünde Dizin Ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1d261-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="1d261-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d261-132">-Name</span></span>
<span data-ttu-id="1d261-133">Gremlın grafik adı.</span><span class="sxs-lookup"><span data-stu-id="1d261-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="1d261-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1d261-134">-ParentObject</span></span>
<span data-ttu-id="1d261-135">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1d261-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="1d261-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="1d261-136">-PartitionKeyKind</span></span>
<span data-ttu-id="1d261-137">Bölümlemek için kullanılan algoritma türü.</span><span class="sxs-lookup"><span data-stu-id="1d261-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="1d261-138">Olası değerler: ' hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="1d261-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="1d261-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="1d261-139">-PartitionKeyPath</span></span>
<span data-ttu-id="1d261-140">Bölüm anahtarı yolu, örneğin, '/adres/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="1d261-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="1d261-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="1d261-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="1d261-142">Bölüm anahtarı tanımının sürümü</span><span class="sxs-lookup"><span data-stu-id="1d261-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="1d261-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d261-143">-ResourceGroupName</span></span>
<span data-ttu-id="1d261-144">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1d261-144">Name of resource group.</span></span>

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

### <span data-ttu-id="1d261-145">-Üretim</span><span class="sxs-lookup"><span data-stu-id="1d261-145">-Throughput</span></span>
<span data-ttu-id="1d261-146">Gremlın grafiğinin (RU/s) miktarı.</span><span class="sxs-lookup"><span data-stu-id="1d261-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="1d261-147">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="1d261-147">Default value is 400.</span></span>

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

### <span data-ttu-id="1d261-148">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="1d261-148">-TtlInSeconds</span></span>
<span data-ttu-id="1d261-149">Varsayılan TTL (saniye).</span><span class="sxs-lookup"><span data-stu-id="1d261-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="1d261-150">Değer eksik veya-1 olarak ayarlanmışsa, öğelerin süresi dolmasın.</span><span class="sxs-lookup"><span data-stu-id="1d261-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="1d261-151">Değer n olarak ayarlanırsa, son değiştirilme saatinden sonraki öğelerin süresi n saniye dolacak.</span><span class="sxs-lookup"><span data-stu-id="1d261-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="1d261-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="1d261-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="1d261-153">Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy türünde UniqueKeyPolicy nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1d261-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="1d261-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d261-154">-WhatIf</span></span>
<span data-ttu-id="1d261-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d261-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d261-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d261-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d261-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d261-157">CommonParameters</span></span>
<span data-ttu-id="1d261-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d261-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d261-159">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1d261-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d261-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d261-160">INPUTS</span></span>

### <span data-ttu-id="1d261-161">Microsoft. Azure. Commands. CosmosDB. modeller. Psındexingpolicy</span><span class="sxs-lookup"><span data-stu-id="1d261-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="1d261-162">Microsoft. Azure. Commands. CosmosDB. modeller. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="1d261-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="1d261-163">Microsoft. Azure. Commands. CosmosDB. modeller. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="1d261-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="1d261-164">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1d261-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="1d261-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d261-165">OUTPUTS</span></span>

### <span data-ttu-id="1d261-166">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="1d261-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="1d261-167">System. Exception</span><span class="sxs-lookup"><span data-stu-id="1d261-167">System.Exception</span></span>

## <span data-ttu-id="1d261-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d261-168">NOTES</span></span>

## <span data-ttu-id="1d261-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d261-169">RELATED LINKS</span></span>
