---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: f31a09f0d148d25796e157eb300a6f5918dade44
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936335"
---
# <span data-ttu-id="df4bb-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="df4bb-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="df4bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="df4bb-103">Azure RBAC 'de özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="df4bb-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="df4bb-104">Silinecek rol, rolün ID özelliği kullanılarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="df4bb-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="df4bb-105">Özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="df4bb-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="df4bb-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df4bb-106">SYNTAX</span></span>

### <span data-ttu-id="df4bb-107">Roledefinitionıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="df4bb-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4bb-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="df4bb-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4bb-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="df4bb-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df4bb-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="df4bb-110">DESCRIPTION</span></span>
<span data-ttu-id="df4bb-111">Remove-AzRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="df4bb-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="df4bb-112">Var olan özel rolün silineceği kimlik parametresini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="df4bb-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="df4bb-113">Varsayılan olarak Remove-AzRoleDefinition sizden onay ister.</span><span class="sxs-lookup"><span data-stu-id="df4bb-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="df4bb-114">İstemi bastırmak için Force parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="df4bb-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="df4bb-115">Silinecek özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="df4bb-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="df4bb-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df4bb-116">EXAMPLES</span></span>

### <span data-ttu-id="df4bb-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="df4bb-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="df4bb-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="df4bb-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="df4bb-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df4bb-119">PARAMETERS</span></span>

### <span data-ttu-id="df4bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4bb-120">-DefaultProfile</span></span>
<span data-ttu-id="df4bb-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="df4bb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4bb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="df4bb-122">-Force</span></span>
<span data-ttu-id="df4bb-123">Ayarlanırsa, özel rolü silmeden önce onay istemez</span><span class="sxs-lookup"><span data-stu-id="df4bb-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="df4bb-124">-ID</span><span class="sxs-lookup"><span data-stu-id="df4bb-124">-Id</span></span>
<span data-ttu-id="df4bb-125">Silinecek rol tanımının kimliği</span><span class="sxs-lookup"><span data-stu-id="df4bb-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="df4bb-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df4bb-126">-InputObject</span></span>
<span data-ttu-id="df4bb-127">Kaldırılacak rol tanımını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="df4bb-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="df4bb-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="df4bb-128">-Name</span></span>
<span data-ttu-id="df4bb-129">Silinecek rol tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="df4bb-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="df4bb-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="df4bb-130">-PassThru</span></span>
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

### <span data-ttu-id="df4bb-131">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="df4bb-131">-Scope</span></span>
<span data-ttu-id="df4bb-132">Rol tanımı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="df4bb-132">Role definition scope.</span></span>

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

### <span data-ttu-id="df4bb-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="df4bb-133">-Confirm</span></span>
<span data-ttu-id="df4bb-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df4bb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df4bb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df4bb-135">-WhatIf</span></span>
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

### <span data-ttu-id="df4bb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4bb-136">CommonParameters</span></span>
<span data-ttu-id="df4bb-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df4bb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4bb-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df4bb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4bb-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df4bb-139">INPUTS</span></span>

### <span data-ttu-id="df4bb-140">System. Guid</span><span class="sxs-lookup"><span data-stu-id="df4bb-140">System.Guid</span></span>

### <span data-ttu-id="df4bb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="df4bb-141">System.String</span></span>

### <span data-ttu-id="df4bb-142">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="df4bb-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="df4bb-143">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="df4bb-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="df4bb-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df4bb-144">OUTPUTS</span></span>

### <span data-ttu-id="df4bb-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df4bb-145">System.Boolean</span></span>

## <span data-ttu-id="df4bb-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df4bb-146">NOTES</span></span>
<span data-ttu-id="df4bb-147">Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="df4bb-147">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="df4bb-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df4bb-148">RELATED LINKS</span></span>

[<span data-ttu-id="df4bb-149">Yeni-Azrol tanımı</span><span class="sxs-lookup"><span data-stu-id="df4bb-149">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="df4bb-150">Get-Azroltanımı</span><span class="sxs-lookup"><span data-stu-id="df4bb-150">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="df4bb-151">Set-Azroltanımı</span><span class="sxs-lookup"><span data-stu-id="df4bb-151">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

