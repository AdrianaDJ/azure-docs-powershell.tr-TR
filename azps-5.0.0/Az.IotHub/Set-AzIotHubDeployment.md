---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 1fac3ef0db0022bcb837392bf1c0b64e63c40401
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280251"
---
# <span data-ttu-id="b80e7-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="b80e7-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="b80e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b80e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b80e7-103">IoT Edge dağıtımının kesilebilir alanlarını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="b80e7-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="b80e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b80e7-104">SYNTAX</span></span>

### <span data-ttu-id="b80e7-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b80e7-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b80e7-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="b80e7-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b80e7-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="b80e7-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b80e7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b80e7-108">DESCRIPTION</span></span>
<span data-ttu-id="b80e7-109">IoT Edge dağıtımının belirtilen özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="b80e7-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="b80e7-110">Not: yapılandırma içeriği sabittir.</span><span class="sxs-lookup"><span data-stu-id="b80e7-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="b80e7-111">Güncelleştirilebilen yapılandırma özellikleri ' Etiketler ', ' ölçümler ', ' öncelik ' ve ' Targetkoşul '.</span><span class="sxs-lookup"><span data-stu-id="b80e7-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="b80e7-112"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="b80e7-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="b80e7-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b80e7-113">EXAMPLES</span></span>

### <span data-ttu-id="b80e7-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b80e7-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="b80e7-115">IoT Edge dağıtımının önceliğini değiştirin ve hedef koşulunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="b80e7-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

## <span data-ttu-id="b80e7-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b80e7-116">PARAMETERS</span></span>

### <span data-ttu-id="b80e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80e7-117">-DefaultProfile</span></span>
<span data-ttu-id="b80e7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b80e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b80e7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b80e7-119">-Force</span></span>
<span data-ttu-id="b80e7-120">En son alındığı zamandan beri güncelleştirilmiş olsa bile dağıtım nesnesinin değiştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="b80e7-120">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="b80e7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b80e7-121">-InputObject</span></span>
<span data-ttu-id="b80e7-122">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="b80e7-122">IotHub object</span></span>

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

### <span data-ttu-id="b80e7-123">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="b80e7-123">-IotHubName</span></span>
<span data-ttu-id="b80e7-124">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="b80e7-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b80e7-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b80e7-125">-Label</span></span>
<span data-ttu-id="b80e7-126">Hedef dağıtıma uygulanacak etiketlerin haritası.</span><span class="sxs-lookup"><span data-stu-id="b80e7-126">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="b80e7-127">-Metrik</span><span class="sxs-lookup"><span data-stu-id="b80e7-127">-Metric</span></span>
<span data-ttu-id="b80e7-128">IoT Edge dağıtım ölçümleri tanımı için sorgular koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="b80e7-128">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="b80e7-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="b80e7-129">-Name</span></span>
<span data-ttu-id="b80e7-130">Dağıtımın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b80e7-130">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="b80e7-131">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="b80e7-131">-Priority</span></span>
<span data-ttu-id="b80e7-132">Rekabet kuralları (en yüksek WINS) durumunda dağıtımın ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="b80e7-132">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="b80e7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b80e7-133">-ResourceGroupName</span></span>
<span data-ttu-id="b80e7-134">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b80e7-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b80e7-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b80e7-135">-ResourceId</span></span>
<span data-ttu-id="b80e7-136">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b80e7-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b80e7-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="b80e7-137">-TargetCondition</span></span>
<span data-ttu-id="b80e7-138">Bir Edge dağıtımının uygulandığı hedef koşulu.</span><span class="sxs-lookup"><span data-stu-id="b80e7-138">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="b80e7-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="b80e7-139">-Confirm</span></span>
<span data-ttu-id="b80e7-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b80e7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b80e7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b80e7-141">-WhatIf</span></span>
<span data-ttu-id="b80e7-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b80e7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b80e7-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b80e7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b80e7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80e7-144">CommonParameters</span></span>
<span data-ttu-id="b80e7-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b80e7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b80e7-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b80e7-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80e7-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b80e7-147">INPUTS</span></span>

### <span data-ttu-id="b80e7-148">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="b80e7-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b80e7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b80e7-149">System.String</span></span>

## <span data-ttu-id="b80e7-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b80e7-150">OUTPUTS</span></span>

### <span data-ttu-id="b80e7-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeplote</span><span class="sxs-lookup"><span data-stu-id="b80e7-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="b80e7-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b80e7-152">NOTES</span></span>

## <span data-ttu-id="b80e7-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b80e7-153">RELATED LINKS</span></span>
