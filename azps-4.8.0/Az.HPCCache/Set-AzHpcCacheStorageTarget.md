---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107733"
---
# <span data-ttu-id="45726-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="45726-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="45726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45726-102">SYNOPSIS</span></span>
<span data-ttu-id="45726-103">Depolama hedefini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="45726-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="45726-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45726-104">SYNTAX</span></span>

### <span data-ttu-id="45726-105">ClfsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="45726-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45726-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="45726-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45726-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="45726-107">DESCRIPTION</span></span>
<span data-ttu-id="45726-108">**Set-AzHpcCacheStorageTarget** cmdlet 'ı Azure HPC Cache 'e bağlı bir depolama hedefini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="45726-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="45726-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45726-109">EXAMPLES</span></span>

### <span data-ttu-id="45726-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="45726-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="45726-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="45726-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="45726-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45726-112">PARAMETERS</span></span>

### <span data-ttu-id="45726-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="45726-113">-AsJob</span></span>
<span data-ttu-id="45726-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="45726-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45726-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="45726-115">-CacheName</span></span>
<span data-ttu-id="45726-116">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="45726-116">Name of cache.</span></span>

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

### <span data-ttu-id="45726-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="45726-117">-CLFS</span></span>
<span data-ttu-id="45726-118">CLFS depolama hedef türünü güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="45726-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45726-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45726-119">-DefaultProfile</span></span>
<span data-ttu-id="45726-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45726-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45726-121">-Force</span><span class="sxs-lookup"><span data-stu-id="45726-121">-Force</span></span>
<span data-ttu-id="45726-122">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="45726-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="45726-123">Varsayılan olarak, bu cmdlet önbelleğin temizlenmesi istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45726-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="45726-124">-Kavşak</span><span class="sxs-lookup"><span data-stu-id="45726-124">-Junction</span></span>
<span data-ttu-id="45726-125">Kavş.</span><span class="sxs-lookup"><span data-stu-id="45726-125">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45726-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="45726-126">-Name</span></span>
<span data-ttu-id="45726-127">Depolama hedefinin adı.</span><span class="sxs-lookup"><span data-stu-id="45726-127">Name of storage target.</span></span>

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

### <span data-ttu-id="45726-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="45726-128">-NFS</span></span>
<span data-ttu-id="45726-129">NFS depolama hedef türünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="45726-129">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45726-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45726-130">-ResourceGroupName</span></span>
<span data-ttu-id="45726-131">Depolama hedefini güncelleştirmek istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="45726-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="45726-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="45726-132">-Confirm</span></span>
<span data-ttu-id="45726-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="45726-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45726-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45726-134">-WhatIf</span></span>
<span data-ttu-id="45726-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="45726-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45726-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="45726-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45726-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45726-137">CommonParameters</span></span>
<span data-ttu-id="45726-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45726-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45726-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45726-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45726-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45726-140">INPUTS</span></span>

### <span data-ttu-id="45726-141">System. String</span><span class="sxs-lookup"><span data-stu-id="45726-141">System.String</span></span>

## <span data-ttu-id="45726-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45726-142">OUTPUTS</span></span>

### <span data-ttu-id="45726-143">Microsoft. Azure. PowerShell. cmdlet. HPCCache. modeller. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="45726-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="45726-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45726-144">NOTES</span></span>

## <span data-ttu-id="45726-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45726-145">RELATED LINKS</span></span>
