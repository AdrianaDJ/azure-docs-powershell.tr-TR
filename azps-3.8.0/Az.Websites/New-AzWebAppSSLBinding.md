---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1f43b551a24cc0e98c3c42322b030549a74938
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096212"
---
# <span data-ttu-id="4cd3b-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="4cd3b-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="4cd3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd3b-103">Azure Web App için SSL sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="4cd3b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cd3b-104">SYNTAX</span></span>

### <span data-ttu-id="4cd3b-105">S1</span><span class="sxs-lookup"><span data-stu-id="4cd3b-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cd3b-106">S2</span><span class="sxs-lookup"><span data-stu-id="4cd3b-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cd3b-107">S3</span><span class="sxs-lookup"><span data-stu-id="4cd3b-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cd3b-108">Modundan</span><span class="sxs-lookup"><span data-stu-id="4cd3b-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cd3b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cd3b-109">DESCRIPTION</span></span>
<span data-ttu-id="4cd3b-110">**Yeni-AzWebAppSSLBinding** cmdlet 'i, bir Azure Web App Için güvenli yuva KATMANı (SSL) sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="4cd3b-111">Cmdlet iki yoldan bir SSL bağlaması oluşturur:</span><span class="sxs-lookup"><span data-stu-id="4cd3b-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="4cd3b-112">Web uygulamasını var olan bir sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="4cd3b-113">Yeni bir sertifikayı karşıya yükleyebilir ve Web uygulamasını bu yeni sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="4cd3b-114">Kullandığınız yaklaşımdan bağımsız olarak, sertifika ve Web uygulaması aynı Azure Resource grubuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="4cd3b-115">A kaynak grubunda bir Web uygulamanız varsa ve bu Web uygulamasını B kaynak grubundaki bir sertifikaya bağlamak istiyorsanız, bunu yapmanın tek yolu, sertifikanın bir kopyasını kaynak grubuna A yüklemek demektir. Yeni bir sertifikayı karşıya yüklediyseniz, bir Azure SSL sertifikası için aşağıdaki gereksinimleri aklınızda bulundurun:</span><span class="sxs-lookup"><span data-stu-id="4cd3b-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="4cd3b-116">Sertifikanın özel bir anahtar içermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="4cd3b-117">Sertifikanın kişisel bilgi değişimi (PFX) biçimini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="4cd3b-118">Sertifikanın konu adı, Web uygulamasına erişmek için kullanılan etki alanıyla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="4cd3b-119">Sertifikanın en az 2048 bit şifreleme kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="4cd3b-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cd3b-120">EXAMPLES</span></span>

### <span data-ttu-id="4cd3b-121">Örnek 1: sertifikayı Web uygulamasına bağlama</span><span class="sxs-lookup"><span data-stu-id="4cd3b-121">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="4cd3b-122">Bu komut mevcut bir Azure sertifikasını (Parmak Izi E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 sertifika), ContosoWebApp adlı Web uygulamasına bağlar.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="4cd3b-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cd3b-123">PARAMETERS</span></span>

### <span data-ttu-id="4cd3b-124">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4cd3b-124">-CertificateFilePath</span></span>
<span data-ttu-id="4cd3b-125">Karşıya yüklenecek sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-125">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="4cd3b-126">*Certificatefilepath* parametresi yalnızca sertifika henüz Azure 'a yüklenmediyse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-126">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="4cd3b-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4cd3b-127">-CertificatePassword</span></span>
<span data-ttu-id="4cd3b-128">Sertifikanın şifre çözme parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-128">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="4cd3b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd3b-129">-DefaultProfile</span></span>
<span data-ttu-id="4cd3b-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cd3b-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="4cd3b-131">-Name</span></span>
<span data-ttu-id="4cd3b-132">Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-132">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="4cd3b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd3b-133">-ResourceGroupName</span></span>
<span data-ttu-id="4cd3b-134">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-134">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="4cd3b-135">Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-135">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="4cd3b-136">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="4cd3b-136">-Slot</span></span>
<span data-ttu-id="4cd3b-137">Web uygulaması dağıtım yuvasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-137">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="4cd3b-138">Yuva almak için Get-AzWebAppSlot cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-138">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="4cd3b-139">Dağıtım yuvaları, Internet üzerinden erişilebilir olması gerekmeden Web uygulamalarını, Web uygulamalarını aşamalandırmanızın ve doğrulayamanızın bir yolunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-139">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="4cd3b-140">Genellikle değişikliklerinizi bir basamaklandırma sitesine dağıtırsınız, bu değişiklikleri doğrulayabilir ve ardından üretime (Internet erişimi erişilebilir) dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-140">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="4cd3b-141">-SslState</span><span class="sxs-lookup"><span data-stu-id="4cd3b-141">-SslState</span></span>
<span data-ttu-id="4cd3b-142">Sertifikanın etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-142">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="4cd3b-143">Sertifikayı etkinleştirmek için *SslState* parametresini 1 olarak ayarlayın veya sertifikayı devre dışı bırakmak Için *SslState* 'i 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-143">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="4cd3b-144">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="4cd3b-144">-Thumbprint</span></span>
<span data-ttu-id="4cd3b-145">Sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-145">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="4cd3b-146">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4cd3b-146">-WebApp</span></span>
<span data-ttu-id="4cd3b-147">Web uygulaması belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-147">Specifies a Web App.</span></span>
<span data-ttu-id="4cd3b-148">Web uygulaması edinmek için Get-AzWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-148">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="4cd3b-149">*WebApp* parametresini, *resourcegroupname* parametresi ve/veya *webappname* ile aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-149">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="4cd3b-150">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="4cd3b-150">-WebAppName</span></span>
<span data-ttu-id="4cd3b-151">Yeni SSL bağlaması oluşturulan Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-151">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="4cd3b-152">Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-152">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="4cd3b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd3b-153">CommonParameters</span></span>
<span data-ttu-id="4cd3b-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cd3b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd3b-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd3b-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd3b-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cd3b-156">INPUTS</span></span>

### <span data-ttu-id="4cd3b-157">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="4cd3b-157">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4cd3b-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cd3b-158">OUTPUTS</span></span>

### <span data-ttu-id="4cd3b-159">Microsoft. Azure. Management. Web sitesi. modeller. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="4cd3b-159">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="4cd3b-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cd3b-160">NOTES</span></span>

## <span data-ttu-id="4cd3b-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cd3b-161">RELATED LINKS</span></span>

[<span data-ttu-id="4cd3b-162">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="4cd3b-162">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="4cd3b-163">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="4cd3b-163">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="4cd3b-164">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4cd3b-164">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="4cd3b-165">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4cd3b-165">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

