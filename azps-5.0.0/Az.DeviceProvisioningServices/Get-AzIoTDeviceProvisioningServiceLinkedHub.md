---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275516"
---
# <span data-ttu-id="5c71a-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="5c71a-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="5c71a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c71a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c71a-103">Bir Azure IoT Hub cihaz sağlama hizmetinde, bağlantılı IoT Hub 'larının tüm ayrıntılarını listeler veya ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="5c71a-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5c71a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c71a-104">SYNTAX</span></span>

### <span data-ttu-id="5c71a-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5c71a-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c71a-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="5c71a-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c71a-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="5c71a-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c71a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c71a-108">DESCRIPTION</span></span>
<span data-ttu-id="5c71a-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5c71a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5c71a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c71a-110">EXAMPLES</span></span>

### <span data-ttu-id="5c71a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5c71a-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="5c71a-112">"Myıotdps" içindeki tüm bağlantılı IoT 'leri listeleyin.</span><span class="sxs-lookup"><span data-stu-id="5c71a-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="5c71a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5c71a-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="5c71a-114">Azure IoT Hub cihaz sağlama hizmetinde bağlantılı IoT Merkezi "myiothub1" ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="5c71a-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5c71a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c71a-115">PARAMETERS</span></span>

### <span data-ttu-id="5c71a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c71a-116">-DefaultProfile</span></span>
<span data-ttu-id="5c71a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c71a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c71a-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5c71a-118">-DpsObject</span></span>
<span data-ttu-id="5c71a-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="5c71a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5c71a-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="5c71a-120">-LinkedHubName</span></span>
<span data-ttu-id="5c71a-121">Bağlı IoT Hub 'ının adı</span><span class="sxs-lookup"><span data-stu-id="5c71a-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="5c71a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c71a-122">-Name</span></span>
<span data-ttu-id="5c71a-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="5c71a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5c71a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c71a-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c71a-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5c71a-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5c71a-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5c71a-126">-ResourceId</span></span>
<span data-ttu-id="5c71a-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="5c71a-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5c71a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c71a-128">CommonParameters</span></span>
<span data-ttu-id="5c71a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c71a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c71a-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c71a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c71a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c71a-131">INPUTS</span></span>

### <span data-ttu-id="5c71a-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5c71a-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5c71a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5c71a-133">System.String</span></span>

## <span data-ttu-id="5c71a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c71a-134">OUTPUTS</span></span>

### <span data-ttu-id="5c71a-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="5c71a-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="5c71a-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitions</span><span class="sxs-lookup"><span data-stu-id="5c71a-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="5c71a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c71a-137">NOTES</span></span>

## <span data-ttu-id="5c71a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c71a-138">RELATED LINKS</span></span>
