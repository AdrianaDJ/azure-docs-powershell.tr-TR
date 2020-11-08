---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104108"
---
# <span data-ttu-id="1642a-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="1642a-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="1642a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1642a-102">SYNOPSIS</span></span>
<span data-ttu-id="1642a-103">CosmosDB SQL kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="1642a-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="1642a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1642a-104">SYNTAX</span></span>

### <span data-ttu-id="1642a-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1642a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="1642a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1642a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1642a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1642a-107">DESCRIPTION</span></span>
<span data-ttu-id="1642a-108">**Get-AzCosmosDBSqlContainer** cmdlet 'i, belirli bir Resourcegroupname, AccountName ve DatabaseName için var olan Cosmosdb SQL kapsayıcılarının listesini alır ve belirli bir Resourcegroupname, AccountName, DatabaseName ve ContainerName için tek bir Cosmosdb SQL kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="1642a-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="1642a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1642a-109">EXAMPLES</span></span>

### <span data-ttu-id="1642a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1642a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="1642a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1642a-111">PARAMETERS</span></span>

### <span data-ttu-id="1642a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1642a-112">-AccountName</span></span>
<span data-ttu-id="1642a-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="1642a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1642a-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1642a-114">-DatabaseName</span></span>
<span data-ttu-id="1642a-115">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="1642a-115">Database name.</span></span>

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

### <span data-ttu-id="1642a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1642a-116">-DefaultProfile</span></span>
<span data-ttu-id="1642a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1642a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1642a-118">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="1642a-118">-Detailed</span></span>
<span data-ttu-id="1642a-119">Sağlanmışsa, cmdlet, üretilen iş değerini içeren kapsayıcıyı döndürür.</span><span class="sxs-lookup"><span data-stu-id="1642a-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1642a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1642a-120">-InputObject</span></span>
<span data-ttu-id="1642a-121">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1642a-121">Sql Database object.</span></span>

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

### <span data-ttu-id="1642a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="1642a-122">-Name</span></span>
<span data-ttu-id="1642a-123">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="1642a-123">Container name.</span></span>

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

### <span data-ttu-id="1642a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1642a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1642a-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1642a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="1642a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1642a-126">CommonParameters</span></span>
<span data-ttu-id="1642a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1642a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1642a-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1642a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1642a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1642a-129">INPUTS</span></span>

### <span data-ttu-id="1642a-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1642a-130">None</span></span>

## <span data-ttu-id="1642a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1642a-131">OUTPUTS</span></span>

### <span data-ttu-id="1642a-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="1642a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="1642a-133">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1642a-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1642a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1642a-134">NOTES</span></span>

## <span data-ttu-id="1642a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1642a-135">RELATED LINKS</span></span>
