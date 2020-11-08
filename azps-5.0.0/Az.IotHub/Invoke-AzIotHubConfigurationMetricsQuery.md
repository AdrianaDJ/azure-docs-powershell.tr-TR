---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280268"
---
# <span data-ttu-id="e737c-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="e737c-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="e737c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e737c-102">SYNOPSIS</span></span>
<span data-ttu-id="e737c-103">IoT cihaz yapılandırma ölçümü sorgusunu çağırın.</span><span class="sxs-lookup"><span data-stu-id="e737c-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="e737c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e737c-104">SYNTAX</span></span>

### <span data-ttu-id="e737c-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e737c-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e737c-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="e737c-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e737c-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="e737c-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e737c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e737c-108">DESCRIPTION</span></span>
<span data-ttu-id="e737c-109">IoT cihaz yapılandırmasında tanımlanan bir hedef özel veya sistem ölçüsünü değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="e737c-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="e737c-110">IoT Hub tarafından hesaplanan ve özelleştirilebilecek önceden tanımlanmış sistem ölçümleri vardır.</span><span class="sxs-lookup"><span data-stu-id="e737c-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="e737c-111">"Hedefli" hedef koşulla eşleşen aygıt TWINS sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e737c-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="e737c-112">"Uygulandı" belirtildi, yapılandırma tarafından değiştirilmiş olan aygıt TWINS sayısı.</span><span class="sxs-lookup"><span data-stu-id="e737c-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="e737c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e737c-113">EXAMPLES</span></span>

### <span data-ttu-id="e737c-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e737c-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="e737c-115">Özel tanımlanmış ' warningLimit ' ölçüsünü değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="e737c-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="e737c-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e737c-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="e737c-117">Sistemin "uyguladığı" ölçüsünü değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="e737c-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="e737c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e737c-118">PARAMETERS</span></span>

### <span data-ttu-id="e737c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e737c-119">-DefaultProfile</span></span>
<span data-ttu-id="e737c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e737c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e737c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e737c-121">-InputObject</span></span>
<span data-ttu-id="e737c-122">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="e737c-122">IotHub object</span></span>

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

### <span data-ttu-id="e737c-123">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="e737c-123">-IotHubName</span></span>
<span data-ttu-id="e737c-124">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="e737c-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e737c-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="e737c-125">-MetricName</span></span>
<span data-ttu-id="e737c-126">Değerlendirme için hedef ölçümü.</span><span class="sxs-lookup"><span data-stu-id="e737c-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="e737c-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="e737c-127">-MetricType</span></span>
<span data-ttu-id="e737c-128">Bir ölçüyü aramak için hangi ölçüm koleksiyonunun kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e737c-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="e737c-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="e737c-129">-Name</span></span>
<span data-ttu-id="e737c-130">Yapılandırma kimliği.</span><span class="sxs-lookup"><span data-stu-id="e737c-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="e737c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e737c-131">-ResourceGroupName</span></span>
<span data-ttu-id="e737c-132">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="e737c-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e737c-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e737c-133">-ResourceId</span></span>
<span data-ttu-id="e737c-134">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e737c-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e737c-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="e737c-135">-Confirm</span></span>
<span data-ttu-id="e737c-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e737c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e737c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e737c-137">-WhatIf</span></span>
<span data-ttu-id="e737c-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e737c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e737c-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e737c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e737c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e737c-140">CommonParameters</span></span>
<span data-ttu-id="e737c-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e737c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e737c-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e737c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e737c-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e737c-143">INPUTS</span></span>

### <span data-ttu-id="e737c-144">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="e737c-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e737c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e737c-145">System.String</span></span>

## <span data-ttu-id="e737c-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e737c-146">OUTPUTS</span></span>

### <span data-ttu-id="e737c-147">Microsoft. Azure. Commands. Management. IotHub. modeller. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="e737c-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="e737c-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e737c-148">NOTES</span></span>

## <span data-ttu-id="e737c-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e737c-149">RELATED LINKS</span></span>
