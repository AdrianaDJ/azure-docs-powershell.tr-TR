---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274609"
---
# <span data-ttu-id="3781e-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="3781e-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="3781e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3781e-102">SYNOPSIS</span></span>
<span data-ttu-id="3781e-103">CosmosDB Gremlın veritabanındaki üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3781e-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="3781e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3781e-104">SYNTAX</span></span>

### <span data-ttu-id="3781e-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3781e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3781e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3781e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3781e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3781e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3781e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3781e-108">DESCRIPTION</span></span>
<span data-ttu-id="3781e-109">CosmosDB Gremlın veritabanındaki üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3781e-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="3781e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3781e-110">EXAMPLES</span></span>

### <span data-ttu-id="3781e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3781e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="3781e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3781e-112">PARAMETERS</span></span>

### <span data-ttu-id="3781e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3781e-113">-AccountName</span></span>
<span data-ttu-id="3781e-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="3781e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3781e-115">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="3781e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="3781e-116">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="3781e-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="3781e-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="3781e-117">-Confirm</span></span>
<span data-ttu-id="3781e-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3781e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3781e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3781e-119">-DefaultProfile</span></span>
<span data-ttu-id="3781e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3781e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3781e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3781e-121">-InputObject</span></span>
<span data-ttu-id="3781e-122">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="3781e-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3781e-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="3781e-123">-Name</span></span>
<span data-ttu-id="3781e-124">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="3781e-124">Database name.</span></span>

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

### <span data-ttu-id="3781e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3781e-125">-ParentObject</span></span>
<span data-ttu-id="3781e-126">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="3781e-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3781e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3781e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3781e-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3781e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="3781e-129">-Üretim</span><span class="sxs-lookup"><span data-stu-id="3781e-129">-Throughput</span></span>
<span data-ttu-id="3781e-130">Gremlın veritabanının (RU/s) aktarımı.</span><span class="sxs-lookup"><span data-stu-id="3781e-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="3781e-131">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="3781e-131">Default value is 400.</span></span>

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

### <span data-ttu-id="3781e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3781e-132">-WhatIf</span></span>
<span data-ttu-id="3781e-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3781e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3781e-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3781e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3781e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3781e-135">CommonParameters</span></span>
<span data-ttu-id="3781e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3781e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3781e-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3781e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3781e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3781e-138">INPUTS</span></span>

### <span data-ttu-id="3781e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="3781e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="3781e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3781e-140">OUTPUTS</span></span>

### <span data-ttu-id="3781e-141">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3781e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3781e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3781e-142">NOTES</span></span>

## <span data-ttu-id="3781e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3781e-143">RELATED LINKS</span></span>
