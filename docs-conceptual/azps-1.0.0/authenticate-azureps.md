---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: b5635e291cdc324e66c936aa16c5772507fc78e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/04/2019
ms.locfileid: "54055685"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="22d5c-103">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="22d5c-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="22d5c-104">Azure PowerShell, çeşitli kimlik doğrulama yöntemlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="22d5c-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="22d5c-105">Başlangıç yapmanın en kolay yolu, oturumunuzu otomatik olarak açan [Azure Cloud Shell](/azure/cloud-shell/overview)'i kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="22d5c-106">Yerel yüklemeyle, tarayıcınızdan etkileşimli oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22d5c-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="22d5c-107">Otomasyon betikleri yazarken önerilen yaklaşım, gerekli izinlere sahip bir [hizmet sorumlusu](create-azure-service-principal-azureps.md) kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="22d5c-108">Kendi kullanım örneğinizde oturum açma izinlerini olabildiğince kısıtladığınızda, Azure kaynaklarınızın güvenliğini korumaya yardım etmiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="22d5c-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="22d5c-109">Oturum açtıktan sonra, komutlar varsayılan aboneliğinizde çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="22d5c-110">Bir oturumda etkin aboneliğinizi değiştirmek için [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="22d5c-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="22d5c-111">Azure PowerShell'de oturum açarken kullanılan varsayılan aboneliği değiştirmek için [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) kullanın.</span><span class="sxs-lookup"><span data-stu-id="22d5c-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="22d5c-112">Oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="22d5c-113">Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="22d5c-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="22d5c-114">Etkileşimli olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="22d5c-114">Sign in interactively</span></span>

<span data-ttu-id="22d5c-115">Etkileşimli olarak oturum açmak için [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="22d5c-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="22d5c-116">Bu cmdlet çalıştırıldığında bir belirteç dizesi sunar.</span><span class="sxs-lookup"><span data-stu-id="22d5c-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="22d5c-117">Oturum açmak için bu dizeyi kopyalayıp bir tarayıcıda https://microsoft.com/devicelogin sayfasına yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="22d5c-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="22d5c-118">Azure’a bağlanmak için PowerShell oturumunuzun kimliği doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

## <a name="sign-in-with-credentials"></a><span data-ttu-id="22d5c-119">Kimlik bilgileriyle oturum açma</span><span class="sxs-lookup"><span data-stu-id="22d5c-119">Sign in with credentials</span></span>

<span data-ttu-id="22d5c-120">Ayrıca Azure'a bağlanmak için yetkilendirilmiş bir `PSCredential` nesnesiyle de oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22d5c-120">You can also sign in with a `PSCredential` object authorized to connect to Azure.</span></span>
<span data-ttu-id="22d5c-121">Kimlik bilgileri nesnesini almanın en kolay yolu [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet'ini kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-121">The easiest way to get a credential object is with the [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet.</span></span> <span data-ttu-id="22d5c-122">Bu cmdlet çalıştırıldığında, sizden kullanıcı adı/parola bilgileri çiftini ister.</span><span class="sxs-lookup"><span data-stu-id="22d5c-122">When run, this cmdlet will prompt you for a username/password credential pair.</span></span>

> [!Note]
> <span data-ttu-id="22d5c-123">Bu yaklaşım Microsoft hesaplarıyla veya iki faktörlü kimlik doğrulamasını etkinleştirdiğiniz hesaplarla kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="22d5c-123">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="22d5c-124">Hizmet sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="22d5c-124">Sign in with a service principal</span></span>

<span data-ttu-id="22d5c-125">Hizmet sorumluları etkileşimli olmayan Azure hesaplarıdır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="22d5c-126">Diğer kullanıcı hesapları gibi onların izinleri de Azure Active Directory ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="22d5c-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="22d5c-127">Otomasyon betikleriniz hizmet sorumlusuna yalnızca ihtiyacı olan izinleri vererek güvenliğini korur.</span><span class="sxs-lookup"><span data-stu-id="22d5c-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="22d5c-128">Azure PowerShell'le kullanmak üzere hizmet sorumlusu oluşturmayı öğrenmek için, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="22d5c-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="22d5c-129">Hizmet sorumlusuyla oturum açmak için `Connect-AzAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın.</span><span class="sxs-lookup"><span data-stu-id="22d5c-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="22d5c-130">Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="22d5c-131">Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="22d5c-131">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="22d5c-132">Bu cmdlet, hizmet sorumlusu kullanıcı kimliği ve parolası için bir istem sunar.</span><span class="sxs-lookup"><span data-stu-id="22d5c-132">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="22d5c-133">Yönetilen kimlik kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="22d5c-133">Sign in using a managed identity</span></span> 

<span data-ttu-id="22d5c-134">Yönetilen kimlikler Azure Active Directory’nin bir özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="22d5c-134">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="22d5c-135">Yönetilen kimlikler, Azure'da çalıştırılan kaynaklara atanmış hizmet sorumlularıdır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-135">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="22d5c-136">Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22d5c-136">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="22d5c-137">Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan kaynaklarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="22d5c-137">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="22d5c-138">Azure kaynaklarına ilişkin yönetilen kimlikler hakkında daha fazla bilgi edinmek için bkz. [Erişim belirteci almak için Azure VM'de Azure kaynaklarına ilişkin yönetilen kimlikleri kullanma](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="22d5c-138">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="22d5c-139">Varsayılan olmayan bir kiracıyla veya Bulut Çözümü Sağlayıcısı (CSP) olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="22d5c-139">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="22d5c-140">Hesabınız birden fazla kiracıyla ilişkilendirildiyse, bağlantı kurarken oturum açmak için `-TenantId` parametresinin kullanılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="22d5c-140">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="22d5c-141">Bu parametre, diğer tüm oturum açma yöntemiyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="22d5c-141">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="22d5c-142">Oturum açılırken, bu parametre değeri kiracının Azure nesne kimliği (Kiracı Kimliği) veya kiracının tam etki alanı adı olabilir.</span><span class="sxs-lookup"><span data-stu-id="22d5c-142">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="22d5c-143">[Bulut Çözümü Sağlayıcısıysanız (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), `-TenantId` değerin kiracı kimliği olması **gerekir**.</span><span class="sxs-lookup"><span data-stu-id="22d5c-143">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="22d5c-144">Başka bir bulut oturumu açma</span><span class="sxs-lookup"><span data-stu-id="22d5c-144">Sign in to another Cloud</span></span>

<span data-ttu-id="22d5c-145">Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasalara uygun ortamlar sunar.</span><span class="sxs-lookup"><span data-stu-id="22d5c-145">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="22d5c-146">Bölgesel buluttaki hesaplar için, oturum açarken `-Environment` bağımsız değişkeniyle ortamı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="22d5c-146">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="22d5c-147">Örneğin, hesabınız Çin bulutundaysa:</span><span class="sxs-lookup"><span data-stu-id="22d5c-147">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="22d5c-148">Aşağıdaki komut, kullanılabilir ortamların listesini alır:</span><span class="sxs-lookup"><span data-stu-id="22d5c-148">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```