---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104437"
---
# <span data-ttu-id="ed8c8-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="ed8c8-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="ed8c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8c8-103">CosmosDB MongoDB koleksiyonunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="ed8c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed8c8-104">SYNTAX</span></span>

### <span data-ttu-id="ed8c8-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed8c8-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed8c8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed8c8-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed8c8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed8c8-107">DESCRIPTION</span></span>
<span data-ttu-id="ed8c8-108">**Set-AzCosmosDBMongoDBCollection** cmdlet 'ı Cosmosdb MongoDB koleksiyonunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="ed8c8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed8c8-109">EXAMPLES</span></span>

### <span data-ttu-id="ed8c8-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed8c8-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="ed8c8-111">Resource nesnesi Mongoındexes, _rid, _ts, _etag özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="ed8c8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed8c8-112">PARAMETERS</span></span>

### <span data-ttu-id="ed8c8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed8c8-113">-AccountName</span></span>
<span data-ttu-id="ed8c8-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ed8c8-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed8c8-115">-Confirm</span></span>
<span data-ttu-id="ed8c8-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed8c8-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed8c8-117">-DatabaseName</span></span>
<span data-ttu-id="ed8c8-118">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-118">Database name.</span></span>

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

### <span data-ttu-id="ed8c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8c8-119">-DefaultProfile</span></span>
<span data-ttu-id="ed8c8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed8c8-121">-Index</span><span class="sxs-lookup"><span data-stu-id="ed8c8-121">-Index</span></span>
<span data-ttu-id="ed8c8-122">Psmte Goındex nesneleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-122">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="ed8c8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed8c8-123">-InputObject</span></span>
<span data-ttu-id="ed8c8-124">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="ed8c8-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed8c8-125">-Name</span></span>
<span data-ttu-id="ed8c8-126">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-126">Collection name.</span></span>

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

### <span data-ttu-id="ed8c8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8c8-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed8c8-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-128">Name of resource group.</span></span>

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

### <span data-ttu-id="ed8c8-129">-Shard</span><span class="sxs-lookup"><span data-stu-id="ed8c8-129">-Shard</span></span>
<span data-ttu-id="ed8c8-130">Paylaşım anahtarı yolu.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-130">Sharding key path.</span></span>

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

### <span data-ttu-id="ed8c8-131">-Üretim</span><span class="sxs-lookup"><span data-stu-id="ed8c8-131">-Throughput</span></span>
<span data-ttu-id="ed8c8-132">SQL kapsayıcısının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ed8c8-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="ed8c8-133">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-133">Default value is 400.</span></span>

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

### <span data-ttu-id="ed8c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed8c8-134">-WhatIf</span></span>
<span data-ttu-id="ed8c8-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed8c8-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed8c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8c8-137">CommonParameters</span></span>
<span data-ttu-id="ed8c8-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8c8-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed8c8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8c8-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed8c8-140">INPUTS</span></span>

### <span data-ttu-id="ed8c8-141">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="ed8c8-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="ed8c8-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed8c8-142">OUTPUTS</span></span>

### <span data-ttu-id="ed8c8-143">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbcollectiongetresults</span><span class="sxs-lookup"><span data-stu-id="ed8c8-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="ed8c8-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed8c8-144">NOTES</span></span>

## <span data-ttu-id="ed8c8-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed8c8-145">RELATED LINKS</span></span>
