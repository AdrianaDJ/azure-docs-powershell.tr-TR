---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279821"
---
# <span data-ttu-id="db762-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="db762-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="db762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db762-102">SYNOPSIS</span></span>
<span data-ttu-id="db762-103">Kiracı kapsamındaki bir dağıtımı ve ilişkili işlemleri kaldırır</span><span class="sxs-lookup"><span data-stu-id="db762-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="db762-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db762-104">SYNTAX</span></span>

### <span data-ttu-id="db762-105">RemoveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="db762-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db762-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="db762-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db762-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="db762-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db762-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="db762-108">DESCRIPTION</span></span>
<span data-ttu-id="db762-109">**Remove-AzTenantDeployment** cmdlet 'i geçerli kiracı kapsamındaki bir Azure dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="db762-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="db762-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db762-110">EXAMPLES</span></span>

### <span data-ttu-id="db762-111">Örnek 1: verilen bir ada sahip bir dağıtımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="db762-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="db762-112">Bu komut, geçerli kiracı kapsamındaki "RolesDeployment" dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="db762-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="db762-113">Örnek 2: bir dağıtım alın ve kaldırın</span><span class="sxs-lookup"><span data-stu-id="db762-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="db762-114">Bu komut, geçerli kiracı kapsamındaki "RolesDeployment" dağıtımını alır ve kaldırır.</span><span class="sxs-lookup"><span data-stu-id="db762-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="db762-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db762-115">PARAMETERS</span></span>

### <span data-ttu-id="db762-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="db762-116">-AsJob</span></span>
<span data-ttu-id="db762-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="db762-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db762-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db762-118">-DefaultProfile</span></span>
<span data-ttu-id="db762-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db762-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db762-120">-ID</span><span class="sxs-lookup"><span data-stu-id="db762-120">-Id</span></span>
<span data-ttu-id="db762-121">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="db762-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="db762-122">Örnek:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="db762-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="db762-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db762-123">-InputObject</span></span>
<span data-ttu-id="db762-124">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="db762-124">The deployment object.</span></span>

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

### <span data-ttu-id="db762-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="db762-125">-Name</span></span>
<span data-ttu-id="db762-126">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="db762-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db762-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="db762-127">-PassThru</span></span>
<span data-ttu-id="db762-128">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="db762-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="db762-129">-Pre-</span><span class="sxs-lookup"><span data-stu-id="db762-129">-Pre</span></span>
<span data-ttu-id="db762-130">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db762-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="db762-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="db762-131">-Confirm</span></span>
<span data-ttu-id="db762-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db762-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db762-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db762-133">-WhatIf</span></span>
<span data-ttu-id="db762-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db762-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db762-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db762-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db762-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db762-136">CommonParameters</span></span>
<span data-ttu-id="db762-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db762-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db762-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="db762-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db762-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db762-139">INPUTS</span></span>

### <span data-ttu-id="db762-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="db762-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="db762-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db762-141">OUTPUTS</span></span>

### <span data-ttu-id="db762-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db762-142">System.Boolean</span></span>

## <span data-ttu-id="db762-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db762-143">NOTES</span></span>

## <span data-ttu-id="db762-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db762-144">RELATED LINKS</span></span>
