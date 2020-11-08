---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105895"
---
# <span data-ttu-id="1a051-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="1a051-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="1a051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a051-102">SYNOPSIS</span></span>
<span data-ttu-id="1a051-103">Dağıtım için bir Uzak Masaüstü uzantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a051-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="1a051-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a051-104">SYNTAX</span></span>

### <span data-ttu-id="1a051-105">NewExtension (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a051-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1a051-106">Newextensionusingparmak Izi</span><span class="sxs-lookup"><span data-stu-id="1a051-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1a051-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a051-107">DESCRIPTION</span></span>
<span data-ttu-id="1a051-108">**Yeni-Azurezerviceremotedesktopextensionconfig** cmdlet 'i bir dağıtımın Uzak Masaüstü uzantısı için yapılandırma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a051-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="1a051-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a051-109">EXAMPLES</span></span>

### <span data-ttu-id="1a051-110">Örnek 1: Uzak Masaüstü uzantısı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a051-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="1a051-111">Bu komut belirtilen kimlik bilgileri için Uzak Masaüstü uzantısı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a051-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="1a051-112">Örnek 2: belirli bir rol için Uzak Masaüstü uzantısı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a051-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="1a051-113">Bu komut, belirtilen kimlik bilgileri ve WebRole01 rolü için Uzak Masaüstü uzantısı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a051-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="1a051-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a051-114">PARAMETERS</span></span>

### <span data-ttu-id="1a051-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="1a051-115">-CertificateThumbprint</span></span>
<span data-ttu-id="1a051-116">Özel yapılandırmayı şifrelemek için kullanılacak sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="1a051-117">Bu sertifika, sertifika deposunda zaten var.</span><span class="sxs-lookup"><span data-stu-id="1a051-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="1a051-118">Sertifika belirtmezseniz, bu cmdlet bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a051-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="1a051-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="1a051-119">-Credential</span></span>
<span data-ttu-id="1a051-120">Uzak Masaüstü için etkinleştirilecek kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="1a051-121">Kimlik bilgileri bir Kullanıcı adı ve parola içerir.</span><span class="sxs-lookup"><span data-stu-id="1a051-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a051-122">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="1a051-122">-Expiration</span></span>
<span data-ttu-id="1a051-123">Kullanıcının Kullanıcı hesabının ne zaman sona ereceğini belirtmesine olanak tanıyan bir **DateTime** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a051-124">-ExtensionID</span><span class="sxs-lookup"><span data-stu-id="1a051-124">-ExtensionId</span></span>
<span data-ttu-id="1a051-125">Uzantı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a051-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1a051-126">-InformationAction</span></span>
<span data-ttu-id="1a051-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1a051-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1a051-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a051-129">'A</span><span class="sxs-lookup"><span data-stu-id="1a051-129">Continue</span></span>
- <span data-ttu-id="1a051-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="1a051-130">Ignore</span></span>
- <span data-ttu-id="1a051-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="1a051-131">Inquire</span></span>
- <span data-ttu-id="1a051-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="1a051-132">SilentlyContinue</span></span>
- <span data-ttu-id="1a051-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="1a051-133">Stop</span></span>
- <span data-ttu-id="1a051-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="1a051-134">Suspend</span></span>

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

### <span data-ttu-id="1a051-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="1a051-135">-InformationVariable</span></span>
<span data-ttu-id="1a051-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1a051-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="1a051-137">-Profile</span></span>
<span data-ttu-id="1a051-138">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a051-139">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1a051-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a051-140">-Role</span><span class="sxs-lookup"><span data-stu-id="1a051-140">-Role</span></span>
<span data-ttu-id="1a051-141">Uzak Masaüstü yapılandırmasının belirtilmesi için isteğe bağlı bir roller dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="1a051-142">Bu parametre belirtilmezse, uzak masaüstü yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="1a051-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a051-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1a051-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="1a051-144">Sertifikayı tanıtmak için parmak iziyle kullanılan bir parmak izi karma algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="1a051-145">Bu parametre isteğe bağlıdır ve varsayılan olarak SHA1 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a051-145">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a051-146">-Version</span><span class="sxs-lookup"><span data-stu-id="1a051-146">-Version</span></span>
<span data-ttu-id="1a051-147">Uzantı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a051-148">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="1a051-148">-X509Certificate</span></span>
<span data-ttu-id="1a051-149">Belirtilen bir x509 sertifikasını, bu sertifikanın otomatik olarak bulut hizmetine yüklenip, uzantının özel yapılandırmasını şifrelemek için kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a051-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="1a051-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a051-150">CommonParameters</span></span>
<span data-ttu-id="1a051-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a051-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a051-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a051-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a051-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a051-153">INPUTS</span></span>

## <span data-ttu-id="1a051-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a051-154">OUTPUTS</span></span>

## <span data-ttu-id="1a051-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a051-155">NOTES</span></span>

## <span data-ttu-id="1a051-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a051-156">RELATED LINKS</span></span>

[<span data-ttu-id="1a051-157">Set-Azurezerviceremotedesktopextension</span><span class="sxs-lookup"><span data-stu-id="1a051-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


