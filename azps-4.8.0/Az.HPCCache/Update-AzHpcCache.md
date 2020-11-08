---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274935"
---
# <span data-ttu-id="ba0e5-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="ba0e5-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="ba0e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba0e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ba0e5-103">HPC önbelleğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="ba0e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba0e5-104">SYNTAX</span></span>

### <span data-ttu-id="ba0e5-105">FlushParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba0e5-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba0e5-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ba0e5-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba0e5-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba0e5-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba0e5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba0e5-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba0e5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba0e5-109">DESCRIPTION</span></span>
<span data-ttu-id="ba0e5-110">**Güncelleştirme-AzHpcCache** cmdlet 'ı BIR Azure HPC önbelleğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="ba0e5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba0e5-111">EXAMPLES</span></span>

### <span data-ttu-id="ba0e5-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ba0e5-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="ba0e5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba0e5-113">PARAMETERS</span></span>

### <span data-ttu-id="ba0e5-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="ba0e5-114">-AsJob</span></span>
<span data-ttu-id="ba0e5-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ba0e5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba0e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba0e5-116">-DefaultProfile</span></span>
<span data-ttu-id="ba0e5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba0e5-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="ba0e5-118">-Flush</span></span>
<span data-ttu-id="ba0e5-119">HPC önbelleğini temizler.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba0e5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ba0e5-120">-Force</span></span>
<span data-ttu-id="ba0e5-121">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="ba0e5-122">Varsayılan olarak, bu cmdlet önbelleği güncelleştirmek istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="ba0e5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba0e5-123">-InputObject</span></span>
<span data-ttu-id="ba0e5-124">Güncelleştirilecek önbellek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-124">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0e5-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba0e5-125">-Name</span></span>
<span data-ttu-id="ba0e5-126">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-126">Name of cache.</span></span>

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

### <span data-ttu-id="ba0e5-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ba0e5-127">-PassThru</span></span>
<span data-ttu-id="ba0e5-128">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ba0e5-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ba0e5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba0e5-130">-ResourceGroupName</span></span>
<span data-ttu-id="ba0e5-131">Önbelleğini güncelleştirmek istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="ba0e5-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ba0e5-132">-ResourceId</span></span>
<span data-ttu-id="ba0e5-133">Önbelleğin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ba0e5-133">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0e5-134">-Yükseltme</span><span class="sxs-lookup"><span data-stu-id="ba0e5-134">-Upgrade</span></span>
<span data-ttu-id="ba0e5-135">HpcCache 'i yükseltme.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba0e5-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba0e5-136">-Confirm</span></span>
<span data-ttu-id="ba0e5-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba0e5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba0e5-138">-WhatIf</span></span>
<span data-ttu-id="ba0e5-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba0e5-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba0e5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba0e5-141">CommonParameters</span></span>
<span data-ttu-id="ba0e5-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba0e5-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba0e5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba0e5-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba0e5-144">INPUTS</span></span>

### <span data-ttu-id="ba0e5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ba0e5-145">System.String</span></span>

## <span data-ttu-id="ba0e5-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba0e5-146">OUTPUTS</span></span>

## <span data-ttu-id="ba0e5-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba0e5-147">NOTES</span></span>

## <span data-ttu-id="ba0e5-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba0e5-148">RELATED LINKS</span></span>
