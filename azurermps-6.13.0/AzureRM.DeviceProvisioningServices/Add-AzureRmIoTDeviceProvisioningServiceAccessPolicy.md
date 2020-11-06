---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 23d9e40fe6d25fbd2a6bb3e23959d1a4bf087af2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593256"
---
# <span data-ttu-id="7a22a-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7a22a-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="7a22a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a22a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a22a-103">Azure IoT Hub cihaz sağlama hizmetine yeni bir paylaşılan erişim ilkesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7a22a-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a22a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a22a-104">SYNTAX</span></span>

### <span data-ttu-id="7a22a-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7a22a-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a22a-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="7a22a-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a22a-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="7a22a-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a22a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a22a-108">DESCRIPTION</span></span>
<span data-ttu-id="7a22a-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="7a22a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7a22a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a22a-110">EXAMPLES</span></span>

### <span data-ttu-id="7a22a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7a22a-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="7a22a-112">EnrollmentWrite ve ServiceConfig haklarıyla Azure IoT Hub cihaz sağlama hizmetine yeni bir paylaşılan erişim ilkesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7a22a-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="7a22a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7a22a-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="7a22a-114">Bir Azure IoT Hub cihaz sağlama hizmetine yeni bir paylaşılan erişim ilkesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7a22a-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="7a22a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a22a-115">PARAMETERS</span></span>

### <span data-ttu-id="7a22a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a22a-116">-DefaultProfile</span></span>
<span data-ttu-id="7a22a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a22a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a22a-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="7a22a-118">-DpsObject</span></span>
<span data-ttu-id="7a22a-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a22a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7a22a-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="7a22a-120">-KeyName</span></span>
<span data-ttu-id="7a22a-121">IoT cihazı sağlama hizmeti erişim ilkesi anahtar adı</span><span class="sxs-lookup"><span data-stu-id="7a22a-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="7a22a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7a22a-122">-Name</span></span>
<span data-ttu-id="7a22a-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="7a22a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7a22a-124">-İzinler</span><span class="sxs-lookup"><span data-stu-id="7a22a-124">-Permissions</span></span>
<span data-ttu-id="7a22a-125">IoT cihaz sağlama hizmeti erişim ilkesi izinleri</span><span class="sxs-lookup"><span data-stu-id="7a22a-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a22a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a22a-126">-ResourceGroupName</span></span>
<span data-ttu-id="7a22a-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="7a22a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7a22a-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7a22a-128">-ResourceId</span></span>
<span data-ttu-id="7a22a-129">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7a22a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7a22a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="7a22a-130">-Confirm</span></span>
<span data-ttu-id="7a22a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7a22a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a22a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a22a-132">-WhatIf</span></span>
<span data-ttu-id="7a22a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a22a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a22a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7a22a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a22a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a22a-135">CommonParameters</span></span>
<span data-ttu-id="7a22a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a22a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a22a-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a22a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a22a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a22a-138">INPUTS</span></span>

### <span data-ttu-id="7a22a-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7a22a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="7a22a-140">Parametreler: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a22a-140">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="7a22a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7a22a-141">System.String</span></span>

## <span data-ttu-id="7a22a-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a22a-142">OUTPUTS</span></span>

### <span data-ttu-id="7a22a-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Pssharedaccesstabetureauthorizationruleaccesssıntsdescription</span><span class="sxs-lookup"><span data-stu-id="7a22a-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="7a22a-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a22a-144">NOTES</span></span>

## <span data-ttu-id="7a22a-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a22a-145">RELATED LINKS</span></span>
