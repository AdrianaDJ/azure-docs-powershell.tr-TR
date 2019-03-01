---
title: Azure PowerShell ile Azure aboneliklerini yönetme
description: Azure PowerShell ile Azure aboneliklerini yönetme
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 29d7c84d0ca9ae8d3e4e22f407b007d2d582f8bc
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837648"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="1b830-103">Birden çok Azure aboneliği kullanma</span><span class="sxs-lookup"><span data-stu-id="1b830-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="1b830-104">Çoğu Azure kullanıcısı sadece tek bir aboneliğe sahip olur.</span><span class="sxs-lookup"><span data-stu-id="1b830-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="1b830-105">Ancak, birden çok kuruluşun parçasıysanız veya kuruluşunuz belirli kaynaklara erişimi gruplar arasında böldüyse, Azure’da birden fazla aboneliğiniz olabilir.</span><span class="sxs-lookup"><span data-stu-id="1b830-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="1b830-106">CLI hem genel olarak hem de komut başına abonelik seçimini destekler.</span><span class="sxs-lookup"><span data-stu-id="1b830-106">The CLI supports selecting a subscription both globally and per command.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="1b830-107">Kiracılar, kullanıcılar ve abonelikler</span><span class="sxs-lookup"><span data-stu-id="1b830-107">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="1b830-108">Azure’da kiracılar, kullanıcılar ve abonelikler arasındaki fark biraz kafa karıştırıcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1b830-108">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="1b830-109">_Kiracı_, kuruluşun tamamını kapsayan bir Azure Active Directory varlığıdır.</span><span class="sxs-lookup"><span data-stu-id="1b830-109">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="1b830-110">Bu kiracı en az bir _abonelik_ ve _kullanıcıya_ sahiptir.</span><span class="sxs-lookup"><span data-stu-id="1b830-110">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="1b830-111">Kullanıcı bir kişidir ve yalnızca ait olduğu kuruluş olan tek bir kiracı ile ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="1b830-111">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="1b830-112">Kullanıcılar, kaynakları oluşturmak, yönetmek ve kullanmak için Azure’da oturum açan hesaplardır.</span><span class="sxs-lookup"><span data-stu-id="1b830-112">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="1b830-113">Bir kullanıcının, Microsoft ile bulut hizmetlerini (Azure dahil) kullanmak için yapılan anlaşmaları ifade eden birden çok _aboneliğe_ erişimi olabilir.</span><span class="sxs-lookup"><span data-stu-id="1b830-113">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="1b830-114">Her kaynak bir abonelik ile ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="1b830-114">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="1b830-115">Kiracılar, kullanıcılar ve abonelikler arasındaki farklar hakkında daha fazla bilgi için bkz. [Azure bulut terimleri sözlüğü](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="1b830-115">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="1b830-116">Azure Active Directory kiracınıza yeni bir abonelik ekleme hakkında bilgi almak için bkz. [Azure Active Directory'ye bir Azure aboneliğini ekleme](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="1b830-116">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="1b830-117">Belirli bir kiracıda oturum açmayı öğrenmek için bkz. [Azure PowerShell ile oturum açma](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="1b830-117">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="1b830-118">Etkin aboneliği değiştirme</span><span class="sxs-lookup"><span data-stu-id="1b830-118">Change the active subscription</span></span>

<span data-ttu-id="1b830-119">Azure PowerShell'de, bir abonelik için kaynaklara erişirken geçerli Azure oturumunuzla ilişkilendirilmiş aboneliğin değiştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="1b830-119">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="1b830-120">Bu işlem etkin oturum bağlamı, cmdlet'lerin çalıştırılacağı kiracı, abonelik ve kullanıcı hakkındaki bilgiler değiştirilerek yapılır.</span><span class="sxs-lookup"><span data-stu-id="1b830-120">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="1b830-121">Abonelikleri değiştirmek için, önce [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) ile bir Azure PowerShell Context nesnesinin alınması ve ardından [Set-AzContext](/powershell/module/az.accounts/set-azcontext) ile geçerli bağlamın değiştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="1b830-121">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="1b830-122">Sonraki örnekte, etkin durumdaki kiracıda bir aboneliği alma ve bunu etkin oturum olarak ayarlama işlemleri gösterilir:</span><span class="sxs-lookup"><span data-stu-id="1b830-122">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="1b830-123">Azure PowerShell bağlamları hakkında daha fazla bilgi edinmek, bunların nasıl kaydedildiğini ve kolayca birden çok abonelikle çalışmak üzere aralarında nasıl hızla geçiş yapıldığını öğrenmek için, bkz. [Azure PowerShell bağlamlarında kimlik bilgilerini kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1b830-123">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>
