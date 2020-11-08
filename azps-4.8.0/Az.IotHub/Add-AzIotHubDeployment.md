---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267452"
---
# <span data-ttu-id="7cd72-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="7cd72-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="7cd72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cd72-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd72-103">Hedef IoT Hub 'ına IoT uç dağıtımı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7cd72-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="7cd72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7cd72-104">SYNTAX</span></span>

### <span data-ttu-id="7cd72-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7cd72-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd72-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="7cd72-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cd72-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="7cd72-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd72-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7cd72-108">DESCRIPTION</span></span>
<span data-ttu-id="7cd72-109">Edge dağıtımları, isteğe bağlı değerlendirme için Kullanıcı tanımlı ölçümler ile oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="7cd72-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="7cd72-110"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="7cd72-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="7cd72-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7cd72-111">EXAMPLES</span></span>

### <span data-ttu-id="7cd72-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7cd72-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="7cd72-113">Varsayılan meta veriler içeren bir kenar dağıtımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7cd72-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="7cd72-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7cd72-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="7cd72-115">Bir cihaz 9 ' un içinde etiketlenmişse ve ortam ' test ' olduğunda, bir öncelik 3 olan bir kenar dağıtımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7cd72-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="7cd72-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7cd72-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="7cd72-117">Kullanıcı ölçümlerine sahip bir kenar dağıtımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7cd72-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="7cd72-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="7cd72-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="7cd72-119">Etiketlerle bir kenar dağıtımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7cd72-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="7cd72-120">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="7cd72-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="7cd72-121">İçerikle bir kenar dağıtımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7cd72-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="7cd72-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7cd72-122">PARAMETERS</span></span>

### <span data-ttu-id="7cd72-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd72-123">-DefaultProfile</span></span>
<span data-ttu-id="7cd72-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7cd72-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cd72-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cd72-125">-InputObject</span></span>
<span data-ttu-id="7cd72-126">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="7cd72-126">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-127">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="7cd72-127">-IotHubName</span></span>
<span data-ttu-id="7cd72-128">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="7cd72-128">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7cd72-129">-Label</span></span>
<span data-ttu-id="7cd72-130">Hedef dağıtıma uygulanacak etiketlerin haritası.</span><span class="sxs-lookup"><span data-stu-id="7cd72-130">Map of labels to be applied to target deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-131">-Metrik</span><span class="sxs-lookup"><span data-stu-id="7cd72-131">-Metric</span></span>
<span data-ttu-id="7cd72-132">IoT Edge dağıtım ölçümleri tanımı için sorgular koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="7cd72-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="7cd72-133">-ModulesContent</span></span>
<span data-ttu-id="7cd72-134">IoT Edge cihazları için modüllerin dağıtım içeriği.</span><span class="sxs-lookup"><span data-stu-id="7cd72-134">Deployment content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="7cd72-135">-Name</span></span>
<span data-ttu-id="7cd72-136">Dağıtımın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7cd72-136">Identifier for the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-137">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="7cd72-137">-Priority</span></span>
<span data-ttu-id="7cd72-138">Rekabet kuralları (en yüksek WINS) durumunda dağıtımın ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="7cd72-138">Weight of deployment in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd72-139">-ResourceGroupName</span></span>
<span data-ttu-id="7cd72-140">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="7cd72-140">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7cd72-141">-ResourceId</span></span>
<span data-ttu-id="7cd72-142">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7cd72-142">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="7cd72-143">-TargetCondition</span></span>
<span data-ttu-id="7cd72-144">Bir Edge dağıtımının uygulandığı hedef koşulu.</span><span class="sxs-lookup"><span data-stu-id="7cd72-144">Target condition in which an Edge deployment applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd72-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="7cd72-145">-Confirm</span></span>
<span data-ttu-id="7cd72-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7cd72-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd72-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd72-147">-WhatIf</span></span>
<span data-ttu-id="7cd72-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cd72-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd72-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7cd72-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cd72-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd72-150">CommonParameters</span></span>
<span data-ttu-id="7cd72-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7cd72-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd72-152">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd72-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd72-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7cd72-153">INPUTS</span></span>

### <span data-ttu-id="7cd72-154">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="7cd72-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7cd72-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7cd72-155">System.String</span></span>

## <span data-ttu-id="7cd72-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7cd72-156">OUTPUTS</span></span>

### <span data-ttu-id="7cd72-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="7cd72-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="7cd72-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7cd72-158">NOTES</span></span>

## <span data-ttu-id="7cd72-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7cd72-159">RELATED LINKS</span></span>
