---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: d3971c2838b3fed04e1aa38d96e2cd27b2e8276e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592843"
---
# <span data-ttu-id="a75bf-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a75bf-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="a75bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a75bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a75bf-103">Azure Web App için SSL sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a75bf-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a75bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a75bf-104">SYNTAX</span></span>

### <span data-ttu-id="a75bf-105">S1</span><span class="sxs-lookup"><span data-stu-id="a75bf-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a75bf-106">S2</span><span class="sxs-lookup"><span data-stu-id="a75bf-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a75bf-107">S3</span><span class="sxs-lookup"><span data-stu-id="a75bf-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a75bf-108">Modundan</span><span class="sxs-lookup"><span data-stu-id="a75bf-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a75bf-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a75bf-109">DESCRIPTION</span></span>
<span data-ttu-id="a75bf-110">**Yeni-AzureRmWebAppSSLBinding** cmdlet 'i, bir Azure Web App Için güvenli yuva KATMANı (SSL) sertifikası bağlaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a75bf-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="a75bf-111">Cmdlet iki yoldan bir SSL bağlaması oluşturur:</span><span class="sxs-lookup"><span data-stu-id="a75bf-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="a75bf-112">Web uygulamasını var olan bir sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a75bf-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="a75bf-113">Yeni bir sertifikayı karşıya yükleyebilir ve Web uygulamasını bu yeni sertifikaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a75bf-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="a75bf-114">Kullandığınız yaklaşımdan bağımsız olarak, sertifika ve Web uygulaması aynı Azure Resource grubuyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="a75bf-115">A kaynak grubunda bir Web uygulamanız varsa ve bu Web uygulamasını B kaynak grubundaki bir sertifikaya bağlamak istiyorsanız, bunu yapmanın tek yolu, sertifikanın bir kopyasını kaynak grubuna A yüklemek demektir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="a75bf-116">Yeni bir sertifikayı karşıya yüklediyseniz, bir Azure SSL sertifikası için aşağıdaki gereksinimleri aklınızda bulundurun:</span><span class="sxs-lookup"><span data-stu-id="a75bf-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="a75bf-117">Sertifikanın özel bir anahtar içermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="a75bf-118">Sertifikanın kişisel bilgi değişimi (PFX) biçimini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="a75bf-119">Sertifikanın konu adı, Web uygulamasına erişmek için kullanılan etki alanıyla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="a75bf-120">Sertifikanın en az 2048 bit şifreleme kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="a75bf-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a75bf-121">EXAMPLES</span></span>

### <span data-ttu-id="a75bf-122">Örnek 1: sertifikayı Web uygulamasına bağlama</span><span class="sxs-lookup"><span data-stu-id="a75bf-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="a75bf-123">Bu komut mevcut bir Azure sertifikasını (Parmak Izi E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 sertifika), ContosoWebApp adlı Web uygulamasına bağlar.</span><span class="sxs-lookup"><span data-stu-id="a75bf-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="a75bf-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a75bf-124">PARAMETERS</span></span>

### <span data-ttu-id="a75bf-125">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a75bf-125">-CertificateFilePath</span></span>
<span data-ttu-id="a75bf-126">Karşıya yüklenecek sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-126">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="a75bf-127">*Certificatefilepath* parametresi yalnızca sertifika henüz Azure 'a yüklenmediyse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-127">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-128">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a75bf-128">-CertificatePassword</span></span>
<span data-ttu-id="a75bf-129">Sertifikanın şifre çözme parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-129">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a75bf-130">-DefaultProfile</span></span>
<span data-ttu-id="a75bf-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a75bf-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="a75bf-132">-Name</span></span>
<span data-ttu-id="a75bf-133">Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-133">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a75bf-134">-ResourceGroupName</span></span>
<span data-ttu-id="a75bf-135">Sertifikanın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="a75bf-136">Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a75bf-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-137">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="a75bf-137">-Slot</span></span>
<span data-ttu-id="a75bf-138">Web uygulaması dağıtım yuvasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-138">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="a75bf-139">Yuva almak için Get-AzureRMWebAppSlot cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a75bf-139">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="a75bf-140">Dağıtım yuvaları, Internet üzerinden erişilebilir olması gerekmeden Web uygulamalarını, Web uygulamalarını aşamalandırmanızın ve doğrulayamanızın bir yolunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="a75bf-140">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="a75bf-141">Genellikle değişikliklerinizi bir basamaklandırma sitesine dağıtırsınız, bu değişiklikleri doğrulayabilir ve ardından üretime (Internet erişimi erişilebilir) dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a75bf-141">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-142">-SslState</span><span class="sxs-lookup"><span data-stu-id="a75bf-142">-SslState</span></span>
<span data-ttu-id="a75bf-143">Sertifikanın etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-143">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="a75bf-144">Sertifikayı etkinleştirmek için *SslState* parametresini 1 olarak ayarlayın veya sertifikayı devre dışı bırakmak Için *SslState* 'i 0 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a75bf-144">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-145">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="a75bf-145">-Thumbprint</span></span>
<span data-ttu-id="a75bf-146">Sertifikanın benzersiz tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-146">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a75bf-147">-WebApp</span></span>
<span data-ttu-id="a75bf-148">Web uygulaması belirtir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-148">Specifies a Web App.</span></span>
<span data-ttu-id="a75bf-149">Web uygulaması edinmek için Get-AzureRmWebApp cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a75bf-149">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="a75bf-150">*WebApp* parametresini, *resourcegroupname* parametresi ve/veya *webappname* ile aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a75bf-150">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-151">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a75bf-151">-WebAppName</span></span>
<span data-ttu-id="a75bf-152">Yeni SSL bağlaması oluşturulan Web uygulamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a75bf-152">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="a75bf-153">Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a75bf-153">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75bf-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75bf-154">CommonParameters</span></span>
<span data-ttu-id="a75bf-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a75bf-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75bf-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a75bf-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75bf-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a75bf-157">INPUTS</span></span>

### <span data-ttu-id="a75bf-158">Bölge</span><span class="sxs-lookup"><span data-stu-id="a75bf-158">Site</span></span>
<span data-ttu-id="a75bf-159">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a75bf-159">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a75bf-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a75bf-160">OUTPUTS</span></span>

## <span data-ttu-id="a75bf-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a75bf-161">NOTES</span></span>

## <span data-ttu-id="a75bf-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a75bf-162">RELATED LINKS</span></span>

[<span data-ttu-id="a75bf-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a75bf-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="a75bf-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a75bf-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="a75bf-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a75bf-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="a75bf-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a75bf-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

