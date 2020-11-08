---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: f1cb4a45a68758dc1209b4e30d352def8e348e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104106"
---
# <span data-ttu-id="76e1d-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="76e1d-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="76e1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="76e1d-103">CosmosDB MongoDB veritabanını alır</span><span class="sxs-lookup"><span data-stu-id="76e1d-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="76e1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76e1d-104">SYNTAX</span></span>

### <span data-ttu-id="76e1d-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76e1d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76e1d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76e1d-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76e1d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76e1d-107">DESCRIPTION</span></span>
<span data-ttu-id="76e1d-108">**Get-AzCosmosDBMongoDBDatabase** cmdlet 'ı Cosmosdb MongoDB veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="76e1d-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="76e1d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76e1d-109">EXAMPLES</span></span>

### <span data-ttu-id="76e1d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76e1d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="76e1d-111">Kaynak nesnesi _rid, _ts _etag özelliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="76e1d-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="76e1d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76e1d-112">PARAMETERS</span></span>

### <span data-ttu-id="76e1d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="76e1d-113">-AccountName</span></span>
<span data-ttu-id="76e1d-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="76e1d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="76e1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e1d-115">-DefaultProfile</span></span>
<span data-ttu-id="76e1d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76e1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76e1d-117">-Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="76e1d-117">-Detailed</span></span>
<span data-ttu-id="76e1d-118">Sağlanmışsa, cmdlet, ilgili üretilen iş değerini içeren veritabanını döndürür.</span><span class="sxs-lookup"><span data-stu-id="76e1d-118">If provided then, the cmdlet returns the database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="76e1d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76e1d-119">-InputObject</span></span>
<span data-ttu-id="76e1d-120">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="76e1d-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="76e1d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="76e1d-121">-Name</span></span>
<span data-ttu-id="76e1d-122">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="76e1d-122">Database name.</span></span>

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

### <span data-ttu-id="76e1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76e1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="76e1d-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="76e1d-124">Name of resource group.</span></span>

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

### <span data-ttu-id="76e1d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e1d-125">CommonParameters</span></span>
<span data-ttu-id="76e1d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76e1d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e1d-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76e1d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e1d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76e1d-128">INPUTS</span></span>

### <span data-ttu-id="76e1d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="76e1d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="76e1d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76e1d-130">OUTPUTS</span></span>

### <span data-ttu-id="76e1d-131">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="76e1d-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="76e1d-132">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="76e1d-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="76e1d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76e1d-133">NOTES</span></span>

## <span data-ttu-id="76e1d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76e1d-134">RELATED LINKS</span></span>
