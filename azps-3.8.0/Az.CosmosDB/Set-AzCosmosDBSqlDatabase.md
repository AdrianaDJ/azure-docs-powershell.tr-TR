---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1af202573ff4b783756b8884707922c64ffcf953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096032"
---
# <span data-ttu-id="e3b08-101">Set-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e3b08-101">Set-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="e3b08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3b08-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b08-103">Yeni bir CosmosDB SQL veritabanını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e3b08-103">Creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="e3b08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3b08-104">SYNTAX</span></span>

### <span data-ttu-id="e3b08-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e3b08-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b08-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3b08-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b08-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3b08-107">DESCRIPTION</span></span>
<span data-ttu-id="e3b08-108">**Set-AzCosmosDBSqlDatabase** cmdlet 'i, yeni bir Cosmosdb SQL veritabanını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e3b08-108">The **Set-AzCosmosDBSqlDatabase** cmdlet creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="e3b08-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3b08-109">EXAMPLES</span></span>

### <span data-ttu-id="e3b08-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e3b08-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName}-Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
SqlDatabaseGetResultsId :
_rid                    :
_ts                     :
_etag                   :
_colls                  :
_users                  :
```

## <span data-ttu-id="e3b08-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3b08-111">PARAMETERS</span></span>

### <span data-ttu-id="e3b08-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e3b08-112">-AccountName</span></span>
<span data-ttu-id="e3b08-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="e3b08-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e3b08-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3b08-114">-Confirm</span></span>
<span data-ttu-id="e3b08-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3b08-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b08-116">-DefaultProfile</span></span>
<span data-ttu-id="e3b08-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3b08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b08-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3b08-118">-InputObject</span></span>
<span data-ttu-id="e3b08-119">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="e3b08-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b08-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3b08-120">-Name</span></span>
<span data-ttu-id="e3b08-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="e3b08-121">Database name.</span></span>

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

### <span data-ttu-id="e3b08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b08-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3b08-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e3b08-123">Name of resource group.</span></span>

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

### <span data-ttu-id="e3b08-124">-Üretim</span><span class="sxs-lookup"><span data-stu-id="e3b08-124">-Throughput</span></span>
<span data-ttu-id="e3b08-125">SQL veritabanının üretimi (RU/s).</span><span class="sxs-lookup"><span data-stu-id="e3b08-125">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="e3b08-126">Varsayılan değer 400 ' dır.</span><span class="sxs-lookup"><span data-stu-id="e3b08-126">Default value is 400.</span></span>

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

### <span data-ttu-id="e3b08-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b08-127">-WhatIf</span></span>
<span data-ttu-id="e3b08-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3b08-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b08-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3b08-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b08-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b08-130">CommonParameters</span></span>
<span data-ttu-id="e3b08-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3b08-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b08-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e3b08-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b08-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3b08-133">INPUTS</span></span>

### <span data-ttu-id="e3b08-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e3b08-134">None</span></span>

## <span data-ttu-id="e3b08-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3b08-135">OUTPUTS</span></span>

### <span data-ttu-id="e3b08-136">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e3b08-136">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="e3b08-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3b08-137">NOTES</span></span>

## <span data-ttu-id="e3b08-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3b08-138">RELATED LINKS</span></span>
