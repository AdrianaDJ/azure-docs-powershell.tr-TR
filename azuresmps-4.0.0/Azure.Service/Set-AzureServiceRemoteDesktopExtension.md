---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105813"
---
# <span data-ttu-id="e7f2f-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="e7f2f-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="e7f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f2f-103">Belirtilen rolde veya dağıtımdaki tüm rollerde Uzak Masaüstü uzantısı 'nı etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="e7f2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7f2f-104">SYNTAX</span></span>

### <span data-ttu-id="e7f2f-105">SetExtension (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7f2f-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e7f2f-106">Sebir Sionparmak Izi</span><span class="sxs-lookup"><span data-stu-id="e7f2f-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e7f2f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7f2f-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f2f-108">**Set-Azurezerviceremotedesktopextension** cmdlet 'i, dağıtılan hizmet veya dağıtımdaki tüm roller için Uzak Masaüstü uzantısının kullanılmasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="e7f2f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7f2f-109">EXAMPLES</span></span>

### <span data-ttu-id="e7f2f-110">Örnek 1: Uzak Masaüstü uzantısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e7f2f-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="e7f2f-111">Bu komut belirtilen hizmet için Uzak Masaüstü uzantısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="e7f2f-112">Örnek 2: belirtilen rol için Uzak Masaüstü uzantısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e7f2f-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="e7f2f-113">Bu komut, belirtilen hizmet ve rol için Uzak Masaüstü uzantısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="e7f2f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7f2f-114">PARAMETERS</span></span>

### <span data-ttu-id="e7f2f-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e7f2f-115">-CertificateThumbprint</span></span>
<span data-ttu-id="e7f2f-116">Özel yapılandırmayı şifrelemek için kullanılacak sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="e7f2f-117">Bu sertifika, sertifika deposunda zaten var.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="e7f2f-118">Sertifika belirtmezseniz, bu cmdlet bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="e7f2f-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="e7f2f-119">-Credential</span></span>
<span data-ttu-id="e7f2f-120">Uzak Masaüstü için etkinleştirilecek kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="e7f2f-121">Kimlik bilgileri bir Kullanıcı adı ve parola içerir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f2f-122">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="e7f2f-122">-Expiration</span></span>
<span data-ttu-id="e7f2f-123">Kullanıcının Kullanıcı hesabının ne zaman sona ereceğini belirtmesine olanak sağlayan bir tarih saat nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f2f-124">-ExtensionID</span><span class="sxs-lookup"><span data-stu-id="e7f2f-124">-ExtensionId</span></span>
<span data-ttu-id="e7f2f-125">Uzantı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f2f-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e7f2f-126">-InformationAction</span></span>
<span data-ttu-id="e7f2f-127">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e7f2f-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e7f2f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7f2f-129">'A</span><span class="sxs-lookup"><span data-stu-id="e7f2f-129">Continue</span></span>
- <span data-ttu-id="e7f2f-130">Manıza</span><span class="sxs-lookup"><span data-stu-id="e7f2f-130">Ignore</span></span>
- <span data-ttu-id="e7f2f-131">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="e7f2f-131">Inquire</span></span>
- <span data-ttu-id="e7f2f-132">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="e7f2f-132">SilentlyContinue</span></span>
- <span data-ttu-id="e7f2f-133">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="e7f2f-133">Stop</span></span>
- <span data-ttu-id="e7f2f-134">Biliriz</span><span class="sxs-lookup"><span data-stu-id="e7f2f-134">Suspend</span></span>

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

### <span data-ttu-id="e7f2f-135">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="e7f2f-135">-InformationVariable</span></span>
<span data-ttu-id="e7f2f-136">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e7f2f-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7f2f-137">-Profile</span></span>
<span data-ttu-id="e7f2f-138">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7f2f-139">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7f2f-140">-Role</span><span class="sxs-lookup"><span data-stu-id="e7f2f-140">-Role</span></span>
<span data-ttu-id="e7f2f-141">Uzak Masaüstü yapılandırmasının belirtilmesi için isteğe bağlı bir roller dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="e7f2f-142">Bu parametre belirtilmezse, uzak masaüstü yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="e7f2f-143">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="e7f2f-143">-ServiceName</span></span>
<span data-ttu-id="e7f2f-144">Dağıtımın Azure hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-144">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="e7f2f-145">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="e7f2f-145">-Slot</span></span>
<span data-ttu-id="e7f2f-146">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="e7f2f-147">Bu parametre için kabul edilebilir değerler: üretim, aşamalandırma.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-147">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="e7f2f-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e7f2f-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e7f2f-149">Sertifikayı tanıtmak için parmak iziyle kullanılan bir parmak izi karma algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="e7f2f-150">Bu parametre isteğe bağlıdır ve varsayılan olarak SHA1 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-150">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="e7f2f-151">-Version</span><span class="sxs-lookup"><span data-stu-id="e7f2f-151">-Version</span></span>
<span data-ttu-id="e7f2f-152">Uzantı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f2f-153">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="e7f2f-153">-X509Certificate</span></span>
<span data-ttu-id="e7f2f-154">Bulut hizmetine otomatik olarak yüklenen ve uzantının özel yapılandırmasını şifrelemek için kullanılan bir x509 sertifikası belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

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

### <span data-ttu-id="e7f2f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f2f-155">CommonParameters</span></span>
<span data-ttu-id="e7f2f-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7f2f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f2f-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f2f-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f2f-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7f2f-158">INPUTS</span></span>

## <span data-ttu-id="e7f2f-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7f2f-159">OUTPUTS</span></span>

## <span data-ttu-id="e7f2f-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7f2f-160">NOTES</span></span>

## <span data-ttu-id="e7f2f-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7f2f-161">RELATED LINKS</span></span>

[<span data-ttu-id="e7f2f-162">Get-Azurezerviceremotedesktopextension</span><span class="sxs-lookup"><span data-stu-id="e7f2f-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


