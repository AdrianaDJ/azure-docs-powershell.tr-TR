---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571426"
---
# <span data-ttu-id="fc3a7-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="fc3a7-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="fc3a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3a7-103">Bir dağıtımı siler.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-103">Deletes a rollout.</span></span>

## <span data-ttu-id="fc3a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc3a7-104">SYNTAX</span></span>

### <span data-ttu-id="fc3a7-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc3a7-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc3a7-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="fc3a7-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc3a7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fc3a7-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc3a7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc3a7-108">DESCRIPTION</span></span>
<span data-ttu-id="fc3a7-109">**Remove-Azurermdeploymentmanagerpiyasaya çıkarma** cmdlet 'i Terminal durumundaki bir dağıtımı siler.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="fc3a7-110">Dağıtımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="fc3a7-111">Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="fc3a7-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc3a7-112">EXAMPLES</span></span>

### <span data-ttu-id="fc3a7-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fc3a7-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="fc3a7-114">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı siler.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fc3a7-115">Örnek 2: kaynak tanımlayıcısını kullanarak bir dağıtımı silme</span><span class="sxs-lookup"><span data-stu-id="fc3a7-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="fc3a7-116">Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı siler.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fc3a7-117">Örnek 3: piyasaya çıkarma nesnesini kullanarak silme.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="fc3a7-118">Bu komut, adı ve ResourceGroup 'ın sırasıyla $rolloutObject ad ve ResourceGroupName özellikleriyle eşleştiğini siler.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="fc3a7-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc3a7-119">PARAMETERS</span></span>

### <span data-ttu-id="fc3a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc3a7-120">-DefaultProfile</span></span>
<span data-ttu-id="fc3a7-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc3a7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fc3a7-122">-Force</span></span>
<span data-ttu-id="fc3a7-123">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fc3a7-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc3a7-124">-Name</span></span>
<span data-ttu-id="fc3a7-125">Ürün adı.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="fc3a7-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fc3a7-126">-PassThru</span></span>
<span data-ttu-id="fc3a7-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="fc3a7-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fc3a7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc3a7-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc3a7-129">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-129">The resource group.</span></span>

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

### <span data-ttu-id="fc3a7-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fc3a7-130">-ResourceId</span></span>
<span data-ttu-id="fc3a7-131">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-131">The resource identifier.</span></span>

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

### <span data-ttu-id="fc3a7-132">-Ürün</span><span class="sxs-lookup"><span data-stu-id="fc3a7-132">-Rollout</span></span>
<span data-ttu-id="fc3a7-133">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="fc3a7-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc3a7-134">-Confirm</span></span>
<span data-ttu-id="fc3a7-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc3a7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc3a7-136">-WhatIf</span></span>
<span data-ttu-id="fc3a7-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc3a7-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc3a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3a7-139">CommonParameters</span></span>
<span data-ttu-id="fc3a7-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc3a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3a7-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc3a7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3a7-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc3a7-142">INPUTS</span></span>

### <span data-ttu-id="fc3a7-143">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="fc3a7-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="fc3a7-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc3a7-144">OUTPUTS</span></span>

### <span data-ttu-id="fc3a7-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc3a7-145">System.Boolean</span></span>

## <span data-ttu-id="fc3a7-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc3a7-146">NOTES</span></span>

## <span data-ttu-id="fc3a7-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc3a7-147">RELATED LINKS</span></span>

[<span data-ttu-id="fc3a7-148">Get-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="fc3a7-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="fc3a7-149">Stop-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="fc3a7-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="fc3a7-150">Restart-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="fc3a7-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)