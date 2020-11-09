---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: ed97687a03a40df8bbc965a21d7beb268cb67432
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321354"
---
# <span data-ttu-id="ced11-101">Update-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="ced11-101">Update-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="ced11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ced11-102">SYNOPSIS</span></span>
<span data-ttu-id="ced11-103">CosmosDB MongoDB veritabanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ced11-103">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="ced11-104">Var olan veritabanını okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="ced11-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="ced11-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ced11-105">SYNTAX</span></span>

### <span data-ttu-id="ced11-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ced11-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced11-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced11-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ced11-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced11-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ced11-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ced11-109">DESCRIPTION</span></span>
<span data-ttu-id="ced11-110">CosmosDB MongoDB veritabanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ced11-110">Updates the CosmosDB MongoDB Database.</span></span> <span data-ttu-id="ced11-111">Var olan veritabanını okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="ced11-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="ced11-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ced11-112">EXAMPLES</span></span>

### <span data-ttu-id="ced11-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ced11-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 600

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="ced11-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ced11-114">PARAMETERS</span></span>

### <span data-ttu-id="ced11-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ced11-115">-AccountName</span></span>
<span data-ttu-id="ced11-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="ced11-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ced11-117">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="ced11-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ced11-118">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="ced11-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ced11-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ced11-119">-Confirm</span></span>
<span data-ttu-id="ced11-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ced11-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced11-121">-DefaultProfile</span></span>
<span data-ttu-id="ced11-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ced11-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced11-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ced11-123">-InputObject</span></span>
<span data-ttu-id="ced11-124">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ced11-124">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ced11-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ced11-125">-Name</span></span>
<span data-ttu-id="ced11-126">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="ced11-126">Database name.</span></span>

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

### <span data-ttu-id="ced11-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ced11-127">-ParentObject</span></span>
<span data-ttu-id="ced11-128">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="ced11-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ced11-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced11-129">-ResourceGroupName</span></span>
<span data-ttu-id="ced11-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ced11-130">Name of resource group.</span></span>

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

### <span data-ttu-id="ced11-131">-Üretim</span><span class="sxs-lookup"><span data-stu-id="ced11-131">-Throughput</span></span>
<span data-ttu-id="ced11-132">Monto veritabanının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="ced11-132">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="ced11-133">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="ced11-133">Default value is 400.</span></span>

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

### <span data-ttu-id="ced11-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced11-134">-WhatIf</span></span>
<span data-ttu-id="ced11-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ced11-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced11-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ced11-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced11-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced11-137">CommonParameters</span></span>
<span data-ttu-id="ced11-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ced11-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced11-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ced11-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced11-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ced11-140">INPUTS</span></span>

### <span data-ttu-id="ced11-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ced11-141">None</span></span>

## <span data-ttu-id="ced11-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ced11-142">OUTPUTS</span></span>

### <span data-ttu-id="ced11-143">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="ced11-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="ced11-144">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ced11-144">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="ced11-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ced11-145">NOTES</span></span>

## <span data-ttu-id="ced11-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ced11-146">RELATED LINKS</span></span>
