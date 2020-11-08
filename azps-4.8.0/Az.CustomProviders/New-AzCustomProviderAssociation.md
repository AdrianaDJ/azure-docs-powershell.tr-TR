---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268035"
---
# <span data-ttu-id="252d3-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="252d3-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="252d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="252d3-102">SYNOPSIS</span></span>
<span data-ttu-id="252d3-103">Bir ilişki oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="252d3-103">Create or update an association.</span></span>

## <span data-ttu-id="252d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="252d3-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="252d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="252d3-105">DESCRIPTION</span></span>
<span data-ttu-id="252d3-106">Bir ilişki oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="252d3-106">Create or update an association.</span></span>

## <span data-ttu-id="252d3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="252d3-107">EXAMPLES</span></span>

### <span data-ttu-id="252d3-108">Örnek 1: özel sağlayıcı ilişkilendirmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="252d3-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="252d3-109">Özel bir sağlayıcı ilişkilendirmesi oluşturmak için, ilişkili hedef provioder</span><span class="sxs-lookup"><span data-stu-id="252d3-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="252d3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="252d3-110">PARAMETERS</span></span>

### <span data-ttu-id="252d3-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="252d3-111">-AsJob</span></span>
<span data-ttu-id="252d3-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="252d3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="252d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252d3-113">-DefaultProfile</span></span>
<span data-ttu-id="252d3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="252d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252d3-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="252d3-115">-Name</span></span>
<span data-ttu-id="252d3-116">İlişkinin adı.</span><span class="sxs-lookup"><span data-stu-id="252d3-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252d3-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="252d3-117">-NoWait</span></span>
<span data-ttu-id="252d3-118">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="252d3-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="252d3-119">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="252d3-119">-Scope</span></span>
<span data-ttu-id="252d3-120">İlişkilendirmenin kapsamı.</span><span class="sxs-lookup"><span data-stu-id="252d3-120">The scope of the association.</span></span>
<span data-ttu-id="252d3-121">Kapsam herhangi bir geçerli REST kaynak örneği olabilir.</span><span class="sxs-lookup"><span data-stu-id="252d3-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="252d3-122">Örneğin, sanal makine kaynağı için '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name} ' kullanın.</span><span class="sxs-lookup"><span data-stu-id="252d3-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252d3-123">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="252d3-123">-TargetResourceId</span></span>
<span data-ttu-id="252d3-124">Bu ilişki için hedef kaynağın REST kaynak örneği.</span><span class="sxs-lookup"><span data-stu-id="252d3-124">The REST resource instance of the target resource for this association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252d3-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="252d3-125">-Confirm</span></span>
<span data-ttu-id="252d3-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="252d3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="252d3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="252d3-127">-WhatIf</span></span>
<span data-ttu-id="252d3-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="252d3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="252d3-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="252d3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="252d3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252d3-130">CommonParameters</span></span>
<span data-ttu-id="252d3-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="252d3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252d3-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="252d3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252d3-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="252d3-133">INPUTS</span></span>

## <span data-ttu-id="252d3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="252d3-134">OUTPUTS</span></span>

### <span data-ttu-id="252d3-135">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. model. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="252d3-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="252d3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="252d3-136">NOTES</span></span>

<span data-ttu-id="252d3-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="252d3-137">ALIASES</span></span>

## <span data-ttu-id="252d3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="252d3-138">RELATED LINKS</span></span>

