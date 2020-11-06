---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b3cd05b286ddfef69228b8aae12e222e5fffd4d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590306"
---
# <span data-ttu-id="4c900-101">Update-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="4c900-101">Update-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="4c900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c900-102">SYNOPSIS</span></span>
<span data-ttu-id="4c900-103">Bir Azure IoT Hub cihaz sağlama hizmetinde bağlantılı bir IoT Hub 'ı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="4c900-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c900-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c900-104">SYNTAX</span></span>

### <span data-ttu-id="4c900-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c900-105">ResourceSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c900-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="4c900-106">InputObjectSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c900-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="4c900-107">ResourceIdSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c900-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c900-108">DESCRIPTION</span></span>
<span data-ttu-id="4c900-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="4c900-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4c900-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c900-110">EXAMPLES</span></span>

### <span data-ttu-id="4c900-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4c900-111">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="4c900-112">Azure IoT Hub cihaz sağlama hizmetinde bağlı IoT Hub "myiothub.azure-devices.net" öğesini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="4c900-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="4c900-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c900-113">PARAMETERS</span></span>

### <span data-ttu-id="4c900-114">-Ayırağırlığı</span><span class="sxs-lookup"><span data-stu-id="4c900-114">-AllocationWeight</span></span>
<span data-ttu-id="4c900-115">IoT Hub 'ının tahsis ağırlığı</span><span class="sxs-lookup"><span data-stu-id="4c900-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="4c900-116">-Applyalkonumilkesi</span><span class="sxs-lookup"><span data-stu-id="4c900-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="4c900-117">IoT Hub 'ına ayırma ilkesi uygulama</span><span class="sxs-lookup"><span data-stu-id="4c900-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="4c900-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c900-118">-DefaultProfile</span></span>
<span data-ttu-id="4c900-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c900-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c900-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c900-120">-InputObject</span></span>
<span data-ttu-id="4c900-121">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="4c900-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4c900-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="4c900-122">-LinkedHubName</span></span>
<span data-ttu-id="4c900-123">Bağlı IoT Hub 'ının adı</span><span class="sxs-lookup"><span data-stu-id="4c900-123">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="4c900-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c900-124">-Name</span></span>
<span data-ttu-id="4c900-125">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="4c900-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4c900-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c900-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c900-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4c900-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4c900-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4c900-128">-ResourceId</span></span>
<span data-ttu-id="4c900-129">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4c900-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4c900-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c900-130">-Confirm</span></span>
<span data-ttu-id="4c900-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c900-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c900-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c900-132">-WhatIf</span></span>
<span data-ttu-id="4c900-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c900-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c900-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c900-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c900-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c900-135">CommonParameters</span></span>
<span data-ttu-id="4c900-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c900-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c900-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c900-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c900-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c900-138">INPUTS</span></span>

### <span data-ttu-id="4c900-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="4c900-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="4c900-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4c900-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4c900-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4c900-141">System.String</span></span>

## <span data-ttu-id="4c900-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c900-142">OUTPUTS</span></span>

### <span data-ttu-id="4c900-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="4c900-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="4c900-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c900-144">NOTES</span></span>

## <span data-ttu-id="4c900-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c900-145">RELATED LINKS</span></span>
