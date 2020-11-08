---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274919"
---
# <span data-ttu-id="d157f-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="d157f-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="d157f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d157f-102">SYNOPSIS</span></span>
<span data-ttu-id="d157f-103">IoT Edge dağıtım ölçümü sorgusunu çağırma.</span><span class="sxs-lookup"><span data-stu-id="d157f-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="d157f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d157f-104">SYNTAX</span></span>

### <span data-ttu-id="d157f-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d157f-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d157f-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="d157f-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d157f-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="d157f-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d157f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d157f-108">DESCRIPTION</span></span>
<span data-ttu-id="d157f-109">IoT Edge dağıtımında tanımlanan bir hedef özel veya sistem ölçüsünü değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="d157f-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="d157f-110">IoT Hub tarafından hesaplanan ve özelleştirilebilecek önceden tanımlanmış sistem ölçümleri vardır.</span><span class="sxs-lookup"><span data-stu-id="d157f-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="d157f-111">"Hedefli" dağıtım hedefleme durumuyla eşleşen IoT Edge aygıtlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d157f-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="d157f-112">"Uygulandı", daha yüksek önceliğe sahip bir dağıtımın hedeflediği hedeflenen IoT Edge cihazlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d157f-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="d157f-113">"Raporlama başarısı", modüllerin başarıyla dağıtıldığını bildiren IoT Edge cihazlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d157f-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="d157f-114">"Raporlama hatası", bir veya daha fazla modülün başarıyla dağıtılamadığını bildiren IoT Edge cihazlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d157f-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="d157f-115">Hatayı daha da araştırmak için, bu aygıtlara uzaktan bağlanın ve günlük dosyalarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="d157f-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="d157f-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d157f-116">EXAMPLES</span></span>

### <span data-ttu-id="d157f-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d157f-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="d157f-118">Özel tanımlanmış ' warningLimit ' ölçüsünü değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="d157f-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="d157f-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d157f-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="d157f-120">Sistemin raporlama başarısı ' ölçüsünü değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="d157f-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="d157f-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d157f-121">PARAMETERS</span></span>

### <span data-ttu-id="d157f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d157f-122">-DefaultProfile</span></span>
<span data-ttu-id="d157f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d157f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d157f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d157f-124">-InputObject</span></span>
<span data-ttu-id="d157f-125">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="d157f-125">IotHub object</span></span>

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

### <span data-ttu-id="d157f-126">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="d157f-126">-IotHubName</span></span>
<span data-ttu-id="d157f-127">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="d157f-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d157f-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="d157f-128">-MetricName</span></span>
<span data-ttu-id="d157f-129">Değerlendirme için hedef ölçümü.</span><span class="sxs-lookup"><span data-stu-id="d157f-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="d157f-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="d157f-130">-MetricType</span></span>
<span data-ttu-id="d157f-131">Bir ölçüyü aramak için hangi ölçüm koleksiyonunun kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d157f-131">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d157f-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="d157f-132">-Name</span></span>
<span data-ttu-id="d157f-133">Dağıtımın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d157f-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="d157f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d157f-134">-ResourceGroupName</span></span>
<span data-ttu-id="d157f-135">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d157f-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d157f-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d157f-136">-ResourceId</span></span>
<span data-ttu-id="d157f-137">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d157f-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d157f-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="d157f-138">-Confirm</span></span>
<span data-ttu-id="d157f-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d157f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d157f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d157f-140">-WhatIf</span></span>
<span data-ttu-id="d157f-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d157f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d157f-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d157f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d157f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d157f-143">CommonParameters</span></span>
<span data-ttu-id="d157f-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d157f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d157f-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d157f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d157f-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d157f-146">INPUTS</span></span>

### <span data-ttu-id="d157f-147">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="d157f-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d157f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d157f-148">System.String</span></span>

## <span data-ttu-id="d157f-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d157f-149">OUTPUTS</span></span>

### <span data-ttu-id="d157f-150">Microsoft. Azure. Commands. Management. IotHub. modeller. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="d157f-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="d157f-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d157f-151">NOTES</span></span>

## <span data-ttu-id="d157f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d157f-152">RELATED LINKS</span></span>
