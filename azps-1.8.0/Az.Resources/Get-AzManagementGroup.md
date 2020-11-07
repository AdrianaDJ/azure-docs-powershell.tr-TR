---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: 19e2c227e8715d74cd9c33eaacd2807a96a5afc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759441"
---
# <span data-ttu-id="0b2b4-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b2b4-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="0b2b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2b4-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2b4-103">Yönetim gruplarını alır</span><span class="sxs-lookup"><span data-stu-id="0b2b4-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="0b2b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b2b4-104">SYNTAX</span></span>

### <span data-ttu-id="0b2b4-105">Lıperation (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b2b4-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2b4-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="0b2b4-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b2b4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b2b4-107">DESCRIPTION</span></span>
<span data-ttu-id="0b2b4-108">Get-AzManagementGroup cmdlet 'i veya belirli bir yönetim grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="0b2b4-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="0b2b4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b2b4-109">EXAMPLES</span></span>

### <span data-ttu-id="0b2b4-110">Örnek 1: tüm yönetim gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="0b2b4-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="0b2b4-111">Örnek 2: belirli bir yönetim grubu edinin</span><span class="sxs-lookup"><span data-stu-id="0b2b4-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="0b2b4-112">Örnek 3: belirli bir yönetim grubu ve hiyerarşinin birinci düzeyini alma</span><span class="sxs-lookup"><span data-stu-id="0b2b4-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="0b2b4-113">Bayrak ile `Expand` bir tane, dizi boyunca gezinilerek `Children` her çocuğun ayrıntılarını alabilirler.</span><span class="sxs-lookup"><span data-stu-id="0b2b4-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="0b2b4-114">Örneğin, `Children[0]` görünen adı olan grubun ayrıntılarını sağlayacaktır `TestGroup1DisplayName` .</span><span class="sxs-lookup"><span data-stu-id="0b2b4-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="0b2b4-115">Örnek 4: belirli bir yönetim grubu ve tüm hiyerarşi düzeylerini alma</span><span class="sxs-lookup"><span data-stu-id="0b2b4-115">Example 4: Get specific Management Group and all levels of hiearchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="0b2b4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b2b4-116">PARAMETERS</span></span>

### <span data-ttu-id="0b2b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2b4-117">-DefaultProfile</span></span>
<span data-ttu-id="0b2b4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b2b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2b4-119">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="0b2b4-119">-Expand</span></span>
<span data-ttu-id="0b2b4-120">Yönetim grubunun alt öğelerini listelemek için çıktıyı genişletme</span><span class="sxs-lookup"><span data-stu-id="0b2b4-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b4-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="0b2b4-121">-GroupName</span></span>
<span data-ttu-id="0b2b4-122">Yönetim grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="0b2b4-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b4-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="0b2b4-123">-Recurse</span></span>
<span data-ttu-id="0b2b4-124">Yinelemeli olarak yönetim grubunun alt öğelerini listeler</span><span class="sxs-lookup"><span data-stu-id="0b2b4-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2b4-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b2b4-125">-Confirm</span></span>
<span data-ttu-id="0b2b4-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b2b4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2b4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2b4-127">-WhatIf</span></span>
<span data-ttu-id="0b2b4-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b2b4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2b4-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b2b4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2b4-130">CommonParameters</span></span>
<span data-ttu-id="0b2b4-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b2b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2b4-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2b4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2b4-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b2b4-133">INPUTS</span></span>

### <span data-ttu-id="0b2b4-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0b2b4-134">None</span></span>

## <span data-ttu-id="0b2b4-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b2b4-135">OUTPUTS</span></span>

### <span data-ttu-id="0b2b4-136">Microsoft. Azure. Commands. resources. model. ManagementGroups. Psmanagementgroupınfo</span><span class="sxs-lookup"><span data-stu-id="0b2b4-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="0b2b4-137">Microsoft. Azure. Commands. resources. modeller. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b2b4-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="0b2b4-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b2b4-138">NOTES</span></span>

## <span data-ttu-id="0b2b4-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b2b4-139">RELATED LINKS</span></span>