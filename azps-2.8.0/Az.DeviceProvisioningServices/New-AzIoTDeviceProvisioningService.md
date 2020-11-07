---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ac9d9423bf0098f0f6cf7abba958eb2b08404778
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752061"
---
# <span data-ttu-id="2e3b5-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="2e3b5-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="2e3b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e3b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3b5-103">Azure IoT Hub cihazı sağlama hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2e3b5-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="2e3b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e3b5-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e3b5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e3b5-105">DESCRIPTION</span></span>
<span data-ttu-id="2e3b5-106">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="2e3b5-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="2e3b5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e3b5-107">EXAMPLES</span></span>

### <span data-ttu-id="2e3b5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2e3b5-108">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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

<span data-ttu-id="2e3b5-109">Kaynak grubunun bölgesinde standart fiyatlandırma katmanı S1 ile Azure IoT Hub cihaz sağlama hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2e3b5-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="2e3b5-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2e3b5-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

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

<span data-ttu-id="2e3b5-111">' Eastus ' bölgesinde standart fiyatlandırma katmanı S1 ile Azure IoT Hub cihaz sağlama hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2e3b5-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="2e3b5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e3b5-112">PARAMETERS</span></span>

### <span data-ttu-id="2e3b5-113">-Ayıra Ilkesi</span><span class="sxs-lookup"><span data-stu-id="2e3b5-113">-AllocationPolicy</span></span>
<span data-ttu-id="2e3b5-114">IoT cihaz sağlama hizmeti ayırma ilkesi</span><span class="sxs-lookup"><span data-stu-id="2e3b5-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="2e3b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3b5-115">-DefaultProfile</span></span>
<span data-ttu-id="2e3b5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e3b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e3b5-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="2e3b5-117">-Location</span></span>
<span data-ttu-id="2e3b5-118">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="2e3b5-118">Location</span></span>

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

### <span data-ttu-id="2e3b5-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e3b5-119">-Name</span></span>
<span data-ttu-id="2e3b5-120">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="2e3b5-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2e3b5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e3b5-121">-ResourceGroupName</span></span>
<span data-ttu-id="2e3b5-122">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2e3b5-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2e3b5-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2e3b5-123">-SkuName</span></span>
<span data-ttu-id="2e3b5-124">'Sunda</span><span class="sxs-lookup"><span data-stu-id="2e3b5-124">Sku</span></span>

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

### <span data-ttu-id="2e3b5-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e3b5-125">-Confirm</span></span>
<span data-ttu-id="2e3b5-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e3b5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e3b5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e3b5-127">-WhatIf</span></span>
<span data-ttu-id="2e3b5-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e3b5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e3b5-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e3b5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e3b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3b5-130">CommonParameters</span></span>
<span data-ttu-id="2e3b5-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e3b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3b5-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e3b5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3b5-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e3b5-133">INPUTS</span></span>

### <span data-ttu-id="2e3b5-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2e3b5-134">None</span></span>

## <span data-ttu-id="2e3b5-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e3b5-135">OUTPUTS</span></span>

### <span data-ttu-id="2e3b5-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2e3b5-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="2e3b5-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e3b5-137">NOTES</span></span>

## <span data-ttu-id="2e3b5-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e3b5-138">RELATED LINKS</span></span>
