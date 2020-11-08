---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7c5c2f747b5de24e1ccf3a4cf047930746c0d863
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108304"
---
# <span data-ttu-id="d4e8e-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="d4e8e-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="d4e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e8e-103">Bir cihaz kayıt grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="d4e8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4e8e-104">SYNTAX</span></span>

### <span data-ttu-id="d4e8e-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4e8e-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e8e-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="d4e8e-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e8e-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="d4e8e-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e8e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4e8e-108">DESCRIPTION</span></span>
<span data-ttu-id="d4e8e-109">Azure IoT Hub cihaz sağlama hizmetinde bir kayıt grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d4e8e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4e8e-110">EXAMPLES</span></span>

### <span data-ttu-id="d4e8e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d4e8e-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="d4e8e-112">Kanıtlama türü SymmetricKey ile kayıt oluşturma</span><span class="sxs-lookup"><span data-stu-id="d4e8e-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="d4e8e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d4e8e-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="d4e8e-114">Kanıt türü x509 ile kayıt oluşturma</span><span class="sxs-lookup"><span data-stu-id="d4e8e-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="d4e8e-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d4e8e-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="d4e8e-116">Kanıtlama türü SymmetricKey ve ilk ikili durumunda bir kayıt oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="d4e8e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4e8e-117">PARAMETERS</span></span>

### <span data-ttu-id="d4e8e-118">-Ayıra Ilkesi</span><span class="sxs-lookup"><span data-stu-id="d4e8e-118">-AllocationPolicy</span></span>
<span data-ttu-id="d4e8e-119">Hub 'a atanan cihazın tahsis türü.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-119">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="d4e8e-120">-ApiVersion</span></span>
<span data-ttu-id="d4e8e-121">Özel tahsisat isteğindeki sağlama hizmetinin API sürümü.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="d4e8e-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="d4e8e-122">-AttestationType</span></span>
<span data-ttu-id="d4e8e-123">Kanıtlama mekanizması.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-123">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e8e-124">-DefaultProfile</span></span>
<span data-ttu-id="d4e8e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e8e-126">-İstenilen</span><span class="sxs-lookup"><span data-stu-id="d4e8e-126">-Desired</span></span>
<span data-ttu-id="d4e8e-127">İlk ikili istenen özellikler.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-127">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-128">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="d4e8e-128">-DpsName</span></span>
<span data-ttu-id="d4e8e-129">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="d4e8e-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d4e8e-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d4e8e-130">-DpsObject</span></span>
<span data-ttu-id="d4e8e-131">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="d4e8e-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d4e8e-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="d4e8e-132">-EdgeEnabled</span></span>
<span data-ttu-id="d4e8e-133">Kenarı etkinleştirme bayrağı.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-133">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="d4e8e-134">-IotHub</span></span>
<span data-ttu-id="d4e8e-135">Hedef IoT Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="d4e8e-136">Birden çok IoT Hub için boşlukla ayrılmış liste kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-136">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-137">-Iothubhostname</span><span class="sxs-lookup"><span data-stu-id="d4e8e-137">-IotHubHostName</span></span>
<span data-ttu-id="d4e8e-138">Hedef IoT Hub 'ının ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="d4e8e-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4e8e-139">-Name</span></span>
<span data-ttu-id="d4e8e-140">Kayıt grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-140">Name of the enrollment group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-141">-Primarycaadı</span><span class="sxs-lookup"><span data-stu-id="d4e8e-141">-PrimaryCAName</span></span>
<span data-ttu-id="d4e8e-142">Birincil kök CA sertifikasının adı.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="d4e8e-143">Kök CA sertifikasıyla kanıtlama isteniyorsa, kök CA adı sağlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="d4e8e-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="d4e8e-144">-PrimaryCertificate</span></span>
<span data-ttu-id="d4e8e-145">Birincil sertifikayı içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="d4e8e-146">X509 Certificate. cer dosyasının veya. pem dosya yolunun Base-64 temsili.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="d4e8e-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d4e8e-147">-PrimaryKey</span></span>
<span data-ttu-id="d4e8e-148">Base64 biçiminde depolanan birincil simetrik paylaşılan erişim anahtarı.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="d4e8e-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="d4e8e-149">-ProvisioningStatus</span></span>
<span data-ttu-id="d4e8e-150">Kayıt girişini etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-150">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="d4e8e-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="d4e8e-152">Farklı IoT Hub 'ına yeniden temin edilecek cihaz verileri.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e8e-153">-ResourceGroupName</span></span>
<span data-ttu-id="d4e8e-154">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d4e8e-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d4e8e-155">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d4e8e-155">-ResourceId</span></span>
<span data-ttu-id="d4e8e-156">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d4e8e-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d4e8e-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="d4e8e-157">-RootCertificate</span></span>
<span data-ttu-id="d4e8e-158">Kök sertifikaları kullanarak X509attestation oluşturmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-158">Allows to create X509attestation using root certificates.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-159">-Secondarycaadı</span><span class="sxs-lookup"><span data-stu-id="d4e8e-159">-SecondaryCAName</span></span>
<span data-ttu-id="d4e8e-160">İkincil kök CA sertifikasının adı.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="d4e8e-161">Kök CA sertifikasıyla kanıtlama isteniyorsa, kök CA adı sağlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="d4e8e-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="d4e8e-162">-SecondaryCertificate</span></span>
<span data-ttu-id="d4e8e-163">İkincil sertifikayı içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="d4e8e-164">X509 Certificate. cer dosyasının veya. pem dosya yolunun Base-64 temsili.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="d4e8e-165">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="d4e8e-165">-SecondaryKey</span></span>
<span data-ttu-id="d4e8e-166">Base64 biçiminde depolanan ikincil simetrik paylaşılan erişim anahtarı.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="d4e8e-167">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d4e8e-167">-Tag</span></span>
<span data-ttu-id="d4e8e-168">İlk ikili etiketleri.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-168">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e8e-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="d4e8e-169">-WebhookUrl</span></span>
<span data-ttu-id="d4e8e-170">Özel tahsisat isteklerinde kullanılan Web kancası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="d4e8e-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4e8e-171">-Confirm</span></span>
<span data-ttu-id="d4e8e-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e8e-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e8e-173">-WhatIf</span></span>
<span data-ttu-id="d4e8e-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e8e-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e8e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e8e-176">CommonParameters</span></span>
<span data-ttu-id="d4e8e-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4e8e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e8e-178">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e8e-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e8e-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4e8e-179">INPUTS</span></span>

### <span data-ttu-id="d4e8e-180">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d4e8e-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d4e8e-181">System. String</span><span class="sxs-lookup"><span data-stu-id="d4e8e-181">System.String</span></span>

## <span data-ttu-id="d4e8e-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4e8e-182">OUTPUTS</span></span>

### <span data-ttu-id="d4e8e-183">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="d4e8e-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="d4e8e-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4e8e-184">NOTES</span></span>

## <span data-ttu-id="d4e8e-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4e8e-185">RELATED LINKS</span></span>
