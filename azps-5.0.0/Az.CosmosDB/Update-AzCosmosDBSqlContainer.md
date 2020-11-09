---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321345"
---
# <span data-ttu-id="14899-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="14899-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="14899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14899-102">SYNOPSIS</span></span>
<span data-ttu-id="14899-103">CosmosDB SQL kapsayıcısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="14899-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="14899-104">Var olan kapsayıcıyı okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="14899-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="14899-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14899-105">SYNTAX</span></span>

### <span data-ttu-id="14899-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="14899-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14899-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14899-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14899-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14899-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14899-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="14899-109">DESCRIPTION</span></span>
<span data-ttu-id="14899-110">CosmosDB SQL kapsayıcısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="14899-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="14899-111">Var olan kapsayıcıyı okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="14899-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="14899-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14899-112">EXAMPLES</span></span>

### <span data-ttu-id="14899-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="14899-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="14899-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14899-114">PARAMETERS</span></span>

### <span data-ttu-id="14899-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="14899-115">-AccountName</span></span>
<span data-ttu-id="14899-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="14899-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="14899-117">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="14899-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="14899-118">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="14899-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="14899-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="14899-119">-Confirm</span></span>
<span data-ttu-id="14899-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="14899-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14899-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="14899-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="14899-122">Pssdconflictresolutionpolicy türünde ConflictResolutionPolicy nesnesi, kapsayıcının ConflictResolutionPolicy olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="14899-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14899-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="14899-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="14899-124">Şu değerlere sahip olabilir: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="14899-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="14899-125">ConflictResolutionPolicy parametresiyle birlikte sağlanmışsa, yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="14899-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="14899-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="14899-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="14899-127">Tür Lastwriterwıns olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="14899-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="14899-128">ConflictResolutionPolicy parametresiyle birlikte sağlanmışsa, yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="14899-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="14899-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="14899-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="14899-130">Türü özel olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="14899-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="14899-131">ConflictResolutionPolicy parametresiyle birlikte sağlanmışsa, yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="14899-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="14899-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="14899-132">-DatabaseName</span></span>
<span data-ttu-id="14899-133">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="14899-133">Database name.</span></span>

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

### <span data-ttu-id="14899-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14899-134">-DefaultProfile</span></span>
<span data-ttu-id="14899-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14899-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14899-136">-Indexingpolicy</span><span class="sxs-lookup"><span data-stu-id="14899-136">-IndexingPolicy</span></span>
<span data-ttu-id="14899-137">Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy türündeki Dizin Ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="14899-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14899-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14899-138">-InputObject</span></span>
<span data-ttu-id="14899-139">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="14899-139">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14899-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="14899-140">-Name</span></span>
<span data-ttu-id="14899-141">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="14899-141">Container name.</span></span>

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

### <span data-ttu-id="14899-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="14899-142">-ParentObject</span></span>
<span data-ttu-id="14899-143">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="14899-143">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14899-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="14899-144">-PartitionKeyKind</span></span>
<span data-ttu-id="14899-145">Bölümlemek için kullanılan algoritma türü.</span><span class="sxs-lookup"><span data-stu-id="14899-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="14899-146">Olası değerler: ' hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="14899-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="14899-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="14899-147">-PartitionKeyPath</span></span>
<span data-ttu-id="14899-148">Bölüm anahtarı yolu, örneğin, '/adres/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="14899-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="14899-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="14899-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="14899-150">Bölüm anahtarı tanımının sürümü</span><span class="sxs-lookup"><span data-stu-id="14899-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="14899-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14899-151">-ResourceGroupName</span></span>
<span data-ttu-id="14899-152">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="14899-152">Name of resource group.</span></span>

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

### <span data-ttu-id="14899-153">-Üretim</span><span class="sxs-lookup"><span data-stu-id="14899-153">-Throughput</span></span>
<span data-ttu-id="14899-154">SQL kapsayıcısının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="14899-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="14899-155">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="14899-155">Default value is 400.</span></span>

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

### <span data-ttu-id="14899-156">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="14899-156">-TtlInSeconds</span></span>
<span data-ttu-id="14899-157">Varsayılan TTL (saniye).</span><span class="sxs-lookup"><span data-stu-id="14899-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="14899-158">Değer eksik veya-1 olarak ayarlanmışsa, öğelerin süresi dolmasın.</span><span class="sxs-lookup"><span data-stu-id="14899-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="14899-159">Değer n olarak ayarlanırsa, son değiştirilme saatinden sonraki öğelerin süresi n saniye dolacak.</span><span class="sxs-lookup"><span data-stu-id="14899-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="14899-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="14899-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="14899-161">Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy türünde UniqueKeyPolicy nesnesi.</span><span class="sxs-lookup"><span data-stu-id="14899-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14899-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14899-162">-WhatIf</span></span>
<span data-ttu-id="14899-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14899-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14899-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="14899-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14899-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14899-165">CommonParameters</span></span>
<span data-ttu-id="14899-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14899-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14899-167">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="14899-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14899-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14899-168">INPUTS</span></span>

### <span data-ttu-id="14899-169">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="14899-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="14899-170">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="14899-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="14899-171">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="14899-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="14899-172">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="14899-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="14899-173">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="14899-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="14899-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14899-174">OUTPUTS</span></span>

### <span data-ttu-id="14899-175">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="14899-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="14899-176">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="14899-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="14899-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14899-177">NOTES</span></span>

## <span data-ttu-id="14899-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14899-178">RELATED LINKS</span></span>
