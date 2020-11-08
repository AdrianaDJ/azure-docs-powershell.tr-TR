---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268861"
---
# <span data-ttu-id="0b168-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="0b168-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="0b168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b168-102">SYNOPSIS</span></span>
<span data-ttu-id="0b168-103">Depolama hedefini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b168-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="0b168-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b168-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b168-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b168-105">DESCRIPTION</span></span>
<span data-ttu-id="0b168-106">**Remove-AzHpcCacheStorageTarget** cmdlet 'ı Azure HPC Cache 'Den bir depolama hedefini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b168-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="0b168-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b168-107">EXAMPLES</span></span>

### <span data-ttu-id="0b168-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0b168-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="0b168-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b168-109">PARAMETERS</span></span>

### <span data-ttu-id="0b168-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="0b168-110">-AsJob</span></span>
<span data-ttu-id="0b168-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0b168-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b168-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="0b168-112">-CacheName</span></span>
<span data-ttu-id="0b168-113">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="0b168-113">Name of cache.</span></span>

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

### <span data-ttu-id="0b168-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b168-114">-DefaultProfile</span></span>
<span data-ttu-id="0b168-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b168-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b168-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0b168-116">-Force</span></span>
<span data-ttu-id="0b168-117">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b168-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="0b168-118">Varsayılan olarak, bu cmdlet depolama hedefini kaldırmak istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b168-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="0b168-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b168-119">-Name</span></span>
<span data-ttu-id="0b168-120">Depolama hedefinin adı.</span><span class="sxs-lookup"><span data-stu-id="0b168-120">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b168-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0b168-121">-PassThru</span></span>
<span data-ttu-id="0b168-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0b168-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0b168-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0b168-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b168-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b168-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b168-125">Depolama hedefini önbellekten kaldırmak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b168-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="0b168-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b168-126">-Confirm</span></span>
<span data-ttu-id="0b168-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b168-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b168-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b168-128">-WhatIf</span></span>
<span data-ttu-id="0b168-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b168-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b168-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b168-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b168-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b168-131">CommonParameters</span></span>
<span data-ttu-id="0b168-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b168-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b168-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b168-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b168-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b168-134">INPUTS</span></span>

### <span data-ttu-id="0b168-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0b168-135">System.String</span></span>

## <span data-ttu-id="0b168-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b168-136">OUTPUTS</span></span>

## <span data-ttu-id="0b168-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b168-137">NOTES</span></span>

## <span data-ttu-id="0b168-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b168-138">RELATED LINKS</span></span>
