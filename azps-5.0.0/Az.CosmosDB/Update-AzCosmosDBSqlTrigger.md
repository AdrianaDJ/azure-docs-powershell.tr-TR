---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321322"
---
# <span data-ttu-id="de55a-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="de55a-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="de55a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de55a-102">SYNOPSIS</span></span>
<span data-ttu-id="de55a-103">CosmosDB SQL tetikleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="de55a-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="de55a-104">Var olan tetikleyiciyi okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="de55a-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="de55a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de55a-105">SYNTAX</span></span>

### <span data-ttu-id="de55a-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="de55a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de55a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de55a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de55a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de55a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de55a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="de55a-109">DESCRIPTION</span></span>
<span data-ttu-id="de55a-110">CosmosDB SQL tetikleyicisini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="de55a-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="de55a-111">Var olan tetikleyiciyi okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="de55a-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="de55a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de55a-112">EXAMPLES</span></span>

### <span data-ttu-id="de55a-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="de55a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="de55a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de55a-114">PARAMETERS</span></span>

### <span data-ttu-id="de55a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de55a-115">-AccountName</span></span>
<span data-ttu-id="de55a-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="de55a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="de55a-117">-Gövde</span><span class="sxs-lookup"><span data-stu-id="de55a-117">-Body</span></span>
<span data-ttu-id="de55a-118">Tetikleyicinin gövdesi.</span><span class="sxs-lookup"><span data-stu-id="de55a-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="de55a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="de55a-119">-Confirm</span></span>
<span data-ttu-id="de55a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de55a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de55a-121">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="de55a-121">-ContainerName</span></span>
<span data-ttu-id="de55a-122">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="de55a-122">Container name.</span></span>

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

### <span data-ttu-id="de55a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de55a-123">-DatabaseName</span></span>
<span data-ttu-id="de55a-124">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="de55a-124">Database name.</span></span>

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

### <span data-ttu-id="de55a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de55a-125">-DefaultProfile</span></span>
<span data-ttu-id="de55a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="de55a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de55a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de55a-127">-InputObject</span></span>
<span data-ttu-id="de55a-128">SQL tetik nesnesi</span><span class="sxs-lookup"><span data-stu-id="de55a-128">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de55a-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="de55a-129">-Name</span></span>
<span data-ttu-id="de55a-130">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="de55a-130">Trigger name.</span></span>

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

### <span data-ttu-id="de55a-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="de55a-131">-ParentObject</span></span>
<span data-ttu-id="de55a-132">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="de55a-132">Sql Container object.</span></span>

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

### <span data-ttu-id="de55a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de55a-133">-ResourceGroupName</span></span>
<span data-ttu-id="de55a-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="de55a-134">Name of resource group.</span></span>

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

### <span data-ttu-id="de55a-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="de55a-135">-TriggerOperation</span></span>
<span data-ttu-id="de55a-136">Tetikleyicinin ilişkilendirildiği işlem.</span><span class="sxs-lookup"><span data-stu-id="de55a-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="de55a-137">Olası değerler: ' tümü ', ' oluştur ', ' Güncelleştir ', ' Sil ', ' Değiştir '</span><span class="sxs-lookup"><span data-stu-id="de55a-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="de55a-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="de55a-138">-TriggerType</span></span>
<span data-ttu-id="de55a-139">Tetik türü.</span><span class="sxs-lookup"><span data-stu-id="de55a-139">Type of the Trigger.</span></span>
<span data-ttu-id="de55a-140">Olası değerler: ' Pre ', ' Post '</span><span class="sxs-lookup"><span data-stu-id="de55a-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="de55a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de55a-141">-WhatIf</span></span>
<span data-ttu-id="de55a-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de55a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de55a-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de55a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de55a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de55a-144">CommonParameters</span></span>
<span data-ttu-id="de55a-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de55a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de55a-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="de55a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de55a-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de55a-147">INPUTS</span></span>

### <span data-ttu-id="de55a-148">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="de55a-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="de55a-149">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="de55a-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="de55a-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de55a-150">OUTPUTS</span></span>

### <span data-ttu-id="de55a-151">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="de55a-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="de55a-152">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="de55a-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="de55a-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de55a-153">NOTES</span></span>

## <span data-ttu-id="de55a-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de55a-154">RELATED LINKS</span></span>
