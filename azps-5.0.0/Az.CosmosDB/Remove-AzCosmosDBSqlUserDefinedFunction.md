---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321410"
---
# <span data-ttu-id="15879-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="15879-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="15879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15879-102">SYNOPSIS</span></span>
<span data-ttu-id="15879-103">CosmosDB SQL Userdefinedişlevini siler.</span><span class="sxs-lookup"><span data-stu-id="15879-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="15879-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15879-104">SYNTAX</span></span>

### <span data-ttu-id="15879-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="15879-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15879-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15879-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15879-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="15879-107">DESCRIPTION</span></span>
<span data-ttu-id="15879-108">**Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet 'i, verilen Resourcegroupname, AccountName ve DatabaseName 'e karşılık gelen Cosmosdb SQL userdefinedişlevini siler.</span><span class="sxs-lookup"><span data-stu-id="15879-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="15879-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15879-109">EXAMPLES</span></span>

### <span data-ttu-id="15879-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15879-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="15879-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15879-111">PARAMETERS</span></span>

### <span data-ttu-id="15879-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15879-112">-AccountName</span></span>
<span data-ttu-id="15879-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="15879-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="15879-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="15879-114">-Confirm</span></span>
<span data-ttu-id="15879-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15879-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15879-116">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="15879-116">-ContainerName</span></span>
<span data-ttu-id="15879-117">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="15879-117">Container name.</span></span>

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

### <span data-ttu-id="15879-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="15879-118">-DatabaseName</span></span>
<span data-ttu-id="15879-119">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="15879-119">Database name.</span></span>

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

### <span data-ttu-id="15879-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15879-120">-DefaultProfile</span></span>
<span data-ttu-id="15879-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15879-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15879-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15879-122">-InputObject</span></span>
<span data-ttu-id="15879-123">SQL Kullanıcı tanımlı Işlev nesnesi</span><span class="sxs-lookup"><span data-stu-id="15879-123">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="15879-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="15879-124">-Name</span></span>
<span data-ttu-id="15879-125">Kullanıcı tanımlı Işlev adı.</span><span class="sxs-lookup"><span data-stu-id="15879-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="15879-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="15879-126">-PassThru</span></span>
<span data-ttu-id="15879-127">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="15879-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="15879-128">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="15879-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="15879-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15879-129">-ResourceGroupName</span></span>
<span data-ttu-id="15879-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="15879-130">Name of resource group.</span></span>

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

### <span data-ttu-id="15879-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15879-131">-WhatIf</span></span>
<span data-ttu-id="15879-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15879-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15879-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15879-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15879-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15879-134">CommonParameters</span></span>
<span data-ttu-id="15879-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15879-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15879-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15879-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15879-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15879-137">INPUTS</span></span>

### <span data-ttu-id="15879-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="15879-138">None</span></span>

## <span data-ttu-id="15879-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15879-139">OUTPUTS</span></span>

### <span data-ttu-id="15879-140">System. void</span><span class="sxs-lookup"><span data-stu-id="15879-140">System.Void</span></span>

### <span data-ttu-id="15879-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15879-141">System.Boolean</span></span>

## <span data-ttu-id="15879-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15879-142">NOTES</span></span>

## <span data-ttu-id="15879-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15879-143">RELATED LINKS</span></span>
