---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571277"
---
# <span data-ttu-id="974ba-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="974ba-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="974ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="974ba-102">SYNOPSIS</span></span>
<span data-ttu-id="974ba-103">Bir piyasaya çıkma alır.</span><span class="sxs-lookup"><span data-stu-id="974ba-103">Gets a rollout.</span></span>

## <span data-ttu-id="974ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="974ba-104">SYNTAX</span></span>

### <span data-ttu-id="974ba-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="974ba-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="974ba-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="974ba-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="974ba-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="974ba-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="974ba-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="974ba-108">DESCRIPTION</span></span>
<span data-ttu-id="974ba-109">**Get-Azurermdeploymentmanagerpiyasaya** çıkarma cmdlet 'i bir piyasaya alır ve bu sürümü, kademeli olan bilgilerin tüm ayrıntılı bilgileriyle birlikte döndürür.</span><span class="sxs-lookup"><span data-stu-id="974ba-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="974ba-110">Dağıtımı adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="974ba-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="974ba-111">Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="974ba-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="974ba-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="974ba-112">EXAMPLES</span></span>

### <span data-ttu-id="974ba-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="974ba-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="974ba-114">Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır.</span><span class="sxs-lookup"><span data-stu-id="974ba-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="974ba-115">Örnek 2: kaynak tanımlayıcısını kullanarak bir ürün edinin</span><span class="sxs-lookup"><span data-stu-id="974ba-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="974ba-116">Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır.</span><span class="sxs-lookup"><span data-stu-id="974ba-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="974ba-117">Örnek 3: piyasaya çıkarma nesnesini kullanarak bir ürün edinin.</span><span class="sxs-lookup"><span data-stu-id="974ba-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="974ba-118">Bu komut, adı ve ResourceGroup 'in sırasıyla $rolloutObject Name ve ResourceGroupName özellikleriyle eşleşen bir dağıtımı alır.</span><span class="sxs-lookup"><span data-stu-id="974ba-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="974ba-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="974ba-119">PARAMETERS</span></span>

### <span data-ttu-id="974ba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="974ba-120">-DefaultProfile</span></span>
<span data-ttu-id="974ba-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="974ba-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="974ba-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="974ba-122">-Name</span></span>
<span data-ttu-id="974ba-123">Ürün adı.</span><span class="sxs-lookup"><span data-stu-id="974ba-123">The name of the rollout.</span></span>

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

### <span data-ttu-id="974ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="974ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="974ba-125">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="974ba-125">The resource group.</span></span>

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

### <span data-ttu-id="974ba-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="974ba-126">-ResourceId</span></span>
<span data-ttu-id="974ba-127">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="974ba-127">The resource identifier.</span></span>

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

### <span data-ttu-id="974ba-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="974ba-128">-RetryAttempt</span></span>
<span data-ttu-id="974ba-129">Piyasaya yeniden deneme girişimi.</span><span class="sxs-lookup"><span data-stu-id="974ba-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974ba-130">-Ürün</span><span class="sxs-lookup"><span data-stu-id="974ba-130">-Rollout</span></span>
<span data-ttu-id="974ba-131">Piyasaya çıkarma nesnesi.</span><span class="sxs-lookup"><span data-stu-id="974ba-131">Rollout object.</span></span>

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

### <span data-ttu-id="974ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="974ba-132">CommonParameters</span></span>
<span data-ttu-id="974ba-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="974ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="974ba-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="974ba-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="974ba-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="974ba-135">INPUTS</span></span>

### <span data-ttu-id="974ba-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="974ba-136">None</span></span>

## <span data-ttu-id="974ba-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="974ba-137">OUTPUTS</span></span>

### <span data-ttu-id="974ba-138">Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma</span><span class="sxs-lookup"><span data-stu-id="974ba-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="974ba-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="974ba-139">NOTES</span></span>

## <span data-ttu-id="974ba-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="974ba-140">RELATED LINKS</span></span>

[<span data-ttu-id="974ba-141">Stop-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="974ba-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="974ba-142">Restart-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="974ba-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="974ba-143">Remove-Azurermdeploymentmanagerpiyasaya</span><span class="sxs-lookup"><span data-stu-id="974ba-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)