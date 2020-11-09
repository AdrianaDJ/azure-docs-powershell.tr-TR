---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321586"
---
# <span data-ttu-id="55ccb-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="55ccb-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="55ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="55ccb-103">Yeni bir CosmosDB Cassandra anahtar uzayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55ccb-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="55ccb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55ccb-104">SYNTAX</span></span>

### <span data-ttu-id="55ccb-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55ccb-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55ccb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55ccb-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55ccb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55ccb-107">DESCRIPTION</span></span>
<span data-ttu-id="55ccb-108">Yeni bir CosmosDB Cassandra anahtar uzayı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55ccb-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="55ccb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55ccb-109">EXAMPLES</span></span>

### <span data-ttu-id="55ccb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55ccb-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="55ccb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55ccb-111">PARAMETERS</span></span>

### <span data-ttu-id="55ccb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55ccb-112">-AccountName</span></span>
<span data-ttu-id="55ccb-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="55ccb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="55ccb-114">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="55ccb-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="55ccb-115">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="55ccb-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="55ccb-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="55ccb-116">-Confirm</span></span>
<span data-ttu-id="55ccb-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55ccb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55ccb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ccb-118">-DefaultProfile</span></span>
<span data-ttu-id="55ccb-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55ccb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55ccb-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="55ccb-120">-Name</span></span>
<span data-ttu-id="55ccb-121">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="55ccb-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="55ccb-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="55ccb-122">-ParentObject</span></span>
<span data-ttu-id="55ccb-123">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="55ccb-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="55ccb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ccb-124">-ResourceGroupName</span></span>
<span data-ttu-id="55ccb-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="55ccb-125">Name of resource group.</span></span>

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

### <span data-ttu-id="55ccb-126">-Üretim</span><span class="sxs-lookup"><span data-stu-id="55ccb-126">-Throughput</span></span>
<span data-ttu-id="55ccb-127">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="55ccb-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="55ccb-128">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="55ccb-128">Default value is 400.</span></span>

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

### <span data-ttu-id="55ccb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55ccb-129">-WhatIf</span></span>
<span data-ttu-id="55ccb-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55ccb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55ccb-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55ccb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55ccb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ccb-132">CommonParameters</span></span>
<span data-ttu-id="55ccb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55ccb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ccb-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55ccb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ccb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55ccb-135">INPUTS</span></span>

### <span data-ttu-id="55ccb-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="55ccb-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="55ccb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55ccb-137">OUTPUTS</span></span>

### <span data-ttu-id="55ccb-138">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="55ccb-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="55ccb-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="55ccb-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="55ccb-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55ccb-140">NOTES</span></span>

## <span data-ttu-id="55ccb-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55ccb-141">RELATED LINKS</span></span>
