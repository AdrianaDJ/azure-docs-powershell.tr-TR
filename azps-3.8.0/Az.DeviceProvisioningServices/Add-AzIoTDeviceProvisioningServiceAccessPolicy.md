---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097860"
---
# <span data-ttu-id="d03b4-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d03b4-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="d03b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d03b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d03b4-103">Azure IoT Hub cihaz sağlama hizmetine yeni bir paylaşılan erişim ilkesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d03b4-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d03b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d03b4-104">SYNTAX</span></span>

### <span data-ttu-id="d03b4-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d03b4-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d03b4-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="d03b4-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d03b4-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="d03b4-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d03b4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d03b4-108">DESCRIPTION</span></span>
<span data-ttu-id="d03b4-109">Azure IoT Hub cihaz sağlama hizmetine giriş için bkz https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="d03b4-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d03b4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d03b4-110">EXAMPLES</span></span>

### <span data-ttu-id="d03b4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d03b4-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="d03b4-112">EnrollmentWrite ve ServiceConfig haklarıyla Azure IoT Hub cihaz sağlama hizmetine yeni bir paylaşılan erişim ilkesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d03b4-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="d03b4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d03b4-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="d03b4-114">Bir Azure IoT Hub cihaz sağlama hizmetine yeni bir paylaşılan erişim ilkesi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d03b4-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="d03b4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d03b4-115">PARAMETERS</span></span>

### <span data-ttu-id="d03b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d03b4-116">-DefaultProfile</span></span>
<span data-ttu-id="d03b4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d03b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d03b4-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d03b4-118">-DpsObject</span></span>
<span data-ttu-id="d03b4-119">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="d03b4-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d03b4-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="d03b4-120">-KeyName</span></span>
<span data-ttu-id="d03b4-121">IoT cihazı sağlama hizmeti erişim ilkesi anahtar adı</span><span class="sxs-lookup"><span data-stu-id="d03b4-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="d03b4-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d03b4-122">-Name</span></span>
<span data-ttu-id="d03b4-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="d03b4-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d03b4-124">-İzinler</span><span class="sxs-lookup"><span data-stu-id="d03b4-124">-Permissions</span></span>
<span data-ttu-id="d03b4-125">IoT cihaz sağlama hizmeti erişim ilkesi izinleri</span><span class="sxs-lookup"><span data-stu-id="d03b4-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="d03b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d03b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="d03b4-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d03b4-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d03b4-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d03b4-128">-ResourceId</span></span>
<span data-ttu-id="d03b4-129">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d03b4-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d03b4-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="d03b4-130">-Confirm</span></span>
<span data-ttu-id="d03b4-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d03b4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d03b4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d03b4-132">-WhatIf</span></span>
<span data-ttu-id="d03b4-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d03b4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d03b4-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d03b4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d03b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d03b4-135">CommonParameters</span></span>
<span data-ttu-id="d03b4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d03b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d03b4-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d03b4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d03b4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d03b4-138">INPUTS</span></span>

### <span data-ttu-id="d03b4-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d03b4-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d03b4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d03b4-140">System.String</span></span>

## <span data-ttu-id="d03b4-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d03b4-141">OUTPUTS</span></span>

### <span data-ttu-id="d03b4-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Pssharedaccesstabetureauthorizationruleaccesssıntsdescription</span><span class="sxs-lookup"><span data-stu-id="d03b4-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="d03b4-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d03b4-143">NOTES</span></span>

## <span data-ttu-id="d03b4-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d03b4-144">RELATED LINKS</span></span>
