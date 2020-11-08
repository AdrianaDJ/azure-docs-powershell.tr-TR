---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108373"
---
# <span data-ttu-id="0182e-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="0182e-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="0182e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0182e-102">SYNOPSIS</span></span>
<span data-ttu-id="0182e-103">Yeni bir CosmosDB SQL kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0182e-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="0182e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0182e-104">SYNTAX</span></span>

### <span data-ttu-id="0182e-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0182e-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0182e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0182e-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0182e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0182e-107">DESCRIPTION</span></span>
<span data-ttu-id="0182e-108">Yeni bir CosmosDB SQL kapsayıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0182e-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="0182e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0182e-109">EXAMPLES</span></span>

### <span data-ttu-id="0182e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0182e-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="0182e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0182e-111">PARAMETERS</span></span>

### <span data-ttu-id="0182e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0182e-112">-AccountName</span></span>
<span data-ttu-id="0182e-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="0182e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0182e-114">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="0182e-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0182e-115">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="0182e-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0182e-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="0182e-116">-Confirm</span></span>
<span data-ttu-id="0182e-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0182e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0182e-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0182e-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="0182e-119">Pssdconflictresolutionpolicy türünde ConflictResolutionPolicy nesnesi, kapsayıcının ConflictResolutionPolicy olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="0182e-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="0182e-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="0182e-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="0182e-121">Şu değerlere sahip olabilir: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="0182e-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="0182e-122">ConflictResolutionPolicy parametresiyle birlikte sağlanmışsa, yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="0182e-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="0182e-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="0182e-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="0182e-124">Tür Lastwriterwıns olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="0182e-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="0182e-125">ConflictResolutionPolicy parametresiyle birlikte sağlanmışsa, yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="0182e-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="0182e-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="0182e-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="0182e-127">Türü özel olduğunda sağlanacak şekilde.</span><span class="sxs-lookup"><span data-stu-id="0182e-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="0182e-128">ConflictResolutionPolicy parametresiyle birlikte sağlanmışsa, yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="0182e-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="0182e-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0182e-129">-DatabaseName</span></span>
<span data-ttu-id="0182e-130">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="0182e-130">Database name.</span></span>

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

### <span data-ttu-id="0182e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0182e-131">-DefaultProfile</span></span>
<span data-ttu-id="0182e-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0182e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0182e-133">-Indexingpolicy</span><span class="sxs-lookup"><span data-stu-id="0182e-133">-IndexingPolicy</span></span>
<span data-ttu-id="0182e-134">Microsoft. Azure. Commands. CosmosDB. PSSqlIndexingPolicy türündeki Dizin Ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0182e-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="0182e-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="0182e-135">-Name</span></span>
<span data-ttu-id="0182e-136">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="0182e-136">Container name.</span></span>

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

### <span data-ttu-id="0182e-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0182e-137">-ParentObject</span></span>
<span data-ttu-id="0182e-138">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0182e-138">Sql Database object.</span></span>

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

### <span data-ttu-id="0182e-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="0182e-139">-PartitionKeyKind</span></span>
<span data-ttu-id="0182e-140">Bölümlemek için kullanılan algoritma türü.</span><span class="sxs-lookup"><span data-stu-id="0182e-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="0182e-141">Olası değerler: ' hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="0182e-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="0182e-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="0182e-142">-PartitionKeyPath</span></span>
<span data-ttu-id="0182e-143">Bölüm anahtarı yolu, örneğin, '/adres/ZipCode '.</span><span class="sxs-lookup"><span data-stu-id="0182e-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="0182e-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="0182e-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="0182e-145">Bölüm anahtarı tanımının sürümü</span><span class="sxs-lookup"><span data-stu-id="0182e-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="0182e-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0182e-146">-ResourceGroupName</span></span>
<span data-ttu-id="0182e-147">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0182e-147">Name of resource group.</span></span>

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

### <span data-ttu-id="0182e-148">-Üretim</span><span class="sxs-lookup"><span data-stu-id="0182e-148">-Throughput</span></span>
<span data-ttu-id="0182e-149">SQL kapsayıcısının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="0182e-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="0182e-150">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="0182e-150">Default value is 400.</span></span>

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

### <span data-ttu-id="0182e-151">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="0182e-151">-TtlInSeconds</span></span>
<span data-ttu-id="0182e-152">Varsayılan TTL (saniye).</span><span class="sxs-lookup"><span data-stu-id="0182e-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="0182e-153">Değer eksik veya-1 olarak ayarlanmışsa, öğelerin süresi dolmasın.</span><span class="sxs-lookup"><span data-stu-id="0182e-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="0182e-154">Değer n olarak ayarlanırsa, son değiştirilme saatinden sonraki öğelerin süresi n saniye dolacak.</span><span class="sxs-lookup"><span data-stu-id="0182e-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="0182e-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0182e-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="0182e-156">Microsoft. Azure. Commands. CosmosDB. PSSqlUniqueKeyPolicy türünde UniqueKeyPolicy nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0182e-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="0182e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0182e-157">-WhatIf</span></span>
<span data-ttu-id="0182e-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0182e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0182e-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0182e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0182e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0182e-160">CommonParameters</span></span>
<span data-ttu-id="0182e-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0182e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0182e-162">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0182e-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0182e-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0182e-163">INPUTS</span></span>

### <span data-ttu-id="0182e-164">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0182e-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="0182e-165">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0182e-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="0182e-166">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0182e-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="0182e-167">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0182e-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="0182e-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0182e-168">OUTPUTS</span></span>

### <span data-ttu-id="0182e-169">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0182e-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="0182e-170">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="0182e-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="0182e-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0182e-171">NOTES</span></span>

## <span data-ttu-id="0182e-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0182e-172">RELATED LINKS</span></span>
