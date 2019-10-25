---
title: Azure bağlamları ve oturum açma bilgileri
description: Farklı PowerShell oturumlarında Azure kimlik bilgilerini ve diğer bilgileri yeniden kullanmayı öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: 0e8dd4f766307d9ab2e27e2cf8bec6bbd34f5e51
ms.sourcegitcommit: 1cdff856d1d559b978aac6bc034dd2f99ac04afe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2019
ms.locfileid: "72791423"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="203d3-103">Azure PowerShell bağlam nesneleri</span><span class="sxs-lookup"><span data-stu-id="203d3-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="203d3-104">Azure PowerShell abonelik ve kimlik doğrulaması bilgilerini tutmak için _Azure PowerShell bağlam nesneleri_ (Azure bağlamları) kullanır.</span><span class="sxs-lookup"><span data-stu-id="203d3-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="203d3-105">Birden fazla aboneliğiniz varsa, Azure bağlamları Azure PowerShell cmdlet'lerinin üzerinde çalıştırılacağı aboneliği seçmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="203d3-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="203d3-106">Azure bağlamları birden fazla PowerShell oturumunda oturum açma bilgilerini depolamak ve arka plan görevlerini çalıştırmak için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="203d3-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="203d3-107">Bu makalede aboneliklerin veya hesapların yönetimi değil Azure bağlamlarının yönetimi açıklanır.</span><span class="sxs-lookup"><span data-stu-id="203d3-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="203d3-108">Kullanıcıları, abonelikleri, kiracıları veya diğer hesap bilgilerini yönetme konusunu arıyorsanız [Azure Active Directory](/azure/active-directory) belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="203d3-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="203d3-109">Bağlamları kullanarak arka plan görevlerini veya paralel görevleri çalıştırmayı öğrenmek için, Azure bağlamlarını anladıktan sonra [PowerShell işlerinde Azure PowerShell cmdlet'lerini kullanma](using-psjobs.md) belgesine bakın.</span><span class="sxs-lookup"><span data-stu-id="203d3-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="203d3-110">Azure bağlam nesnelerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="203d3-110">Overview of Azure context objects</span></span>

<span data-ttu-id="203d3-111">Azure bağlamları, üzerinde komutların çalıştırılacağı etkin aboneliğinizi ve Azure bulutuna bağlanmak için gereken kimlik doğrulama bilgilerini temsil eden PowerShell nesneleridir.</span><span class="sxs-lookup"><span data-stu-id="203d3-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="203d3-112">Azure bağlamlarıyla, Azure PowerShell'in her abonelik değiştirdiğinizde kimliğinizi yeniden doğrulaması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="203d3-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="203d3-113">Azure bağlamı şunlardan oluşur:</span><span class="sxs-lookup"><span data-stu-id="203d3-113">An Azure context consists of:</span></span>

* <span data-ttu-id="203d3-114">[Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) ile Azure'da oturum açarken kullanılmış olan _hesap_.</span><span class="sxs-lookup"><span data-stu-id="203d3-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="203d3-115">Azure bağlamları, hesap açısından kullanıcıları, uygulama kimliklerini ve hizmet sorumlularını aynı şekilde değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="203d3-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="203d3-116">_Kiracı_ ile ilişkilendirilmiş Azure kaynaklarını oluşturmak ve çalıştırmak için Microsoft'la yapılan bir hizmet sözleşmesi olan etkin _abonelik_.</span><span class="sxs-lookup"><span data-stu-id="203d3-116">The active _subscription_, a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="203d3-117">Belgelerde ve Active Directory ile çalışırken kiracılardan genellikle _kuruluşlar_ olarak söz edilir.</span><span class="sxs-lookup"><span data-stu-id="203d3-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="203d3-118">Azure bulutuna erişmek için depolanan kimlik doğrulama belirteci olan _belirteç önbelleği_ başvurusu.</span><span class="sxs-lookup"><span data-stu-id="203d3-118">A reference to a _token cache_, a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="203d3-119">Bu belirtecin nerede depolandığı ve ne kadar süreyle kalıcı olacağı [bağlam otomatik kaydetme ayarları](#save-azure-contexts-across-powershell-sessions) tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="203d3-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="203d3-120">Bu terimlerle ilgili daha fazla bilgi için bkz. [Azure Active Directory Terminolojisi](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span><span class="sxs-lookup"><span data-stu-id="203d3-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="203d3-121">Azure bağlamları tarafından kullanılan kimlik doğrulama belirteçleri, kalıcı bir oturumun parçası olan diğer depolanmış belirteçlerle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="203d3-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span> 

<span data-ttu-id="203d3-122">`Connect-AzAccount` ile oturum açtığınızda varsayılan aboneliğiniz için en az bir Azure bağlamı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="203d3-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="203d3-123">`Connect-AzAccount` tarafından döndürülen nesne, PowerShell oturumunun kalanında kullanılan varsayılan Azure bağlamıdır.</span><span class="sxs-lookup"><span data-stu-id="203d3-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="203d3-124">Azure bağlamlarını alma</span><span class="sxs-lookup"><span data-stu-id="203d3-124">Get Azure contexts</span></span>

<span data-ttu-id="203d3-125">Kullanılabilir Azure bağlamları [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet'iyle alınır.</span><span class="sxs-lookup"><span data-stu-id="203d3-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="203d3-126">Tüm kullanılabilir bağlamları listelemek için `-ListAvailable` kullanın:</span><span class="sxs-lookup"><span data-stu-id="203d3-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="203d3-127">İsterseniz bağlamı adını belirterek de alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="203d3-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-Context -Name "mycontext"
```

<span data-ttu-id="203d3-128">Bağlam adları, ilişkili aboneliğin adından farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="203d3-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="203d3-129">Kullanılabilir Azure bağlamları her zaman sizin kullanılabilir abonelikleriniz __olmayabilir__.</span><span class="sxs-lookup"><span data-stu-id="203d3-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="203d3-130">Azure bağlamları yalnızca yerel olarak depolanmış bilgileri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="203d3-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="203d3-131">Aboneliklerinizi [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet'iyle alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="203d3-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="203d3-132">Abonelik bilgilerinden yeni Azure bağlamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="203d3-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="203d3-133">Hem yeni Azure bağlamlarını oluşturmak hem de bunları etkin bağlam olarak ayarlamak için [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext?view=azps-1.8.0) cmdlet'i kullanılır.</span><span class="sxs-lookup"><span data-stu-id="203d3-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext?view=azps-1.8.0) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="203d3-134">Yeni Azure bağlamı oluşturmanın en kolay yolu mevcut abonelik bilgilerini kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="203d3-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="203d3-135">Cmdlet, çıkış nesnesini `Get-AzSubscription` cmdlet'inden yönlendirilmiş değer olarak alacak ve yeni Azure bağlamını yapılandıracak şekilde tasarlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="203d3-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="203d3-136">Gerekirse abonelik adını veya kimliğini ve kiracı kimliğini de verebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="203d3-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="203d3-137">`-Name` bağımsız değişkeni atlanırsa, bağlam adı olarak `Subscription Name (subscription-id)` biçiminde aboneliğin adı ve kimliği kullanılır.</span><span class="sxs-lookup"><span data-stu-id="203d3-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="203d3-138">Etkin Azure bağlamını değiştirme</span><span class="sxs-lookup"><span data-stu-id="203d3-138">Change the active Azure context</span></span>

<span data-ttu-id="203d3-139">Etkin Azure bağlamını değiştirmek için hem `Set-AzContext` hem de [Select-AzContext](/powershell/module/az.accounts/set-azcontext?view=azps-1.8.0) kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="203d3-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext?view=azps-1.8.0) can be used to change the active Azure context.</span></span> <span data-ttu-id="203d3-140">[Yeni Azure bağlamı oluşturma](#create-a-new-azure-context-from-subscription-information) bölümünde açıklandığı gibi, abonelik için Azure bağlamı yoksa `Set-AzContext` yeni bir Azure bağlamı oluşturur ve ardından etkin bağlam olarak bunu kullanmaya geçer.</span><span class="sxs-lookup"><span data-stu-id="203d3-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="203d3-141">`Select-AzContext` cmdlet'inin yalnızca mevcut Azure bağlamlarıyla kullanılması amaçlanmıştır ve `Set-AzContext -Context` kullanımına benzer şekilde çalışır ama yönlendirmeyle kullanılacak şekilde tasarlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="203d3-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="203d3-142">Azure PowerShell'deki diğer birçok hesap ve bağlam yönetimi komutu gibi `Set-AzContext` ve `Select-AzContext` de `-Scope` bağımsız değişkenini desteklendiğinden bağlamın ne kadar süreyle etkin olacağını denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="203d3-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="203d3-143">`-Scope`, varsayılanı değiştirmeden tek oturumun etkin bağlamını değiştirmenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="203d3-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="203d3-144">PowerShell oturumunun tamamında bağlamların değiştirilmesini önlemek için, tüm Azure PowerShell komutları `-AzContext` bağımsız değişkeniyle verilen bir bağlamda çalıştırılabilir:</span><span class="sxs-lookup"><span data-stu-id="203d3-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="203d3-145">Azure PowerShell cmdlet'lerinde bağlamların diğer önemli kullanım şekli arka plan komutlarını çalıştırmaktır.</span><span class="sxs-lookup"><span data-stu-id="203d3-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="203d3-146">Azure PowerShell kullanarak PowerShell İşlerini çalıştırma hakkında daha fazla bilgi edinmek için bkz. [PowerShell İşlerinde Azure PowerShell cmdlet'lerini çalıştırma](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="203d3-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="203d3-147">PowerShell oturumları arasında Azure bağlamlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="203d3-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="203d3-148">Azure bağlamları varsayılan olarak PowerShell oturumları arasında kullanılmak üzere kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="203d3-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="203d3-149">Bu davranışı aşağıdaki yollarla değiştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="203d3-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="203d3-150">`Connect-AzAccount` cmdlet'iyle `-Scope Process` kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="203d3-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="203d3-151">Bu oturum açma işleminin bir parçası olarak döndürülen Azure bağlamı _yalnızca_ güncel oturumda geçerlidir ve Azure PowerShell bağlam otomatik kaydetme ayarı ne olursa olsun otomatik olarak kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="203d3-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="203d3-152">Azure PowerShell'in bağlam otomatik kaydetme ayarını [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet'iyle devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="203d3-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="203d3-153">Bağlam otomatik kaydetme ayarı devre dışı bırakıldığında depolanmış olan belirteçler __temizlenmez__.</span><span class="sxs-lookup"><span data-stu-id="203d3-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="203d3-154">Depolanan Azure bağlam bilgilerini temizlemeyi öğrenmek için bkz. [Azure bağlamlarını ve kimlik bilgilerini kaldırma](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="203d3-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="203d3-155">Azure bağlamı otomatik kaydetme ayarını [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet'iyle açıkça etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="203d3-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="203d3-156">Otomatik kaydetme etkinleştirildiğinde kullanıcının tüm bağlamları sonraki PowerShell oturumları için yerel olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="203d3-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="203d3-157">Bağlamları gelecekteki PowerShell oturumlarında kullanılmak üzere [Save-AzContext](/powershell/module/az.accounts/save-azcontext) cmdlet'iyle el ile kaydedin. Bunlar sonraki oturumlarda [Import-AzContext](/powershell/module/az.accounts/import-azcontext) cmdlet'iyle yüklenebilir:</span><span class="sxs-lookup"><span data-stu-id="203d3-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="203d3-158">Bağlam otomatik kaydetme ayarı devre dışı bırakıldığında, daha önce kaydedilmiş olan depolanan bağlam bilgileri __temizlenmez__.</span><span class="sxs-lookup"><span data-stu-id="203d3-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="203d3-159">Depolanan bilgileri kaldırmak için [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="203d3-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="203d3-160">Kaydedilmiş bağlamları kaldırma hakkında daha fazla bilgi için bkz. [Bağlamları ve kimlik bilgilerini kaldırma](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="203d3-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="203d3-161">Bu komutların her biri, yalnızca çalışan işleme uygulamak üzere `Process` değerini alabilen `-Scope` parametresini destekler.</span><span class="sxs-lookup"><span data-stu-id="203d3-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="203d3-162">Örneğin, yeni oluşturulan bağlamların PowerShell oturumundan çıkarken kaydedilmemesini sağlamak için:</span><span class="sxs-lookup"><span data-stu-id="203d3-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="203d3-163">Bağlam bilgileri ve belirteçler Windows'da `$env:USERPROFILE\.Azure` dizininde ve diğer platformlarda `$HOME/.Azure` konumunda depolanır.</span><span class="sxs-lookup"><span data-stu-id="203d3-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="203d3-164">Abonelik kimlikleri ve kiracı kimlikleri gibi hassas bilgiler yine de günlükler ve kaydedilmiş bağlamlar aracılığıyla depolanan bilgilerde kullanıma sunuluyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="203d3-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="203d3-165">Depolanan bilgileri temizlemeyi öğrenmek için bkz. [Bağlamları ve kimlik bilgilerini kaldırma](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="203d3-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="203d3-166">Azure bağlamlarını ve depolanan kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="203d3-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="203d3-167">Azure bağlamlarını ve kimlik bilgilerini temizlemek için:</span><span class="sxs-lookup"><span data-stu-id="203d3-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="203d3-168">[Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount) ile bir hesabın oturumunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="203d3-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="203d3-169">Hesabın oturumunu hesaba veya bağlama göre kapatabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="203d3-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="203d3-170">Bağlantının kesilmesi her zaman depolanan kimlik doğrulama belirteçlerini kaldırır ve bağlantısı kesilmiş kullanıcıyla veya bağlamla ilişkili kaydedilmiş bağlamları temizler.</span><span class="sxs-lookup"><span data-stu-id="203d3-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="203d3-171">[Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="203d3-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="203d3-172">Bu cmdlet, her zaman depolanan bağlamlarla kimlik doğrulama belirteçlerinin kaldırılmasını garanti eder, ayrıca oturumunuzu da kapatır.</span><span class="sxs-lookup"><span data-stu-id="203d3-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="203d3-173">Bağlamı [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext) ile kaldırın:</span><span class="sxs-lookup"><span data-stu-id="203d3-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="203d3-174">Etkin bağlamı kaldırırsanız Azure'la bağlantınız kesilir ve `Connect-AzAccount` ile yeniden kimlik doğrulaması yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="203d3-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="203d3-175">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="203d3-175">See also</span></span>

* [<span data-ttu-id="203d3-176">PowerShell İşlerinde Azure PowerShell cmdlet'lerini çalıştırma</span><span class="sxs-lookup"><span data-stu-id="203d3-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="203d3-177">Azure Active Directory Terminolojisi</span><span class="sxs-lookup"><span data-stu-id="203d3-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="203d3-178">Az.Accounts başvurusu</span><span class="sxs-lookup"><span data-stu-id="203d3-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)