---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: bae363b984f148ff55f34eaa04b1ba85eaad4449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572774"
---
# <span data-ttu-id="e7a1b-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="e7a1b-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="e7a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a1b-103">Bir Azure IoT Hub cihaz sağlama hizmetinde, bağlantılı IoT Hub 'larının tüm ayrıntılarını listeler veya ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="e7a1b-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7a1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7a1b-104">SYNTAX</span></span>

### <span data-ttu-id="e7a1b-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7a1b-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7a1b-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="e7a1b-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7a1b-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="e7a1b-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7a1b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7a1b-108">DESCRIPTION</span></span>
<span data-ttu-id="e7a1b-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="e7a1b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="e7a1b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7a1b-110">EXAMPLES</span></span>

### <span data-ttu-id="e7a1b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7a1b-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="e7a1b-112">"Myıotdps" içindeki tüm bağlantılı IoT 'leri listeleyin.</span><span class="sxs-lookup"><span data-stu-id="e7a1b-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="e7a1b-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e7a1b-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="e7a1b-114">Azure IoT Hub cihaz sağlama hizmetinde bağlantılı IoT Merkezi "myiothub1" ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="e7a1b-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="e7a1b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7a1b-115">PARAMETERS</span></span>

### <span data-ttu-id="e7a1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a1b-116">-DefaultProfile</span></span>
<span data-ttu-id="e7a1b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7a1b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a1b-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="e7a1b-118">-DpsObject</span></span>
<span data-ttu-id="e7a1b-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="e7a1b-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e7a1b-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="e7a1b-120">-LinkedHubName</span></span>
<span data-ttu-id="e7a1b-121">Bağlı IoT Hub 'ının adı</span><span class="sxs-lookup"><span data-stu-id="e7a1b-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="e7a1b-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7a1b-122">-Name</span></span>
<span data-ttu-id="e7a1b-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="e7a1b-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e7a1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7a1b-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="e7a1b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e7a1b-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e7a1b-126">-ResourceId</span></span>
<span data-ttu-id="e7a1b-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e7a1b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e7a1b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a1b-128">CommonParameters</span></span>
<span data-ttu-id="e7a1b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7a1b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a1b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7a1b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a1b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7a1b-131">INPUTS</span></span>

### <span data-ttu-id="e7a1b-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e7a1b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="e7a1b-133">Parametreler: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7a1b-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="e7a1b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e7a1b-134">System.String</span></span>

## <span data-ttu-id="e7a1b-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7a1b-135">OUTPUTS</span></span>

### <span data-ttu-id="e7a1b-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitiondescription</span><span class="sxs-lookup"><span data-stu-id="e7a1b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="e7a1b-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psiotubdefinitions</span><span class="sxs-lookup"><span data-stu-id="e7a1b-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="e7a1b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7a1b-138">NOTES</span></span>

## <span data-ttu-id="e7a1b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7a1b-139">RELATED LINKS</span></span>
