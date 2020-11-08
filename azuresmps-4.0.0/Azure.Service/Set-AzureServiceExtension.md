---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105447"
---
# <span data-ttu-id="50156-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="50156-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="50156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50156-102">SYNOPSIS</span></span>
<span data-ttu-id="50156-103">Dağıtıma bulut hizmeti uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="50156-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="50156-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50156-104">SYNTAX</span></span>

### <span data-ttu-id="50156-105">SetExtension (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50156-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="50156-106">Sebir Sionparmak Izi</span><span class="sxs-lookup"><span data-stu-id="50156-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="50156-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="50156-107">DESCRIPTION</span></span>
<span data-ttu-id="50156-108">**Set-AzureServiceExtension** cmdlet 'i dağıtıma bir bulut hizmeti uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="50156-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="50156-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50156-109">EXAMPLES</span></span>

### <span data-ttu-id="50156-110">Örnek 1: dağıtıma bulut hizmeti ekleme</span><span class="sxs-lookup"><span data-stu-id="50156-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="50156-111">Bu komut dağıtıma bir bulut hizmeti ekler.</span><span class="sxs-lookup"><span data-stu-id="50156-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="50156-112">Örnek 2: belirli bir rol için bir dağıtıma bulut hizmeti ekleme</span><span class="sxs-lookup"><span data-stu-id="50156-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="50156-113">Bu komut, belirli bir rolün bir dağıtımına bulut hizmeti ekler.</span><span class="sxs-lookup"><span data-stu-id="50156-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="50156-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50156-114">PARAMETERS</span></span>

### <span data-ttu-id="50156-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="50156-115">-CertificateThumbprint</span></span>
<span data-ttu-id="50156-116">Özel yapılandırmayı şifrelemek için kullanılacak sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="50156-117">Bu sertifika, sertifika deposunda zaten var.</span><span class="sxs-lookup"><span data-stu-id="50156-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="50156-118">Sertifika belirtmezseniz, bu cmdlet bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50156-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-119">-ExtensionID</span><span class="sxs-lookup"><span data-stu-id="50156-119">-ExtensionId</span></span>
<span data-ttu-id="50156-120">Uzantı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-120">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="50156-121">-ExtensionName</span></span>
<span data-ttu-id="50156-122">Uzantı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="50156-123">-InformationAction</span></span>
<span data-ttu-id="50156-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="50156-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="50156-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="50156-126">'A</span><span class="sxs-lookup"><span data-stu-id="50156-126">Continue</span></span>
- <span data-ttu-id="50156-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="50156-127">Ignore</span></span>
- <span data-ttu-id="50156-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="50156-128">Inquire</span></span>
- <span data-ttu-id="50156-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="50156-129">SilentlyContinue</span></span>
- <span data-ttu-id="50156-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="50156-130">Stop</span></span>
- <span data-ttu-id="50156-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="50156-131">Suspend</span></span>

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

### <span data-ttu-id="50156-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="50156-132">-InformationVariable</span></span>
<span data-ttu-id="50156-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="50156-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="50156-134">-PrivateConfiguration</span></span>
<span data-ttu-id="50156-135">Özel yapılandırma metnini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="50156-136">-Profile</span></span>
<span data-ttu-id="50156-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50156-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="50156-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50156-139">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="50156-139">-ProviderNamespace</span></span>
<span data-ttu-id="50156-140">Uzantı sağlayıcı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="50156-141">-PublicConfiguration</span></span>
<span data-ttu-id="50156-142">Genel yapılandırma metnini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-143">-Role</span><span class="sxs-lookup"><span data-stu-id="50156-143">-Role</span></span>
<span data-ttu-id="50156-144">Uzak Masaüstü yapılandırmasının belirtilmesi için isteğe bağlı bir roller dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="50156-145">Bu parametre belirtilmezse, uzak masaüstü yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="50156-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-146">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="50156-146">-ServiceName</span></span>
<span data-ttu-id="50156-147">Dağıtımın Azure hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-147">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="50156-148">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="50156-148">-Slot</span></span>
<span data-ttu-id="50156-149">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="50156-150">Geçerli değerler: Production veya basamaklandırma.</span><span class="sxs-lookup"><span data-stu-id="50156-150">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="50156-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="50156-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="50156-152">Sertifikayı tanıtmak için parmak iziyle kullanılan parmak izi karma algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="50156-153">Bu parametre isteğe bağlıdır ve varsayılan olarak SHA1 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="50156-153">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-154">-Version</span><span class="sxs-lookup"><span data-stu-id="50156-154">-Version</span></span>
<span data-ttu-id="50156-155">Uzantı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50156-156">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="50156-156">-X509Certificate</span></span>
<span data-ttu-id="50156-157">Bulut hizmetine otomatik olarak yüklenen ve uzantının özel yapılandırmasını şifrelemek için kullanılan bir X. 509.440 sertifikası belirtir.</span><span class="sxs-lookup"><span data-stu-id="50156-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="50156-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50156-158">CommonParameters</span></span>
<span data-ttu-id="50156-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50156-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50156-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50156-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50156-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50156-161">INPUTS</span></span>

## <span data-ttu-id="50156-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50156-162">OUTPUTS</span></span>

## <span data-ttu-id="50156-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50156-163">NOTES</span></span>

## <span data-ttu-id="50156-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50156-164">RELATED LINKS</span></span>

[<span data-ttu-id="50156-165">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="50156-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="50156-166">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="50156-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


