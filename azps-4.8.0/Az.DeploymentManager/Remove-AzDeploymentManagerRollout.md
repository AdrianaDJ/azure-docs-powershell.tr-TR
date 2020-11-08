---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107797"
---
# <span data-ttu-id="5d325-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="5d325-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="5d325-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d325-102">SYNOPSIS</span></span>
<span data-ttu-id="5d325-103">Dağıtımı siler.</span><span class="sxs-lookup"><span data-stu-id="5d325-103">Deletes the rollout.</span></span>

## <span data-ttu-id="5d325-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d325-104">SYNTAX</span></span>

### <span data-ttu-id="5d325-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d325-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d325-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="5d325-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d325-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5d325-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d325-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d325-108">DESCRIPTION</span></span>
<span data-ttu-id="5d325-109">**Remove-Azdeploymentmanagerpiyasaya dağıtımı** cmdlet 'i Terminal durumundaki bir kademeli silme.</span><span class="sxs-lookup"><span data-stu-id="5d325-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="5d325-110">Dağıtımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="5d325-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="5d325-111">Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5d325-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="5d325-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d325-112">EXAMPLES</span></span>

### <span data-ttu-id="5d325-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5d325-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="5d325-114">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı siler.</span><span class="sxs-lookup"><span data-stu-id="5d325-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5d325-115">Örnek 2: kaynak tanımlayıcısını kullanarak bir dağıtımı silme</span><span class="sxs-lookup"><span data-stu-id="5d325-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="5d325-116">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı siler.</span><span class="sxs-lookup"><span data-stu-id="5d325-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5d325-117">Örnek 3: piyasaya çıkarma nesnesini kullanarak silme.</span><span class="sxs-lookup"><span data-stu-id="5d325-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="5d325-118">Bu komut, adı ve ResourceGroup 'ın sırasıyla $rolloutObject ad ve ResourceGroupName özellikleriyle eşleştiğini siler.</span><span class="sxs-lookup"><span data-stu-id="5d325-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="5d325-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d325-119">PARAMETERS</span></span>

### <span data-ttu-id="5d325-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d325-120">-DefaultProfile</span></span>
<span data-ttu-id="5d325-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d325-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d325-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d325-122">-InputObject</span></span>
<span data-ttu-id="5d325-123">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="5d325-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="5d325-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="5d325-124">-Name</span></span>
<span data-ttu-id="5d325-125">Ürün adı.</span><span class="sxs-lookup"><span data-stu-id="5d325-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="5d325-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5d325-126">-PassThru</span></span>
<span data-ttu-id="5d325-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="5d325-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5d325-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d325-128">-ResourceGroupName</span></span>
<span data-ttu-id="5d325-129">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="5d325-129">The resource group.</span></span>

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

### <span data-ttu-id="5d325-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5d325-130">-ResourceId</span></span>
<span data-ttu-id="5d325-131">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="5d325-131">The resource identifier.</span></span>

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

### <span data-ttu-id="5d325-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="5d325-132">-Confirm</span></span>
<span data-ttu-id="5d325-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5d325-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d325-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d325-134">-WhatIf</span></span>
<span data-ttu-id="5d325-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d325-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d325-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5d325-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d325-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d325-137">CommonParameters</span></span>
<span data-ttu-id="5d325-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d325-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d325-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5d325-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d325-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d325-140">INPUTS</span></span>

### <span data-ttu-id="5d325-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5d325-141">System.String</span></span>

### <span data-ttu-id="5d325-142">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="5d325-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="5d325-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d325-143">OUTPUTS</span></span>

### <span data-ttu-id="5d325-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d325-144">System.Boolean</span></span>

## <span data-ttu-id="5d325-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d325-145">NOTES</span></span>

## <span data-ttu-id="5d325-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d325-146">RELATED LINKS</span></span>
