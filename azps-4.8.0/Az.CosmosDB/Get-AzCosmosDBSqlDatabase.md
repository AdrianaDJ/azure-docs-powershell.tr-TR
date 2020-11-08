---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274198"
---
# <span data-ttu-id="9199f-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9199f-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="9199f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9199f-102">SYNOPSIS</span></span>
<span data-ttu-id="9199f-103">CosmosDB SQL veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="9199f-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="9199f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9199f-104">SYNTAX</span></span>

### <span data-ttu-id="9199f-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9199f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9199f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9199f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9199f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9199f-107">DESCRIPTION</span></span>
<span data-ttu-id="9199f-108">**Get-AzCosmosDBSqlDatabase** cmdlet 'i, belirli bir resourcegroupname için tüm mevcut Cosmosdb SQL veritabanlarının listesini alır ve belirli bir Resourcegroupname, AccountName, DatabaseName ve ContainerName için tek bir Cosmosdb SQL veritabanı alır.</span><span class="sxs-lookup"><span data-stu-id="9199f-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="9199f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9199f-109">EXAMPLES</span></span>

### <span data-ttu-id="9199f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9199f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="9199f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9199f-111">PARAMETERS</span></span>

### <span data-ttu-id="9199f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9199f-112">-AccountName</span></span>
<span data-ttu-id="9199f-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="9199f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9199f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9199f-114">-DefaultProfile</span></span>
<span data-ttu-id="9199f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9199f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9199f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="9199f-116">-Name</span></span>
<span data-ttu-id="9199f-117">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="9199f-117">Database name.</span></span>

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

### <span data-ttu-id="9199f-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9199f-118">-ParentObject</span></span>
<span data-ttu-id="9199f-119">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="9199f-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9199f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9199f-120">-ResourceGroupName</span></span>
<span data-ttu-id="9199f-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9199f-121">Name of resource group.</span></span>

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

### <span data-ttu-id="9199f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9199f-122">CommonParameters</span></span>
<span data-ttu-id="9199f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9199f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9199f-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9199f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9199f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9199f-125">INPUTS</span></span>

### <span data-ttu-id="9199f-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9199f-126">None</span></span>

## <span data-ttu-id="9199f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9199f-127">OUTPUTS</span></span>

### <span data-ttu-id="9199f-128">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9199f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="9199f-129">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9199f-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9199f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9199f-130">NOTES</span></span>

## <span data-ttu-id="9199f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9199f-131">RELATED LINKS</span></span>
