---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: c44e36a0aa08daf7e4a9ae9822f8a4be85db5d57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572782"
---
# <span data-ttu-id="a7d46-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="a7d46-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="a7d46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d46-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d46-103">Tüm sertifikaları veya Azure IoT Hub cihaz sağlama hizmeti içindeki belirli bir sertifikayı listeler.</span><span class="sxs-lookup"><span data-stu-id="a7d46-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7d46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7d46-104">SYNTAX</span></span>

### <span data-ttu-id="a7d46-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7d46-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d46-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="a7d46-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d46-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a7d46-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d46-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7d46-108">DESCRIPTION</span></span>
<span data-ttu-id="a7d46-109">Azure IoT Hub cihaz hazırlama hizmetindeki CA sertifikalarının ayrıntılı açıklaması için bkz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="a7d46-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="a7d46-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7d46-110">EXAMPLES</span></span>

### <span data-ttu-id="a7d46-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7d46-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="a7d46-112">Bir Azure IoT Hub cihaz sağlama hizmetinde "mycertificate" hakkındaki ayrıntıları gösterin.</span><span class="sxs-lookup"><span data-stu-id="a7d46-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="a7d46-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a7d46-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzureRmIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="a7d46-114">Ardışık düzen kullanarak "myıotdps" içindeki tüm sertifikaları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="a7d46-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="a7d46-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7d46-115">PARAMETERS</span></span>

### <span data-ttu-id="a7d46-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a7d46-116">-CertificateName</span></span>
<span data-ttu-id="a7d46-117">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="a7d46-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="a7d46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d46-118">-DefaultProfile</span></span>
<span data-ttu-id="a7d46-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7d46-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d46-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a7d46-120">-DpsObject</span></span>
<span data-ttu-id="a7d46-121">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="a7d46-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a7d46-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7d46-122">-Name</span></span>
<span data-ttu-id="a7d46-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="a7d46-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a7d46-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d46-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7d46-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a7d46-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a7d46-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a7d46-126">-ResourceId</span></span>
<span data-ttu-id="a7d46-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a7d46-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a7d46-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d46-128">CommonParameters</span></span>
<span data-ttu-id="a7d46-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7d46-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d46-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d46-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d46-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7d46-131">INPUTS</span></span>

### <span data-ttu-id="a7d46-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a7d46-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="a7d46-133">Parametreler: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a7d46-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="a7d46-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a7d46-134">System.String</span></span>

## <span data-ttu-id="a7d46-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7d46-135">OUTPUTS</span></span>

### <span data-ttu-id="a7d46-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="a7d46-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="a7d46-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7d46-137">NOTES</span></span>

## <span data-ttu-id="a7d46-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7d46-138">RELATED LINKS</span></span>
