---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: f50c0955d56b42c341b6a1a6b64b1993ee66175e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764659"
---
# <span data-ttu-id="0b11e-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="0b11e-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="0b11e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b11e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b11e-103">Bir Azure IoT Hub cihaz sağlama hizmetinde bağlantılı bir IoT Hub 'ı silin.</span><span class="sxs-lookup"><span data-stu-id="0b11e-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b11e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b11e-104">SYNTAX</span></span>

### <span data-ttu-id="0b11e-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b11e-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b11e-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="0b11e-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b11e-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="0b11e-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b11e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b11e-108">DESCRIPTION</span></span>
<span data-ttu-id="0b11e-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0b11e-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0b11e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b11e-110">EXAMPLES</span></span>

### <span data-ttu-id="0b11e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0b11e-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="0b11e-112">Azure IoT Hub cihaz sağlama hizmetinde bağlı IoT Hub "myiothub" öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="0b11e-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="0b11e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0b11e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzureRmIoTDpsHub
```

<span data-ttu-id="0b11e-114">Ardışık düzen kullanarak bir Azure IoT Hub cihaz sağlama hizmetine bağlı IoT Hub "myiothub" öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="0b11e-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="0b11e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b11e-115">PARAMETERS</span></span>

### <span data-ttu-id="0b11e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b11e-116">-DefaultProfile</span></span>
<span data-ttu-id="0b11e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b11e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b11e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b11e-118">-InputObject</span></span>
<span data-ttu-id="0b11e-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="0b11e-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0b11e-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="0b11e-120">-LinkedHubName</span></span>
<span data-ttu-id="0b11e-121">Bağlı IoT Hub 'ının adı</span><span class="sxs-lookup"><span data-stu-id="0b11e-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="0b11e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b11e-122">-Name</span></span>
<span data-ttu-id="0b11e-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="0b11e-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0b11e-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0b11e-124">-PassThru</span></span>
<span data-ttu-id="0b11e-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="0b11e-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0b11e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b11e-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b11e-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0b11e-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0b11e-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0b11e-128">-ResourceId</span></span>
<span data-ttu-id="0b11e-129">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0b11e-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0b11e-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b11e-130">-Confirm</span></span>
<span data-ttu-id="0b11e-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b11e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b11e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b11e-132">-WhatIf</span></span>
<span data-ttu-id="0b11e-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b11e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b11e-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b11e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b11e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b11e-135">CommonParameters</span></span>
<span data-ttu-id="0b11e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b11e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b11e-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b11e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b11e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b11e-138">INPUTS</span></span>

### <span data-ttu-id="0b11e-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="0b11e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="0b11e-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b11e-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0b11e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0b11e-141">System.String</span></span>

## <span data-ttu-id="0b11e-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b11e-142">OUTPUTS</span></span>

### <span data-ttu-id="0b11e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b11e-143">System.Boolean</span></span>

## <span data-ttu-id="0b11e-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b11e-144">NOTES</span></span>

## <span data-ttu-id="0b11e-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b11e-145">RELATED LINKS</span></span>
