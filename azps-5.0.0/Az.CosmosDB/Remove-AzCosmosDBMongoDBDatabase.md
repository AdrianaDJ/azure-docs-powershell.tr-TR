---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321434"
---
# <span data-ttu-id="ba323-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="ba323-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="ba323-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba323-102">SYNOPSIS</span></span>
<span data-ttu-id="ba323-103">CosmosDB MongoDB veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="ba323-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="ba323-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba323-104">SYNTAX</span></span>

### <span data-ttu-id="ba323-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba323-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba323-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba323-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba323-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba323-107">DESCRIPTION</span></span>
<span data-ttu-id="ba323-108">**Remove-AzCosmosDBMongoDBDatabase** cmdlet 'ı Cosmosdb MongoDB veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="ba323-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="ba323-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba323-109">EXAMPLES</span></span>

### <span data-ttu-id="ba323-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba323-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="ba323-111">Cmdlet bool (ne zaman geçiş geçirilir) türünde, silme işlemi başarılıysa doğru olan bir nesneyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba323-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="ba323-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba323-112">PARAMETERS</span></span>

### <span data-ttu-id="ba323-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ba323-113">-AccountName</span></span>
<span data-ttu-id="ba323-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="ba323-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ba323-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba323-115">-Confirm</span></span>
<span data-ttu-id="ba323-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba323-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba323-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba323-117">-DefaultProfile</span></span>
<span data-ttu-id="ba323-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba323-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba323-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba323-119">-InputObject</span></span>
<span data-ttu-id="ba323-120">Mongit veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ba323-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba323-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba323-121">-Name</span></span>
<span data-ttu-id="ba323-122">Veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="ba323-122">Database name.</span></span>

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

### <span data-ttu-id="ba323-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ba323-123">-PassThru</span></span>
<span data-ttu-id="ba323-124">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ba323-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ba323-125">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="ba323-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ba323-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba323-126">-ResourceGroupName</span></span>
<span data-ttu-id="ba323-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba323-127">Name of resource group.</span></span>

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

### <span data-ttu-id="ba323-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba323-128">-WhatIf</span></span>
<span data-ttu-id="ba323-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba323-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba323-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba323-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba323-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba323-131">CommonParameters</span></span>
<span data-ttu-id="ba323-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba323-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba323-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba323-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba323-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba323-134">INPUTS</span></span>

### <span data-ttu-id="ba323-135">Microsoft. Azure. Commands. CosmosDB. modeller. Psmengodbdatabasegetresults</span><span class="sxs-lookup"><span data-stu-id="ba323-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="ba323-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba323-136">OUTPUTS</span></span>

### <span data-ttu-id="ba323-137">System. void</span><span class="sxs-lookup"><span data-stu-id="ba323-137">System.Void</span></span>

### <span data-ttu-id="ba323-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba323-138">System.Boolean</span></span>

## <span data-ttu-id="ba323-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba323-139">NOTES</span></span>

## <span data-ttu-id="ba323-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba323-140">RELATED LINKS</span></span>
