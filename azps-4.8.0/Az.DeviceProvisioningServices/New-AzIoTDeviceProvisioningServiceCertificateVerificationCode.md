---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274549"
---
# <span data-ttu-id="2ecd2-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="2ecd2-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="2ecd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ecd2-102">SYNOPSIS</span></span>
<span data-ttu-id="2ecd2-103">Azure IoT Hub cihaz sağlama hizmeti sertifikası için bir doğrulama kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="2ecd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ecd2-104">SYNTAX</span></span>

### <span data-ttu-id="2ecd2-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ecd2-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ecd2-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="2ecd2-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ecd2-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="2ecd2-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ecd2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ecd2-108">DESCRIPTION</span></span>
<span data-ttu-id="2ecd2-109">Bu doğrulama kodu, sertifika için bir özgünlük adımını tamamlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="2ecd2-110">Kök sertifikaları özel anahtarıyla imzaladığınız yeni bir sertifikanın CN 'si olarak bu doğrulama kodunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="2ecd2-111">Azure IoT Hub cihaz hazırlama hizmetindeki CA sertifikalarının ayrıntılı açıklaması için bkz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="2ecd2-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="2ecd2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ecd2-112">EXAMPLES</span></span>

### <span data-ttu-id="2ecd2-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ecd2-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="2ecd2-114">"Mycertificate" için bir doğrulama kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="2ecd2-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2ecd2-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

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

<span data-ttu-id="2ecd2-116">Ardışık düzen kullanarak "mycertificate" için doğrulama kodu oluşturma.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="2ecd2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ecd2-117">PARAMETERS</span></span>

### <span data-ttu-id="2ecd2-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2ecd2-118">-CertificateName</span></span>
<span data-ttu-id="2ecd2-119">IoT cihaz hazırlama hizmeti sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="2ecd2-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="2ecd2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ecd2-120">-DefaultProfile</span></span>
<span data-ttu-id="2ecd2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ecd2-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="2ecd2-122">-Etag</span></span>
<span data-ttu-id="2ecd2-123">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="2ecd2-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="2ecd2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ecd2-124">-InputObject</span></span>
<span data-ttu-id="2ecd2-125">IoT cihaz sağlama hizmeti sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="2ecd2-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="2ecd2-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ecd2-126">-Name</span></span>
<span data-ttu-id="2ecd2-127">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="2ecd2-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2ecd2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ecd2-128">-ResourceGroupName</span></span>
<span data-ttu-id="2ecd2-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2ecd2-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2ecd2-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ecd2-130">-ResourceId</span></span>
<span data-ttu-id="2ecd2-131">IoT cihaz sağlama hizmeti sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2ecd2-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="2ecd2-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ecd2-132">-Confirm</span></span>
<span data-ttu-id="2ecd2-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ecd2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ecd2-134">-WhatIf</span></span>
<span data-ttu-id="2ecd2-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ecd2-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ecd2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ecd2-137">CommonParameters</span></span>
<span data-ttu-id="2ecd2-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ecd2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ecd2-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ecd2-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ecd2-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ecd2-140">INPUTS</span></span>

### <span data-ttu-id="2ecd2-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="2ecd2-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="2ecd2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2ecd2-142">System.String</span></span>

## <span data-ttu-id="2ecd2-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ecd2-143">OUTPUTS</span></span>

### <span data-ttu-id="2ecd2-144">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. Psspeicationcoderesß</span><span class="sxs-lookup"><span data-stu-id="2ecd2-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="2ecd2-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ecd2-145">NOTES</span></span>

## <span data-ttu-id="2ecd2-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ecd2-146">RELATED LINKS</span></span>
