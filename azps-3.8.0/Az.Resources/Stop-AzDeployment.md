---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 366bbdf03b5fc7a23e6b71e03e1c3f1652925e7b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097242"
---
# <span data-ttu-id="0146d-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0146d-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="0146d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0146d-102">SYNOPSIS</span></span>
<span data-ttu-id="0146d-103">Çalışan bir dağıtımı iptal etme</span><span class="sxs-lookup"><span data-stu-id="0146d-103">Cancel a running deployment</span></span>

## <span data-ttu-id="0146d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0146d-104">SYNTAX</span></span>

### <span data-ttu-id="0146d-105">StopByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0146d-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0146d-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0146d-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0146d-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="0146d-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0146d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0146d-108">DESCRIPTION</span></span>
<span data-ttu-id="0146d-109">**Stop-AzDeployment** cmdlet 'i, başlatılmış ancak tamamlanmamış olan abonelik kapsamındaki bir dağıtımı iptal eder.</span><span class="sxs-lookup"><span data-stu-id="0146d-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="0146d-110">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0146d-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="0146d-111">Abonelik kapsamında dağıtım oluşturmak için New-AzDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0146d-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="0146d-112">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="0146d-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="0146d-113">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0146d-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="0146d-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0146d-114">EXAMPLES</span></span>

### <span data-ttu-id="0146d-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0146d-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="0146d-116">Bu komut, geçerli abonelik kapsamında çalışan "deployment01" dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="0146d-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="0146d-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0146d-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="0146d-118">Bu komut, geçerli abonelik kapsamındaki "deployment01" dağıtımını alır ve iptal eder.</span><span class="sxs-lookup"><span data-stu-id="0146d-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="0146d-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0146d-119">PARAMETERS</span></span>

### <span data-ttu-id="0146d-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="0146d-120">-ApiVersion</span></span>
<span data-ttu-id="0146d-121">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="0146d-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0146d-122">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0146d-122">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0146d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0146d-123">-DefaultProfile</span></span>
<span data-ttu-id="0146d-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0146d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0146d-125">-ID</span><span class="sxs-lookup"><span data-stu-id="0146d-125">-Id</span></span>
<span data-ttu-id="0146d-126">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0146d-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0146d-127">Örnek:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0146d-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0146d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0146d-128">-InputObject</span></span>
<span data-ttu-id="0146d-129">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0146d-129">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0146d-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="0146d-130">-Name</span></span>
<span data-ttu-id="0146d-131">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="0146d-131">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0146d-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0146d-132">-PassThru</span></span>
<span data-ttu-id="0146d-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="0146d-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0146d-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="0146d-134">-Pre</span></span>
<span data-ttu-id="0146d-135">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0146d-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0146d-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0146d-136">-Confirm</span></span>
<span data-ttu-id="0146d-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0146d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0146d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0146d-138">-WhatIf</span></span>
<span data-ttu-id="0146d-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0146d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0146d-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0146d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0146d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0146d-141">CommonParameters</span></span>
<span data-ttu-id="0146d-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0146d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0146d-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0146d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0146d-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0146d-144">INPUTS</span></span>

### <span data-ttu-id="0146d-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="0146d-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0146d-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0146d-146">OUTPUTS</span></span>

### <span data-ttu-id="0146d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0146d-147">System.Boolean</span></span>

## <span data-ttu-id="0146d-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0146d-148">NOTES</span></span>

## <span data-ttu-id="0146d-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0146d-149">RELATED LINKS</span></span>
