---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321290"
---
# <span data-ttu-id="f2b7c-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="f2b7c-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="f2b7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b7c-103">Bir ilişki oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-103">Create or update an association.</span></span>

## <span data-ttu-id="f2b7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2b7c-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f2b7c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b7c-106">Bir ilişki oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-106">Create or update an association.</span></span>

## <span data-ttu-id="f2b7c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2b7c-107">EXAMPLES</span></span>

### <span data-ttu-id="f2b7c-108">Örnek 1: özel sağlayıcı ilişkilendirmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f2b7c-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="f2b7c-109">Özel bir sağlayıcı ilişkilendirmesi oluşturmak için, ilişkili hedef provioder</span><span class="sxs-lookup"><span data-stu-id="f2b7c-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="f2b7c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2b7c-110">PARAMETERS</span></span>

### <span data-ttu-id="f2b7c-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f2b7c-111">-AsJob</span></span>
<span data-ttu-id="f2b7c-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="f2b7c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f2b7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b7c-113">-DefaultProfile</span></span>
<span data-ttu-id="f2b7c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2b7c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2b7c-115">-Name</span></span>
<span data-ttu-id="f2b7c-116">İlişkinin adı.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-116">The name of the association.</span></span>

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

### <span data-ttu-id="f2b7c-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f2b7c-117">-NoWait</span></span>
<span data-ttu-id="f2b7c-118">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="f2b7c-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f2b7c-119">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="f2b7c-119">-Scope</span></span>
<span data-ttu-id="f2b7c-120">İlişkilendirmenin kapsamı.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-120">The scope of the association.</span></span>
<span data-ttu-id="f2b7c-121">Kapsam herhangi bir geçerli REST kaynak örneği olabilir.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="f2b7c-122">Örneğin, sanal makine kaynağı için '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name} ' kullanın.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="f2b7c-123">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="f2b7c-123">-TargetResourceId</span></span>
<span data-ttu-id="f2b7c-124">Bu ilişki için hedef kaynağın REST kaynak örneği.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="f2b7c-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2b7c-125">-Confirm</span></span>
<span data-ttu-id="f2b7c-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b7c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b7c-127">-WhatIf</span></span>
<span data-ttu-id="f2b7c-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b7c-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b7c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b7c-130">CommonParameters</span></span>
<span data-ttu-id="f2b7c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b7c-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b7c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2b7c-133">INPUTS</span></span>

## <span data-ttu-id="f2b7c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2b7c-134">OUTPUTS</span></span>

### <span data-ttu-id="f2b7c-135">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. model. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="f2b7c-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="f2b7c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2b7c-136">NOTES</span></span>

<span data-ttu-id="f2b7c-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f2b7c-137">ALIASES</span></span>

## <span data-ttu-id="f2b7c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2b7c-138">RELATED LINKS</span></span>

