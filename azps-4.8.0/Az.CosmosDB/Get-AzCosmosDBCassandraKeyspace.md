---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267877"
---
# <span data-ttu-id="17f36-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="17f36-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="17f36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f36-102">SYNOPSIS</span></span>
<span data-ttu-id="17f36-103">CosmosDB Cassandra anahtar uzayını alır.</span><span class="sxs-lookup"><span data-stu-id="17f36-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="17f36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17f36-104">SYNTAX</span></span>

### <span data-ttu-id="17f36-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17f36-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17f36-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17f36-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17f36-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="17f36-107">DESCRIPTION</span></span>
<span data-ttu-id="17f36-108">**Get-AzCosmosDBCassandraKeyspace** cmdlet 'i, yeni bir</span><span class="sxs-lookup"><span data-stu-id="17f36-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="17f36-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17f36-109">EXAMPLES</span></span>

### <span data-ttu-id="17f36-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="17f36-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="17f36-111">Get-AzCosmosDBCassandraKeyspace mevcut CassandraKeyspace 'in özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="17f36-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="17f36-112">_Etag, _ts _rid özelliklerini almak için kaynağı genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17f36-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="17f36-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17f36-113">PARAMETERS</span></span>

### <span data-ttu-id="17f36-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="17f36-114">-AccountName</span></span>
<span data-ttu-id="17f36-115">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="17f36-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="17f36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f36-116">-DefaultProfile</span></span>
<span data-ttu-id="17f36-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17f36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17f36-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="17f36-118">-Name</span></span>
<span data-ttu-id="17f36-119">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="17f36-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="17f36-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="17f36-120">-ParentObject</span></span>
<span data-ttu-id="17f36-121">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="17f36-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17f36-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f36-122">-ResourceGroupName</span></span>
<span data-ttu-id="17f36-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="17f36-123">Name of resource group.</span></span>

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

### <span data-ttu-id="17f36-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f36-124">CommonParameters</span></span>
<span data-ttu-id="17f36-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17f36-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f36-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="17f36-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f36-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17f36-127">INPUTS</span></span>

### <span data-ttu-id="17f36-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="17f36-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="17f36-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17f36-129">OUTPUTS</span></span>

### <span data-ttu-id="17f36-130">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="17f36-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="17f36-131">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="17f36-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="17f36-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17f36-132">NOTES</span></span>

## <span data-ttu-id="17f36-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17f36-133">RELATED LINKS</span></span>
