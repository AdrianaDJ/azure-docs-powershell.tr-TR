---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108382"
---
# <span data-ttu-id="17874-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="17874-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="17874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17874-102">SYNOPSIS</span></span>
<span data-ttu-id="17874-103">CosmosDB SQL StoredProcedure 'ı alır.</span><span class="sxs-lookup"><span data-stu-id="17874-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="17874-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17874-104">SYNTAX</span></span>

### <span data-ttu-id="17874-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="17874-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17874-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17874-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17874-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="17874-107">DESCRIPTION</span></span>
<span data-ttu-id="17874-108">**Get-AzCosmosDBSqlStoredProcedure** cmdlet 'i, belirli bir Resourcegroupname, AccountName, DatabaseName ve kapsayıcıadı için var olan tüm Cosmosdb SQL StoredProcedures listesini alır ve belirli bir Resourcegroupname, AccountName, DatabaseName, ContainerName ve StoredProcedureName için tek bir Cosmosdb SQL StoredProcedure alır.</span><span class="sxs-lookup"><span data-stu-id="17874-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="17874-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17874-109">EXAMPLES</span></span>

### <span data-ttu-id="17874-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="17874-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="17874-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17874-111">PARAMETERS</span></span>

### <span data-ttu-id="17874-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="17874-112">-AccountName</span></span>
<span data-ttu-id="17874-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="17874-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="17874-114">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="17874-114">-ContainerName</span></span>
<span data-ttu-id="17874-115">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="17874-115">Container name.</span></span>

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

### <span data-ttu-id="17874-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="17874-116">-DatabaseName</span></span>
<span data-ttu-id="17874-117">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="17874-117">Database name.</span></span>

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

### <span data-ttu-id="17874-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17874-118">-DefaultProfile</span></span>
<span data-ttu-id="17874-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17874-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17874-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="17874-120">-Name</span></span>
<span data-ttu-id="17874-121">.</span><span class="sxs-lookup"><span data-stu-id="17874-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="17874-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="17874-122">-ParentObject</span></span>
<span data-ttu-id="17874-123">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="17874-123">Sql Container object.</span></span>

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

### <span data-ttu-id="17874-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17874-124">-ResourceGroupName</span></span>
<span data-ttu-id="17874-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="17874-125">Name of resource group.</span></span>

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

### <span data-ttu-id="17874-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17874-126">CommonParameters</span></span>
<span data-ttu-id="17874-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17874-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17874-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="17874-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17874-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17874-129">INPUTS</span></span>

### <span data-ttu-id="17874-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="17874-130">None</span></span>

## <span data-ttu-id="17874-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17874-131">OUTPUTS</span></span>

### <span data-ttu-id="17874-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="17874-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="17874-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17874-133">NOTES</span></span>

## <span data-ttu-id="17874-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17874-134">RELATED LINKS</span></span>
