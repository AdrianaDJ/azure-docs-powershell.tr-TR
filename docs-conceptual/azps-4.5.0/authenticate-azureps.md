---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.openlocfilehash: 7ac723202ca9e81c8ef4cba5e844d46b98ba4b67
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566639"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="e9020-103">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="e9020-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="e9020-104">Azure PowerShell, çeşitli kimlik doğrulama yöntemlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="e9020-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="e9020-105">Başlangıç yapmanın en kolay yolu, oturumunuzu otomatik olarak açan [Azure Cloud Shell](/azure/cloud-shell/overview)'i kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="e9020-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="e9020-106">Yerel yüklemeyle, tarayıcınızdan etkileşimli oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9020-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="e9020-107">Otomasyon betikleri yazarken önerilen yaklaşım, gerekli izinlere sahip bir [hizmet sorumlusu](create-azure-service-principal-azureps.md) kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="e9020-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="e9020-108">Kendi kullanım örneğinizde oturum açma izinlerini olabildiğince kısıtladığınızda, Azure kaynaklarınızın güvenliğini korumaya yardım etmiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="e9020-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="e9020-109">Birden fazla aboneliğe erişiminiz varsa başlangıçta Azure’ın ilk döndürdüğü abonelikte oturumunuz açılır.</span><span class="sxs-lookup"><span data-stu-id="e9020-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="e9020-110">Komutlar varsayılan olarak bu abonelikte çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="e9020-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="e9020-111">Bir oturumda etkin aboneliğinizi değiştirmek için [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e9020-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="e9020-112">Etkin aboneliğinizi değiştirmek ve aynı sistemde oturum değiştirdiğinizde bu değişikliğin geçerliliğini korumasını sağlamak için [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e9020-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9020-113">Oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="e9020-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="e9020-114">Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="e9020-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="e9020-115">Etkileşimli olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="e9020-115">Sign in interactively</span></span>

<span data-ttu-id="e9020-116">Etkileşimli olarak oturum açmak için [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e9020-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="e9020-117">Bu cmdlet PowerShell sürüm 6 veya üzerinde çalıştırıldığında bir belirteç dizesi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9020-117">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="e9020-118">Oturum açmak için bu dizeyi kopyalayıp bir web tarayıcısında [microsoft.com/devicelogin](https://microsoft.com/devicelogin) sayfasına yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="e9020-118">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="e9020-119">Azure’a bağlanmak için PowerShell oturumunuzun kimliği doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="e9020-119">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="e9020-120">Windows PowerShell’de belirteç dizesi almak için `UseDeviceAuthentication` parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9020-120">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9020-121">Active Directory yetkilendirme uygulamalarında yapılan değişiklikler ve güvenlik kaygıları nedeniyle, kullanıcı adı/parola kimlik bilgisi yetkilendirmesi Azure PowerShell’den kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="e9020-121">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="e9020-122">Kimlik bilgisi yetkilendirmesini otomasyon amacıyla kullanıyorsanız, bunun yerine [hizmet sorumlusu oluşturun](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e9020-122">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="e9020-123">Kiracı kimliğinizi bu makalenin sonraki iki bölümünde kullanılacak bir değişkende depolamak için [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e9020-123">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="e9020-124">Hizmet sorumlusu ile oturum açma <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="e9020-124">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="e9020-125">Hizmet sorumluları etkileşimli olmayan Azure hesaplarıdır.</span><span class="sxs-lookup"><span data-stu-id="e9020-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="e9020-126">Diğer kullanıcı hesapları gibi onların izinleri de Azure Active Directory ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="e9020-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="e9020-127">Otomasyon betikleriniz hizmet sorumlusuna yalnızca ihtiyacı olan izinleri vererek güvenliğini korur.</span><span class="sxs-lookup"><span data-stu-id="e9020-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="e9020-128">Azure PowerShell'le kullanmak üzere hizmet sorumlusu oluşturmayı öğrenmek için, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e9020-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="e9020-129">Hizmet sorumlusuyla oturum açmak için `Connect-AzAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e9020-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="e9020-130">Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="e9020-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="e9020-131">Hizmet sorumlusu ile nasıl oturum açacağınız, parola tabanlı veya sertifika tabanlı kimlik doğrulaması yöntemlerinden hangisini kullandığına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e9020-131">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="e9020-132">Parola tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="e9020-132">Password-based authentication</span></span>

<span data-ttu-id="e9020-133">Bu bölümdeki örneklerde kullanılmak üzere bir hizmet sorumlusu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e9020-133">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="e9020-134">Hizmet sorumluları oluşturma hakkında daha fazla bilgi için bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="e9020-134">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="e9020-135">Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e9020-135">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="e9020-136">Bu cmdlet bir kullanıcı adı ve parola için istem gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9020-136">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="e9020-137">Kullanıcı adı için hizmet sorumlusunun `applicationID` kimliğini kullanın ve parola için `secret` gizli dizisini düz metne dönüştürün.</span><span class="sxs-lookup"><span data-stu-id="e9020-137">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="e9020-138">Otomasyon senaryoları için, hizmet sorumlusunun `applicationId` kimliğinden ve `secret` gizli dizisinden kimlik bilgileri oluşturmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="e9020-138">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="e9020-139">Hizmet sorumlusu bağlantılarını otomatikleştirirken, iyi parola depolama yöntemlerini kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e9020-139">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="e9020-140">Sertifika tabanlı kimlik doğrulaması</span><span class="sxs-lookup"><span data-stu-id="e9020-140">Certificate-based authentication</span></span>

<span data-ttu-id="e9020-141">Sertifika tabanlı kimlik doğrulaması, Azure PowerShell’in sertifika parmak izini temel alarak bir yerel sertifika deposundan bilgi alabilir olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="e9020-141">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="e9020-142">Kayıtlı uygulama yerine hizmet sorumlusu kullanırken `-ServicePrincipal` bağımsız değişkenini ekleyin ve `-ApplicationId` parametresinin değeri olarak hizmet sorumlusunun Uygulama kimliğini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="e9020-142">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="e9020-143">PowerShell 5.1'de, sertifika deposu [PKI](/powershell/module/pkiclient) modülü ile yönetilebilir ve denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="e9020-143">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="e9020-144">PowerShell Core 6.x ve sonraki sürümleri için işlem daha karmaşıktır.</span><span class="sxs-lookup"><span data-stu-id="e9020-144">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="e9020-145">Aşağıdaki betikler, mevcut sertifikayı PowerShell tarafından erişilebilir sertifika deposuna nasıl aktarabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9020-145">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="e9020-146">PowerShell 5.1'de sertifikayı içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="e9020-146">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="e9020-147">PowerShell Core 6.x ve sonraki sürümlerinde sertifikayı içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="e9020-147">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="e9020-148">Yönetilen kimlik kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="e9020-148">Sign in using a managed identity</span></span>

<span data-ttu-id="e9020-149">Yönetilen kimlikler Azure Active Directory’nin bir özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="e9020-149">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="e9020-150">Yönetilen kimlikler, Azure'da çalıştırılan kaynaklara atanmış hizmet sorumlularıdır.</span><span class="sxs-lookup"><span data-stu-id="e9020-150">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="e9020-151">Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9020-151">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="e9020-152">Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan kaynaklarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e9020-152">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="e9020-153">Bu örnekte, barındırma ortamının yönetilen kimliği kullanılarak bağlanılır.</span><span class="sxs-lookup"><span data-stu-id="e9020-153">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="e9020-154">Örneğin, atanmış bir Yönetilen Hizmet Kimliğine sahip bir Sanal Makine üzerinde yürütülürse, kodun bu atanmış kimliği kullanarak oturum açmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e9020-154">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="e9020-155">Varsayılan olmayan bir kiracıyla veya Bulut Çözümü Sağlayıcısı (CSP) olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="e9020-155">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="e9020-156">Hesabınız birden fazla kiracıyla ilişkilendirildiyse bağlantı kurarken oturum açmak için `-Tenant` parametresinin belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e9020-156">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="e9020-157">Bu parametre tüm oturum açma yöntemleriyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="e9020-157">This parameter works with any sign-in method.</span></span> <span data-ttu-id="e9020-158">Oturum açılırken, bu parametre değeri kiracının Azure nesne kimliği (Kiracı Kimliği) veya kiracının tam etki alanı adı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e9020-158">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="e9020-159">[Bulut Çözümü Sağlayıcısıysanız (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), `-Tenant` değerin kiracı kimliği olması **gerekir**.</span><span class="sxs-lookup"><span data-stu-id="e9020-159">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="e9020-160">Başka bir bulut oturumu açma</span><span class="sxs-lookup"><span data-stu-id="e9020-160">Sign in to another Cloud</span></span>

<span data-ttu-id="e9020-161">Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasalara uygun ortamlar sunar.</span><span class="sxs-lookup"><span data-stu-id="e9020-161">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="e9020-162">Bölgesel buluttaki hesaplar için, oturum açarken `-Environment` bağımsız değişkeniyle ortamı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9020-162">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="e9020-163">Bu parametre tüm oturum açma yöntemleriyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="e9020-163">This parameter works with any sign-in method.</span></span> <span data-ttu-id="e9020-164">Örneğin, hesabınız Çin bulutundaysa:</span><span class="sxs-lookup"><span data-stu-id="e9020-164">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="e9020-165">Aşağıdaki komut, kullanılabilir ortamların listesini alır:</span><span class="sxs-lookup"><span data-stu-id="e9020-165">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
