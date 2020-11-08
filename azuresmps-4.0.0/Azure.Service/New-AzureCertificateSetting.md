---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105932"
---
# <span data-ttu-id="f19ec-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="f19ec-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="f19ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f19ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f19ec-103">Sertifika için sertifika ayarı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f19ec-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="f19ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f19ec-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f19ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f19ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f19ec-106">**New-Azurecercertificate Atesetting** cmdlet 'ı, Azure hizmetinde bulunan bir sertifika için sertifika ayarı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f19ec-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="f19ec-107">**Add-AzureProvisioningConfig** cmdlet 'ini kullanarak yapılandırma nesnesi oluşturmak için sertifika ayarı nesnesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f19ec-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="f19ec-108">**New-AzureVM** cmdlet 'ini kullanarak sanal makine oluşturmak için yapılandırma nesnesi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f19ec-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f19ec-109">**Yeni-Azutalep Ickvm** cmdlet 'ini kullanarak sanal makine oluşturmak için sertifika ayarı nesnesi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f19ec-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="f19ec-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f19ec-110">EXAMPLES</span></span>

### <span data-ttu-id="f19ec-111">Örnek 1: sertifika ayar nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f19ec-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="f19ec-112">Bu komut, var olan bir sertifika için sertifika ayarı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f19ec-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="f19ec-113">Örnek 2: yapılandırma ayarı nesnesini kullanan bir sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="f19ec-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="f19ec-114">İlk komut, **Add-Azurecercertificate** . cer 'i kullanarak, contosocert. cer ' i contosohizmeti adlı hizmete ekler.</span><span class="sxs-lookup"><span data-stu-id="f19ec-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="f19ec-115">İkinci komut bir sertifika ayarı nesnesi oluşturur ve $CertificateSetting değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f19ec-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="f19ec-116">Üçüncü komut, **Get-AzureVMImage** cmdlet 'ini kullanarak görüntü deposundaki bir resmi alır.</span><span class="sxs-lookup"><span data-stu-id="f19ec-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="f19ec-117">Bu komut, resmi $Image değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f19ec-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="f19ec-118">Son komutu, **Yeni-AzureVMConfig** cmdlet 'ini kullanarak $Image resim temelinde bir sanal makine yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f19ec-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="f19ec-119">Komut, bu nesneyi ardışık düzen işlecini kullanarak **Add-AzureProvisioningConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f19ec-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f19ec-120">Bu cmdlet, yapılandırma bilgilerini yapılandırmaya ekler.</span><span class="sxs-lookup"><span data-stu-id="f19ec-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="f19ec-121">Komut, nesneyi sanal makineyi oluşturan **New-AzureVM** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f19ec-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="f19ec-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f19ec-122">PARAMETERS</span></span>

### <span data-ttu-id="f19ec-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f19ec-123">-InformationAction</span></span>
<span data-ttu-id="f19ec-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f19ec-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f19ec-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f19ec-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f19ec-126">'A</span><span class="sxs-lookup"><span data-stu-id="f19ec-126">Continue</span></span>
- <span data-ttu-id="f19ec-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="f19ec-127">Ignore</span></span>
- <span data-ttu-id="f19ec-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="f19ec-128">Inquire</span></span>
- <span data-ttu-id="f19ec-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="f19ec-129">SilentlyContinue</span></span>
- <span data-ttu-id="f19ec-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="f19ec-130">Stop</span></span>
- <span data-ttu-id="f19ec-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="f19ec-131">Suspend</span></span>

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

### <span data-ttu-id="f19ec-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="f19ec-132">-InformationVariable</span></span>
<span data-ttu-id="f19ec-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="f19ec-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f19ec-134">-StoreName</span><span class="sxs-lookup"><span data-stu-id="f19ec-134">-StoreName</span></span>
<span data-ttu-id="f19ec-135">Sertifikanın yerleştirileceği sertifika deposunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f19ec-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="f19ec-136">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f19ec-136">Valid values are:</span></span> 

- <span data-ttu-id="f19ec-137">Adres defteri</span><span class="sxs-lookup"><span data-stu-id="f19ec-137">AddressBook</span></span>
- <span data-ttu-id="f19ec-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="f19ec-138">AuthRoot</span></span>
- <span data-ttu-id="f19ec-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="f19ec-139">CertificateAuthority</span></span>
- <span data-ttu-id="f19ec-140">Verilemeyen</span><span class="sxs-lookup"><span data-stu-id="f19ec-140">Disallowed</span></span>
- <span data-ttu-id="f19ec-141">Bilgilerimi</span><span class="sxs-lookup"><span data-stu-id="f19ec-141">My</span></span>
- <span data-ttu-id="f19ec-142">Kökü</span><span class="sxs-lookup"><span data-stu-id="f19ec-142">Root</span></span>
- <span data-ttu-id="f19ec-143">Trustedkişilerim</span><span class="sxs-lookup"><span data-stu-id="f19ec-143">TrustedPeople</span></span>
- <span data-ttu-id="f19ec-144">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="f19ec-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19ec-145">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="f19ec-145">-Thumbprint</span></span>
<span data-ttu-id="f19ec-146">Sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f19ec-146">Specifies the thumbprint of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f19ec-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19ec-147">CommonParameters</span></span>
<span data-ttu-id="f19ec-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f19ec-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19ec-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f19ec-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19ec-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f19ec-150">INPUTS</span></span>

## <span data-ttu-id="f19ec-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f19ec-151">OUTPUTS</span></span>

## <span data-ttu-id="f19ec-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f19ec-152">NOTES</span></span>

## <span data-ttu-id="f19ec-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f19ec-153">RELATED LINKS</span></span>

[<span data-ttu-id="f19ec-154">Add-Azurecercertificate</span><span class="sxs-lookup"><span data-stu-id="f19ec-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="f19ec-155">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="f19ec-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="f19ec-156">Get-Azurecercertificate</span><span class="sxs-lookup"><span data-stu-id="f19ec-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="f19ec-157">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="f19ec-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="f19ec-158">Yeni-Azutalep Ickvm</span><span class="sxs-lookup"><span data-stu-id="f19ec-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="f19ec-159">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f19ec-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="f19ec-160">Remove-Azurecercertificate</span><span class="sxs-lookup"><span data-stu-id="f19ec-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


