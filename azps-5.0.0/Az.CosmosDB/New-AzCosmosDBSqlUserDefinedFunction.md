---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321473"
---
# <span data-ttu-id="05f81-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="05f81-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="05f81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05f81-102">SYNOPSIS</span></span>
<span data-ttu-id="05f81-103">Yeni bir CosmosDB SQL Userdefinedişlevi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05f81-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="05f81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05f81-104">SYNTAX</span></span>

### <span data-ttu-id="05f81-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05f81-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05f81-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05f81-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05f81-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="05f81-107">DESCRIPTION</span></span>
<span data-ttu-id="05f81-108">Yeni bir CosmosDB SQL Userdefinedişlevi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05f81-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="05f81-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05f81-109">EXAMPLES</span></span>

### <span data-ttu-id="05f81-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="05f81-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="05f81-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05f81-111">PARAMETERS</span></span>

### <span data-ttu-id="05f81-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="05f81-112">-AccountName</span></span>
<span data-ttu-id="05f81-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="05f81-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="05f81-114">-Gövde</span><span class="sxs-lookup"><span data-stu-id="05f81-114">-Body</span></span>
<span data-ttu-id="05f81-115">Kullanıcı tanımlı Işlevin gövdesi.</span><span class="sxs-lookup"><span data-stu-id="05f81-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="05f81-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="05f81-116">-Confirm</span></span>
<span data-ttu-id="05f81-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05f81-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05f81-118">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="05f81-118">-ContainerName</span></span>
<span data-ttu-id="05f81-119">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="05f81-119">Container name.</span></span>

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

### <span data-ttu-id="05f81-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="05f81-120">-DatabaseName</span></span>
<span data-ttu-id="05f81-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="05f81-121">Database name.</span></span>

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

### <span data-ttu-id="05f81-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f81-122">-DefaultProfile</span></span>
<span data-ttu-id="05f81-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05f81-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05f81-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="05f81-124">-Name</span></span>
<span data-ttu-id="05f81-125">Kullanıcı tanımlı Işlev adı.</span><span class="sxs-lookup"><span data-stu-id="05f81-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="05f81-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="05f81-126">-ParentObject</span></span>
<span data-ttu-id="05f81-127">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="05f81-127">Sql Container object.</span></span>

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

### <span data-ttu-id="05f81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f81-128">-ResourceGroupName</span></span>
<span data-ttu-id="05f81-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="05f81-129">Name of resource group.</span></span>

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

### <span data-ttu-id="05f81-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05f81-130">-WhatIf</span></span>
<span data-ttu-id="05f81-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05f81-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05f81-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05f81-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05f81-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f81-133">CommonParameters</span></span>
<span data-ttu-id="05f81-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05f81-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f81-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="05f81-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f81-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05f81-136">INPUTS</span></span>

### <span data-ttu-id="05f81-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="05f81-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="05f81-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05f81-138">OUTPUTS</span></span>

### <span data-ttu-id="05f81-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="05f81-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="05f81-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="05f81-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="05f81-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05f81-141">NOTES</span></span>

## <span data-ttu-id="05f81-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05f81-142">RELATED LINKS</span></span>
