---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 49ea711740eff624a9560b6d70239edb476dc989
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939235"
---
# <span data-ttu-id="27d70-101">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="27d70-101">Stop-AzureRmDeployment</span></span>

## <span data-ttu-id="27d70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27d70-102">SYNOPSIS</span></span>
<span data-ttu-id="27d70-103">Çalışan bir dağıtım</span><span class="sxs-lookup"><span data-stu-id="27d70-103">Cancal a running deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27d70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27d70-104">SYNTAX</span></span>

### <span data-ttu-id="27d70-105">StopByDeploymentName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27d70-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzureRmDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27d70-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="27d70-106">StopByDeploymentId</span></span>
```
Stop-AzureRmDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27d70-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="27d70-107">StopByInputObject</span></span>
```
Stop-AzureRmDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27d70-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="27d70-108">DESCRIPTION</span></span>
<span data-ttu-id="27d70-109">**Stop-AzureRmDeployment** cmdlet 'i, abonelik kapsamındaki ancak tamamlanmamış bir dağıtımı iptal eder.</span><span class="sxs-lookup"><span data-stu-id="27d70-109">The **Stop-AzureRmDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="27d70-110">Bir dağıtımı durdurmak için dağıtımın, sağlama gibi tamamlanmamış bir sağlama durumu olmalıdır; bunun sağlanması veya başarısız gibi tamamlanmamış bir durumda olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="27d70-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="27d70-111">Abonelik kapsamında dağıtım oluşturmak için New-AzureRmDeployment cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="27d70-111">To create a deployment at subscription scope, use the New-AzureRmDeployment cmdlet.</span></span>

<span data-ttu-id="27d70-112">Bu cmdlet yalnızca bir çalışan dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="27d70-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="27d70-113">Belirli bir dağıtımı durdurmak için *Name* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="27d70-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="27d70-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27d70-114">EXAMPLES</span></span>

### <span data-ttu-id="27d70-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="27d70-115">Example 1</span></span>
```
PS C:\>Stop-AzureRmDeployment -Name "deployment01"
```

<span data-ttu-id="27d70-116">Bu komut, geçerli abonelik kapsamında çalışan "deployment01" dağıtımını iptal eder.</span><span class="sxs-lookup"><span data-stu-id="27d70-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="27d70-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="27d70-117">Example 2</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "deployment01" | Stop-AzureRmDeployment
```

<span data-ttu-id="27d70-118">Bu komut, geçerli abonelik kapsamındaki "deployment01" dağıtımını alır ve iptal eder.</span><span class="sxs-lookup"><span data-stu-id="27d70-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="27d70-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27d70-119">PARAMETERS</span></span>

### <span data-ttu-id="27d70-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="27d70-120">-ApiVersion</span></span>
<span data-ttu-id="27d70-121">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="27d70-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="27d70-122">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="27d70-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="27d70-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27d70-123">-DefaultProfile</span></span>
<span data-ttu-id="27d70-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27d70-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27d70-125">-ID</span><span class="sxs-lookup"><span data-stu-id="27d70-125">-Id</span></span>
<span data-ttu-id="27d70-126">Dağıtımın tam kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="27d70-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="27d70-127">Örnek:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="27d70-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="27d70-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27d70-128">-InputObject</span></span>
<span data-ttu-id="27d70-129">Dağıtım nesnesi.</span><span class="sxs-lookup"><span data-stu-id="27d70-129">The deployment object.</span></span>

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

### <span data-ttu-id="27d70-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="27d70-130">-Name</span></span>
<span data-ttu-id="27d70-131">Dağıtımın adı.</span><span class="sxs-lookup"><span data-stu-id="27d70-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="27d70-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="27d70-132">-PassThru</span></span>
<span data-ttu-id="27d70-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="27d70-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="27d70-134">-Pre-</span><span class="sxs-lookup"><span data-stu-id="27d70-134">-Pre</span></span>
<span data-ttu-id="27d70-135">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27d70-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="27d70-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="27d70-136">-Confirm</span></span>
<span data-ttu-id="27d70-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27d70-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27d70-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27d70-138">-WhatIf</span></span>
<span data-ttu-id="27d70-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27d70-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27d70-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="27d70-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27d70-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27d70-141">CommonParameters</span></span>
<span data-ttu-id="27d70-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27d70-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27d70-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27d70-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27d70-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27d70-144">INPUTS</span></span>

### <span data-ttu-id="27d70-145">System. String</span><span class="sxs-lookup"><span data-stu-id="27d70-145">System.String</span></span>

## <span data-ttu-id="27d70-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27d70-146">OUTPUTS</span></span>

### <span data-ttu-id="27d70-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27d70-147">System.Boolean</span></span>

## <span data-ttu-id="27d70-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27d70-148">NOTES</span></span>

## <span data-ttu-id="27d70-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27d70-149">RELATED LINKS</span></span>
