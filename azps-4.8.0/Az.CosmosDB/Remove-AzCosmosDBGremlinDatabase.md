---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109734"
---
# <span data-ttu-id="c912c-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="c912c-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="c912c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c912c-102">SYNOPSIS</span></span>
<span data-ttu-id="c912c-103">Bir CosmosDB Gremlın veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="c912c-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="c912c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c912c-104">SYNTAX</span></span>

### <span data-ttu-id="c912c-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c912c-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c912c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c912c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c912c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c912c-107">DESCRIPTION</span></span>
<span data-ttu-id="c912c-108">**Remove-AzCosmosDBGremlinDatabase** cmdlet 'ı Cosmosdb Gremlın veritabanından siler.</span><span class="sxs-lookup"><span data-stu-id="c912c-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="c912c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c912c-109">EXAMPLES</span></span>

### <span data-ttu-id="c912c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c912c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="c912c-111">Cmdlet bool (ne zaman geçiş geçirilir) türünde, silme işlemi başarılıysa doğru olan bir nesneyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c912c-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="c912c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c912c-112">PARAMETERS</span></span>

### <span data-ttu-id="c912c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c912c-113">-AccountName</span></span>
<span data-ttu-id="c912c-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="c912c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c912c-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="c912c-115">-Confirm</span></span>
<span data-ttu-id="c912c-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c912c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c912c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c912c-117">-DefaultProfile</span></span>
<span data-ttu-id="c912c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c912c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c912c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c912c-119">-InputObject</span></span>
<span data-ttu-id="c912c-120">Gremlın veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c912c-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c912c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="c912c-121">-Name</span></span>
<span data-ttu-id="c912c-122">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="c912c-122">Database name.</span></span>

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

### <span data-ttu-id="c912c-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c912c-123">-PassThru</span></span>
<span data-ttu-id="c912c-124">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c912c-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="c912c-125">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="c912c-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="c912c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c912c-126">-ResourceGroupName</span></span>
<span data-ttu-id="c912c-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c912c-127">Name of resource group.</span></span>

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

### <span data-ttu-id="c912c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c912c-128">-WhatIf</span></span>
<span data-ttu-id="c912c-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c912c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c912c-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c912c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c912c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c912c-131">CommonParameters</span></span>
<span data-ttu-id="c912c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c912c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c912c-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c912c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c912c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c912c-134">INPUTS</span></span>

### <span data-ttu-id="c912c-135">Microsoft. Azure. Commands. CosmosDB. modeller. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c912c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="c912c-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c912c-136">OUTPUTS</span></span>

### <span data-ttu-id="c912c-137">System. void</span><span class="sxs-lookup"><span data-stu-id="c912c-137">System.Void</span></span>

### <span data-ttu-id="c912c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c912c-138">System.Boolean</span></span>

## <span data-ttu-id="c912c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c912c-139">NOTES</span></span>

## <span data-ttu-id="c912c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c912c-140">RELATED LINKS</span></span>
