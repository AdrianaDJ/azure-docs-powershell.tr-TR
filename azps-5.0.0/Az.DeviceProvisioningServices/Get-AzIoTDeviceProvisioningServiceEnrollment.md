---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275517"
---
# <span data-ttu-id="ff687-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="ff687-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="ff687-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff687-102">SYNOPSIS</span></span>
<span data-ttu-id="ff687-103">Bir cihaz kaydı alın.</span><span class="sxs-lookup"><span data-stu-id="ff687-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="ff687-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff687-104">SYNTAX</span></span>

### <span data-ttu-id="ff687-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ff687-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff687-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="ff687-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff687-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="ff687-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff687-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff687-108">DESCRIPTION</span></span>
<span data-ttu-id="ff687-109">Bir Azure IoT Hub cihaz sağlama hizmetine cihaz kayıt ayrıntılarını veya cihaz kayıt listesini alın.</span><span class="sxs-lookup"><span data-stu-id="ff687-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ff687-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff687-110">EXAMPLES</span></span>

### <span data-ttu-id="ff687-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ff687-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="ff687-112">Bir Azure IoT Hub cihaz sağlama hizmetine cihaz kaydı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="ff687-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="ff687-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ff687-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="ff687-114">Bir Azure IoT Hub cihaz sağlama hizmetine cihaz kayıtları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="ff687-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="ff687-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff687-115">PARAMETERS</span></span>

### <span data-ttu-id="ff687-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff687-116">-DefaultProfile</span></span>
<span data-ttu-id="ff687-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff687-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff687-118">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="ff687-118">-DpsName</span></span>
<span data-ttu-id="ff687-119">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="ff687-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ff687-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="ff687-120">-DpsObject</span></span>
<span data-ttu-id="ff687-121">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="ff687-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ff687-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="ff687-122">-RegistrationId</span></span>
<span data-ttu-id="ff687-123">Tek kayıt kayıt kimliği.</span><span class="sxs-lookup"><span data-stu-id="ff687-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="ff687-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff687-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff687-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="ff687-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ff687-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ff687-126">-ResourceId</span></span>
<span data-ttu-id="ff687-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ff687-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ff687-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff687-128">CommonParameters</span></span>
<span data-ttu-id="ff687-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff687-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff687-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff687-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff687-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff687-131">INPUTS</span></span>

### <span data-ttu-id="ff687-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ff687-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ff687-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ff687-133">System.String</span></span>

## <span data-ttu-id="ff687-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff687-134">OUTPUTS</span></span>

### <span data-ttu-id="ff687-135">Microsoft. Azure. Commands. Management. deviceprovisioningservices. modeller. psındividualenroll</span><span class="sxs-lookup"><span data-stu-id="ff687-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="ff687-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modellerini</span><span class="sxs-lookup"><span data-stu-id="ff687-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="ff687-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff687-137">NOTES</span></span>

## <span data-ttu-id="ff687-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff687-138">RELATED LINKS</span></span>
