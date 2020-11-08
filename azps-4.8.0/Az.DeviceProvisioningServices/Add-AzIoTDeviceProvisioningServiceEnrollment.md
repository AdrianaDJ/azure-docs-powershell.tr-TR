---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: e02d9c1ca9a5d45f081f168c3d8736d502f52094
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267734"
---
# <span data-ttu-id="25d80-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="25d80-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="25d80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25d80-102">SYNOPSIS</span></span>
<span data-ttu-id="25d80-103">Bir cihaz kaydı kaydı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="25d80-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="25d80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25d80-104">SYNTAX</span></span>

### <span data-ttu-id="25d80-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="25d80-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d80-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="25d80-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d80-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="25d80-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25d80-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="25d80-108">DESCRIPTION</span></span>
<span data-ttu-id="25d80-109">Bir Azure IoT Hub cihaz sağlama hizmetinde bir cihaz kaydı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="25d80-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="25d80-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25d80-110">EXAMPLES</span></span>

### <span data-ttu-id="25d80-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="25d80-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="25d80-112">Kanıtlama türü SymmetricKey ile kayıt oluşturma</span><span class="sxs-lookup"><span data-stu-id="25d80-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="25d80-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="25d80-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="25d80-114">TPM kanıtlama ile kayıt oluşturma.</span><span class="sxs-lookup"><span data-stu-id="25d80-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="25d80-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="25d80-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="25d80-116">Kanıt türü x509 ile kayıt oluşturma</span><span class="sxs-lookup"><span data-stu-id="25d80-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="25d80-117">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="25d80-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="25d80-118">Kanıtlama türü SymmetricKey ve ilk ikili durumunda bir kayıt oluşturun.</span><span class="sxs-lookup"><span data-stu-id="25d80-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="25d80-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25d80-119">PARAMETERS</span></span>

### <span data-ttu-id="25d80-120">-Ayıra Ilkesi</span><span class="sxs-lookup"><span data-stu-id="25d80-120">-AllocationPolicy</span></span>
<span data-ttu-id="25d80-121">Hub 'a atanan cihazın tahsis türü.</span><span class="sxs-lookup"><span data-stu-id="25d80-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="25d80-122">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="25d80-122">-ApiVersion</span></span>
<span data-ttu-id="25d80-123">Özel tahsisat isteğindeki sağlama hizmetinin API sürümü.</span><span class="sxs-lookup"><span data-stu-id="25d80-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="25d80-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="25d80-124">-AttestationType</span></span>
<span data-ttu-id="25d80-125">Kanıtlama mekanizması.</span><span class="sxs-lookup"><span data-stu-id="25d80-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="25d80-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d80-126">-DefaultProfile</span></span>
<span data-ttu-id="25d80-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25d80-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25d80-128">-İstenilen</span><span class="sxs-lookup"><span data-stu-id="25d80-128">-Desired</span></span>
<span data-ttu-id="25d80-129">İlk ikili istenen özellikler.</span><span class="sxs-lookup"><span data-stu-id="25d80-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="25d80-130">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="25d80-130">-DeviceId</span></span>
<span data-ttu-id="25d80-131">IoT Hub cihazı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="25d80-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="25d80-132">-Vseçpsname</span><span class="sxs-lookup"><span data-stu-id="25d80-132">-DpsName</span></span>
<span data-ttu-id="25d80-133">IoT cihazı sağlama hizmetinin adı</span><span class="sxs-lookup"><span data-stu-id="25d80-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="25d80-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="25d80-134">-DpsObject</span></span>
<span data-ttu-id="25d80-135">IoT cihazı sağlama hizmeti nesnesi</span><span class="sxs-lookup"><span data-stu-id="25d80-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="25d80-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="25d80-136">-EdgeEnabled</span></span>
<span data-ttu-id="25d80-137">Kenarı etkinleştirme bayrağı.</span><span class="sxs-lookup"><span data-stu-id="25d80-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="25d80-138">-Onaylama</span><span class="sxs-lookup"><span data-stu-id="25d80-138">-EndorsementKey</span></span>
<span data-ttu-id="25d80-139">TPM cihazı için TPM onay anahtarı.</span><span class="sxs-lookup"><span data-stu-id="25d80-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="25d80-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="25d80-140">-IotHub</span></span>
<span data-ttu-id="25d80-141">Hedef IoT Hub 'ının adı.</span><span class="sxs-lookup"><span data-stu-id="25d80-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="25d80-142">Birden çok IoT Hub için boşlukla ayrılmış liste kullanın.</span><span class="sxs-lookup"><span data-stu-id="25d80-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="25d80-143">-Iothubhostname</span><span class="sxs-lookup"><span data-stu-id="25d80-143">-IotHubHostName</span></span>
<span data-ttu-id="25d80-144">Hedef IoT Hub 'ının ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="25d80-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="25d80-145">-Primarycaadı</span><span class="sxs-lookup"><span data-stu-id="25d80-145">-PrimaryCAName</span></span>
<span data-ttu-id="25d80-146">Birincil kök CA sertifikasının adı.</span><span class="sxs-lookup"><span data-stu-id="25d80-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="25d80-147">Kök CA sertifikasıyla kanıtlama isteniyorsa, kök CA adı sağlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="25d80-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="25d80-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="25d80-148">-PrimaryCertificate</span></span>
<span data-ttu-id="25d80-149">Birincil sertifikayı içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="25d80-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="25d80-150">X509 Certificate. cer dosyasının veya. pem dosya yolunun Base-64 temsili.</span><span class="sxs-lookup"><span data-stu-id="25d80-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="25d80-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="25d80-151">-PrimaryKey</span></span>
<span data-ttu-id="25d80-152">Base64 biçiminde depolanan birincil simetrik paylaşılan erişim anahtarı.</span><span class="sxs-lookup"><span data-stu-id="25d80-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="25d80-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="25d80-153">-ProvisioningStatus</span></span>
<span data-ttu-id="25d80-154">Kayıt girişini etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="25d80-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="25d80-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="25d80-155">-RegistrationId</span></span>
<span data-ttu-id="25d80-156">Tek kayıt kayıt kimliği.</span><span class="sxs-lookup"><span data-stu-id="25d80-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="25d80-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="25d80-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="25d80-158">Farklı IoT Hub 'ına yeniden temin edilecek cihaz verileri.</span><span class="sxs-lookup"><span data-stu-id="25d80-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="25d80-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d80-159">-ResourceGroupName</span></span>
<span data-ttu-id="25d80-160">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="25d80-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="25d80-161">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="25d80-161">-ResourceId</span></span>
<span data-ttu-id="25d80-162">IoT cihaz sağlama hizmeti kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="25d80-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="25d80-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="25d80-163">-RootCertificate</span></span>
<span data-ttu-id="25d80-164">Kök sertifikaları kullanarak X509attestation oluşturmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="25d80-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="25d80-165">-Secondarycaadı</span><span class="sxs-lookup"><span data-stu-id="25d80-165">-SecondaryCAName</span></span>
<span data-ttu-id="25d80-166">İkincil kök CA sertifikasının adı.</span><span class="sxs-lookup"><span data-stu-id="25d80-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="25d80-167">Kök CA sertifikasıyla kanıtlama isteniyorsa, kök CA adı sağlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="25d80-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="25d80-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="25d80-168">-SecondaryCertificate</span></span>
<span data-ttu-id="25d80-169">İkincil sertifikayı içeren dosyanın yolu.</span><span class="sxs-lookup"><span data-stu-id="25d80-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="25d80-170">X509 Certificate. cer dosyasının veya. pem dosya yolunun Base-64 temsili.</span><span class="sxs-lookup"><span data-stu-id="25d80-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="25d80-171">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="25d80-171">-SecondaryKey</span></span>
<span data-ttu-id="25d80-172">Base64 biçiminde depolanan ikincil simetrik paylaşılan erişim anahtarı.</span><span class="sxs-lookup"><span data-stu-id="25d80-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="25d80-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="25d80-173">-StorageRootKey</span></span>
<span data-ttu-id="25d80-174">TPM cihazı için TPM depolama kökü anahtarı.</span><span class="sxs-lookup"><span data-stu-id="25d80-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="25d80-175">Etiketli</span><span class="sxs-lookup"><span data-stu-id="25d80-175">-Tag</span></span>
<span data-ttu-id="25d80-176">İlk ikili etiketleri.</span><span class="sxs-lookup"><span data-stu-id="25d80-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="25d80-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="25d80-177">-WebhookUrl</span></span>
<span data-ttu-id="25d80-178">Özel tahsisat isteklerinde kullanılan Web kancası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="25d80-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="25d80-179">-Onay</span><span class="sxs-lookup"><span data-stu-id="25d80-179">-Confirm</span></span>
<span data-ttu-id="25d80-180">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="25d80-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25d80-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d80-181">-WhatIf</span></span>
<span data-ttu-id="25d80-182">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="25d80-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d80-183">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="25d80-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25d80-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d80-184">CommonParameters</span></span>
<span data-ttu-id="25d80-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25d80-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d80-186">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d80-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d80-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25d80-187">INPUTS</span></span>

### <span data-ttu-id="25d80-188">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. modeller. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="25d80-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="25d80-189">System. String</span><span class="sxs-lookup"><span data-stu-id="25d80-189">System.String</span></span>

## <span data-ttu-id="25d80-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25d80-190">OUTPUTS</span></span>

### <span data-ttu-id="25d80-191">Microsoft. Azure. Commands. Management. deviceprovisioningservices. modeller. psındividualenroll</span><span class="sxs-lookup"><span data-stu-id="25d80-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="25d80-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25d80-192">NOTES</span></span>

## <span data-ttu-id="25d80-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25d80-193">RELATED LINKS</span></span>
