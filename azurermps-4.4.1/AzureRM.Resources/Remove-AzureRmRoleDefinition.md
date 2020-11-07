---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 476555b271d58f8e594f0cae1422bcdde1fc46e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763321"
---
# <span data-ttu-id="20435-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20435-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="20435-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20435-102">SYNOPSIS</span></span>
<span data-ttu-id="20435-103">Azure RBAC 'de özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="20435-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="20435-104">Silinecek rol, rolün ID özelliği kullanılarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="20435-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="20435-105">Özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="20435-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20435-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20435-106">SYNTAX</span></span>

### <span data-ttu-id="20435-107">Roledefinitionıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="20435-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20435-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="20435-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20435-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="20435-109">DESCRIPTION</span></span>
<span data-ttu-id="20435-110">Remove-AzureRmRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="20435-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="20435-111">Var olan özel rolün silineceği kimlik parametresini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="20435-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="20435-112">Varsayılan olarak Remove-AzureRmRoleDefinition sizden onay ister.</span><span class="sxs-lookup"><span data-stu-id="20435-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="20435-113">İstemi bastırmak için Force parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="20435-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="20435-114">Silinecek özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="20435-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="20435-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20435-115">EXAMPLES</span></span>

### <span data-ttu-id="20435-116">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="20435-116">--------------------------  Example 1  --------------------------</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="20435-117">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="20435-117">--------------------------  Example 2  --------------------------</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="20435-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20435-118">PARAMETERS</span></span>

### <span data-ttu-id="20435-119">-Force</span><span class="sxs-lookup"><span data-stu-id="20435-119">-Force</span></span>
<span data-ttu-id="20435-120">Ayarlanırsa, özel rolü silmeden önce onay istemez</span><span class="sxs-lookup"><span data-stu-id="20435-120">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="20435-121">-ID</span><span class="sxs-lookup"><span data-stu-id="20435-121">-Id</span></span>
<span data-ttu-id="20435-122">Silinecek rol tanımının kimliği</span><span class="sxs-lookup"><span data-stu-id="20435-122">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="20435-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="20435-123">-Name</span></span>
<span data-ttu-id="20435-124">Silinecek rol tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="20435-124">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="20435-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="20435-125">-PassThru</span></span>
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

### <span data-ttu-id="20435-126">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="20435-126">-Scope</span></span>
<span data-ttu-id="20435-127">Rol tanımı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="20435-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20435-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="20435-128">-Confirm</span></span>
<span data-ttu-id="20435-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="20435-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20435-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20435-130">-WhatIf</span></span>
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

### <span data-ttu-id="20435-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20435-131">-DefaultProfile</span></span>
<span data-ttu-id="20435-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20435-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20435-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20435-133">CommonParameters</span></span>
<span data-ttu-id="20435-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20435-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20435-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20435-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20435-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20435-136">INPUTS</span></span>

## <span data-ttu-id="20435-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20435-137">OUTPUTS</span></span>

### <span data-ttu-id="20435-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20435-138">System.Boolean</span></span>

## <span data-ttu-id="20435-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20435-139">NOTES</span></span>
<span data-ttu-id="20435-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="20435-140">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="20435-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20435-141">RELATED LINKS</span></span>

[<span data-ttu-id="20435-142">Yeni-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20435-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="20435-143">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20435-143">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="20435-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="20435-144">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

