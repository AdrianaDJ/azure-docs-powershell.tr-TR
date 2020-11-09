---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 42ec4db0f9c0967e375cc30a582c35aaca65840f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321581"
---
# <span data-ttu-id="5f912-101">New-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="5f912-101">New-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="5f912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f912-102">SYNOPSIS</span></span>
<span data-ttu-id="5f912-103">Yeni bir CosmosDB Cassandra tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5f912-103">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="5f912-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f912-104">SYNTAX</span></span>

### <span data-ttu-id="5f912-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f912-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f912-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f912-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] -Schema <PSCassandraSchema>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f912-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f912-107">DESCRIPTION</span></span>
<span data-ttu-id="5f912-108">Yeni bir CosmosDB Cassandra tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5f912-108">Creates a new CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="5f912-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f912-109">EXAMPLES</span></span>

### <span data-ttu-id="5f912-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5f912-110">Example 1</span></span>
```powershell
PS C:\>       
      $Column1 = New-AzCosmosDBCassandraColumn -Name "ColumnA" -Type "int"
      $Column2 = New-AzCosmosDBCassandraColumn -Name "ColumnB" -Type "ascii"
      $Column3 = New-AzCosmosDBCassandraColumn -Name "ColumnC" -Type "int"
      $Column4 = New-AzCosmosDBCassandraColumn -Name "ColumnD" -Type "ascii"

      $clusterkey1 = New-AzCosmosDBCassandraClusterKey -Name "ColumnB" -OrderBy "Asc"
      $clusterkey2 = New-AzCosmosDBCassandraClusterKey -Name "ColumnA" -OrderBy "Asc"

      $schema = New-AzCosmosDBCassandraSchema -Column $Column1,$Column2 -ClusterKey $clusterkey1 -PartitionKey "ColumnA"

      New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema $schema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

## <span data-ttu-id="5f912-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f912-111">PARAMETERS</span></span>

### <span data-ttu-id="5f912-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5f912-112">-AccountName</span></span>
<span data-ttu-id="5f912-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="5f912-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5f912-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="5f912-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="5f912-115">Analitik depolama TTL.</span><span class="sxs-lookup"><span data-stu-id="5f912-115">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="5f912-116">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="5f912-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5f912-117">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="5f912-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5f912-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f912-118">-Confirm</span></span>
<span data-ttu-id="5f912-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f912-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f912-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f912-120">-DefaultProfile</span></span>
<span data-ttu-id="5f912-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f912-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f912-122">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="5f912-122">-KeyspaceName</span></span>
<span data-ttu-id="5f912-123">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="5f912-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5f912-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f912-124">-Name</span></span>
<span data-ttu-id="5f912-125">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="5f912-125">Cassandra Table Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f912-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5f912-126">-ParentObject</span></span>
<span data-ttu-id="5f912-127">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5f912-127">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="5f912-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f912-128">-ResourceGroupName</span></span>
<span data-ttu-id="5f912-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5f912-129">Name of resource group.</span></span>

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

### <span data-ttu-id="5f912-130">-Şema</span><span class="sxs-lookup"><span data-stu-id="5f912-130">-Schema</span></span>
<span data-ttu-id="5f912-131">PSCassandraSchema nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5f912-131">PSCassandraSchema object.</span></span>
<span data-ttu-id="5f912-132">Bu nesneyi oluşturmak için New-AzCosmosDBCassandraSchema kullanın.</span><span class="sxs-lookup"><span data-stu-id="5f912-132">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f912-133">-Üretim</span><span class="sxs-lookup"><span data-stu-id="5f912-133">-Throughput</span></span>
<span data-ttu-id="5f912-134">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="5f912-134">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="5f912-135">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5f912-135">Default value is 400.</span></span>

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

### <span data-ttu-id="5f912-136">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="5f912-136">-TtlInSeconds</span></span>
<span data-ttu-id="5f912-137">Varsayılan TTL (saniye).</span><span class="sxs-lookup"><span data-stu-id="5f912-137">Default Ttl in seconds.</span></span>
<span data-ttu-id="5f912-138">Değer eksik veya-1 olarak ayarlanmışsa, öğelerin süresi dolmasın.</span><span class="sxs-lookup"><span data-stu-id="5f912-138">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="5f912-139">Değer n olarak ayarlanırsa, son değiştirilme saatinden sonraki öğelerin süresi n saniye dolacak.</span><span class="sxs-lookup"><span data-stu-id="5f912-139">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="5f912-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f912-140">-WhatIf</span></span>
<span data-ttu-id="5f912-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f912-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f912-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f912-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f912-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f912-143">CommonParameters</span></span>
<span data-ttu-id="5f912-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f912-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f912-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f912-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f912-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f912-146">INPUTS</span></span>

### <span data-ttu-id="5f912-147">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="5f912-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="5f912-148">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5f912-148">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="5f912-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f912-149">OUTPUTS</span></span>

### <span data-ttu-id="5f912-150">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="5f912-150">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="5f912-151">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="5f912-151">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5f912-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f912-152">NOTES</span></span>

## <span data-ttu-id="5f912-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f912-153">RELATED LINKS</span></span>
