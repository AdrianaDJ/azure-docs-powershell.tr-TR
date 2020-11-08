---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103618"
---
# <span data-ttu-id="5f21d-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="5f21d-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="5f21d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f21d-102">SYNOPSIS</span></span>
<span data-ttu-id="5f21d-103">CosmosDB SQL kapsayıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="5f21d-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="5f21d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f21d-104">SYNTAX</span></span>

### <span data-ttu-id="5f21d-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f21d-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f21d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f21d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f21d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f21d-107">DESCRIPTION</span></span>
<span data-ttu-id="5f21d-108">**Remove-AzCosmosDBSqlContainer** cmdlet 'i, verilen Resourcegroupname, AccountName, DatabaseName ve kapsayıcılarla Ilgili Cosmosdb SQL kapsayıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="5f21d-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="5f21d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f21d-109">EXAMPLES</span></span>

### <span data-ttu-id="5f21d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5f21d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="5f21d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f21d-111">PARAMETERS</span></span>

### <span data-ttu-id="5f21d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5f21d-112">-AccountName</span></span>
<span data-ttu-id="5f21d-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="5f21d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5f21d-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f21d-114">-Confirm</span></span>
<span data-ttu-id="5f21d-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f21d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f21d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5f21d-116">-DatabaseName</span></span>
<span data-ttu-id="5f21d-117">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="5f21d-117">Database name.</span></span>

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

### <span data-ttu-id="5f21d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f21d-118">-DefaultProfile</span></span>
<span data-ttu-id="5f21d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f21d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f21d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f21d-120">-InputObject</span></span>
<span data-ttu-id="5f21d-121">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5f21d-121">Sql Container object.</span></span>

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

### <span data-ttu-id="5f21d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f21d-122">-Name</span></span>
<span data-ttu-id="5f21d-123">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="5f21d-123">Container name.</span></span>

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

### <span data-ttu-id="5f21d-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5f21d-124">-PassThru</span></span>
<span data-ttu-id="5f21d-125">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5f21d-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="5f21d-126">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="5f21d-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="5f21d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f21d-127">-ResourceGroupName</span></span>
<span data-ttu-id="5f21d-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5f21d-128">Name of resource group.</span></span>

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

### <span data-ttu-id="5f21d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f21d-129">-WhatIf</span></span>
<span data-ttu-id="5f21d-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f21d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f21d-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f21d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f21d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f21d-132">CommonParameters</span></span>
<span data-ttu-id="5f21d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f21d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f21d-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f21d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f21d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f21d-135">INPUTS</span></span>

### <span data-ttu-id="5f21d-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5f21d-136">None</span></span>

## <span data-ttu-id="5f21d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f21d-137">OUTPUTS</span></span>

### <span data-ttu-id="5f21d-138">System. void</span><span class="sxs-lookup"><span data-stu-id="5f21d-138">System.Void</span></span>

### <span data-ttu-id="5f21d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5f21d-139">System.Boolean</span></span>

## <span data-ttu-id="5f21d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f21d-140">NOTES</span></span>

## <span data-ttu-id="5f21d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f21d-141">RELATED LINKS</span></span>
