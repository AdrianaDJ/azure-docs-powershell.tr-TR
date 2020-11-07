---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f978e6c0a496273535551663a442989b2ab1648e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752068"
---
# <span data-ttu-id="90493-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="90493-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="90493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90493-102">SYNOPSIS</span></span>
<span data-ttu-id="90493-103">Azure IoT Hub cihaz sağlama hizmetinde tüm paylaşılan erişim ilkelerinin ayrıntılarını listeler veya ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="90493-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="90493-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90493-104">SYNTAX</span></span>

### <span data-ttu-id="90493-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="90493-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90493-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="90493-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90493-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="90493-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90493-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="90493-108">DESCRIPTION</span></span>
<span data-ttu-id="90493-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="90493-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="90493-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90493-110">EXAMPLES</span></span>

### <span data-ttu-id="90493-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="90493-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="90493-112">"Myıotdps" içindeki tüm paylaşılan erişim ilkelerini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="90493-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="90493-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="90493-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="90493-114">Azure IoT Hub cihaz sağlama hizmetinde paylaşılan erişim ilkesinin "mypolicy" ayrıntılarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="90493-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="90493-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90493-115">PARAMETERS</span></span>

### <span data-ttu-id="90493-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90493-116">-DefaultProfile</span></span>
<span data-ttu-id="90493-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90493-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90493-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="90493-118">-DpsObject</span></span>
<span data-ttu-id="90493-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="90493-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="90493-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="90493-120">-KeyName</span></span>
<span data-ttu-id="90493-121">IoT cihazı sağlama hizmeti erişim ilkesi anahtar adı</span><span class="sxs-lookup"><span data-stu-id="90493-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="90493-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="90493-122">-Name</span></span>
<span data-ttu-id="90493-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="90493-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="90493-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90493-124">-ResourceGroupName</span></span>
<span data-ttu-id="90493-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="90493-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="90493-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="90493-126">-ResourceId</span></span>
<span data-ttu-id="90493-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="90493-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="90493-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90493-128">CommonParameters</span></span>
<span data-ttu-id="90493-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90493-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90493-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90493-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90493-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90493-131">INPUTS</span></span>

### <span data-ttu-id="90493-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="90493-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="90493-133">System. String</span><span class="sxs-lookup"><span data-stu-id="90493-133">System.String</span></span>

## <span data-ttu-id="90493-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90493-134">OUTPUTS</span></span>

### <span data-ttu-id="90493-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Pssharedaccesstabetureauthorizationruleaccesssıntsdescription</span><span class="sxs-lookup"><span data-stu-id="90493-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="90493-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90493-136">NOTES</span></span>

## <span data-ttu-id="90493-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90493-137">RELATED LINKS</span></span>
