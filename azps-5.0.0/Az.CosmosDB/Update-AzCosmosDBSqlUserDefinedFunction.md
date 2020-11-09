---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321321"
---
# <span data-ttu-id="47a13-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="47a13-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="47a13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47a13-102">SYNOPSIS</span></span>
<span data-ttu-id="47a13-103">CosmosDB SQL Userdefinedişlevini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="47a13-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="47a13-104">Var olan Userdefinedişlevini okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="47a13-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="47a13-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47a13-105">SYNTAX</span></span>

### <span data-ttu-id="47a13-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47a13-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a13-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47a13-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47a13-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47a13-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a13-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="47a13-109">DESCRIPTION</span></span>
<span data-ttu-id="47a13-110">CosmosDB SQL Userdefinedişlevini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="47a13-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="47a13-111">Var olan Userdefinedişlevini okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="47a13-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="47a13-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47a13-112">EXAMPLES</span></span>

### <span data-ttu-id="47a13-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="47a13-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="47a13-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47a13-114">PARAMETERS</span></span>

### <span data-ttu-id="47a13-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="47a13-115">-AccountName</span></span>
<span data-ttu-id="47a13-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="47a13-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="47a13-117">-Gövde</span><span class="sxs-lookup"><span data-stu-id="47a13-117">-Body</span></span>
<span data-ttu-id="47a13-118">Kullanıcı tanımlı Işlevin gövdesi.</span><span class="sxs-lookup"><span data-stu-id="47a13-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="47a13-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="47a13-119">-Confirm</span></span>
<span data-ttu-id="47a13-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47a13-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a13-121">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="47a13-121">-ContainerName</span></span>
<span data-ttu-id="47a13-122">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="47a13-122">Container name.</span></span>

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

### <span data-ttu-id="47a13-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47a13-123">-DatabaseName</span></span>
<span data-ttu-id="47a13-124">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="47a13-124">Database name.</span></span>

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

### <span data-ttu-id="47a13-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a13-125">-DefaultProfile</span></span>
<span data-ttu-id="47a13-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47a13-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47a13-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47a13-127">-InputObject</span></span>
<span data-ttu-id="47a13-128">SQL Kullanıcı tanımlı Işlev nesnesi</span><span class="sxs-lookup"><span data-stu-id="47a13-128">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47a13-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="47a13-129">-Name</span></span>
<span data-ttu-id="47a13-130">Kullanıcı tanımlı Işlev adı.</span><span class="sxs-lookup"><span data-stu-id="47a13-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="47a13-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="47a13-131">-ParentObject</span></span>
<span data-ttu-id="47a13-132">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="47a13-132">Sql Container object.</span></span>

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

### <span data-ttu-id="47a13-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47a13-133">-ResourceGroupName</span></span>
<span data-ttu-id="47a13-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="47a13-134">Name of resource group.</span></span>

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

### <span data-ttu-id="47a13-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a13-135">-WhatIf</span></span>
<span data-ttu-id="47a13-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47a13-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47a13-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47a13-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a13-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a13-138">CommonParameters</span></span>
<span data-ttu-id="47a13-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47a13-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a13-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="47a13-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a13-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47a13-141">INPUTS</span></span>

### <span data-ttu-id="47a13-142">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="47a13-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="47a13-143">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="47a13-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="47a13-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47a13-144">OUTPUTS</span></span>

### <span data-ttu-id="47a13-145">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="47a13-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="47a13-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="47a13-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="47a13-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47a13-147">NOTES</span></span>

## <span data-ttu-id="47a13-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47a13-148">RELATED LINKS</span></span>
