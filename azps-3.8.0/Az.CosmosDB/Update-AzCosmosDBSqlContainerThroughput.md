---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: e38e10765bc9a9768efaf1598a1865ec985b376c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097663"
---
# <span data-ttu-id="4f3de-101">Update-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="4f3de-101">Update-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="4f3de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f3de-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3de-103">CosmosDB SQL kapsayıcısının üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4f3de-103">Updates the throughput value of a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="4f3de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f3de-104">SYNTAX</span></span>

### <span data-ttu-id="4f3de-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f3de-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f3de-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3de-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f3de-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f3de-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainerThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f3de-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f3de-108">EXAMPLES</span></span>

### <span data-ttu-id="4f3de-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4f3de-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlContainerThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {myDatabaseName} -Name {myContainerName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/conatiners/{myContainerName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="4f3de-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f3de-110">PARAMETERS</span></span>

### <span data-ttu-id="4f3de-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4f3de-111">-AccountName</span></span>
<span data-ttu-id="4f3de-112">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="4f3de-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4f3de-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f3de-113">-Confirm</span></span>
<span data-ttu-id="4f3de-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f3de-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f3de-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4f3de-115">-DatabaseName</span></span>
<span data-ttu-id="4f3de-116">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="4f3de-116">Database name.</span></span>

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

### <span data-ttu-id="4f3de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f3de-117">-DefaultProfile</span></span>
<span data-ttu-id="4f3de-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f3de-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f3de-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f3de-119">-InputObject</span></span>
<span data-ttu-id="4f3de-120">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4f3de-120">Sql Database object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3de-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f3de-121">-Name</span></span>
<span data-ttu-id="4f3de-122">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="4f3de-122">Container name.</span></span>

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

### <span data-ttu-id="4f3de-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4f3de-123">-ParentObject</span></span>
<span data-ttu-id="4f3de-124">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4f3de-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f3de-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f3de-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4f3de-126">Name of resource group.</span></span>

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

### <span data-ttu-id="4f3de-127">-Üretim</span><span class="sxs-lookup"><span data-stu-id="4f3de-127">-Throughput</span></span>
<span data-ttu-id="4f3de-128">SQL kapsayıcısının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="4f3de-128">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="4f3de-129">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="4f3de-129">Default value is 400.</span></span>

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

### <span data-ttu-id="4f3de-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f3de-130">-WhatIf</span></span>
<span data-ttu-id="4f3de-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f3de-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f3de-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f3de-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f3de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3de-133">CommonParameters</span></span>
<span data-ttu-id="4f3de-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f3de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3de-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4f3de-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3de-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f3de-136">INPUTS</span></span>

### <span data-ttu-id="4f3de-137">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4f3de-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="4f3de-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f3de-138">OUTPUTS</span></span>

### <span data-ttu-id="4f3de-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4f3de-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4f3de-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f3de-140">NOTES</span></span>

## <span data-ttu-id="4f3de-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f3de-141">RELATED LINKS</span></span>
