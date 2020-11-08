---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104387"
---
# <span data-ttu-id="af25a-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="af25a-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="af25a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af25a-102">SYNOPSIS</span></span>
<span data-ttu-id="af25a-103">Adımı alır.</span><span class="sxs-lookup"><span data-stu-id="af25a-103">Gets the step.</span></span>

## <span data-ttu-id="af25a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af25a-104">SYNTAX</span></span>

### <span data-ttu-id="af25a-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af25a-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af25a-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="af25a-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af25a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="af25a-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af25a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="af25a-108">DESCRIPTION</span></span>
<span data-ttu-id="af25a-109">**Get-AzDeploymentManagerStep** cmdlet 'i bir adım alır ve bu adımı temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="af25a-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="af25a-110">Adım adını ve kaynak grubu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="af25a-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="af25a-111">Alternatif olarak, Step nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af25a-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="af25a-112">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerStep cmdlet 'ini kullanarak yapı kaynağına değişiklikleri uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af25a-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="af25a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af25a-113">EXAMPLES</span></span>

### <span data-ttu-id="af25a-114">Örnek 1: adım alma</span><span class="sxs-lookup"><span data-stu-id="af25a-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="af25a-115">Bu komut, ContosoResourceGroup 'da ContosoService1WaitStep adındaki bir adımı alır.</span><span class="sxs-lookup"><span data-stu-id="af25a-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="af25a-116">Örnek 2: kaynak tanımlayıcısını kullanarak bir adım alma</span><span class="sxs-lookup"><span data-stu-id="af25a-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="af25a-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af25a-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="af25a-118">Bu komut, ContosoResourceGroup 'da ContosoService1WaitStep adındaki bir adımı alır.</span><span class="sxs-lookup"><span data-stu-id="af25a-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="af25a-119">Örnek 3: New-AzDeploymentManagerStep tarafından döndürülen bir nesneyi kullanarak adım alma</span><span class="sxs-lookup"><span data-stu-id="af25a-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="af25a-120">Bu komut, adı ve ResourceGroup 'in sırasıyla $stepObject Name ve ResourceGroupName özellikleriyle eşleşen bir adımını alır.</span><span class="sxs-lookup"><span data-stu-id="af25a-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="af25a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af25a-121">PARAMETERS</span></span>

### <span data-ttu-id="af25a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af25a-122">-DefaultProfile</span></span>
<span data-ttu-id="af25a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af25a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af25a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af25a-124">-InputObject</span></span>
<span data-ttu-id="af25a-125">Adım kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="af25a-125">The step resource object.</span></span>

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

### <span data-ttu-id="af25a-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="af25a-126">-Name</span></span>
<span data-ttu-id="af25a-127">Adımın adı.</span><span class="sxs-lookup"><span data-stu-id="af25a-127">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af25a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af25a-128">-ResourceGroupName</span></span>
<span data-ttu-id="af25a-129">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="af25a-129">The resource group.</span></span>

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

### <span data-ttu-id="af25a-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="af25a-130">-ResourceId</span></span>
<span data-ttu-id="af25a-131">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="af25a-131">The resource identifier.</span></span>

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

### <span data-ttu-id="af25a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af25a-132">CommonParameters</span></span>
<span data-ttu-id="af25a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af25a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af25a-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="af25a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af25a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af25a-135">INPUTS</span></span>

### <span data-ttu-id="af25a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="af25a-136">System.String</span></span>

### <span data-ttu-id="af25a-137">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="af25a-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="af25a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af25a-138">OUTPUTS</span></span>

### <span data-ttu-id="af25a-139">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="af25a-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="af25a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af25a-140">NOTES</span></span>

## <span data-ttu-id="af25a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af25a-141">RELATED LINKS</span></span>
