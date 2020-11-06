---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 6669cdfad83c8e5f4299abe0d1297f7e0659a42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593906"
---
# <span data-ttu-id="27062-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="27062-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="27062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27062-102">SYNOPSIS</span></span>
<span data-ttu-id="27062-103">Azure RBAC 'de özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="27062-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="27062-104">Silinecek rol, rolün ID özelliği kullanılarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="27062-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="27062-105">Özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="27062-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27062-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27062-106">SYNTAX</span></span>

### <span data-ttu-id="27062-107">Roledefinitionıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27062-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27062-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27062-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27062-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="27062-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27062-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="27062-110">DESCRIPTION</span></span>
<span data-ttu-id="27062-111">Remove-AzureRmRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="27062-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="27062-112">Var olan özel rolün silineceği kimlik parametresini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="27062-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="27062-113">Varsayılan olarak Remove-AzureRmRoleDefinition sizden onay ister.</span><span class="sxs-lookup"><span data-stu-id="27062-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="27062-114">İstemi bastırmak için Force parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="27062-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="27062-115">Silinecek özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="27062-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="27062-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27062-116">EXAMPLES</span></span>

### <span data-ttu-id="27062-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="27062-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="27062-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="27062-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="27062-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27062-119">PARAMETERS</span></span>

### <span data-ttu-id="27062-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27062-120">-DefaultProfile</span></span>
<span data-ttu-id="27062-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="27062-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27062-122">-Force</span><span class="sxs-lookup"><span data-stu-id="27062-122">-Force</span></span>
<span data-ttu-id="27062-123">Ayarlanırsa, özel rolü silmeden önce onay istemez</span><span class="sxs-lookup"><span data-stu-id="27062-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="27062-124">-ID</span><span class="sxs-lookup"><span data-stu-id="27062-124">-Id</span></span>
<span data-ttu-id="27062-125">Silinecek rol tanımının kimliği</span><span class="sxs-lookup"><span data-stu-id="27062-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="27062-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27062-126">-InputObject</span></span>
<span data-ttu-id="27062-127">Kaldırılacak rol tanımını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="27062-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="27062-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="27062-128">-Name</span></span>
<span data-ttu-id="27062-129">Silinecek rol tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="27062-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="27062-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="27062-130">-PassThru</span></span>
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

### <span data-ttu-id="27062-131">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="27062-131">-Scope</span></span>
<span data-ttu-id="27062-132">Rol tanımı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="27062-132">Role definition scope.</span></span>

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

### <span data-ttu-id="27062-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="27062-133">-Confirm</span></span>
<span data-ttu-id="27062-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27062-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27062-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27062-135">-WhatIf</span></span>
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

### <span data-ttu-id="27062-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27062-136">CommonParameters</span></span>
<span data-ttu-id="27062-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27062-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27062-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27062-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27062-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27062-139">INPUTS</span></span>

### <span data-ttu-id="27062-140">System. Guid</span><span class="sxs-lookup"><span data-stu-id="27062-140">System.Guid</span></span>

### <span data-ttu-id="27062-141">System. String</span><span class="sxs-lookup"><span data-stu-id="27062-141">System.String</span></span>

### <span data-ttu-id="27062-142">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="27062-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="27062-143">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="27062-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="27062-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27062-144">OUTPUTS</span></span>

### <span data-ttu-id="27062-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27062-145">System.Boolean</span></span>

## <span data-ttu-id="27062-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27062-146">NOTES</span></span>
<span data-ttu-id="27062-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="27062-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="27062-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27062-148">RELATED LINKS</span></span>

[<span data-ttu-id="27062-149">Yeni-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="27062-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="27062-150">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="27062-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="27062-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="27062-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

