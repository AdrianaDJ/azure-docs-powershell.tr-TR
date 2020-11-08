---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103607"
---
# <span data-ttu-id="ef732-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="ef732-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="ef732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef732-102">SYNOPSIS</span></span>
<span data-ttu-id="ef732-103">CosmosDB SQL StoredProcedure öğesini siler.</span><span class="sxs-lookup"><span data-stu-id="ef732-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="ef732-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef732-104">SYNTAX</span></span>

### <span data-ttu-id="ef732-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef732-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef732-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef732-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef732-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef732-107">DESCRIPTION</span></span>
<span data-ttu-id="ef732-108">**Remove-AzCosmosDBSqlStoredProcedure** cmdlet 'i, verilen Resourcegroupname, AccountName ve DatabaseName 'e karşılık gelen Cosmosdb SQL StoredProcedure 'yı siler.</span><span class="sxs-lookup"><span data-stu-id="ef732-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="ef732-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef732-109">EXAMPLES</span></span>

### <span data-ttu-id="ef732-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ef732-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="ef732-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef732-111">PARAMETERS</span></span>

### <span data-ttu-id="ef732-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef732-112">-AccountName</span></span>
<span data-ttu-id="ef732-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="ef732-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ef732-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="ef732-114">-Confirm</span></span>
<span data-ttu-id="ef732-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ef732-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef732-116">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="ef732-116">-ContainerName</span></span>
<span data-ttu-id="ef732-117">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="ef732-117">Container name.</span></span>

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

### <span data-ttu-id="ef732-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef732-118">-DatabaseName</span></span>
<span data-ttu-id="ef732-119">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="ef732-119">Database name.</span></span>

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

### <span data-ttu-id="ef732-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef732-120">-DefaultProfile</span></span>
<span data-ttu-id="ef732-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef732-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef732-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef732-122">-InputObject</span></span>
<span data-ttu-id="ef732-123">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ef732-123">Sql Database object.</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef732-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef732-124">-Name</span></span>
<span data-ttu-id="ef732-125">.</span><span class="sxs-lookup"><span data-stu-id="ef732-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="ef732-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ef732-126">-PassThru</span></span>
<span data-ttu-id="ef732-127">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ef732-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ef732-128">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="ef732-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ef732-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef732-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef732-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ef732-130">Name of resource group.</span></span>

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

### <span data-ttu-id="ef732-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef732-131">-WhatIf</span></span>
<span data-ttu-id="ef732-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef732-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef732-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ef732-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef732-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef732-134">CommonParameters</span></span>
<span data-ttu-id="ef732-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef732-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef732-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ef732-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef732-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef732-137">INPUTS</span></span>

### <span data-ttu-id="ef732-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ef732-138">None</span></span>

## <span data-ttu-id="ef732-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef732-139">OUTPUTS</span></span>

### <span data-ttu-id="ef732-140">System. void</span><span class="sxs-lookup"><span data-stu-id="ef732-140">System.Void</span></span>

### <span data-ttu-id="ef732-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef732-141">System.Boolean</span></span>

## <span data-ttu-id="ef732-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef732-142">NOTES</span></span>

## <span data-ttu-id="ef732-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef732-143">RELATED LINKS</span></span>
