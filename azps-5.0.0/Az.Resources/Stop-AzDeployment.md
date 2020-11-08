---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277034"
---
# <span data-ttu-id="27cbf-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="27cbf-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="27cbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="27cbf-103">Çalışan bir dağıtımı iptal etme</span><span class="sxs-lookup"><span data-stu-id="27cbf-103">Cancel a running deployment</span></span>

## <span data-ttu-id="27cbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27cbf-104">SYNTAX</span></span>

### <span data-ttu-id="27cbf-105">StopByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27cbf-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27cbf-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="27cbf-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27cbf-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="27cbf-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27cbf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="27cbf-108">DESCRIPTION</span></span>
<span data-ttu-id="27cbf-109">**Stop-AzDeployment** cmdlet 'i, başlatılmış ancak tamamlanmamış olan abonelik kapsamındaki bir dağıtımı iptal eder.</span><span class="sxs-lookup"><span data-stu-id="27cbf-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="27cbf-110">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="27cbf-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="27cbf-111">Abonelik kapsamında dağıtım oluşturmak için New-AzDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="27cbf-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="27cbf-112">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="27cbf-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="27cbf-113">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="27cbf-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="27cbf-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27cbf-114">EXAMPLES</span></span>

### <span data-ttu-id="27cbf-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="27cbf-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="27cbf-116">Bu komut, geçerli abonelik kapsamında çalışan "deployment01" dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="27cbf-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="27cbf-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="27cbf-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="27cbf-118">Bu komut, geçerli abonelik kapsamındaki "deployment01" dağıtımını alır ve iptal eder.</span><span class="sxs-lookup"><span data-stu-id="27cbf-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="27cbf-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27cbf-119">PARAMETERS</span></span>

### <span data-ttu-id="27cbf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27cbf-120">-DefaultProfile</span></span>
<span data-ttu-id="27cbf-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27cbf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27cbf-122">-ID</span><span class="sxs-lookup"><span data-stu-id="27cbf-122">-Id</span></span>
<span data-ttu-id="27cbf-123">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="27cbf-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="27cbf-124">Örnek:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="27cbf-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="27cbf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27cbf-125">-InputObject</span></span>
<span data-ttu-id="27cbf-126">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="27cbf-126">The deployment object.</span></span>

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

### <span data-ttu-id="27cbf-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="27cbf-127">-Name</span></span>
<span data-ttu-id="27cbf-128">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="27cbf-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="27cbf-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="27cbf-129">-PassThru</span></span>
<span data-ttu-id="27cbf-130">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="27cbf-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="27cbf-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="27cbf-131">-Pre</span></span>
<span data-ttu-id="27cbf-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27cbf-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="27cbf-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="27cbf-133">-Confirm</span></span>
<span data-ttu-id="27cbf-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27cbf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27cbf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27cbf-135">-WhatIf</span></span>
<span data-ttu-id="27cbf-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27cbf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27cbf-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="27cbf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27cbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cbf-138">CommonParameters</span></span>
<span data-ttu-id="27cbf-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27cbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cbf-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="27cbf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cbf-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27cbf-141">INPUTS</span></span>

### <span data-ttu-id="27cbf-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="27cbf-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="27cbf-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27cbf-143">OUTPUTS</span></span>

### <span data-ttu-id="27cbf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27cbf-144">System.Boolean</span></span>

## <span data-ttu-id="27cbf-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27cbf-145">NOTES</span></span>

## <span data-ttu-id="27cbf-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27cbf-146">RELATED LINKS</span></span>
