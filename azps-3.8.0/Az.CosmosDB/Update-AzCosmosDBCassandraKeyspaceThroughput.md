---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 0c104573fe0ecfb710f37c9c2fe898a6777f49e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096020"
---
# <span data-ttu-id="d2f4b-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="d2f4b-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="d2f4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f4b-103">CosmosDB Cassandra keyspace 'in üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="d2f4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2f4b-104">SYNTAX</span></span>

### <span data-ttu-id="d2f4b-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2f4b-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f4b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2f4b-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2f4b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2f4b-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2f4b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2f4b-108">EXAMPLES</span></span>

### <span data-ttu-id="d2f4b-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2f4b-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="d2f4b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2f4b-110">PARAMETERS</span></span>

### <span data-ttu-id="d2f4b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2f4b-111">-AccountName</span></span>
<span data-ttu-id="d2f4b-112">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d2f4b-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2f4b-113">-Confirm</span></span>
<span data-ttu-id="d2f4b-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f4b-115">-DefaultProfile</span></span>
<span data-ttu-id="d2f4b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f4b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2f4b-117">-InputObject</span></span>
<span data-ttu-id="d2f4b-118">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="d2f4b-118">CosmosDB Account object</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f4b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2f4b-119">-Name</span></span>
<span data-ttu-id="d2f4b-120">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d2f4b-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d2f4b-121">-ParentObject</span></span>
<span data-ttu-id="d2f4b-122">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="d2f4b-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d2f4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="d2f4b-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-124">Name of resource group.</span></span>

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

### <span data-ttu-id="d2f4b-125">-Üretim</span><span class="sxs-lookup"><span data-stu-id="d2f4b-125">-Throughput</span></span>
<span data-ttu-id="d2f4b-126">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d2f4b-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="d2f4b-127">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-127">Default value is 400.</span></span>

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

### <span data-ttu-id="d2f4b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f4b-128">-WhatIf</span></span>
<span data-ttu-id="d2f4b-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f4b-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f4b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f4b-131">CommonParameters</span></span>
<span data-ttu-id="d2f4b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f4b-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d2f4b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f4b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2f4b-134">INPUTS</span></span>

### <span data-ttu-id="d2f4b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d2f4b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d2f4b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2f4b-136">OUTPUTS</span></span>

### <span data-ttu-id="d2f4b-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d2f4b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d2f4b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2f4b-138">NOTES</span></span>

## <span data-ttu-id="d2f4b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2f4b-139">RELATED LINKS</span></span>