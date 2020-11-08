---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: ca78194e0e47b07d2d0d061829bf4db38d85632a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104127"
---
# <span data-ttu-id="4bbc1-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="4bbc1-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="4bbc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bbc1-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbc1-103">CosmosDB Cassandra tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="4bbc1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bbc1-104">SYNTAX</span></span>

### <span data-ttu-id="4bbc1-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bbc1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bbc1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bbc1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bbc1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bbc1-107">DESCRIPTION</span></span>
<span data-ttu-id="4bbc1-108">**Get-AzCosmosDBCassandraTable** cmdlet 'i, yeni bir</span><span class="sxs-lookup"><span data-stu-id="4bbc1-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4bbc1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bbc1-109">EXAMPLES</span></span>

### <span data-ttu-id="4bbc1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4bbc1-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="4bbc1-111">{{Get-AzCosmosDBCassandraTable var olan CassandraKeyspace 'in özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="4bbc1-112">@ Tttl, şema, _etag, _ts, _rid özelliklerini almak için kaynağı genişletebilirsiniz.}}</span><span class="sxs-lookup"><span data-stu-id="4bbc1-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="4bbc1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bbc1-113">PARAMETERS</span></span>

### <span data-ttu-id="4bbc1-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4bbc1-114">-AccountName</span></span>
<span data-ttu-id="4bbc1-115">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4bbc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbc1-116">-DefaultProfile</span></span>
<span data-ttu-id="4bbc1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bbc1-118">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="4bbc1-118">-Detailed</span></span>
<span data-ttu-id="4bbc1-119">Sağlanmışsa, cmdlet, Cassandra tablosunu, karşılık gelen üretilen iş değeri ile döndürür.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-119">If provided then, the cmdlet returns the Cassandra Table with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="4bbc1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bbc1-120">-InputObject</span></span>
<span data-ttu-id="4bbc1-121">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-121">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bbc1-122">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="4bbc1-122">-KeyspaceName</span></span>
<span data-ttu-id="4bbc1-123">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4bbc1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bbc1-124">-Name</span></span>
<span data-ttu-id="4bbc1-125">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="4bbc1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbc1-126">-ResourceGroupName</span></span>
<span data-ttu-id="4bbc1-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-127">Name of resource group.</span></span>

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

### <span data-ttu-id="4bbc1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbc1-128">CommonParameters</span></span>
<span data-ttu-id="4bbc1-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbc1-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4bbc1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbc1-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bbc1-131">INPUTS</span></span>

### <span data-ttu-id="4bbc1-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4bbc1-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="4bbc1-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bbc1-133">OUTPUTS</span></span>

### <span data-ttu-id="4bbc1-134">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="4bbc1-134">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="4bbc1-135">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4bbc1-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4bbc1-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bbc1-136">NOTES</span></span>

## <span data-ttu-id="4bbc1-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bbc1-137">RELATED LINKS</span></span>
