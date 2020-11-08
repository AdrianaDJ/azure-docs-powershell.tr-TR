---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267459"
---
# <span data-ttu-id="42d59-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d59-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="42d59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d59-102">SYNOPSIS</span></span>
<span data-ttu-id="42d59-103">Bir hedef IoT Hub 'ına bir IoT otomatik cihaz yönetimi yapılandırması ekleyin.</span><span class="sxs-lookup"><span data-stu-id="42d59-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="42d59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42d59-104">SYNTAX</span></span>

### <span data-ttu-id="42d59-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42d59-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d59-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="42d59-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d59-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="42d59-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42d59-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="42d59-108">DESCRIPTION</span></span>
<span data-ttu-id="42d59-109">Yapılandırma içeriği JSON ve diğer modül amacına göre değişir.</span><span class="sxs-lookup"><span data-stu-id="42d59-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="42d59-110">Cihaz yapılandırmaları {"deviceContent" biçiminde, {...}}</span><span class="sxs-lookup"><span data-stu-id="42d59-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="42d59-111">Modül yapılandırmaları {"moduleContent" biçiminde, {...}}</span><span class="sxs-lookup"><span data-stu-id="42d59-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="42d59-112">Yapılandırmalar, isteğe bağlı değerlendirme için Kullanıcı tarafından sağlanan ölçümler ile tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="42d59-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="42d59-113">Kullanıcı ölçümleri JSON ve {"queries": {...}} biçiminde</span><span class="sxs-lookup"><span data-stu-id="42d59-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="42d59-114">veya {"ölçüler": {"queries": {...}}}.</span><span class="sxs-lookup"><span data-stu-id="42d59-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="42d59-115">Not: modüller için hedef durumunun "from Devices. modüller where" ile başlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="42d59-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="42d59-116"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="42d59-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="42d59-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42d59-117">EXAMPLES</span></span>

### <span data-ttu-id="42d59-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="42d59-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="42d59-119">Varsayılan meta verilerle bir cihaz yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="42d59-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="42d59-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="42d59-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="42d59-121">Bir cihaz 9 ' da etiketlenmişse ve ortam ' test ' olduğunda, bir öncelik 3 olan bir cihaz yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="42d59-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="42d59-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="42d59-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="42d59-123">Kullanıcı ölçümlerine sahip bir cihaz yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="42d59-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="42d59-124">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="42d59-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="42d59-125">Etiketlerle bir cihaz yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="42d59-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="42d59-126">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="42d59-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="42d59-127">İçerikle bir cihaz yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="42d59-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="42d59-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42d59-128">PARAMETERS</span></span>

### <span data-ttu-id="42d59-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d59-129">-DefaultProfile</span></span>
<span data-ttu-id="42d59-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42d59-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42d59-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="42d59-131">-DeviceContent</span></span>
<span data-ttu-id="42d59-132">IotHub aygıtlarının yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="42d59-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="42d59-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42d59-133">-InputObject</span></span>
<span data-ttu-id="42d59-134">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="42d59-134">IotHub object</span></span>

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

### <span data-ttu-id="42d59-135">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="42d59-135">-IotHubName</span></span>
<span data-ttu-id="42d59-136">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="42d59-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="42d59-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="42d59-137">-Label</span></span>
<span data-ttu-id="42d59-138">Hedef yapılandırmaya uygulanacak etiketlerin haritası.</span><span class="sxs-lookup"><span data-stu-id="42d59-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="42d59-139">-Metrik</span><span class="sxs-lookup"><span data-stu-id="42d59-139">-Metric</span></span>
<span data-ttu-id="42d59-140">Yapılandırma ölçümleri tanımı için sorgular koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="42d59-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="42d59-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="42d59-141">-Name</span></span>
<span data-ttu-id="42d59-142">Yapılandırma kimliği.</span><span class="sxs-lookup"><span data-stu-id="42d59-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="42d59-143">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="42d59-143">-Priority</span></span>
<span data-ttu-id="42d59-144">Rekabet kuralları (en yüksek WINS) durumunda cihaz yapılandırmasının ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="42d59-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="42d59-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d59-145">-ResourceGroupName</span></span>
<span data-ttu-id="42d59-146">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="42d59-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="42d59-147">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="42d59-147">-ResourceId</span></span>
<span data-ttu-id="42d59-148">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="42d59-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="42d59-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="42d59-149">-TargetCondition</span></span>
<span data-ttu-id="42d59-150">Cihaz yapılandırmasının uygulandığı hedef koşulu.</span><span class="sxs-lookup"><span data-stu-id="42d59-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="42d59-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="42d59-151">-Confirm</span></span>
<span data-ttu-id="42d59-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42d59-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d59-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d59-153">-WhatIf</span></span>
<span data-ttu-id="42d59-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42d59-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d59-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42d59-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d59-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d59-156">CommonParameters</span></span>
<span data-ttu-id="42d59-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42d59-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d59-158">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d59-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d59-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42d59-159">INPUTS</span></span>

### <span data-ttu-id="42d59-160">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="42d59-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="42d59-161">System. String</span><span class="sxs-lookup"><span data-stu-id="42d59-161">System.String</span></span>

## <span data-ttu-id="42d59-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42d59-162">OUTPUTS</span></span>

### <span data-ttu-id="42d59-163">Microsoft. Azure. Commands. Management. IotHub. modeller. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="42d59-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="42d59-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42d59-164">NOTES</span></span>

## <span data-ttu-id="42d59-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42d59-165">RELATED LINKS</span></span>
