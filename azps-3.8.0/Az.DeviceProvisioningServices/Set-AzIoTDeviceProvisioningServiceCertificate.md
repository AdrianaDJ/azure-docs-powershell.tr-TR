---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 9b995a0ed80bf32b770fe6b157a283534d01f743
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097386"
---
# <span data-ttu-id="4bdf4-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="4bdf4-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="4bdf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bdf4-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdf4-103">Bir Azure IoT Hub cihaz sağlama hizmeti sertifikasını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="4bdf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bdf4-104">SYNTAX</span></span>

### <span data-ttu-id="4bdf4-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bdf4-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bdf4-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="4bdf4-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bdf4-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="4bdf4-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bdf4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bdf4-108">DESCRIPTION</span></span>
<span data-ttu-id="4bdf4-109">Generate-doğrulama kodu çağrılarak elde edilen doğrulama kodunu içeren bir doğrulama sertifikası yükleyerek sertifikayı doğrulama.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="4bdf4-110">Bu, elinde bulunan en son adımdır.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="4bdf4-111">Azure IoT Hub cihaz hazırlama hizmetindeki CA sertifikalarının ayrıntılı açıklaması için bkz. https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="4bdf4-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="4bdf4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bdf4-112">EXAMPLES</span></span>

### <span data-ttu-id="4bdf4-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4bdf4-113">Example 1</span></span>
```
PS C:\> Set-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="4bdf4-114">"Mycertificate" özel anahtarının sahipliğini doğrulama.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="4bdf4-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4bdf4-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="4bdf4-116">Ardışık düzeni kullanarak "parolam" özel anahtarının sahipliğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="4bdf4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bdf4-117">PARAMETERS</span></span>

### <span data-ttu-id="4bdf4-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4bdf4-118">-CertificateName</span></span>
<span data-ttu-id="4bdf4-119">IoT cihaz hazırlama hizmeti sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="4bdf4-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="4bdf4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdf4-120">-DefaultProfile</span></span>
<span data-ttu-id="4bdf4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bdf4-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="4bdf4-122">-Etag</span></span>
<span data-ttu-id="4bdf4-123">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="4bdf4-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="4bdf4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bdf4-124">-InputObject</span></span>
<span data-ttu-id="4bdf4-125">IoT cihaz sağlama hizmeti sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="4bdf4-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="4bdf4-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bdf4-126">-Name</span></span>
<span data-ttu-id="4bdf4-127">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="4bdf4-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4bdf4-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="4bdf4-128">-Path</span></span>
<span data-ttu-id="4bdf4-129">x509 Certificate. cer dosyasının veya. pem dosyası yolunun temel 64 temsili</span><span class="sxs-lookup"><span data-stu-id="4bdf4-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="4bdf4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bdf4-130">-ResourceGroupName</span></span>
<span data-ttu-id="4bdf4-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4bdf4-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4bdf4-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4bdf4-132">-ResourceId</span></span>
<span data-ttu-id="4bdf4-133">IoT cihaz sağlama hizmeti sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4bdf4-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="4bdf4-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="4bdf4-134">-Confirm</span></span>
<span data-ttu-id="4bdf4-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bdf4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bdf4-136">-WhatIf</span></span>
<span data-ttu-id="4bdf4-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bdf4-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bdf4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdf4-139">CommonParameters</span></span>
<span data-ttu-id="4bdf4-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bdf4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdf4-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bdf4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdf4-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bdf4-142">INPUTS</span></span>

### <span data-ttu-id="4bdf4-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="4bdf4-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="4bdf4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4bdf4-144">System.String</span></span>

## <span data-ttu-id="4bdf4-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bdf4-145">OUTPUTS</span></span>

### <span data-ttu-id="4bdf4-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="4bdf4-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="4bdf4-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bdf4-147">NOTES</span></span>

## <span data-ttu-id="4bdf4-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bdf4-148">RELATED LINKS</span></span>