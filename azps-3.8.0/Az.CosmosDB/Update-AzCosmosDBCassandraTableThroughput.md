---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104423"
---
# <span data-ttu-id="379fc-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="379fc-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="379fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="379fc-102">SYNOPSIS</span></span>
<span data-ttu-id="379fc-103">CosmosDB Cassandra tablosunun üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="379fc-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="379fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="379fc-104">SYNTAX</span></span>

### <span data-ttu-id="379fc-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="379fc-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="379fc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="379fc-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="379fc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="379fc-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="379fc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="379fc-108">EXAMPLES</span></span>

### <span data-ttu-id="379fc-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="379fc-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="379fc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="379fc-110">PARAMETERS</span></span>

### <span data-ttu-id="379fc-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="379fc-111">-AccountName</span></span>
<span data-ttu-id="379fc-112">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="379fc-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="379fc-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="379fc-113">-Confirm</span></span>
<span data-ttu-id="379fc-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="379fc-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="379fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379fc-115">-DefaultProfile</span></span>
<span data-ttu-id="379fc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="379fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="379fc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="379fc-117">-InputObject</span></span>
<span data-ttu-id="379fc-118">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="379fc-118">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="379fc-119">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="379fc-119">-KeyspaceName</span></span>
<span data-ttu-id="379fc-120">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="379fc-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="379fc-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="379fc-121">-Name</span></span>
<span data-ttu-id="379fc-122">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="379fc-122">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="379fc-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="379fc-123">-ParentObject</span></span>
<span data-ttu-id="379fc-124">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="379fc-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="379fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="379fc-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="379fc-126">Name of resource group.</span></span>

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

### <span data-ttu-id="379fc-127">-Üretim</span><span class="sxs-lookup"><span data-stu-id="379fc-127">-Throughput</span></span>
<span data-ttu-id="379fc-128">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="379fc-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="379fc-129">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="379fc-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379fc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="379fc-130">-WhatIf</span></span>
<span data-ttu-id="379fc-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="379fc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="379fc-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="379fc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="379fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379fc-133">CommonParameters</span></span>
<span data-ttu-id="379fc-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="379fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379fc-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="379fc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379fc-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="379fc-136">INPUTS</span></span>

### <span data-ttu-id="379fc-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="379fc-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="379fc-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="379fc-138">OUTPUTS</span></span>

### <span data-ttu-id="379fc-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="379fc-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="379fc-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="379fc-140">NOTES</span></span>

## <span data-ttu-id="379fc-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="379fc-141">RELATED LINKS</span></span>
