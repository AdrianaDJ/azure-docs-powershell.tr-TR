---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097388"
---
# <span data-ttu-id="3b895-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="3b895-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="3b895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b895-102">SYNOPSIS</span></span>
<span data-ttu-id="3b895-103">Bir Azure IoT Hub cihaz sağlama hizmetinde bağlantılı bir IoT Hub 'ı silin.</span><span class="sxs-lookup"><span data-stu-id="3b895-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3b895-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b895-104">SYNTAX</span></span>

### <span data-ttu-id="3b895-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b895-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b895-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="3b895-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b895-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="3b895-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b895-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b895-108">DESCRIPTION</span></span>
<span data-ttu-id="3b895-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3b895-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3b895-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b895-110">EXAMPLES</span></span>

### <span data-ttu-id="3b895-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3b895-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="3b895-112">Azure IoT Hub cihaz sağlama hizmetinde bağlı IoT Hub "myiothub" öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="3b895-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="3b895-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3b895-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="3b895-114">Ardışık düzen kullanarak bir Azure IoT Hub cihaz sağlama hizmetine bağlı IoT Hub "myiothub" öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="3b895-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="3b895-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b895-115">PARAMETERS</span></span>

### <span data-ttu-id="3b895-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b895-116">-DefaultProfile</span></span>
<span data-ttu-id="3b895-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b895-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b895-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b895-118">-InputObject</span></span>
<span data-ttu-id="3b895-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="3b895-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="3b895-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="3b895-120">-LinkedHubName</span></span>
<span data-ttu-id="3b895-121">Bağlı IoT Hub 'ının adı</span><span class="sxs-lookup"><span data-stu-id="3b895-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="3b895-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b895-122">-Name</span></span>
<span data-ttu-id="3b895-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="3b895-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="3b895-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3b895-124">-PassThru</span></span>
<span data-ttu-id="3b895-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="3b895-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3b895-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b895-126">-ResourceGroupName</span></span>
<span data-ttu-id="3b895-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="3b895-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3b895-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3b895-128">-ResourceId</span></span>
<span data-ttu-id="3b895-129">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3b895-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="3b895-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b895-130">-Confirm</span></span>
<span data-ttu-id="3b895-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b895-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b895-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b895-132">-WhatIf</span></span>
<span data-ttu-id="3b895-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b895-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b895-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b895-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b895-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b895-135">CommonParameters</span></span>
<span data-ttu-id="3b895-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b895-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b895-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b895-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b895-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b895-138">INPUTS</span></span>

### <span data-ttu-id="3b895-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="3b895-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="3b895-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3b895-140">System.String</span></span>

## <span data-ttu-id="3b895-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b895-141">OUTPUTS</span></span>

### <span data-ttu-id="3b895-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b895-142">System.Boolean</span></span>

## <span data-ttu-id="3b895-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b895-143">NOTES</span></span>

## <span data-ttu-id="3b895-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b895-144">RELATED LINKS</span></span>
