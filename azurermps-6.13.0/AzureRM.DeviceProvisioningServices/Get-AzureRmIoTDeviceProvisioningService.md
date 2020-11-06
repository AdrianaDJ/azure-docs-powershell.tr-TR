---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: dd9bc81ef24530369a26ff290270a39c8ab1ff40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572781"
---
# <span data-ttu-id="2d923-101">Get-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="2d923-101">Get-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="2d923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d923-102">SYNOPSIS</span></span>
<span data-ttu-id="2d923-103">Tüm bilgileri Listele veya Azure IoT Hub cihaz sağlama hizmetlerinin ayrıntılarını göster.</span><span class="sxs-lookup"><span data-stu-id="2d923-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d923-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d923-104">SYNTAX</span></span>

### <span data-ttu-id="2d923-105">ListIotDpsByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2d923-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningService [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d923-106">Jetiotvseçpsbyname</span><span class="sxs-lookup"><span data-stu-id="2d923-106">GetIotDpsByName</span></span>
```
Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d923-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d923-107">DESCRIPTION</span></span>
<span data-ttu-id="2d923-108">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="2d923-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="2d923-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d923-109">EXAMPLES</span></span>

### <span data-ttu-id="2d923-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d923-110">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="2d923-111">Bir abonelikteki tüm Azure IoT Hub cihaz sağlama hizmetlerini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="2d923-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="2d923-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2d923-112">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="2d923-113">' Myresourcegroup ' kaynak grubundaki tüm Azure IoT Hub cihaz sağlama hizmetlerini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="2d923-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="2d923-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2d923-114">Example 3</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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

<span data-ttu-id="2d923-115">' Myıotdps ' Azure IoT Hub cihaz sağlama hizmeti ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="2d923-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="2d923-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d923-116">PARAMETERS</span></span>

### <span data-ttu-id="2d923-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d923-117">-DefaultProfile</span></span>
<span data-ttu-id="2d923-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d923-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d923-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d923-119">-Name</span></span>
<span data-ttu-id="2d923-120">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="2d923-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2d923-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d923-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d923-122">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2d923-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2d923-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d923-123">CommonParameters</span></span>
<span data-ttu-id="2d923-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d923-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d923-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d923-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d923-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d923-126">INPUTS</span></span>

### <span data-ttu-id="2d923-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2d923-127">None</span></span>

## <span data-ttu-id="2d923-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d923-128">OUTPUTS</span></span>

### <span data-ttu-id="2d923-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2d923-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="2d923-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d923-130">NOTES</span></span>

## <span data-ttu-id="2d923-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d923-131">RELATED LINKS</span></span>
