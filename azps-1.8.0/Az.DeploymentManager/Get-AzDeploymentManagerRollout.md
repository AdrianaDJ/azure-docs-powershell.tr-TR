---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: fbcb93ec75dc0e136c1c18743a8686f7642ef02f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761008"
---
# <span data-ttu-id="4eb5c-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="4eb5c-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="4eb5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb5c-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb5c-103">Dağıtımı alır.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-103">Gets the rollout.</span></span>

## <span data-ttu-id="4eb5c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4eb5c-104">SYNTAX</span></span>

### <span data-ttu-id="4eb5c-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4eb5c-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4eb5c-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="4eb5c-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4eb5c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb5c-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4eb5c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4eb5c-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb5c-109">**Get-Azdeploymentmanagerpiyasaya dağıtım** cmdlet 'i bir piyasaya alır ve bu sürümü, piyasaya çıkarma işleminin ilerleme durumuyla ilgili tüm ayrıntılı bilgilerle birlikte döndürür.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="4eb5c-110">Dağıtımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="4eb5c-111">Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="4eb5c-112">Döndürülen dağıtım nesnesi, dağıtılan Hizmetleri, hizmet birimlerini ve adımları ve sürmekte olan adımları içerir.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="4eb5c-113">Henüz dağıtılmayan olanlar yanıt vermiyor.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="4eb5c-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4eb5c-114">EXAMPLES</span></span>

### <span data-ttu-id="4eb5c-115">Örnek 1 dağıtımı alın</span><span class="sxs-lookup"><span data-stu-id="4eb5c-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="4eb5c-116">Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="4eb5c-117">Örnek 2 dağıtım ayrıntılarını alma ve görüntüleme</span><span class="sxs-lookup"><span data-stu-id="4eb5c-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="4eb5c-118">Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="4eb5c-119">-Verbose anahtarı tüm dağıtım ayrıntılarını hiyerarşik olarak görüntüler; Hizmetin, hizmet birimlerinin ve her bir Holistic görünümü için her adımın altındaki adımları gösterin.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="4eb5c-120">Örnek 3: kaynak tanımlayıcısını kullanarak bir ürün edinin</span><span class="sxs-lookup"><span data-stu-id="4eb5c-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="4eb5c-121">Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4eb5c-122">Örnek 4: piyasaya çıkarma nesnesini kullanarak bir ürün edinin.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="4eb5c-123">Bu komut, adı ve ResourceGroup 'in sırasıyla $rolloutObject Name ve ResourceGroupName özellikleriyle eşleşen bir dağıtımı alır.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="4eb5c-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4eb5c-124">PARAMETERS</span></span>

### <span data-ttu-id="4eb5c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb5c-125">-DefaultProfile</span></span>
<span data-ttu-id="4eb5c-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb5c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb5c-127">-InputObject</span></span>
<span data-ttu-id="4eb5c-128">Piyasaya çıkarma nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-128">Rollout object.</span></span>

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

### <span data-ttu-id="4eb5c-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="4eb5c-129">-Name</span></span>
<span data-ttu-id="4eb5c-130">Ürün adı.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="4eb5c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb5c-131">-ResourceGroupName</span></span>
<span data-ttu-id="4eb5c-132">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-132">The resource group.</span></span>

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

### <span data-ttu-id="4eb5c-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4eb5c-133">-ResourceId</span></span>
<span data-ttu-id="4eb5c-134">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-134">The resource identifier.</span></span>

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

### <span data-ttu-id="4eb5c-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="4eb5c-135">-RetryAttempt</span></span>
<span data-ttu-id="4eb5c-136">Piyasaya yeniden deneme girişimi.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb5c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb5c-137">CommonParameters</span></span>
<span data-ttu-id="4eb5c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4eb5c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb5c-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb5c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb5c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4eb5c-140">INPUTS</span></span>

### <span data-ttu-id="4eb5c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4eb5c-141">System.String</span></span>

### <span data-ttu-id="4eb5c-142">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4eb5c-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4eb5c-143">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="4eb5c-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="4eb5c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4eb5c-144">OUTPUTS</span></span>

### <span data-ttu-id="4eb5c-145">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="4eb5c-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="4eb5c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4eb5c-146">NOTES</span></span>

## <span data-ttu-id="4eb5c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4eb5c-147">RELATED LINKS</span></span>
