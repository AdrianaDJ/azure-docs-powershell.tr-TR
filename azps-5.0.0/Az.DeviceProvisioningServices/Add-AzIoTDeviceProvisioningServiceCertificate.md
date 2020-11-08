---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275535"
---
# <span data-ttu-id="c9fca-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="c9fca-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="c9fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9fca-102">SYNOPSIS</span></span>
<span data-ttu-id="c9fca-103">Bir Azure IoT Hub cihaz sağlama hizmeti sertifikası oluşturun/güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c9fca-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="c9fca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9fca-104">SYNTAX</span></span>

### <span data-ttu-id="c9fca-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9fca-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9fca-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="c9fca-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9fca-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="c9fca-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9fca-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9fca-108">DESCRIPTION</span></span>
<span data-ttu-id="c9fca-109">Yeni bir sertifikayı karşıya yükler veya varolan sertifikayı aynı adla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c9fca-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="c9fca-110">Azure IoT Hub cihaz hazırlama hizmetindeki CA sertifikalarının ayrıntılı açıklaması için bkz https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="c9fca-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="c9fca-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9fca-111">EXAMPLES</span></span>

### <span data-ttu-id="c9fca-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c9fca-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="c9fca-113">Bir Azure IoT Hub cihaz sağlama hizmetine CA sertifika CER dosyası yükleyin.</span><span class="sxs-lookup"><span data-stu-id="c9fca-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="c9fca-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c9fca-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="c9fca-115">Yeni bir CER dosyası yükleyerek bir IoT Hub cihaz sağlama hizmetinde CA sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c9fca-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="c9fca-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9fca-116">PARAMETERS</span></span>

### <span data-ttu-id="c9fca-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c9fca-117">-CertificateName</span></span>
<span data-ttu-id="c9fca-118">IoT cihaz hazırlama hizmeti sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="c9fca-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="c9fca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9fca-119">-DefaultProfile</span></span>
<span data-ttu-id="c9fca-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9fca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9fca-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="c9fca-121">-Etag</span></span>
<span data-ttu-id="c9fca-122">Sertifikanın ETag 'i</span><span class="sxs-lookup"><span data-stu-id="c9fca-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="c9fca-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9fca-123">-InputObject</span></span>
<span data-ttu-id="c9fca-124">IoT cihaz sağlama hizmeti sertifika nesnesi</span><span class="sxs-lookup"><span data-stu-id="c9fca-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="c9fca-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="c9fca-125">-Name</span></span>
<span data-ttu-id="c9fca-126">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="c9fca-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c9fca-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="c9fca-127">-Path</span></span>
<span data-ttu-id="c9fca-128">x509 Certificate. cer dosyasının veya. pem dosyası yolunun temel 64 temsili</span><span class="sxs-lookup"><span data-stu-id="c9fca-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9fca-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9fca-129">-ResourceGroupName</span></span>
<span data-ttu-id="c9fca-130">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="c9fca-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c9fca-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c9fca-131">-ResourceId</span></span>
<span data-ttu-id="c9fca-132">IoT cihaz sağlama hizmeti sertifika kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c9fca-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="c9fca-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9fca-133">-Confirm</span></span>
<span data-ttu-id="c9fca-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9fca-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9fca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9fca-135">-WhatIf</span></span>
<span data-ttu-id="c9fca-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9fca-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9fca-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9fca-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9fca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9fca-138">CommonParameters</span></span>
<span data-ttu-id="c9fca-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9fca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9fca-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9fca-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9fca-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9fca-141">INPUTS</span></span>

### <span data-ttu-id="c9fca-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c9fca-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="c9fca-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c9fca-143">System.String</span></span>

## <span data-ttu-id="c9fca-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9fca-144">OUTPUTS</span></span>

### <span data-ttu-id="c9fca-145">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c9fca-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="c9fca-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9fca-146">NOTES</span></span>

## <span data-ttu-id="c9fca-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9fca-147">RELATED LINKS</span></span>
