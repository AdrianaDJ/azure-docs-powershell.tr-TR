---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104441"
---
# <span data-ttu-id="26c98-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="26c98-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="26c98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26c98-102">SYNOPSIS</span></span>
<span data-ttu-id="26c98-103">CosmosDB tablosunu siler.</span><span class="sxs-lookup"><span data-stu-id="26c98-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="26c98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26c98-104">SYNTAX</span></span>

### <span data-ttu-id="26c98-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="26c98-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c98-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26c98-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c98-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="26c98-107">DESCRIPTION</span></span>
<span data-ttu-id="26c98-108">**Remove-AzCosmosDBTable** cmdlet 'ı cosmosdb tablosunu siler.</span><span class="sxs-lookup"><span data-stu-id="26c98-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="26c98-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26c98-109">EXAMPLES</span></span>

### <span data-ttu-id="26c98-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="26c98-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="26c98-111">Cmdlet bool (ne zaman geçiş geçirilir) türünde, silme işlemi başarılıysa doğru olan bir nesneyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="26c98-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="26c98-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26c98-112">PARAMETERS</span></span>

### <span data-ttu-id="26c98-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26c98-113">-AccountName</span></span>
<span data-ttu-id="26c98-114">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="26c98-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26c98-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="26c98-115">-Confirm</span></span>
<span data-ttu-id="26c98-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26c98-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26c98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c98-117">-DefaultProfile</span></span>
<span data-ttu-id="26c98-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26c98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26c98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26c98-119">-InputObject</span></span>
<span data-ttu-id="26c98-120">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="26c98-120">Sql Database object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26c98-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="26c98-121">-Name</span></span>
<span data-ttu-id="26c98-122">Tablonun adı.</span><span class="sxs-lookup"><span data-stu-id="26c98-122">Name of the Table.</span></span>

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

### <span data-ttu-id="26c98-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="26c98-123">-PassThru</span></span>
<span data-ttu-id="26c98-124">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="26c98-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="26c98-125">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="26c98-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="26c98-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c98-126">-ResourceGroupName</span></span>
<span data-ttu-id="26c98-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="26c98-127">Name of resource group.</span></span>

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

### <span data-ttu-id="26c98-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26c98-128">-WhatIf</span></span>
<span data-ttu-id="26c98-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26c98-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26c98-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26c98-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26c98-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c98-131">CommonParameters</span></span>
<span data-ttu-id="26c98-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26c98-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c98-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="26c98-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c98-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26c98-134">INPUTS</span></span>

### <span data-ttu-id="26c98-135">Microsoft. Azure. Commands. CosmosDB. modeller. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="26c98-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="26c98-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26c98-136">OUTPUTS</span></span>

### <span data-ttu-id="26c98-137">System. void</span><span class="sxs-lookup"><span data-stu-id="26c98-137">System.Void</span></span>

### <span data-ttu-id="26c98-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26c98-138">System.Boolean</span></span>

## <span data-ttu-id="26c98-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26c98-139">NOTES</span></span>

## <span data-ttu-id="26c98-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26c98-140">RELATED LINKS</span></span>
