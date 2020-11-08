---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275077"
---
# <span data-ttu-id="78e4c-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="78e4c-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="78e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="78e4c-103">CosmosDB Gremlın grafiğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="78e4c-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="78e4c-104">Var olan grafiği okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="78e4c-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="78e4c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78e4c-105">SYNTAX</span></span>

### <span data-ttu-id="78e4c-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="78e4c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78e4c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e4c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78e4c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e4c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78e4c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="78e4c-109">DESCRIPTION</span></span>
<span data-ttu-id="78e4c-110">CosmosDB Gremlın grafiğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="78e4c-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="78e4c-111">Var olan grafiği okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="78e4c-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="78e4c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78e4c-112">EXAMPLES</span></span>

### <span data-ttu-id="78e4c-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="78e4c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="78e4c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78e4c-114">PARAMETERS</span></span>

### <span data-ttu-id="78e4c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78e4c-115">-AccountName</span></span>
<span data-ttu-id="78e4c-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="78e4c-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="78e4c-117">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="78e4c-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="78e4c-118">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="78e4c-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="78e4c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="78e4c-119">-Confirm</span></span>
<span data-ttu-id="78e4c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="78e4c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78e4c-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="78e4c-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="78e4c-122">PSConflictResolutionPolicy türünde ConflictResolutionPolicy nesnesi, kapsayıcının ConflictResolutionPolicy olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="78e4c-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="78e4c-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="78e4c-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="78e4c-124">Şu değerlere sahip olabilir: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="78e4c-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="78e4c-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="78e4c-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="78e4c-126">Tür Lastwriterwıns olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="78e4c-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="78e4c-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="78e4c-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="78e4c-128">Türü özel olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="78e4c-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="78e4c-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78e4c-129">-DatabaseName</span></span>
<span data-ttu-id="78e4c-130">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="78e4c-130">Database name.</span></span>

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

### <span data-ttu-id="78e4c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e4c-131">-DefaultProfile</span></span>
<span data-ttu-id="78e4c-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78e4c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78e4c-133">-Indexingpolicy</span><span class="sxs-lookup"><span data-stu-id="78e4c-133">-IndexingPolicy</span></span>
<span data-ttu-id="78e4c-134">Microsoft. Azure. Commands. CosmosDB. Psındexingpolicy türünde Dizin Ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="78e4c-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="78e4c-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78e4c-135">-InputObject</span></span>
<span data-ttu-id="78e4c-136">Gremlın grafik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="78e4c-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78e4c-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="78e4c-137">-Name</span></span>
<span data-ttu-id="78e4c-138">Gremlın grafik adı.</span><span class="sxs-lookup"><span data-stu-id="78e4c-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="78e4c-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="78e4c-139">-ParentObject</span></span>
<span data-ttu-id="78e4c-140">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="78e4c-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="78e4c-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="78e4c-141">-PartitionKeyKind</span></span>
<span data-ttu-id="78e4c-142">Bölümlemek için kullanılan algoritma türü.</span><span class="sxs-lookup"><span data-stu-id="78e4c-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="78e4c-143">Olası değerler: ' hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="78e4c-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="78e4c-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="78e4c-144">-PartitionKeyPath</span></span>
<span data-ttu-id="78e4c-145">Bölüm anahtarı yolu, örneğin, '/adres/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="78e4c-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="78e4c-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="78e4c-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="78e4c-147">Bölüm anahtarı tanımının sürümü</span><span class="sxs-lookup"><span data-stu-id="78e4c-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="78e4c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e4c-148">-ResourceGroupName</span></span>
<span data-ttu-id="78e4c-149">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="78e4c-149">Name of resource group.</span></span>

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

### <span data-ttu-id="78e4c-150">-Üretim</span><span class="sxs-lookup"><span data-stu-id="78e4c-150">-Throughput</span></span>
<span data-ttu-id="78e4c-151">Gremlın grafiğinin (RU/s) miktarı.</span><span class="sxs-lookup"><span data-stu-id="78e4c-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="78e4c-152">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="78e4c-152">Default value is 400.</span></span>

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

### <span data-ttu-id="78e4c-153">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="78e4c-153">-TtlInSeconds</span></span>
<span data-ttu-id="78e4c-154">Varsayılan TTL (saniye).</span><span class="sxs-lookup"><span data-stu-id="78e4c-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="78e4c-155">Değer eksik veya-1 olarak ayarlanmışsa, öğelerin süresi dolmasın.</span><span class="sxs-lookup"><span data-stu-id="78e4c-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="78e4c-156">Değer n olarak ayarlanırsa, son değiştirilme saatinden sonraki öğelerin süresi n saniye dolacak.</span><span class="sxs-lookup"><span data-stu-id="78e4c-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="78e4c-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="78e4c-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="78e4c-158">Microsoft. Azure. Commands. CosmosDB. PSUniqueKeyPolicy türünde UniqueKeyPolicy nesnesi.</span><span class="sxs-lookup"><span data-stu-id="78e4c-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="78e4c-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78e4c-159">-WhatIf</span></span>
<span data-ttu-id="78e4c-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="78e4c-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78e4c-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="78e4c-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78e4c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e4c-162">CommonParameters</span></span>
<span data-ttu-id="78e4c-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78e4c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e4c-164">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="78e4c-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e4c-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78e4c-165">INPUTS</span></span>

### <span data-ttu-id="78e4c-166">Microsoft. Azure. Commands. CosmosDB. modeller. Psındexingpolicy</span><span class="sxs-lookup"><span data-stu-id="78e4c-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="78e4c-167">Microsoft. Azure. Commands. CosmosDB. modeller. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="78e4c-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="78e4c-168">Microsoft. Azure. Commands. CosmosDB. modeller. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="78e4c-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="78e4c-169">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="78e4c-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="78e4c-170">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="78e4c-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="78e4c-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78e4c-171">OUTPUTS</span></span>

### <span data-ttu-id="78e4c-172">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="78e4c-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="78e4c-173">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="78e4c-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="78e4c-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78e4c-174">NOTES</span></span>

## <span data-ttu-id="78e4c-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78e4c-175">RELATED LINKS</span></span>
