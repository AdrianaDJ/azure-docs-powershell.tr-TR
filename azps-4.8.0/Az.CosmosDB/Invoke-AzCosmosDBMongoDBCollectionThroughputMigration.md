---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: e2f1449536f9b4db5b743c1a1e352e427ae86821
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274634"
---
# <span data-ttu-id="12881-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="12881-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="12881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12881-102">SYNOPSIS</span></span>
<span data-ttu-id="12881-103">Otomatik ölçeklendirme çıkışını elle üretilen işleme geçirmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="12881-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="12881-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12881-104">SYNTAX</span></span>

### <span data-ttu-id="12881-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12881-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12881-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12881-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12881-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12881-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12881-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="12881-108">DESCRIPTION</span></span>
<span data-ttu-id="12881-109">ThroughpyteType paramter, geçiş yapmak istediğiniz üretimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="12881-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="12881-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12881-110">EXAMPLES</span></span>

### <span data-ttu-id="12881-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="12881-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```


## <span data-ttu-id="12881-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12881-112">PARAMETERS</span></span>

### <span data-ttu-id="12881-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12881-113">-AccountName</span></span>
<span data-ttu-id="12881-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="12881-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="12881-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="12881-115">-Confirm</span></span>
<span data-ttu-id="12881-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12881-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12881-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="12881-117">-DatabaseName</span></span>
<span data-ttu-id="12881-118">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="12881-118">Database name.</span></span>

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

### <span data-ttu-id="12881-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12881-119">-DefaultProfile</span></span>
<span data-ttu-id="12881-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12881-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12881-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12881-121">-InputObject</span></span>
<span data-ttu-id="12881-122">Mongit koleksiyon nesnesi.</span><span class="sxs-lookup"><span data-stu-id="12881-122">Mongo Collection object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12881-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="12881-123">-Name</span></span>
<span data-ttu-id="12881-124">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="12881-124">Collection name.</span></span>

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

### <span data-ttu-id="12881-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="12881-125">-ParentObject</span></span>
<span data-ttu-id="12881-126">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="12881-126">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12881-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12881-127">-ResourceGroupName</span></span>
<span data-ttu-id="12881-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="12881-128">Name of resource group.</span></span>

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

### <span data-ttu-id="12881-129">-Throughınputtype</span><span class="sxs-lookup"><span data-stu-id="12881-129">-ThroughputType</span></span>
<span data-ttu-id="12881-130">Geçirilecek aktarım türü.</span><span class="sxs-lookup"><span data-stu-id="12881-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="12881-131">Olası değerler: otomatik ölçeklendirme, El Ile.</span><span class="sxs-lookup"><span data-stu-id="12881-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="12881-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12881-132">-WhatIf</span></span>
<span data-ttu-id="12881-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12881-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12881-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="12881-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12881-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12881-135">CommonParameters</span></span>
<span data-ttu-id="12881-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12881-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12881-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="12881-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12881-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12881-138">INPUTS</span></span>

### <span data-ttu-id="12881-139">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="12881-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="12881-140">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbcollectiongetresults</span><span class="sxs-lookup"><span data-stu-id="12881-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="12881-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12881-141">OUTPUTS</span></span>

### <span data-ttu-id="12881-142">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="12881-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="12881-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12881-143">NOTES</span></span>

## <span data-ttu-id="12881-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12881-144">RELATED LINKS</span></span>
