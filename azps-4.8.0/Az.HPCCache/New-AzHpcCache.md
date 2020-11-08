---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267698"
---
# <span data-ttu-id="88ef1-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="88ef1-101">New-AzHpcCache</span></span>

## <span data-ttu-id="88ef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="88ef1-103">HPC önbelleği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ef1-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="88ef1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88ef1-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88ef1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="88ef1-106">**Yeni-AzHpcCache** cmdlet 'ı Azure HPC Cache oluşturur.</span><span class="sxs-lookup"><span data-stu-id="88ef1-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="88ef1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88ef1-107">EXAMPLES</span></span>

### <span data-ttu-id="88ef1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="88ef1-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="88ef1-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88ef1-109">PARAMETERS</span></span>

### <span data-ttu-id="88ef1-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="88ef1-110">-AsJob</span></span>
<span data-ttu-id="88ef1-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="88ef1-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="88ef1-112">-CacheSize</span></span>
<span data-ttu-id="88ef1-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="88ef1-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ef1-114">-DefaultProfile</span></span>
<span data-ttu-id="88ef1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88ef1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="88ef1-116">-Location</span></span>
<span data-ttu-id="88ef1-117">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="88ef1-117">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="88ef1-118">-Name</span></span>
<span data-ttu-id="88ef1-119">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="88ef1-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ef1-120">-ResourceGroupName</span></span>
<span data-ttu-id="88ef1-121">Önbelleğini oluşturmak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="88ef1-121">Name of resource group under which you want to create cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="88ef1-122">-Sku</span></span>
<span data-ttu-id="88ef1-123">'Sunda.</span><span class="sxs-lookup"><span data-stu-id="88ef1-123">Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="88ef1-124">-SubnetUri</span></span>
<span data-ttu-id="88ef1-125">Alt Neturi.</span><span class="sxs-lookup"><span data-stu-id="88ef1-125">SubnetURI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="88ef1-126">-Tag</span></span>
<span data-ttu-id="88ef1-127">HPC Cache ile ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="88ef1-127">The tags to associate with HPC Cache.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="88ef1-128">-Confirm</span></span>
<span data-ttu-id="88ef1-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="88ef1-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ef1-130">-WhatIf</span></span>
<span data-ttu-id="88ef1-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="88ef1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88ef1-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="88ef1-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ef1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ef1-133">CommonParameters</span></span>
<span data-ttu-id="88ef1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88ef1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ef1-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="88ef1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ef1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88ef1-136">INPUTS</span></span>

### <span data-ttu-id="88ef1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="88ef1-137">System.String</span></span>

### <span data-ttu-id="88ef1-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="88ef1-138">System.Int32</span></span>

## <span data-ttu-id="88ef1-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88ef1-139">OUTPUTS</span></span>

### <span data-ttu-id="88ef1-140">Microsoft. Azure. PowerShell. cmdlet. HPCCache. modeller. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="88ef1-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="88ef1-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88ef1-141">NOTES</span></span>

## <span data-ttu-id="88ef1-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88ef1-142">RELATED LINKS</span></span>
