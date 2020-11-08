---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277811"
---
# <span data-ttu-id="e1120-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e1120-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="e1120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1120-102">SYNOPSIS</span></span>
<span data-ttu-id="e1120-103">HPC önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e1120-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="e1120-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1120-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1120-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1120-105">DESCRIPTION</span></span>
<span data-ttu-id="e1120-106">**Remove-AzHpcCache** cmdlet 'ı BIR Azure HPC önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e1120-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="e1120-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1120-107">EXAMPLES</span></span>

### <span data-ttu-id="e1120-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e1120-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="e1120-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1120-109">PARAMETERS</span></span>

### <span data-ttu-id="e1120-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="e1120-110">-AsJob</span></span>
<span data-ttu-id="e1120-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e1120-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1120-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1120-112">-DefaultProfile</span></span>
<span data-ttu-id="e1120-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1120-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1120-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e1120-114">-Force</span></span>
<span data-ttu-id="e1120-115">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1120-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e1120-116">Varsayılan olarak, bu cmdlet önbelleğin kaldırılmasını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1120-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="e1120-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1120-117">-Name</span></span>
<span data-ttu-id="e1120-118">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="e1120-118">Name of cache.</span></span>

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

### <span data-ttu-id="e1120-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e1120-119">-PassThru</span></span>
<span data-ttu-id="e1120-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e1120-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1120-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e1120-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1120-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1120-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1120-123">Önbelleğini kaldırmak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e1120-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="e1120-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="e1120-124">-Confirm</span></span>
<span data-ttu-id="e1120-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1120-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1120-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1120-126">-WhatIf</span></span>
<span data-ttu-id="e1120-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1120-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1120-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e1120-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1120-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1120-129">CommonParameters</span></span>
<span data-ttu-id="e1120-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1120-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1120-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e1120-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1120-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1120-132">INPUTS</span></span>

### <span data-ttu-id="e1120-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e1120-133">System.String</span></span>

## <span data-ttu-id="e1120-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1120-134">OUTPUTS</span></span>

## <span data-ttu-id="e1120-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1120-135">NOTES</span></span>

## <span data-ttu-id="e1120-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1120-136">RELATED LINKS</span></span>
