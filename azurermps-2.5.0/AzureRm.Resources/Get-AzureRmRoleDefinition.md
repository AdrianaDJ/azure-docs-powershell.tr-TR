---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 219ff64309cc11fd5e65d614f67d2d531737c8b1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939680"
---
# <span data-ttu-id="9470d-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9470d-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="9470d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9470d-102">SYNOPSIS</span></span>
<span data-ttu-id="9470d-103">Ödev için kullanılabilen tüm Azure RBAC rollerini listeler.</span><span class="sxs-lookup"><span data-stu-id="9470d-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9470d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9470d-104">SYNTAX</span></span>

### <span data-ttu-id="9470d-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9470d-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9470d-106">Roledefinitionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9470d-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9470d-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="9470d-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9470d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9470d-108">DESCRIPTION</span></span>
<span data-ttu-id="9470d-109">Ayrıntılarını görüntülemek için Get-AzureRmRoleDefinition komutunu belirli bir rol adıyla birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="9470d-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="9470d-110">Rolün erişim verdiği tek tek işlemleri denetlemek için, rolün eylemlerini ve NotActions özelliklerini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="9470d-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="9470d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9470d-111">EXAMPLES</span></span>

### <span data-ttu-id="9470d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9470d-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="9470d-113">Okuyucu rol tanımını alma</span><span class="sxs-lookup"><span data-stu-id="9470d-113">Get the Reader role definition</span></span>

### <span data-ttu-id="9470d-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9470d-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="9470d-115">Tüm RBAC rol tanımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="9470d-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="9470d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9470d-116">PARAMETERS</span></span>

### <span data-ttu-id="9470d-117">-Özel</span><span class="sxs-lookup"><span data-stu-id="9470d-117">-Custom</span></span>
<span data-ttu-id="9470d-118">Belirtilmişse, yalnızca dizindeki özel oluşturulmuş rolleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="9470d-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9470d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9470d-119">-DefaultProfile</span></span>
<span data-ttu-id="9470d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9470d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9470d-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9470d-121">-Id</span></span>
<span data-ttu-id="9470d-122">Rol tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="9470d-122">Role definition Id.</span></span>

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

### <span data-ttu-id="9470d-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="9470d-123">-Name</span></span>
<span data-ttu-id="9470d-124">Rol tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="9470d-124">Role definition name.</span></span>
<span data-ttu-id="9470d-125">Örneğin, okuyucu, katılımcı, sanal makine katılımcısı.</span><span class="sxs-lookup"><span data-stu-id="9470d-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9470d-126">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="9470d-126">-Scope</span></span>
<span data-ttu-id="9470d-127">Rol tanımı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="9470d-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9470d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9470d-128">CommonParameters</span></span>
<span data-ttu-id="9470d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9470d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9470d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9470d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9470d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9470d-131">INPUTS</span></span>

### <span data-ttu-id="9470d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9470d-132">System.String</span></span>
<span data-ttu-id="9470d-133">Parametreler: Scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9470d-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="9470d-134">System. Guid</span><span class="sxs-lookup"><span data-stu-id="9470d-134">System.Guid</span></span>

### <span data-ttu-id="9470d-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9470d-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9470d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9470d-136">OUTPUTS</span></span>

### <span data-ttu-id="9470d-137">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9470d-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="9470d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9470d-138">NOTES</span></span>
<span data-ttu-id="9470d-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="9470d-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9470d-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9470d-140">RELATED LINKS</span></span>

[<span data-ttu-id="9470d-141">Yeni-Azurermroleataması</span><span class="sxs-lookup"><span data-stu-id="9470d-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="9470d-142">Get-Azurermroleödev</span><span class="sxs-lookup"><span data-stu-id="9470d-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="9470d-143">Yeni-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9470d-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="9470d-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9470d-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

