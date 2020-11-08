---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275490"
---
# <span data-ttu-id="04bf5-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="04bf5-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="04bf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="04bf5-103">Cihaz kayıt grubunu güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="04bf5-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="04bf5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04bf5-104">SYNTAX</span></span>

### <span data-ttu-id="04bf5-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04bf5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04bf5-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="04bf5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04bf5-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="04bf5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04bf5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="04bf5-108">DESCRIPTION</span></span>
<span data-ttu-id="04bf5-109">Azure IoT Hub cihaz sağlama hizmetindeki bir kayıt grubunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="04bf5-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="04bf5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04bf5-110">EXAMPLES</span></span>

### <span data-ttu-id="04bf5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="04bf5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="04bf5-112">Kayıt grubuna yönelik ayırma ilkesini ve hubları güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="04bf5-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="04bf5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04bf5-113">PARAMETERS</span></span>

### <span data-ttu-id="04bf5-114">-Ayıra Ilkesi</span><span class="sxs-lookup"><span data-stu-id="04bf5-114">-AllocationPolicy</span></span>
<span data-ttu-id="04bf5-115">Hub 'a atanan cihazın tahsis türü.</span><span class="sxs-lookup"><span data-stu-id="04bf5-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="04bf5-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="04bf5-116">-ApiVersion</span></span>
<span data-ttu-id="04bf5-117">Özel tahsisat isteğindeki sağlama hizmetinin API sürümü.</span><span class="sxs-lookup"><span data-stu-id="04bf5-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="04bf5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04bf5-118">-DefaultProfile</span></span>
<span data-ttu-id="04bf5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04bf5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04bf5-120">-İstenilen</span><span class="sxs-lookup"><span data-stu-id="04bf5-120">-Desired</span></span>
<span data-ttu-id="04bf5-121">İlk ikili istenen özellikler.</span><span class="sxs-lookup"><span data-stu-id="04bf5-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="04bf5-122">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="04bf5-122">-DpsName</span></span>
<span data-ttu-id="04bf5-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="04bf5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="04bf5-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="04bf5-124">-DpsObject</span></span>
<span data-ttu-id="04bf5-125">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="04bf5-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="04bf5-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="04bf5-126">-EdgeEnabled</span></span>
<span data-ttu-id="04bf5-127">Kenarı etkinleştirme bayrağı.</span><span class="sxs-lookup"><span data-stu-id="04bf5-127">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="04bf5-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="04bf5-128">-IotHub</span></span>
<span data-ttu-id="04bf5-129">Hedef IoT Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="04bf5-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="04bf5-130">Birden çok IoT Hub için boşlukla ayrılmış liste kullanın.</span><span class="sxs-lookup"><span data-stu-id="04bf5-130">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="04bf5-131">-Iothubhostname</span><span class="sxs-lookup"><span data-stu-id="04bf5-131">-IotHubHostName</span></span>
<span data-ttu-id="04bf5-132">Hedef IoT Hub 'ının ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="04bf5-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="04bf5-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="04bf5-133">-Name</span></span>
<span data-ttu-id="04bf5-134">Kayıt grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="04bf5-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="04bf5-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="04bf5-135">-ProvisioningStatus</span></span>
<span data-ttu-id="04bf5-136">Kayıt girişini etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="04bf5-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="04bf5-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="04bf5-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="04bf5-138">Farklı IoT Hub 'ına yeniden temin edilecek cihaz verileri.</span><span class="sxs-lookup"><span data-stu-id="04bf5-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="04bf5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04bf5-139">-ResourceGroupName</span></span>
<span data-ttu-id="04bf5-140">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="04bf5-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="04bf5-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="04bf5-141">-ResourceId</span></span>
<span data-ttu-id="04bf5-142">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="04bf5-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="04bf5-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="04bf5-143">-Tag</span></span>
<span data-ttu-id="04bf5-144">İlk ikili etiketleri.</span><span class="sxs-lookup"><span data-stu-id="04bf5-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="04bf5-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="04bf5-145">-WebhookUrl</span></span>
<span data-ttu-id="04bf5-146">Özel tahsisat isteklerinde kullanılan Web kancası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="04bf5-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="04bf5-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="04bf5-147">-Confirm</span></span>
<span data-ttu-id="04bf5-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04bf5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04bf5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04bf5-149">-WhatIf</span></span>
<span data-ttu-id="04bf5-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04bf5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04bf5-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04bf5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04bf5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04bf5-152">CommonParameters</span></span>
<span data-ttu-id="04bf5-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04bf5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04bf5-154">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04bf5-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04bf5-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04bf5-155">INPUTS</span></span>

### <span data-ttu-id="04bf5-156">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="04bf5-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="04bf5-157">System. String</span><span class="sxs-lookup"><span data-stu-id="04bf5-157">System.String</span></span>

## <span data-ttu-id="04bf5-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04bf5-158">OUTPUTS</span></span>

### <span data-ttu-id="04bf5-159">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="04bf5-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="04bf5-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04bf5-160">NOTES</span></span>

## <span data-ttu-id="04bf5-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04bf5-161">RELATED LINKS</span></span>
