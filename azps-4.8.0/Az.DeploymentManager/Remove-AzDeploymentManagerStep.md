---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107793"
---
# <span data-ttu-id="f4dd9-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f4dd9-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f4dd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="f4dd9-103">Adımı siler.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-103">Deletes the step.</span></span>

## <span data-ttu-id="f4dd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4dd9-104">SYNTAX</span></span>

### <span data-ttu-id="f4dd9-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4dd9-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dd9-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f4dd9-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dd9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4dd9-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4dd9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4dd9-108">DESCRIPTION</span></span>
<span data-ttu-id="f4dd9-109">**Remove-AzDeploymentManagerStep** cmdlet 'i bir adımı siler.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="f4dd9-110">Adımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="f4dd9-111">Alternatif olarak, Step nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="f4dd9-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4dd9-112">EXAMPLES</span></span>

### <span data-ttu-id="f4dd9-113">Örnek 1: adımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="f4dd9-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="f4dd9-114">Bu komut, ContosoResourceGroup 'ta ContosoService1WaitStep adındaki bir adımı siler.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f4dd9-115">Örnek 2: kaynak tanımlayıcısını kullanarak bir adımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="f4dd9-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="f4dd9-116">Bu komut, ContosoResourceGroup 'ta ContosoService1WaitStep adındaki bir adımı siler.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f4dd9-117">Örnek 3: New-AzDeploymentManagerStep tarafından döndürülen bir nesneyi kullanarak adımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="f4dd9-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="f4dd9-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4dd9-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="f4dd9-119">Bu komut, adı ve ResourceGroup 'in sırasıyla $stepObject Name ve ResourceGroupName özellikleriyle eşleşen bir adımını siler.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="f4dd9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4dd9-120">PARAMETERS</span></span>

### <span data-ttu-id="f4dd9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4dd9-121">-DefaultProfile</span></span>
<span data-ttu-id="f4dd9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4dd9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4dd9-123">-InputObject</span></span>
<span data-ttu-id="f4dd9-124">Kaldırılacak adım.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd9-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4dd9-125">-Name</span></span>
<span data-ttu-id="f4dd9-126">Adımın adı.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-126">The name of the step.</span></span>

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

### <span data-ttu-id="f4dd9-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f4dd9-127">-PassThru</span></span>
<span data-ttu-id="f4dd9-128">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f4dd9-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f4dd9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4dd9-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4dd9-130">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-130">The resource group.</span></span>

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

### <span data-ttu-id="f4dd9-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f4dd9-131">-ResourceId</span></span>
<span data-ttu-id="f4dd9-132">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-132">The resource identifier.</span></span>

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

### <span data-ttu-id="f4dd9-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4dd9-133">-Confirm</span></span>
<span data-ttu-id="f4dd9-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4dd9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4dd9-135">-WhatIf</span></span>
<span data-ttu-id="f4dd9-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4dd9-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4dd9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4dd9-138">CommonParameters</span></span>
<span data-ttu-id="f4dd9-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4dd9-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4dd9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4dd9-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4dd9-141">INPUTS</span></span>

### <span data-ttu-id="f4dd9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f4dd9-142">System.String</span></span>

### <span data-ttu-id="f4dd9-143">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f4dd9-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f4dd9-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4dd9-144">OUTPUTS</span></span>

### <span data-ttu-id="f4dd9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4dd9-145">System.Boolean</span></span>

## <span data-ttu-id="f4dd9-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4dd9-146">NOTES</span></span>

## <span data-ttu-id="f4dd9-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4dd9-147">RELATED LINKS</span></span>
