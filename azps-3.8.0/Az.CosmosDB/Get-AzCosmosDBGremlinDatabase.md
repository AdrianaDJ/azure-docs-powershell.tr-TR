---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104125"
---
# <span data-ttu-id="e2871-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="e2871-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="e2871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2871-102">SYNOPSIS</span></span>
<span data-ttu-id="e2871-103">CosmosDB Gremlın veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="e2871-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e2871-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2871-104">SYNTAX</span></span>

### <span data-ttu-id="e2871-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2871-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2871-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2871-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2871-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2871-107">DESCRIPTION</span></span>
<span data-ttu-id="e2871-108">**Get-AzCosmosDBGremlinDatabase** cmdlet 'ı Cosmosdb Gremlın veritabanından alır.</span><span class="sxs-lookup"><span data-stu-id="e2871-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="e2871-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2871-109">EXAMPLES</span></span>

### <span data-ttu-id="e2871-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2871-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="e2871-111">Kaynak nesnesi _rid, _ts _etag içerir.</span><span class="sxs-lookup"><span data-stu-id="e2871-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="e2871-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2871-112">PARAMETERS</span></span>

### <span data-ttu-id="e2871-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e2871-113">-AccountName</span></span>
<span data-ttu-id="e2871-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="e2871-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e2871-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2871-115">-DefaultProfile</span></span>
<span data-ttu-id="e2871-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2871-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2871-117">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="e2871-117">-Detailed</span></span>
<span data-ttu-id="e2871-118">Sağlanmışsa, cmdlet, ilgili üretilen iş değerini içeren veritabanını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e2871-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="e2871-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2871-119">-InputObject</span></span>
<span data-ttu-id="e2871-120">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="e2871-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2871-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2871-121">-Name</span></span>
<span data-ttu-id="e2871-122">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="e2871-122">Database name.</span></span>

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

### <span data-ttu-id="e2871-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2871-123">-ResourceGroupName</span></span>
<span data-ttu-id="e2871-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e2871-124">Name of resource group.</span></span>

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

### <span data-ttu-id="e2871-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2871-125">CommonParameters</span></span>
<span data-ttu-id="e2871-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2871-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2871-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2871-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2871-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2871-128">INPUTS</span></span>

### <span data-ttu-id="e2871-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e2871-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e2871-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2871-130">OUTPUTS</span></span>

### <span data-ttu-id="e2871-131">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e2871-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="e2871-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e2871-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e2871-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2871-133">NOTES</span></span>

## <span data-ttu-id="e2871-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2871-134">RELATED LINKS</span></span>
