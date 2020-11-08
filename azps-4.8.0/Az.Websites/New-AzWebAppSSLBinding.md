---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268600"
---
# <span data-ttu-id="82ade-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="82ade-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="82ade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82ade-102">SYNOPSIS</span></span>
<span data-ttu-id="82ade-103">Azure Web App için SSL sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82ade-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="82ade-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82ade-104">SYNTAX</span></span>

### <span data-ttu-id="82ade-105">S1</span><span class="sxs-lookup"><span data-stu-id="82ade-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82ade-106">S2</span><span class="sxs-lookup"><span data-stu-id="82ade-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82ade-107">S3</span><span class="sxs-lookup"><span data-stu-id="82ade-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82ade-108">Modundan</span><span class="sxs-lookup"><span data-stu-id="82ade-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82ade-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="82ade-109">DESCRIPTION</span></span>
<span data-ttu-id="82ade-110">**Yeni-AzWebAppSSLBinding** cmdlet 'i, bir Azure Web App Için güvenli yuva KATMANı (SSL) sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82ade-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="82ade-111">Cmdlet iki yoldan bir SSL bağlaması oluşturur:</span><span class="sxs-lookup"><span data-stu-id="82ade-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="82ade-112">Web uygulamasını var olan bir sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82ade-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="82ade-113">Yeni bir sertifikayı karşıya yükleyebilir ve Web uygulamasını bu yeni sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82ade-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="82ade-114">Kullandığınız yaklaşımdan bağımsız olarak, sertifika ve Web uygulaması aynı Azure Resource grubuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="82ade-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="82ade-115">A kaynak grubunda bir Web uygulamanız varsa ve bu Web uygulamasını B kaynak grubundaki bir sertifikaya bağlamak istiyorsanız, bunu yapmanın tek yolu, sertifikanın bir kopyasını kaynak grubuna A yüklemek demektir. Yeni bir sertifikayı karşıya yüklediyseniz, bir Azure SSL sertifikası için aşağıdaki gereksinimleri aklınızda bulundurun:</span><span class="sxs-lookup"><span data-stu-id="82ade-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="82ade-116">Sertifikanın özel bir anahtar içermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="82ade-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="82ade-117">Sertifikanın kişisel bilgi değişimi (PFX) biçimini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="82ade-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="82ade-118">Sertifikanın konu adı, Web uygulamasına erişmek için kullanılan etki alanıyla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="82ade-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="82ade-119">Sertifikanın en az 2048 bit şifreleme kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="82ade-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="82ade-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82ade-120">EXAMPLES</span></span>

### <span data-ttu-id="82ade-121">Örnek 1: sertifikayı Web uygulamasına bağlama</span><span class="sxs-lookup"><span data-stu-id="82ade-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="82ade-122">Bu komut mevcut bir Azure sertifikasını (Parmak Izi E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 sertifika), ContosoWebApp adlı Web uygulamasına bağlar.</span><span class="sxs-lookup"><span data-stu-id="82ade-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="82ade-123">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="82ade-123">Example 2</span></span>

<span data-ttu-id="82ade-124">Azure Web App için SSL sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82ade-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="82ade-125">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="82ade-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="82ade-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82ade-126">PARAMETERS</span></span>

### <span data-ttu-id="82ade-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="82ade-127">-CertificateFilePath</span></span>
<span data-ttu-id="82ade-128">Karşıya yüklenecek sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="82ade-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="82ade-129">*Certificatefilepath* parametresi yalnızca sertifika henüz Azure 'a yüklenmediyse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="82ade-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="82ade-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="82ade-130">-CertificatePassword</span></span>
<span data-ttu-id="82ade-131">Sertifikanın şifre çözme parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82ade-131">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="82ade-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ade-132">-DefaultProfile</span></span>
<span data-ttu-id="82ade-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82ade-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82ade-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="82ade-134">-Name</span></span>
<span data-ttu-id="82ade-135">Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82ade-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="82ade-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ade-136">-ResourceGroupName</span></span>
<span data-ttu-id="82ade-137">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82ade-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="82ade-138">Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="82ade-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="82ade-139">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="82ade-139">-Slot</span></span>
<span data-ttu-id="82ade-140">Web uygulaması dağıtım yuvasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82ade-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="82ade-141">Yuva almak için Get-AzWebAppSlot cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82ade-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="82ade-142">Dağıtım yuvaları, Internet üzerinden erişilebilir olması gerekmeden Web uygulamalarını, Web uygulamalarını aşamalandırmanızın ve doğrulayamanızın bir yolunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="82ade-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="82ade-143">Genellikle değişikliklerinizi bir basamaklandırma sitesine dağıtırsınız, bu değişiklikleri doğrulayabilir ve ardından üretime (Internet erişimi erişilebilir) dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="82ade-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="82ade-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="82ade-144">-SslState</span></span>
<span data-ttu-id="82ade-145">Sertifikanın etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="82ade-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="82ade-146">Sertifikayı etkinleştirmek için *SslState* parametresini 1 olarak ayarlayın veya sertifikayı devre dışı bırakmak Için *SslState* 'i 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="82ade-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="82ade-147">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="82ade-147">-Thumbprint</span></span>
<span data-ttu-id="82ade-148">Sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82ade-148">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="82ade-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="82ade-149">-WebApp</span></span>
<span data-ttu-id="82ade-150">Web uygulaması belirtir.</span><span class="sxs-lookup"><span data-stu-id="82ade-150">Specifies a Web App.</span></span>
<span data-ttu-id="82ade-151">Web uygulaması edinmek için Get-AzWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="82ade-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="82ade-152">*WebApp* parametresini, *resourcegroupname* parametresi ve/veya *webappname* ile aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="82ade-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="82ade-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="82ade-153">-WebAppName</span></span>
<span data-ttu-id="82ade-154">Yeni SSL bağlaması oluşturulan Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82ade-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="82ade-155">Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="82ade-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="82ade-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ade-156">CommonParameters</span></span>
<span data-ttu-id="82ade-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82ade-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ade-158">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ade-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ade-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82ade-159">INPUTS</span></span>

### <span data-ttu-id="82ade-160">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="82ade-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="82ade-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82ade-161">OUTPUTS</span></span>

### <span data-ttu-id="82ade-162">Microsoft. Azure. Management. Web sitesi. modeller. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="82ade-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="82ade-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82ade-163">NOTES</span></span>

## <span data-ttu-id="82ade-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82ade-164">RELATED LINKS</span></span>

[<span data-ttu-id="82ade-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="82ade-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="82ade-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="82ade-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="82ade-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="82ade-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="82ade-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="82ade-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


