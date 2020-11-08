---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108298"
---
# <span data-ttu-id="a57f4-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="a57f4-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="a57f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a57f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a57f4-103">Tüm sertifikaları veya Azure IoT Hub cihaz sağlama hizmeti içindeki belirli bir sertifikayı listeler.</span><span class="sxs-lookup"><span data-stu-id="a57f4-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a57f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a57f4-104">SYNTAX</span></span>

### <span data-ttu-id="a57f4-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a57f4-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a57f4-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="a57f4-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a57f4-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a57f4-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a57f4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a57f4-108">DESCRIPTION</span></span>
<span data-ttu-id="a57f4-109">Azure IoT Hub cihaz hazırlama hizmetindeki CA sertifikalarının ayrıntılı açıklaması için bkz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="a57f4-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="a57f4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a57f4-110">EXAMPLES</span></span>

### <span data-ttu-id="a57f4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a57f4-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="a57f4-112">Bir Azure IoT Hub cihaz sağlama hizmetinde "mycertificate" hakkındaki ayrıntıları gösterin.</span><span class="sxs-lookup"><span data-stu-id="a57f4-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="a57f4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a57f4-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="a57f4-114">Ardışık düzen kullanarak "myıotdps" içindeki tüm sertifikaları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="a57f4-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="a57f4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a57f4-115">PARAMETERS</span></span>

### <span data-ttu-id="a57f4-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a57f4-116">-CertificateName</span></span>
<span data-ttu-id="a57f4-117">Sertifikanın adı</span><span class="sxs-lookup"><span data-stu-id="a57f4-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="a57f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57f4-118">-DefaultProfile</span></span>
<span data-ttu-id="a57f4-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a57f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57f4-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a57f4-120">-DpsObject</span></span>
<span data-ttu-id="a57f4-121">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="a57f4-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a57f4-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a57f4-122">-Name</span></span>
<span data-ttu-id="a57f4-123">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="a57f4-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a57f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="a57f4-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a57f4-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a57f4-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a57f4-126">-ResourceId</span></span>
<span data-ttu-id="a57f4-127">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a57f4-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a57f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57f4-128">CommonParameters</span></span>
<span data-ttu-id="a57f4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a57f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57f4-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a57f4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57f4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a57f4-131">INPUTS</span></span>

### <span data-ttu-id="a57f4-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a57f4-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a57f4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a57f4-133">System.String</span></span>

## <span data-ttu-id="a57f4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a57f4-134">OUTPUTS</span></span>

### <span data-ttu-id="a57f4-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="a57f4-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="a57f4-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a57f4-136">NOTES</span></span>

## <span data-ttu-id="a57f4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a57f4-137">RELATED LINKS</span></span>
