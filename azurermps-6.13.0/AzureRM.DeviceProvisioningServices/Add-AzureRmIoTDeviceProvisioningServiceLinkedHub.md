---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ca32f2d0436ea16d8897f279239ce4de079d1550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762949"
---
# <span data-ttu-id="49a66-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="49a66-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="49a66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49a66-102">SYNOPSIS</span></span>
<span data-ttu-id="49a66-103">Bir Azure IoT Hub cihaz sağlama hizmetine bağlı IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="49a66-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49a66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49a66-104">SYNTAX</span></span>

### <span data-ttu-id="49a66-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="49a66-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a66-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="49a66-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49a66-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="49a66-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49a66-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="49a66-108">DESCRIPTION</span></span>
<span data-ttu-id="49a66-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="49a66-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="49a66-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49a66-110">EXAMPLES</span></span>

### <span data-ttu-id="49a66-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49a66-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="49a66-112">Bir Azure IoT Hub cihaz sağlama hizmetine bağlı IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="49a66-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="49a66-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="49a66-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="49a66-114">Bir Azure IoT Hub 'ı olan bir Azure IoT Hub 'ı bir</span><span class="sxs-lookup"><span data-stu-id="49a66-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="49a66-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49a66-115">PARAMETERS</span></span>

### <span data-ttu-id="49a66-116">-Ayırağırlığı</span><span class="sxs-lookup"><span data-stu-id="49a66-116">-AllocationWeight</span></span>
<span data-ttu-id="49a66-117">IoT Hub 'ının tahsis ağırlığı</span><span class="sxs-lookup"><span data-stu-id="49a66-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="49a66-118">-Applyalkonumilkesi</span><span class="sxs-lookup"><span data-stu-id="49a66-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="49a66-119">IoT Hub 'ına ayırma ilkesi uygulanıp uygulanmayacağınızı gösteren Boole değeri</span><span class="sxs-lookup"><span data-stu-id="49a66-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="49a66-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a66-120">-DefaultProfile</span></span>
<span data-ttu-id="49a66-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49a66-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49a66-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="49a66-122">-DpsObject</span></span>
<span data-ttu-id="49a66-123">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="49a66-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="49a66-124">-Iothubconnectionstring</span><span class="sxs-lookup"><span data-stu-id="49a66-124">-IotHubConnectionString</span></span>
<span data-ttu-id="49a66-125">IoT Hub kaynağının bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="49a66-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="49a66-126">-Iothublocation</span><span class="sxs-lookup"><span data-stu-id="49a66-126">-IotHubLocation</span></span>
<span data-ttu-id="49a66-127">IoT Hub 'ın konumu</span><span class="sxs-lookup"><span data-stu-id="49a66-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="49a66-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="49a66-128">-Name</span></span>
<span data-ttu-id="49a66-129">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="49a66-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="49a66-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a66-130">-ResourceGroupName</span></span>
<span data-ttu-id="49a66-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="49a66-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="49a66-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="49a66-132">-ResourceId</span></span>
<span data-ttu-id="49a66-133">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="49a66-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="49a66-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="49a66-134">-Confirm</span></span>
<span data-ttu-id="49a66-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="49a66-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a66-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a66-136">-WhatIf</span></span>
<span data-ttu-id="49a66-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="49a66-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a66-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="49a66-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a66-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a66-139">CommonParameters</span></span>
<span data-ttu-id="49a66-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49a66-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a66-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a66-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a66-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49a66-142">INPUTS</span></span>

### <span data-ttu-id="49a66-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="49a66-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="49a66-144">Parametreler: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="49a66-144">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="49a66-145">System. String</span><span class="sxs-lookup"><span data-stu-id="49a66-145">System.String</span></span>

## <span data-ttu-id="49a66-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49a66-146">OUTPUTS</span></span>

### <span data-ttu-id="49a66-147">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="49a66-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="49a66-148">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitions</span><span class="sxs-lookup"><span data-stu-id="49a66-148">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="49a66-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49a66-149">NOTES</span></span>

## <span data-ttu-id="49a66-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49a66-150">RELATED LINKS</span></span>
