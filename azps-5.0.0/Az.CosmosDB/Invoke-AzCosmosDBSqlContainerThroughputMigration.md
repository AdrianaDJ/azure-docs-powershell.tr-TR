---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321618"
---
# <span data-ttu-id="378d5-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="378d5-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="378d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="378d5-102">SYNOPSIS</span></span>
<span data-ttu-id="378d5-103">Otomatik ölçeklendirme çıkışını elle üretilen işleme geçirmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="378d5-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="378d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="378d5-104">SYNTAX</span></span>

### <span data-ttu-id="378d5-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="378d5-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="378d5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="378d5-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="378d5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="378d5-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="378d5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="378d5-108">DESCRIPTION</span></span>
<span data-ttu-id="378d5-109">ThroughpyteType paramter, geçiş yapmak istediğiniz üretimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="378d5-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="378d5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="378d5-110">EXAMPLES</span></span>

### <span data-ttu-id="378d5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="378d5-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="378d5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="378d5-112">PARAMETERS</span></span>

### <span data-ttu-id="378d5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="378d5-113">-AccountName</span></span>
<span data-ttu-id="378d5-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="378d5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="378d5-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="378d5-115">-Confirm</span></span>
<span data-ttu-id="378d5-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="378d5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="378d5-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="378d5-117">-DatabaseName</span></span>
<span data-ttu-id="378d5-118">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="378d5-118">Database name.</span></span>

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

### <span data-ttu-id="378d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378d5-119">-DefaultProfile</span></span>
<span data-ttu-id="378d5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="378d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="378d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="378d5-121">-InputObject</span></span>
<span data-ttu-id="378d5-122">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="378d5-122">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="378d5-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="378d5-123">-Name</span></span>
<span data-ttu-id="378d5-124">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="378d5-124">Container name.</span></span>

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

### <span data-ttu-id="378d5-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="378d5-125">-ParentObject</span></span>
<span data-ttu-id="378d5-126">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="378d5-126">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="378d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="378d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="378d5-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="378d5-128">Name of resource group.</span></span>

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

### <span data-ttu-id="378d5-129">-Throughınputtype</span><span class="sxs-lookup"><span data-stu-id="378d5-129">-ThroughputType</span></span>
<span data-ttu-id="378d5-130">Geçirilecek aktarım türü.</span><span class="sxs-lookup"><span data-stu-id="378d5-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="378d5-131">Olası değerler: otomatik ölçeklendirme, El Ile.</span><span class="sxs-lookup"><span data-stu-id="378d5-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="378d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="378d5-132">-WhatIf</span></span>
<span data-ttu-id="378d5-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="378d5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="378d5-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="378d5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="378d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378d5-135">CommonParameters</span></span>
<span data-ttu-id="378d5-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="378d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378d5-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="378d5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378d5-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="378d5-138">INPUTS</span></span>

### <span data-ttu-id="378d5-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="378d5-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="378d5-140">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="378d5-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="378d5-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="378d5-141">OUTPUTS</span></span>

### <span data-ttu-id="378d5-142">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="378d5-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="378d5-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="378d5-143">NOTES</span></span>

## <span data-ttu-id="378d5-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="378d5-144">RELATED LINKS</span></span>
