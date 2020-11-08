---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104119"
---
# <span data-ttu-id="7fd75-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="7fd75-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="7fd75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fd75-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd75-103">MongoDB koleksiyonunun CosmosDB aktarımı özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="7fd75-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="7fd75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fd75-104">SYNTAX</span></span>

### <span data-ttu-id="7fd75-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7fd75-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd75-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd75-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fd75-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fd75-107">DESCRIPTION</span></span>
<span data-ttu-id="7fd75-108">**Get-Azcosmosdbmongodbcollectionüretiminin** cmdlet 'ı MongoDB koleksiyonunun üretilen iş özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="7fd75-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="7fd75-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fd75-109">EXAMPLES</span></span>

### <span data-ttu-id="7fd75-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7fd75-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="7fd75-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fd75-111">PARAMETERS</span></span>

### <span data-ttu-id="7fd75-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7fd75-112">-AccountName</span></span>
<span data-ttu-id="7fd75-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="7fd75-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7fd75-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="7fd75-114">-Confirm</span></span>
<span data-ttu-id="7fd75-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7fd75-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fd75-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7fd75-116">-DatabaseName</span></span>
<span data-ttu-id="7fd75-117">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="7fd75-117">Database name.</span></span>

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

### <span data-ttu-id="7fd75-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd75-118">-DefaultProfile</span></span>
<span data-ttu-id="7fd75-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fd75-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fd75-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fd75-120">-InputObject</span></span>
<span data-ttu-id="7fd75-121">Sağlanmışsa, cmdlet, ilgili üretilen iş değerini içeren koleksiyonu döndürür.</span><span class="sxs-lookup"><span data-stu-id="7fd75-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd75-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7fd75-122">-Name</span></span>
<span data-ttu-id="7fd75-123">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="7fd75-123">Collection name.</span></span>

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

### <span data-ttu-id="7fd75-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd75-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fd75-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7fd75-125">Name of resource group.</span></span>

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

### <span data-ttu-id="7fd75-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd75-126">-WhatIf</span></span>
<span data-ttu-id="7fd75-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fd75-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fd75-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7fd75-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fd75-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd75-129">CommonParameters</span></span>
<span data-ttu-id="7fd75-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fd75-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd75-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7fd75-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd75-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fd75-132">INPUTS</span></span>

### <span data-ttu-id="7fd75-133">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbcollectiongetresults</span><span class="sxs-lookup"><span data-stu-id="7fd75-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="7fd75-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fd75-134">OUTPUTS</span></span>

### <span data-ttu-id="7fd75-135">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7fd75-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7fd75-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fd75-136">NOTES</span></span>

## <span data-ttu-id="7fd75-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fd75-137">RELATED LINKS</span></span>
