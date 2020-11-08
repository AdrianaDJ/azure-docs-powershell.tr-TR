---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097661"
---
# <span data-ttu-id="faeb2-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="faeb2-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="faeb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faeb2-102">SYNOPSIS</span></span>
<span data-ttu-id="faeb2-103">CosmosDB Gremlın grafiğinin üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="faeb2-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="faeb2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="faeb2-104">SYNTAX</span></span>

### <span data-ttu-id="faeb2-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="faeb2-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faeb2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="faeb2-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faeb2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="faeb2-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="faeb2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="faeb2-108">EXAMPLES</span></span>

### <span data-ttu-id="faeb2-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="faeb2-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="faeb2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="faeb2-110">PARAMETERS</span></span>

### <span data-ttu-id="faeb2-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="faeb2-111">-AccountName</span></span>
<span data-ttu-id="faeb2-112">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="faeb2-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="faeb2-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="faeb2-113">-Confirm</span></span>
<span data-ttu-id="faeb2-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="faeb2-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faeb2-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="faeb2-115">-DatabaseName</span></span>
<span data-ttu-id="faeb2-116">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="faeb2-116">Database name.</span></span>

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

### <span data-ttu-id="faeb2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faeb2-117">-DefaultProfile</span></span>
<span data-ttu-id="faeb2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="faeb2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faeb2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faeb2-119">-InputObject</span></span>
<span data-ttu-id="faeb2-120">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="faeb2-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faeb2-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="faeb2-121">-Name</span></span>
<span data-ttu-id="faeb2-122">Gremlın grafik adı.</span><span class="sxs-lookup"><span data-stu-id="faeb2-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="faeb2-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="faeb2-123">-ParentObject</span></span>
<span data-ttu-id="faeb2-124">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="faeb2-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faeb2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faeb2-125">-ResourceGroupName</span></span>
<span data-ttu-id="faeb2-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="faeb2-126">Name of resource group.</span></span>

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

### <span data-ttu-id="faeb2-127">-Üretim</span><span class="sxs-lookup"><span data-stu-id="faeb2-127">-Throughput</span></span>
<span data-ttu-id="faeb2-128">Gremlın grafiğinin (RU/s) miktarı.</span><span class="sxs-lookup"><span data-stu-id="faeb2-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="faeb2-129">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="faeb2-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faeb2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faeb2-130">-WhatIf</span></span>
<span data-ttu-id="faeb2-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="faeb2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faeb2-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="faeb2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faeb2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faeb2-133">CommonParameters</span></span>
<span data-ttu-id="faeb2-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="faeb2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faeb2-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="faeb2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faeb2-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="faeb2-136">INPUTS</span></span>

### <span data-ttu-id="faeb2-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="faeb2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="faeb2-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="faeb2-138">OUTPUTS</span></span>

### <span data-ttu-id="faeb2-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="faeb2-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="faeb2-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="faeb2-140">NOTES</span></span>

## <span data-ttu-id="faeb2-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="faeb2-141">RELATED LINKS</span></span>
