---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321673"
---
# <span data-ttu-id="dd479-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="dd479-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="dd479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd479-102">SYNOPSIS</span></span>
<span data-ttu-id="dd479-103">CosmosDB SQL kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="dd479-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="dd479-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd479-104">SYNTAX</span></span>

### <span data-ttu-id="dd479-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd479-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="dd479-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd479-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd479-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd479-107">DESCRIPTION</span></span>
<span data-ttu-id="dd479-108">**Get-AzCosmosDBSqlContainer** cmdlet 'i, belirli bir Resourcegroupname, AccountName ve DatabaseName için var olan Cosmosdb SQL kapsayıcılarının listesini alır ve belirli bir Resourcegroupname, AccountName, DatabaseName ve ContainerName için tek bir Cosmosdb SQL kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="dd479-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="dd479-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd479-109">EXAMPLES</span></span>

### <span data-ttu-id="dd479-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd479-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="dd479-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd479-111">PARAMETERS</span></span>

### <span data-ttu-id="dd479-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dd479-112">-AccountName</span></span>
<span data-ttu-id="dd479-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="dd479-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dd479-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd479-114">-DatabaseName</span></span>
<span data-ttu-id="dd479-115">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="dd479-115">Database name.</span></span>

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

### <span data-ttu-id="dd479-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd479-116">-DefaultProfile</span></span>
<span data-ttu-id="dd479-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd479-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd479-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd479-118">-Name</span></span>
<span data-ttu-id="dd479-119">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="dd479-119">Container name.</span></span>

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

### <span data-ttu-id="dd479-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dd479-120">-ParentObject</span></span>
<span data-ttu-id="dd479-121">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dd479-121">Sql Database object.</span></span>

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

### <span data-ttu-id="dd479-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd479-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd479-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dd479-123">Name of resource group.</span></span>

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

### <span data-ttu-id="dd479-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd479-124">CommonParameters</span></span>
<span data-ttu-id="dd479-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd479-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd479-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dd479-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd479-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd479-127">INPUTS</span></span>

### <span data-ttu-id="dd479-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dd479-128">None</span></span>

## <span data-ttu-id="dd479-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd479-129">OUTPUTS</span></span>

### <span data-ttu-id="dd479-130">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="dd479-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="dd479-131">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dd479-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dd479-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd479-132">NOTES</span></span>

## <span data-ttu-id="dd479-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd479-133">RELATED LINKS</span></span>
