---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: d43ec874af02d57abedddb1b49b3cc8723af5c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936421"
---
# <span data-ttu-id="24279-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24279-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="24279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24279-102">SYNOPSIS</span></span>
<span data-ttu-id="24279-103">Ödev için kullanılabilen tüm Azure RBAC rollerini listeler.</span><span class="sxs-lookup"><span data-stu-id="24279-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="24279-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24279-104">SYNTAX</span></span>

### <span data-ttu-id="24279-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24279-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24279-106">Roledefinitionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="24279-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24279-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="24279-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24279-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="24279-108">DESCRIPTION</span></span>
<span data-ttu-id="24279-109">Ayrıntılarını görüntülemek için Get-AzRoleDefinition komutunu belirli bir rol adıyla birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="24279-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="24279-110">Rolün erişim verdiği tek tek işlemleri denetlemek için, rolün eylemlerini ve NotActions özelliklerini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="24279-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="24279-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24279-111">EXAMPLES</span></span>

### <span data-ttu-id="24279-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="24279-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="24279-113">Okuyucu rol tanımını alma</span><span class="sxs-lookup"><span data-stu-id="24279-113">Get the Reader role definition</span></span>

### <span data-ttu-id="24279-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="24279-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="24279-115">Tüm RBAC rol tanımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="24279-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="24279-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24279-116">PARAMETERS</span></span>

### <span data-ttu-id="24279-117">-Özel</span><span class="sxs-lookup"><span data-stu-id="24279-117">-Custom</span></span>
<span data-ttu-id="24279-118">Belirtilmişse, yalnızca dizindeki özel oluşturulmuş rolleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="24279-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="24279-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24279-119">-DefaultProfile</span></span>
<span data-ttu-id="24279-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="24279-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24279-121">-ID</span><span class="sxs-lookup"><span data-stu-id="24279-121">-Id</span></span>
<span data-ttu-id="24279-122">Rol tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="24279-122">Role definition Id.</span></span>

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

### <span data-ttu-id="24279-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="24279-123">-Name</span></span>
<span data-ttu-id="24279-124">Rol tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="24279-124">Role definition name.</span></span>
<span data-ttu-id="24279-125">Örneğin, okuyucu, katılımcı, sanal makine katılımcısı.</span><span class="sxs-lookup"><span data-stu-id="24279-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="24279-126">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="24279-126">-Scope</span></span>
<span data-ttu-id="24279-127">Rol tanımı kapsamı.</span><span class="sxs-lookup"><span data-stu-id="24279-127">Role definition scope.</span></span>

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

### <span data-ttu-id="24279-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24279-128">CommonParameters</span></span>
<span data-ttu-id="24279-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24279-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24279-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24279-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24279-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24279-131">INPUTS</span></span>

### <span data-ttu-id="24279-132">System. String</span><span class="sxs-lookup"><span data-stu-id="24279-132">System.String</span></span>
<span data-ttu-id="24279-133">Parametreler: Scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24279-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="24279-134">System. Guid</span><span class="sxs-lookup"><span data-stu-id="24279-134">System.Guid</span></span>

### <span data-ttu-id="24279-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="24279-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24279-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24279-136">OUTPUTS</span></span>

### <span data-ttu-id="24279-137">Microsoft. Azure. Commands. resources. modeller. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24279-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="24279-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24279-138">NOTES</span></span>
<span data-ttu-id="24279-139">Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="24279-139">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="24279-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24279-140">RELATED LINKS</span></span>

[<span data-ttu-id="24279-141">Yeni-Azrol ataması</span><span class="sxs-lookup"><span data-stu-id="24279-141">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="24279-142">Get-Azrol ataması</span><span class="sxs-lookup"><span data-stu-id="24279-142">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="24279-143">Yeni-Azrol tanımı</span><span class="sxs-lookup"><span data-stu-id="24279-143">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="24279-144">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="24279-144">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

