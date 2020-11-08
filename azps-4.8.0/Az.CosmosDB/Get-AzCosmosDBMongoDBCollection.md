---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268045"
---
# <span data-ttu-id="bf529-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="bf529-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="bf529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf529-102">SYNOPSIS</span></span>
<span data-ttu-id="bf529-103">CosmosDB MongoDB koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="bf529-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="bf529-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf529-104">SYNTAX</span></span>

### <span data-ttu-id="bf529-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf529-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="bf529-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf529-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf529-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf529-107">DESCRIPTION</span></span>
<span data-ttu-id="bf529-108">**Get-AzCosmosDBMongoDBCollection** cmdlet 'ı Cosmosdb MongoDB koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="bf529-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="bf529-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf529-109">EXAMPLES</span></span>

### <span data-ttu-id="bf529-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bf529-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="bf529-111">Resource nesnesi Mongoındexes, _rid, _ts, _etag özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="bf529-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="bf529-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bf529-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="bf529-113">Bu örnekte, alınan koleksiyonun ShardKey</span><span class="sxs-lookup"><span data-stu-id="bf529-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="bf529-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf529-114">PARAMETERS</span></span>

### <span data-ttu-id="bf529-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf529-115">-AccountName</span></span>
<span data-ttu-id="bf529-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="bf529-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bf529-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf529-117">-DatabaseName</span></span>
<span data-ttu-id="bf529-118">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="bf529-118">Database name.</span></span>

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

### <span data-ttu-id="bf529-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf529-119">-DefaultProfile</span></span>
<span data-ttu-id="bf529-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf529-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf529-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf529-121">-Name</span></span>
<span data-ttu-id="bf529-122">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="bf529-122">Collection name.</span></span>

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

### <span data-ttu-id="bf529-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bf529-123">-ParentObject</span></span>
<span data-ttu-id="bf529-124">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bf529-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="bf529-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf529-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf529-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bf529-126">Name of resource group.</span></span>

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

### <span data-ttu-id="bf529-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf529-127">CommonParameters</span></span>
<span data-ttu-id="bf529-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf529-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf529-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf529-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf529-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf529-130">INPUTS</span></span>

### <span data-ttu-id="bf529-131">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="bf529-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="bf529-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf529-132">OUTPUTS</span></span>

### <span data-ttu-id="bf529-133">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbcollectiongetresults</span><span class="sxs-lookup"><span data-stu-id="bf529-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="bf529-134">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bf529-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bf529-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf529-135">NOTES</span></span>

## <span data-ttu-id="bf529-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf529-136">RELATED LINKS</span></span>
