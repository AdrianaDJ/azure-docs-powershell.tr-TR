---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 59445c2e162a7cbfce5cff26bac91d133c8928a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588118"
---
# <span data-ttu-id="d5cf7-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="d5cf7-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="d5cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="d5cf7-103">Azure IoT Hub cihaz sağlama hizmeti sertifikası için bir doğrulama kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5cf7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5cf7-104">SYNTAX</span></span>

### <span data-ttu-id="d5cf7-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d5cf7-105">ResourceSet (Default)</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String>
 [-Name] <String> [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5cf7-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="d5cf7-106">InputObjectSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5cf7-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="d5cf7-107">ResourceIdSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5cf7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5cf7-108">DESCRIPTION</span></span>
<span data-ttu-id="d5cf7-109">Bu doğrulama kodu, sertifika için bir özgünlük adımını tamamlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="d5cf7-110">Kök sertifikaları özel anahtarıyla imzaladığınız yeni bir sertifikanın CN 'si olarak bu doğrulama kodunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="d5cf7-111">Azure IoT Hub cihaz hazırlama hizmetindeki CA sertifikalarının ayrıntılı açıklaması için bkz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="d5cf7-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="d5cf7-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5cf7-112">EXAMPLES</span></span>

### <span data-ttu-id="d5cf7-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d5cf7-113">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="d5cf7-114">"Mycertificate" için bir doğrulama kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="d5cf7-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d5cf7-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzureRmIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="d5cf7-116">Ardışık düzen kullanarak "mycertificate" için doğrulama kodu oluşturma.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="d5cf7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5cf7-117">PARAMETERS</span></span>

### <span data-ttu-id="d5cf7-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d5cf7-118">-CertificateName</span></span>
<span data-ttu-id="d5cf7-119">IoT cihaz hazırlama hizmeti sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="d5cf7-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5cf7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5cf7-120">-DefaultProfile</span></span>
<span data-ttu-id="d5cf7-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5cf7-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="d5cf7-122">-Etag</span></span>
<span data-ttu-id="d5cf7-123">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="d5cf7-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5cf7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5cf7-124">-InputObject</span></span>
<span data-ttu-id="d5cf7-125">IoT cihaz sağlama hizmeti sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="d5cf7-125">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5cf7-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5cf7-126">-Name</span></span>
<span data-ttu-id="d5cf7-127">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="d5cf7-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d5cf7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5cf7-128">-ResourceGroupName</span></span>
<span data-ttu-id="d5cf7-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d5cf7-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d5cf7-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d5cf7-130">-ResourceId</span></span>
<span data-ttu-id="d5cf7-131">IoT cihaz sağlama hizmeti sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d5cf7-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="d5cf7-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5cf7-132">-Confirm</span></span>
<span data-ttu-id="d5cf7-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5cf7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5cf7-134">-WhatIf</span></span>
<span data-ttu-id="d5cf7-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5cf7-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5cf7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5cf7-137">CommonParameters</span></span>
<span data-ttu-id="d5cf7-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5cf7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5cf7-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5cf7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5cf7-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5cf7-140">INPUTS</span></span>

### <span data-ttu-id="d5cf7-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d5cf7-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="d5cf7-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5cf7-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d5cf7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d5cf7-143">System.String</span></span>

## <span data-ttu-id="d5cf7-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5cf7-144">OUTPUTS</span></span>

### <span data-ttu-id="d5cf7-145">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psspeicationcoderesß</span><span class="sxs-lookup"><span data-stu-id="d5cf7-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="d5cf7-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5cf7-146">NOTES</span></span>

## <span data-ttu-id="d5cf7-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5cf7-147">RELATED LINKS</span></span>
