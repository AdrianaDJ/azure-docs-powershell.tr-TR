---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 8aca11c8ce56c42842e96fa1e3623979612ffec7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268335"
---
# <span data-ttu-id="5c95a-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="5c95a-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="5c95a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c95a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c95a-103">CosmosDB SQL tetikleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="5c95a-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="5c95a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c95a-104">SYNTAX</span></span>

### <span data-ttu-id="5c95a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c95a-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c95a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c95a-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c95a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c95a-107">DESCRIPTION</span></span>
<span data-ttu-id="5c95a-108">**Remove-AzCosmosDBSqlTrigger** cmdlet 'i, verilen Resourcegroupname, AccountName ve DatabaseName 'e karşılık gelen Cosmosdb SQL tetikleyicisini siler.</span><span class="sxs-lookup"><span data-stu-id="5c95a-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="5c95a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c95a-109">EXAMPLES</span></span>

### <span data-ttu-id="5c95a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5c95a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="5c95a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c95a-111">PARAMETERS</span></span>

### <span data-ttu-id="5c95a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5c95a-112">-AccountName</span></span>
<span data-ttu-id="5c95a-113">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="5c95a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5c95a-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c95a-114">-Confirm</span></span>
<span data-ttu-id="5c95a-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c95a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c95a-116">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="5c95a-116">-ContainerName</span></span>
<span data-ttu-id="5c95a-117">Kapsayıcı adı.</span><span class="sxs-lookup"><span data-stu-id="5c95a-117">Container name.</span></span>

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

### <span data-ttu-id="5c95a-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5c95a-118">-DatabaseName</span></span>
<span data-ttu-id="5c95a-119">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="5c95a-119">Database name.</span></span>

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

### <span data-ttu-id="5c95a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c95a-120">-DefaultProfile</span></span>
<span data-ttu-id="5c95a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c95a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c95a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c95a-122">-InputObject</span></span>
<span data-ttu-id="5c95a-123">SQL tetik nesnesi</span><span class="sxs-lookup"><span data-stu-id="5c95a-123">Sql trigger Object</span></span>

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

### <span data-ttu-id="5c95a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c95a-124">-Name</span></span>
<span data-ttu-id="5c95a-125">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="5c95a-125">Trigger name.</span></span>

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

### <span data-ttu-id="5c95a-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5c95a-126">-PassThru</span></span>
<span data-ttu-id="5c95a-127">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c95a-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="5c95a-128">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="5c95a-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="5c95a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c95a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5c95a-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5c95a-130">Name of resource group.</span></span>

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

### <span data-ttu-id="5c95a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c95a-131">-WhatIf</span></span>
<span data-ttu-id="5c95a-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c95a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c95a-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c95a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c95a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c95a-134">CommonParameters</span></span>
<span data-ttu-id="5c95a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c95a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c95a-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5c95a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c95a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c95a-137">INPUTS</span></span>

### <span data-ttu-id="5c95a-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5c95a-138">None</span></span>

## <span data-ttu-id="5c95a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c95a-139">OUTPUTS</span></span>

### <span data-ttu-id="5c95a-140">System. void</span><span class="sxs-lookup"><span data-stu-id="5c95a-140">System.Void</span></span>

### <span data-ttu-id="5c95a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c95a-141">System.Boolean</span></span>

## <span data-ttu-id="5c95a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c95a-142">NOTES</span></span>

## <span data-ttu-id="5c95a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c95a-143">RELATED LINKS</span></span>
