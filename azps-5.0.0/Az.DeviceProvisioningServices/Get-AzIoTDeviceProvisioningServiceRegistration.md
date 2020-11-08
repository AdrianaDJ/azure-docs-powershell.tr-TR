---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275514"
---
# <span data-ttu-id="98034-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="98034-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="98034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98034-102">SYNOPSIS</span></span>
<span data-ttu-id="98034-103">Cihaz kayıt durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="98034-103">Gets the device registration state.</span></span>

## <span data-ttu-id="98034-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98034-104">SYNTAX</span></span>

### <span data-ttu-id="98034-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="98034-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98034-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="98034-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98034-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="98034-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98034-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="98034-108">DESCRIPTION</span></span>
<span data-ttu-id="98034-109">Bir Azure IoT Hub cihaz sağlama hizmetinde, kaynak grubu altındaki cihazların kayıt durumunu veya kayıt durumunu alın.</span><span class="sxs-lookup"><span data-stu-id="98034-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="98034-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98034-110">EXAMPLES</span></span>

### <span data-ttu-id="98034-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="98034-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="98034-112">Bir Azure IoT Hub cihaz sağlama hizmetine cihaz kayıt durumu ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="98034-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="98034-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="98034-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="98034-114">Bu kayıt grubundaki aygıtların tüm kayıt durumlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="98034-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="98034-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98034-115">PARAMETERS</span></span>

### <span data-ttu-id="98034-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98034-116">-DefaultProfile</span></span>
<span data-ttu-id="98034-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98034-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98034-118">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="98034-118">-DpsName</span></span>
<span data-ttu-id="98034-119">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="98034-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="98034-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="98034-120">-DpsObject</span></span>
<span data-ttu-id="98034-121">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="98034-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="98034-122">-, Mentid</span><span class="sxs-lookup"><span data-stu-id="98034-122">-EnrollmentId</span></span>
<span data-ttu-id="98034-123">Kayıt grubunun KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="98034-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="98034-124">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="98034-124">-Query</span></span>
<span data-ttu-id="98034-125">SQL sorgusu.</span><span class="sxs-lookup"><span data-stu-id="98034-125">Sql query.</span></span>

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

### <span data-ttu-id="98034-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="98034-126">-RegistrationId</span></span>
<span data-ttu-id="98034-127">Cihaz kaydı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="98034-127">ID of device registration.</span></span>

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

### <span data-ttu-id="98034-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98034-128">-ResourceGroupName</span></span>
<span data-ttu-id="98034-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="98034-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="98034-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="98034-130">-ResourceId</span></span>
<span data-ttu-id="98034-131">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="98034-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="98034-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98034-132">CommonParameters</span></span>
<span data-ttu-id="98034-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98034-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98034-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98034-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98034-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98034-135">INPUTS</span></span>

### <span data-ttu-id="98034-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="98034-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="98034-137">System. String</span><span class="sxs-lookup"><span data-stu-id="98034-137">System.String</span></span>

## <span data-ttu-id="98034-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98034-138">OUTPUTS</span></span>

### <span data-ttu-id="98034-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDçıkarma Eregistrationstate</span><span class="sxs-lookup"><span data-stu-id="98034-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="98034-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDçıkarma Eregistrationstates []</span><span class="sxs-lookup"><span data-stu-id="98034-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="98034-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98034-141">NOTES</span></span>

## <span data-ttu-id="98034-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98034-142">RELATED LINKS</span></span>
