---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097823"
---
# <span data-ttu-id="0119e-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0119e-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="0119e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0119e-102">SYNOPSIS</span></span>
<span data-ttu-id="0119e-103">Azure IoT Hub cihaz sağlama hizmetinde tüm paylaşılan erişim ilkelerinin ayrıntılarını listeler veya ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="0119e-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0119e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0119e-104">SYNTAX</span></span>

### <span data-ttu-id="0119e-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0119e-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0119e-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="0119e-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0119e-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="0119e-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0119e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0119e-108">DESCRIPTION</span></span>
<span data-ttu-id="0119e-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0119e-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0119e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0119e-110">EXAMPLES</span></span>

### <span data-ttu-id="0119e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0119e-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="0119e-112">"Myıotdps" içindeki tüm paylaşılan erişim ilkelerini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="0119e-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="0119e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0119e-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="0119e-114">Azure IoT Hub cihaz sağlama hizmetinde paylaşılan erişim ilkesinin "mypolicy" ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="0119e-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0119e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0119e-115">PARAMETERS</span></span>

### <span data-ttu-id="0119e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0119e-116">-DefaultProfile</span></span>
<span data-ttu-id="0119e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0119e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0119e-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="0119e-118">-DpsObject</span></span>
<span data-ttu-id="0119e-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="0119e-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0119e-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="0119e-120">-KeyName</span></span>
<span data-ttu-id="0119e-121">IoT cihazı sağlama hizmeti erişim ilkesi anahtar adı</span><span class="sxs-lookup"><span data-stu-id="0119e-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="0119e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0119e-122">-Name</span></span>
<span data-ttu-id="0119e-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="0119e-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0119e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0119e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0119e-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0119e-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0119e-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0119e-126">-ResourceId</span></span>
<span data-ttu-id="0119e-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0119e-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0119e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0119e-128">CommonParameters</span></span>
<span data-ttu-id="0119e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0119e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0119e-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0119e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0119e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0119e-131">INPUTS</span></span>

### <span data-ttu-id="0119e-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0119e-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0119e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0119e-133">System.String</span></span>

## <span data-ttu-id="0119e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0119e-134">OUTPUTS</span></span>

### <span data-ttu-id="0119e-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Pssharedaccesstabetureauthorizationruleaccesssıntsdescription</span><span class="sxs-lookup"><span data-stu-id="0119e-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="0119e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0119e-136">NOTES</span></span>

## <span data-ttu-id="0119e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0119e-137">RELATED LINKS</span></span>