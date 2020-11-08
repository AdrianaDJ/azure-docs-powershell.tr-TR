---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106048"
---
# <span data-ttu-id="7e2a3-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7e2a3-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="7e2a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="7e2a3-103">Bulut hizmeti için bir AD etki alanı uzantısını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="7e2a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e2a3-104">SYNTAX</span></span>

### <span data-ttu-id="7e2a3-105">JoinDomainUsingEnumOptions (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e2a3-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e2a3-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="7e2a3-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e2a3-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="7e2a3-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e2a3-108">Joindomainusingenumoptionsandparmak Izi</span><span class="sxs-lookup"><span data-stu-id="7e2a3-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e2a3-109">Joindomainusingjoinoptionandparmak Izi</span><span class="sxs-lookup"><span data-stu-id="7e2a3-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7e2a3-110">Workgroupnameparmak Izi</span><span class="sxs-lookup"><span data-stu-id="7e2a3-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7e2a3-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e2a3-111">DESCRIPTION</span></span>
<span data-ttu-id="7e2a3-112">**Set-AzureServiceADDomainExtension** cmdlet 'i bulut hizmeti IÇIN bir ad (Active Directory) etki alanı uzantısı verir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="7e2a3-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e2a3-113">EXAMPLES</span></span>

### <span data-ttu-id="7e2a3-114">2</span><span class="sxs-lookup"><span data-stu-id="7e2a3-114">1:</span></span>
```

```

## <span data-ttu-id="7e2a3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e2a3-115">PARAMETERS</span></span>

### <span data-ttu-id="7e2a3-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="7e2a3-116">-CertificateThumbprint</span></span>
<span data-ttu-id="7e2a3-117">Özel yapılandırmayı şifrelemek için kullanılacak sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="7e2a3-118">Bu sertifika, sertifika deposunda zaten var.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="7e2a3-119">Sertifika belirtmezseniz, bu cmdlet bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-120">-Credential</span><span class="sxs-lookup"><span data-stu-id="7e2a3-120">-Credential</span></span>
<span data-ttu-id="7e2a3-121">AD etki alanına katılma kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="7e2a3-122">Kimlik bilgileri bir Kullanıcı adı ve parola içerir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-123">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="7e2a3-123">-DomainName</span></span>
<span data-ttu-id="7e2a3-124">AD etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-125">-ExtensionID</span><span class="sxs-lookup"><span data-stu-id="7e2a3-125">-ExtensionId</span></span>
<span data-ttu-id="7e2a3-126">Uzantı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7e2a3-127">-InformationAction</span></span>
<span data-ttu-id="7e2a3-128">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7e2a3-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7e2a3-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e2a3-130">'A</span><span class="sxs-lookup"><span data-stu-id="7e2a3-130">Continue</span></span>
- <span data-ttu-id="7e2a3-131">Manıza</span><span class="sxs-lookup"><span data-stu-id="7e2a3-131">Ignore</span></span>
- <span data-ttu-id="7e2a3-132">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="7e2a3-132">Inquire</span></span>
- <span data-ttu-id="7e2a3-133">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="7e2a3-133">SilentlyContinue</span></span>
- <span data-ttu-id="7e2a3-134">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="7e2a3-134">Stop</span></span>
- <span data-ttu-id="7e2a3-135">Biliriz</span><span class="sxs-lookup"><span data-stu-id="7e2a3-135">Suspend</span></span>

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

### <span data-ttu-id="7e2a3-136">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="7e2a3-136">-InformationVariable</span></span>
<span data-ttu-id="7e2a3-137">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7e2a3-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="7e2a3-138">-JoinOption</span></span>
<span data-ttu-id="7e2a3-139">Katılma seçeneği numaralandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-140">-Seçenekler</span><span class="sxs-lookup"><span data-stu-id="7e2a3-140">-Options</span></span>
<span data-ttu-id="7e2a3-141">İşaretsiz tamsayı birleştirme seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="7e2a3-142">-OUPath</span></span>
<span data-ttu-id="7e2a3-143">AD etki alanına katılma işleminin kuruluş birimi (OU) yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="7e2a3-144">-Profile</span></span>
<span data-ttu-id="7e2a3-145">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e2a3-146">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e2a3-147">-Restart</span><span class="sxs-lookup"><span data-stu-id="7e2a3-147">-Restart</span></span>
<span data-ttu-id="7e2a3-148">Katılma işlemi başarılı olursa bilgisayarın yeniden başlatılıp edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-149">-Role</span><span class="sxs-lookup"><span data-stu-id="7e2a3-149">-Role</span></span>
<span data-ttu-id="7e2a3-150">Uzak Masaüstü yapılandırmasının belirtilmesi için isteğe bağlı bir roller dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="7e2a3-151">Belirtilmemişse, AD etki alanı yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="7e2a3-152">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="7e2a3-152">-ServiceName</span></span>
<span data-ttu-id="7e2a3-153">Bulut hizmeti adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-153">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="7e2a3-154">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="7e2a3-154">-Slot</span></span>
<span data-ttu-id="7e2a3-155">Değiştirilecek dağıtımın ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="7e2a3-156">Bu parametre için kabul edilebilir değerler: Production veya basamaklandırma.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-156">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="7e2a3-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7e2a3-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="7e2a3-158">Sertifikayı tanıtmak için parmak iziyle kullanılan bir parmak izi karma algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="7e2a3-159">Bu parametre isteğe bağlıdır ve varsayılan olarak SHA1 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-159">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="7e2a3-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="7e2a3-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="7e2a3-161">AD etki alanına katılmak için kimlik bilgilerini (Kullanıcı adı ve parola) belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-162">-Version</span><span class="sxs-lookup"><span data-stu-id="7e2a3-162">-Version</span></span>
<span data-ttu-id="7e2a3-163">Uzantı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-164">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="7e2a3-164">-WorkgroupName</span></span>
<span data-ttu-id="7e2a3-165">Çalışma grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-166">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="7e2a3-166">-X509Certificate</span></span>
<span data-ttu-id="7e2a3-167">Belirtilen bir x509 sertifikasını, bu sertifikanın otomatik olarak bulut hizmetine yüklenip, uzantının özel yapılandırmasını şifrelemek için kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e2a3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e2a3-168">CommonParameters</span></span>
<span data-ttu-id="7e2a3-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e2a3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e2a3-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e2a3-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e2a3-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e2a3-171">INPUTS</span></span>

## <span data-ttu-id="7e2a3-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e2a3-172">OUTPUTS</span></span>

## <span data-ttu-id="7e2a3-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e2a3-173">NOTES</span></span>

## <span data-ttu-id="7e2a3-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e2a3-174">RELATED LINKS</span></span>

[<span data-ttu-id="7e2a3-175">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7e2a3-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="7e2a3-176">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7e2a3-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="7e2a3-177">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="7e2a3-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


