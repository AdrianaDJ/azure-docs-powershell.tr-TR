---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275492"
---
# <span data-ttu-id="dacb2-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="dacb2-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="dacb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dacb2-102">SYNOPSIS</span></span>
<span data-ttu-id="dacb2-103">Bir cihaz kaydı kaydını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="dacb2-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="dacb2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dacb2-104">SYNTAX</span></span>

### <span data-ttu-id="dacb2-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dacb2-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dacb2-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="dacb2-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dacb2-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="dacb2-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dacb2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dacb2-108">DESCRIPTION</span></span>
<span data-ttu-id="dacb2-109">Bir Azure IoT Hub cihaz sağlama hizmetinde bir cihaz kaydını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="dacb2-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="dacb2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dacb2-110">EXAMPLES</span></span>

### <span data-ttu-id="dacb2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dacb2-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="dacb2-112">Kayıt kaydı için ayırma ilkesini ve hubları güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="dacb2-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="dacb2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dacb2-113">PARAMETERS</span></span>

### <span data-ttu-id="dacb2-114">-Ayıra Ilkesi</span><span class="sxs-lookup"><span data-stu-id="dacb2-114">-AllocationPolicy</span></span>
<span data-ttu-id="dacb2-115">Hub 'a atanan cihazın tahsis türü.</span><span class="sxs-lookup"><span data-stu-id="dacb2-115">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacb2-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="dacb2-116">-ApiVersion</span></span>
<span data-ttu-id="dacb2-117">Özel tahsisat isteğindeki sağlama hizmetinin API sürümü.</span><span class="sxs-lookup"><span data-stu-id="dacb2-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="dacb2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacb2-118">-DefaultProfile</span></span>
<span data-ttu-id="dacb2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dacb2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dacb2-120">-İstenilen</span><span class="sxs-lookup"><span data-stu-id="dacb2-120">-Desired</span></span>
<span data-ttu-id="dacb2-121">İlk ikili istenen özellikler.</span><span class="sxs-lookup"><span data-stu-id="dacb2-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="dacb2-122">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="dacb2-122">-DeviceId</span></span>
<span data-ttu-id="dacb2-123">IoT Hub cihazı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dacb2-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="dacb2-124">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="dacb2-124">-DpsName</span></span>
<span data-ttu-id="dacb2-125">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="dacb2-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="dacb2-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="dacb2-126">-DpsObject</span></span>
<span data-ttu-id="dacb2-127">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="dacb2-127">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dacb2-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="dacb2-128">-EdgeEnabled</span></span>
<span data-ttu-id="dacb2-129">Kenarı etkinleştirme bayrağı.</span><span class="sxs-lookup"><span data-stu-id="dacb2-129">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacb2-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="dacb2-130">-IotHub</span></span>
<span data-ttu-id="dacb2-131">Hedef IoT Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="dacb2-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="dacb2-132">Birden çok IoT Hub için boşlukla ayrılmış liste kullanın.</span><span class="sxs-lookup"><span data-stu-id="dacb2-132">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacb2-133">-Iothubhostname</span><span class="sxs-lookup"><span data-stu-id="dacb2-133">-IotHubHostName</span></span>
<span data-ttu-id="dacb2-134">Hedef IoT Hub 'ının ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="dacb2-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="dacb2-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="dacb2-135">-ProvisioningStatus</span></span>
<span data-ttu-id="dacb2-136">Kayıt girişini etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="dacb2-136">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacb2-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="dacb2-137">-RegistrationId</span></span>
<span data-ttu-id="dacb2-138">Tek kayıt kayıt kimliği.</span><span class="sxs-lookup"><span data-stu-id="dacb2-138">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="dacb2-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="dacb2-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="dacb2-140">Farklı IoT Hub 'ına yeniden temin edilecek cihaz verileri.</span><span class="sxs-lookup"><span data-stu-id="dacb2-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dacb2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dacb2-141">-ResourceGroupName</span></span>
<span data-ttu-id="dacb2-142">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="dacb2-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dacb2-143">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dacb2-143">-ResourceId</span></span>
<span data-ttu-id="dacb2-144">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="dacb2-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="dacb2-145">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dacb2-145">-Tag</span></span>
<span data-ttu-id="dacb2-146">İlk ikili etiketleri.</span><span class="sxs-lookup"><span data-stu-id="dacb2-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="dacb2-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="dacb2-147">-WebhookUrl</span></span>
<span data-ttu-id="dacb2-148">Özel tahsisat isteklerinde kullanılan Web kancası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="dacb2-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="dacb2-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="dacb2-149">-Confirm</span></span>
<span data-ttu-id="dacb2-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dacb2-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dacb2-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dacb2-151">-WhatIf</span></span>
<span data-ttu-id="dacb2-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dacb2-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dacb2-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dacb2-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dacb2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacb2-154">CommonParameters</span></span>
<span data-ttu-id="dacb2-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dacb2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacb2-156">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dacb2-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacb2-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dacb2-157">INPUTS</span></span>

### <span data-ttu-id="dacb2-158">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="dacb2-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="dacb2-159">System. String</span><span class="sxs-lookup"><span data-stu-id="dacb2-159">System.String</span></span>

## <span data-ttu-id="dacb2-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dacb2-160">OUTPUTS</span></span>

### <span data-ttu-id="dacb2-161">Microsoft. Azure. Commands. Management. deviceprovisioningservices. modeller. psındividualenroll</span><span class="sxs-lookup"><span data-stu-id="dacb2-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="dacb2-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dacb2-162">NOTES</span></span>

## <span data-ttu-id="dacb2-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dacb2-163">RELATED LINKS</span></span>
