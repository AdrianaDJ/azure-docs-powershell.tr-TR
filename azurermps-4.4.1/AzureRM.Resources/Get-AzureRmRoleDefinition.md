---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: 4c4bbd9dd845caa263f5dd333228d71e3f2e65b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763330"
---
# <span data-ttu-id="e8c3c-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e8c3c-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="e8c3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c3c-103">Ödev için kullanılabilen tüm Azure RBAC rollerini listeler.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8c3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8c3c-104">SYNTAX</span></span>

### <span data-ttu-id="e8c3c-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8c3c-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8c3c-106">Roledefinitionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e8c3c-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8c3c-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8c3c-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8c3c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8c3c-108">DESCRIPTION</span></span>
<span data-ttu-id="e8c3c-109">Ayrıntılarını görüntülemek için Get-AzureRmRoleDefinition komutunu belirli bir rol adıyla birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="e8c3c-110">Rolün erişim verdiği tek tek işlemleri denetlemek için, rolün eylemlerini ve NotActions özelliklerini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="e8c3c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8c3c-111">EXAMPLES</span></span>

### <span data-ttu-id="e8c3c-112">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e8c3c-112">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="e8c3c-113">Okuyucu rol tanımını alma</span><span class="sxs-lookup"><span data-stu-id="e8c3c-113">Get the Reader role definition</span></span>

### <span data-ttu-id="e8c3c-114">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e8c3c-114">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="e8c3c-115">Tüm RBAC rol tanımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="e8c3c-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="e8c3c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8c3c-116">PARAMETERS</span></span>

### <span data-ttu-id="e8c3c-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="e8c3c-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="e8c3c-118">Belirtilmişse, tüm rol tanımlarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-118">If specified, displays all role definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8c3c-119">-Özel</span><span class="sxs-lookup"><span data-stu-id="e8c3c-119">-Custom</span></span>
<span data-ttu-id="e8c3c-120">Belirtilmişse, yalnızca dizindeki özel oluşturulmuş rolleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-120">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="e8c3c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e8c3c-121">-Id</span></span>
<span data-ttu-id="e8c3c-122">Rol tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-122">Role definition Id.</span></span>

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

### <span data-ttu-id="e8c3c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8c3c-123">-Name</span></span>
<span data-ttu-id="e8c3c-124">Rol tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-124">Role definition name.</span></span>
<span data-ttu-id="e8c3c-125">Örneğin, okuyucu, katılımcı, sanal makine katılımcısı.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="e8c3c-126">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="e8c3c-126">-Scope</span></span>
<span data-ttu-id="e8c3c-127">Rol tanımı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-127">Role definition scope.</span></span>

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

### <span data-ttu-id="e8c3c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c3c-128">-DefaultProfile</span></span>
<span data-ttu-id="e8c3c-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8c3c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c3c-130">CommonParameters</span></span>
<span data-ttu-id="e8c3c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8c3c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c3c-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8c3c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c3c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8c3c-133">INPUTS</span></span>

### <span data-ttu-id="e8c3c-134">Dizisi</span><span class="sxs-lookup"><span data-stu-id="e8c3c-134">String</span></span>
<span data-ttu-id="e8c3c-135">' Scope ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e8c3c-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e8c3c-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8c3c-136">OUTPUTS</span></span>

### <span data-ttu-id="e8c3c-137">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition]</span><span class="sxs-lookup"><span data-stu-id="e8c3c-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="e8c3c-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8c3c-138">NOTES</span></span>
<span data-ttu-id="e8c3c-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="e8c3c-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e8c3c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8c3c-140">RELATED LINKS</span></span>

[<span data-ttu-id="e8c3c-141">Yeni-Azurermroleataması</span><span class="sxs-lookup"><span data-stu-id="e8c3c-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="e8c3c-142">Get-Azurermroleödev</span><span class="sxs-lookup"><span data-stu-id="e8c3c-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="e8c3c-143">Yeni-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e8c3c-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="e8c3c-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e8c3c-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

