---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: c8cfb1077f418c9d671729cb0ff762141a7b77c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937534"
---
# <span data-ttu-id="1b52e-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="1b52e-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="1b52e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b52e-102">SYNOPSIS</span></span>
<span data-ttu-id="1b52e-103">CosmosDB SQL Kullanıcı tanımlı Işlevini alır.</span><span class="sxs-lookup"><span data-stu-id="1b52e-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="1b52e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b52e-104">SYNTAX</span></span>

### <span data-ttu-id="1b52e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b52e-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b52e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b52e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b52e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b52e-107">DESCRIPTION</span></span>
<span data-ttu-id="1b52e-108">**Get-AzCosmosDBSqlUserDefinedFunction** cmdlet 'i, belirli bir Resourcegroupname, AccountName, DatabaseName ve ContainerName için var olan Cosmosdb SQL userdefinedişlevlerinin listesini alır ve belirli bir Resourcegroupname, AccountName, DatabaseName, ContainerName ve userdefinedfonksiyonadı için tek bir Cosmosdb SQL userdefinedişlevi alır.</span><span class="sxs-lookup"><span data-stu-id="1b52e-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="1b52e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b52e-109">EXAMPLES</span></span>

### <span data-ttu-id="1b52e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b52e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="1b52e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b52e-111">PARAMETERS</span></span>

### <span data-ttu-id="1b52e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b52e-112">-AccountName</span></span>
<span data-ttu-id="1b52e-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="1b52e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1b52e-114">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="1b52e-114">-ContainerName</span></span>
<span data-ttu-id="1b52e-115">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="1b52e-115">Container name.</span></span>

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

### <span data-ttu-id="1b52e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b52e-116">-DatabaseName</span></span>
<span data-ttu-id="1b52e-117">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="1b52e-117">Database name.</span></span>

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

### <span data-ttu-id="1b52e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b52e-118">-DefaultProfile</span></span>
<span data-ttu-id="1b52e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b52e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b52e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b52e-120">-InputObject</span></span>
<span data-ttu-id="1b52e-121">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1b52e-121">Sql Container object.</span></span>

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

### <span data-ttu-id="1b52e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b52e-122">-Name</span></span>
<span data-ttu-id="1b52e-123">Kullanıcı tanımlı Işlev adı.</span><span class="sxs-lookup"><span data-stu-id="1b52e-123">User Defined Function Name.</span></span>

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

### <span data-ttu-id="1b52e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b52e-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b52e-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1b52e-125">Name of resource group.</span></span>

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

### <span data-ttu-id="1b52e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b52e-126">CommonParameters</span></span>
<span data-ttu-id="1b52e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b52e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b52e-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b52e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b52e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b52e-129">INPUTS</span></span>

### <span data-ttu-id="1b52e-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1b52e-130">None</span></span>

## <span data-ttu-id="1b52e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b52e-131">OUTPUTS</span></span>

### <span data-ttu-id="1b52e-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="1b52e-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="1b52e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b52e-133">NOTES</span></span>

## <span data-ttu-id="1b52e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b52e-134">RELATED LINKS</span></span>
