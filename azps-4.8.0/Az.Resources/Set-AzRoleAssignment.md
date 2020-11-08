---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266400"
---
# <span data-ttu-id="6d4cb-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6d4cb-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="6d4cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d4cb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d4cb-103">Var olan bir rol atamasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="6d4cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d4cb-104">SYNTAX</span></span>

### <span data-ttu-id="6d4cb-105">Roleatamaifade kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6d4cb-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d4cb-106">Inputfileparameterset</span><span class="sxs-lookup"><span data-stu-id="6d4cb-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d4cb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d4cb-107">DESCRIPTION</span></span>
<span data-ttu-id="6d4cb-108">Varolan bir atamayı değiştirmek için New-AzRoleAssignment komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="6d4cb-109">Açıklamalar geçerli bir dize olabilir, bunu kullanarak bir başkasına daha çok dikkatli olun.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="6d4cb-110">Koşul ayarlandıysa, koşul sürümü de ayarlanmalıdır, ancak gerekli olmayan bir koşulu güncelleştiriyorsanız.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="6d4cb-111">Condition sürümü 1,0 'den 2,0 'e yükseltilebilirken geri dönemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="6d4cb-112">2,0 1,0 ile daha uyumlu olmadığından dikkatli olun.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="6d4cb-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d4cb-113">EXAMPLES</span></span>

### <span data-ttu-id="6d4cb-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6d4cb-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="6d4cb-115">Var olan rol atamasını bir nesneyi değiştirerek güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6d4cb-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="6d4cb-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6d4cb-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="6d4cb-117">Dosya kullanarak varolan rol atamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6d4cb-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="6d4cb-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d4cb-118">PARAMETERS</span></span>

### <span data-ttu-id="6d4cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d4cb-119">-DefaultProfile</span></span>
<span data-ttu-id="6d4cb-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d4cb-121">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="6d4cb-121">-InputFile</span></span>
<span data-ttu-id="6d4cb-122">Tek bir rol tanımı içeren dosya adı.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-122">File name containing a single role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d4cb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d4cb-123">-InputObject</span></span>
<span data-ttu-id="6d4cb-124">Rol ataması.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d4cb-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6d4cb-125">-PassThru</span></span>
<span data-ttu-id="6d4cb-126">Belirtilmişse, güncelleştirilmiş rol atamasını görüntüler</span><span class="sxs-lookup"><span data-stu-id="6d4cb-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="6d4cb-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d4cb-127">-Confirm</span></span>
<span data-ttu-id="6d4cb-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d4cb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d4cb-129">-WhatIf</span></span>
<span data-ttu-id="6d4cb-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d4cb-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d4cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d4cb-132">CommonParameters</span></span>
<span data-ttu-id="6d4cb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d4cb-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6d4cb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d4cb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d4cb-135">INPUTS</span></span>

### <span data-ttu-id="6d4cb-136">Microsoft. Azure. Commands. resources. modeller. Authorization. Psroleödev</span><span class="sxs-lookup"><span data-stu-id="6d4cb-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="6d4cb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d4cb-137">OUTPUTS</span></span>

### <span data-ttu-id="6d4cb-138">Microsoft. Azure. Commands. resources. modeller. Authorization. Psroleödev</span><span class="sxs-lookup"><span data-stu-id="6d4cb-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="6d4cb-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d4cb-139">NOTES</span></span>

## <span data-ttu-id="6d4cb-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d4cb-140">RELATED LINKS</span></span>
