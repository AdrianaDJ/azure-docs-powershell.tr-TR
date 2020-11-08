---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 8aca11c8ce56c42842e96fa1e3623979612ffec7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103606"
---
# <span data-ttu-id="dc185-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="dc185-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="dc185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc185-102">SYNOPSIS</span></span>
<span data-ttu-id="dc185-103">CosmosDB SQL tetikleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="dc185-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="dc185-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc185-104">SYNTAX</span></span>

### <span data-ttu-id="dc185-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc185-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc185-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc185-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc185-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc185-107">DESCRIPTION</span></span>
<span data-ttu-id="dc185-108">**Remove-AzCosmosDBSqlTrigger** cmdlet 'i, verilen Resourcegroupname, AccountName ve DatabaseName 'e karşılık gelen Cosmosdb SQL tetikleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="dc185-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="dc185-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc185-109">EXAMPLES</span></span>

### <span data-ttu-id="dc185-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dc185-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="dc185-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc185-111">PARAMETERS</span></span>

### <span data-ttu-id="dc185-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc185-112">-AccountName</span></span>
<span data-ttu-id="dc185-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="dc185-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dc185-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc185-114">-Confirm</span></span>
<span data-ttu-id="dc185-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc185-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc185-116">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="dc185-116">-ContainerName</span></span>
<span data-ttu-id="dc185-117">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="dc185-117">Container name.</span></span>

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

### <span data-ttu-id="dc185-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc185-118">-DatabaseName</span></span>
<span data-ttu-id="dc185-119">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="dc185-119">Database name.</span></span>

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

### <span data-ttu-id="dc185-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc185-120">-DefaultProfile</span></span>
<span data-ttu-id="dc185-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc185-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc185-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc185-122">-InputObject</span></span>
<span data-ttu-id="dc185-123">SQL tetik nesnesi</span><span class="sxs-lookup"><span data-stu-id="dc185-123">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc185-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc185-124">-Name</span></span>
<span data-ttu-id="dc185-125">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="dc185-125">Trigger name.</span></span>

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

### <span data-ttu-id="dc185-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dc185-126">-PassThru</span></span>
<span data-ttu-id="dc185-127">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dc185-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="dc185-128">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="dc185-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="dc185-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc185-129">-ResourceGroupName</span></span>
<span data-ttu-id="dc185-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dc185-130">Name of resource group.</span></span>

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

### <span data-ttu-id="dc185-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc185-131">-WhatIf</span></span>
<span data-ttu-id="dc185-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc185-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc185-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc185-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc185-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc185-134">CommonParameters</span></span>
<span data-ttu-id="dc185-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc185-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc185-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dc185-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc185-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc185-137">INPUTS</span></span>

### <span data-ttu-id="dc185-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dc185-138">None</span></span>

## <span data-ttu-id="dc185-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc185-139">OUTPUTS</span></span>

### <span data-ttu-id="dc185-140">System. void</span><span class="sxs-lookup"><span data-stu-id="dc185-140">System.Void</span></span>

### <span data-ttu-id="dc185-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc185-141">System.Boolean</span></span>

## <span data-ttu-id="dc185-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc185-142">NOTES</span></span>

## <span data-ttu-id="dc185-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc185-143">RELATED LINKS</span></span>
