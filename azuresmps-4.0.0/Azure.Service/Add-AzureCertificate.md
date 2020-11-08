---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106395"
---
# <span data-ttu-id="9a2bc-101">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9a2bc-101">Add-AzureCertificate</span></span>

## <span data-ttu-id="9a2bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="9a2bc-103">Bir Azure bulut hizmetine sertifika yükler.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-103">Uploads a certificate to an Azure cloud service.</span></span>

## <span data-ttu-id="9a2bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a2bc-104">SYNTAX</span></span>

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a2bc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="9a2bc-106">**Add-Azurecercertificate** . cmdlet 'ı bir Azure hizmeti için sertifika yükler.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-106">The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.</span></span>

## <span data-ttu-id="9a2bc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a2bc-107">EXAMPLES</span></span>

### <span data-ttu-id="9a2bc-108">Örnek 1: sertifikayı ve parolayı karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="9a2bc-108">Example 1: Upload a certificate and password</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

<span data-ttu-id="9a2bc-109">Bu komut, bir bulut hizmetine ContosoCertificate. pfx sertifika dosyasını yükler.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-109">This command uploads the certificate file ContosoCertificate.pfx to a cloud service.</span></span>
<span data-ttu-id="9a2bc-110">Komut, sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-110">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="9a2bc-111">Örnek 2: sertifika dosyası yükleme</span><span class="sxs-lookup"><span data-stu-id="9a2bc-111">Example 2: Upload a certificate file</span></span>
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

<span data-ttu-id="9a2bc-112">Bu komut, bir bulut hizmetine ContosoCertificate. cer sertifika dosyasını yükler.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-112">This command uploads the certificate file ContosoCertificate.cer to a cloud service.</span></span>
<span data-ttu-id="9a2bc-113">Komut, sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-113">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="9a2bc-114">Örnek 3: sertifika nesnesi yükleme</span><span class="sxs-lookup"><span data-stu-id="9a2bc-114">Example 3: Upload a certificate object</span></span>
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

<span data-ttu-id="9a2bc-115">İlk komut, Windows PowerShell çekirdek **Get-Item** cmdlet 'ini kullanarak bir Kullanıcı mağazasından bir sertifika alır.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-115">The first command gets a certificate from the MY store of a user by using the Windows PowerShell core **Get-Item** cmdlet.</span></span>
<span data-ttu-id="9a2bc-116">Komut, sertifikayı $Certificate değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-116">The command stores the certificate in the $Certificate variable.</span></span>

<span data-ttu-id="9a2bc-117">İkinci komut $certificate sertifikayı bir bulut hizmetine yükler.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-117">The second command uploads the certificate in $certificate to a cloud service.</span></span>

## <span data-ttu-id="9a2bc-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a2bc-118">PARAMETERS</span></span>

### <span data-ttu-id="9a2bc-119">-CertToDeploy</span><span class="sxs-lookup"><span data-stu-id="9a2bc-119">-CertToDeploy</span></span>
<span data-ttu-id="9a2bc-120">Dağıtılacak sertifikayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-120">Specifies the certificate to deploy.</span></span>
<span data-ttu-id="9a2bc-121">\*. Cer veya \* içeren dosya gibi bir sertifika dosyasının tam yolunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-121">You can specify the full path of a certificate file, such as a file that has a \*.cer or \*.</span></span>
<span data-ttu-id="9a2bc-122">pfx dosya adı uzantısı veya X. 509.440 sertifika nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-122">pfx file name extension, or an X.509 Certificate object.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a2bc-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9a2bc-123">-InformationAction</span></span>
<span data-ttu-id="9a2bc-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9a2bc-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9a2bc-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a2bc-126">'A</span><span class="sxs-lookup"><span data-stu-id="9a2bc-126">Continue</span></span>
- <span data-ttu-id="9a2bc-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="9a2bc-127">Ignore</span></span>
- <span data-ttu-id="9a2bc-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="9a2bc-128">Inquire</span></span>
- <span data-ttu-id="9a2bc-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="9a2bc-129">SilentlyContinue</span></span>
- <span data-ttu-id="9a2bc-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="9a2bc-130">Stop</span></span>
- <span data-ttu-id="9a2bc-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="9a2bc-131">Suspend</span></span>

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

### <span data-ttu-id="9a2bc-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="9a2bc-132">-InformationVariable</span></span>
<span data-ttu-id="9a2bc-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9a2bc-134">-Parola</span><span class="sxs-lookup"><span data-stu-id="9a2bc-134">-Password</span></span>
<span data-ttu-id="9a2bc-135">Sertifika parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-135">Specifies the certificate password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a2bc-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="9a2bc-136">-Profile</span></span>
<span data-ttu-id="9a2bc-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9a2bc-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9a2bc-139">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="9a2bc-139">-ServiceName</span></span>
<span data-ttu-id="9a2bc-140">Bu cmdlet 'in sertifika eklediği Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-140">Specifies the name of the Azure service to which this cmdlet adds a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a2bc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a2bc-141">CommonParameters</span></span>
<span data-ttu-id="9a2bc-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a2bc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a2bc-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a2bc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a2bc-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a2bc-144">INPUTS</span></span>

## <span data-ttu-id="9a2bc-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a2bc-145">OUTPUTS</span></span>

### <span data-ttu-id="9a2bc-146">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="9a2bc-146">ManagementOperationContext</span></span>

## <span data-ttu-id="9a2bc-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a2bc-147">NOTES</span></span>

## <span data-ttu-id="9a2bc-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a2bc-148">RELATED LINKS</span></span>

[<span data-ttu-id="9a2bc-149">Get-Azurecercertificate</span><span class="sxs-lookup"><span data-stu-id="9a2bc-149">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="9a2bc-150">New-Azurecercertificate Atesetting</span><span class="sxs-lookup"><span data-stu-id="9a2bc-150">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="9a2bc-151">Remove-Azurecercertificate</span><span class="sxs-lookup"><span data-stu-id="9a2bc-151">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


