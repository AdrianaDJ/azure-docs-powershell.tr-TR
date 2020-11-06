---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571513"
---
# <span data-ttu-id="b6a19-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b6a19-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="b6a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6a19-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a19-103">Bir adımı siler.</span><span class="sxs-lookup"><span data-stu-id="b6a19-103">Deletes a step.</span></span>

## <span data-ttu-id="b6a19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6a19-104">SYNTAX</span></span>

### <span data-ttu-id="b6a19-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6a19-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6a19-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b6a19-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6a19-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6a19-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a19-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6a19-108">DESCRIPTION</span></span>
<span data-ttu-id="b6a19-109">**Remove-AzureRmDeploymentManagerStep** cmdlet 'i bir adımı siler.</span><span class="sxs-lookup"><span data-stu-id="b6a19-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="b6a19-110">Adımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="b6a19-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="b6a19-111">Alternatif olarak, Step nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6a19-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="b6a19-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6a19-112">EXAMPLES</span></span>
### <span data-ttu-id="b6a19-113">Örnek 1: adımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="b6a19-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="b6a19-114">Bu komut, ContosoResourceGroup 'ta ContosoService1WaitStep adındaki bir adımı siler.</span><span class="sxs-lookup"><span data-stu-id="b6a19-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b6a19-115">Örnek 2: kaynak tanımlayıcısını kullanarak bir adımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="b6a19-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="b6a19-116">Bu komut, ContosoResourceGroup 'ta ContosoService1WaitStep adındaki bir adımı siler.</span><span class="sxs-lookup"><span data-stu-id="b6a19-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b6a19-117">Örnek 3: New-AzureRmDeploymentManagerStep tarafından döndürülen bir nesneyi kullanarak adımı kaldırma</span><span class="sxs-lookup"><span data-stu-id="b6a19-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="b6a19-118">Bu komut, adı ve ResourceGroup 'in sırasıyla $stepObject Name ve ResourceGroupName özellikleriyle eşleşen bir adımını siler.</span><span class="sxs-lookup"><span data-stu-id="b6a19-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="b6a19-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6a19-119">PARAMETERS</span></span>

### <span data-ttu-id="b6a19-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a19-120">-DefaultProfile</span></span>
<span data-ttu-id="b6a19-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6a19-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a19-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b6a19-122">-Force</span></span>
<span data-ttu-id="b6a19-123">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="b6a19-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b6a19-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6a19-124">-Name</span></span>
<span data-ttu-id="b6a19-125">Adımın adı.</span><span class="sxs-lookup"><span data-stu-id="b6a19-125">The name of the step.</span></span>

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

### <span data-ttu-id="b6a19-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b6a19-126">-PassThru</span></span>
<span data-ttu-id="b6a19-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="b6a19-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b6a19-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a19-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6a19-129">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b6a19-129">The resource group.</span></span>

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

### <span data-ttu-id="b6a19-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b6a19-130">-ResourceId</span></span>
<span data-ttu-id="b6a19-131">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b6a19-131">The resource identifier.</span></span>

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

### <span data-ttu-id="b6a19-132">-Adım</span><span class="sxs-lookup"><span data-stu-id="b6a19-132">-Step</span></span>
<span data-ttu-id="b6a19-133">Kaldırılacak adım.</span><span class="sxs-lookup"><span data-stu-id="b6a19-133">The step to be removed.</span></span>

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

### <span data-ttu-id="b6a19-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6a19-134">-Confirm</span></span>
<span data-ttu-id="b6a19-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6a19-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a19-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a19-136">-WhatIf</span></span>
<span data-ttu-id="b6a19-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6a19-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a19-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6a19-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a19-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a19-139">CommonParameters</span></span>
<span data-ttu-id="b6a19-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6a19-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b6a19-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a19-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a19-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6a19-142">INPUTS</span></span>

### <span data-ttu-id="b6a19-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a19-143">System.String</span></span>

### <span data-ttu-id="b6a19-144">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b6a19-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b6a19-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6a19-145">OUTPUTS</span></span>

### <span data-ttu-id="b6a19-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6a19-146">System.Boolean</span></span>

## <span data-ttu-id="b6a19-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6a19-147">NOTES</span></span>

## <span data-ttu-id="b6a19-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6a19-148">RELATED LINKS</span></span>
