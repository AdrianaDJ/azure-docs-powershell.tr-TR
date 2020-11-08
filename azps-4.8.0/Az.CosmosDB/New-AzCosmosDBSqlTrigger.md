---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268345"
---
# <span data-ttu-id="1f506-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="1f506-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="1f506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f506-102">SYNOPSIS</span></span>
<span data-ttu-id="1f506-103">Yeni bir CosmosDB SQL tetikleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f506-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="1f506-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f506-104">SYNTAX</span></span>

### <span data-ttu-id="1f506-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1f506-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f506-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f506-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f506-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f506-107">DESCRIPTION</span></span>
<span data-ttu-id="1f506-108">Yeni bir CosmosDB SQL tetikleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f506-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="1f506-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f506-109">EXAMPLES</span></span>

### <span data-ttu-id="1f506-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f506-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="1f506-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f506-111">PARAMETERS</span></span>

### <span data-ttu-id="1f506-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1f506-112">-AccountName</span></span>
<span data-ttu-id="1f506-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="1f506-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1f506-114">-Gövde</span><span class="sxs-lookup"><span data-stu-id="1f506-114">-Body</span></span>
<span data-ttu-id="1f506-115">Tetikleyicinin gövdesi.</span><span class="sxs-lookup"><span data-stu-id="1f506-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="1f506-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f506-116">-Confirm</span></span>
<span data-ttu-id="1f506-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f506-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f506-118">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="1f506-118">-ContainerName</span></span>
<span data-ttu-id="1f506-119">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="1f506-119">Container name.</span></span>

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

### <span data-ttu-id="1f506-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f506-120">-DatabaseName</span></span>
<span data-ttu-id="1f506-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="1f506-121">Database name.</span></span>

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

### <span data-ttu-id="1f506-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f506-122">-DefaultProfile</span></span>
<span data-ttu-id="1f506-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f506-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f506-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f506-124">-Name</span></span>
<span data-ttu-id="1f506-125">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="1f506-125">Trigger name.</span></span>

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

### <span data-ttu-id="1f506-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1f506-126">-ParentObject</span></span>
<span data-ttu-id="1f506-127">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1f506-127">Sql Container object.</span></span>

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

### <span data-ttu-id="1f506-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f506-128">-ResourceGroupName</span></span>
<span data-ttu-id="1f506-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1f506-129">Name of resource group.</span></span>

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

### <span data-ttu-id="1f506-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="1f506-130">-TriggerOperation</span></span>
<span data-ttu-id="1f506-131">Tetikleyicinin ilişkilendirildiği işlem.</span><span class="sxs-lookup"><span data-stu-id="1f506-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="1f506-132">Olası değerler: ' tümü ', ' oluştur ', ' Güncelleştir ', ' Sil ', ' Değiştir '</span><span class="sxs-lookup"><span data-stu-id="1f506-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="1f506-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="1f506-133">-TriggerType</span></span>
<span data-ttu-id="1f506-134">Tetik türü.</span><span class="sxs-lookup"><span data-stu-id="1f506-134">Type of the Trigger.</span></span>
<span data-ttu-id="1f506-135">Olası değerler: ' Pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="1f506-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="1f506-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f506-136">-WhatIf</span></span>
<span data-ttu-id="1f506-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f506-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f506-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f506-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f506-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f506-139">CommonParameters</span></span>
<span data-ttu-id="1f506-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f506-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f506-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1f506-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f506-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f506-142">INPUTS</span></span>

### <span data-ttu-id="1f506-143">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="1f506-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="1f506-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f506-144">OUTPUTS</span></span>

### <span data-ttu-id="1f506-145">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="1f506-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="1f506-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="1f506-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="1f506-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f506-147">NOTES</span></span>

## <span data-ttu-id="1f506-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f506-148">RELATED LINKS</span></span>
