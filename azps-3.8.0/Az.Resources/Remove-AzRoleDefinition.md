---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097268"
---
# <span data-ttu-id="a0379-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a0379-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="a0379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0379-102">SYNOPSIS</span></span>
<span data-ttu-id="a0379-103">Azure RBAC 'de özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="a0379-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="a0379-104">Silinecek rol, rolün ID özelliği kullanılarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="a0379-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="a0379-105">Özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="a0379-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="a0379-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0379-106">SYNTAX</span></span>

### <span data-ttu-id="a0379-107">Roledefinitionıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0379-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0379-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0379-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0379-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="a0379-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0379-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0379-110">DESCRIPTION</span></span>
<span data-ttu-id="a0379-111">Remove-AzRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="a0379-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="a0379-112">Var olan özel rolün silineceği kimlik parametresini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="a0379-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="a0379-113">Varsayılan olarak Remove-AzRoleDefinition sizden onay ister.</span><span class="sxs-lookup"><span data-stu-id="a0379-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="a0379-114">İstemi bastırmak için Force parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0379-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="a0379-115">Silinecek özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="a0379-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="a0379-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0379-116">EXAMPLES</span></span>

### <span data-ttu-id="a0379-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0379-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="a0379-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a0379-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="a0379-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0379-119">PARAMETERS</span></span>

### <span data-ttu-id="a0379-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0379-120">-DefaultProfile</span></span>
<span data-ttu-id="a0379-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a0379-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0379-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a0379-122">-Force</span></span>
<span data-ttu-id="a0379-123">Ayarlanırsa, özel rolü silmeden önce onay istemez</span><span class="sxs-lookup"><span data-stu-id="a0379-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="a0379-124">-ID</span><span class="sxs-lookup"><span data-stu-id="a0379-124">-Id</span></span>
<span data-ttu-id="a0379-125">Silinecek rol tanımının kimliği</span><span class="sxs-lookup"><span data-stu-id="a0379-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0379-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0379-126">-InputObject</span></span>
<span data-ttu-id="a0379-127">Kaldırılacak rol tanımını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="a0379-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0379-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0379-128">-Name</span></span>
<span data-ttu-id="a0379-129">Silinecek rol tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="a0379-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0379-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a0379-130">-PassThru</span></span>
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

### <span data-ttu-id="a0379-131">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="a0379-131">-Scope</span></span>
<span data-ttu-id="a0379-132">Rol tanımı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="a0379-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0379-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0379-133">-Confirm</span></span>
<span data-ttu-id="a0379-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0379-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0379-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0379-135">-WhatIf</span></span>
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

### <span data-ttu-id="a0379-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0379-136">CommonParameters</span></span>
<span data-ttu-id="a0379-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0379-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0379-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0379-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0379-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0379-139">INPUTS</span></span>

### <span data-ttu-id="a0379-140">System. Guid</span><span class="sxs-lookup"><span data-stu-id="a0379-140">System.Guid</span></span>

### <span data-ttu-id="a0379-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a0379-141">System.String</span></span>

### <span data-ttu-id="a0379-142">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a0379-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="a0379-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0379-143">OUTPUTS</span></span>

### <span data-ttu-id="a0379-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0379-144">System.Boolean</span></span>

## <span data-ttu-id="a0379-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0379-145">NOTES</span></span>
<span data-ttu-id="a0379-146">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="a0379-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a0379-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0379-147">RELATED LINKS</span></span>

[<span data-ttu-id="a0379-148">Yeni-Azrol tanımı</span><span class="sxs-lookup"><span data-stu-id="a0379-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="a0379-149">Get-Azroltanımı</span><span class="sxs-lookup"><span data-stu-id="a0379-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="a0379-150">Set-Azroltanımı</span><span class="sxs-lookup"><span data-stu-id="a0379-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

