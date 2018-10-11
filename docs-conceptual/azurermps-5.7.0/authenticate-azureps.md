---
title: Azure PowerShell ile oturum açma
description: Kullanıcı olarak, hizmet sorumlusu olarak veya Azure kaynakları için yönetilen kimlikleri kullanarak Azure PowerShell oturumu açma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 530eafcd0d14dbfd790a22d80c5922f304f4e0b2
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882546"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="09fb9-103">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="09fb9-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="09fb9-104">Azure PowerShell, birden fazla kimlik doğrulama yöntemini destekler.</span><span class="sxs-lookup"><span data-stu-id="09fb9-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="09fb9-105">Hizmeti kullanmaya başlamanın en basit yolu, komut satırından etkileşimli olarak oturum açmaktır.</span><span class="sxs-lookup"><span data-stu-id="09fb9-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="09fb9-106">Etkileşimli olarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="09fb9-106">Sign in interactively</span></span>

<span data-ttu-id="09fb9-107">Etkileşimli olarak oturum açmak için [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="09fb9-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="09fb9-108">Bu cmdlet çalıştırıldığında, Azure hesabınızla ilişkilendirilmiş e-posta adresinizle parolanızı soran bir iletişim kutusu açar.</span><span class="sxs-lookup"><span data-stu-id="09fb9-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="09fb9-109">Kimlik doğrulaması yaptığınızda, bu bilgiler geçerli PowerShell oturumu için kaydedilir, iletişim kutusu kapatılır ve tüm Azure PowerShell cmdlet'lerine erişim kazanırsınız.</span><span class="sxs-lookup"><span data-stu-id="09fb9-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09fb9-110">Bu oturum açma işlemi _yalnızca_ geçerli PowerShell oturumuna yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="09fb9-110">This sign in is for the current PowerShell session _only_.</span></span> <span data-ttu-id="09fb9-111">Kimlik doğrulamasının birden çok oturumda kalıcı olmasını sağlamak için, [Kalıcı Kimlik Bilgileri](context-persistence.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="09fb9-111">To persist authentication across multiple sessions, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="09fb9-112">Hizmet sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="09fb9-112">Sign in with a service principal</span></span>

<span data-ttu-id="09fb9-113">Hizmet sorumluları kaynakları düzenlemek amacıyla kullanabileceğiniz, etkileşimli olmayan hesaplar oluşturmanız için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="09fb9-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="09fb9-114">Hizmet sorumluları, Azure Active Directory’yi kullanarak kurallarınızı uygulayabileceğiniz kullanıcı hesapları gibidir.</span><span class="sxs-lookup"><span data-stu-id="09fb9-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="09fb9-115">Bir hizmet sorumlusuna gerekli en düşük izinleri vererek otomasyon betiklerinizin daha da güvenli olmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09fb9-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="09fb9-116">Azure PowerShell'le kullanmak üzere bir hizmet sorumlusu oluşturmanız gerekirse, bkz. [Azure PowerShell ile Azure hizmet sorumlusu oluşturma](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="09fb9-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="09fb9-117">Hizmet sorumlusuyla oturum açmak için `Connect-AzureRmAccount` cmdlet'iyle `-ServicePrincipal` bağımsız değişkenini kullanın.</span><span class="sxs-lookup"><span data-stu-id="09fb9-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="09fb9-118">Hizmet sorumlusunun uygulama kimliğine, oturum açma kimlik bilgilerine ve hizmet sorumlusuyla ilişkilendirilmiş kiracı kimliğine de ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="09fb9-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="09fb9-119">Hizmet sorumlusunun kimlik bilgilerini uygun bir nesne olarak almak için [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="09fb9-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="09fb9-120">Bu cmdlet, hizmet sorumlusu kimliğini ve parolasını girmeniz için bir iletişim kutusu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="09fb9-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="09fb9-121">Azure kaynakları için yönetilen kimlikleri kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="09fb9-121">Sign in using managed identities for Azure resources</span></span>

<span data-ttu-id="09fb9-122">Azure kaynakları için yönetilen kimlikler bir Azure Active Directory özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="09fb9-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="09fb9-123">Oturum açmak için bir yönetilen kimlik hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09fb9-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="09fb9-124">Yönetilen kimlikler yalnızca Azure bulutunda çalıştırılan sanal makinelerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="09fb9-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="09fb9-125">Azure kaynaklarına ilişkin yönetilen kimlikler hakkında daha fazla bilgi için bkz. [Erişim belirteci almak için Azure VM'de Azure kaynaklarına ilişkin yönetilen kimlikleri kullanma](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="09fb9-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="09fb9-126">Başka bir bulut oturumu açma</span><span class="sxs-lookup"><span data-stu-id="09fb9-126">Sign in to another Cloud</span></span>

<span data-ttu-id="09fb9-127">Azure Cloud Services, çeşitli bölgelerin veri işleme düzenlemelerine uygun farklı ortamlar sunar.</span><span class="sxs-lookup"><span data-stu-id="09fb9-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="09fb9-128">Azure hesabınız bu bölgelerden biriyle ilişkili bir buluttaysa, oturum açarken ortamı belirtmeni gerekir.</span><span class="sxs-lookup"><span data-stu-id="09fb9-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="09fb9-129">Örneğin hesabınız Çin bulutundaysa şu komutla oturum açmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="09fb9-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="09fb9-130">Kullanabileceğiniz ortamların listesine ulaşmak için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="09fb9-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="09fb9-131">Azure rol tabanlı erişimi yönetme hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="09fb9-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="09fb9-132">Azure’da kimlik doğrulama ve abonelik yönetimi hakkında daha fazla bilgi edinmek için bkz. [Hesapları, Abonelikleri ve Yönetici Rollerini Yönetme](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="09fb9-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="09fb9-133">Rol yönetimi için Azure PowerShell cmdlet'leri:</span><span class="sxs-lookup"><span data-stu-id="09fb9-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="09fb9-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="09fb9-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="09fb9-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="09fb9-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="09fb9-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="09fb9-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="09fb9-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="09fb9-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="09fb9-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="09fb9-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="09fb9-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="09fb9-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="09fb9-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="09fb9-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
