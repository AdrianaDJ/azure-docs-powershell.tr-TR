---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321705"
---
# <span data-ttu-id="cb3ca-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="cb3ca-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="cb3ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3ca-103">CosmosDB Gremlın veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="cb3ca-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="cb3ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb3ca-104">SYNTAX</span></span>

### <span data-ttu-id="cb3ca-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb3ca-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb3ca-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb3ca-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb3ca-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb3ca-107">DESCRIPTION</span></span>
<span data-ttu-id="cb3ca-108">**Get-AzCosmosDBGremlinDatabase** cmdlet 'ı Cosmosdb Gremlın veritabanından alır.</span><span class="sxs-lookup"><span data-stu-id="cb3ca-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="cb3ca-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb3ca-109">EXAMPLES</span></span>

### <span data-ttu-id="cb3ca-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb3ca-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="cb3ca-111">Kaynak nesnesi _rid, _ts _etag içerir.</span><span class="sxs-lookup"><span data-stu-id="cb3ca-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="cb3ca-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb3ca-112">PARAMETERS</span></span>

### <span data-ttu-id="cb3ca-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb3ca-113">-AccountName</span></span>
<span data-ttu-id="cb3ca-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="cb3ca-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cb3ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3ca-115">-DefaultProfile</span></span>
<span data-ttu-id="cb3ca-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb3ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3ca-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb3ca-117">-Name</span></span>
<span data-ttu-id="cb3ca-118">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="cb3ca-118">Database name.</span></span>

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

### <span data-ttu-id="cb3ca-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cb3ca-119">-ParentObject</span></span>
<span data-ttu-id="cb3ca-120">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="cb3ca-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="cb3ca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb3ca-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb3ca-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cb3ca-122">Name of resource group.</span></span>

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

### <span data-ttu-id="cb3ca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3ca-123">CommonParameters</span></span>
<span data-ttu-id="cb3ca-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb3ca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3ca-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cb3ca-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3ca-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb3ca-126">INPUTS</span></span>

### <span data-ttu-id="cb3ca-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="cb3ca-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="cb3ca-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb3ca-128">OUTPUTS</span></span>

### <span data-ttu-id="cb3ca-129">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="cb3ca-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="cb3ca-130">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cb3ca-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cb3ca-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb3ca-131">NOTES</span></span>

## <span data-ttu-id="cb3ca-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb3ca-132">RELATED LINKS</span></span>
