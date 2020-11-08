---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104360"
---
# <span data-ttu-id="147bf-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="147bf-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="147bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="147bf-102">SYNOPSIS</span></span>
<span data-ttu-id="147bf-103">Dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="147bf-103">Stops the rollout.</span></span>

## <span data-ttu-id="147bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="147bf-104">SYNTAX</span></span>

### <span data-ttu-id="147bf-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="147bf-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="147bf-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="147bf-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="147bf-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="147bf-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="147bf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="147bf-108">DESCRIPTION</span></span>
<span data-ttu-id="147bf-109">**Stop-Azdeploymentmanagerpiyasaya dağıtım** cmdlet 'i bir piyasaya çıkarma işlemi durdurur</span><span class="sxs-lookup"><span data-stu-id="147bf-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="147bf-110">Dağıtımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="147bf-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="147bf-111">Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="147bf-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="147bf-112">Bir dağıtım durdurulduğunda, sürdürülemez veya yeniden başlatılamaz.</span><span class="sxs-lookup"><span data-stu-id="147bf-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="147bf-113">Yalnızca yeni bir ürün oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="147bf-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="147bf-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="147bf-114">EXAMPLES</span></span>

### <span data-ttu-id="147bf-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="147bf-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="147bf-116">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="147bf-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="147bf-117">Örnek 2: kaynak tanımlayıcısını kullanarak bir dağıtımı durdurma</span><span class="sxs-lookup"><span data-stu-id="147bf-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="147bf-118">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı durdurur.</span><span class="sxs-lookup"><span data-stu-id="147bf-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="147bf-119">Örnek 3: piyasaya çıkarma nesnesini kullanarak bir dağıtımı durdurma.</span><span class="sxs-lookup"><span data-stu-id="147bf-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="147bf-120">Bu komut, adı ve ResourceGroup 'ın sırasıyla $rolloutObject ad ve ResourceGroupName özellikleriyle eşleştiğini durdurur.</span><span class="sxs-lookup"><span data-stu-id="147bf-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="147bf-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="147bf-121">PARAMETERS</span></span>

### <span data-ttu-id="147bf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="147bf-122">-DefaultProfile</span></span>
<span data-ttu-id="147bf-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="147bf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="147bf-124">-Force</span><span class="sxs-lookup"><span data-stu-id="147bf-124">-Force</span></span>
<span data-ttu-id="147bf-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="147bf-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="147bf-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="147bf-126">-InputObject</span></span>
<span data-ttu-id="147bf-127">Kaldırılacak olan ürün.</span><span class="sxs-lookup"><span data-stu-id="147bf-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="147bf-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="147bf-128">-Name</span></span>
<span data-ttu-id="147bf-129">Ürün adı.</span><span class="sxs-lookup"><span data-stu-id="147bf-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="147bf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="147bf-130">-ResourceGroupName</span></span>
<span data-ttu-id="147bf-131">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="147bf-131">The resource group.</span></span>

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

### <span data-ttu-id="147bf-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="147bf-132">-ResourceId</span></span>
<span data-ttu-id="147bf-133">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="147bf-133">The resource identifier.</span></span>

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

### <span data-ttu-id="147bf-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="147bf-134">-Confirm</span></span>
<span data-ttu-id="147bf-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="147bf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="147bf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="147bf-136">-WhatIf</span></span>
<span data-ttu-id="147bf-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="147bf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="147bf-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="147bf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="147bf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147bf-139">CommonParameters</span></span>
<span data-ttu-id="147bf-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="147bf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147bf-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="147bf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147bf-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="147bf-142">INPUTS</span></span>

### <span data-ttu-id="147bf-143">System. String</span><span class="sxs-lookup"><span data-stu-id="147bf-143">System.String</span></span>

### <span data-ttu-id="147bf-144">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="147bf-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="147bf-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="147bf-145">OUTPUTS</span></span>

### <span data-ttu-id="147bf-146">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="147bf-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="147bf-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="147bf-147">NOTES</span></span>

## <span data-ttu-id="147bf-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="147bf-148">RELATED LINKS</span></span>
