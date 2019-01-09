---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786688"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="4d1cc-103">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="4d1cc-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="4d1cc-104">Azure PowerShell, çeşitli kimlik doğrulama yöntemlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="4d1cc-105">Hizmeti kullanmaya başlamanın en basit yolu, komut satırından etkileşimli olarak oturum açmaktır.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="4d1cc-106">Etkileşimli olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="4d1cc-106">Sign in interactively</span></span>

<span data-ttu-id="4d1cc-107">Etkileşimli olarak oturum açmak için [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-107">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="4d1cc-108">Bu cmdlet çalıştırıldığında bir belirteç dizesi sunar.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-108">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="4d1cc-109">Oturum açmak için bu dizeyi kopyalayıp bir tarayıcıda https://microsoft.com/devicelogin sayfasına yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-109">To log in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="4d1cc-110">Ardından Azure’a bağlanmak için PowerShell oturumunuzun kimliği doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-110">Your PowerShell session will then be authenticated to connect to Azure.</span></span> <span data-ttu-id="4d1cc-111">Bu kimlik doğrulaması geçerli PowerShell oturumunu süresince kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-111">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="4d1cc-112">Oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="4d1cc-113">Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="4d1cc-114">Hizmet sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="4d1cc-114">Sign in with a service principal</span></span>

<span data-ttu-id="4d1cc-115">Hizmet sorumluları etkileşimli olmayan Azure hesaplarıdır.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-115">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="4d1cc-116">Diğer kullanıcı hesapları gibi onların izinleri de Azure Active Directory ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-116">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="4d1cc-117">Otomasyon betikleriniz hizmet sorumlusuna yalnızca ihtiyacı olan izinleri vererek güvenliğini korur.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-117">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="4d1cc-118">Azure PowerShell'le kullanmak üzere hizmet sorumlusu oluşturmayı öğrenmek için, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="4d1cc-118">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="4d1cc-119">Hizmet sorumlusuyla oturum açmak için `Connect-AzAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-119">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="4d1cc-120">Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-120">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="4d1cc-121">Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-121">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="4d1cc-122">Bu cmdlet, hizmet sorumlusu kullanıcı kimliği ve parolası için bir istem sunar.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-122">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="4d1cc-123">Azure Yönetilen Hizmet Kimliği kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="4d1cc-123">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="4d1cc-124">Azure kaynakları için yönetilen kimlikler bir Azure Active Directory özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-124">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="4d1cc-125">Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-125">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="4d1cc-126">Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan sanal makinelerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-126">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="4d1cc-127">Azure kaynaklarına ilişkin yönetilen kimlikler hakkında daha fazla bilgi için bkz. [Erişim belirteci almak için Azure VM'de Azure kaynaklarına ilişkin yönetilen kimlikleri kullanma](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="4d1cc-127">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="4d1cc-128">Bulut Çözümü Sağlayıcısı (CSP) olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="4d1cc-128">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="4d1cc-129">[Bulut Çözümü Sağlayıcısı (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) olarak oturum açmak için `-TenantId` kullanılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-129">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="4d1cc-130">Normalde bu parametre kiracı kimliği veya etki alanı adı olarak sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-130">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="4d1cc-131">Ancak CSP olarak oturum açmak için **kiracı kimliği** sağlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-131">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="4d1cc-132">Başka bir bulut oturumu açma</span><span class="sxs-lookup"><span data-stu-id="4d1cc-132">Sign in to another Cloud</span></span>

<span data-ttu-id="4d1cc-133">Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasal düzenlerle uyumlu ortamlar sunar.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-133">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="4d1cc-134">Bölgesel buluttaki hesaplar için, oturum açarken `-Environment` bağımsız değişkeniyle ortamı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4d1cc-134">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="4d1cc-135">Örneğin, hesabınız Çin bulutundaysa:</span><span class="sxs-lookup"><span data-stu-id="4d1cc-135">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="4d1cc-136">Aşağıdaki komut, kullanılabilir ortamların listesini alır:</span><span class="sxs-lookup"><span data-stu-id="4d1cc-136">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="4d1cc-137">Azure rol tabanlı erişimi yönetme hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="4d1cc-137">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="4d1cc-138">Azure’da kimlik doğrulama ve abonelik yönetimi hakkında daha fazla bilgi edinmek için bkz. [Hesapları, Abonelikleri ve Yönetici Rollerini Yönetme](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="4d1cc-138">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="4d1cc-139">Rol yönetimi için Azure PowerShell cmdlet'leri:</span><span class="sxs-lookup"><span data-stu-id="4d1cc-139">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="4d1cc-140">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4d1cc-140">Get-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Get-azRoleAssignment)
* [<span data-ttu-id="4d1cc-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4d1cc-141">Get-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Get-azRoleDefinition)
* [<span data-ttu-id="4d1cc-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4d1cc-142">New-AzRoleAssignment</span></span>](/powershell/module/az.Resources/New-azRoleAssignment)
* [<span data-ttu-id="4d1cc-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4d1cc-143">New-AzRoleDefinition</span></span>](/powershell/module/az.Resources/New-azRoleDefinition)
* [<span data-ttu-id="4d1cc-144">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4d1cc-144">Remove-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [<span data-ttu-id="4d1cc-145">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4d1cc-145">Remove-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [<span data-ttu-id="4d1cc-146">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4d1cc-146">Set-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Set-azRoleDefinition)
