---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: d941e59c3d0681b91cdef9d05617c665dcc83177
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752044"
---
# <span data-ttu-id="58d9b-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="58d9b-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="58d9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="58d9b-103">Bir Azure IoT Hub cihaz sağlama hizmetinde bağlantılı bir IoT Hub 'ı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="58d9b-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="58d9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58d9b-104">SYNTAX</span></span>

### <span data-ttu-id="58d9b-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58d9b-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d9b-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="58d9b-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d9b-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="58d9b-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58d9b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="58d9b-108">DESCRIPTION</span></span>
<span data-ttu-id="58d9b-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="58d9b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="58d9b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58d9b-110">EXAMPLES</span></span>

### <span data-ttu-id="58d9b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="58d9b-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="58d9b-112">Azure IoT Hub cihaz sağlama hizmetinde bağlı IoT Hub "myiothub.azure-devices.net" öğesini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="58d9b-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="58d9b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58d9b-113">PARAMETERS</span></span>

### <span data-ttu-id="58d9b-114">-Ayırağırlığı</span><span class="sxs-lookup"><span data-stu-id="58d9b-114">-AllocationWeight</span></span>
<span data-ttu-id="58d9b-115">IoT Hub 'ının tahsis ağırlığı</span><span class="sxs-lookup"><span data-stu-id="58d9b-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="58d9b-116">-Applyalkonumilkesi</span><span class="sxs-lookup"><span data-stu-id="58d9b-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="58d9b-117">IoT Hub 'ına ayırma ilkesi uygulama</span><span class="sxs-lookup"><span data-stu-id="58d9b-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="58d9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d9b-118">-DefaultProfile</span></span>
<span data-ttu-id="58d9b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58d9b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58d9b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58d9b-120">-InputObject</span></span>
<span data-ttu-id="58d9b-121">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="58d9b-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58d9b-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="58d9b-122">-LinkedHubName</span></span>
<span data-ttu-id="58d9b-123">Bağlı IoT Hub 'ının adı</span><span class="sxs-lookup"><span data-stu-id="58d9b-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d9b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="58d9b-124">-Name</span></span>
<span data-ttu-id="58d9b-125">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="58d9b-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="58d9b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58d9b-126">-ResourceGroupName</span></span>
<span data-ttu-id="58d9b-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="58d9b-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="58d9b-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="58d9b-128">-ResourceId</span></span>
<span data-ttu-id="58d9b-129">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="58d9b-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="58d9b-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="58d9b-130">-Confirm</span></span>
<span data-ttu-id="58d9b-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58d9b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d9b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d9b-132">-WhatIf</span></span>
<span data-ttu-id="58d9b-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58d9b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d9b-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="58d9b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d9b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d9b-135">CommonParameters</span></span>
<span data-ttu-id="58d9b-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58d9b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d9b-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58d9b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d9b-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58d9b-138">INPUTS</span></span>

### <span data-ttu-id="58d9b-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="58d9b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="58d9b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="58d9b-140">System.String</span></span>

## <span data-ttu-id="58d9b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58d9b-141">OUTPUTS</span></span>

### <span data-ttu-id="58d9b-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="58d9b-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="58d9b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58d9b-143">NOTES</span></span>

## <span data-ttu-id="58d9b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58d9b-144">RELATED LINKS</span></span>
