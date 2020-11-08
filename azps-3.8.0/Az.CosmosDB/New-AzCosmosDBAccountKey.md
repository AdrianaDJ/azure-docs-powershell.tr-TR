---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccountKey.md
ms.openlocfilehash: a9cea343a67e7e23e820c0995484aab9a1434f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097395"
---
# <span data-ttu-id="2ff7c-101">New-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="2ff7c-101">New-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="2ff7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ff7c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff7c-103">Belirli bir CosmosDB hesap anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-103">Regenerate a given CosmosDB Account Key.</span></span>

## <span data-ttu-id="2ff7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ff7c-104">SYNTAX</span></span>

### <span data-ttu-id="2ff7c-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ff7c-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-KeyKind <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff7c-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2ff7c-106">ByResourceIdParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff7c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ff7c-107">ByObjectParameterSet</span></span>
```
New-AzCosmosDBAccountKey [-KeyKind <String>] -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff7c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ff7c-108">DESCRIPTION</span></span>
<span data-ttu-id="2ff7c-109">Verilen ResourceGroup 'ta yeni bir CosmosDB hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-109">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="2ff7c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ff7c-110">EXAMPLES</span></span>

### <span data-ttu-id="2ff7c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ff7c-111">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccountKey -ResourceGroupName rg -Name dbname
```

<span data-ttu-id="2ff7c-112">Yeni anahtarlar, ResourceGroup RG.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-112">New keys are generated for Account with account name dbname in ResourceGroup rg.</span></span>

## <span data-ttu-id="2ff7c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ff7c-113">PARAMETERS</span></span>

### <span data-ttu-id="2ff7c-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="2ff7c-114">-AsJob</span></span>
<span data-ttu-id="2ff7c-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2ff7c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ff7c-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ff7c-116">-Confirm</span></span>
<span data-ttu-id="2ff7c-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff7c-118">-DefaultProfile</span></span>
<span data-ttu-id="2ff7c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff7c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ff7c-120">-InputObject</span></span>
<span data-ttu-id="2ff7c-121">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="2ff7c-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2ff7c-122">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="2ff7c-122">-KeyKind</span></span>
<span data-ttu-id="2ff7c-123">Yeniden üretmek için erişim tuşu.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-123">The access key to regenerate.</span></span>
<span data-ttu-id="2ff7c-124">Kabul edilen değerler: birincil, primaryReadonly, ikincil, secondaryReadonly</span><span class="sxs-lookup"><span data-stu-id="2ff7c-124">Accepted values: primary, primaryReadonly, secondary, secondaryReadonly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff7c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ff7c-125">-Name</span></span>
<span data-ttu-id="2ff7c-126">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2ff7c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff7c-127">-ResourceGroupName</span></span>
<span data-ttu-id="2ff7c-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-128">Name of resource group.</span></span>

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

### <span data-ttu-id="2ff7c-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ff7c-129">-ResourceId</span></span>
<span data-ttu-id="2ff7c-130">Kaynağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="2ff7c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff7c-131">-WhatIf</span></span>
<span data-ttu-id="2ff7c-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ff7c-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff7c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff7c-134">CommonParameters</span></span>
<span data-ttu-id="2ff7c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff7c-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ff7c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff7c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ff7c-137">INPUTS</span></span>

### <span data-ttu-id="2ff7c-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2ff7c-138">None</span></span>

## <span data-ttu-id="2ff7c-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ff7c-139">OUTPUTS</span></span>

### <span data-ttu-id="2ff7c-140">System. void</span><span class="sxs-lookup"><span data-stu-id="2ff7c-140">System.Void</span></span>

## <span data-ttu-id="2ff7c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ff7c-141">NOTES</span></span>

## <span data-ttu-id="2ff7c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ff7c-142">RELATED LINKS</span></span>
