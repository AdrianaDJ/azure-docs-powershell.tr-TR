---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268858"
---
# <span data-ttu-id="34199-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="34199-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="34199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34199-102">SYNOPSIS</span></span>
<span data-ttu-id="34199-103">HPC önbelleğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="34199-103">Stops HPC cache.</span></span>

## <span data-ttu-id="34199-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34199-104">SYNTAX</span></span>

### <span data-ttu-id="34199-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34199-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34199-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="34199-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34199-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34199-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34199-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34199-108">DESCRIPTION</span></span>
<span data-ttu-id="34199-109">**Stop-AzHpcCache** cmdlet 'ı BIR Azure HPC önbelleğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="34199-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="34199-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34199-110">EXAMPLES</span></span>

### <span data-ttu-id="34199-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34199-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="34199-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34199-112">PARAMETERS</span></span>

### <span data-ttu-id="34199-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34199-113">-DefaultProfile</span></span>
<span data-ttu-id="34199-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34199-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34199-115">-Force</span><span class="sxs-lookup"><span data-stu-id="34199-115">-Force</span></span>
<span data-ttu-id="34199-116">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34199-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="34199-117">Varsayılan olarak, bu cmdlet önbelleğin durmasını istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34199-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="34199-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34199-118">-InputObject</span></span>
<span data-ttu-id="34199-119">Durdurulacak önbellek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="34199-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="34199-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="34199-120">-Name</span></span>
<span data-ttu-id="34199-121">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="34199-121">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34199-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34199-122">-PassThru</span></span>
<span data-ttu-id="34199-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="34199-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="34199-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="34199-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34199-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34199-125">-ResourceGroupName</span></span>
<span data-ttu-id="34199-126">Önbelleğini durdurmak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34199-126">Name of resource group under which you want to stop cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34199-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="34199-127">-ResourceId</span></span>
<span data-ttu-id="34199-128">Önbelleğin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="34199-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="34199-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="34199-129">-Confirm</span></span>
<span data-ttu-id="34199-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34199-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34199-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34199-131">-WhatIf</span></span>
<span data-ttu-id="34199-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34199-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34199-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34199-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34199-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34199-134">CommonParameters</span></span>
<span data-ttu-id="34199-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34199-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34199-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34199-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34199-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34199-137">INPUTS</span></span>

### <span data-ttu-id="34199-138">System. String</span><span class="sxs-lookup"><span data-stu-id="34199-138">System.String</span></span>

## <span data-ttu-id="34199-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34199-139">OUTPUTS</span></span>

## <span data-ttu-id="34199-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34199-140">NOTES</span></span>

## <span data-ttu-id="34199-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34199-141">RELATED LINKS</span></span>
