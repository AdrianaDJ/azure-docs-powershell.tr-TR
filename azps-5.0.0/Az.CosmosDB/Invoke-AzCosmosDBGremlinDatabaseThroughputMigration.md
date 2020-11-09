---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 84039f883937354cf8c8fae3c99bfbc6f73bb574
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321630"
---
# <span data-ttu-id="b121b-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="b121b-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="b121b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b121b-102">SYNOPSIS</span></span>
<span data-ttu-id="b121b-103">Otomatik ölçeklendirme çıkışını elle üretilen işleme geçirmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="b121b-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="b121b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b121b-104">SYNTAX</span></span>

### <span data-ttu-id="b121b-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b121b-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b121b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b121b-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b121b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b121b-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b121b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b121b-108">DESCRIPTION</span></span>
<span data-ttu-id="b121b-109">ThroughpyteType paramter, geçiş yapmak istediğiniz üretimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b121b-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="b121b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b121b-110">EXAMPLES</span></span>

### <span data-ttu-id="b121b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b121b-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```


## <span data-ttu-id="b121b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b121b-112">PARAMETERS</span></span>

### <span data-ttu-id="b121b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b121b-113">-AccountName</span></span>
<span data-ttu-id="b121b-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="b121b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b121b-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="b121b-115">-Confirm</span></span>
<span data-ttu-id="b121b-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b121b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b121b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b121b-117">-DefaultProfile</span></span>
<span data-ttu-id="b121b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b121b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b121b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b121b-119">-InputObject</span></span>
<span data-ttu-id="b121b-120">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b121b-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b121b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="b121b-121">-Name</span></span>
<span data-ttu-id="b121b-122">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="b121b-122">Database name.</span></span>

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

### <span data-ttu-id="b121b-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b121b-123">-ParentObject</span></span>
<span data-ttu-id="b121b-124">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="b121b-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b121b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b121b-125">-ResourceGroupName</span></span>
<span data-ttu-id="b121b-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b121b-126">Name of resource group.</span></span>

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

### <span data-ttu-id="b121b-127">-Throughınputtype</span><span class="sxs-lookup"><span data-stu-id="b121b-127">-ThroughputType</span></span>
<span data-ttu-id="b121b-128">Geçirilecek aktarım türü.</span><span class="sxs-lookup"><span data-stu-id="b121b-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="b121b-129">Olası değerler: otomatik ölçeklendirme, El Ile.</span><span class="sxs-lookup"><span data-stu-id="b121b-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="b121b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b121b-130">-WhatIf</span></span>
<span data-ttu-id="b121b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b121b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b121b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b121b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b121b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b121b-133">CommonParameters</span></span>
<span data-ttu-id="b121b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b121b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b121b-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b121b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b121b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b121b-136">INPUTS</span></span>

### <span data-ttu-id="b121b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="b121b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="b121b-138">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b121b-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b121b-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b121b-139">OUTPUTS</span></span>

### <span data-ttu-id="b121b-140">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b121b-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b121b-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b121b-141">NOTES</span></span>

## <span data-ttu-id="b121b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b121b-142">RELATED LINKS</span></span>
