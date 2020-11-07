---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 346a09a635b72612c270889afd904a1535994624
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752075"
---
# <span data-ttu-id="668b5-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="668b5-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="668b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668b5-102">SYNOPSIS</span></span>
<span data-ttu-id="668b5-103">Bir Azure IoT Hub cihaz sağlama hizmetine bağlı IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="668b5-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="668b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="668b5-104">SYNTAX</span></span>

### <span data-ttu-id="668b5-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="668b5-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="668b5-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="668b5-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="668b5-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="668b5-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="668b5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="668b5-108">DESCRIPTION</span></span>
<span data-ttu-id="668b5-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="668b5-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="668b5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="668b5-110">EXAMPLES</span></span>

### <span data-ttu-id="668b5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="668b5-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="668b5-112">Bir Azure IoT Hub cihaz sağlama hizmetine bağlı IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="668b5-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="668b5-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="668b5-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="668b5-114">Bir Azure IoT Hub 'ı olan bir Azure IoT Hub 'ı bir</span><span class="sxs-lookup"><span data-stu-id="668b5-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="668b5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="668b5-115">PARAMETERS</span></span>

### <span data-ttu-id="668b5-116">-Ayırağırlığı</span><span class="sxs-lookup"><span data-stu-id="668b5-116">-AllocationWeight</span></span>
<span data-ttu-id="668b5-117">IoT Hub 'ının tahsis ağırlığı</span><span class="sxs-lookup"><span data-stu-id="668b5-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="668b5-118">-Applyalkonumilkesi</span><span class="sxs-lookup"><span data-stu-id="668b5-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="668b5-119">IoT Hub 'ına ayırma ilkesi uygulanıp uygulanmayacağınızı gösteren Boole değeri</span><span class="sxs-lookup"><span data-stu-id="668b5-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="668b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668b5-120">-DefaultProfile</span></span>
<span data-ttu-id="668b5-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="668b5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="668b5-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="668b5-122">-DpsObject</span></span>
<span data-ttu-id="668b5-123">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="668b5-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="668b5-124">-Iothubconnectionstring</span><span class="sxs-lookup"><span data-stu-id="668b5-124">-IotHubConnectionString</span></span>
<span data-ttu-id="668b5-125">IoT Hub kaynağının bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="668b5-125">Connection String of the Iot Hub resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="668b5-126">-Iothublocation</span><span class="sxs-lookup"><span data-stu-id="668b5-126">-IotHubLocation</span></span>
<span data-ttu-id="668b5-127">IoT Hub 'ın konumu</span><span class="sxs-lookup"><span data-stu-id="668b5-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="668b5-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="668b5-128">-Name</span></span>
<span data-ttu-id="668b5-129">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="668b5-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="668b5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="668b5-130">-ResourceGroupName</span></span>
<span data-ttu-id="668b5-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="668b5-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="668b5-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="668b5-132">-ResourceId</span></span>
<span data-ttu-id="668b5-133">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="668b5-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="668b5-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="668b5-134">-Confirm</span></span>
<span data-ttu-id="668b5-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="668b5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="668b5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="668b5-136">-WhatIf</span></span>
<span data-ttu-id="668b5-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="668b5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="668b5-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="668b5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="668b5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668b5-139">CommonParameters</span></span>
<span data-ttu-id="668b5-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="668b5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668b5-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="668b5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668b5-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="668b5-142">INPUTS</span></span>

### <span data-ttu-id="668b5-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="668b5-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="668b5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="668b5-144">System.String</span></span>

## <span data-ttu-id="668b5-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="668b5-145">OUTPUTS</span></span>

### <span data-ttu-id="668b5-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="668b5-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="668b5-147">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitions</span><span class="sxs-lookup"><span data-stu-id="668b5-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="668b5-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="668b5-148">NOTES</span></span>

## <span data-ttu-id="668b5-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="668b5-149">RELATED LINKS</span></span>
