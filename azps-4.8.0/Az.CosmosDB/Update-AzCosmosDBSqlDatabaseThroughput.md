---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 324350329b166ab3a41f7e2bd8b59af1b9efdcb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274607"
---
# <span data-ttu-id="46b89-101">Update-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="46b89-101">Update-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="46b89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46b89-102">SYNOPSIS</span></span>
<span data-ttu-id="46b89-103">CosmosDB SQL veritabanının üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="46b89-103">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="46b89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46b89-104">SYNTAX</span></span>

### <span data-ttu-id="46b89-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="46b89-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b89-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46b89-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b89-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46b89-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabaseThroughput [-Name <String>] -InputObject <PSSqlDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46b89-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="46b89-108">DESCRIPTION</span></span>
<span data-ttu-id="46b89-109">CosmosDB SQL veritabanının üretilen iş değerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="46b89-109">Updates the throughput value of a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="46b89-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46b89-110">EXAMPLES</span></span>

### <span data-ttu-id="46b89-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="46b89-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/sqlDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="46b89-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46b89-112">PARAMETERS</span></span>

### <span data-ttu-id="46b89-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="46b89-113">-AccountName</span></span>
<span data-ttu-id="46b89-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="46b89-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="46b89-115">-Otomatik ölçek Maxüretilen Iş</span><span class="sxs-lookup"><span data-stu-id="46b89-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="46b89-116">Otomatik ölçeklendirme etkinleştirilirse maksimum üretilen Iş değeri.</span><span class="sxs-lookup"><span data-stu-id="46b89-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="46b89-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="46b89-117">-Confirm</span></span>
<span data-ttu-id="46b89-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46b89-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46b89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b89-119">-DefaultProfile</span></span>
<span data-ttu-id="46b89-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46b89-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b89-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46b89-121">-InputObject</span></span>
<span data-ttu-id="46b89-122">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="46b89-122">CosmosDB Account object</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46b89-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="46b89-123">-Name</span></span>
<span data-ttu-id="46b89-124">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="46b89-124">Database name.</span></span>

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

### <span data-ttu-id="46b89-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="46b89-125">-ParentObject</span></span>
<span data-ttu-id="46b89-126">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="46b89-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="46b89-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b89-127">-ResourceGroupName</span></span>
<span data-ttu-id="46b89-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="46b89-128">Name of resource group.</span></span>

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

### <span data-ttu-id="46b89-129">-Üretim</span><span class="sxs-lookup"><span data-stu-id="46b89-129">-Throughput</span></span>
<span data-ttu-id="46b89-130">SQL veritabanının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="46b89-130">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="46b89-131">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="46b89-131">Default value is 400.</span></span>

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

### <span data-ttu-id="46b89-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b89-132">-WhatIf</span></span>
<span data-ttu-id="46b89-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46b89-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46b89-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46b89-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46b89-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b89-135">CommonParameters</span></span>
<span data-ttu-id="46b89-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46b89-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b89-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46b89-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b89-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46b89-138">INPUTS</span></span>

### <span data-ttu-id="46b89-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="46b89-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="46b89-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46b89-140">OUTPUTS</span></span>

### <span data-ttu-id="46b89-141">Microsoft. Azure. Commands. CosmosDB. modeller. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="46b89-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="46b89-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46b89-142">NOTES</span></span>

## <span data-ttu-id="46b89-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46b89-143">RELATED LINKS</span></span>
