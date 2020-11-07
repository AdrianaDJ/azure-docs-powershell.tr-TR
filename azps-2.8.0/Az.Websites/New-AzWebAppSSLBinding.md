---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: ed0e0f0ddf42266921113b219d81cfd5b6b6417c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932374"
---
# <span data-ttu-id="79af9-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="79af9-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="79af9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79af9-102">SYNOPSIS</span></span>
<span data-ttu-id="79af9-103">Azure Web App için SSL sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79af9-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="79af9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79af9-104">SYNTAX</span></span>

### <span data-ttu-id="79af9-105">S1</span><span class="sxs-lookup"><span data-stu-id="79af9-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79af9-106">S2</span><span class="sxs-lookup"><span data-stu-id="79af9-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79af9-107">S3</span><span class="sxs-lookup"><span data-stu-id="79af9-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79af9-108">Modundan</span><span class="sxs-lookup"><span data-stu-id="79af9-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79af9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="79af9-109">DESCRIPTION</span></span>
<span data-ttu-id="79af9-110">**Yeni-AzWebAppSSLBinding** cmdlet 'i, bir Azure Web App Için güvenli yuva KATMANı (SSL) sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79af9-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="79af9-111">Cmdlet iki yoldan bir SSL bağlaması oluşturur:</span><span class="sxs-lookup"><span data-stu-id="79af9-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="79af9-112">Web uygulamasını var olan bir sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79af9-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="79af9-113">Yeni bir sertifikayı karşıya yükleyebilir ve Web uygulamasını bu yeni sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79af9-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="79af9-114">Kullandığınız yaklaşımdan bağımsız olarak, sertifika ve Web uygulaması aynı Azure Resource grubuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="79af9-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="79af9-115">A kaynak grubunda bir Web uygulamanız varsa ve bu Web uygulamasını B kaynak grubundaki bir sertifikaya bağlamak istiyorsanız, bunu yapmanın tek yolu, sertifikanın bir kopyasını kaynak grubuna A yüklemek demektir. Yeni bir sertifikayı karşıya yüklediyseniz, bir Azure SSL sertifikası için aşağıdaki gereksinimleri aklınızda bulundurun:</span><span class="sxs-lookup"><span data-stu-id="79af9-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="79af9-116">Sertifikanın özel bir anahtar içermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="79af9-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="79af9-117">Sertifikanın kişisel bilgi değişimi (PFX) biçimini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="79af9-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="79af9-118">Sertifikanın konu adı, Web uygulamasına erişmek için kullanılan etki alanıyla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="79af9-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="79af9-119">Sertifikanın en az 2048 bit şifreleme kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="79af9-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="79af9-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79af9-120">EXAMPLES</span></span>

### <span data-ttu-id="79af9-121">Örnek 1: sertifikayı Web uygulamasına bağlama</span><span class="sxs-lookup"><span data-stu-id="79af9-121">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="79af9-122">Bu komut mevcut bir Azure sertifikasını (Parmak Izi E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 sertifika), ContosoWebApp adlı Web uygulamasına bağlar.</span><span class="sxs-lookup"><span data-stu-id="79af9-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="79af9-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79af9-123">PARAMETERS</span></span>

### <span data-ttu-id="79af9-124">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="79af9-124">-CertificateFilePath</span></span>
<span data-ttu-id="79af9-125">Karşıya yüklenecek sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="79af9-125">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="79af9-126">*Certificatefilepath* parametresi yalnızca sertifika henüz Azure 'a yüklenmediyse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="79af9-126">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="79af9-127">-CertificatePassword</span></span>
<span data-ttu-id="79af9-128">Sertifikanın şifre çözme parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79af9-128">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79af9-129">-DefaultProfile</span></span>
<span data-ttu-id="79af9-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79af9-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="79af9-131">-Name</span></span>
<span data-ttu-id="79af9-132">Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79af9-132">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79af9-133">-ResourceGroupName</span></span>
<span data-ttu-id="79af9-134">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79af9-134">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="79af9-135">Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="79af9-135">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-136">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="79af9-136">-Slot</span></span>
<span data-ttu-id="79af9-137">Web uygulaması dağıtım yuvasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79af9-137">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="79af9-138">Yuva almak için Get-AzWebAppSlot cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79af9-138">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="79af9-139">Dağıtım yuvaları, Internet üzerinden erişilebilir olması gerekmeden Web uygulamalarını, Web uygulamalarını aşamalandırmanızın ve doğrulayamanızın bir yolunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="79af9-139">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="79af9-140">Genellikle değişikliklerinizi bir basamaklandırma sitesine dağıtırsınız, bu değişiklikleri doğrulayabilir ve ardından üretime (Internet erişimi erişilebilir) dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79af9-140">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-141">-SslState</span><span class="sxs-lookup"><span data-stu-id="79af9-141">-SslState</span></span>
<span data-ttu-id="79af9-142">Sertifikanın etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79af9-142">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="79af9-143">Sertifikayı etkinleştirmek için *SslState* parametresini 1 olarak ayarlayın veya sertifikayı devre dışı bırakmak Için *SslState* 'i 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="79af9-143">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-144">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="79af9-144">-Thumbprint</span></span>
<span data-ttu-id="79af9-145">Sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79af9-145">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-146">-WebApp</span><span class="sxs-lookup"><span data-stu-id="79af9-146">-WebApp</span></span>
<span data-ttu-id="79af9-147">Web uygulaması belirtir.</span><span class="sxs-lookup"><span data-stu-id="79af9-147">Specifies a Web App.</span></span>
<span data-ttu-id="79af9-148">Web uygulaması edinmek için Get-AzWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="79af9-148">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="79af9-149">*WebApp* parametresini, *resourcegroupname* parametresi ve/veya *webappname* ile aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="79af9-149">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-150">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="79af9-150">-WebAppName</span></span>
<span data-ttu-id="79af9-151">Yeni SSL bağlaması oluşturulan Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79af9-151">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="79af9-152">Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="79af9-152">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79af9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79af9-153">CommonParameters</span></span>
<span data-ttu-id="79af9-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79af9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79af9-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79af9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79af9-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79af9-156">INPUTS</span></span>

### <span data-ttu-id="79af9-157">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="79af9-157">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="79af9-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79af9-158">OUTPUTS</span></span>

### <span data-ttu-id="79af9-159">Microsoft. Azure. Management. Web sitesi. modeller. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="79af9-159">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="79af9-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79af9-160">NOTES</span></span>

## <span data-ttu-id="79af9-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79af9-161">RELATED LINKS</span></span>

[<span data-ttu-id="79af9-162">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="79af9-162">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="79af9-163">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="79af9-163">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="79af9-164">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="79af9-164">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="79af9-165">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="79af9-165">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


