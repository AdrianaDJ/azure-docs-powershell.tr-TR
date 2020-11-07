---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: eb0c7db4706aacfba4010632422869f0dca54694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752141"
---
# <span data-ttu-id="fa168-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="fa168-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="fa168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa168-102">SYNOPSIS</span></span>
<span data-ttu-id="fa168-103">Adımı alır.</span><span class="sxs-lookup"><span data-stu-id="fa168-103">Gets the step.</span></span>

## <span data-ttu-id="fa168-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa168-104">SYNTAX</span></span>

### <span data-ttu-id="fa168-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa168-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa168-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="fa168-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa168-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fa168-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa168-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa168-108">DESCRIPTION</span></span>
<span data-ttu-id="fa168-109">**Get-AzDeploymentManagerStep** cmdlet 'i bir adım alır ve bu adımı temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fa168-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="fa168-110">Adım adını ve kaynak grubu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="fa168-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="fa168-111">Alternatif olarak, Step nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa168-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="fa168-112">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerStep cmdlet 'ini kullanarak yapı kaynağına değişiklikleri uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa168-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="fa168-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa168-113">EXAMPLES</span></span>

### <span data-ttu-id="fa168-114">Örnek 1: adım alma</span><span class="sxs-lookup"><span data-stu-id="fa168-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="fa168-115">Bu komut, ContosoResourceGroup 'da ContosoService1WaitStep adındaki bir adımı alır.</span><span class="sxs-lookup"><span data-stu-id="fa168-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="fa168-116">Örnek 2: kaynak tanımlayıcısını kullanarak bir adım alma</span><span class="sxs-lookup"><span data-stu-id="fa168-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="fa168-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fa168-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="fa168-118">Bu komut, ContosoResourceGroup 'da ContosoService1WaitStep adındaki bir adımı alır.</span><span class="sxs-lookup"><span data-stu-id="fa168-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="fa168-119">Örnek 3: New-AzDeploymentManagerStep tarafından döndürülen bir nesneyi kullanarak adım alma</span><span class="sxs-lookup"><span data-stu-id="fa168-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="fa168-120">Bu komut, adı ve ResourceGroup 'in sırasıyla $stepObject Name ve ResourceGroupName özellikleriyle eşleşen bir adımını alır.</span><span class="sxs-lookup"><span data-stu-id="fa168-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="fa168-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa168-121">PARAMETERS</span></span>

### <span data-ttu-id="fa168-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa168-122">-DefaultProfile</span></span>
<span data-ttu-id="fa168-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa168-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa168-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa168-124">-InputObject</span></span>
<span data-ttu-id="fa168-125">Adım kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fa168-125">The step resource object.</span></span>

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

### <span data-ttu-id="fa168-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa168-126">-Name</span></span>
<span data-ttu-id="fa168-127">Adımın adı.</span><span class="sxs-lookup"><span data-stu-id="fa168-127">The name of the step.</span></span>

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

### <span data-ttu-id="fa168-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa168-128">-ResourceGroupName</span></span>
<span data-ttu-id="fa168-129">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fa168-129">The resource group.</span></span>

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

### <span data-ttu-id="fa168-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fa168-130">-ResourceId</span></span>
<span data-ttu-id="fa168-131">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="fa168-131">The resource identifier.</span></span>

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

### <span data-ttu-id="fa168-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa168-132">CommonParameters</span></span>
<span data-ttu-id="fa168-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa168-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa168-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa168-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa168-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa168-135">INPUTS</span></span>

### <span data-ttu-id="fa168-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fa168-136">System.String</span></span>

### <span data-ttu-id="fa168-137">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="fa168-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="fa168-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa168-138">OUTPUTS</span></span>

### <span data-ttu-id="fa168-139">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="fa168-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="fa168-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa168-140">NOTES</span></span>

## <span data-ttu-id="fa168-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa168-141">RELATED LINKS</span></span>