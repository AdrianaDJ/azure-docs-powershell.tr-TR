---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105898"
---
# <span data-ttu-id="3ac4c-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="3ac4c-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="3ac4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ac4c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac4c-103">Belirtilen rollerin veya tüm rollerin tanılama uzantısı için yapılandırma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="3ac4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ac4c-104">SYNTAX</span></span>

### <span data-ttu-id="3ac4c-105">NewExtension (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ac4c-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3ac4c-106">Newextensionusingparmak Izi</span><span class="sxs-lookup"><span data-stu-id="3ac4c-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ac4c-107">Sebir Sionparmak Izi</span><span class="sxs-lookup"><span data-stu-id="3ac4c-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3ac4c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ac4c-108">DESCRIPTION</span></span>
<span data-ttu-id="3ac4c-109">**Yeni-Azurezervicediagnoçıkartsextensionconfig** cmdlet 'i, belirtilen roller veya tüm roller için bir tanılama uzantısı için yapılandırma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="3ac4c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ac4c-110">EXAMPLES</span></span>

### <span data-ttu-id="3ac4c-111">Örnek 1: bulut hizmetindeki tüm roller için Azure tanılama uzantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3ac4c-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="3ac4c-112">Bu komut, bulut hizmetindeki tüm roller için Azure tanılama uzantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="3ac4c-113">Örnek 2: bir rol için Azure tanılama uzantısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3ac4c-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="3ac4c-114">Bu komut, bulut hizmetinde WebRole01 rol için Azure tanılama uzantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="3ac4c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ac4c-115">PARAMETERS</span></span>

### <span data-ttu-id="3ac4c-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="3ac4c-116">-CertificateThumbprint</span></span>
<span data-ttu-id="3ac4c-117">Özel yapılandırmayı şifrelemek için kullanılacak sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="3ac4c-118">Bu sertifika, sertifika deposunda zaten var.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="3ac4c-119">Sertifika belirtmezseniz, bu cmdlet bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="3ac4c-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="3ac4c-121">Tanılama yapılandırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-121">Specifies the diagnostics configuration path.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-122">-ExtensionID</span><span class="sxs-lookup"><span data-stu-id="3ac4c-122">-ExtensionId</span></span>
<span data-ttu-id="3ac4c-123">Uzantı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-123">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3ac4c-124">-InformationAction</span></span>
<span data-ttu-id="3ac4c-125">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3ac4c-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="3ac4c-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ac4c-127">'A</span><span class="sxs-lookup"><span data-stu-id="3ac4c-127">Continue</span></span>
- <span data-ttu-id="3ac4c-128">Manıza</span><span class="sxs-lookup"><span data-stu-id="3ac4c-128">Ignore</span></span>
- <span data-ttu-id="3ac4c-129">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="3ac4c-129">Inquire</span></span>
- <span data-ttu-id="3ac4c-130">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="3ac4c-130">SilentlyContinue</span></span>
- <span data-ttu-id="3ac4c-131">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="3ac4c-131">Stop</span></span>
- <span data-ttu-id="3ac4c-132">Biliriz</span><span class="sxs-lookup"><span data-stu-id="3ac4c-132">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-133">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="3ac4c-133">-InformationVariable</span></span>
<span data-ttu-id="3ac4c-134">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-134">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="3ac4c-135">-Profile</span></span>
<span data-ttu-id="3ac4c-136">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ac4c-137">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-138">-Role</span><span class="sxs-lookup"><span data-stu-id="3ac4c-138">-Role</span></span>
<span data-ttu-id="3ac4c-139">Tanılama yapılandırmasını belirtmek için isteğe bağlı bir rol dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="3ac4c-140">Belirtilmezse, tanılama yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ac4c-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="3ac4c-142">Depolama hesabı uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3ac4c-143">-StorageAccountKey</span></span>
<span data-ttu-id="3ac4c-144">Depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3ac4c-145">-StorageAccountName</span></span>
<span data-ttu-id="3ac4c-146">Depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-147">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="3ac4c-147">-StorageContext</span></span>
<span data-ttu-id="3ac4c-148">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="3ac4c-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="3ac4c-150">Sertifikayı tanıtmak için parmak iziyle kullanılan bir parmak izi karma algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="3ac4c-151">Bu parametre isteğe bağlıdır ve varsayılan olarak SHA1 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-151">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-152">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="3ac4c-152">-X509Certificate</span></span>
<span data-ttu-id="3ac4c-153">Bulut hizmetine otomatik olarak yüklenen ve uzantının özel yapılandırmasını şifrelemek için kullanılan bir X. 509.440 sertifikası belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac4c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac4c-154">CommonParameters</span></span>
<span data-ttu-id="3ac4c-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ac4c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac4c-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ac4c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac4c-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ac4c-157">INPUTS</span></span>

## <span data-ttu-id="3ac4c-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ac4c-158">OUTPUTS</span></span>

## <span data-ttu-id="3ac4c-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ac4c-159">NOTES</span></span>

## <span data-ttu-id="3ac4c-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ac4c-160">RELATED LINKS</span></span>

[<span data-ttu-id="3ac4c-161">Get-azurezervicediagnoyapışsexten</span><span class="sxs-lookup"><span data-stu-id="3ac4c-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="3ac4c-162">Set-azurezervicediagnoyapışsexten</span><span class="sxs-lookup"><span data-stu-id="3ac4c-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


