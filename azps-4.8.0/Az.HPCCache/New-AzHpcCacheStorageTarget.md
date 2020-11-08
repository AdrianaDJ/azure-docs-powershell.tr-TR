---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107734"
---
# <span data-ttu-id="a5c0c-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="a5c0c-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="a5c0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c0c-103">Depolama hedefi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="a5c0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5c0c-104">SYNTAX</span></span>

### <span data-ttu-id="a5c0c-105">ClfsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5c0c-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c0c-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c0c-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c0c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5c0c-107">DESCRIPTION</span></span>
<span data-ttu-id="a5c0c-108">**New-AzHpcCacheStorageTarget** cmdlet 'ı Azure HPC Cache 'e bir depolama hedefi ekler.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="a5c0c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5c0c-109">EXAMPLES</span></span>

### <span data-ttu-id="a5c0c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5c0c-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="a5c0c-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a5c0c-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="a5c0c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5c0c-112">PARAMETERS</span></span>

### <span data-ttu-id="a5c0c-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a5c0c-113">-AsJob</span></span>
<span data-ttu-id="a5c0c-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a5c0c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5c0c-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="a5c0c-115">-CacheName</span></span>
<span data-ttu-id="a5c0c-116">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-116">Name of cache.</span></span>

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

### <span data-ttu-id="a5c0c-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="a5c0c-117">-CLFS</span></span>
<span data-ttu-id="a5c0c-118">CLFS depolama hedef türünü güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="a5c0c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c0c-119">-DefaultProfile</span></span>
<span data-ttu-id="a5c0c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5c0c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a5c0c-121">-Force</span></span>
<span data-ttu-id="a5c0c-122">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="a5c0c-123">Varsayılan olarak, bu cmdlet önbelleğin temizlenmesi istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="a5c0c-124">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="a5c0c-124">-HostName</span></span>
<span data-ttu-id="a5c0c-125">NFS ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c0c-126">-Kavşak</span><span class="sxs-lookup"><span data-stu-id="a5c0c-126">-Junction</span></span>
<span data-ttu-id="a5c0c-127">Kavş.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-127">Junction.</span></span>

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

### <span data-ttu-id="a5c0c-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5c0c-128">-Name</span></span>
<span data-ttu-id="a5c0c-129">Depolama hedefinin adı.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-129">Name of storage target.</span></span>

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

### <span data-ttu-id="a5c0c-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="a5c0c-130">-NFS</span></span>
<span data-ttu-id="a5c0c-131">NFS depolama hedef türünü güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="a5c0c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c0c-132">-ResourceGroupName</span></span>
<span data-ttu-id="a5c0c-133">"Verilen önbellek için depolama hedefini oluşturmak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="a5c0c-134">-Storagecontainerıd</span><span class="sxs-lookup"><span data-stu-id="a5c0c-134">-StorageContainerID</span></span>
<span data-ttu-id="a5c0c-135">Storagecontainerıd</span><span class="sxs-lookup"><span data-stu-id="a5c0c-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c0c-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="a5c0c-136">-UsageModel</span></span>
<span data-ttu-id="a5c0c-137">NFS kullanım modeli.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c0c-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5c0c-138">-Confirm</span></span>
<span data-ttu-id="a5c0c-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c0c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c0c-140">-WhatIf</span></span>
<span data-ttu-id="a5c0c-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5c0c-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c0c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c0c-143">CommonParameters</span></span>
<span data-ttu-id="a5c0c-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c0c-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a5c0c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c0c-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5c0c-146">INPUTS</span></span>

### <span data-ttu-id="a5c0c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a5c0c-147">System.String</span></span>

## <span data-ttu-id="a5c0c-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5c0c-148">OUTPUTS</span></span>

### <span data-ttu-id="a5c0c-149">Microsoft. Azure. PowerShell. cmdlet. HPCCache. modeller. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="a5c0c-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="a5c0c-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5c0c-150">NOTES</span></span>

## <span data-ttu-id="a5c0c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5c0c-151">RELATED LINKS</span></span>
