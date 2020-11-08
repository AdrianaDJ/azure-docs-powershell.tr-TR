---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268340"
---
# <span data-ttu-id="398ff-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="398ff-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="398ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="398ff-102">SYNOPSIS</span></span>
<span data-ttu-id="398ff-103">CosmosDB MongoDB koleksiyonunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="398ff-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="398ff-104">Var olan koleksiyonu okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="398ff-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="398ff-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="398ff-105">SYNTAX</span></span>

### <span data-ttu-id="398ff-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="398ff-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="398ff-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="398ff-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="398ff-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="398ff-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="398ff-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="398ff-109">DESCRIPTION</span></span>
<span data-ttu-id="398ff-110">CosmosDB MongoDB koleksiyonunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="398ff-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="398ff-111">Var olan koleksiyonu okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="398ff-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="398ff-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="398ff-112">EXAMPLES</span></span>

### <span data-ttu-id="398ff-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="398ff-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="398ff-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="398ff-114">PARAMETERS</span></span>

### <span data-ttu-id="398ff-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="398ff-115">-AccountName</span></span>
<span data-ttu-id="398ff-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="398ff-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="398ff-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="398ff-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="398ff-118">Analitik depolama için TTL.</span><span class="sxs-lookup"><span data-stu-id="398ff-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="398ff-119">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="398ff-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="398ff-120">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="398ff-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="398ff-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="398ff-121">-Confirm</span></span>
<span data-ttu-id="398ff-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="398ff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="398ff-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="398ff-123">-DatabaseName</span></span>
<span data-ttu-id="398ff-124">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="398ff-124">Database name.</span></span>

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

### <span data-ttu-id="398ff-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="398ff-125">-DefaultProfile</span></span>
<span data-ttu-id="398ff-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="398ff-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="398ff-127">-Index</span><span class="sxs-lookup"><span data-stu-id="398ff-127">-Index</span></span>
<span data-ttu-id="398ff-128">Psmte Goındex nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="398ff-128">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="398ff-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="398ff-129">-InputObject</span></span>
<span data-ttu-id="398ff-130">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="398ff-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="398ff-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="398ff-131">-Name</span></span>
<span data-ttu-id="398ff-132">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="398ff-132">Collection name.</span></span>

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

### <span data-ttu-id="398ff-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="398ff-133">-ParentObject</span></span>
<span data-ttu-id="398ff-134">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="398ff-134">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="398ff-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="398ff-135">-ResourceGroupName</span></span>
<span data-ttu-id="398ff-136">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="398ff-136">Name of resource group.</span></span>

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

### <span data-ttu-id="398ff-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="398ff-137">-Shard</span></span>
<span data-ttu-id="398ff-138">Paylaşım anahtarı yolu.</span><span class="sxs-lookup"><span data-stu-id="398ff-138">Sharding key path.</span></span>

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

### <span data-ttu-id="398ff-139">-Üretim</span><span class="sxs-lookup"><span data-stu-id="398ff-139">-Throughput</span></span>
<span data-ttu-id="398ff-140">SQL kapsayıcısının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="398ff-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="398ff-141">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="398ff-141">Default value is 400.</span></span>

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

### <span data-ttu-id="398ff-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="398ff-142">-WhatIf</span></span>
<span data-ttu-id="398ff-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="398ff-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="398ff-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="398ff-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="398ff-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398ff-145">CommonParameters</span></span>
<span data-ttu-id="398ff-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="398ff-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398ff-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="398ff-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398ff-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="398ff-148">INPUTS</span></span>

### <span data-ttu-id="398ff-149">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="398ff-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="398ff-150">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbcollectiongetresults</span><span class="sxs-lookup"><span data-stu-id="398ff-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="398ff-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="398ff-151">OUTPUTS</span></span>

### <span data-ttu-id="398ff-152">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbcollectiongetresults</span><span class="sxs-lookup"><span data-stu-id="398ff-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="398ff-153">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="398ff-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="398ff-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="398ff-154">NOTES</span></span>

## <span data-ttu-id="398ff-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="398ff-155">RELATED LINKS</span></span>
