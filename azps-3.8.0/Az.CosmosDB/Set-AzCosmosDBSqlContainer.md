---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104425"
---
# <span data-ttu-id="2f917-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="2f917-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="2f917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f917-102">SYNOPSIS</span></span>
<span data-ttu-id="2f917-103">Yeni bir CosmosDB SQL kapsayıcısını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2f917-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="2f917-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f917-104">SYNTAX</span></span>

### <span data-ttu-id="2f917-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f917-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f917-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f917-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f917-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f917-107">DESCRIPTION</span></span>
<span data-ttu-id="2f917-108">**Set-AzCosmosDBSqlContainer** cmdlet 'i, yeni bir</span><span class="sxs-lookup"><span data-stu-id="2f917-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="2f917-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f917-109">EXAMPLES</span></span>

### <span data-ttu-id="2f917-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2f917-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="2f917-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f917-111">PARAMETERS</span></span>

### <span data-ttu-id="2f917-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2f917-112">-AccountName</span></span>
<span data-ttu-id="2f917-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="2f917-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2f917-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="2f917-114">-Confirm</span></span>
<span data-ttu-id="2f917-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2f917-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f917-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="2f917-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="2f917-117">Pssdconflictresolutionpolicy türünde ConflictResolutionPolicy nesnesi, kapsayıcının ConflictResolutionPolicy olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="2f917-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="2f917-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="2f917-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="2f917-119">Şu değerlere sahip olabilir: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="2f917-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="2f917-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="2f917-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="2f917-121">Tür Lastwriterwıns olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="2f917-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="2f917-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="2f917-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="2f917-123">Türü özel olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="2f917-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="2f917-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2f917-124">-DatabaseName</span></span>
<span data-ttu-id="2f917-125">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="2f917-125">Database name.</span></span>

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

### <span data-ttu-id="2f917-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f917-126">-DefaultProfile</span></span>
<span data-ttu-id="2f917-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f917-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f917-128">-Indexingpolicy</span><span class="sxs-lookup"><span data-stu-id="2f917-128">-IndexingPolicy</span></span>
<span data-ttu-id="2f917-129">Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy türündeki Dizin Ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2f917-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="2f917-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f917-130">-InputObject</span></span>
<span data-ttu-id="2f917-131">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2f917-131">Sql Database object.</span></span>

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

### <span data-ttu-id="2f917-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="2f917-132">-Name</span></span>
<span data-ttu-id="2f917-133">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="2f917-133">Container name.</span></span>

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

### <span data-ttu-id="2f917-134">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="2f917-134">-PartitionKeyKind</span></span>
<span data-ttu-id="2f917-135">Bölümlemek için kullanılan algoritma türü.</span><span class="sxs-lookup"><span data-stu-id="2f917-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="2f917-136">Olası değerler: ' hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="2f917-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="2f917-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="2f917-137">-PartitionKeyPath</span></span>
<span data-ttu-id="2f917-138">Bölüm anahtarı yolu, örneğin, '/adres/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="2f917-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="2f917-139">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="2f917-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="2f917-140">Bölüm anahtarı tanımının sürümü</span><span class="sxs-lookup"><span data-stu-id="2f917-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="2f917-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f917-141">-ResourceGroupName</span></span>
<span data-ttu-id="2f917-142">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2f917-142">Name of resource group.</span></span>

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

### <span data-ttu-id="2f917-143">-Üretim</span><span class="sxs-lookup"><span data-stu-id="2f917-143">-Throughput</span></span>
<span data-ttu-id="2f917-144">SQL kapsayıcısının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="2f917-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="2f917-145">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="2f917-145">Default value is 400.</span></span>

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

### <span data-ttu-id="2f917-146">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="2f917-146">-TtlInSeconds</span></span>
<span data-ttu-id="2f917-147">Varsayılan TTL (saniye).</span><span class="sxs-lookup"><span data-stu-id="2f917-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="2f917-148">Değer eksik veya-1 olarak ayarlanmışsa, öğelerin süresi dolmasın.</span><span class="sxs-lookup"><span data-stu-id="2f917-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="2f917-149">Değer n olarak ayarlanırsa, son değiştirilme saatinden sonraki öğelerin süresi n saniye dolacak.</span><span class="sxs-lookup"><span data-stu-id="2f917-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="2f917-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="2f917-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="2f917-151">Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy türünde UniqueKeyPolicy nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2f917-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="2f917-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f917-152">-WhatIf</span></span>
<span data-ttu-id="2f917-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f917-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f917-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2f917-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f917-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f917-155">CommonParameters</span></span>
<span data-ttu-id="2f917-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f917-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f917-157">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2f917-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f917-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f917-158">INPUTS</span></span>

### <span data-ttu-id="2f917-159">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2f917-159">None</span></span>

## <span data-ttu-id="2f917-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f917-160">OUTPUTS</span></span>

### <span data-ttu-id="2f917-161">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2f917-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="2f917-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f917-162">NOTES</span></span>

## <span data-ttu-id="2f917-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f917-163">RELATED LINKS</span></span>
