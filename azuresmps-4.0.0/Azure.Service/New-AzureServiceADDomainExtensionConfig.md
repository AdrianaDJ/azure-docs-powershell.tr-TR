---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105897"
---
# <span data-ttu-id="f16e6-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="f16e6-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="f16e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f16e6-102">SYNOPSIS</span></span>
<span data-ttu-id="f16e6-103">Bulut hizmetleri için AD etki alanı uzantısının yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f16e6-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="f16e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f16e6-104">SYNTAX</span></span>

### <span data-ttu-id="f16e6-105">JoinDomainUsingEnumOptions (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f16e6-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f16e6-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="f16e6-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f16e6-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="f16e6-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f16e6-108">Joindomainusingenumoptionsandparmak Izi</span><span class="sxs-lookup"><span data-stu-id="f16e6-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f16e6-109">Joindomainusingjoinoptionandparmak Izi</span><span class="sxs-lookup"><span data-stu-id="f16e6-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f16e6-110">Workgroupnameparmak Izi</span><span class="sxs-lookup"><span data-stu-id="f16e6-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f16e6-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="f16e6-111">DESCRIPTION</span></span>
<span data-ttu-id="f16e6-112">**New-AzureServiceADDomainExtensionConfig** cmdlet 'i, bulut hizmetleri Için Active DIRECTORY (ad) etki alanı uzantısının yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f16e6-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="f16e6-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f16e6-113">EXAMPLES</span></span>

### <span data-ttu-id="f16e6-114">Örnek 1: AD etki alanı yapılandırmasını belirtme</span><span class="sxs-lookup"><span data-stu-id="f16e6-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="f16e6-115">Bu komut, AD etki alanı uzantısının yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f16e6-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="f16e6-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f16e6-116">PARAMETERS</span></span>

### <span data-ttu-id="f16e6-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f16e6-117">-CertificateThumbprint</span></span>
<span data-ttu-id="f16e6-118">Özel yapılandırmayı şifrelemek için kullanılacak sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="f16e6-119">Bu sertifika, sertifika deposunda zaten var.</span><span class="sxs-lookup"><span data-stu-id="f16e6-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="f16e6-120">Sertifika belirtmezseniz, bu cmdlet bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f16e6-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-121">-Credential</span><span class="sxs-lookup"><span data-stu-id="f16e6-121">-Credential</span></span>
<span data-ttu-id="f16e6-122">AD etki alanına katılmak için kullanılacak kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="f16e6-123">Kimlik bilgileri bir Kullanıcı adı ve parola içerir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-124">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="f16e6-124">-DomainName</span></span>
<span data-ttu-id="f16e6-125">AD etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-126">-ExtensionID</span><span class="sxs-lookup"><span data-stu-id="f16e6-126">-ExtensionId</span></span>
<span data-ttu-id="f16e6-127">Uzantı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-127">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="f16e6-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f16e6-128">-InformationAction</span></span>
<span data-ttu-id="f16e6-129">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f16e6-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f16e6-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f16e6-131">'A</span><span class="sxs-lookup"><span data-stu-id="f16e6-131">Continue</span></span>
- <span data-ttu-id="f16e6-132">Manıza</span><span class="sxs-lookup"><span data-stu-id="f16e6-132">Ignore</span></span>
- <span data-ttu-id="f16e6-133">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f16e6-133">Inquire</span></span>
- <span data-ttu-id="f16e6-134">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f16e6-134">SilentlyContinue</span></span>
- <span data-ttu-id="f16e6-135">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f16e6-135">Stop</span></span>
- <span data-ttu-id="f16e6-136">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f16e6-136">Suspend</span></span>

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

### <span data-ttu-id="f16e6-137">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f16e6-137">-InformationVariable</span></span>
<span data-ttu-id="f16e6-138">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f16e6-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="f16e6-139">-JoinOption</span></span>
<span data-ttu-id="f16e6-140">Katılma seçeneği numaralandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-141">-Seçenekler</span><span class="sxs-lookup"><span data-stu-id="f16e6-141">-Options</span></span>
<span data-ttu-id="f16e6-142">İşaretsiz tamsayı birleştirme seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="f16e6-143">-OUPath</span></span>
<span data-ttu-id="f16e6-144">AD etki alanına katılma işleminin kuruluş birimi (OU) yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-145">-Profil</span><span class="sxs-lookup"><span data-stu-id="f16e6-145">-Profile</span></span>
<span data-ttu-id="f16e6-146">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f16e6-147">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f16e6-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f16e6-148">-Restart</span><span class="sxs-lookup"><span data-stu-id="f16e6-148">-Restart</span></span>
<span data-ttu-id="f16e6-149">Katılma işlemi başarılı olursa bilgisayarın yeniden başlatılıp edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-150">-Role</span><span class="sxs-lookup"><span data-stu-id="f16e6-150">-Role</span></span>
<span data-ttu-id="f16e6-151">AD etki alanı yapılandırmasının uzak masaüstü yapılandırmasını belirtmek için isteğe bağlı bir rol dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="f16e6-152">Bu parametreyi belirtmezseniz, AD etki alanı yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f16e6-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="f16e6-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f16e6-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="f16e6-154">Sertifikayı tanıtmak için parmak iziyle kullanılan bir parmak izi karma algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="f16e6-155">Bu parametre isteğe bağlıdır ve varsayılan olarak SHA1 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f16e6-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="f16e6-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="f16e6-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="f16e6-157">AD etki alanına katılmak için kimlik bilgilerini (Kullanıcı adı ve parola) belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-158">-Version</span><span class="sxs-lookup"><span data-stu-id="f16e6-158">-Version</span></span>
<span data-ttu-id="f16e6-159">Uzantı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-160">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="f16e6-160">-WorkgroupName</span></span>
<span data-ttu-id="f16e6-161">Çalışma grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="f16e6-162">-X509Certificate</span></span>
<span data-ttu-id="f16e6-163">Bulut hizmetine otomatik olarak yüklenen ve uzantının özel yapılandırmasını şifrelemek için kullanılan bir X. 509.440 sertifikası belirtir.</span><span class="sxs-lookup"><span data-stu-id="f16e6-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f16e6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f16e6-164">CommonParameters</span></span>
<span data-ttu-id="f16e6-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f16e6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f16e6-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f16e6-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f16e6-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f16e6-167">INPUTS</span></span>

## <span data-ttu-id="f16e6-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f16e6-168">OUTPUTS</span></span>

## <span data-ttu-id="f16e6-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f16e6-169">NOTES</span></span>

## <span data-ttu-id="f16e6-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f16e6-170">RELATED LINKS</span></span>

[<span data-ttu-id="f16e6-171">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f16e6-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="f16e6-172">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f16e6-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


