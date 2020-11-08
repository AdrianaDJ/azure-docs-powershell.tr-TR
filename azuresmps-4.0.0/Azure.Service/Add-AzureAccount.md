---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106396"
---
# <span data-ttu-id="e2995-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="e2995-101">Add-AzureAccount</span></span>

## <span data-ttu-id="e2995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2995-102">SYNOPSIS</span></span>
<span data-ttu-id="e2995-103">Azure hesabını Windows PowerShell 'e ekler.</span><span class="sxs-lookup"><span data-stu-id="e2995-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="e2995-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2995-104">SYNTAX</span></span>

### <span data-ttu-id="e2995-105">Kullanıcı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2995-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e2995-106">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e2995-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2995-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2995-107">DESCRIPTION</span></span>
<span data-ttu-id="e2995-108">**Add-AzureAccount** cmdlet 'ı, Azure hesabınızın ve aboneliklerinizin Windows PowerShell 'de kullanılabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="e2995-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="e2995-109">Windows PowerShell 'de Azure hesabınızda oturum açmak gibidir.</span><span class="sxs-lookup"><span data-stu-id="e2995-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="e2995-110">Hesabı oturumu açmak için **Remove-AzureAccount** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e2995-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="e2995-111">**Add-AzureAccount** , Azure hesabınızla ilgili bilgileri indirir ve gezici kullanıcı profilinizde bir abonelik verileri dosyasına kaydeder.</span><span class="sxs-lookup"><span data-stu-id="e2995-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="e2995-112">Ayrıca, Windows PowerShell 'in sizin adınıza Azure hesabınıza erişmesini sağlayan bir erişim simgesi de alır.</span><span class="sxs-lookup"><span data-stu-id="e2995-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="e2995-113">Komut tamamlandığında, Azure hesabınızı Windows PowerShell 'de yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2995-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="e2995-114">Azure hesabınızı Windows PowerShell 'in kullanımına sunmak için iki farklı yol vardır.</span><span class="sxs-lookup"><span data-stu-id="e2995-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="e2995-115">Bir yönetim sertifikası kullanan Azure Active Directory (Azure AD) kimlik doğrulama erişim belirteçlerini veya **Içeri aktarma-Azuikinci ad ayarları dosyasını** kullanan **Add-AzureAccount** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2995-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="e2995-116">Hangi yöntemin kullanılacağı konusunda rehberlik için, [nasıl yapılır: aboneliğinize nasıl bağlanabilirim](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .</span><span class="sxs-lookup"><span data-stu-id="e2995-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="e2995-117">**Add-AzureAccount** ' i çalıştırdığınızda, Azure hesabınızda oturum açmanızı isteyen etkileşimli bir pencere görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e2995-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="e2995-118">Bu oturum açma işlemi, erişim belirtecinin süresi dolana kadar geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="e2995-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="e2995-119">Süresi dolduğunda, hesabınıza erişmesi gereken cmdlet 'ler **AzureAccount** 'i yeniden çalıştırmanız istenir.</span><span class="sxs-lookup"><span data-stu-id="e2995-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="e2995-120">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e2995-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e2995-121">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e2995-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="e2995-122">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2995-122">EXAMPLES</span></span>

### <span data-ttu-id="e2995-123">Örnek 1: hesap ekleme</span><span class="sxs-lookup"><span data-stu-id="e2995-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="e2995-124">Bu komut Windows PowerShell 'e bir Azure hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="e2995-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="e2995-125">Komutu çalıştırdığınızda, hesabın kullanıcı adını ve parolasını istemek için Windows açılır.</span><span class="sxs-lookup"><span data-stu-id="e2995-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="e2995-126">Örnek 2: alternatif bir abonelik veri dosyası kullanın</span><span class="sxs-lookup"><span data-stu-id="e2995-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="e2995-127">Bu komut, **AzureAccount doğrudan Add-** ' **u, varsayılan** dosya yerine C:\Testing\SDF.xml dosyasındaki hesap verilerini depolamak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="e2995-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="e2995-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2995-128">PARAMETERS</span></span>

### <span data-ttu-id="e2995-129">-Credential</span><span class="sxs-lookup"><span data-stu-id="e2995-129">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2995-130">-Ortam</span><span class="sxs-lookup"><span data-stu-id="e2995-130">-Environment</span></span>
<span data-ttu-id="e2995-131">Bir Azure ortamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2995-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="e2995-132">Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="e2995-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="e2995-133">Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2995-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="e2995-134">Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e2995-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="e2995-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2995-135">-Profile</span></span>
<span data-ttu-id="e2995-136">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2995-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e2995-137">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e2995-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2995-138">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e2995-138">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2995-139">-Tenant</span><span class="sxs-lookup"><span data-stu-id="e2995-139">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2995-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2995-140">CommonParameters</span></span>
<span data-ttu-id="e2995-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2995-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2995-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2995-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2995-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2995-143">INPUTS</span></span>

### <span data-ttu-id="e2995-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e2995-144">None</span></span>
<span data-ttu-id="e2995-145">Bu cmdlet 'e giriş kanalı oluşturamazsınız</span><span class="sxs-lookup"><span data-stu-id="e2995-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="e2995-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2995-146">OUTPUTS</span></span>

### <span data-ttu-id="e2995-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e2995-147">None</span></span>
<span data-ttu-id="e2995-148">Bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="e2995-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="e2995-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2995-149">NOTES</span></span>
* <span data-ttu-id="e2995-150">**Add-AzureAccount** (ve Azure AD doğrulama yöntemi) **Import-azuikinci** site (ve yönetim sertifikası yöntemi) ile önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="e2995-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="e2995-151">Hesabınızda **AzureAccount eklentisini** bir kez kullanıyorsanız, Azure AD doğrulama yöntemi kullanılır ve yönetim sertifikası yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="e2995-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="e2995-152">Azure AD belirtecini kaldırmak ve yönetim sertifikası yöntemini geri yüklemek için **Remove-AzureAccount** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e2995-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="e2995-153">Daha fazla bilgi için şunu yazın: **Get-Help Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="e2995-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="e2995-154">"Kimlik bilgilerinizin süresi doldu.</span><span class="sxs-lookup"><span data-stu-id="e2995-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="e2995-155">Lütfen tekrar oturum açmak için Add-AzureAccount kullanın. "</span><span class="sxs-lookup"><span data-stu-id="e2995-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="e2995-156">erişim belirtecinizin süresinin dolduğunu ve Windows PowerShell 'in Azure hesabınıza erişemediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2995-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="e2995-157">Hesabınıza erişimi geri yüklemek için **Add-AzureAccount** ' i yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="e2995-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="e2995-158">Azure PowerShell hesabı ve abonelik cmdlet 'leri, verileri Live Azure hesabından değil, abonelik verileri dosyasından alırlar.</span><span class="sxs-lookup"><span data-stu-id="e2995-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="e2995-159">Windows PowerShell dışında, örneğin Azure yönetim portalı 'nı kullanarak hesabınızı veya aboneliklerinizi değiştirirseniz, abonelik verileri dosyasını yenilemek için **Add-AzureAccount** ' i yeniden çalıştırarak.</span><span class="sxs-lookup"><span data-stu-id="e2995-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="e2995-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2995-160">RELATED LINKS</span></span>

[<span data-ttu-id="e2995-161">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e2995-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="e2995-162">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e2995-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="e2995-163">Import-Azuyeniden yayımlayan ayarları dosyası</span><span class="sxs-lookup"><span data-stu-id="e2995-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="e2995-164">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="e2995-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="e2995-165">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="e2995-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


