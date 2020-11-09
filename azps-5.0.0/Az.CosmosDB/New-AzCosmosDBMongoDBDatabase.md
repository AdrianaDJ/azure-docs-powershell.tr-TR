---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: d4724976d5b4c702999fdd64c0811aa975c258d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321526"
---
# <span data-ttu-id="bf6bb-101">New-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="bf6bb-101">New-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="bf6bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="bf6bb-103">Yeni bir CosmosDB MongoDB veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-103">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="bf6bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf6bb-104">SYNTAX</span></span>

### <span data-ttu-id="bf6bb-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf6bb-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf6bb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf6bb-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf6bb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf6bb-107">DESCRIPTION</span></span>
<span data-ttu-id="bf6bb-108">Yeni bir CosmosDB MongoDB veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-108">Creates a new CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="bf6bb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf6bb-109">EXAMPLES</span></span>

### <span data-ttu-id="bf6bb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bf6bb-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="bf6bb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf6bb-111">PARAMETERS</span></span>

### <span data-ttu-id="bf6bb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bf6bb-112">-AccountName</span></span>
<span data-ttu-id="bf6bb-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bf6bb-114">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="bf6bb-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="bf6bb-115">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="bf6bb-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf6bb-116">-Confirm</span></span>
<span data-ttu-id="bf6bb-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf6bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf6bb-118">-DefaultProfile</span></span>
<span data-ttu-id="bf6bb-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf6bb-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf6bb-120">-Name</span></span>
<span data-ttu-id="bf6bb-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-121">Database name.</span></span>

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

### <span data-ttu-id="bf6bb-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bf6bb-122">-ParentObject</span></span>
<span data-ttu-id="bf6bb-123">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="bf6bb-123">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf6bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf6bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf6bb-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-125">Name of resource group.</span></span>

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

### <span data-ttu-id="bf6bb-126">-Üretim</span><span class="sxs-lookup"><span data-stu-id="bf6bb-126">-Throughput</span></span>
<span data-ttu-id="bf6bb-127">Monto veritabanının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="bf6bb-127">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="bf6bb-128">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-128">Default value is 400.</span></span>

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

### <span data-ttu-id="bf6bb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf6bb-129">-WhatIf</span></span>
<span data-ttu-id="bf6bb-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf6bb-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf6bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf6bb-132">CommonParameters</span></span>
<span data-ttu-id="bf6bb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf6bb-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf6bb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf6bb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf6bb-135">INPUTS</span></span>

### <span data-ttu-id="bf6bb-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bf6bb-136">None</span></span>

## <span data-ttu-id="bf6bb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf6bb-137">OUTPUTS</span></span>

### <span data-ttu-id="bf6bb-138">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="bf6bb-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="bf6bb-139">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="bf6bb-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="bf6bb-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf6bb-140">NOTES</span></span>

## <span data-ttu-id="bf6bb-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf6bb-141">RELATED LINKS</span></span>
