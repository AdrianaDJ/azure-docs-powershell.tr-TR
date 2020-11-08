---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105896"
---
# <span data-ttu-id="90e9f-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="90e9f-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="90e9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="90e9f-103">Bir dağıtım için bulut hizmeti uzantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90e9f-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="90e9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90e9f-104">SYNTAX</span></span>

### <span data-ttu-id="90e9f-105">NewExtension (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="90e9f-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="90e9f-106">Newextensionusingparmak Izi</span><span class="sxs-lookup"><span data-stu-id="90e9f-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="90e9f-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="90e9f-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="90e9f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="90e9f-108">DESCRIPTION</span></span>
<span data-ttu-id="90e9f-109">**New-AzureServiceExtensionConfig** cmdlet 'i bir dağıtım için bulut hizmeti uzantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90e9f-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="90e9f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90e9f-110">EXAMPLES</span></span>

### <span data-ttu-id="90e9f-111">Örnek 1: uzantı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="90e9f-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="90e9f-112">Bu komut, bir uzantı yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="90e9f-113">Örnek 2: rol için genişletme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="90e9f-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="90e9f-114">Bu komut, rol WebRole1 için bir genişletme yapılandırması belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="90e9f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90e9f-115">PARAMETERS</span></span>

### <span data-ttu-id="90e9f-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="90e9f-116">-CertificateThumbprint</span></span>
<span data-ttu-id="90e9f-117">Özel yapılandırmayı şifrelemek için kullanılacak sertifika parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="90e9f-118">Bu sertifika, sertifika deposunda zaten var.</span><span class="sxs-lookup"><span data-stu-id="90e9f-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="90e9f-119">Sertifika belirtmezseniz, bu cmdlet bir sertifika oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90e9f-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="90e9f-120">-ExtensionID</span><span class="sxs-lookup"><span data-stu-id="90e9f-120">-ExtensionId</span></span>
<span data-ttu-id="90e9f-121">Uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-121">Specifies the name of the extension.</span></span>

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

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e9f-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="90e9f-122">-ExtensionName</span></span>
<span data-ttu-id="90e9f-123">Uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e9f-124">-ExtensionState</span><span class="sxs-lookup"><span data-stu-id="90e9f-124">-ExtensionState</span></span>
<span data-ttu-id="90e9f-125">Uzantının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="90e9f-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="90e9f-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90e9f-127">Etkinleştiremez</span><span class="sxs-lookup"><span data-stu-id="90e9f-127">Enable</span></span> 
- <span data-ttu-id="90e9f-128">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="90e9f-128">Disable</span></span> 
- <span data-ttu-id="90e9f-129">Kaldırma</span><span class="sxs-lookup"><span data-stu-id="90e9f-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e9f-130">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="90e9f-130">-InformationAction</span></span>
<span data-ttu-id="90e9f-131">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="90e9f-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="90e9f-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90e9f-133">'A</span><span class="sxs-lookup"><span data-stu-id="90e9f-133">Continue</span></span>
- <span data-ttu-id="90e9f-134">Manıza</span><span class="sxs-lookup"><span data-stu-id="90e9f-134">Ignore</span></span>
- <span data-ttu-id="90e9f-135">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="90e9f-135">Inquire</span></span>
- <span data-ttu-id="90e9f-136">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="90e9f-136">SilentlyContinue</span></span>
- <span data-ttu-id="90e9f-137">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="90e9f-137">Stop</span></span>
- <span data-ttu-id="90e9f-138">Biliriz</span><span class="sxs-lookup"><span data-stu-id="90e9f-138">Suspend</span></span>

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

### <span data-ttu-id="90e9f-139">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="90e9f-139">-InformationVariable</span></span>
<span data-ttu-id="90e9f-140">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="90e9f-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e9f-141">-PrivateConfiguration</span></span>
<span data-ttu-id="90e9f-142">Özel yapılandırma metnini belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e9f-143">-Profil</span><span class="sxs-lookup"><span data-stu-id="90e9f-143">-Profile</span></span>
<span data-ttu-id="90e9f-144">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="90e9f-145">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="90e9f-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90e9f-146">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="90e9f-146">-ProviderNamespace</span></span>
<span data-ttu-id="90e9f-147">Uzantının sağlayıcı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e9f-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="90e9f-148">-PublicConfiguration</span></span>
<span data-ttu-id="90e9f-149">Genel yapılandırma metnini belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e9f-150">-Role</span><span class="sxs-lookup"><span data-stu-id="90e9f-150">-Role</span></span>
<span data-ttu-id="90e9f-151">Uzak Masaüstü yapılandırmasını belirtmek için isteğe bağlı bir rol dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="90e9f-152">Belirtilmezse, uzak masaüstü yapılandırması tüm roller için varsayılan yapılandırma olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="90e9f-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="90e9f-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="90e9f-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="90e9f-154">Sertifikayı tanıtmak için parmak iziyle kullanılan bir parmak izi karma algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="90e9f-155">Bu parametre isteğe bağlıdır ve varsayılan olarak SHA1 kullanılır.</span><span class="sxs-lookup"><span data-stu-id="90e9f-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="90e9f-156">-Version</span><span class="sxs-lookup"><span data-stu-id="90e9f-156">-Version</span></span>
<span data-ttu-id="90e9f-157">Uzantı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-157">Specifies the extension version.</span></span>

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

### <span data-ttu-id="90e9f-158">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="90e9f-158">-X509Certificate</span></span>
<span data-ttu-id="90e9f-159">Belirtilen bir x509 sertifikasını, bu sertifikanın otomatik olarak bulut hizmetine yüklenip, uzantının özel yapılandırmasını şifrelemek için kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90e9f-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="90e9f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e9f-160">CommonParameters</span></span>
<span data-ttu-id="90e9f-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90e9f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e9f-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e9f-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e9f-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90e9f-163">INPUTS</span></span>

## <span data-ttu-id="90e9f-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90e9f-164">OUTPUTS</span></span>

## <span data-ttu-id="90e9f-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90e9f-165">NOTES</span></span>

## <span data-ttu-id="90e9f-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90e9f-166">RELATED LINKS</span></span>

[<span data-ttu-id="90e9f-167">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="90e9f-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="90e9f-168">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="90e9f-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


