---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321358"
---
# <span data-ttu-id="0c942-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="0c942-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="0c942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c942-102">SYNOPSIS</span></span>
<span data-ttu-id="0c942-103">CosmosDB MongoDB koleksiyonunun üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0c942-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="0c942-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c942-104">SYNTAX</span></span>

### <span data-ttu-id="0c942-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c942-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c942-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c942-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c942-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c942-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c942-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c942-108">DESCRIPTION</span></span>
<span data-ttu-id="0c942-109">CosmosDB MongoDB koleksiyonunun üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0c942-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="0c942-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c942-110">EXAMPLES</span></span>

### <span data-ttu-id="0c942-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c942-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="0c942-112">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="0c942-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="0c942-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c942-113">PARAMETERS</span></span>

### <span data-ttu-id="0c942-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c942-114">-AccountName</span></span>
<span data-ttu-id="0c942-115">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="0c942-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0c942-116">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="0c942-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0c942-117">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="0c942-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0c942-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c942-118">-Confirm</span></span>
<span data-ttu-id="0c942-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c942-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c942-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c942-120">-DatabaseName</span></span>
<span data-ttu-id="0c942-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="0c942-121">Database name.</span></span>

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

### <span data-ttu-id="0c942-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c942-122">-DefaultProfile</span></span>
<span data-ttu-id="0c942-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c942-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c942-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c942-124">-InputObject</span></span>
<span data-ttu-id="0c942-125">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0c942-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="0c942-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c942-126">-Name</span></span>
<span data-ttu-id="0c942-127">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="0c942-127">Collection name.</span></span>

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

### <span data-ttu-id="0c942-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0c942-128">-ParentObject</span></span>
<span data-ttu-id="0c942-129">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0c942-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="0c942-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c942-130">-ResourceGroupName</span></span>
<span data-ttu-id="0c942-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0c942-131">Name of resource group.</span></span>

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

### <span data-ttu-id="0c942-132">-Üretim</span><span class="sxs-lookup"><span data-stu-id="0c942-132">-Throughput</span></span>
<span data-ttu-id="0c942-133">SQL kapsayıcısının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="0c942-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="0c942-134">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="0c942-134">Default value is 400.</span></span>

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

### <span data-ttu-id="0c942-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c942-135">-WhatIf</span></span>
<span data-ttu-id="0c942-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c942-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c942-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c942-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c942-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c942-138">CommonParameters</span></span>
<span data-ttu-id="0c942-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c942-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c942-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0c942-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c942-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c942-141">INPUTS</span></span>

### <span data-ttu-id="0c942-142">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="0c942-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="0c942-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c942-143">OUTPUTS</span></span>

### <span data-ttu-id="0c942-144">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0c942-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0c942-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c942-145">NOTES</span></span>

## <span data-ttu-id="0c942-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c942-146">RELATED LINKS</span></span>
