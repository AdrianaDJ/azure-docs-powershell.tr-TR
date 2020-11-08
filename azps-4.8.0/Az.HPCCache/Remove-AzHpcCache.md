---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267233"
---
# <span data-ttu-id="a438a-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="a438a-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="a438a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a438a-102">SYNOPSIS</span></span>
<span data-ttu-id="a438a-103">HPC önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a438a-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="a438a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a438a-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a438a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a438a-105">DESCRIPTION</span></span>
<span data-ttu-id="a438a-106">**Remove-AzHpcCache** cmdlet 'ı BIR Azure HPC önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a438a-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="a438a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a438a-107">EXAMPLES</span></span>

### <span data-ttu-id="a438a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a438a-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="a438a-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a438a-109">PARAMETERS</span></span>

### <span data-ttu-id="a438a-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="a438a-110">-AsJob</span></span>
<span data-ttu-id="a438a-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a438a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a438a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a438a-112">-DefaultProfile</span></span>
<span data-ttu-id="a438a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a438a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a438a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a438a-114">-Force</span></span>
<span data-ttu-id="a438a-115">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a438a-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="a438a-116">Varsayılan olarak, bu cmdlet önbelleğin kaldırılmasını onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a438a-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="a438a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a438a-117">-Name</span></span>
<span data-ttu-id="a438a-118">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="a438a-118">Name of cache.</span></span>

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

### <span data-ttu-id="a438a-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a438a-119">-PassThru</span></span>
<span data-ttu-id="a438a-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a438a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a438a-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a438a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a438a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a438a-122">-ResourceGroupName</span></span>
<span data-ttu-id="a438a-123">Önbelleğini kaldırmak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a438a-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="a438a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="a438a-124">-Confirm</span></span>
<span data-ttu-id="a438a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a438a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a438a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a438a-126">-WhatIf</span></span>
<span data-ttu-id="a438a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a438a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a438a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a438a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a438a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a438a-129">CommonParameters</span></span>
<span data-ttu-id="a438a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a438a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a438a-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a438a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a438a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a438a-132">INPUTS</span></span>

### <span data-ttu-id="a438a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a438a-133">System.String</span></span>

## <span data-ttu-id="a438a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a438a-134">OUTPUTS</span></span>

## <span data-ttu-id="a438a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a438a-135">NOTES</span></span>

## <span data-ttu-id="a438a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a438a-136">RELATED LINKS</span></span>
