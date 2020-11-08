---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 2914284849fa9a00e3cb2d0b1c96c1efd905e9e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096029"
---
# <span data-ttu-id="b5f87-101">Set-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="b5f87-101">Set-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="b5f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5f87-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f87-103">Yeni bir CosmosDB SQL StoredProcedure oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b5f87-103">Creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="b5f87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5f87-104">SYNTAX</span></span>

### <span data-ttu-id="b5f87-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5f87-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f87-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5f87-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5f87-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5f87-107">DESCRIPTION</span></span>
<span data-ttu-id="b5f87-108">**Set-AzCosmosDBSqlStoredProcedure** cmdlet 'i, yeni bir Cosmosdb SQL StoredProcedure oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b5f87-108">The **Set-AzCosmosDBSqlStoredProcedure** cmdlet creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="b5f87-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5f87-109">EXAMPLES</span></span>

### <span data-ttu-id="b5f87-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5f87-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName} -Body {sampleBody}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
SqlStoredProcedureGetResultsId :
Body                           :
_rid                           :
_ts                            :
_etag                          :
```

## <span data-ttu-id="b5f87-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5f87-111">PARAMETERS</span></span>

### <span data-ttu-id="b5f87-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b5f87-112">-AccountName</span></span>
<span data-ttu-id="b5f87-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="b5f87-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b5f87-114">-Gövde</span><span class="sxs-lookup"><span data-stu-id="b5f87-114">-Body</span></span>
<span data-ttu-id="b5f87-115">Saklı yordamın gövdesi.</span><span class="sxs-lookup"><span data-stu-id="b5f87-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="b5f87-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5f87-116">-Confirm</span></span>
<span data-ttu-id="b5f87-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5f87-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f87-118">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="b5f87-118">-ContainerName</span></span>
<span data-ttu-id="b5f87-119">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="b5f87-119">Container name.</span></span>

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

### <span data-ttu-id="b5f87-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5f87-120">-DatabaseName</span></span>
<span data-ttu-id="b5f87-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="b5f87-121">Database name.</span></span>

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

### <span data-ttu-id="b5f87-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f87-122">-DefaultProfile</span></span>
<span data-ttu-id="b5f87-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5f87-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5f87-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5f87-124">-InputObject</span></span>
<span data-ttu-id="b5f87-125">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b5f87-125">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f87-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5f87-126">-Name</span></span>
<span data-ttu-id="b5f87-127">.</span><span class="sxs-lookup"><span data-stu-id="b5f87-127">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="b5f87-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f87-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5f87-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b5f87-129">Name of resource group.</span></span>

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

### <span data-ttu-id="b5f87-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f87-130">-WhatIf</span></span>
<span data-ttu-id="b5f87-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5f87-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5f87-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5f87-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f87-133">CommonParameters</span></span>
<span data-ttu-id="b5f87-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5f87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f87-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b5f87-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f87-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5f87-136">INPUTS</span></span>

### <span data-ttu-id="b5f87-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b5f87-137">None</span></span>

## <span data-ttu-id="b5f87-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5f87-138">OUTPUTS</span></span>

### <span data-ttu-id="b5f87-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="b5f87-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="b5f87-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5f87-140">NOTES</span></span>

## <span data-ttu-id="b5f87-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5f87-141">RELATED LINKS</span></span>
