---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321625"
---
# <span data-ttu-id="d6016-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="d6016-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="d6016-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6016-102">SYNOPSIS</span></span>
<span data-ttu-id="d6016-103">Otomatik ölçeklendirme çıkışını elle üretilen işleme geçirmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6016-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="d6016-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6016-104">SYNTAX</span></span>

### <span data-ttu-id="d6016-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d6016-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6016-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6016-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6016-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6016-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6016-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6016-108">DESCRIPTION</span></span>
<span data-ttu-id="d6016-109">ThroughpyteType paramter, geçiş yapmak istediğiniz üretimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d6016-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="d6016-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6016-110">EXAMPLES</span></span>

### <span data-ttu-id="d6016-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d6016-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="d6016-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6016-112">PARAMETERS</span></span>

### <span data-ttu-id="d6016-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d6016-113">-AccountName</span></span>
<span data-ttu-id="d6016-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="d6016-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d6016-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="d6016-115">-Confirm</span></span>
<span data-ttu-id="d6016-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d6016-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6016-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d6016-117">-DatabaseName</span></span>
<span data-ttu-id="d6016-118">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="d6016-118">Database name.</span></span>

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

### <span data-ttu-id="d6016-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6016-119">-DefaultProfile</span></span>
<span data-ttu-id="d6016-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6016-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6016-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6016-121">-InputObject</span></span>
<span data-ttu-id="d6016-122">Gremlın grafik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d6016-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6016-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d6016-123">-Name</span></span>
<span data-ttu-id="d6016-124">Gremlın grafik adı.</span><span class="sxs-lookup"><span data-stu-id="d6016-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="d6016-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d6016-125">-ParentObject</span></span>
<span data-ttu-id="d6016-126">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d6016-126">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6016-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6016-127">-ResourceGroupName</span></span>
<span data-ttu-id="d6016-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d6016-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d6016-129">-Throughınputtype</span><span class="sxs-lookup"><span data-stu-id="d6016-129">-ThroughputType</span></span>
<span data-ttu-id="d6016-130">Geçirilecek aktarım türü.</span><span class="sxs-lookup"><span data-stu-id="d6016-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="d6016-131">Olası değerler: otomatik ölçeklendirme, El Ile.</span><span class="sxs-lookup"><span data-stu-id="d6016-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="d6016-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6016-132">-WhatIf</span></span>
<span data-ttu-id="d6016-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d6016-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6016-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d6016-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6016-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6016-135">CommonParameters</span></span>
<span data-ttu-id="d6016-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6016-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6016-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d6016-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6016-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6016-138">INPUTS</span></span>

### <span data-ttu-id="d6016-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d6016-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="d6016-140">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="d6016-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="d6016-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6016-141">OUTPUTS</span></span>

### <span data-ttu-id="d6016-142">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d6016-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d6016-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6016-143">NOTES</span></span>

## <span data-ttu-id="d6016-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6016-144">RELATED LINKS</span></span>
