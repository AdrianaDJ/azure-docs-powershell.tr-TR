---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274608"
---
# <span data-ttu-id="42d30-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="42d30-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="42d30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d30-102">SYNOPSIS</span></span>
<span data-ttu-id="42d30-103">CosmosDB Cassandra tablosunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="42d30-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="42d30-104">Var olan tabloyu okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="42d30-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="42d30-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42d30-105">SYNTAX</span></span>

### <span data-ttu-id="42d30-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42d30-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d30-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42d30-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42d30-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42d30-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42d30-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="42d30-109">DESCRIPTION</span></span>
<span data-ttu-id="42d30-110">CosmosDB Cassandra tablosunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="42d30-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="42d30-111">Var olan tabloyu okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="42d30-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="42d30-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42d30-112">EXAMPLES</span></span>

### <span data-ttu-id="42d30-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="42d30-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="42d30-114">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="42d30-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="42d30-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42d30-115">PARAMETERS</span></span>

### <span data-ttu-id="42d30-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42d30-116">-AccountName</span></span>
<span data-ttu-id="42d30-117">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="42d30-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="42d30-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="42d30-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="42d30-119">Analitik depolama TTL.</span><span class="sxs-lookup"><span data-stu-id="42d30-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="42d30-120">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="42d30-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="42d30-121">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="42d30-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="42d30-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="42d30-122">-Confirm</span></span>
<span data-ttu-id="42d30-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42d30-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d30-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d30-124">-DefaultProfile</span></span>
<span data-ttu-id="42d30-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42d30-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42d30-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42d30-126">-InputObject</span></span>
<span data-ttu-id="42d30-127">Cassandra tablo nesnesi.</span><span class="sxs-lookup"><span data-stu-id="42d30-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="42d30-128">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="42d30-128">-KeyspaceName</span></span>
<span data-ttu-id="42d30-129">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="42d30-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="42d30-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="42d30-130">-Name</span></span>
<span data-ttu-id="42d30-131">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="42d30-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="42d30-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="42d30-132">-ParentObject</span></span>
<span data-ttu-id="42d30-133">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="42d30-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="42d30-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d30-134">-ResourceGroupName</span></span>
<span data-ttu-id="42d30-135">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="42d30-135">Name of resource group.</span></span>

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

### <span data-ttu-id="42d30-136">-Şema</span><span class="sxs-lookup"><span data-stu-id="42d30-136">-Schema</span></span>
<span data-ttu-id="42d30-137">PSCassandraSchema nesnesi.</span><span class="sxs-lookup"><span data-stu-id="42d30-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="42d30-138">Bu nesneyi oluşturmak için New-AzCosmosDBCassandraSchema kullanın.</span><span class="sxs-lookup"><span data-stu-id="42d30-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42d30-139">-Üretim</span><span class="sxs-lookup"><span data-stu-id="42d30-139">-Throughput</span></span>
<span data-ttu-id="42d30-140">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="42d30-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="42d30-141">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="42d30-141">Default value is 400.</span></span>

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

### <span data-ttu-id="42d30-142">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="42d30-142">-TtlInSeconds</span></span>
<span data-ttu-id="42d30-143">Varsayılan TTL (saniye).</span><span class="sxs-lookup"><span data-stu-id="42d30-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="42d30-144">Değer eksik veya-1 olarak ayarlanmışsa, öğelerin süresi dolmasın.</span><span class="sxs-lookup"><span data-stu-id="42d30-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="42d30-145">Değer n olarak ayarlanırsa, son değiştirilme saatinden sonraki öğelerin süresi n saniye dolacak.</span><span class="sxs-lookup"><span data-stu-id="42d30-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="42d30-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d30-146">-WhatIf</span></span>
<span data-ttu-id="42d30-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42d30-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d30-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42d30-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d30-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d30-149">CommonParameters</span></span>
<span data-ttu-id="42d30-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42d30-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d30-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42d30-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d30-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42d30-152">INPUTS</span></span>

### <span data-ttu-id="42d30-153">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="42d30-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="42d30-154">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="42d30-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="42d30-155">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="42d30-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="42d30-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42d30-156">OUTPUTS</span></span>

### <span data-ttu-id="42d30-157">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="42d30-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="42d30-158">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="42d30-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="42d30-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42d30-159">NOTES</span></span>

## <span data-ttu-id="42d30-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42d30-160">RELATED LINKS</span></span>
