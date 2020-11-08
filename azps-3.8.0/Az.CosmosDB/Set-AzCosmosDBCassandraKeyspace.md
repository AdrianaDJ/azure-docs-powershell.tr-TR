---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: d1b0dcee6c4337a572f98a51cb03c3fcdcd6c84e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104440"
---
# <span data-ttu-id="01eed-101">Set-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="01eed-101">Set-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="01eed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01eed-102">SYNOPSIS</span></span>
<span data-ttu-id="01eed-103">CosmosDB Cassandra tuş uzayını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="01eed-103">Sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="01eed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01eed-104">SYNTAX</span></span>

### <span data-ttu-id="01eed-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="01eed-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01eed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01eed-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01eed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="01eed-107">DESCRIPTION</span></span>
<span data-ttu-id="01eed-108">**Set-AzCosmosDBCassandraKeyspace** cmdlet 'ı Cosmosdb Cassandra anahtar uzayını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="01eed-108">The **Set-AzCosmosDBCassandraKeyspace** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="01eed-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01eed-109">EXAMPLES</span></span>

### <span data-ttu-id="01eed-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="01eed-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraKeyspace -ResourceGroupName {rgName} -AccountName {accountName} -Name {keyspaceName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

<span data-ttu-id="01eed-111">Resource nesnesi _rid, _ts _etag özelliklerinin değerlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="01eed-111">Resource object contains the values of the _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="01eed-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01eed-112">PARAMETERS</span></span>

### <span data-ttu-id="01eed-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01eed-113">-AccountName</span></span>
<span data-ttu-id="01eed-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="01eed-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="01eed-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="01eed-115">-Confirm</span></span>
<span data-ttu-id="01eed-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01eed-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01eed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01eed-117">-DefaultProfile</span></span>
<span data-ttu-id="01eed-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01eed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01eed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01eed-119">-InputObject</span></span>
<span data-ttu-id="01eed-120">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="01eed-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="01eed-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="01eed-121">-Name</span></span>
<span data-ttu-id="01eed-122">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="01eed-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="01eed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01eed-123">-ResourceGroupName</span></span>
<span data-ttu-id="01eed-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="01eed-124">Name of resource group.</span></span>

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

### <span data-ttu-id="01eed-125">-Üretim</span><span class="sxs-lookup"><span data-stu-id="01eed-125">-Throughput</span></span>
<span data-ttu-id="01eed-126">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="01eed-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="01eed-127">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="01eed-127">Default value is 400.</span></span>

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

### <span data-ttu-id="01eed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01eed-128">-WhatIf</span></span>
<span data-ttu-id="01eed-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01eed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01eed-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01eed-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01eed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01eed-131">CommonParameters</span></span>
<span data-ttu-id="01eed-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01eed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01eed-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="01eed-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01eed-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01eed-134">INPUTS</span></span>

### <span data-ttu-id="01eed-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="01eed-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="01eed-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01eed-136">OUTPUTS</span></span>

### <span data-ttu-id="01eed-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="01eed-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="01eed-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01eed-138">NOTES</span></span>

## <span data-ttu-id="01eed-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01eed-139">RELATED LINKS</span></span>
