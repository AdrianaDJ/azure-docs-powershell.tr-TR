---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 9665b0ae486c12aec350db572aee6fc4f718ed43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589549"
---
# <span data-ttu-id="0e06d-101">New-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="0e06d-101">New-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="0e06d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e06d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e06d-103">Azure IoT Hub cihazı sağlama hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0e06d-103">Create an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e06d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e06d-104">SYNTAX</span></span>

```
New-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e06d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e06d-105">DESCRIPTION</span></span>
<span data-ttu-id="0e06d-106">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0e06d-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0e06d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e06d-107">EXAMPLES</span></span>

### <span data-ttu-id="0e06d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0e06d-108">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="0e06d-109">Kaynak grubunun bölgesinde standart fiyatlandırma katmanı S1 ile Azure IoT Hub cihaz sağlama hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0e06d-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="0e06d-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0e06d-110">Example 2</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="0e06d-111">' Eastus ' bölgesinde standart fiyatlandırma katmanı S1 ile Azure IoT Hub cihaz sağlama hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0e06d-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="0e06d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e06d-112">PARAMETERS</span></span>

### <span data-ttu-id="0e06d-113">-Ayıra Ilkesi</span><span class="sxs-lookup"><span data-stu-id="0e06d-113">-AllocationPolicy</span></span>
<span data-ttu-id="0e06d-114">IoT cihaz sağlama hizmeti ayırma ilkesi</span><span class="sxs-lookup"><span data-stu-id="0e06d-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e06d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e06d-115">-DefaultProfile</span></span>
<span data-ttu-id="0e06d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e06d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e06d-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="0e06d-117">-Location</span></span>
<span data-ttu-id="0e06d-118">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="0e06d-118">Location</span></span>

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

### <span data-ttu-id="0e06d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e06d-119">-Name</span></span>
<span data-ttu-id="0e06d-120">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="0e06d-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0e06d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e06d-121">-ResourceGroupName</span></span>
<span data-ttu-id="0e06d-122">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0e06d-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e06d-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0e06d-123">-SkuName</span></span>
<span data-ttu-id="0e06d-124">'Sunda</span><span class="sxs-lookup"><span data-stu-id="0e06d-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e06d-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e06d-125">-Confirm</span></span>
<span data-ttu-id="0e06d-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e06d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e06d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e06d-127">-WhatIf</span></span>
<span data-ttu-id="0e06d-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e06d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e06d-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e06d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e06d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e06d-130">CommonParameters</span></span>
<span data-ttu-id="0e06d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e06d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e06d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e06d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e06d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e06d-133">INPUTS</span></span>

### <span data-ttu-id="0e06d-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0e06d-134">None</span></span>

## <span data-ttu-id="0e06d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e06d-135">OUTPUTS</span></span>

### <span data-ttu-id="0e06d-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0e06d-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="0e06d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e06d-137">NOTES</span></span>

## <span data-ttu-id="0e06d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e06d-138">RELATED LINKS</span></span>
