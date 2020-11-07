---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 264978e5cf66436667434c265a7a3ae0c5a31a5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760929"
---
# <span data-ttu-id="a402c-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="a402c-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="a402c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a402c-102">SYNOPSIS</span></span>
<span data-ttu-id="a402c-103">Tüm bilgileri Listele veya Azure IoT Hub cihaz sağlama hizmetlerinin ayrıntılarını göster.</span><span class="sxs-lookup"><span data-stu-id="a402c-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="a402c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a402c-104">SYNTAX</span></span>

### <span data-ttu-id="a402c-105">ListIotDpsByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a402c-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a402c-106">Jetiotvseçpsbyname</span><span class="sxs-lookup"><span data-stu-id="a402c-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a402c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a402c-107">DESCRIPTION</span></span>
<span data-ttu-id="a402c-108">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="a402c-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a402c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a402c-109">EXAMPLES</span></span>

### <span data-ttu-id="a402c-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a402c-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="a402c-111">Bir abonelikteki tüm Azure IoT Hub cihaz sağlama hizmetlerini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="a402c-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="a402c-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a402c-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="a402c-113">' Myresourcegroup ' kaynak grubundaki tüm Azure IoT Hub cihaz sağlama hizmetlerini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="a402c-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="a402c-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a402c-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="a402c-115">' Myıotdps ' Azure IoT Hub cihaz sağlama hizmeti ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="a402c-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="a402c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a402c-116">PARAMETERS</span></span>

### <span data-ttu-id="a402c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a402c-117">-DefaultProfile</span></span>
<span data-ttu-id="a402c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a402c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a402c-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a402c-119">-Name</span></span>
<span data-ttu-id="a402c-120">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="a402c-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a402c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a402c-121">-ResourceGroupName</span></span>
<span data-ttu-id="a402c-122">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a402c-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a402c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a402c-123">CommonParameters</span></span>
<span data-ttu-id="a402c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a402c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a402c-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a402c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a402c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a402c-126">INPUTS</span></span>

### <span data-ttu-id="a402c-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a402c-127">None</span></span>

## <span data-ttu-id="a402c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a402c-128">OUTPUTS</span></span>

### <span data-ttu-id="a402c-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a402c-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="a402c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a402c-130">NOTES</span></span>

## <span data-ttu-id="a402c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a402c-131">RELATED LINKS</span></span>