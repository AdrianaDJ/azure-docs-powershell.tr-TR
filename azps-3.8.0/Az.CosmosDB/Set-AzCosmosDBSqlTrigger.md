---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096028"
---
# <span data-ttu-id="d80f6-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="d80f6-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="d80f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d80f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d80f6-103">Yeni bir CosmosDB SQL tetikleyicisini oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d80f6-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="d80f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d80f6-104">SYNTAX</span></span>

### <span data-ttu-id="d80f6-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d80f6-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80f6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d80f6-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d80f6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d80f6-107">DESCRIPTION</span></span>
<span data-ttu-id="d80f6-108">**Set-AzCosmosDBSqlTrigger** cmdlet 'i, yeni bir</span><span class="sxs-lookup"><span data-stu-id="d80f6-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="d80f6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d80f6-109">EXAMPLES</span></span>

### <span data-ttu-id="d80f6-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d80f6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="d80f6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d80f6-111">PARAMETERS</span></span>

### <span data-ttu-id="d80f6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d80f6-112">-AccountName</span></span>
<span data-ttu-id="d80f6-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="d80f6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d80f6-114">-Gövde</span><span class="sxs-lookup"><span data-stu-id="d80f6-114">-Body</span></span>
<span data-ttu-id="d80f6-115">Tetikleyicinin gövdesi.</span><span class="sxs-lookup"><span data-stu-id="d80f6-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="d80f6-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="d80f6-116">-Confirm</span></span>
<span data-ttu-id="d80f6-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d80f6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d80f6-118">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="d80f6-118">-ContainerName</span></span>
<span data-ttu-id="d80f6-119">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="d80f6-119">Container name.</span></span>

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

### <span data-ttu-id="d80f6-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d80f6-120">-DatabaseName</span></span>
<span data-ttu-id="d80f6-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="d80f6-121">Database name.</span></span>

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

### <span data-ttu-id="d80f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80f6-122">-DefaultProfile</span></span>
<span data-ttu-id="d80f6-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d80f6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d80f6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d80f6-124">-InputObject</span></span>
<span data-ttu-id="d80f6-125">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d80f6-125">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d80f6-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="d80f6-126">-Name</span></span>
<span data-ttu-id="d80f6-127">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="d80f6-127">Trigger name.</span></span>

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

### <span data-ttu-id="d80f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d80f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="d80f6-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d80f6-129">Name of resource group.</span></span>

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

### <span data-ttu-id="d80f6-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="d80f6-130">-TriggerOperation</span></span>
<span data-ttu-id="d80f6-131">Tetikleyicinin ilişkilendirildiği işlem.</span><span class="sxs-lookup"><span data-stu-id="d80f6-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="d80f6-132">Olası değerler: ' tümü ', ' oluştur ', ' Güncelleştir ', ' Sil ', ' Değiştir '</span><span class="sxs-lookup"><span data-stu-id="d80f6-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="d80f6-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="d80f6-133">-TriggerType</span></span>
<span data-ttu-id="d80f6-134">Tetik türü.</span><span class="sxs-lookup"><span data-stu-id="d80f6-134">Type of the Trigger.</span></span>
<span data-ttu-id="d80f6-135">Olası değerler: ' Pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="d80f6-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="d80f6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80f6-136">-WhatIf</span></span>
<span data-ttu-id="d80f6-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d80f6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d80f6-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d80f6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d80f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80f6-139">CommonParameters</span></span>
<span data-ttu-id="d80f6-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d80f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80f6-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d80f6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80f6-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d80f6-142">INPUTS</span></span>

### <span data-ttu-id="d80f6-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d80f6-143">None</span></span>

## <span data-ttu-id="d80f6-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d80f6-144">OUTPUTS</span></span>

### <span data-ttu-id="d80f6-145">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="d80f6-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="d80f6-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d80f6-146">NOTES</span></span>

## <span data-ttu-id="d80f6-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d80f6-147">RELATED LINKS</span></span>
