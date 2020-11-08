---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 4a6c93c0946780420cffb8b5cb6d2e9331d55bae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096026"
---
# <span data-ttu-id="098e2-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="098e2-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="098e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098e2-102">SYNOPSIS</span></span>
<span data-ttu-id="098e2-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="098e2-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="098e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="098e2-104">SYNTAX</span></span>

### <span data-ttu-id="098e2-105">ByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="098e2-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="098e2-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="098e2-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="098e2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="098e2-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="098e2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="098e2-108">DESCRIPTION</span></span>
<span data-ttu-id="098e2-109">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="098e2-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="098e2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="098e2-110">EXAMPLES</span></span>

### <span data-ttu-id="098e2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="098e2-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="098e2-112">FailoverPolicies region1, FailoverPriority 1 olarak Region2, FailoverPriority 2 olarak ve FailoverPriority 3 olarak region3.</span><span class="sxs-lookup"><span data-stu-id="098e2-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="098e2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="098e2-113">PARAMETERS</span></span>

### <span data-ttu-id="098e2-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="098e2-114">-AsJob</span></span>
<span data-ttu-id="098e2-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="098e2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="098e2-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="098e2-116">-Confirm</span></span>
<span data-ttu-id="098e2-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="098e2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="098e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098e2-118">-DefaultProfile</span></span>
<span data-ttu-id="098e2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="098e2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="098e2-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="098e2-120">-FailoverPolicy</span></span>
<span data-ttu-id="098e2-121">Bölge adlarına sahip, yük devretme önceliğine göre sıralanan dizeler dizisi.</span><span class="sxs-lookup"><span data-stu-id="098e2-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="098e2-122">Örneğin eastus, westus</span><span class="sxs-lookup"><span data-stu-id="098e2-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="098e2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="098e2-123">-InputObject</span></span>
<span data-ttu-id="098e2-124">CosmosDB hesap nesnesi</span><span class="sxs-lookup"><span data-stu-id="098e2-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="098e2-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="098e2-125">-Name</span></span>
<span data-ttu-id="098e2-126">Cosmos DB veritabanı hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="098e2-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="098e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="098e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="098e2-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="098e2-128">Name of resource group.</span></span>

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

### <span data-ttu-id="098e2-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="098e2-129">-ResourceId</span></span>
<span data-ttu-id="098e2-130">Kaynağın RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="098e2-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="098e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="098e2-131">-WhatIf</span></span>
<span data-ttu-id="098e2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="098e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="098e2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="098e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="098e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098e2-134">CommonParameters</span></span>
<span data-ttu-id="098e2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="098e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098e2-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="098e2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098e2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="098e2-137">INPUTS</span></span>

### <span data-ttu-id="098e2-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="098e2-138">None</span></span>

## <span data-ttu-id="098e2-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="098e2-139">OUTPUTS</span></span>

### <span data-ttu-id="098e2-140">System. void</span><span class="sxs-lookup"><span data-stu-id="098e2-140">System.Void</span></span>

## <span data-ttu-id="098e2-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="098e2-141">NOTES</span></span>

## <span data-ttu-id="098e2-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="098e2-142">RELATED LINKS</span></span>