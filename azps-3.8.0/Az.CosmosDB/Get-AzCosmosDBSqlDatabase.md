---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 5efdbc3f1f8172ba59a78d4ec462f57a527faf07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938391"
---
# <span data-ttu-id="ed7f4-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed7f4-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="ed7f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7f4-103">CosmosDB SQL veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="ed7f4-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="ed7f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed7f4-104">SYNTAX</span></span>

### <span data-ttu-id="ed7f4-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed7f4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed7f4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed7f4-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed7f4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed7f4-107">DESCRIPTION</span></span>
<span data-ttu-id="ed7f4-108">**Get-AzCosmosDBSqlDatabase** cmdlet 'i, belirli bir resourcegroupname için tüm mevcut Cosmosdb SQL veritabanlarının listesini alır ve belirli bir Resourcegroupname, AccountName, DatabaseName ve ContainerName için tek bir Cosmosdb SQL veritabanı alır.</span><span class="sxs-lookup"><span data-stu-id="ed7f4-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="ed7f4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed7f4-109">EXAMPLES</span></span>

### <span data-ttu-id="ed7f4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed7f4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="ed7f4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed7f4-111">PARAMETERS</span></span>

### <span data-ttu-id="ed7f4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed7f4-112">-AccountName</span></span>
<span data-ttu-id="ed7f4-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="ed7f4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ed7f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7f4-114">-DefaultProfile</span></span>
<span data-ttu-id="ed7f4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed7f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed7f4-116">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="ed7f4-116">-Detailed</span></span>
<span data-ttu-id="ed7f4-117">Sağlanmışsa, cmdlet, üretilen iş değerini içeren kapsayıcıyı döndürür.</span><span class="sxs-lookup"><span data-stu-id="ed7f4-117">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="ed7f4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed7f4-118">-InputObject</span></span>
<span data-ttu-id="ed7f4-119">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="ed7f4-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed7f4-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed7f4-120">-Name</span></span>
<span data-ttu-id="ed7f4-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="ed7f4-121">Database name.</span></span>

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

### <span data-ttu-id="ed7f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed7f4-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ed7f4-123">Name of resource group.</span></span>

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

### <span data-ttu-id="ed7f4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7f4-124">CommonParameters</span></span>
<span data-ttu-id="ed7f4-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed7f4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7f4-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed7f4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7f4-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed7f4-127">INPUTS</span></span>

### <span data-ttu-id="ed7f4-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ed7f4-128">None</span></span>

## <span data-ttu-id="ed7f4-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed7f4-129">OUTPUTS</span></span>

### <span data-ttu-id="ed7f4-130">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ed7f4-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="ed7f4-131">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ed7f4-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ed7f4-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed7f4-132">NOTES</span></span>

## <span data-ttu-id="ed7f4-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed7f4-133">RELATED LINKS</span></span>
