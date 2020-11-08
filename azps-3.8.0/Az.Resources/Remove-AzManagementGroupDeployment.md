---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097247"
---
# <span data-ttu-id="c6028-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c6028-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="c6028-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6028-102">SYNOPSIS</span></span>
<span data-ttu-id="c6028-103">Yönetim grubundaki bir dağıtımı ve ilişkili işlemleri kaldırır</span><span class="sxs-lookup"><span data-stu-id="c6028-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="c6028-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6028-104">SYNTAX</span></span>

### <span data-ttu-id="c6028-105">RemoveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c6028-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6028-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c6028-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6028-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c6028-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6028-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6028-108">DESCRIPTION</span></span>
<span data-ttu-id="c6028-109">**Remove-AzManagementGroupDeployment** cmdlet 'i, bir yönetim grubundaki bir Azure dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c6028-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="c6028-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6028-110">EXAMPLES</span></span>

### <span data-ttu-id="c6028-111">Örnek 1: verilen bir ada sahip bir dağıtımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="c6028-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="c6028-112">Bu komut, "myMG" yönetim grubundaki "RolesDeployment" dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c6028-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="c6028-113">Örnek 2: bir dağıtım alın ve kaldırın</span><span class="sxs-lookup"><span data-stu-id="c6028-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="c6028-114">Bu komut, "myMG" yönetim grubundaki "RolesDeployment" dağıtımını alır ve kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c6028-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="c6028-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6028-115">PARAMETERS</span></span>

### <span data-ttu-id="c6028-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c6028-116">-ApiVersion</span></span>
<span data-ttu-id="c6028-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6028-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c6028-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c6028-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6028-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="c6028-119">-AsJob</span></span>
<span data-ttu-id="c6028-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c6028-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6028-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6028-121">-DefaultProfile</span></span>
<span data-ttu-id="c6028-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6028-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6028-123">-ID</span><span class="sxs-lookup"><span data-stu-id="c6028-123">-Id</span></span>
<span data-ttu-id="c6028-124">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c6028-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c6028-125">Örnek:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c6028-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6028-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6028-126">-InputObject</span></span>
<span data-ttu-id="c6028-127">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c6028-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6028-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c6028-128">-ManagementGroupId</span></span>
<span data-ttu-id="c6028-129">Yönetim grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="c6028-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6028-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6028-130">-Name</span></span>
<span data-ttu-id="c6028-131">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="c6028-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6028-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c6028-132">-PassThru</span></span>
<span data-ttu-id="c6028-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c6028-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c6028-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c6028-134">-Pre</span></span>
<span data-ttu-id="c6028-135">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6028-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c6028-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6028-136">-Confirm</span></span>
<span data-ttu-id="c6028-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6028-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6028-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6028-138">-WhatIf</span></span>
<span data-ttu-id="c6028-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6028-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6028-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6028-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6028-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6028-141">CommonParameters</span></span>
<span data-ttu-id="c6028-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6028-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6028-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c6028-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6028-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6028-144">INPUTS</span></span>

### <span data-ttu-id="c6028-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="c6028-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c6028-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6028-146">OUTPUTS</span></span>

### <span data-ttu-id="c6028-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6028-147">System.Boolean</span></span>

## <span data-ttu-id="c6028-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6028-148">NOTES</span></span>

## <span data-ttu-id="c6028-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6028-149">RELATED LINKS</span></span>
