---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277394"
---
# <span data-ttu-id="9a797-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="9a797-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="9a797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a797-102">SYNOPSIS</span></span>
<span data-ttu-id="9a797-103">Bir HPC önbelleğindeki etiketleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9a797-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="9a797-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a797-104">SYNTAX</span></span>

### <span data-ttu-id="9a797-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9a797-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a797-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a797-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a797-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a797-107">DESCRIPTION</span></span>
<span data-ttu-id="9a797-108">**Set-AzHpcCache** cmdlet 'ı BIR Azure HPC Cache etiketini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9a797-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="9a797-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a797-109">EXAMPLES</span></span>

### <span data-ttu-id="9a797-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9a797-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="9a797-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a797-111">PARAMETERS</span></span>

### <span data-ttu-id="9a797-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="9a797-112">-AsJob</span></span>
<span data-ttu-id="9a797-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9a797-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a797-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a797-114">-DefaultProfile</span></span>
<span data-ttu-id="9a797-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9a797-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a797-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a797-116">-InputObject</span></span>
<span data-ttu-id="9a797-117">Güncelleştirilecek önbellek nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9a797-117">The cache object to update.</span></span>

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

### <span data-ttu-id="9a797-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9a797-118">-Name</span></span>
<span data-ttu-id="9a797-119">Önbelleğin adı.</span><span class="sxs-lookup"><span data-stu-id="9a797-119">Name of cache.</span></span>

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

### <span data-ttu-id="9a797-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a797-120">-ResourceGroupName</span></span>
<span data-ttu-id="9a797-121">Önbelleğini güncelleştirmek istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9a797-121">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="9a797-122">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9a797-122">-Tag</span></span>
<span data-ttu-id="9a797-123">HPC Cache ile ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="9a797-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a797-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="9a797-124">-Confirm</span></span>
<span data-ttu-id="9a797-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9a797-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a797-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a797-126">-WhatIf</span></span>
<span data-ttu-id="9a797-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9a797-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a797-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9a797-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a797-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a797-129">CommonParameters</span></span>
<span data-ttu-id="9a797-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a797-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a797-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9a797-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a797-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a797-132">INPUTS</span></span>

### <span data-ttu-id="9a797-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9a797-133">System.String</span></span>

### <span data-ttu-id="9a797-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9a797-134">System.Int32</span></span>

## <span data-ttu-id="9a797-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a797-135">OUTPUTS</span></span>

### <span data-ttu-id="9a797-136">Microsoft. Azure. PowerShell. cmdlet. HPCCache. modeller. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="9a797-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="9a797-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a797-137">NOTES</span></span>

## <span data-ttu-id="9a797-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a797-138">RELATED LINKS</span></span>
