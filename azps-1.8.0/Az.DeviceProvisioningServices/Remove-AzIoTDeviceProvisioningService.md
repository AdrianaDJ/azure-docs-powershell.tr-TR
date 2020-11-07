---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: a2700c1872e53234d97e82c41a93ef6e9e328391
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760920"
---
# <span data-ttu-id="1158b-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="1158b-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="1158b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1158b-102">SYNOPSIS</span></span>
<span data-ttu-id="1158b-103">Azure IoT Hub cihazı sağlama hizmetini silme.</span><span class="sxs-lookup"><span data-stu-id="1158b-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1158b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1158b-104">SYNTAX</span></span>

### <span data-ttu-id="1158b-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1158b-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1158b-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="1158b-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1158b-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="1158b-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1158b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1158b-108">DESCRIPTION</span></span>
<span data-ttu-id="1158b-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="1158b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1158b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1158b-110">EXAMPLES</span></span>

### <span data-ttu-id="1158b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1158b-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="1158b-112">Azure IoT Hub cihaz sağlama hizmeti ' myıotdps ' öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="1158b-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="1158b-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1158b-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="1158b-114">Ardışık düzen kullanan bir Azure IoT Hub cihaz sağlama hizmeti ' myıotdps ' öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="1158b-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="1158b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1158b-115">PARAMETERS</span></span>

### <span data-ttu-id="1158b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1158b-116">-DefaultProfile</span></span>
<span data-ttu-id="1158b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1158b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1158b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1158b-118">-InputObject</span></span>
<span data-ttu-id="1158b-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="1158b-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1158b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="1158b-120">-Name</span></span>
<span data-ttu-id="1158b-121">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="1158b-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1158b-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1158b-122">-PassThru</span></span>
<span data-ttu-id="1158b-123">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="1158b-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1158b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1158b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1158b-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="1158b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1158b-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1158b-126">-ResourceId</span></span>
<span data-ttu-id="1158b-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1158b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1158b-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="1158b-128">-Confirm</span></span>
<span data-ttu-id="1158b-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1158b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1158b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1158b-130">-WhatIf</span></span>
<span data-ttu-id="1158b-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1158b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1158b-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1158b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1158b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1158b-133">CommonParameters</span></span>
<span data-ttu-id="1158b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1158b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1158b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1158b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1158b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1158b-136">INPUTS</span></span>

### <span data-ttu-id="1158b-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1158b-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1158b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1158b-138">System.String</span></span>

## <span data-ttu-id="1158b-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1158b-139">OUTPUTS</span></span>

### <span data-ttu-id="1158b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1158b-140">System.Boolean</span></span>

## <span data-ttu-id="1158b-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1158b-141">NOTES</span></span>

## <span data-ttu-id="1158b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1158b-142">RELATED LINKS</span></span>
