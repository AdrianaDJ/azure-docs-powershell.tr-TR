---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267842"
---
# <span data-ttu-id="40e36-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="40e36-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="40e36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40e36-102">SYNOPSIS</span></span>
<span data-ttu-id="40e36-103">CosmosDB SQL StoredProcedure 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="40e36-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="40e36-104">Var olan StoredProcedure 'ı okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="40e36-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="40e36-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40e36-105">SYNTAX</span></span>

### <span data-ttu-id="40e36-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="40e36-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e36-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40e36-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e36-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40e36-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40e36-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="40e36-109">DESCRIPTION</span></span>
<span data-ttu-id="40e36-110">CosmosDB SQL StoredProcedure 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="40e36-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="40e36-111">Var olan StoredProcedure 'ı okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="40e36-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="40e36-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40e36-112">EXAMPLES</span></span>

### <span data-ttu-id="40e36-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="40e36-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="40e36-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40e36-114">PARAMETERS</span></span>

### <span data-ttu-id="40e36-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40e36-115">-AccountName</span></span>
<span data-ttu-id="40e36-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="40e36-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40e36-117">-Gövde</span><span class="sxs-lookup"><span data-stu-id="40e36-117">-Body</span></span>
<span data-ttu-id="40e36-118">Saklı yordamın gövdesi.</span><span class="sxs-lookup"><span data-stu-id="40e36-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="40e36-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="40e36-119">-Confirm</span></span>
<span data-ttu-id="40e36-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40e36-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e36-121">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="40e36-121">-ContainerName</span></span>
<span data-ttu-id="40e36-122">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="40e36-122">Container name.</span></span>

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

### <span data-ttu-id="40e36-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40e36-123">-DatabaseName</span></span>
<span data-ttu-id="40e36-124">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="40e36-124">Database name.</span></span>

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

### <span data-ttu-id="40e36-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e36-125">-DefaultProfile</span></span>
<span data-ttu-id="40e36-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40e36-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40e36-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40e36-127">-InputObject</span></span>
<span data-ttu-id="40e36-128">SQL saklı yordam nesnesi</span><span class="sxs-lookup"><span data-stu-id="40e36-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40e36-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="40e36-129">-Name</span></span>
<span data-ttu-id="40e36-130">.</span><span class="sxs-lookup"><span data-stu-id="40e36-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="40e36-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="40e36-131">-ParentObject</span></span>
<span data-ttu-id="40e36-132">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="40e36-132">Sql Container object.</span></span>

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

### <span data-ttu-id="40e36-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e36-133">-ResourceGroupName</span></span>
<span data-ttu-id="40e36-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="40e36-134">Name of resource group.</span></span>

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

### <span data-ttu-id="40e36-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e36-135">-WhatIf</span></span>
<span data-ttu-id="40e36-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40e36-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e36-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40e36-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e36-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e36-138">CommonParameters</span></span>
<span data-ttu-id="40e36-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40e36-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e36-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="40e36-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e36-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40e36-141">INPUTS</span></span>

### <span data-ttu-id="40e36-142">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="40e36-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="40e36-143">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="40e36-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="40e36-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40e36-144">OUTPUTS</span></span>

### <span data-ttu-id="40e36-145">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="40e36-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="40e36-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="40e36-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="40e36-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40e36-147">NOTES</span></span>

## <span data-ttu-id="40e36-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40e36-148">RELATED LINKS</span></span>
