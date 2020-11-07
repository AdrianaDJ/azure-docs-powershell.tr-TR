---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: d68ca0e13c279e58715b57ae73a2c8e2f4f30d8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760966"
---
# <span data-ttu-id="e4a4f-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="e4a4f-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="e4a4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="e4a4f-103">Dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-103">Stops the rollout.</span></span>

## <span data-ttu-id="e4a4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4a4f-104">SYNTAX</span></span>

### <span data-ttu-id="e4a4f-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e4a4f-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4a4f-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="e4a4f-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4a4f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e4a4f-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4a4f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4a4f-108">DESCRIPTION</span></span>
<span data-ttu-id="e4a4f-109">**Stop-Azdeploymentmanagerpiyasaya dağıtım** cmdlet 'i bir piyasaya çıkarma işlemi durdurur</span><span class="sxs-lookup"><span data-stu-id="e4a4f-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="e4a4f-110">Dağıtımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="e4a4f-111">Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="e4a4f-112">Bir dağıtım durdurulduğunda, sürdürülemez veya yeniden başlatılamaz.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="e4a4f-113">Yalnızca yeni bir ürün oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="e4a4f-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4a4f-114">EXAMPLES</span></span>

### <span data-ttu-id="e4a4f-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e4a4f-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="e4a4f-116">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="e4a4f-117">Örnek 2: kaynak tanımlayıcısını kullanarak bir dağıtımı durdurma</span><span class="sxs-lookup"><span data-stu-id="e4a4f-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="e4a4f-118">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e4a4f-119">Örnek 3: piyasaya çıkarma nesnesini kullanarak bir dağıtımı durdurma.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="e4a4f-120">Bu komut, adı ve ResourceGroup 'ın sırasıyla $rolloutObject ad ve ResourceGroupName özellikleriyle eşleştiğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="e4a4f-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4a4f-121">PARAMETERS</span></span>

### <span data-ttu-id="e4a4f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4a4f-122">-DefaultProfile</span></span>
<span data-ttu-id="e4a4f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4a4f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e4a4f-124">-Force</span></span>
<span data-ttu-id="e4a4f-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e4a4f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4a4f-126">-InputObject</span></span>
<span data-ttu-id="e4a4f-127">Kaldırılacak olan ürün.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-127">The rollout to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4a4f-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4a4f-128">-Name</span></span>
<span data-ttu-id="e4a4f-129">Ürün adı.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-129">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4a4f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4a4f-130">-ResourceGroupName</span></span>
<span data-ttu-id="e4a4f-131">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4a4f-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e4a4f-132">-ResourceId</span></span>
<span data-ttu-id="e4a4f-133">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-133">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4a4f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4a4f-134">-Confirm</span></span>
<span data-ttu-id="e4a4f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4a4f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4a4f-136">-WhatIf</span></span>
<span data-ttu-id="e4a4f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4a4f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4a4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4a4f-139">CommonParameters</span></span>
<span data-ttu-id="e4a4f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4a4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4a4f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4a4f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4a4f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4a4f-142">INPUTS</span></span>

### <span data-ttu-id="e4a4f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e4a4f-143">System.String</span></span>

### <span data-ttu-id="e4a4f-144">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="e4a4f-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e4a4f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4a4f-145">OUTPUTS</span></span>

### <span data-ttu-id="e4a4f-146">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="e4a4f-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e4a4f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4a4f-147">NOTES</span></span>

## <span data-ttu-id="e4a4f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4a4f-148">RELATED LINKS</span></span>
