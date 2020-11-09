---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 927cdbd6c599b090a66120e95a1ac1a024360271
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321610"
---
# <span data-ttu-id="a0a74-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="a0a74-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="a0a74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0a74-102">SYNOPSIS</span></span>
<span data-ttu-id="a0a74-103">Otomatik ölçeklendirme çıkışını elle üretilen işleme geçirmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0a74-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="a0a74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0a74-104">SYNTAX</span></span>

### <span data-ttu-id="a0a74-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0a74-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0a74-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0a74-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0a74-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0a74-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0a74-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0a74-108">DESCRIPTION</span></span>
<span data-ttu-id="a0a74-109">ThroughpyteType paramter, geçiş yapmak istediğiniz üretimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a0a74-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="a0a74-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0a74-110">EXAMPLES</span></span>

### <span data-ttu-id="a0a74-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0a74-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="a0a74-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0a74-112">PARAMETERS</span></span>

### <span data-ttu-id="a0a74-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a0a74-113">-AccountName</span></span>
<span data-ttu-id="a0a74-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="a0a74-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a0a74-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0a74-115">-Confirm</span></span>
<span data-ttu-id="a0a74-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0a74-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0a74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0a74-117">-DefaultProfile</span></span>
<span data-ttu-id="a0a74-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0a74-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0a74-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0a74-119">-InputObject</span></span>
<span data-ttu-id="a0a74-120">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a0a74-120">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0a74-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0a74-121">-Name</span></span>
<span data-ttu-id="a0a74-122">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="a0a74-122">Database name.</span></span>

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

### <span data-ttu-id="a0a74-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a0a74-123">-ParentObject</span></span>
<span data-ttu-id="a0a74-124">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="a0a74-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a0a74-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0a74-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0a74-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a0a74-126">Name of resource group.</span></span>

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

### <span data-ttu-id="a0a74-127">-Throughınputtype</span><span class="sxs-lookup"><span data-stu-id="a0a74-127">-ThroughputType</span></span>
<span data-ttu-id="a0a74-128">Geçirilecek aktarım türü.</span><span class="sxs-lookup"><span data-stu-id="a0a74-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="a0a74-129">Olası değerler: otomatik ölçeklendirme, El Ile.</span><span class="sxs-lookup"><span data-stu-id="a0a74-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="a0a74-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0a74-130">-WhatIf</span></span>
<span data-ttu-id="a0a74-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0a74-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0a74-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0a74-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0a74-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0a74-133">CommonParameters</span></span>
<span data-ttu-id="a0a74-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0a74-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0a74-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0a74-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0a74-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0a74-136">INPUTS</span></span>

### <span data-ttu-id="a0a74-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="a0a74-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="a0a74-138">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a0a74-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="a0a74-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0a74-139">OUTPUTS</span></span>

### <span data-ttu-id="a0a74-140">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a0a74-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a0a74-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0a74-141">NOTES</span></span>

## <span data-ttu-id="a0a74-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0a74-142">RELATED LINKS</span></span>
