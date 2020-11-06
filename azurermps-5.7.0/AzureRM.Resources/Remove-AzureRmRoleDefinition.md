---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: ae4f8e11ac213943d8cfcec162b43abde60fe753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593437"
---
# <span data-ttu-id="971f6-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="971f6-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="971f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="971f6-102">SYNOPSIS</span></span>
<span data-ttu-id="971f6-103">Azure RBAC 'de özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="971f6-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="971f6-104">Silinecek rol, rolün ID özelliği kullanılarak belirtilir.</span><span class="sxs-lookup"><span data-stu-id="971f6-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="971f6-105">Özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="971f6-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="971f6-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="971f6-106">SYNTAX</span></span>

### <span data-ttu-id="971f6-107">Roledefinitionıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="971f6-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="971f6-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="971f6-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="971f6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="971f6-109">DESCRIPTION</span></span>
<span data-ttu-id="971f6-110">Remove-AzureRmRoleDefinition cmdlet 'i Azure Role-Based erişim denetiminde özel bir rol siler.</span><span class="sxs-lookup"><span data-stu-id="971f6-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="971f6-111">Var olan özel rolün silineceği kimlik parametresini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="971f6-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="971f6-112">Varsayılan olarak Remove-AzureRmRoleDefinition sizden onay ister.</span><span class="sxs-lookup"><span data-stu-id="971f6-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="971f6-113">İstemi bastırmak için Force parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="971f6-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="971f6-114">Silinecek özel rolde yapılan rol atamaları varsa, silme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="971f6-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="971f6-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="971f6-115">EXAMPLES</span></span>

### <span data-ttu-id="971f6-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="971f6-116">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="971f6-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="971f6-117">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="971f6-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="971f6-118">PARAMETERS</span></span>

### <span data-ttu-id="971f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971f6-119">-DefaultProfile</span></span>
<span data-ttu-id="971f6-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="971f6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971f6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="971f6-121">-Force</span></span>
<span data-ttu-id="971f6-122">Ayarlanırsa, özel rolü silmeden önce onay istemez</span><span class="sxs-lookup"><span data-stu-id="971f6-122">If set, does not prompt for a confirmation before deleting the custom role</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971f6-123">-ID</span><span class="sxs-lookup"><span data-stu-id="971f6-123">-Id</span></span>
<span data-ttu-id="971f6-124">Silinecek rol tanımının kimliği</span><span class="sxs-lookup"><span data-stu-id="971f6-124">Id of the Role definition to be deleted</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971f6-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="971f6-125">-Name</span></span>
<span data-ttu-id="971f6-126">Silinecek rol tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="971f6-126">Name of the Role definition to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971f6-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="971f6-127">-PassThru</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971f6-128">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="971f6-128">-Scope</span></span>
<span data-ttu-id="971f6-129">Rol tanımı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="971f6-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971f6-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="971f6-130">-Confirm</span></span>
<span data-ttu-id="971f6-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="971f6-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971f6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971f6-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971f6-133">CommonParameters</span></span>
<span data-ttu-id="971f6-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="971f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971f6-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="971f6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971f6-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="971f6-136">INPUTS</span></span>

### <span data-ttu-id="971f6-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="971f6-137">None</span></span>
<span data-ttu-id="971f6-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="971f6-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="971f6-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="971f6-139">OUTPUTS</span></span>

### <span data-ttu-id="971f6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="971f6-140">System.Boolean</span></span>

## <span data-ttu-id="971f6-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="971f6-141">NOTES</span></span>
<span data-ttu-id="971f6-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="971f6-142">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="971f6-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="971f6-143">RELATED LINKS</span></span>

[<span data-ttu-id="971f6-144">Yeni-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="971f6-144">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="971f6-145">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="971f6-145">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="971f6-146">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="971f6-146">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

