---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106047"
---
# <span data-ttu-id="aa886-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="aa886-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="aa886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa886-102">SYNOPSIS</span></span>
<span data-ttu-id="aa886-103">Dağıtılan hizmet veya dağıtımda, belirtilen roller veya tüm roller üzerinde Azure tanılama uzantısı 'nı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="aa886-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="aa886-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa886-104">SYNTAX</span></span>

### <span data-ttu-id="aa886-105">SetExtension (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aa886-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa886-106">Sebir Sionparmak Izi</span><span class="sxs-lookup"><span data-stu-id="aa886-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa886-107">Sebir Sionusingdiagnosticsconfiguration</span><span class="sxs-lookup"><span data-stu-id="aa886-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="aa886-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa886-108">DESCRIPTION</span></span>
<span data-ttu-id="aa886-109">**Set-Azurezervicediagnoksextensextencmdlet** 'i, belirtilen roller veya dağıtılmış hizmet üzerindeki tüm roller üzerinde Azure tanılama uzantısı 'nı verir.</span><span class="sxs-lookup"><span data-stu-id="aa886-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="aa886-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa886-110">EXAMPLES</span></span>

### <span data-ttu-id="aa886-111">Örnek 1: Azure tanılama uzantısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="aa886-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="aa886-112">Bu komut, tüm roller için Azure tanılama uzantısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="aa886-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="aa886-113">Örnek 2: belirtilen rol için Azure tanılama uzantısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="aa886-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="aa886-114">Bu komut, belirtilen bir rol için Azure tanılama uzantısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="aa886-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="aa886-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa886-115">PARAMETERS</span></span>

### <span data-ttu-id="aa886-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="aa886-116">-CertificateThumbprint</span></span>
<span data-ttu-id="aa886-117">Özel yapılandırmayı şifrelemek için kullanılacak sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="aa886-118">Bu sertifika, sertifika deposunda zaten var.</span><span class="sxs-lookup"><span data-stu-id="aa886-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="aa886-119">Sertifika belirtmezseniz, bu cmdlet bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa886-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa886-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="aa886-121">Azure Diagnostics için bir yapılandırma dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="aa886-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="aa886-123">Azure Diagnostics 'in yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="aa886-124">Aşağıdaki komutu kullanarak şemayı indirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="aa886-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-125">-ExtensionID</span><span class="sxs-lookup"><span data-stu-id="aa886-125">-ExtensionId</span></span>
<span data-ttu-id="aa886-126">Uzantı KIMLIĞINI belirtir</span><span class="sxs-lookup"><span data-stu-id="aa886-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="aa886-127">-InformationAction</span></span>
<span data-ttu-id="aa886-128">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aa886-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aa886-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aa886-130">'A</span><span class="sxs-lookup"><span data-stu-id="aa886-130">Continue</span></span>
- <span data-ttu-id="aa886-131">Manıza</span><span class="sxs-lookup"><span data-stu-id="aa886-131">Ignore</span></span>
- <span data-ttu-id="aa886-132">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="aa886-132">Inquire</span></span>
- <span data-ttu-id="aa886-133">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="aa886-133">SilentlyContinue</span></span>
- <span data-ttu-id="aa886-134">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="aa886-134">Stop</span></span>
- <span data-ttu-id="aa886-135">Biliriz</span><span class="sxs-lookup"><span data-stu-id="aa886-135">Suspend</span></span>

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

### <span data-ttu-id="aa886-136">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="aa886-136">-InformationVariable</span></span>
<span data-ttu-id="aa886-137">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aa886-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="aa886-138">-Profile</span></span>
<span data-ttu-id="aa886-139">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aa886-140">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="aa886-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aa886-141">-Role</span><span class="sxs-lookup"><span data-stu-id="aa886-141">-Role</span></span>
<span data-ttu-id="aa886-142">Azure tanılama yapılandırmasını belirtebilmeniz için isteğe bağlı bir roller dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="aa886-143">Bu parametreyi belirtmezseniz, tanılama yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="aa886-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-144">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="aa886-144">-ServiceName</span></span>
<span data-ttu-id="aa886-145">Dağıtımın Azure hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-145">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-146">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="aa886-146">-Slot</span></span>
<span data-ttu-id="aa886-147">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="aa886-148">Bu parametre için kabul edilebilir değerler: Production veya basamaklandırma.</span><span class="sxs-lookup"><span data-stu-id="aa886-148">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa886-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="aa886-150">Bir depolama hesabı uç noktası belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="aa886-151">-StorageAccountKey</span></span>
<span data-ttu-id="aa886-152">Bir depolama hesabı anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aa886-153">-StorageAccountName</span></span>
<span data-ttu-id="aa886-154">Bir depolama hesabı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-155">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="aa886-155">-StorageContext</span></span>
<span data-ttu-id="aa886-156">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="aa886-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="aa886-158">Sertifikayı tanıtmak için parmak iziyle kullanılan bir parmak izi karma algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="aa886-159">Bu parametre isteğe bağlıdır ve varsayılan olarak SHA1 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aa886-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-160">-Version</span><span class="sxs-lookup"><span data-stu-id="aa886-160">-Version</span></span>
<span data-ttu-id="aa886-161">Uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="aa886-162">-X509Certificate</span></span>
<span data-ttu-id="aa886-163">Belirtildiğinde, bulut hizmetine otomatik olarak yüklenen ve uzantının özel yapılandırmasını şifrelemek için kullanılan bir X. 509.440 sertifikası belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa886-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa886-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa886-164">CommonParameters</span></span>
<span data-ttu-id="aa886-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa886-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa886-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa886-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa886-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa886-167">INPUTS</span></span>

## <span data-ttu-id="aa886-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa886-168">OUTPUTS</span></span>

## <span data-ttu-id="aa886-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa886-169">NOTES</span></span>

## <span data-ttu-id="aa886-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa886-170">RELATED LINKS</span></span>

[<span data-ttu-id="aa886-171">Get-azurezervicediagnoyapışsexten</span><span class="sxs-lookup"><span data-stu-id="aa886-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="aa886-172">Remove-azurezervicediagnoyapışsexten</span><span class="sxs-lookup"><span data-stu-id="aa886-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


