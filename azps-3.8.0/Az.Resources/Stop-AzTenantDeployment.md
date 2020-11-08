---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097187"
---
# <span data-ttu-id="79160-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="79160-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="79160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79160-102">SYNOPSIS</span></span>
<span data-ttu-id="79160-103">Kiracı kapsamında çalışan bir dağıtımı iptal etme</span><span class="sxs-lookup"><span data-stu-id="79160-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="79160-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79160-104">SYNTAX</span></span>

### <span data-ttu-id="79160-105">StopByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79160-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79160-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="79160-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79160-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="79160-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79160-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="79160-108">DESCRIPTION</span></span>
<span data-ttu-id="79160-109">**Stop-AzTenantDeployment** cmdlet 'i, geçerli kiracı kapsamında başlatılmış ancak tamamlanmamış bir dağıtımı iptal eder.</span><span class="sxs-lookup"><span data-stu-id="79160-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="79160-110">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="79160-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="79160-111">Kiracı kapsamında dağıtım oluşturmak için New-AzTenantDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="79160-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="79160-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79160-112">EXAMPLES</span></span>

### <span data-ttu-id="79160-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="79160-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="79160-114">Bu komut, geçerli kiracı kapsamındaki "deployment01" çalışan dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="79160-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="79160-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="79160-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="79160-116">Bu komut, geçerli kiracı kapsamındaki "deployment01" dağıtımını alır ve iptal eder.</span><span class="sxs-lookup"><span data-stu-id="79160-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="79160-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79160-117">PARAMETERS</span></span>

### <span data-ttu-id="79160-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="79160-118">-ApiVersion</span></span>
<span data-ttu-id="79160-119">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="79160-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="79160-120">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="79160-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="79160-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79160-121">-DefaultProfile</span></span>
<span data-ttu-id="79160-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79160-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79160-123">-ID</span><span class="sxs-lookup"><span data-stu-id="79160-123">-Id</span></span>
<span data-ttu-id="79160-124">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="79160-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="79160-125">Örnek:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="79160-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79160-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79160-126">-InputObject</span></span>
<span data-ttu-id="79160-127">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="79160-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79160-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="79160-128">-Name</span></span>
<span data-ttu-id="79160-129">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="79160-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79160-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="79160-130">-PassThru</span></span>
<span data-ttu-id="79160-131">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="79160-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="79160-132">-Pre-</span><span class="sxs-lookup"><span data-stu-id="79160-132">-Pre</span></span>
<span data-ttu-id="79160-133">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79160-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="79160-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="79160-134">-Confirm</span></span>
<span data-ttu-id="79160-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79160-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79160-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79160-136">-WhatIf</span></span>
<span data-ttu-id="79160-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79160-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79160-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79160-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79160-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79160-139">CommonParameters</span></span>
<span data-ttu-id="79160-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79160-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79160-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="79160-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79160-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79160-142">INPUTS</span></span>

### <span data-ttu-id="79160-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="79160-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="79160-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79160-144">OUTPUTS</span></span>

### <span data-ttu-id="79160-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79160-145">System.Boolean</span></span>

## <span data-ttu-id="79160-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79160-146">NOTES</span></span>

## <span data-ttu-id="79160-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79160-147">RELATED LINKS</span></span>
