---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 15dc9e6a24aa78523a020af541250c5c51b32994
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759300"
---
# <span data-ttu-id="608da-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="608da-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="608da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="608da-102">SYNOPSIS</span></span>
<span data-ttu-id="608da-103">Çalışan bir dağıtım</span><span class="sxs-lookup"><span data-stu-id="608da-103">Cancal a running deployment</span></span>

## <span data-ttu-id="608da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="608da-104">SYNTAX</span></span>

### <span data-ttu-id="608da-105">StopByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="608da-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="608da-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="608da-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="608da-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="608da-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="608da-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="608da-108">DESCRIPTION</span></span>
<span data-ttu-id="608da-109">**Stop-AzDeployment** cmdlet 'i, başlatılmış ancak tamamlanmamış olan abonelik kapsamındaki bir dağıtımı iptal eder.</span><span class="sxs-lookup"><span data-stu-id="608da-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="608da-110">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="608da-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="608da-111">Abonelik kapsamında dağıtım oluşturmak için New-AzDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="608da-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="608da-112">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="608da-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="608da-113">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="608da-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="608da-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="608da-114">EXAMPLES</span></span>

### <span data-ttu-id="608da-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="608da-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="608da-116">Bu komut, geçerli abonelik kapsamında çalışan "deployment01" dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="608da-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="608da-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="608da-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="608da-118">Bu komut, geçerli abonelik kapsamındaki "deployment01" dağıtımını alır ve iptal eder.</span><span class="sxs-lookup"><span data-stu-id="608da-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="608da-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="608da-119">PARAMETERS</span></span>

### <span data-ttu-id="608da-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="608da-120">-ApiVersion</span></span>
<span data-ttu-id="608da-121">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="608da-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="608da-122">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="608da-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="608da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="608da-123">-DefaultProfile</span></span>
<span data-ttu-id="608da-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="608da-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="608da-125">-ID</span><span class="sxs-lookup"><span data-stu-id="608da-125">-Id</span></span>
<span data-ttu-id="608da-126">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="608da-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="608da-127">Örnek:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="608da-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="608da-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="608da-128">-InputObject</span></span>
<span data-ttu-id="608da-129">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="608da-129">The deployment object.</span></span>

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

### <span data-ttu-id="608da-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="608da-130">-Name</span></span>
<span data-ttu-id="608da-131">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="608da-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="608da-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="608da-132">-PassThru</span></span>
<span data-ttu-id="608da-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="608da-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="608da-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="608da-134">-Pre</span></span>
<span data-ttu-id="608da-135">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="608da-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="608da-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="608da-136">-Confirm</span></span>
<span data-ttu-id="608da-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="608da-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="608da-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="608da-138">-WhatIf</span></span>
<span data-ttu-id="608da-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="608da-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="608da-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="608da-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="608da-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608da-141">CommonParameters</span></span>
<span data-ttu-id="608da-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="608da-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608da-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="608da-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608da-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="608da-144">INPUTS</span></span>

### <span data-ttu-id="608da-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="608da-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="608da-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="608da-146">OUTPUTS</span></span>

### <span data-ttu-id="608da-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="608da-147">System.Boolean</span></span>

## <span data-ttu-id="608da-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="608da-148">NOTES</span></span>

## <span data-ttu-id="608da-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="608da-149">RELATED LINKS</span></span>
