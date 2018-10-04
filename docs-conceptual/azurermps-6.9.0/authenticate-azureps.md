---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 2a118e1aa8b6755ef5769f44429427d22532780d
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425253"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="83041-103">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="83041-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="83041-104">Azure PowerShell, çeşitli kimlik doğrulama yöntemlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="83041-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="83041-105">Hizmeti kullanmaya başlamanın en basit yolu, komut satırından etkileşimli olarak oturum açmaktır.</span><span class="sxs-lookup"><span data-stu-id="83041-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="83041-106">Etkileşimli olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="83041-106">Sign in interactively</span></span>

<span data-ttu-id="83041-107">Etkileşimli olarak oturum açmak için [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="83041-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="83041-108">Bu cmdlet çalıştırıldığında, Azure hesabınızla ilişkilendirilmiş e-posta adresinizle parolanızı soran bir iletişim kutusu açar.</span><span class="sxs-lookup"><span data-stu-id="83041-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="83041-109">Bu kimlik doğrulaması geçerli PowerShell oturumunu süresince kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83041-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83041-110">Azure PowerShell 6.3.0'dan başlayarak, Windows'da oturumunuz açık kaldığı sürece kimlik bilgileriniz birden çok PowerShell oturumu arasında paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="83041-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="83041-111">Daha fazla bilgi için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="83041-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="83041-112">Hizmet sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="83041-112">Sign in with a service principal</span></span>

<span data-ttu-id="83041-113">Hizmet sorumluları etkileşimli olmayan Azure hesaplarıdır.</span><span class="sxs-lookup"><span data-stu-id="83041-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="83041-114">Diğer kullanıcı hesapları gibi onların izinleri de Azure Active Directory ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="83041-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="83041-115">Otomasyon betikleriniz hizmet sorumlusuna yalnızca ihtiyacı olan izinleri vererek güvenliğini korur.</span><span class="sxs-lookup"><span data-stu-id="83041-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="83041-116">Azure PowerShell'le kullanmak üzere hizmet sorumlusu oluşturmayı öğrenmek için, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="83041-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="83041-117">Hizmet sorumlusuyla oturum açmak için `Connect-AzureRmAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın.</span><span class="sxs-lookup"><span data-stu-id="83041-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="83041-118">Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="83041-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="83041-119">Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="83041-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="83041-120">Bu cmdlet, hizmet sorumlusu kimliğini ve parolasını girmeniz için bir iletişim kutusu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="83041-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="83041-121">Azure Yönetilen Hizmet Kimliği kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="83041-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="83041-122">Azure kaynakları için yönetilen kimlikler bir Azure Active Directory özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="83041-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="83041-123">Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="83041-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="83041-124">Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan sanal makinelerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="83041-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="83041-125">Azure kaynaklarına ilişkin yönetilen kimlikler hakkında daha fazla bilgi için bkz. [Erişim belirteci almak için Azure VM'de Azure kaynaklarına ilişkin yönetilen kimlikleri kullanma](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="83041-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="83041-126">Başka bir bulut oturumu açma</span><span class="sxs-lookup"><span data-stu-id="83041-126">Sign in to another Cloud</span></span>

<span data-ttu-id="83041-127">Azure bulut hizmetleri, bölgesel veri işlemeyle ilgili yasal düzenlerle uyumlu ortamlar sunar.</span><span class="sxs-lookup"><span data-stu-id="83041-127">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="83041-128">Bölgesel buluttaki hesaplar için, oturum açarken `-Environment` bağımsız değişkeniyle ortamı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="83041-128">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="83041-129">Örneğin, hesabınız Çin bulutundaysa:</span><span class="sxs-lookup"><span data-stu-id="83041-129">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="83041-130">Aşağıdaki komut, kullanılabilir ortamların listesini alır:</span><span class="sxs-lookup"><span data-stu-id="83041-130">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="83041-131">Azure rol tabanlı erişimi yönetme hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="83041-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="83041-132">Azure’da kimlik doğrulama ve abonelik yönetimi hakkında daha fazla bilgi edinmek için bkz. [Hesapları, Abonelikleri ve Yönetici Rollerini Yönetme](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="83041-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="83041-133">Rol yönetimi için Azure PowerShell cmdlet'leri:</span><span class="sxs-lookup"><span data-stu-id="83041-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="83041-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="83041-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="83041-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="83041-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="83041-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="83041-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="83041-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="83041-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="83041-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="83041-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="83041-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="83041-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="83041-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="83041-140">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
