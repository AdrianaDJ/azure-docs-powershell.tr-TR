---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268032"
---
# <span data-ttu-id="b294b-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="b294b-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="b294b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b294b-102">SYNOPSIS</span></span>
<span data-ttu-id="b294b-103">CosmosDB Gremlın veritabanında güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b294b-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="b294b-104">Var olan veritabanını okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="b294b-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="b294b-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b294b-105">SYNTAX</span></span>

### <span data-ttu-id="b294b-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b294b-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b294b-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b294b-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b294b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b294b-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b294b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b294b-109">DESCRIPTION</span></span>
<span data-ttu-id="b294b-110">CosmosDB Gremlın veritabanında güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b294b-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="b294b-111">Var olan veritabanını okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="b294b-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="b294b-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b294b-112">EXAMPLES</span></span>

### <span data-ttu-id="b294b-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b294b-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="b294b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b294b-114">PARAMETERS</span></span>

### <span data-ttu-id="b294b-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b294b-115">-AccountName</span></span>
<span data-ttu-id="b294b-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="b294b-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b294b-117">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="b294b-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b294b-118">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="b294b-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b294b-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="b294b-119">-Confirm</span></span>
<span data-ttu-id="b294b-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b294b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b294b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b294b-121">-DefaultProfile</span></span>
<span data-ttu-id="b294b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b294b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b294b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b294b-123">-InputObject</span></span>
<span data-ttu-id="b294b-124">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b294b-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="b294b-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b294b-125">-Name</span></span>
<span data-ttu-id="b294b-126">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="b294b-126">Database name.</span></span>

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

### <span data-ttu-id="b294b-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b294b-127">-ParentObject</span></span>
<span data-ttu-id="b294b-128">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="b294b-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b294b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b294b-129">-ResourceGroupName</span></span>
<span data-ttu-id="b294b-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b294b-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b294b-131">-Üretim</span><span class="sxs-lookup"><span data-stu-id="b294b-131">-Throughput</span></span>
<span data-ttu-id="b294b-132">Gremlın veritabanının (RU/s) aktarımı.</span><span class="sxs-lookup"><span data-stu-id="b294b-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="b294b-133">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b294b-133">Default value is 400.</span></span>

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

### <span data-ttu-id="b294b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b294b-134">-WhatIf</span></span>
<span data-ttu-id="b294b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b294b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b294b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b294b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b294b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b294b-137">CommonParameters</span></span>
<span data-ttu-id="b294b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b294b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b294b-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b294b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b294b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b294b-140">INPUTS</span></span>

### <span data-ttu-id="b294b-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b294b-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="b294b-142">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b294b-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b294b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b294b-143">OUTPUTS</span></span>

### <span data-ttu-id="b294b-144">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b294b-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="b294b-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="b294b-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="b294b-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b294b-146">NOTES</span></span>

## <span data-ttu-id="b294b-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b294b-147">RELATED LINKS</span></span>
