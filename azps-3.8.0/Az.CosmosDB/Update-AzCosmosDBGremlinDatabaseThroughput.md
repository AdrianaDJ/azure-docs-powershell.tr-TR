---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 75ea7849424d8587f4eb4151bde63f31ea35676f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938536"
---
# <span data-ttu-id="bb0d3-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="bb0d3-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="bb0d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0d3-103">CosmosDB Gremlın veritabanındaki üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="bb0d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb0d3-104">SYNTAX</span></span>

### <span data-ttu-id="bb0d3-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb0d3-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb0d3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb0d3-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb0d3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb0d3-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb0d3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb0d3-108">EXAMPLES</span></span>

### <span data-ttu-id="bb0d3-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb0d3-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="bb0d3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb0d3-110">PARAMETERS</span></span>

### <span data-ttu-id="bb0d3-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bb0d3-111">-AccountName</span></span>
<span data-ttu-id="bb0d3-112">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bb0d3-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb0d3-113">-Confirm</span></span>
<span data-ttu-id="bb0d3-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb0d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0d3-115">-DefaultProfile</span></span>
<span data-ttu-id="bb0d3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb0d3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb0d3-117">-InputObject</span></span>
<span data-ttu-id="bb0d3-118">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="bb0d3-118">CosmosDB Account object</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0d3-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb0d3-119">-Name</span></span>
<span data-ttu-id="bb0d3-120">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-120">Database name.</span></span>

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

### <span data-ttu-id="bb0d3-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bb0d3-121">-ParentObject</span></span>
<span data-ttu-id="bb0d3-122">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="bb0d3-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="bb0d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb0d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb0d3-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-124">Name of resource group.</span></span>

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

### <span data-ttu-id="bb0d3-125">-Üretim</span><span class="sxs-lookup"><span data-stu-id="bb0d3-125">-Throughput</span></span>
<span data-ttu-id="bb0d3-126">Gremlın veritabanının (RU/s) aktarımı.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="bb0d3-127">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-127">Default value is 400.</span></span>

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

### <span data-ttu-id="bb0d3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb0d3-128">-WhatIf</span></span>
<span data-ttu-id="bb0d3-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb0d3-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb0d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0d3-131">CommonParameters</span></span>
<span data-ttu-id="bb0d3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0d3-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bb0d3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0d3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb0d3-134">INPUTS</span></span>

### <span data-ttu-id="bb0d3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="bb0d3-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="bb0d3-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb0d3-136">OUTPUTS</span></span>

### <span data-ttu-id="bb0d3-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bb0d3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bb0d3-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb0d3-138">NOTES</span></span>

## <span data-ttu-id="bb0d3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb0d3-139">RELATED LINKS</span></span>