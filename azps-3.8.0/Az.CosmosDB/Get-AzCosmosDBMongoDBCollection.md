---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 623ed0391ba36722cce26a42f1dd3d820cbd49f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104120"
---
# <span data-ttu-id="b3147-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="b3147-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="b3147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3147-102">SYNOPSIS</span></span>
<span data-ttu-id="b3147-103">CosmosDB MongoDB koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="b3147-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="b3147-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3147-104">SYNTAX</span></span>

### <span data-ttu-id="b3147-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3147-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="b3147-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3147-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3147-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3147-107">DESCRIPTION</span></span>
<span data-ttu-id="b3147-108">**Get-AzCosmosDBMongoDBCollection** cmdlet 'ı Cosmosdb MongoDB koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="b3147-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="b3147-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3147-109">EXAMPLES</span></span>

### <span data-ttu-id="b3147-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b3147-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="b3147-111">Resource nesnesi Mongoındexes, _rid, _ts, _etag özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="b3147-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="b3147-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3147-112">PARAMETERS</span></span>

### <span data-ttu-id="b3147-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3147-113">-AccountName</span></span>
<span data-ttu-id="b3147-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="b3147-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b3147-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b3147-115">-DatabaseName</span></span>
<span data-ttu-id="b3147-116">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="b3147-116">Database name.</span></span>

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

### <span data-ttu-id="b3147-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3147-117">-DefaultProfile</span></span>
<span data-ttu-id="b3147-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3147-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3147-119">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="b3147-119">-Detailed</span></span>
<span data-ttu-id="b3147-120">Sağlanmışsa, cmdlet, ilgili üretilen iş değerini içeren koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3147-120">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="b3147-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3147-121">-InputObject</span></span>
<span data-ttu-id="b3147-122">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b3147-122">Mongo Database object.</span></span>

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

### <span data-ttu-id="b3147-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3147-123">-Name</span></span>
<span data-ttu-id="b3147-124">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="b3147-124">Collection name.</span></span>

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

### <span data-ttu-id="b3147-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3147-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3147-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b3147-126">Name of resource group.</span></span>

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

### <span data-ttu-id="b3147-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3147-127">CommonParameters</span></span>
<span data-ttu-id="b3147-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3147-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3147-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b3147-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3147-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3147-130">INPUTS</span></span>

### <span data-ttu-id="b3147-131">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="b3147-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="b3147-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3147-132">OUTPUTS</span></span>

### <span data-ttu-id="b3147-133">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbcollectiongetresults</span><span class="sxs-lookup"><span data-stu-id="b3147-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="b3147-134">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b3147-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b3147-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3147-135">NOTES</span></span>

## <span data-ttu-id="b3147-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3147-136">RELATED LINKS</span></span>
