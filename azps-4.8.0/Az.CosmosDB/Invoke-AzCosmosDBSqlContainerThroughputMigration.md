---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbsqlcontainerthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBSqlContainerThroughputMigration.md
ms.openlocfilehash: 61b564e8b92193b873e815b4a65f7c009dabf0f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274631"
---
# <span data-ttu-id="e55bb-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="e55bb-101">Invoke-AzCosmosDBSqlContainerThroughputMigration</span></span>

## <span data-ttu-id="e55bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e55bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e55bb-103">Otomatik ölçeklendirme çıkışını elle üretilen işleme geçirmek için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="e55bb-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="e55bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e55bb-104">SYNTAX</span></span>

### <span data-ttu-id="e55bb-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e55bb-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e55bb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e55bb-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e55bb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e55bb-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBSqlContainerThroughputMigration [-Name <String>] -InputObject <PSSqlContainerGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e55bb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e55bb-108">DESCRIPTION</span></span>
<span data-ttu-id="e55bb-109">ThroughpyteType paramter, geçiş yapmak istediğiniz üretimi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e55bb-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="e55bb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e55bb-110">EXAMPLES</span></span>

### <span data-ttu-id="e55bb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e55bb-111">Example 1</span></span>
```powershell
PS C:\>$NewSqlContainer =  New-AzCosmosDBSqlContainer -AccountName myAccountName -ResourceGroupName myRgName -Name myContainerName  -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBSqlContainerThroughputMigration -InputObject $NewSqlContainer -ThroughputType Autoscale
```


## <span data-ttu-id="e55bb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e55bb-112">PARAMETERS</span></span>

### <span data-ttu-id="e55bb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e55bb-113">-AccountName</span></span>
<span data-ttu-id="e55bb-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="e55bb-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e55bb-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="e55bb-115">-Confirm</span></span>
<span data-ttu-id="e55bb-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e55bb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e55bb-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e55bb-117">-DatabaseName</span></span>
<span data-ttu-id="e55bb-118">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="e55bb-118">Database name.</span></span>

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

### <span data-ttu-id="e55bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e55bb-119">-DefaultProfile</span></span>
<span data-ttu-id="e55bb-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e55bb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e55bb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e55bb-121">-InputObject</span></span>
<span data-ttu-id="e55bb-122">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e55bb-122">Sql Container object.</span></span>

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

### <span data-ttu-id="e55bb-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e55bb-123">-Name</span></span>
<span data-ttu-id="e55bb-124">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="e55bb-124">Container name.</span></span>

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

### <span data-ttu-id="e55bb-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e55bb-125">-ParentObject</span></span>
<span data-ttu-id="e55bb-126">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e55bb-126">Sql Database object.</span></span>

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

### <span data-ttu-id="e55bb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e55bb-127">-ResourceGroupName</span></span>
<span data-ttu-id="e55bb-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e55bb-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e55bb-129">-Throughınputtype</span><span class="sxs-lookup"><span data-stu-id="e55bb-129">-ThroughputType</span></span>
<span data-ttu-id="e55bb-130">Geçirilecek aktarım türü.</span><span class="sxs-lookup"><span data-stu-id="e55bb-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="e55bb-131">Olası değerler: otomatik ölçeklendirme, El Ile.</span><span class="sxs-lookup"><span data-stu-id="e55bb-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="e55bb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e55bb-132">-WhatIf</span></span>
<span data-ttu-id="e55bb-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e55bb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e55bb-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e55bb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e55bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55bb-135">CommonParameters</span></span>
<span data-ttu-id="e55bb-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e55bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55bb-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e55bb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55bb-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e55bb-138">INPUTS</span></span>

### <span data-ttu-id="e55bb-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e55bb-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e55bb-140">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e55bb-140">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="e55bb-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e55bb-141">OUTPUTS</span></span>

### <span data-ttu-id="e55bb-142">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e55bb-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e55bb-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e55bb-143">NOTES</span></span>

## <span data-ttu-id="e55bb-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e55bb-144">RELATED LINKS</span></span>
