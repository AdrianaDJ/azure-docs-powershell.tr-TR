---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321697"
---
# <span data-ttu-id="edb88-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="edb88-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="edb88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb88-102">SYNOPSIS</span></span>
<span data-ttu-id="edb88-103">CosmosDB Gremlın grafiğinin verimini alır.</span><span class="sxs-lookup"><span data-stu-id="edb88-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="edb88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edb88-104">SYNTAX</span></span>

### <span data-ttu-id="edb88-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="edb88-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edb88-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edb88-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb88-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="edb88-107">DESCRIPTION</span></span>
<span data-ttu-id="edb88-108">**Get-Azcosmosdbgremlingraphüretimi** cmdlet 'ı Cosmosdb Gremlın grafiğinin verimini alır.</span><span class="sxs-lookup"><span data-stu-id="edb88-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="edb88-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edb88-109">EXAMPLES</span></span>

### <span data-ttu-id="edb88-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="edb88-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="edb88-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edb88-111">PARAMETERS</span></span>

### <span data-ttu-id="edb88-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="edb88-112">-AccountName</span></span>
<span data-ttu-id="edb88-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="edb88-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="edb88-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="edb88-114">-Confirm</span></span>
<span data-ttu-id="edb88-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edb88-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb88-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="edb88-116">-DatabaseName</span></span>
<span data-ttu-id="edb88-117">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="edb88-117">Database name.</span></span>

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

### <span data-ttu-id="edb88-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb88-118">-DefaultProfile</span></span>
<span data-ttu-id="edb88-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edb88-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edb88-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edb88-120">-InputObject</span></span>
<span data-ttu-id="edb88-121">Gremlın grafik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="edb88-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edb88-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="edb88-122">-Name</span></span>
<span data-ttu-id="edb88-123">Gremlın grafik adı.</span><span class="sxs-lookup"><span data-stu-id="edb88-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="edb88-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb88-124">-ResourceGroupName</span></span>
<span data-ttu-id="edb88-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="edb88-125">Name of resource group.</span></span>

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

### <span data-ttu-id="edb88-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb88-126">-WhatIf</span></span>
<span data-ttu-id="edb88-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edb88-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edb88-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edb88-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb88-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb88-129">CommonParameters</span></span>
<span data-ttu-id="edb88-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edb88-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb88-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="edb88-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb88-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edb88-132">INPUTS</span></span>

### <span data-ttu-id="edb88-133">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="edb88-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="edb88-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edb88-134">OUTPUTS</span></span>

### <span data-ttu-id="edb88-135">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="edb88-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="edb88-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edb88-136">NOTES</span></span>

## <span data-ttu-id="edb88-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edb88-137">RELATED LINKS</span></span>
