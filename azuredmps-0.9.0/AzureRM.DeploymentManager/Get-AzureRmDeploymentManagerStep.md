---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571530"
---
# <span data-ttu-id="f0e8b-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f0e8b-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="f0e8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e8b-103">Dağıtım adımını alır.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-103">Gets the deployment step.</span></span>

## <span data-ttu-id="f0e8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0e8b-104">SYNTAX</span></span>

### <span data-ttu-id="f0e8b-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0e8b-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e8b-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f0e8b-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0e8b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f0e8b-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0e8b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0e8b-108">DESCRIPTION</span></span>
<span data-ttu-id="f0e8b-109">**Get-AzureRmDeploymentManagerStep** cmdlet 'i bir adım alır ve bu adımı temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="f0e8b-110">Adım adını ve kaynak grubu adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="f0e8b-111">Alternatif olarak, Step nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="f0e8b-112">Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerStep cmdlet 'ini kullanarak yapı kaynağına değişiklikleri uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="f0e8b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0e8b-113">EXAMPLES</span></span>

### <span data-ttu-id="f0e8b-114">Örnek 1: adım alma</span><span class="sxs-lookup"><span data-stu-id="f0e8b-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="f0e8b-115">Bu komut, ContosoResourceGroup 'da ContosoService1WaitStep adındaki bir adımı alır.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f0e8b-116">Örnek 2: kaynak tanımlayıcısını kullanarak bir adım alma</span><span class="sxs-lookup"><span data-stu-id="f0e8b-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="f0e8b-117">Bu komut, ContosoResourceGroup 'da ContosoService1WaitStep adındaki bir adımı alır.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f0e8b-118">Örnek 3: New-AzureRmDeploymentManagerStep tarafından döndürülen bir nesneyi kullanarak adım alma</span><span class="sxs-lookup"><span data-stu-id="f0e8b-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="f0e8b-119">Bu komut, adı ve ResourceGroup 'in sırasıyla $stepObject Name ve ResourceGroupName özellikleriyle eşleşen bir adımını alır.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="f0e8b-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0e8b-120">PARAMETERS</span></span>

### <span data-ttu-id="f0e8b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e8b-121">-DefaultProfile</span></span>
<span data-ttu-id="f0e8b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0e8b-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0e8b-123">-Name</span></span>
<span data-ttu-id="f0e8b-124">Adımın adı.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-124">The name of the step.</span></span>

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

### <span data-ttu-id="f0e8b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e8b-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0e8b-126">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-126">The resource group.</span></span>

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

### <span data-ttu-id="f0e8b-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f0e8b-127">-ResourceId</span></span>
<span data-ttu-id="f0e8b-128">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-128">The resource identifier.</span></span>

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

### <span data-ttu-id="f0e8b-129">-Adım</span><span class="sxs-lookup"><span data-stu-id="f0e8b-129">-Step</span></span>
<span data-ttu-id="f0e8b-130">Adım kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-130">The step resource object.</span></span>

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

### <span data-ttu-id="f0e8b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e8b-131">CommonParameters</span></span>
<span data-ttu-id="f0e8b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0e8b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f0e8b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e8b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e8b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0e8b-134">INPUTS</span></span>

### <span data-ttu-id="f0e8b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f0e8b-135">System.String</span></span>

### <span data-ttu-id="f0e8b-136">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f0e8b-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f0e8b-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0e8b-137">OUTPUTS</span></span>

### <span data-ttu-id="f0e8b-138">Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f0e8b-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f0e8b-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0e8b-139">NOTES</span></span>

## <span data-ttu-id="f0e8b-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0e8b-140">RELATED LINKS</span></span>
