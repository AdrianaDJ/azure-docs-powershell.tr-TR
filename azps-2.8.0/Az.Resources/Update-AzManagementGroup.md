---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdccb01293f60c876470d2ac443c8e85f354e2d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932529"
---
# <span data-ttu-id="6d1dc-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6d1dc-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="6d1dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1dc-103">Yönetim grubunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="6d1dc-103">Updates a Management Group</span></span>

## <span data-ttu-id="6d1dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d1dc-104">SYNTAX</span></span>

### <span data-ttu-id="6d1dc-105">GroupOperations (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6d1dc-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d1dc-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="6d1dc-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d1dc-107">Yönetim</span><span class="sxs-lookup"><span data-stu-id="6d1dc-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d1dc-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="6d1dc-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d1dc-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d1dc-109">DESCRIPTION</span></span>
<span data-ttu-id="6d1dc-110">**Update-AzManagementGroup** cmdlet 'ı bir yönetim grubu için **parentID** veya **DisplayName** 'i güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="6d1dc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d1dc-111">EXAMPLES</span></span>

### <span data-ttu-id="6d1dc-112">Örnek 1: yönetim grubunun görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6d1dc-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="6d1dc-113">Örnek 2: yönetim grubunun üst öğesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6d1dc-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="6d1dc-114">Örnek 3: bir yönetim grubunu, PSManagementGroup nesnesini kullanarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6d1dc-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="6d1dc-115">Örnek 4: ParentObject kullanarak yönetim grubunun üst öğesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6d1dc-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="6d1dc-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d1dc-116">PARAMETERS</span></span>

### <span data-ttu-id="6d1dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1dc-117">-DefaultProfile</span></span>
<span data-ttu-id="6d1dc-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d1dc-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6d1dc-119">-DisplayName</span></span>
<span data-ttu-id="6d1dc-120">Yönetim grubunun görünen adı</span><span class="sxs-lookup"><span data-stu-id="6d1dc-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="6d1dc-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="6d1dc-121">-GroupName</span></span>
<span data-ttu-id="6d1dc-122">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="6d1dc-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1dc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d1dc-123">-InputObject</span></span>
<span data-ttu-id="6d1dc-124">Arama al 'dan giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="6d1dc-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1dc-125">-ParentID</span><span class="sxs-lookup"><span data-stu-id="6d1dc-125">-ParentId</span></span>
<span data-ttu-id="6d1dc-126">Yönetim grubunun üst kimliği</span><span class="sxs-lookup"><span data-stu-id="6d1dc-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1dc-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6d1dc-127">-ParentObject</span></span>
<span data-ttu-id="6d1dc-128">Arama al 'dan giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="6d1dc-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1dc-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d1dc-129">-Confirm</span></span>
<span data-ttu-id="6d1dc-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d1dc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d1dc-131">-WhatIf</span></span>
<span data-ttu-id="6d1dc-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d1dc-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d1dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1dc-134">CommonParameters</span></span>
<span data-ttu-id="6d1dc-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d1dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1dc-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d1dc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1dc-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d1dc-137">INPUTS</span></span>

### <span data-ttu-id="6d1dc-138">Microsoft. Azure. Commands. resources. modeller. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6d1dc-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6d1dc-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d1dc-139">OUTPUTS</span></span>

### <span data-ttu-id="6d1dc-140">Microsoft. Azure. Commands. resources. modeller. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6d1dc-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="6d1dc-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d1dc-141">NOTES</span></span>

## <span data-ttu-id="6d1dc-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d1dc-142">RELATED LINKS</span></span>
