---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321390"
---
# <span data-ttu-id="1d77c-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="1d77c-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="1d77c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d77c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d77c-103">CosmosDB Cassandra keyspace 'in üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1d77c-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1d77c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d77c-104">SYNTAX</span></span>

### <span data-ttu-id="1d77c-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1d77c-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d77c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d77c-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d77c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d77c-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d77c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d77c-108">DESCRIPTION</span></span>
<span data-ttu-id="1d77c-109">CosmosDB Cassandra keyspace 'in üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1d77c-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="1d77c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d77c-110">EXAMPLES</span></span>

### <span data-ttu-id="1d77c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1d77c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="1d77c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d77c-112">PARAMETERS</span></span>

### <span data-ttu-id="1d77c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1d77c-113">-AccountName</span></span>
<span data-ttu-id="1d77c-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="1d77c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d77c-115">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="1d77c-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1d77c-116">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="1d77c-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="1d77c-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d77c-117">-Confirm</span></span>
<span data-ttu-id="1d77c-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d77c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d77c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d77c-119">-DefaultProfile</span></span>
<span data-ttu-id="1d77c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d77c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d77c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d77c-121">-InputObject</span></span>
<span data-ttu-id="1d77c-122">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="1d77c-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1d77c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d77c-123">-Name</span></span>
<span data-ttu-id="1d77c-124">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="1d77c-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="1d77c-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1d77c-125">-ParentObject</span></span>
<span data-ttu-id="1d77c-126">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="1d77c-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1d77c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d77c-127">-ResourceGroupName</span></span>
<span data-ttu-id="1d77c-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1d77c-128">Name of resource group.</span></span>

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

### <span data-ttu-id="1d77c-129">-Üretim</span><span class="sxs-lookup"><span data-stu-id="1d77c-129">-Throughput</span></span>
<span data-ttu-id="1d77c-130">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="1d77c-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="1d77c-131">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="1d77c-131">Default value is 400.</span></span>

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

### <span data-ttu-id="1d77c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d77c-132">-WhatIf</span></span>
<span data-ttu-id="1d77c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d77c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d77c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d77c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d77c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d77c-135">CommonParameters</span></span>
<span data-ttu-id="1d77c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d77c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d77c-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1d77c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d77c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d77c-138">INPUTS</span></span>

### <span data-ttu-id="1d77c-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1d77c-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1d77c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d77c-140">OUTPUTS</span></span>

### <span data-ttu-id="1d77c-141">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1d77c-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1d77c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d77c-142">NOTES</span></span>

## <span data-ttu-id="1d77c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d77c-143">RELATED LINKS</span></span>
