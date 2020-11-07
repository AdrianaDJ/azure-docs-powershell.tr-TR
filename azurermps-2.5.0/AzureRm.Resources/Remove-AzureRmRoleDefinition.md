---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 90b7b0b1d7909210d86ec1d5ac6b465f6e9fb239
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939666"
---
# <span data-ttu-id="bb84d-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bb84d-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="bb84d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb84d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb84d-103">Azure RBAC 'de özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="bb84d-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="bb84d-104">Silinecek rol, rolün ID özelliği kullanılarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="bb84d-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="bb84d-105">Özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="bb84d-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb84d-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb84d-106">SYNTAX</span></span>

### <span data-ttu-id="bb84d-107">Roledefinitionıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb84d-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb84d-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb84d-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb84d-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="bb84d-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb84d-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb84d-110">DESCRIPTION</span></span>
<span data-ttu-id="bb84d-111">Remove-AzureRmRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="bb84d-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="bb84d-112">Var olan özel rolün silineceği kimlik parametresini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="bb84d-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="bb84d-113">Varsayılan olarak Remove-AzureRmRoleDefinition sizden onay ister.</span><span class="sxs-lookup"><span data-stu-id="bb84d-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="bb84d-114">İstemi bastırmak için Force parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb84d-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="bb84d-115">Silinecek özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="bb84d-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="bb84d-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb84d-116">EXAMPLES</span></span>

### <span data-ttu-id="bb84d-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb84d-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="bb84d-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bb84d-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="bb84d-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb84d-119">PARAMETERS</span></span>

### <span data-ttu-id="bb84d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb84d-120">-DefaultProfile</span></span>
<span data-ttu-id="bb84d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bb84d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb84d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bb84d-122">-Force</span></span>
<span data-ttu-id="bb84d-123">Ayarlanırsa, özel rolü silmeden önce onay istemez</span><span class="sxs-lookup"><span data-stu-id="bb84d-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="bb84d-124">-ID</span><span class="sxs-lookup"><span data-stu-id="bb84d-124">-Id</span></span>
<span data-ttu-id="bb84d-125">Silinecek rol tanımının kimliği</span><span class="sxs-lookup"><span data-stu-id="bb84d-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="bb84d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb84d-126">-InputObject</span></span>
<span data-ttu-id="bb84d-127">Kaldırılacak rol tanımını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="bb84d-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="bb84d-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb84d-128">-Name</span></span>
<span data-ttu-id="bb84d-129">Silinecek rol tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="bb84d-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="bb84d-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bb84d-130">-PassThru</span></span>
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

### <span data-ttu-id="bb84d-131">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="bb84d-131">-Scope</span></span>
<span data-ttu-id="bb84d-132">Rol tanımı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="bb84d-132">Role definition scope.</span></span>

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

### <span data-ttu-id="bb84d-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb84d-133">-Confirm</span></span>
<span data-ttu-id="bb84d-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb84d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb84d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb84d-135">-WhatIf</span></span>
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

### <span data-ttu-id="bb84d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb84d-136">CommonParameters</span></span>
<span data-ttu-id="bb84d-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb84d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb84d-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb84d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb84d-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb84d-139">INPUTS</span></span>

### <span data-ttu-id="bb84d-140">System. Guid</span><span class="sxs-lookup"><span data-stu-id="bb84d-140">System.Guid</span></span>

### <span data-ttu-id="bb84d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bb84d-141">System.String</span></span>

### <span data-ttu-id="bb84d-142">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bb84d-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="bb84d-143">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb84d-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bb84d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb84d-144">OUTPUTS</span></span>

### <span data-ttu-id="bb84d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb84d-145">System.Boolean</span></span>

## <span data-ttu-id="bb84d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb84d-146">NOTES</span></span>
<span data-ttu-id="bb84d-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="bb84d-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="bb84d-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb84d-148">RELATED LINKS</span></span>

[<span data-ttu-id="bb84d-149">Yeni-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bb84d-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="bb84d-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bb84d-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="bb84d-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="bb84d-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

