---
title: Azure PowerShell ile oturum açma
description: Azure PowerShell ile oturum açma
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 1af5aeffb8e87e916df3e2440a84805935136c0f
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2018
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="c953a-103">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="c953a-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="c953a-104">Azure PowerShell, birden fazla oturum açma yöntemini destekler.</span><span class="sxs-lookup"><span data-stu-id="c953a-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="c953a-105">Hizmeti kullanmaya başlamanın en basit yolu, komut satırından etkileşimli olarak oturum açmaktır.</span><span class="sxs-lookup"><span data-stu-id="c953a-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="c953a-106">Etkileşimli oturum açma</span><span class="sxs-lookup"><span data-stu-id="c953a-106">Interactive log in</span></span>

1. <span data-ttu-id="c953a-107">`Login-AzureRmAccount` yazın.</span><span class="sxs-lookup"><span data-stu-id="c953a-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="c953a-108">Azure kimlik bilgilerinizi isteyen bir iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="c953a-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="c953a-109">Hesabınızla ilişkili e-posta adresini ve parolayı yazın.</span><span class="sxs-lookup"><span data-stu-id="c953a-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="c953a-110">Azure, kimlik bilgilerini doğrulayıp kaydeder ve pencereyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="c953a-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="c953a-111">Hizmet sorumlusu ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="c953a-111">Log in with a service principal</span></span>

<span data-ttu-id="c953a-112">Hizmet sorumluları kaynakları düzenlemek amacıyla kullanabileceğiniz, etkileşimli olmayan hesaplar oluşturmanız için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="c953a-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="c953a-113">Hizmet sorumluları, Azure Active Directory’yi kullanarak kurallarınızı uygulayabileceğiniz kullanıcı hesapları gibidir.</span><span class="sxs-lookup"><span data-stu-id="c953a-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="c953a-114">Bir hizmet sorumlusuna gerekli en düşük izinleri vererek otomasyon betiklerinizin daha da güvenli olmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c953a-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="c953a-115">Zaten bir hizmet sorumlunuz yoksa [hizmet sorumlusu oluşturun](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c953a-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="c953a-116">Hizmet sorumlusu ile oturum açın.</span><span class="sxs-lookup"><span data-stu-id="c953a-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="c953a-117">TenantId’nizi almak için etkileşimli olarak oturum açın ve aboneliğinizden TenantId’yi edinin.</span><span class="sxs-lookup"><span data-stu-id="c953a-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="c953a-118">Azure VM Yönetilen Hizmet Kimliği kullanarak oturum açma</span><span class="sxs-lookup"><span data-stu-id="c953a-118">Log in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="c953a-119">Yönetilen Hizmet Kimliği (MSI), Azure Active Directory’nin bir önizleme özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="c953a-119">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="c953a-120">Oturum açmak için bir MSI hizmet sorumlusu kullanabilir ve diğer kaynaklara erişmek için yalnızca uygulamaya yönelik bir erişim belirteci edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c953a-120">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="c953a-121">MSI hakkında daha fazla bilgi için bkz. [Oturum açma ve belirteç edinme için Azure VM Yönetilen Hizmet Kimliği’ni (MSI) kullanma](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span><span class="sxs-lookup"><span data-stu-id="c953a-121">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="c953a-122">Başka bir bulut oturumu açma</span><span class="sxs-lookup"><span data-stu-id="c953a-122">Log in to another Cloud</span></span>

<span data-ttu-id="c953a-123">Azure Cloud Services, devletlerin veri işleme düzenlemelerine uygun farklı ortamlar sunar.</span><span class="sxs-lookup"><span data-stu-id="c953a-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="c953a-124">Azure hesabınız kamu bulutlarından birindeyse oturum açtığınızda ilgili ortamı belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c953a-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="c953a-125">Örneğin hesabınız Çin bulutundaysa şu komutla oturum açmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="c953a-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="c953a-126">Kullanabileceğiniz ortamların listesine ulaşmak için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="c953a-126">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="c953a-127">Azure rol tabanlı erişimi yönetme hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="c953a-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="c953a-128">Azure’da kimlik doğrulama ve abonelik yönetimi hakkında daha fazla bilgi edinmek için bkz. [Hesapları, Abonelikleri ve Yönetici Rollerini Yönetme](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="c953a-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="c953a-129">Rol yönetimi için Azure PowerShell cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="c953a-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="c953a-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c953a-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="c953a-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c953a-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="c953a-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c953a-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="c953a-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c953a-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="c953a-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c953a-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="c953a-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c953a-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="c953a-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c953a-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
