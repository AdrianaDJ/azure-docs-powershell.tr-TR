---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322372"
---
# <span data-ttu-id="c2805-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c2805-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="c2805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2805-102">SYNOPSIS</span></span>
<span data-ttu-id="c2805-103">Yönetim grubundaki bir dağıtımı ve ilişkili işlemleri kaldırır</span><span class="sxs-lookup"><span data-stu-id="c2805-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="c2805-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2805-104">SYNTAX</span></span>

### <span data-ttu-id="c2805-105">RemoveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2805-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2805-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c2805-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2805-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2805-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2805-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2805-108">DESCRIPTION</span></span>
<span data-ttu-id="c2805-109">**Remove-AzManagementGroupDeployment** cmdlet 'i, bir yönetim grubundaki bir Azure dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c2805-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="c2805-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2805-110">EXAMPLES</span></span>

### <span data-ttu-id="c2805-111">Örnek 1: verilen bir ada sahip bir dağıtımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="c2805-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="c2805-112">Bu komut, "myMG" yönetim grubundaki "RolesDeployment" dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c2805-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="c2805-113">Örnek 2: bir dağıtım alın ve kaldırın</span><span class="sxs-lookup"><span data-stu-id="c2805-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="c2805-114">Bu komut, "myMG" yönetim grubundaki "RolesDeployment" dağıtımını alır ve kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c2805-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="c2805-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2805-115">PARAMETERS</span></span>

### <span data-ttu-id="c2805-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="c2805-116">-AsJob</span></span>
<span data-ttu-id="c2805-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c2805-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2805-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2805-118">-DefaultProfile</span></span>
<span data-ttu-id="c2805-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2805-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2805-120">-ID</span><span class="sxs-lookup"><span data-stu-id="c2805-120">-Id</span></span>
<span data-ttu-id="c2805-121">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c2805-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c2805-122">Örnek:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c2805-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2805-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2805-123">-InputObject</span></span>
<span data-ttu-id="c2805-124">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c2805-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2805-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c2805-125">-ManagementGroupId</span></span>
<span data-ttu-id="c2805-126">Yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="c2805-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2805-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2805-127">-Name</span></span>
<span data-ttu-id="c2805-128">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="c2805-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2805-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c2805-129">-PassThru</span></span>
<span data-ttu-id="c2805-130">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c2805-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c2805-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c2805-131">-Pre</span></span>
<span data-ttu-id="c2805-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2805-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c2805-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2805-133">-Confirm</span></span>
<span data-ttu-id="c2805-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2805-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2805-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2805-135">-WhatIf</span></span>
<span data-ttu-id="c2805-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2805-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2805-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2805-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2805-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2805-138">CommonParameters</span></span>
<span data-ttu-id="c2805-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2805-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2805-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c2805-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2805-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2805-141">INPUTS</span></span>

### <span data-ttu-id="c2805-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="c2805-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c2805-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2805-143">OUTPUTS</span></span>

### <span data-ttu-id="c2805-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2805-144">System.Boolean</span></span>

## <span data-ttu-id="c2805-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2805-145">NOTES</span></span>

## <span data-ttu-id="c2805-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2805-146">RELATED LINKS</span></span>
