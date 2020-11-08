---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274199"
---
# <span data-ttu-id="58716-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="58716-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="58716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58716-102">SYNOPSIS</span></span>
<span data-ttu-id="58716-103">Otomatik ölçeklendirme çıkışını elle üretilen işleme geçirmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="58716-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="58716-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58716-104">SYNTAX</span></span>

### <span data-ttu-id="58716-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58716-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58716-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58716-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58716-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58716-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58716-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="58716-108">DESCRIPTION</span></span>
<span data-ttu-id="58716-109">ThroughpyteType paramter, geçiş yapmak istediğiniz üretimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="58716-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="58716-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58716-110">EXAMPLES</span></span>

### <span data-ttu-id="58716-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="58716-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="58716-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58716-112">PARAMETERS</span></span>

### <span data-ttu-id="58716-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58716-113">-AccountName</span></span>
<span data-ttu-id="58716-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="58716-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="58716-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="58716-115">-Confirm</span></span>
<span data-ttu-id="58716-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58716-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58716-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58716-117">-DefaultProfile</span></span>
<span data-ttu-id="58716-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58716-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58716-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58716-119">-InputObject</span></span>
<span data-ttu-id="58716-120">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="58716-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="58716-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="58716-121">-Name</span></span>
<span data-ttu-id="58716-122">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="58716-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="58716-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="58716-123">-ParentObject</span></span>
<span data-ttu-id="58716-124">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="58716-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="58716-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58716-125">-ResourceGroupName</span></span>
<span data-ttu-id="58716-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="58716-126">Name of resource group.</span></span>

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

### <span data-ttu-id="58716-127">-Throughınputtype</span><span class="sxs-lookup"><span data-stu-id="58716-127">-ThroughputType</span></span>
<span data-ttu-id="58716-128">Geçirilecek aktarım türü.</span><span class="sxs-lookup"><span data-stu-id="58716-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="58716-129">Olası değerler: otomatik ölçeklendirme, El Ile.</span><span class="sxs-lookup"><span data-stu-id="58716-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="58716-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58716-130">-WhatIf</span></span>
<span data-ttu-id="58716-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58716-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58716-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="58716-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58716-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58716-133">CommonParameters</span></span>
<span data-ttu-id="58716-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58716-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58716-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="58716-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58716-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58716-136">INPUTS</span></span>

### <span data-ttu-id="58716-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="58716-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="58716-138">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="58716-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="58716-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58716-139">OUTPUTS</span></span>

### <span data-ttu-id="58716-140">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="58716-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="58716-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58716-141">NOTES</span></span>

## <span data-ttu-id="58716-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58716-142">RELATED LINKS</span></span>
