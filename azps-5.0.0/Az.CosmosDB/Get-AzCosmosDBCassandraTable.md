---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321713"
---
# <span data-ttu-id="452ec-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="452ec-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="452ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="452ec-102">SYNOPSIS</span></span>
<span data-ttu-id="452ec-103">CosmosDB Cassandra tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="452ec-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="452ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="452ec-104">SYNTAX</span></span>

### <span data-ttu-id="452ec-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="452ec-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="452ec-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="452ec-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="452ec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="452ec-107">DESCRIPTION</span></span>
<span data-ttu-id="452ec-108">**Get-AzCosmosDBCassandraTable** cmdlet 'i, yeni bir</span><span class="sxs-lookup"><span data-stu-id="452ec-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="452ec-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="452ec-109">EXAMPLES</span></span>

### <span data-ttu-id="452ec-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="452ec-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="452ec-111">{{Get-AzCosmosDBCassandraTable var olan CassandraKeyspace 'in özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="452ec-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="452ec-112">@ Tttl, şema, _etag, _ts, _rid özelliklerini almak için kaynağı genişletebilirsiniz.}}</span><span class="sxs-lookup"><span data-stu-id="452ec-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="452ec-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="452ec-113">PARAMETERS</span></span>

### <span data-ttu-id="452ec-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="452ec-114">-AccountName</span></span>
<span data-ttu-id="452ec-115">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="452ec-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="452ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="452ec-116">-DefaultProfile</span></span>
<span data-ttu-id="452ec-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="452ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="452ec-118">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="452ec-118">-KeyspaceName</span></span>
<span data-ttu-id="452ec-119">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="452ec-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="452ec-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="452ec-120">-Name</span></span>
<span data-ttu-id="452ec-121">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="452ec-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="452ec-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="452ec-122">-ParentObject</span></span>
<span data-ttu-id="452ec-123">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="452ec-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="452ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="452ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="452ec-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="452ec-125">Name of resource group.</span></span>

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

### <span data-ttu-id="452ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452ec-126">CommonParameters</span></span>
<span data-ttu-id="452ec-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="452ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452ec-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="452ec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452ec-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="452ec-129">INPUTS</span></span>

### <span data-ttu-id="452ec-130">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="452ec-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="452ec-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="452ec-131">OUTPUTS</span></span>

### <span data-ttu-id="452ec-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="452ec-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="452ec-133">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="452ec-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="452ec-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="452ec-134">NOTES</span></span>

## <span data-ttu-id="452ec-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="452ec-135">RELATED LINKS</span></span>
