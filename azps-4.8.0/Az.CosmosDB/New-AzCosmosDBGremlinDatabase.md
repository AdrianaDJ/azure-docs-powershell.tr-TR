---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267856"
---
# <span data-ttu-id="24606-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="24606-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="24606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24606-102">SYNOPSIS</span></span>
<span data-ttu-id="24606-103">Yeni bir CosmosDB Gremlda veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24606-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="24606-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24606-104">SYNTAX</span></span>

### <span data-ttu-id="24606-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="24606-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24606-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24606-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24606-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="24606-107">DESCRIPTION</span></span>
<span data-ttu-id="24606-108">Yeni bir CosmosDB Gremlda veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24606-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="24606-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24606-109">EXAMPLES</span></span>

### <span data-ttu-id="24606-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="24606-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="24606-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24606-111">PARAMETERS</span></span>

### <span data-ttu-id="24606-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24606-112">-AccountName</span></span>
<span data-ttu-id="24606-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="24606-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="24606-114">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="24606-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="24606-115">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="24606-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="24606-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="24606-116">-Confirm</span></span>
<span data-ttu-id="24606-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24606-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24606-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24606-118">-DefaultProfile</span></span>
<span data-ttu-id="24606-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24606-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24606-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="24606-120">-Name</span></span>
<span data-ttu-id="24606-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="24606-121">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24606-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="24606-122">-ParentObject</span></span>
<span data-ttu-id="24606-123">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="24606-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="24606-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24606-124">-ResourceGroupName</span></span>
<span data-ttu-id="24606-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="24606-125">Name of resource group.</span></span>

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

### <span data-ttu-id="24606-126">-Üretim</span><span class="sxs-lookup"><span data-stu-id="24606-126">-Throughput</span></span>
<span data-ttu-id="24606-127">Gremlın veritabanının (RU/s) aktarımı.</span><span class="sxs-lookup"><span data-stu-id="24606-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="24606-128">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="24606-128">Default value is 400.</span></span>

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

### <span data-ttu-id="24606-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24606-129">-WhatIf</span></span>
<span data-ttu-id="24606-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24606-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24606-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24606-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24606-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24606-132">CommonParameters</span></span>
<span data-ttu-id="24606-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24606-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24606-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="24606-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24606-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24606-135">INPUTS</span></span>

### <span data-ttu-id="24606-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="24606-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="24606-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24606-137">OUTPUTS</span></span>

### <span data-ttu-id="24606-138">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="24606-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="24606-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="24606-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="24606-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24606-140">NOTES</span></span>

## <span data-ttu-id="24606-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24606-141">RELATED LINKS</span></span>
