---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321394"
---
# <span data-ttu-id="82c4c-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="82c4c-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="82c4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="82c4c-103">CosmosDB Cassandra anahtar uzayını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="82c4c-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="82c4c-104">Mevcut tuş uzayını okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="82c4c-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="82c4c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82c4c-105">SYNTAX</span></span>

### <span data-ttu-id="82c4c-106">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="82c4c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82c4c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82c4c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82c4c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82c4c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82c4c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="82c4c-109">DESCRIPTION</span></span>
<span data-ttu-id="82c4c-110">CosmosDB Cassandra anahtar uzayını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="82c4c-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="82c4c-111">Mevcut tuş uzayını okuyarak bir istemci tarafı düzeltme eki işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="82c4c-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="82c4c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82c4c-112">EXAMPLES</span></span>

### <span data-ttu-id="82c4c-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="82c4c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="82c4c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82c4c-114">PARAMETERS</span></span>

### <span data-ttu-id="82c4c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82c4c-115">-AccountName</span></span>
<span data-ttu-id="82c4c-116">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="82c4c-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="82c4c-117">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="82c4c-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="82c4c-118">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="82c4c-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="82c4c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="82c4c-119">-Confirm</span></span>
<span data-ttu-id="82c4c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="82c4c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82c4c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c4c-121">-DefaultProfile</span></span>
<span data-ttu-id="82c4c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82c4c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c4c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82c4c-123">-InputObject</span></span>
<span data-ttu-id="82c4c-124">Cassandra keyspace nesnesi.</span><span class="sxs-lookup"><span data-stu-id="82c4c-124">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82c4c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="82c4c-125">-Name</span></span>
<span data-ttu-id="82c4c-126">Cassandra tuş alanı adı.</span><span class="sxs-lookup"><span data-stu-id="82c4c-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="82c4c-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="82c4c-127">-ParentObject</span></span>
<span data-ttu-id="82c4c-128">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="82c4c-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="82c4c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c4c-129">-ResourceGroupName</span></span>
<span data-ttu-id="82c4c-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="82c4c-130">Name of resource group.</span></span>

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

### <span data-ttu-id="82c4c-131">-Üretim</span><span class="sxs-lookup"><span data-stu-id="82c4c-131">-Throughput</span></span>
<span data-ttu-id="82c4c-132">Cassandra keyspace 'in üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="82c4c-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="82c4c-133">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="82c4c-133">Default value is 400.</span></span>

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

### <span data-ttu-id="82c4c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c4c-134">-WhatIf</span></span>
<span data-ttu-id="82c4c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82c4c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82c4c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="82c4c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82c4c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c4c-137">CommonParameters</span></span>
<span data-ttu-id="82c4c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82c4c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c4c-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="82c4c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c4c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82c4c-140">INPUTS</span></span>

### <span data-ttu-id="82c4c-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="82c4c-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="82c4c-142">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="82c4c-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="82c4c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82c4c-143">OUTPUTS</span></span>

### <span data-ttu-id="82c4c-144">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="82c4c-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="82c4c-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="82c4c-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="82c4c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82c4c-146">NOTES</span></span>

## <span data-ttu-id="82c4c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82c4c-147">RELATED LINKS</span></span>
