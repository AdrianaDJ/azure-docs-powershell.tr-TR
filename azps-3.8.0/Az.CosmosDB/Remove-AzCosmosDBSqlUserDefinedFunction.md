---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104442"
---
# <span data-ttu-id="09cc1-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="09cc1-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="09cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="09cc1-103">CosmosDB SQL Userdefinedişlevini siler.</span><span class="sxs-lookup"><span data-stu-id="09cc1-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="09cc1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09cc1-104">SYNTAX</span></span>

### <span data-ttu-id="09cc1-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09cc1-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09cc1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09cc1-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09cc1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="09cc1-107">DESCRIPTION</span></span>
<span data-ttu-id="09cc1-108">**Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet 'i, verilen Resourcegroupname, AccountName ve DatabaseName 'e karşılık gelen Cosmosdb SQL userdefinedişlevini siler.</span><span class="sxs-lookup"><span data-stu-id="09cc1-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="09cc1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09cc1-109">EXAMPLES</span></span>

### <span data-ttu-id="09cc1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="09cc1-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="09cc1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09cc1-111">PARAMETERS</span></span>

### <span data-ttu-id="09cc1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09cc1-112">-AccountName</span></span>
<span data-ttu-id="09cc1-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="09cc1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09cc1-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="09cc1-114">-Confirm</span></span>
<span data-ttu-id="09cc1-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="09cc1-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09cc1-116">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="09cc1-116">-ContainerName</span></span>
<span data-ttu-id="09cc1-117">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="09cc1-117">Container name.</span></span>

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

### <span data-ttu-id="09cc1-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09cc1-118">-DatabaseName</span></span>
<span data-ttu-id="09cc1-119">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="09cc1-119">Database name.</span></span>

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

### <span data-ttu-id="09cc1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09cc1-120">-DefaultProfile</span></span>
<span data-ttu-id="09cc1-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09cc1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09cc1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09cc1-122">-InputObject</span></span>
<span data-ttu-id="09cc1-123">SQL Kullanıcı tanımlı Işlev nesnesi</span><span class="sxs-lookup"><span data-stu-id="09cc1-123">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09cc1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="09cc1-124">-Name</span></span>
<span data-ttu-id="09cc1-125">Kullanıcı tanımlı Işlev adı.</span><span class="sxs-lookup"><span data-stu-id="09cc1-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="09cc1-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="09cc1-126">-PassThru</span></span>
<span data-ttu-id="09cc1-127">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="09cc1-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="09cc1-128">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="09cc1-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09cc1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09cc1-129">-ResourceGroupName</span></span>
<span data-ttu-id="09cc1-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="09cc1-130">Name of resource group.</span></span>

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

### <span data-ttu-id="09cc1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09cc1-131">-WhatIf</span></span>
<span data-ttu-id="09cc1-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09cc1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09cc1-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="09cc1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09cc1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09cc1-134">CommonParameters</span></span>
<span data-ttu-id="09cc1-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09cc1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09cc1-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="09cc1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09cc1-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09cc1-137">INPUTS</span></span>

### <span data-ttu-id="09cc1-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="09cc1-138">None</span></span>

## <span data-ttu-id="09cc1-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09cc1-139">OUTPUTS</span></span>

### <span data-ttu-id="09cc1-140">System. void</span><span class="sxs-lookup"><span data-stu-id="09cc1-140">System.Void</span></span>

### <span data-ttu-id="09cc1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09cc1-141">System.Boolean</span></span>

## <span data-ttu-id="09cc1-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09cc1-142">NOTES</span></span>

## <span data-ttu-id="09cc1-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09cc1-143">RELATED LINKS</span></span>
