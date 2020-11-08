---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268286"
---
# <span data-ttu-id="b2208-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="b2208-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="b2208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2208-102">SYNOPSIS</span></span>
<span data-ttu-id="b2208-103">Başarısız bir dağıtımı yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b2208-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="b2208-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2208-104">SYNTAX</span></span>

### <span data-ttu-id="b2208-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2208-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2208-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b2208-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2208-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b2208-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2208-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2208-108">DESCRIPTION</span></span>
<span data-ttu-id="b2208-109">**Restart-Azdeploymentmanagerpiyasaya dağıtım** cmdlet 'i başarısız olan bir dağıtımı yeniden başlatır ve bu sürümü, kademeli bir dağıtımı ilerleme durumuyla ilgili tüm ayrıntılı bilgilerle birlikte döndürür.</span><span class="sxs-lookup"><span data-stu-id="b2208-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="b2208-110">Dağıtımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="b2208-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="b2208-111">Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b2208-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="b2208-112">İsteğe bağlı parametre SkipSucceeded, önceki sürümdeki tüm başarılı adımları atlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b2208-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="b2208-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2208-113">EXAMPLES</span></span>

### <span data-ttu-id="b2208-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b2208-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="b2208-115">Bu komut, ContosoRollout adındaki bir dağıtımı yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b2208-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="b2208-116">SkipSucceeded bayrağı, başarıyla çalıştırılan tüm adımların atlanacağını ve piyasaya yürütmenin son başarısız olduğunda yürütmeye devam etmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2208-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="b2208-117">Örnek 2: kaynak tanımlayıcısını kullanarak bir dağıtımı yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="b2208-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="b2208-118">Bu komut, ContosoRollout adındaki bir dağıtımı yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b2208-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b2208-119">Örnek 3: piyasaya çıkarma nesnesini kullanarak bir dağıtımı yeniden başlatın.</span><span class="sxs-lookup"><span data-stu-id="b2208-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="b2208-120">Bu komut, adı ve ResourceGroup 'ın sırasıyla $rolloutObject ad ve ResourceGroupName özellikleriyle eşleştiğini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b2208-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="b2208-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2208-121">PARAMETERS</span></span>

### <span data-ttu-id="b2208-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2208-122">-DefaultProfile</span></span>
<span data-ttu-id="b2208-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2208-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2208-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2208-124">-InputObject</span></span>
<span data-ttu-id="b2208-125">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="b2208-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="b2208-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2208-126">-Name</span></span>
<span data-ttu-id="b2208-127">Ürün adı.</span><span class="sxs-lookup"><span data-stu-id="b2208-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="b2208-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2208-128">-ResourceGroupName</span></span>
<span data-ttu-id="b2208-129">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b2208-129">The resource group.</span></span>

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

### <span data-ttu-id="b2208-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b2208-130">-ResourceId</span></span>
<span data-ttu-id="b2208-131">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b2208-131">The resource identifier.</span></span>

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

### <span data-ttu-id="b2208-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="b2208-132">-SkipSucceeded</span></span>
<span data-ttu-id="b2208-133">Önceki çalıştırmada başarılı olan adımları atlayın.</span><span class="sxs-lookup"><span data-stu-id="b2208-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="b2208-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="b2208-134">-Confirm</span></span>
<span data-ttu-id="b2208-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b2208-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2208-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2208-136">-WhatIf</span></span>
<span data-ttu-id="b2208-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2208-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2208-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b2208-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2208-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2208-139">CommonParameters</span></span>
<span data-ttu-id="b2208-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2208-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2208-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b2208-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2208-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2208-142">INPUTS</span></span>

### <span data-ttu-id="b2208-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b2208-143">System.String</span></span>

### <span data-ttu-id="b2208-144">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="b2208-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="b2208-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2208-145">OUTPUTS</span></span>

### <span data-ttu-id="b2208-146">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="b2208-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="b2208-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2208-147">NOTES</span></span>

## <span data-ttu-id="b2208-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2208-148">RELATED LINKS</span></span>
