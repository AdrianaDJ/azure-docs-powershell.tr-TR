---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274629"
---
# <span data-ttu-id="6d2de-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="6d2de-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="6d2de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d2de-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2de-103">Yeni bir CosmosDB MongoDB koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d2de-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="6d2de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d2de-104">SYNTAX</span></span>

### <span data-ttu-id="6d2de-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6d2de-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d2de-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d2de-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d2de-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d2de-107">DESCRIPTION</span></span>
<span data-ttu-id="6d2de-108">Yeni bir CosmosDB MongoDB koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d2de-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="6d2de-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d2de-109">EXAMPLES</span></span>

### <span data-ttu-id="6d2de-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6d2de-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="6d2de-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d2de-111">PARAMETERS</span></span>

### <span data-ttu-id="6d2de-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d2de-112">-AccountName</span></span>
<span data-ttu-id="6d2de-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="6d2de-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6d2de-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="6d2de-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="6d2de-115">Analitik depolama için TTL.</span><span class="sxs-lookup"><span data-stu-id="6d2de-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="6d2de-116">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="6d2de-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6d2de-117">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="6d2de-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="6d2de-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d2de-118">-Confirm</span></span>
<span data-ttu-id="6d2de-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d2de-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d2de-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6d2de-120">-DatabaseName</span></span>
<span data-ttu-id="6d2de-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="6d2de-121">Database name.</span></span>

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

### <span data-ttu-id="6d2de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2de-122">-DefaultProfile</span></span>
<span data-ttu-id="6d2de-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d2de-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d2de-124">-Index</span><span class="sxs-lookup"><span data-stu-id="6d2de-124">-Index</span></span>
<span data-ttu-id="6d2de-125">Psmte Goındex nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="6d2de-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="6d2de-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d2de-126">-Name</span></span>
<span data-ttu-id="6d2de-127">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="6d2de-127">Collection name.</span></span>

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

### <span data-ttu-id="6d2de-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6d2de-128">-ParentObject</span></span>
<span data-ttu-id="6d2de-129">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6d2de-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="6d2de-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d2de-130">-ResourceGroupName</span></span>
<span data-ttu-id="6d2de-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6d2de-131">Name of resource group.</span></span>

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

### <span data-ttu-id="6d2de-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="6d2de-132">-Shard</span></span>
<span data-ttu-id="6d2de-133">Paylaşım anahtarı yolu.</span><span class="sxs-lookup"><span data-stu-id="6d2de-133">Sharding key path.</span></span>

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

### <span data-ttu-id="6d2de-134">-Üretim</span><span class="sxs-lookup"><span data-stu-id="6d2de-134">-Throughput</span></span>
<span data-ttu-id="6d2de-135">SQL kapsayıcısının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="6d2de-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="6d2de-136">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="6d2de-136">Default value is 400.</span></span>

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

### <span data-ttu-id="6d2de-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d2de-137">-WhatIf</span></span>
<span data-ttu-id="6d2de-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d2de-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d2de-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d2de-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d2de-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2de-140">CommonParameters</span></span>
<span data-ttu-id="6d2de-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d2de-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2de-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6d2de-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2de-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d2de-143">INPUTS</span></span>

### <span data-ttu-id="6d2de-144">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="6d2de-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="6d2de-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d2de-145">OUTPUTS</span></span>

### <span data-ttu-id="6d2de-146">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbcollectiongetresults</span><span class="sxs-lookup"><span data-stu-id="6d2de-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="6d2de-147">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="6d2de-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="6d2de-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d2de-148">NOTES</span></span>

## <span data-ttu-id="6d2de-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d2de-149">RELATED LINKS</span></span>
