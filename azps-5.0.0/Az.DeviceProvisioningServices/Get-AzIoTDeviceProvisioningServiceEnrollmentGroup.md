---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275515"
---
# <span data-ttu-id="9e12a-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="9e12a-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="9e12a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e12a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e12a-103">Bir cihaz kayıt grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="9e12a-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="9e12a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e12a-104">SYNTAX</span></span>

### <span data-ttu-id="9e12a-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e12a-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e12a-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="9e12a-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e12a-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="9e12a-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e12a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e12a-108">DESCRIPTION</span></span>
<span data-ttu-id="9e12a-109">Bir kayıt grubunun ayrıntılarını alın veya Azure IoT Hub cihaz hazırlama hizmetindeki tüm kayıt gruplarının listesini alın.</span><span class="sxs-lookup"><span data-stu-id="9e12a-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="9e12a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e12a-110">EXAMPLES</span></span>

### <span data-ttu-id="9e12a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9e12a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="9e12a-112">Bir Azure IoT Hub cihaz sağlama hizmetine cihaz kaydı alın.</span><span class="sxs-lookup"><span data-stu-id="9e12a-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="9e12a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9e12a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="9e12a-114">Bir Azure IoT Hub cihaz sağlama hizmetindeki tüm cihaz kaydı gruplarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="9e12a-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="9e12a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e12a-115">PARAMETERS</span></span>

### <span data-ttu-id="9e12a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e12a-116">-DefaultProfile</span></span>
<span data-ttu-id="9e12a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e12a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e12a-118">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="9e12a-118">-DpsName</span></span>
<span data-ttu-id="9e12a-119">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="9e12a-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9e12a-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="9e12a-120">-DpsObject</span></span>
<span data-ttu-id="9e12a-121">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="9e12a-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9e12a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e12a-122">-Name</span></span>
<span data-ttu-id="9e12a-123">Kayıt grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9e12a-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="9e12a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e12a-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e12a-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9e12a-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9e12a-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9e12a-126">-ResourceId</span></span>
<span data-ttu-id="9e12a-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9e12a-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9e12a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e12a-128">CommonParameters</span></span>
<span data-ttu-id="9e12a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e12a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e12a-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e12a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e12a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e12a-131">INPUTS</span></span>

### <span data-ttu-id="9e12a-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9e12a-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9e12a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9e12a-133">System.String</span></span>

## <span data-ttu-id="9e12a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e12a-134">OUTPUTS</span></span>

### <span data-ttu-id="9e12a-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="9e12a-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="9e12a-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSEnrollmentGroups []</span><span class="sxs-lookup"><span data-stu-id="9e12a-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="9e12a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e12a-137">NOTES</span></span>

## <span data-ttu-id="9e12a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e12a-138">RELATED LINKS</span></span>
