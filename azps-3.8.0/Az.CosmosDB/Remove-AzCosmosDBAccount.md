---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: e9ec1f1626a1fb4335c6e5df43a96727692538c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103715"
---
# <span data-ttu-id="e7cfa-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e7cfa-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e7cfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="e7cfa-103">CosmosDB hesabını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="e7cfa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7cfa-104">SYNTAX</span></span>

### <span data-ttu-id="e7cfa-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7cfa-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7cfa-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e7cfa-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7cfa-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7cfa-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7cfa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7cfa-108">DESCRIPTION</span></span>
<span data-ttu-id="e7cfa-109">Verilen ResourceGroup 'daki belirli bir ada sahip bir CosmosDB hesabını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="e7cfa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7cfa-110">EXAMPLES</span></span>

### <span data-ttu-id="e7cfa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7cfa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="e7cfa-112">ResourceGroup RG hesap adı</span><span class="sxs-lookup"><span data-stu-id="e7cfa-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="e7cfa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7cfa-113">PARAMETERS</span></span>

### <span data-ttu-id="e7cfa-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="e7cfa-114">-AsJob</span></span>
<span data-ttu-id="e7cfa-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e7cfa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7cfa-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7cfa-116">-Confirm</span></span>
<span data-ttu-id="e7cfa-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7cfa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7cfa-118">-DefaultProfile</span></span>
<span data-ttu-id="e7cfa-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7cfa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7cfa-120">-InputObject</span></span>
<span data-ttu-id="e7cfa-121">Veritabanı hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="e7cfa-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7cfa-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7cfa-122">-Name</span></span>
<span data-ttu-id="e7cfa-123">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e7cfa-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e7cfa-124">-PassThru</span></span>
<span data-ttu-id="e7cfa-125">Kullanıcı çıktı almak isterse true olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e7cfa-126">İşlem başarılı olduysa ve değilse hata atılır.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="e7cfa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7cfa-127">-ResourceGroupName</span></span>
<span data-ttu-id="e7cfa-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e7cfa-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e7cfa-129">-ResourceId</span></span>
<span data-ttu-id="e7cfa-130">Kaynağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7cfa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7cfa-131">-WhatIf</span></span>
<span data-ttu-id="e7cfa-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7cfa-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7cfa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7cfa-134">CommonParameters</span></span>
<span data-ttu-id="e7cfa-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7cfa-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e7cfa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7cfa-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7cfa-137">INPUTS</span></span>

### <span data-ttu-id="e7cfa-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e7cfa-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e7cfa-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7cfa-139">OUTPUTS</span></span>

### <span data-ttu-id="e7cfa-140">System. void</span><span class="sxs-lookup"><span data-stu-id="e7cfa-140">System.Void</span></span>

## <span data-ttu-id="e7cfa-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7cfa-141">NOTES</span></span>

## <span data-ttu-id="e7cfa-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7cfa-142">RELATED LINKS</span></span>
