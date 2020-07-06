---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/18/2020
ms.openlocfilehash: f82a9e373806f2f071ae59f6aee7e0a0bd4ea13d
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85268394"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="087a6-103">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="087a6-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="087a6-104">Azure PowerShell, çeşitli kimlik doğrulama yöntemlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="087a6-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="087a6-105">Başlangıç yapmanın en kolay yolu, oturumunuzu otomatik olarak açan [Azure Cloud Shell](/azure/cloud-shell/overview)'i kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="087a6-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="087a6-106">Yerel yüklemeyle, tarayıcınızdan etkileşimli oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="087a6-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="087a6-107">Otomasyon betikleri yazarken önerilen yaklaşım, gerekli izinlere sahip bir [hizmet sorumlusu](create-azure-service-principal-azureps.md) kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="087a6-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="087a6-108">Kendi kullanım örneğinizde oturum açma izinlerini olabildiğince kısıtladığınızda, Azure kaynaklarınızın güvenliğini korumaya yardım etmiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="087a6-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="087a6-109">Oturum açtıktan sonra, komutlar varsayılan aboneliğinizde çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="087a6-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="087a6-110">Bir oturumda etkin aboneliğinizi değiştirmek için [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="087a6-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="087a6-111">Azure PowerShell'de oturum açarken kullanılan varsayılan aboneliği değiştirmek için [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) kullanın.</span><span class="sxs-lookup"><span data-stu-id="087a6-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="087a6-112">Oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="087a6-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="087a6-113">Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="087a6-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="087a6-114">Etkileşimli olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="087a6-114">Sign in interactively</span></span>

<span data-ttu-id="087a6-115">Etkileşimli olarak oturum açmak için [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="087a6-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="087a6-116">Bu cmdlet PowerShell sürüm 6 veya üzerinde çalıştırıldığında bir belirteç dizesi gösterir.</span><span class="sxs-lookup"><span data-stu-id="087a6-116">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="087a6-117">Oturum açmak için bu dizeyi kopyalayıp bir web tarayıcısında [microsoft.com/devicelogin](https://microsoft.com/devicelogin) sayfasına yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="087a6-117">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="087a6-118">Azure’a bağlanmak için PowerShell oturumunuzun kimliği doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="087a6-118">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="087a6-119">Windows PowerShell’de belirteç dizesi almak için `UseDeviceAuthentication` parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="087a6-119">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="087a6-120">Active Directory yetkilendirme uygulamalarında yapılan değişiklikler ve güvenlik kaygıları nedeniyle, kullanıcı adı/parola kimlik bilgisi yetkilendirmesi Azure PowerShell’den kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="087a6-120">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="087a6-121">Kimlik bilgisi yetkilendirmesini otomasyon amacıyla kullanıyorsanız, bunun yerine [hizmet sorumlusu oluşturun](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="087a6-121">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="087a6-122">Kiracı kimliğinizi bu makalenin sonraki iki bölümünde kullanılacak bir değişkende depolamak için [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="087a6-122">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="087a6-123">Hizmet sorumlusu ile oturum açma <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="087a6-123">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="087a6-124">Hizmet sorumluları etkileşimli olmayan Azure hesaplarıdır.</span><span class="sxs-lookup"><span data-stu-id="087a6-124">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="087a6-125">Diğer kullanıcı hesapları gibi onların izinleri de Azure Active Directory ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="087a6-125">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="087a6-126">Otomasyon betikleriniz hizmet sorumlusuna yalnızca ihtiyacı olan izinleri vererek güvenliğini korur.</span><span class="sxs-lookup"><span data-stu-id="087a6-126">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="087a6-127">Azure PowerShell'le kullanmak üzere hizmet sorumlusu oluşturmayı öğrenmek için, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="087a6-127">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="087a6-128">Hizmet sorumlusuyla oturum açmak için `Connect-AzAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın.</span><span class="sxs-lookup"><span data-stu-id="087a6-128">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="087a6-129">Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="087a6-129">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="087a6-130">Hizmet sorumlusu ile nasıl oturum açacağınız, parola tabanlı veya sertifika tabanlı kimlik doğrulaması yöntemlerinden hangisini kullandığına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="087a6-130">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="087a6-131">Parola tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="087a6-131">Password-based authentication</span></span>

<span data-ttu-id="087a6-132">Bu bölümdeki örneklerde kullanılmak üzere bir hizmet sorumlusu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="087a6-132">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="087a6-133">Hizmet sorumluları oluşturma hakkında daha fazla bilgi için bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="087a6-133">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="087a6-134">Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="087a6-134">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="087a6-135">Bu cmdlet bir kullanıcı adı ve parola için istem gösterir.</span><span class="sxs-lookup"><span data-stu-id="087a6-135">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="087a6-136">Kullanıcı adı için hizmet sorumlusunun `applicationID` kimliğini kullanın ve parola için `secret` gizli dizisini düz metne dönüştürün.</span><span class="sxs-lookup"><span data-stu-id="087a6-136">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="087a6-137">Otomasyon senaryoları için, hizmet sorumlusunun `applicationId` kimliğinden ve `secret` gizli dizisinden kimlik bilgileri oluşturmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="087a6-137">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="087a6-138">Hizmet sorumlusu bağlantılarını otomatikleştirirken, iyi parola depolama yöntemlerini kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="087a6-138">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="087a6-139">Sertifika tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="087a6-139">Certificate-based authentication</span></span>

<span data-ttu-id="087a6-140">Sertifika tabanlı kimlik doğrulaması, Azure PowerShell’in sertifika parmak izini temel alarak bir yerel sertifika deposundan bilgi alabilir olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="087a6-140">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="087a6-141">Kayıtlı uygulama yerine hizmet sorumlusu kullanırken `-ServicePrincipal` bağımsız değişkenini ekleyin ve `-ApplicationId` parametresinin değeri olarak hizmet sorumlusunun Uygulama kimliğini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="087a6-141">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="087a6-142">PowerShell 5.1'de, sertifika deposu [PKI](/powershell/module/pkiclient) modülü ile yönetilebilir ve denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="087a6-142">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="087a6-143">PowerShell Core 6.x ve sonraki sürümleri için işlem daha karmaşıktır.</span><span class="sxs-lookup"><span data-stu-id="087a6-143">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="087a6-144">Aşağıdaki betikler, mevcut sertifikayı PowerShell tarafından erişilebilir sertifika deposuna nasıl aktarabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="087a6-144">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="087a6-145">PowerShell 5.1'de sertifikayı içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="087a6-145">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="087a6-146">PowerShell Core 6.x ve sonraki sürümlerinde sertifikayı içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="087a6-146">Import a certificate in PowerShell Core 6.x and later</span></span>

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation)
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag)
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite)
$store.Add($Certificate)
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="087a6-147">Yönetilen kimlik kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="087a6-147">Sign in using a managed identity</span></span>

<span data-ttu-id="087a6-148">Yönetilen kimlikler Azure Active Directory’nin bir özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="087a6-148">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="087a6-149">Yönetilen kimlikler, Azure'da çalıştırılan kaynaklara atanmış hizmet sorumlularıdır.</span><span class="sxs-lookup"><span data-stu-id="087a6-149">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="087a6-150">Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="087a6-150">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="087a6-151">Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan kaynaklarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="087a6-151">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="087a6-152">Bu örnekte, barındırma ortamının yönetilen kimliği kullanılarak bağlanılır.</span><span class="sxs-lookup"><span data-stu-id="087a6-152">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="087a6-153">Örneğin, atanmış bir Yönetilen Hizmet Kimliğine sahip bir Sanal Makine üzerinde yürütülürse, kodun bu atanmış kimliği kullanarak oturum açmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="087a6-153">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="087a6-154">Varsayılan olmayan bir kiracıyla veya Bulut Çözümü Sağlayıcısı (CSP) olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="087a6-154">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="087a6-155">Hesabınız birden fazla kiracıyla ilişkilendirildiyse bağlantı kurarken oturum açmak için `-Tenant` parametresinin belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="087a6-155">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="087a6-156">Bu parametre tüm oturum açma yöntemleriyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="087a6-156">This parameter works with any sign-in method.</span></span> <span data-ttu-id="087a6-157">Oturum açılırken, bu parametre değeri kiracının Azure nesne kimliği (Kiracı Kimliği) veya kiracının tam etki alanı adı olabilir.</span><span class="sxs-lookup"><span data-stu-id="087a6-157">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="087a6-158">[Bulut Çözümü Sağlayıcısıysanız (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), `-Tenant` değerin kiracı kimliği olması **gerekir**.</span><span class="sxs-lookup"><span data-stu-id="087a6-158">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="087a6-159">Başka bir bulut oturumu açma</span><span class="sxs-lookup"><span data-stu-id="087a6-159">Sign in to another Cloud</span></span>

<span data-ttu-id="087a6-160">Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasalara uygun ortamlar sunar.</span><span class="sxs-lookup"><span data-stu-id="087a6-160">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="087a6-161">Bölgesel buluttaki hesaplar için, oturum açarken `-Environment` bağımsız değişkeniyle ortamı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="087a6-161">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="087a6-162">Bu parametre tüm oturum açma yöntemleriyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="087a6-162">This parameter works with any sign-in method.</span></span> <span data-ttu-id="087a6-163">Örneğin, hesabınız Çin bulutundaysa:</span><span class="sxs-lookup"><span data-stu-id="087a6-163">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="087a6-164">Aşağıdaki komut, kullanılabilir ortamların listesini alır:</span><span class="sxs-lookup"><span data-stu-id="087a6-164">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
