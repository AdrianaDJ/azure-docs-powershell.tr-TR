---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321437"
---
# <span data-ttu-id="c0d55-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="c0d55-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="c0d55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0d55-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d55-103">CosmosDB MongoDB koleksiyonunu siler.</span><span class="sxs-lookup"><span data-stu-id="c0d55-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="c0d55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0d55-104">SYNTAX</span></span>

### <span data-ttu-id="c0d55-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0d55-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0d55-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0d55-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d55-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0d55-107">DESCRIPTION</span></span>
<span data-ttu-id="c0d55-108">**Remove-AzCosmosDBMongoDBCollection** cmdlet 'ı Cosmosdb MongoDB koleksiyonunu siler.</span><span class="sxs-lookup"><span data-stu-id="c0d55-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="c0d55-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0d55-109">EXAMPLES</span></span>

### <span data-ttu-id="c0d55-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0d55-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="c0d55-111">Cmdlet bool (ne zaman geçiş geçirilir) türünde, silme işlemi başarılıysa doğru olan bir nesneyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c0d55-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="c0d55-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0d55-112">PARAMETERS</span></span>

### <span data-ttu-id="c0d55-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c0d55-113">-AccountName</span></span>
<span data-ttu-id="c0d55-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="c0d55-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c0d55-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0d55-115">-Confirm</span></span>
<span data-ttu-id="c0d55-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0d55-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0d55-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c0d55-117">-DatabaseName</span></span>
<span data-ttu-id="c0d55-118">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="c0d55-118">Database name.</span></span>

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

### <span data-ttu-id="c0d55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d55-119">-DefaultProfile</span></span>
<span data-ttu-id="c0d55-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0d55-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d55-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0d55-121">-InputObject</span></span>
<span data-ttu-id="c0d55-122">SQL kapsayıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c0d55-122">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d55-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0d55-123">-Name</span></span>
<span data-ttu-id="c0d55-124">Koleksiyon adı.</span><span class="sxs-lookup"><span data-stu-id="c0d55-124">Collection name.</span></span>

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

### <span data-ttu-id="c0d55-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c0d55-125">-PassThru</span></span>
<span data-ttu-id="c0d55-126">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c0d55-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="c0d55-127">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="c0d55-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="c0d55-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d55-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0d55-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c0d55-129">Name of resource group.</span></span>

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

### <span data-ttu-id="c0d55-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d55-130">-WhatIf</span></span>
<span data-ttu-id="c0d55-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0d55-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0d55-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0d55-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0d55-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d55-133">CommonParameters</span></span>
<span data-ttu-id="c0d55-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0d55-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d55-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c0d55-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d55-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0d55-136">INPUTS</span></span>

### <span data-ttu-id="c0d55-137">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbcollectiongetresults</span><span class="sxs-lookup"><span data-stu-id="c0d55-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="c0d55-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0d55-138">OUTPUTS</span></span>

### <span data-ttu-id="c0d55-139">System. void</span><span class="sxs-lookup"><span data-stu-id="c0d55-139">System.Void</span></span>

### <span data-ttu-id="c0d55-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0d55-140">System.Boolean</span></span>

## <span data-ttu-id="c0d55-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0d55-141">NOTES</span></span>

## <span data-ttu-id="c0d55-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0d55-142">RELATED LINKS</span></span>
