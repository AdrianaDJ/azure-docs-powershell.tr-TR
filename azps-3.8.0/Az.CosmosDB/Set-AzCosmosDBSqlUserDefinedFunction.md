---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 27363873996505a15e8eccd3dcb3620a2f88c1a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937295"
---
# <span data-ttu-id="721ce-101">Set-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="721ce-101">Set-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="721ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="721ce-102">SYNOPSIS</span></span>
<span data-ttu-id="721ce-103">Yeni bir CosmosDB SQL Userdefinedişlevi oluşturur veya bunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="721ce-103">Creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="721ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="721ce-104">SYNTAX</span></span>

### <span data-ttu-id="721ce-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="721ce-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="721ce-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="721ce-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="721ce-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="721ce-107">DESCRIPTION</span></span>
<span data-ttu-id="721ce-108">**Set-AzCosmosDBSqlUserDefinedFunction** cmdlet 'i yeni oluşturur veya mevcut Cosmosdb SQL userdefinedişlevini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="721ce-108">The **Set-AzCosmosDBSqlUserDefinedFunction** cmdlet creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="721ce-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="721ce-109">EXAMPLES</span></span>

### <span data-ttu-id="721ce-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="721ce-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {udfName} -ContainerName {containerName} -Body {sampleBody}

Name                               : {udfName}
Id                                 : {udfId}
SqlUserDefinedFunctionGetResultsId :
Body                               :
_rid                               :
_ts                                :
_etag                              :
```

## <span data-ttu-id="721ce-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="721ce-111">PARAMETERS</span></span>

### <span data-ttu-id="721ce-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="721ce-112">-AccountName</span></span>
<span data-ttu-id="721ce-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="721ce-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="721ce-114">-Gövde</span><span class="sxs-lookup"><span data-stu-id="721ce-114">-Body</span></span>
<span data-ttu-id="721ce-115">Kullanıcı tanımlı Işlevin gövdesi.</span><span class="sxs-lookup"><span data-stu-id="721ce-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="721ce-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="721ce-116">-Confirm</span></span>
<span data-ttu-id="721ce-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="721ce-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="721ce-118">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="721ce-118">-ContainerName</span></span>
<span data-ttu-id="721ce-119">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="721ce-119">Container name.</span></span>

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

### <span data-ttu-id="721ce-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="721ce-120">-DatabaseName</span></span>
<span data-ttu-id="721ce-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="721ce-121">Database name.</span></span>

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

### <span data-ttu-id="721ce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721ce-122">-DefaultProfile</span></span>
<span data-ttu-id="721ce-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="721ce-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="721ce-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="721ce-124">-InputObject</span></span>
<span data-ttu-id="721ce-125">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="721ce-125">Sql Container object.</span></span>

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

### <span data-ttu-id="721ce-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="721ce-126">-Name</span></span>
<span data-ttu-id="721ce-127">Kullanıcı tanımlı Işlev adı.</span><span class="sxs-lookup"><span data-stu-id="721ce-127">User Defined Function Name.</span></span>

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

### <span data-ttu-id="721ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="721ce-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="721ce-129">Name of resource group.</span></span>

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

### <span data-ttu-id="721ce-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="721ce-130">-WhatIf</span></span>
<span data-ttu-id="721ce-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="721ce-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="721ce-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="721ce-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="721ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721ce-133">CommonParameters</span></span>
<span data-ttu-id="721ce-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="721ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721ce-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="721ce-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721ce-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="721ce-136">INPUTS</span></span>

### <span data-ttu-id="721ce-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="721ce-137">None</span></span>

## <span data-ttu-id="721ce-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="721ce-138">OUTPUTS</span></span>

### <span data-ttu-id="721ce-139">Microsoft. Azure. Commands. CosmosDB. modeller. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="721ce-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="721ce-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="721ce-140">NOTES</span></span>

## <span data-ttu-id="721ce-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="721ce-141">RELATED LINKS</span></span>
