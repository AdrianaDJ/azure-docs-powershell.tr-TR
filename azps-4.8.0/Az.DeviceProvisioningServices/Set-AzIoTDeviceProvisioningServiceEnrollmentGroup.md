---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108293"
---
# <span data-ttu-id="47904-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="47904-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="47904-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47904-102">SYNOPSIS</span></span>
<span data-ttu-id="47904-103">Cihaz kayıt grubunu güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="47904-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="47904-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47904-104">SYNTAX</span></span>

### <span data-ttu-id="47904-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47904-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47904-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="47904-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47904-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="47904-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47904-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47904-108">DESCRIPTION</span></span>
<span data-ttu-id="47904-109">Azure IoT Hub cihaz sağlama hizmetindeki bir kayıt grubunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="47904-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="47904-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47904-110">EXAMPLES</span></span>

### <span data-ttu-id="47904-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="47904-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="47904-112">Kayıt grubuna yönelik ayırma ilkesini ve hubları güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="47904-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="47904-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47904-113">PARAMETERS</span></span>

### <span data-ttu-id="47904-114">-Ayıra Ilkesi</span><span class="sxs-lookup"><span data-stu-id="47904-114">-AllocationPolicy</span></span>
<span data-ttu-id="47904-115">Hub 'a atanan cihazın tahsis türü.</span><span class="sxs-lookup"><span data-stu-id="47904-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="47904-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="47904-116">-ApiVersion</span></span>
<span data-ttu-id="47904-117">Özel tahsisat isteğindeki sağlama hizmetinin API sürümü.</span><span class="sxs-lookup"><span data-stu-id="47904-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="47904-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47904-118">-DefaultProfile</span></span>
<span data-ttu-id="47904-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47904-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47904-120">-İstenilen</span><span class="sxs-lookup"><span data-stu-id="47904-120">-Desired</span></span>
<span data-ttu-id="47904-121">İlk ikili istenen özellikler.</span><span class="sxs-lookup"><span data-stu-id="47904-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="47904-122">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="47904-122">-DpsName</span></span>
<span data-ttu-id="47904-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="47904-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="47904-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="47904-124">-DpsObject</span></span>
<span data-ttu-id="47904-125">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="47904-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="47904-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="47904-126">-EdgeEnabled</span></span>
<span data-ttu-id="47904-127">Kenarı etkinleştirme bayrağı.</span><span class="sxs-lookup"><span data-stu-id="47904-127">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="47904-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="47904-128">-IotHub</span></span>
<span data-ttu-id="47904-129">Hedef IoT Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="47904-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="47904-130">Birden çok IoT Hub için boşlukla ayrılmış liste kullanın.</span><span class="sxs-lookup"><span data-stu-id="47904-130">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="47904-131">-Iothubhostname</span><span class="sxs-lookup"><span data-stu-id="47904-131">-IotHubHostName</span></span>
<span data-ttu-id="47904-132">Hedef IoT Hub 'ının ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="47904-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="47904-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="47904-133">-Name</span></span>
<span data-ttu-id="47904-134">Kayıt grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="47904-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="47904-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="47904-135">-ProvisioningStatus</span></span>
<span data-ttu-id="47904-136">Kayıt girişini etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="47904-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="47904-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="47904-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="47904-138">Farklı IoT Hub 'ına yeniden temin edilecek cihaz verileri.</span><span class="sxs-lookup"><span data-stu-id="47904-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="47904-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47904-139">-ResourceGroupName</span></span>
<span data-ttu-id="47904-140">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="47904-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="47904-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="47904-141">-ResourceId</span></span>
<span data-ttu-id="47904-142">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="47904-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="47904-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="47904-143">-Tag</span></span>
<span data-ttu-id="47904-144">İlk ikili etiketleri.</span><span class="sxs-lookup"><span data-stu-id="47904-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="47904-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="47904-145">-WebhookUrl</span></span>
<span data-ttu-id="47904-146">Özel tahsisat isteklerinde kullanılan Web kancası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="47904-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="47904-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="47904-147">-Confirm</span></span>
<span data-ttu-id="47904-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47904-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47904-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47904-149">-WhatIf</span></span>
<span data-ttu-id="47904-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47904-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47904-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47904-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47904-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47904-152">CommonParameters</span></span>
<span data-ttu-id="47904-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47904-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47904-154">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47904-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47904-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47904-155">INPUTS</span></span>

### <span data-ttu-id="47904-156">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="47904-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="47904-157">System. String</span><span class="sxs-lookup"><span data-stu-id="47904-157">System.String</span></span>

## <span data-ttu-id="47904-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47904-158">OUTPUTS</span></span>

### <span data-ttu-id="47904-159">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="47904-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="47904-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47904-160">NOTES</span></span>

## <span data-ttu-id="47904-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47904-161">RELATED LINKS</span></span>
