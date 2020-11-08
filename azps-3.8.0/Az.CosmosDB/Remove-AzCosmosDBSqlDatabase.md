---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103614"
---
# <span data-ttu-id="a0e99-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0e99-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="a0e99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0e99-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e99-103">CosmosDB SQL veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="a0e99-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="a0e99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0e99-104">SYNTAX</span></span>

### <span data-ttu-id="a0e99-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0e99-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0e99-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0e99-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0e99-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0e99-107">DESCRIPTION</span></span>
<span data-ttu-id="a0e99-108">**Remove-AzCosmosDBSqlDatabase** cmdlet 'i, verilen Resourcegroupname, AccountName ve DatabaseName 'e karşılık gelen Cosmosdb SQL veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="a0e99-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="a0e99-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0e99-109">EXAMPLES</span></span>

### <span data-ttu-id="a0e99-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0e99-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="a0e99-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0e99-111">PARAMETERS</span></span>

### <span data-ttu-id="a0e99-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a0e99-112">-AccountName</span></span>
<span data-ttu-id="a0e99-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="a0e99-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a0e99-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0e99-114">-Confirm</span></span>
<span data-ttu-id="a0e99-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0e99-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0e99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e99-116">-DefaultProfile</span></span>
<span data-ttu-id="a0e99-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0e99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0e99-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0e99-118">-InputObject</span></span>
<span data-ttu-id="a0e99-119">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a0e99-119">Sql Database object.</span></span>

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

### <span data-ttu-id="a0e99-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0e99-120">-Name</span></span>
<span data-ttu-id="a0e99-121">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="a0e99-121">Database name.</span></span>

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

### <span data-ttu-id="a0e99-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a0e99-122">-PassThru</span></span>
<span data-ttu-id="a0e99-123">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a0e99-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="a0e99-124">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="a0e99-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="a0e99-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e99-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0e99-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a0e99-126">Name of resource group.</span></span>

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

### <span data-ttu-id="a0e99-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e99-127">-WhatIf</span></span>
<span data-ttu-id="a0e99-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0e99-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0e99-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0e99-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0e99-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e99-130">CommonParameters</span></span>
<span data-ttu-id="a0e99-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0e99-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e99-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0e99-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e99-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0e99-133">INPUTS</span></span>

### <span data-ttu-id="a0e99-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a0e99-134">None</span></span>

## <span data-ttu-id="a0e99-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0e99-135">OUTPUTS</span></span>

### <span data-ttu-id="a0e99-136">System. void</span><span class="sxs-lookup"><span data-stu-id="a0e99-136">System.Void</span></span>

### <span data-ttu-id="a0e99-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0e99-137">System.Boolean</span></span>

## <span data-ttu-id="a0e99-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0e99-138">NOTES</span></span>

## <span data-ttu-id="a0e99-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0e99-139">RELATED LINKS</span></span>
