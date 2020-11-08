---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqldatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlDatabaseThroughputMigration.md
ms.openlocfilehash: 927cdbd6c599b090a66120e95a1ac1a024360271
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109760"
---
# <span data-ttu-id="a3ef1-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="a3ef1-101">Invoke-AzCosmosDBSqlDatabaseThroughputMigration</span></span>

## <span data-ttu-id="a3ef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ef1-103">Otomatik ölçeklendirme çıkışını elle üretilen işleme geçirmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="a3ef1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3ef1-104">SYNTAX</span></span>

### <span data-ttu-id="a3ef1-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3ef1-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3ef1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3ef1-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3ef1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3ef1-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlDatabaseThroughputMigration [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3ef1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3ef1-108">DESCRIPTION</span></span>
<span data-ttu-id="a3ef1-109">ThroughpyteType paramter, geçiş yapmak istediğiniz üretimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="a3ef1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3ef1-110">EXAMPLES</span></span>

### <span data-ttu-id="a3ef1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3ef1-111">Example 1</span></span>
```powershell
PS C:\> $NewSqlDatabase =  New-AzCosmosDBSqlDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlDatabaseThroughputMigration -InputObject $NewSqlDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="a3ef1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3ef1-112">PARAMETERS</span></span>

### <span data-ttu-id="a3ef1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a3ef1-113">-AccountName</span></span>
<span data-ttu-id="a3ef1-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a3ef1-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3ef1-115">-Confirm</span></span>
<span data-ttu-id="a3ef1-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ef1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ef1-117">-DefaultProfile</span></span>
<span data-ttu-id="a3ef1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3ef1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3ef1-119">-InputObject</span></span>
<span data-ttu-id="a3ef1-120">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-120">Sql Database object.</span></span>

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

### <span data-ttu-id="a3ef1-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3ef1-121">-Name</span></span>
<span data-ttu-id="a3ef1-122">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-122">Database name.</span></span>

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

### <span data-ttu-id="a3ef1-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a3ef1-123">-ParentObject</span></span>
<span data-ttu-id="a3ef1-124">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="a3ef1-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a3ef1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ef1-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3ef1-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-126">Name of resource group.</span></span>

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

### <span data-ttu-id="a3ef1-127">-Throughınputtype</span><span class="sxs-lookup"><span data-stu-id="a3ef1-127">-ThroughputType</span></span>
<span data-ttu-id="a3ef1-128">Geçirilecek aktarım türü.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="a3ef1-129">Olası değerler: otomatik ölçeklendirme, El Ile.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="a3ef1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ef1-130">-WhatIf</span></span>
<span data-ttu-id="a3ef1-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ef1-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ef1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ef1-133">CommonParameters</span></span>
<span data-ttu-id="a3ef1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ef1-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a3ef1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ef1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3ef1-136">INPUTS</span></span>

### <span data-ttu-id="a3ef1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="a3ef1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="a3ef1-138">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a3ef1-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="a3ef1-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3ef1-139">OUTPUTS</span></span>

### <span data-ttu-id="a3ef1-140">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a3ef1-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a3ef1-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3ef1-141">NOTES</span></span>

## <span data-ttu-id="a3ef1-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3ef1-142">RELATED LINKS</span></span>
