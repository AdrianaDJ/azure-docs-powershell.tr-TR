---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 3102cafabecb5df8daea15a40eb179405c6c0ea8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275509"
---
# <span data-ttu-id="882e6-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="882e6-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="882e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="882e6-102">SYNOPSIS</span></span>
<span data-ttu-id="882e6-103">Azure IoT Hub cihazı sağlama hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="882e6-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="882e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="882e6-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="882e6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="882e6-105">DESCRIPTION</span></span>
<span data-ttu-id="882e6-106">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="882e6-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="882e6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="882e6-107">EXAMPLES</span></span>

### <span data-ttu-id="882e6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="882e6-108">Example 1</span></span>
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

<span data-ttu-id="882e6-109">Kaynak grubunun bölgesinde standart fiyatlandırma katmanı S1 ile Azure IoT Hub cihaz sağlama hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="882e6-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="882e6-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="882e6-110">Example 2</span></span>
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

<span data-ttu-id="882e6-111">' Eastus ' bölgesinde standart fiyatlandırma katmanı S1 ile Azure IoT Hub cihaz sağlama hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="882e6-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="882e6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="882e6-112">PARAMETERS</span></span>

### <span data-ttu-id="882e6-113">-Ayıra Ilkesi</span><span class="sxs-lookup"><span data-stu-id="882e6-113">-AllocationPolicy</span></span>
<span data-ttu-id="882e6-114">IoT cihaz sağlama hizmeti ayırma ilkesi</span><span class="sxs-lookup"><span data-stu-id="882e6-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="882e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882e6-115">-DefaultProfile</span></span>
<span data-ttu-id="882e6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="882e6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="882e6-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="882e6-117">-Location</span></span>
<span data-ttu-id="882e6-118">Konumuyla</span><span class="sxs-lookup"><span data-stu-id="882e6-118">Location</span></span>

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

### <span data-ttu-id="882e6-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="882e6-119">-Name</span></span>
<span data-ttu-id="882e6-120">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="882e6-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="882e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="882e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="882e6-122">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="882e6-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="882e6-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="882e6-123">-SkuName</span></span>
<span data-ttu-id="882e6-124">'Sunda</span><span class="sxs-lookup"><span data-stu-id="882e6-124">Sku</span></span>

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

### <span data-ttu-id="882e6-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="882e6-125">-Confirm</span></span>
<span data-ttu-id="882e6-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="882e6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="882e6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="882e6-127">-WhatIf</span></span>
<span data-ttu-id="882e6-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="882e6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="882e6-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="882e6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="882e6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882e6-130">CommonParameters</span></span>
<span data-ttu-id="882e6-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="882e6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882e6-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="882e6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882e6-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="882e6-133">INPUTS</span></span>

### <span data-ttu-id="882e6-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="882e6-134">None</span></span>

## <span data-ttu-id="882e6-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="882e6-135">OUTPUTS</span></span>

### <span data-ttu-id="882e6-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="882e6-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="882e6-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="882e6-137">NOTES</span></span>

## <span data-ttu-id="882e6-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="882e6-138">RELATED LINKS</span></span>
