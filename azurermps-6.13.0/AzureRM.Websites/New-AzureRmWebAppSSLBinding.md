---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 33efe02dd463334745e39d846d0b43c2ccd9dd6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764090"
---
# <span data-ttu-id="90b65-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="90b65-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="90b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90b65-102">SYNOPSIS</span></span>
<span data-ttu-id="90b65-103">Azure Web App için SSL sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90b65-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90b65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90b65-104">SYNTAX</span></span>

### <span data-ttu-id="90b65-105">S1</span><span class="sxs-lookup"><span data-stu-id="90b65-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90b65-106">S2</span><span class="sxs-lookup"><span data-stu-id="90b65-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90b65-107">S3</span><span class="sxs-lookup"><span data-stu-id="90b65-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90b65-108">Modundan</span><span class="sxs-lookup"><span data-stu-id="90b65-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90b65-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="90b65-109">DESCRIPTION</span></span>
<span data-ttu-id="90b65-110">**Yeni-AzureRmWebAppSSLBinding** cmdlet 'i, bir Azure Web App Için güvenli yuva KATMANı (SSL) sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90b65-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="90b65-111">Cmdlet iki yoldan bir SSL bağlaması oluşturur:</span><span class="sxs-lookup"><span data-stu-id="90b65-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="90b65-112">Web uygulamasını var olan bir sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="90b65-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="90b65-113">Yeni bir sertifikayı karşıya yükleyebilir ve Web uygulamasını bu yeni sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="90b65-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="90b65-114">Kullandığınız yaklaşımdan bağımsız olarak, sertifika ve Web uygulaması aynı Azure Resource grubuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="90b65-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="90b65-115">A kaynak grubunda bir Web uygulamanız varsa ve bu Web uygulamasını B kaynak grubundaki bir sertifikaya bağlamak istiyorsanız, bunu yapmanın tek yolu, sertifikanın bir kopyasını kaynak grubuna A yüklemek demektir. Yeni bir sertifikayı karşıya yüklediyseniz, bir Azure SSL sertifikası için aşağıdaki gereksinimleri aklınızda bulundurun:</span><span class="sxs-lookup"><span data-stu-id="90b65-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="90b65-116">Sertifikanın özel bir anahtar içermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="90b65-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="90b65-117">Sertifikanın kişisel bilgi değişimi (PFX) biçimini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="90b65-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="90b65-118">Sertifikanın konu adı, Web uygulamasına erişmek için kullanılan etki alanıyla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="90b65-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="90b65-119">Sertifikanın en az 2048 bit şifreleme kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="90b65-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="90b65-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90b65-120">EXAMPLES</span></span>

### <span data-ttu-id="90b65-121">Örnek 1: sertifikayı Web uygulamasına bağlama</span><span class="sxs-lookup"><span data-stu-id="90b65-121">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="90b65-122">Bu komut mevcut bir Azure sertifikasını (Parmak Izi E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 sertifika), ContosoWebApp adlı Web uygulamasına bağlar.</span><span class="sxs-lookup"><span data-stu-id="90b65-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="90b65-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90b65-123">PARAMETERS</span></span>

### <span data-ttu-id="90b65-124">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="90b65-124">-CertificateFilePath</span></span>
<span data-ttu-id="90b65-125">Karşıya yüklenecek sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="90b65-125">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="90b65-126">*Certificatefilepath* parametresi yalnızca sertifika henüz Azure 'a yüklenmediyse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="90b65-126">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="90b65-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="90b65-127">-CertificatePassword</span></span>
<span data-ttu-id="90b65-128">Sertifikanın şifre çözme parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90b65-128">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="90b65-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b65-129">-DefaultProfile</span></span>
<span data-ttu-id="90b65-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90b65-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b65-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="90b65-131">-Name</span></span>
<span data-ttu-id="90b65-132">Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90b65-132">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="90b65-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b65-133">-ResourceGroupName</span></span>
<span data-ttu-id="90b65-134">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90b65-134">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="90b65-135">Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="90b65-135">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="90b65-136">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="90b65-136">-Slot</span></span>
<span data-ttu-id="90b65-137">Web uygulaması dağıtım yuvasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90b65-137">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="90b65-138">Yuva almak için Get-AzureRMWebAppSlot cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="90b65-138">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="90b65-139">Dağıtım yuvaları, Internet üzerinden erişilebilir olması gerekmeden Web uygulamalarını, Web uygulamalarını aşamalandırmanızın ve doğrulayamanızın bir yolunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="90b65-139">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="90b65-140">Genellikle değişikliklerinizi bir basamaklandırma sitesine dağıtırsınız, bu değişiklikleri doğrulayabilir ve ardından üretime (Internet erişimi erişilebilir) dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="90b65-140">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="90b65-141">-SslState</span><span class="sxs-lookup"><span data-stu-id="90b65-141">-SslState</span></span>
<span data-ttu-id="90b65-142">Sertifikanın etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="90b65-142">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="90b65-143">Sertifikayı etkinleştirmek için *SslState* parametresini 1 olarak ayarlayın veya sertifikayı devre dışı bırakmak Için *SslState* 'i 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="90b65-143">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="90b65-144">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="90b65-144">-Thumbprint</span></span>
<span data-ttu-id="90b65-145">Sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90b65-145">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="90b65-146">-WebApp</span><span class="sxs-lookup"><span data-stu-id="90b65-146">-WebApp</span></span>
<span data-ttu-id="90b65-147">Web uygulaması belirtir.</span><span class="sxs-lookup"><span data-stu-id="90b65-147">Specifies a Web App.</span></span>
<span data-ttu-id="90b65-148">Web uygulaması edinmek için Get-AzureRmWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="90b65-148">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>
<span data-ttu-id="90b65-149">*WebApp* parametresini, *resourcegroupname* parametresi ve/veya *webappname* ile aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="90b65-149">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="90b65-150">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="90b65-150">-WebAppName</span></span>
<span data-ttu-id="90b65-151">Yeni SSL bağlaması oluşturulan Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90b65-151">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="90b65-152">Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="90b65-152">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="90b65-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b65-153">CommonParameters</span></span>
<span data-ttu-id="90b65-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90b65-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b65-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b65-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b65-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90b65-156">INPUTS</span></span>

### <span data-ttu-id="90b65-157">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="90b65-157">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="90b65-158">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="90b65-158">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="90b65-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90b65-159">OUTPUTS</span></span>

### <span data-ttu-id="90b65-160">Microsoft. Azure. Management. Web sitesi. modeller. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="90b65-160">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="90b65-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90b65-161">NOTES</span></span>

## <span data-ttu-id="90b65-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90b65-162">RELATED LINKS</span></span>

[<span data-ttu-id="90b65-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="90b65-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="90b65-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="90b65-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="90b65-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="90b65-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="90b65-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="90b65-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


