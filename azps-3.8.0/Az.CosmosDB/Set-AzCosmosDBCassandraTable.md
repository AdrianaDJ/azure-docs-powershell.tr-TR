---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104439"
---
# <span data-ttu-id="9ab13-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="9ab13-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="9ab13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ab13-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab13-103">CosmosDB Cassandra tablosunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9ab13-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="9ab13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ab13-104">SYNTAX</span></span>

### <span data-ttu-id="9ab13-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9ab13-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab13-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ab13-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ab13-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ab13-107">DESCRIPTION</span></span>
<span data-ttu-id="9ab13-108">**Set-AzCosmosDBCassandraTable** cmdlet 'ı Cosmosdb Cassandra tuş uzayını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9ab13-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9ab13-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ab13-109">EXAMPLES</span></span>

### <span data-ttu-id="9ab13-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9ab13-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="9ab13-111">Kaynak nesnesi _rid, _ts, _etag, DefaultTtl ve şema özelliklerinin değerlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="9ab13-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="9ab13-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ab13-112">PARAMETERS</span></span>

### <span data-ttu-id="9ab13-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ab13-113">-AccountName</span></span>
<span data-ttu-id="9ab13-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="9ab13-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9ab13-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ab13-115">-Confirm</span></span>
<span data-ttu-id="9ab13-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ab13-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ab13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab13-117">-DefaultProfile</span></span>
<span data-ttu-id="9ab13-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ab13-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ab13-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ab13-119">-InputObject</span></span>
<span data-ttu-id="9ab13-120">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9ab13-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="9ab13-121">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="9ab13-121">-KeyspaceName</span></span>
<span data-ttu-id="9ab13-122">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="9ab13-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9ab13-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ab13-123">-Name</span></span>
<span data-ttu-id="9ab13-124">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="9ab13-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="9ab13-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab13-125">-ResourceGroupName</span></span>
<span data-ttu-id="9ab13-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9ab13-126">Name of resource group.</span></span>

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

### <span data-ttu-id="9ab13-127">-Şema</span><span class="sxs-lookup"><span data-stu-id="9ab13-127">-Schema</span></span>
<span data-ttu-id="9ab13-128">PSCassandraSchema nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9ab13-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="9ab13-129">Bu nesneyi oluşturmak için New-AzCosmosDBCassandraSchema kullanın.</span><span class="sxs-lookup"><span data-stu-id="9ab13-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

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

### <span data-ttu-id="9ab13-130">-Üretim</span><span class="sxs-lookup"><span data-stu-id="9ab13-130">-Throughput</span></span>
<span data-ttu-id="9ab13-131">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="9ab13-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="9ab13-132">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="9ab13-132">Default value is 400.</span></span>

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

### <span data-ttu-id="9ab13-133">-Ttlinsaniye</span><span class="sxs-lookup"><span data-stu-id="9ab13-133">-TtlInSeconds</span></span>
<span data-ttu-id="9ab13-134">Varsayılan TTL (saniye).</span><span class="sxs-lookup"><span data-stu-id="9ab13-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="9ab13-135">Değer eksik veya-1 olarak ayarlanmışsa, öğelerin süresi dolmasın.</span><span class="sxs-lookup"><span data-stu-id="9ab13-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="9ab13-136">Değer n olarak ayarlanırsa, son değiştirilme saatinden sonraki öğelerin süresi n saniye dolacak.</span><span class="sxs-lookup"><span data-stu-id="9ab13-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="9ab13-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ab13-137">-WhatIf</span></span>
<span data-ttu-id="9ab13-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ab13-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ab13-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ab13-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ab13-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab13-140">CommonParameters</span></span>
<span data-ttu-id="9ab13-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ab13-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab13-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9ab13-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab13-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ab13-143">INPUTS</span></span>

### <span data-ttu-id="9ab13-144">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="9ab13-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="9ab13-145">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9ab13-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="9ab13-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ab13-146">OUTPUTS</span></span>

### <span data-ttu-id="9ab13-147">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="9ab13-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="9ab13-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ab13-148">NOTES</span></span>

## <span data-ttu-id="9ab13-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ab13-149">RELATED LINKS</span></span>
