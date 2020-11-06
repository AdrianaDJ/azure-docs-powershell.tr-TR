---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589547"
---
# <span data-ttu-id="4969f-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="4969f-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="4969f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4969f-102">SYNOPSIS</span></span>
<span data-ttu-id="4969f-103">Azure IoT Hub cihazı sağlama hizmetini silme.</span><span class="sxs-lookup"><span data-stu-id="4969f-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4969f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4969f-104">SYNTAX</span></span>

### <span data-ttu-id="4969f-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4969f-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4969f-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="4969f-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4969f-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="4969f-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4969f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4969f-108">DESCRIPTION</span></span>
<span data-ttu-id="4969f-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="4969f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="4969f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4969f-110">EXAMPLES</span></span>

### <span data-ttu-id="4969f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4969f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="4969f-112">Azure IoT Hub cihaz sağlama hizmeti ' myıotdps ' öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="4969f-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="4969f-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4969f-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="4969f-114">Ardışık düzen kullanan bir Azure IoT Hub cihaz sağlama hizmeti ' myıotdps ' öğesini silin.</span><span class="sxs-lookup"><span data-stu-id="4969f-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="4969f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4969f-115">PARAMETERS</span></span>

### <span data-ttu-id="4969f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4969f-116">-DefaultProfile</span></span>
<span data-ttu-id="4969f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4969f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4969f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4969f-118">-InputObject</span></span>
<span data-ttu-id="4969f-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="4969f-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4969f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4969f-120">-Name</span></span>
<span data-ttu-id="4969f-121">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="4969f-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4969f-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4969f-122">-PassThru</span></span>
<span data-ttu-id="4969f-123">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="4969f-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4969f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4969f-124">-ResourceGroupName</span></span>
<span data-ttu-id="4969f-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4969f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4969f-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4969f-126">-ResourceId</span></span>
<span data-ttu-id="4969f-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4969f-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4969f-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="4969f-128">-Confirm</span></span>
<span data-ttu-id="4969f-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4969f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4969f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4969f-130">-WhatIf</span></span>
<span data-ttu-id="4969f-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4969f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4969f-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4969f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4969f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4969f-133">CommonParameters</span></span>
<span data-ttu-id="4969f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4969f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4969f-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4969f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4969f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4969f-136">INPUTS</span></span>

### <span data-ttu-id="4969f-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4969f-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="4969f-138">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4969f-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4969f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4969f-139">System.String</span></span>

## <span data-ttu-id="4969f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4969f-140">OUTPUTS</span></span>

### <span data-ttu-id="4969f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4969f-141">System.Boolean</span></span>

## <span data-ttu-id="4969f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4969f-142">NOTES</span></span>

## <span data-ttu-id="4969f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4969f-143">RELATED LINKS</span></span>
