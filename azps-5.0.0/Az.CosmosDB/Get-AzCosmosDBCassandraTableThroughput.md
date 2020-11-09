---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321714"
---
# <span data-ttu-id="40e3f-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="40e3f-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="40e3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="40e3f-103">Cassandra tablosunun üretilen iş değerini alır.</span><span class="sxs-lookup"><span data-stu-id="40e3f-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="40e3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40e3f-104">SYNTAX</span></span>

### <span data-ttu-id="40e3f-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="40e3f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40e3f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40e3f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e3f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="40e3f-107">DESCRIPTION</span></span>
<span data-ttu-id="40e3f-108">**Get-Azcosmosdbcassandratableüretiminin** cmdlet 'i, verilen bir keyspace 'e karşılık gelen üretilen iş nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="40e3f-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="40e3f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40e3f-109">EXAMPLES</span></span>

### <span data-ttu-id="40e3f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="40e3f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="40e3f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40e3f-111">PARAMETERS</span></span>

### <span data-ttu-id="40e3f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="40e3f-112">-AccountName</span></span>
<span data-ttu-id="40e3f-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="40e3f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="40e3f-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="40e3f-114">-Confirm</span></span>
<span data-ttu-id="40e3f-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40e3f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e3f-116">-DefaultProfile</span></span>
<span data-ttu-id="40e3f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40e3f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40e3f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40e3f-118">-InputObject</span></span>
<span data-ttu-id="40e3f-119">Cassandra tablo nesnesi.</span><span class="sxs-lookup"><span data-stu-id="40e3f-119">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40e3f-120">-Anahtararalığı</span><span class="sxs-lookup"><span data-stu-id="40e3f-120">-KeyspaceName</span></span>
<span data-ttu-id="40e3f-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="40e3f-121">Database name.</span></span>

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

### <span data-ttu-id="40e3f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="40e3f-122">-Name</span></span>
<span data-ttu-id="40e3f-123">Cassandra tablo adı.</span><span class="sxs-lookup"><span data-stu-id="40e3f-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="40e3f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e3f-124">-ResourceGroupName</span></span>
<span data-ttu-id="40e3f-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="40e3f-125">Name of resource group.</span></span>

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

### <span data-ttu-id="40e3f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e3f-126">-WhatIf</span></span>
<span data-ttu-id="40e3f-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40e3f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e3f-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40e3f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e3f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e3f-129">CommonParameters</span></span>
<span data-ttu-id="40e3f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40e3f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e3f-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="40e3f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e3f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40e3f-132">INPUTS</span></span>

### <span data-ttu-id="40e3f-133">Microsoft. Azure. Commands. CosmosDB. modeller. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="40e3f-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="40e3f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40e3f-134">OUTPUTS</span></span>

### <span data-ttu-id="40e3f-135">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="40e3f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="40e3f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40e3f-136">NOTES</span></span>

## <span data-ttu-id="40e3f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40e3f-137">RELATED LINKS</span></span>
