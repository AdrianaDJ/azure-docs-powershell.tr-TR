---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572201"
---
# <span data-ttu-id="beb79-101">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="beb79-101">Restart-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="beb79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beb79-102">SYNOPSIS</span></span>
<span data-ttu-id="beb79-103">Başarısız bir dağıtımı yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="beb79-103">Restart a failed rollout.</span></span>

## <span data-ttu-id="beb79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="beb79-104">SYNTAX</span></span>

### <span data-ttu-id="beb79-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="beb79-105">Interactive (Default)</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beb79-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="beb79-106">ResourceId</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beb79-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="beb79-107">InputObject</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beb79-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="beb79-108">DESCRIPTION</span></span>
<span data-ttu-id="beb79-109">**Restart-Azurermdeploymentmanagerpiyasaya kapatma** cmdlet 'i başarısız olan bir dağıtımı yeniden başlatır ve bu sürümü, kademeli olan bilgilerin tüm ayrıntılı bilgileriyle birlikte döndürür.</span><span class="sxs-lookup"><span data-stu-id="beb79-109">The **Restart-AzureRmDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="beb79-110">Dağıtımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="beb79-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="beb79-111">Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="beb79-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="beb79-112">İsteğe bağlı parametre SkipSucceeded, önceki sürümdeki tüm başarılı adımları atlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="beb79-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="beb79-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="beb79-113">EXAMPLES</span></span>

### <span data-ttu-id="beb79-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="beb79-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="beb79-115">Bu komut, ContosoRollout adındaki bir dağıtımı yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="beb79-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="beb79-116">SkipSucceeded bayrağı, başarıyla çalıştırılan tüm adımların atlanacağını ve piyasaya yürütmenin son başarısız olduğunda yürütmeye devam etmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="beb79-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="beb79-117">Örnek 2: kaynak tanımlayıcısını kullanarak bir dağıtımı yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="beb79-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="beb79-118">Bu komut, ContosoRollout adındaki bir dağıtımı yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="beb79-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="beb79-119">Örnek 3: piyasaya çıkarma nesnesini kullanarak bir dağıtımı yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="beb79-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="beb79-120">Bu komut, adı ve ResourceGroup 'ın sırasıyla $rolloutObject ad ve ResourceGroupName özellikleriyle eşleştiğini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="beb79-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="beb79-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="beb79-121">PARAMETERS</span></span>

### <span data-ttu-id="beb79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beb79-122">-DefaultProfile</span></span>
<span data-ttu-id="beb79-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="beb79-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beb79-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="beb79-124">-Name</span></span>
<span data-ttu-id="beb79-125">Ürün adı.</span><span class="sxs-lookup"><span data-stu-id="beb79-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="beb79-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beb79-126">-ResourceGroupName</span></span>
<span data-ttu-id="beb79-127">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="beb79-127">The resource group.</span></span>

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

### <span data-ttu-id="beb79-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="beb79-128">-ResourceId</span></span>
<span data-ttu-id="beb79-129">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="beb79-129">The resource identifier.</span></span>

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

### <span data-ttu-id="beb79-130">-Ürün</span><span class="sxs-lookup"><span data-stu-id="beb79-130">-Rollout</span></span>
<span data-ttu-id="beb79-131">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="beb79-131">The resource to be removed.</span></span>

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

### <span data-ttu-id="beb79-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="beb79-132">-SkipSucceeded</span></span>
<span data-ttu-id="beb79-133">Önceki çalıştırmada başarılı olan adımları atlayın.</span><span class="sxs-lookup"><span data-stu-id="beb79-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="beb79-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="beb79-134">-Confirm</span></span>
<span data-ttu-id="beb79-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="beb79-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beb79-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beb79-136">-WhatIf</span></span>
<span data-ttu-id="beb79-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="beb79-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beb79-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="beb79-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beb79-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb79-139">CommonParameters</span></span>
<span data-ttu-id="beb79-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="beb79-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb79-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beb79-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb79-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="beb79-142">INPUTS</span></span>

### <span data-ttu-id="beb79-143">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="beb79-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="beb79-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="beb79-144">OUTPUTS</span></span>

### <span data-ttu-id="beb79-145">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="beb79-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="beb79-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="beb79-146">NOTES</span></span>

## <span data-ttu-id="beb79-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="beb79-147">RELATED LINKS</span></span>

[<span data-ttu-id="beb79-148">Get-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="beb79-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="beb79-149">Stop-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="beb79-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="beb79-150">Remove-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="beb79-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)