---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274939"
---
# <span data-ttu-id="ebe7c-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="ebe7c-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="ebe7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebe7c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe7c-103">HPC Cache 'i başlatır.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-103">Starts HPC cache.</span></span>

## <span data-ttu-id="ebe7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebe7c-104">SYNTAX</span></span>

### <span data-ttu-id="ebe7c-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ebe7c-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe7c-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ebe7c-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe7c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebe7c-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebe7c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebe7c-108">DESCRIPTION</span></span>
<span data-ttu-id="ebe7c-109">**Start-AzHpcCache** cmdlet 'ı BIR Azure HPC Cache başlatır.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="ebe7c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebe7c-110">EXAMPLES</span></span>

### <span data-ttu-id="ebe7c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ebe7c-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="ebe7c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebe7c-112">PARAMETERS</span></span>

### <span data-ttu-id="ebe7c-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ebe7c-113">-AsJob</span></span>
<span data-ttu-id="ebe7c-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ebe7c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebe7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe7c-115">-DefaultProfile</span></span>
<span data-ttu-id="ebe7c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebe7c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ebe7c-117">-Force</span></span>
<span data-ttu-id="ebe7c-118">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="ebe7c-119">Varsayılan olarak, bu cmdlet önbelleğin başlamasını istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="ebe7c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebe7c-120">-InputObject</span></span>
<span data-ttu-id="ebe7c-121">Başlayacak önbellek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-121">The cache object to start.</span></span>

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

### <span data-ttu-id="ebe7c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ebe7c-122">-Name</span></span>
<span data-ttu-id="ebe7c-123">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-123">Name of cache.</span></span>

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

### <span data-ttu-id="ebe7c-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ebe7c-124">-PassThru</span></span>
<span data-ttu-id="ebe7c-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ebe7c-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ebe7c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe7c-127">-ResourceGroupName</span></span>
<span data-ttu-id="ebe7c-128">Önbelleğini başlatmak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="ebe7c-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ebe7c-129">-ResourceId</span></span>
<span data-ttu-id="ebe7c-130">Önbelleğin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ebe7c-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="ebe7c-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="ebe7c-131">-Confirm</span></span>
<span data-ttu-id="ebe7c-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebe7c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebe7c-133">-WhatIf</span></span>
<span data-ttu-id="ebe7c-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebe7c-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebe7c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe7c-136">CommonParameters</span></span>
<span data-ttu-id="ebe7c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe7c-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ebe7c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe7c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebe7c-139">INPUTS</span></span>

### <span data-ttu-id="ebe7c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ebe7c-140">System.String</span></span>

## <span data-ttu-id="ebe7c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebe7c-141">OUTPUTS</span></span>

## <span data-ttu-id="ebe7c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebe7c-142">NOTES</span></span>

## <span data-ttu-id="ebe7c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebe7c-143">RELATED LINKS</span></span>
