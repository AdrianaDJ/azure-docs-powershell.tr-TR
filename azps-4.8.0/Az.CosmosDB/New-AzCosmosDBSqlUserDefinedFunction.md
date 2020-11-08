---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274614"
---
# <span data-ttu-id="2cbf0-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="2cbf0-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="2cbf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbf0-103">Yeni bir CosmosDB SQL Userdefinedişlevi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="2cbf0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cbf0-104">SYNTAX</span></span>

### <span data-ttu-id="2cbf0-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2cbf0-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cbf0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cbf0-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cbf0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cbf0-107">DESCRIPTION</span></span>
<span data-ttu-id="2cbf0-108">Yeni bir CosmosDB SQL Userdefinedişlevi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="2cbf0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cbf0-109">EXAMPLES</span></span>

### <span data-ttu-id="2cbf0-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2cbf0-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="2cbf0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cbf0-111">PARAMETERS</span></span>

### <span data-ttu-id="2cbf0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2cbf0-112">-AccountName</span></span>
<span data-ttu-id="2cbf0-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2cbf0-114">-Gövde</span><span class="sxs-lookup"><span data-stu-id="2cbf0-114">-Body</span></span>
<span data-ttu-id="2cbf0-115">Kullanıcı tanımlı Işlevin gövdesi.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="2cbf0-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="2cbf0-116">-Confirm</span></span>
<span data-ttu-id="2cbf0-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cbf0-118">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="2cbf0-118">-ContainerName</span></span>
<span data-ttu-id="2cbf0-119">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-119">Container name.</span></span>

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

### <span data-ttu-id="2cbf0-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2cbf0-120">-DatabaseName</span></span>
<span data-ttu-id="2cbf0-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-121">Database name.</span></span>

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

### <span data-ttu-id="2cbf0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbf0-122">-DefaultProfile</span></span>
<span data-ttu-id="2cbf0-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cbf0-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="2cbf0-124">-Name</span></span>
<span data-ttu-id="2cbf0-125">Kullanıcı tanımlı Işlev adı.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="2cbf0-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2cbf0-126">-ParentObject</span></span>
<span data-ttu-id="2cbf0-127">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-127">Sql Container object.</span></span>

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

### <span data-ttu-id="2cbf0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cbf0-128">-ResourceGroupName</span></span>
<span data-ttu-id="2cbf0-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-129">Name of resource group.</span></span>

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

### <span data-ttu-id="2cbf0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cbf0-130">-WhatIf</span></span>
<span data-ttu-id="2cbf0-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cbf0-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cbf0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbf0-133">CommonParameters</span></span>
<span data-ttu-id="2cbf0-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbf0-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2cbf0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbf0-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cbf0-136">INPUTS</span></span>

### <span data-ttu-id="2cbf0-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2cbf0-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="2cbf0-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cbf0-138">OUTPUTS</span></span>

### <span data-ttu-id="2cbf0-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="2cbf0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="2cbf0-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="2cbf0-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="2cbf0-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cbf0-141">NOTES</span></span>

## <span data-ttu-id="2cbf0-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cbf0-142">RELATED LINKS</span></span>
