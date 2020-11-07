---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937543"
---
# <span data-ttu-id="1e6a9-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="1e6a9-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="1e6a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6a9-103">CosmosDB Cassandra anahtar uzayını alır.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1e6a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e6a9-104">SYNTAX</span></span>

### <span data-ttu-id="1e6a9-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e6a9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6a9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e6a9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e6a9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e6a9-107">DESCRIPTION</span></span>
<span data-ttu-id="1e6a9-108">**Get-AzCosmosDBCassandraKeyspace** cmdlet 'i, yeni bir</span><span class="sxs-lookup"><span data-stu-id="1e6a9-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1e6a9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e6a9-109">EXAMPLES</span></span>

### <span data-ttu-id="1e6a9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e6a9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="1e6a9-111">Get-AzCosmosDBCassandraKeyspace mevcut CassandraKeyspace 'in özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="1e6a9-112">_Etag, _ts _rid özelliklerini almak için kaynağı genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="1e6a9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e6a9-113">PARAMETERS</span></span>

### <span data-ttu-id="1e6a9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1e6a9-114">-AccountName</span></span>
<span data-ttu-id="1e6a9-115">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1e6a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6a9-116">-DefaultProfile</span></span>
<span data-ttu-id="1e6a9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e6a9-118">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="1e6a9-118">-Detailed</span></span>
<span data-ttu-id="1e6a9-119">Sağlanmışsa, cmdlet, karşılık gelen üretilen iş değeri ile birlikte tuş uzayını döndürür.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="1e6a9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e6a9-120">-InputObject</span></span>
<span data-ttu-id="1e6a9-121">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="1e6a9-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6a9-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e6a9-122">-Name</span></span>
<span data-ttu-id="1e6a9-123">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1e6a9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6a9-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e6a9-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-125">Name of resource group.</span></span>

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

### <span data-ttu-id="1e6a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6a9-126">CommonParameters</span></span>
<span data-ttu-id="1e6a9-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6a9-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1e6a9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6a9-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e6a9-129">INPUTS</span></span>

### <span data-ttu-id="1e6a9-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1e6a9-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1e6a9-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e6a9-131">OUTPUTS</span></span>

### <span data-ttu-id="1e6a9-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="1e6a9-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="1e6a9-133">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1e6a9-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1e6a9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e6a9-134">NOTES</span></span>

## <span data-ttu-id="1e6a9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e6a9-135">RELATED LINKS</span></span>
