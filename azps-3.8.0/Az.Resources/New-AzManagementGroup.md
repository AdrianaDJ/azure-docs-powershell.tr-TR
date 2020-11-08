---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 7998772b1a8e6a510e1eaec5daefaf4203259ab2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938050"
---
# <span data-ttu-id="e07dc-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e07dc-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="e07dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e07dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e07dc-103">Yönetim grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="e07dc-103">Creates a Management Group</span></span>

## <span data-ttu-id="e07dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e07dc-104">SYNTAX</span></span>

### <span data-ttu-id="e07dc-105">GroupOperations (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e07dc-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07dc-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="e07dc-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e07dc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e07dc-107">DESCRIPTION</span></span>
<span data-ttu-id="e07dc-108">**New-AzManagementGroup** cmdlet 'i bir yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e07dc-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="e07dc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e07dc-109">EXAMPLES</span></span>

### <span data-ttu-id="e07dc-110">Örnek 1: yönetim grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e07dc-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="e07dc-111">`DisplayName`Ve olarak ayarlanmış yeni bir grup oluşturma `ParentId` `null` .</span><span class="sxs-lookup"><span data-stu-id="e07dc-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="e07dc-112">`DisplayName`İle aynı olacak `GroupName` ve grubun üst öğesi kiracı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e07dc-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="e07dc-113">Örnek 2: görünen ad içeren bir yönetim grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e07dc-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="e07dc-114">Bu durumda, grubun üst öğesi kiracı olur ve `DisplayName` verilen değere ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e07dc-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="e07dc-115">Örnek 3: üst öğe ve görünen ad içeren bir yönetim grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e07dc-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="e07dc-116">Örnek 4: üst nesne kullanarak yönetim grubu oluşturma (üst nesne kullanarak)</span><span class="sxs-lookup"><span data-stu-id="e07dc-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="e07dc-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e07dc-117">PARAMETERS</span></span>

### <span data-ttu-id="e07dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07dc-118">-DefaultProfile</span></span>
<span data-ttu-id="e07dc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e07dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e07dc-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e07dc-120">-DisplayName</span></span>
<span data-ttu-id="e07dc-121">Yönetim grubunun görünen adı</span><span class="sxs-lookup"><span data-stu-id="e07dc-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="e07dc-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="e07dc-122">-GroupName</span></span>
<span data-ttu-id="e07dc-123">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="e07dc-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07dc-124">-ParentID</span><span class="sxs-lookup"><span data-stu-id="e07dc-124">-ParentId</span></span>
<span data-ttu-id="e07dc-125">Yönetim grubunun üst kimliği</span><span class="sxs-lookup"><span data-stu-id="e07dc-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07dc-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e07dc-126">-ParentObject</span></span>
<span data-ttu-id="e07dc-127">Üst nesne</span><span class="sxs-lookup"><span data-stu-id="e07dc-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07dc-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="e07dc-128">-Confirm</span></span>
<span data-ttu-id="e07dc-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e07dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07dc-130">-WhatIf</span></span>
<span data-ttu-id="e07dc-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e07dc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07dc-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e07dc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07dc-133">CommonParameters</span></span>
<span data-ttu-id="e07dc-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e07dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07dc-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e07dc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07dc-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e07dc-136">INPUTS</span></span>

### <span data-ttu-id="e07dc-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e07dc-137">None</span></span>

## <span data-ttu-id="e07dc-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e07dc-138">OUTPUTS</span></span>

### <span data-ttu-id="e07dc-139">Microsoft. Azure. Commands. resources. modeller. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e07dc-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="e07dc-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e07dc-140">NOTES</span></span>

## <span data-ttu-id="e07dc-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e07dc-141">RELATED LINKS</span></span>

[<span data-ttu-id="e07dc-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e07dc-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="e07dc-143">Güncelleştirme-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e07dc-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="e07dc-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e07dc-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)