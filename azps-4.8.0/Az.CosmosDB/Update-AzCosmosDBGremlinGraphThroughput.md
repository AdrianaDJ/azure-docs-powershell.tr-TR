---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275076"
---
# <span data-ttu-id="5e1ab-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="5e1ab-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="5e1ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1ab-103">CosmosDB Gremlın grafiğinin üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5e1ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e1ab-104">SYNTAX</span></span>

### <span data-ttu-id="5e1ab-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e1ab-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1ab-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e1ab-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e1ab-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e1ab-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e1ab-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e1ab-108">DESCRIPTION</span></span>
<span data-ttu-id="5e1ab-109">CosmosDB Gremlın grafiğinin üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="5e1ab-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e1ab-110">EXAMPLES</span></span>

### <span data-ttu-id="5e1ab-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e1ab-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="5e1ab-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e1ab-112">PARAMETERS</span></span>

### <span data-ttu-id="5e1ab-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e1ab-113">-AccountName</span></span>
<span data-ttu-id="5e1ab-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5e1ab-115">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="5e1ab-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5e1ab-116">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-116">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1ab-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e1ab-117">-Confirm</span></span>
<span data-ttu-id="5e1ab-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e1ab-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e1ab-119">-DatabaseName</span></span>
<span data-ttu-id="5e1ab-120">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-120">Database name.</span></span>

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

### <span data-ttu-id="5e1ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1ab-121">-DefaultProfile</span></span>
<span data-ttu-id="5e1ab-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e1ab-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e1ab-123">-InputObject</span></span>
<span data-ttu-id="5e1ab-124">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5e1ab-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e1ab-125">-Name</span></span>
<span data-ttu-id="5e1ab-126">Gremlın grafik adı.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="5e1ab-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e1ab-127">-ParentObject</span></span>
<span data-ttu-id="5e1ab-128">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5e1ab-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e1ab-129">-ResourceGroupName</span></span>
<span data-ttu-id="5e1ab-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-130">Name of resource group.</span></span>

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

### <span data-ttu-id="5e1ab-131">-Üretim</span><span class="sxs-lookup"><span data-stu-id="5e1ab-131">-Throughput</span></span>
<span data-ttu-id="5e1ab-132">Gremlın grafiğinin (RU/s) miktarı.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="5e1ab-133">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e1ab-134">-WhatIf</span></span>
<span data-ttu-id="5e1ab-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e1ab-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e1ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1ab-137">CommonParameters</span></span>
<span data-ttu-id="5e1ab-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1ab-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1ab-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e1ab-140">INPUTS</span></span>

### <span data-ttu-id="5e1ab-141">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5e1ab-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="5e1ab-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e1ab-142">OUTPUTS</span></span>

### <span data-ttu-id="5e1ab-143">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5e1ab-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5e1ab-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e1ab-144">NOTES</span></span>

## <span data-ttu-id="5e1ab-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e1ab-145">RELATED LINKS</span></span>
