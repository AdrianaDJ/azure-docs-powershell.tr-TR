---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 897bc20721305c03a0545bc236fa91292861ef1e
ms.sourcegitcommit: 18de3041f9084f60424ccbd1d004da761277a304
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57016478"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="b0e7d-103">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="b0e7d-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="b0e7d-104">Azure PowerShell, çeşitli kimlik doğrulama yöntemlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="b0e7d-105">Başlangıç yapmanın en kolay yolu, oturumunuzu otomatik olarak açan [Azure Cloud Shell](/azure/cloud-shell/overview)'i kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="b0e7d-106">Yerel yüklemeyle, tarayıcınızdan etkileşimli oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="b0e7d-107">Otomasyon betikleri yazarken önerilen yaklaşım, gerekli izinlere sahip bir [hizmet sorumlusu](create-azure-service-principal-azureps.md) kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="b0e7d-108">Kendi kullanım örneğinizde oturum açma izinlerini olabildiğince kısıtladığınızda, Azure kaynaklarınızın güvenliğini korumaya yardım etmiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="b0e7d-109">Oturum açtıktan sonra, komutlar varsayılan aboneliğinizde çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="b0e7d-110">Bir oturumda etkin aboneliğinizi değiştirmek için [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="b0e7d-111">Azure PowerShell'de oturum açarken kullanılan varsayılan aboneliği değiştirmek için [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="b0e7d-112">Oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="b0e7d-113">Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="b0e7d-114">Etkileşimli olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="b0e7d-114">Sign in interactively</span></span>

<span data-ttu-id="b0e7d-115">Etkileşimli olarak oturum açmak için [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="b0e7d-116">Bu cmdlet çalıştırıldığında bir belirteç dizesi sunar.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="b0e7d-117">Oturum açmak için bu dizeyi kopyalayıp bir tarayıcıda https://microsoft.com/devicelogin sayfasına yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="b0e7d-118">Azure’a bağlanmak için PowerShell oturumunuzun kimliği doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="b0e7d-119">Active Directory yetkilendirme uygulamalarında yapılan değişiklikler ve güvenlik kaygıları nedeniyle, kullanıcı adı/parola kimlik bilgisi yetkilendirmesi Azure PowerShell’den kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="b0e7d-120">Kimlik bilgisi yetkilendirmesini otomasyon amacıyla kullanıyorsanız, bunun yerine [hizmet sorumlusu oluşturun](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="b0e7d-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="b0e7d-121">Hizmet sorumlusu ile oturum açma <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="b0e7d-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="b0e7d-122">Hizmet sorumluları etkileşimli olmayan Azure hesaplarıdır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="b0e7d-123">Diğer kullanıcı hesapları gibi onların izinleri de Azure Active Directory ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="b0e7d-124">Otomasyon betikleriniz hizmet sorumlusuna yalnızca ihtiyacı olan izinleri vererek güvenliğini korur.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="b0e7d-125">Azure PowerShell'le kullanmak üzere hizmet sorumlusu oluşturmayı öğrenmek için, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="b0e7d-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="b0e7d-126">Hizmet sorumlusuyla oturum açmak için `Connect-AzAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="b0e7d-127">Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="b0e7d-128">Hizmet sorumlusu ile nasıl oturum açacağınız, parola tabanlı veya sertifika tabanlı kimlik doğrulaması yöntemlerinden hangisini kullandığına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="b0e7d-129">Parola tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="b0e7d-129">Password-based authentication</span></span>

<span data-ttu-id="b0e7d-130">Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="b0e7d-131">Bu cmdlet, bir kullanıcı adı ve parola için istem sunacaktır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="b0e7d-132">Kullanıcı adı olarak hizmet sorumlusu kimliğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="b0e7d-133">Otomasyon senaryoları için, bir kullanıcı adı ve güvenli dizeden kimlik bilgileri oluşturmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="b0e7d-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="b0e7d-134">Hizmet sorumlusu bağlantılarını otomatikleştirirken, iyi parola depolama yöntemlerini kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="b0e7d-135">Sertifika tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="b0e7d-135">Certificate-based authentication</span></span>

<span data-ttu-id="b0e7d-136">Sertifika tabanlı kimlik doğrulaması, Azure PowerShell’in sertifika parmak izini temel alarak bir yerel sertifika deposundan bilgi alabilir olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>
```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="b0e7d-137">PowerShell 5'te, sertifika deposu [PKI](/powershell/module/pkiclient) modülü ile yönetilebilir ve denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-137">In PowerShell 5, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="b0e7d-138">PowerShell 6 için işlem daha karmaşıktır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-138">For PowerShell 6, the process is more complicated.</span></span> <span data-ttu-id="b0e7d-139">Aşağıdaki betikler, mevcut sertifikayı PowerShell tarafından erişilebilir sertifika deposuna nasıl aktarabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-139">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-5"></a><span data-ttu-id="b0e7d-140">PowerShell 5'te sertifikayı içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="b0e7d-140">Import a certificate in PowerShell 5</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-6"></a><span data-ttu-id="b0e7d-141">PowerShell 6’da sertifikayı içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="b0e7d-141">Import a certificate in PowerShell 6</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="b0e7d-142">Yönetilen kimlik kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="b0e7d-142">Sign in using a managed identity</span></span> 

<span data-ttu-id="b0e7d-143">Yönetilen kimlikler Azure Active Directory’nin bir özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-143">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="b0e7d-144">Yönetilen kimlikler, Azure'da çalıştırılan kaynaklara atanmış hizmet sorumlularıdır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-144">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="b0e7d-145">Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-145">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="b0e7d-146">Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan kaynaklarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-146">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="b0e7d-147">Azure kaynaklarına ilişkin yönetilen kimlikler hakkında daha fazla bilgi edinmek için bkz. [Erişim belirteci almak için Azure VM'de Azure kaynaklarına ilişkin yönetilen kimlikleri kullanma](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="b0e7d-147">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="b0e7d-148">Varsayılan olmayan bir kiracıyla veya Bulut Çözümü Sağlayıcısı (CSP) olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="b0e7d-148">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="b0e7d-149">Hesabınız birden fazla kiracıyla ilişkilendirildiyse, bağlantı kurarken oturum açmak için `-TenantId` parametresinin kullanılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-149">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="b0e7d-150">Bu parametre, diğer tüm oturum açma yöntemiyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-150">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="b0e7d-151">Oturum açılırken, bu parametre değeri kiracının Azure nesne kimliği (Kiracı Kimliği) veya kiracının tam etki alanı adı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-151">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="b0e7d-152">[Bulut Çözümü Sağlayıcısıysanız (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), `-TenantId` değerin kiracı kimliği olması **gerekir**.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-152">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="b0e7d-153">Başka bir bulut oturumu açma</span><span class="sxs-lookup"><span data-stu-id="b0e7d-153">Sign in to another Cloud</span></span>

<span data-ttu-id="b0e7d-154">Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasalara uygun ortamlar sunar.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-154">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="b0e7d-155">Bölgesel buluttaki hesaplar için, oturum açarken `-Environment` bağımsız değişkeniyle ortamı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b0e7d-155">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="b0e7d-156">Örneğin, hesabınız Çin bulutundaysa:</span><span class="sxs-lookup"><span data-stu-id="b0e7d-156">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="b0e7d-157">Aşağıdaki komut, kullanılabilir ortamların listesini alır:</span><span class="sxs-lookup"><span data-stu-id="b0e7d-157">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
