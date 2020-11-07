---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/stop-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 3c4f221fc00187c4faea2dbcc1a5014822c476c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761704"
---
# <span data-ttu-id="47e16-101">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="47e16-101">Stop-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="47e16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e16-102">SYNOPSIS</span></span>
<span data-ttu-id="47e16-103">Devam eden bir dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="47e16-103">Stops a rollout in progress.</span></span>

## <span data-ttu-id="47e16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47e16-104">SYNTAX</span></span>

### <span data-ttu-id="47e16-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47e16-105">Interactive (Default)</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47e16-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="47e16-106">ResourceId</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47e16-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="47e16-107">InputObject</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47e16-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47e16-108">DESCRIPTION</span></span>
<span data-ttu-id="47e16-109">**Stop-Azurermdeploymentmanagerpiyasaya** çıkarma cmdlet 'i devam etmekte olan bir dağıtımı durdurur</span><span class="sxs-lookup"><span data-stu-id="47e16-109">The **Stop-AzureRmDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="47e16-110">Dağıtımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="47e16-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="47e16-111">Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47e16-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="47e16-112">Bir dağıtım durdurulduğunda, sürdürülemez veya yeniden başlatılamaz.</span><span class="sxs-lookup"><span data-stu-id="47e16-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="47e16-113">Yalnızca yeni bir ürün oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47e16-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="47e16-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47e16-114">EXAMPLES</span></span>

### <span data-ttu-id="47e16-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="47e16-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="47e16-116">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="47e16-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="47e16-117">Örnek 2: kaynak tanımlayıcısını kullanarak bir dağıtımı durdurma</span><span class="sxs-lookup"><span data-stu-id="47e16-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="47e16-118">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="47e16-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="47e16-119">Örnek 3: piyasaya çıkarma nesnesini kullanarak bir dağıtımı durdurma.</span><span class="sxs-lookup"><span data-stu-id="47e16-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="47e16-120">Bu komut, adı ve ResourceGroup 'ın sırasıyla $rolloutObject ad ve ResourceGroupName özellikleriyle eşleştiğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="47e16-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="47e16-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47e16-121">PARAMETERS</span></span>

### <span data-ttu-id="47e16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e16-122">-DefaultProfile</span></span>
<span data-ttu-id="47e16-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47e16-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e16-124">-Force</span><span class="sxs-lookup"><span data-stu-id="47e16-124">-Force</span></span>
<span data-ttu-id="47e16-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="47e16-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="47e16-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="47e16-126">-Name</span></span>
<span data-ttu-id="47e16-127">Ürün adı.</span><span class="sxs-lookup"><span data-stu-id="47e16-127">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e16-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e16-128">-ResourceGroupName</span></span>
<span data-ttu-id="47e16-129">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="47e16-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e16-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="47e16-130">-ResourceId</span></span>
<span data-ttu-id="47e16-131">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="47e16-131">The resource identifier.</span></span>

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

### <span data-ttu-id="47e16-132">-Ürün</span><span class="sxs-lookup"><span data-stu-id="47e16-132">-Rollout</span></span>
<span data-ttu-id="47e16-133">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="47e16-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="47e16-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="47e16-134">-Confirm</span></span>
<span data-ttu-id="47e16-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47e16-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e16-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e16-136">-WhatIf</span></span>
<span data-ttu-id="47e16-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47e16-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47e16-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47e16-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e16-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e16-139">CommonParameters</span></span>
<span data-ttu-id="47e16-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47e16-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e16-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e16-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e16-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47e16-142">INPUTS</span></span>

### <span data-ttu-id="47e16-143">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="47e16-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="47e16-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47e16-144">OUTPUTS</span></span>

### <span data-ttu-id="47e16-145">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="47e16-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="47e16-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47e16-146">NOTES</span></span>

## <span data-ttu-id="47e16-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47e16-147">RELATED LINKS</span></span>

[<span data-ttu-id="47e16-148">Get-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="47e16-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="47e16-149">Restart-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="47e16-149">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="47e16-150">Remove-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="47e16-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)