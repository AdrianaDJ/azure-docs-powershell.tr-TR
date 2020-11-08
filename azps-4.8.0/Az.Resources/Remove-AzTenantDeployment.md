---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: ae9257860a54943dfe262d1574f834404ae0e3ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266413"
---
# <span data-ttu-id="51132-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="51132-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="51132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51132-102">SYNOPSIS</span></span>
<span data-ttu-id="51132-103">Kiracı kapsamındaki bir dağıtımı ve ilişkili işlemleri kaldırır</span><span class="sxs-lookup"><span data-stu-id="51132-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="51132-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51132-104">SYNTAX</span></span>

### <span data-ttu-id="51132-105">RemoveByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51132-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51132-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="51132-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51132-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="51132-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51132-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="51132-108">DESCRIPTION</span></span>
<span data-ttu-id="51132-109">**Remove-AzTenantDeployment** cmdlet 'i geçerli kiracı kapsamındaki bir Azure dağıtımını ve ilişkili işlemleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51132-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="51132-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51132-110">EXAMPLES</span></span>

### <span data-ttu-id="51132-111">Örnek 1: verilen bir ada sahip bir dağıtımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="51132-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="51132-112">Bu komut, geçerli kiracı kapsamındaki "RolesDeployment" dağıtımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51132-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="51132-113">Örnek 2: bir dağıtım alın ve kaldırın</span><span class="sxs-lookup"><span data-stu-id="51132-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="51132-114">Bu komut, geçerli kiracı kapsamındaki "RolesDeployment" dağıtımını alır ve kaldırır.</span><span class="sxs-lookup"><span data-stu-id="51132-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="51132-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51132-115">PARAMETERS</span></span>

### <span data-ttu-id="51132-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="51132-116">-ApiVersion</span></span>
<span data-ttu-id="51132-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="51132-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="51132-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="51132-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="51132-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="51132-119">-AsJob</span></span>
<span data-ttu-id="51132-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="51132-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51132-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51132-121">-DefaultProfile</span></span>
<span data-ttu-id="51132-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51132-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51132-123">-ID</span><span class="sxs-lookup"><span data-stu-id="51132-123">-Id</span></span>
<span data-ttu-id="51132-124">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="51132-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="51132-125">Örnek:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="51132-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="51132-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51132-126">-InputObject</span></span>
<span data-ttu-id="51132-127">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="51132-127">The deployment object.</span></span>

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

### <span data-ttu-id="51132-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="51132-128">-Name</span></span>
<span data-ttu-id="51132-129">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="51132-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51132-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="51132-130">-PassThru</span></span>
<span data-ttu-id="51132-131">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="51132-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="51132-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="51132-132">-Pre</span></span>
<span data-ttu-id="51132-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51132-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="51132-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="51132-134">-Confirm</span></span>
<span data-ttu-id="51132-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51132-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51132-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51132-136">-WhatIf</span></span>
<span data-ttu-id="51132-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51132-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51132-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="51132-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51132-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51132-139">CommonParameters</span></span>
<span data-ttu-id="51132-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51132-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51132-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="51132-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51132-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51132-142">INPUTS</span></span>

### <span data-ttu-id="51132-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="51132-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="51132-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51132-144">OUTPUTS</span></span>

### <span data-ttu-id="51132-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51132-145">System.Boolean</span></span>

## <span data-ttu-id="51132-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51132-146">NOTES</span></span>

## <span data-ttu-id="51132-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51132-147">RELATED LINKS</span></span>
