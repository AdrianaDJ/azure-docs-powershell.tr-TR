---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274191"
---
# <span data-ttu-id="08f31-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="08f31-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="08f31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08f31-102">SYNOPSIS</span></span>
<span data-ttu-id="08f31-103">CosmosDB Cassandra tablosunun üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="08f31-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="08f31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08f31-104">SYNTAX</span></span>

### <span data-ttu-id="08f31-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="08f31-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f31-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08f31-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f31-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08f31-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08f31-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="08f31-108">DESCRIPTION</span></span>
<span data-ttu-id="08f31-109">CosmosDB Cassandra tablosunun üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="08f31-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="08f31-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08f31-110">EXAMPLES</span></span>

### <span data-ttu-id="08f31-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="08f31-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="08f31-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08f31-112">PARAMETERS</span></span>

### <span data-ttu-id="08f31-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="08f31-113">-AccountName</span></span>
<span data-ttu-id="08f31-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="08f31-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="08f31-115">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="08f31-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="08f31-116">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="08f31-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="08f31-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="08f31-117">-Confirm</span></span>
<span data-ttu-id="08f31-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08f31-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f31-119">-DefaultProfile</span></span>
<span data-ttu-id="08f31-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08f31-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f31-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08f31-121">-InputObject</span></span>
<span data-ttu-id="08f31-122">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="08f31-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="08f31-123">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="08f31-123">-KeyspaceName</span></span>
<span data-ttu-id="08f31-124">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="08f31-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="08f31-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="08f31-125">-Name</span></span>
<span data-ttu-id="08f31-126">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="08f31-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="08f31-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="08f31-127">-ParentObject</span></span>
<span data-ttu-id="08f31-128">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="08f31-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="08f31-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08f31-129">-ResourceGroupName</span></span>
<span data-ttu-id="08f31-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="08f31-130">Name of resource group.</span></span>

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

### <span data-ttu-id="08f31-131">-Üretim</span><span class="sxs-lookup"><span data-stu-id="08f31-131">-Throughput</span></span>
<span data-ttu-id="08f31-132">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="08f31-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="08f31-133">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="08f31-133">Default value is 400.</span></span>

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

### <span data-ttu-id="08f31-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f31-134">-WhatIf</span></span>
<span data-ttu-id="08f31-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08f31-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f31-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08f31-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f31-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f31-137">CommonParameters</span></span>
<span data-ttu-id="08f31-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08f31-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f31-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="08f31-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f31-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08f31-140">INPUTS</span></span>

### <span data-ttu-id="08f31-141">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="08f31-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="08f31-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08f31-142">OUTPUTS</span></span>

### <span data-ttu-id="08f31-143">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="08f31-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="08f31-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08f31-144">NOTES</span></span>

## <span data-ttu-id="08f31-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08f31-145">RELATED LINKS</span></span>
