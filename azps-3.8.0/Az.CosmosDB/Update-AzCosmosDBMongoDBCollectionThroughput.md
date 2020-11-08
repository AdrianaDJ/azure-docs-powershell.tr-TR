---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 605998d6bc5ae8b647b3644dc71b8063f0881910
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097662"
---
# <span data-ttu-id="29425-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="29425-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="29425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29425-102">SYNOPSIS</span></span>
<span data-ttu-id="29425-103">CosmosDB MongoDB koleksiyonunun üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="29425-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="29425-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29425-104">SYNTAX</span></span>

### <span data-ttu-id="29425-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="29425-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29425-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29425-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29425-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29425-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29425-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29425-108">EXAMPLES</span></span>

### <span data-ttu-id="29425-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="29425-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="29425-110">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="29425-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="29425-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29425-111">PARAMETERS</span></span>

### <span data-ttu-id="29425-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="29425-112">-AccountName</span></span>
<span data-ttu-id="29425-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="29425-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="29425-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="29425-114">-Confirm</span></span>
<span data-ttu-id="29425-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29425-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29425-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29425-116">-DatabaseName</span></span>
<span data-ttu-id="29425-117">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="29425-117">Database name.</span></span>

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

### <span data-ttu-id="29425-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29425-118">-DefaultProfile</span></span>
<span data-ttu-id="29425-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29425-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29425-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29425-120">-InputObject</span></span>
<span data-ttu-id="29425-121">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="29425-121">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29425-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="29425-122">-Name</span></span>
<span data-ttu-id="29425-123">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="29425-123">Collection name.</span></span>

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

### <span data-ttu-id="29425-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="29425-124">-ParentObject</span></span>
<span data-ttu-id="29425-125">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="29425-125">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29425-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29425-126">-ResourceGroupName</span></span>
<span data-ttu-id="29425-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="29425-127">Name of resource group.</span></span>

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

### <span data-ttu-id="29425-128">-Üretim</span><span class="sxs-lookup"><span data-stu-id="29425-128">-Throughput</span></span>
<span data-ttu-id="29425-129">SQL kapsayıcısının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="29425-129">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="29425-130">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="29425-130">Default value is 400.</span></span>

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

### <span data-ttu-id="29425-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29425-131">-WhatIf</span></span>
<span data-ttu-id="29425-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29425-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29425-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29425-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29425-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29425-134">CommonParameters</span></span>
<span data-ttu-id="29425-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29425-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29425-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="29425-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29425-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29425-137">INPUTS</span></span>

### <span data-ttu-id="29425-138">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="29425-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="29425-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29425-139">OUTPUTS</span></span>

### <span data-ttu-id="29425-140">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="29425-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="29425-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29425-141">NOTES</span></span>

## <span data-ttu-id="29425-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29425-142">RELATED LINKS</span></span>
