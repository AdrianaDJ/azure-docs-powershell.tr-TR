---
title: PowerShell oturumları arasında kullanıcı oturumlarını sürdürme
description: Bu makalede Azure PowerShell’in kimlik bilgilerini ve diğer kullanıcı bilgilerini birden fazla PowerShell oturumunda yeniden kullanmanıza olanak tanıyan yeni özellikleri açıklanmaktadır.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 15e1c9ca770c9fcd72513c4f53f7726edd9c2469
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2018
---
# <a name="persisting-user-logins-across-powershell-sessions"></a><span data-ttu-id="7da6c-103">PowerShell oturumları arasında kullanıcı oturumlarını sürdürme</span><span class="sxs-lookup"><span data-stu-id="7da6c-103">Persisting user logins across PowerShell sessions</span></span>

<span data-ttu-id="7da6c-104">Azure PowerShell’in Eylül 2017 sürümünde, Azure Resource Manager cmdlet’leri **Azure Bağlam Otomatik Kaydı** adlı yeni bir özelliği kullanıma sunmuştur.</span><span class="sxs-lookup"><span data-stu-id="7da6c-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="7da6c-105">Bu özellik aşağıdaki birkaç yeni kullanıcı senaryosunu mümkün kılar:</span><span class="sxs-lookup"><span data-stu-id="7da6c-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="7da6c-106">Yeni PowerShell oturumlarında yeniden kullanım için oturum açma bilgilerini tutma.</span><span class="sxs-lookup"><span data-stu-id="7da6c-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="7da6c-107">Uzun süre çalışan cmdlet'leri yürütmek için arka plan görevlerini daha kolay kullanma.</span><span class="sxs-lookup"><span data-stu-id="7da6c-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="7da6c-108">Ayrı bir oturum açma olmadan hesaplar, abonelikler ve ortamlar arasında geçiş yapma.</span><span class="sxs-lookup"><span data-stu-id="7da6c-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="7da6c-109">Farklı kimlik bilgileri ve abonelikler kullanarak, görevleri aynı PowerShell oturumundan aynı anda yürütme.</span><span class="sxs-lookup"><span data-stu-id="7da6c-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="7da6c-110">Tanımlanan Azure bağlamları</span><span class="sxs-lookup"><span data-stu-id="7da6c-110">Azure contexts defined</span></span>

<span data-ttu-id="7da6c-111">*Azure bağlamı*, Azure PowerShell cmdlet’lerinin hedefini tanımlayan bilgiler kümesidir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="7da6c-112">Bağlam beş bölümden oluşur:</span><span class="sxs-lookup"><span data-stu-id="7da6c-112">The context consists of five parts:</span></span>

- <span data-ttu-id="7da6c-113">*Hesap* - Azure ile iletişimin kimliğini doğrulamak için kullanılan UserName veya Hizmet Sorumlusu</span><span class="sxs-lookup"><span data-stu-id="7da6c-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="7da6c-114">*Abonelik* - Üzerinde işlem yapılan Kaynakları içeren Azure Aboneliği.</span><span class="sxs-lookup"><span data-stu-id="7da6c-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="7da6c-115">*Kiracı* - Aboneliğinizi içeren Azure Active Directory kiracısı.</span><span class="sxs-lookup"><span data-stu-id="7da6c-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="7da6c-116">Kiracılar ServicePrincipal kimlik doğrulaması için daha önemlidir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="7da6c-117">*Ortam* - Hedeflenen Azure Bulutu, genellikle Azure genel bulutudur.</span><span class="sxs-lookup"><span data-stu-id="7da6c-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="7da6c-118">Ancak, ortamı ayarı Ulusal, Kamu ve şirket içi (Azure Stack) bulutları da hedeflemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="7da6c-119">*Kimlik Bilgileri* - Kimliğinizi doğrulamak ve Azure’daki kaynaklara erişim yetkinizden emin olmak için Azure tarafından kullanılan bilgiler</span><span class="sxs-lookup"><span data-stu-id="7da6c-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="7da6c-120">Önceki sürümlerde, Azure Bağlamınızın yeni bir PowerShell oturumu açtığınız her durumda oluşturulması gerekiyordu.</span><span class="sxs-lookup"><span data-stu-id="7da6c-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="7da6c-121">Azure PowerShell v4.4.0’dan itibaren, Azure Bağlamlarının otomatik kaydedilmesini ve yeni bir PowerShell oturumu açtığınız her durumda yeniden kullanılmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da6c-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="7da6c-122">Sonraki oturum için bağlamı otomatik olarak kaydetme</span><span class="sxs-lookup"><span data-stu-id="7da6c-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="7da6c-123">Azure PowerShell varsayılan olarak PowerShell oturumunuzu her kapattığınızda bağlam bilgilerinizi siler.</span><span class="sxs-lookup"><span data-stu-id="7da6c-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="7da6c-124">Azure PowerShell’in PowerShell oturumu kapatıldıktan sonra bağlamınızı hatırlamasına izin vermek için `Enable-AzureRmContextAutosave` kullanın.</span><span class="sxs-lookup"><span data-stu-id="7da6c-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="7da6c-125">Bağlam ve kimlik bilgileri, kullanıcı dizininizdeki (`%AppData%\Roaming\Windows Azure PowerShell`) özel bir gizli klasöre otomatik olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="7da6c-126">Daha sonra, her yeni PowerShell oturumu son oturumunuzda kullanılan bağlamı hedefler.</span><span class="sxs-lookup"><span data-stu-id="7da6c-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="7da6c-127">PowerShell’i bağlam ve kimlik bilgilerinizi unutacak şekilde ayarlamak için `Disable-AzureRmContextAutoSave` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7da6c-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="7da6c-128">Açtığınız her PowerShell oturumunda Azure oturumu açmanız gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="7da6c-129">Azure bağlamlarını yönetmenizi sağlayan cmdlet’ler, hassas denetime de olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="7da6c-130">Değişikliklerin yalnızca mevcut PowerShell oturumunda (`Process` kapsamı) veya her PowerShell oturumunda (`CurrentUser` kapsamı) geçerli olmasını istiyorsanız.</span><span class="sxs-lookup"><span data-stu-id="7da6c-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="7da6c-131">Bu seçenekler [Bağlam Kapsamlarını Kullanma](#Using-Context-Scopes) bölümünde daha ayrıntılı olarak ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="7da6c-132">Azure PowerShell cmdlet'lerini arka plan işleri olarak çalıştırma</span><span class="sxs-lookup"><span data-stu-id="7da6c-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="7da6c-133">**Azure Bağlam Otomatik Kaydı** özelliği ayrıca bağlamınızı PowerShell arka plan işleri ile paylaşmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="7da6c-134">PowerShell, uzun süre yürütülen görevlerin tamamlanmasını beklemek zorunda kalmadan görevleri arka plan işleri olarak başlatıp izlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7da6c-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="7da6c-135">Kimlik bilgilerini arka plan işleri ile iki farklı şekilde paylaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7da6c-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="7da6c-136">Bağlamı bağımsız değişken olarak geçirme</span><span class="sxs-lookup"><span data-stu-id="7da6c-136">Passing the context as an argument</span></span>

  <span data-ttu-id="7da6c-137">Birçok AzureRM cmdlet’i, bağlamı cmdlet’e parametre olarak geçirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="7da6c-138">Bağlamı bir arka plan işine aşağıdaki örnekte gösterildiği gibi geçirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7da6c-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="7da6c-139">Otomatik kaydetme etkinken varsayılan bağlamı kullanma</span><span class="sxs-lookup"><span data-stu-id="7da6c-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="7da6c-140">**Bağlam Otomatik Kaydı**’nı etkinleştirdiyseniz, arka plan işlerinde otomatik olarak kayıtlı varsayılan bağlam kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="7da6c-141">Arka plan görevinin sonucunu öğrenmek istediğiniz, `Get-Job` seçeneğini kullanarak iş durumunu denetleyin ve `Wait-Job` ile İşin tamamlanmasını bekleyin.</span><span class="sxs-lookup"><span data-stu-id="7da6c-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="7da6c-142">Arka plan işinin çıktısını yakalamak veya görüntülemek için `Receive-Job` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7da6c-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="7da6c-143">Daha fazla bilgi için bkz. [İşler hakkında](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="7da6c-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="7da6c-144">Bağlam oluşturma, seçme, yeniden adlandırma ve kaldırma</span><span class="sxs-lookup"><span data-stu-id="7da6c-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="7da6c-145">Bağlam oluşturmak için Azure'da oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="7da6c-146">`Connect-AzureRmAccount` cmdlet’i (veya diğer adıyla `Login-AzureRmAccount`), sonraki Azure PowerShell cmdlet’leri tarafından kullanılan varsayılan bağlamı ayarlar ve oturum açma bilgilerinizin izin verdiği tüm kiracı ya da aboneliklere erişmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-146">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="7da6c-147">Oturum açtıktan sonra yeni bir bağlam eklemek için `Set-AzureRmContext` (veya diğer adıyla `Select-AzureRmSubscription`) cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7da6c-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="7da6c-148">Önceki örnekte, mevcut kimlik bilgileriniz kullanılarak 'Contoso Aboneliği 1'’i hedefleyen yeni bir bağlam eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="7da6c-149">Yeni bağlam 'Contoso1' olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="7da6c-150">Bağlam için bir ad belirtmezseniz, hesap kimliği ve abonelik kimliğinin kullanıldığı varsayılan bir ad kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="7da6c-151">Var olan bir bağlamı yeniden adlandırmak için `Rename-AzureRmContext` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7da6c-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="7da6c-152">Örnek:</span><span class="sxs-lookup"><span data-stu-id="7da6c-152">For example:</span></span>

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="7da6c-153">Bu örnekte, otomatik adı `[user1@contoso.org; 123456-7890-1234-564321]` olan bağlam 'Contoso2' basit adıyla yeniden adlandırılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="7da6c-154">Bağlamları yöneten cmdlet’ler aynı zamanda sekme tamamlamayı kullanarak bağlamı hızlıca seçmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="7da6c-155">Son olarak, bir bağlamı kaldırmak için `Remove-AzureRmContext` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7da6c-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="7da6c-156">Örnek:</span><span class="sxs-lookup"><span data-stu-id="7da6c-156">For example:</span></span>

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="7da6c-157">'Contoso2' adlı bağlamı unutur.</span><span class="sxs-lookup"><span data-stu-id="7da6c-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="7da6c-158">Bu bağlamı daha sonra `Set-AzureRmContext` kullanarak yeniden oluşturabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7da6c-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="7da6c-159">Kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="7da6c-159">Removing credentials</span></span>

<span data-ttu-id="7da6c-160">`Disconnect-AzureRmAccount` (aynı zamanda `Logout-AzureRmAccount` olarak bilinir) kullanarak bir kullanıcı ya da hizmet sorumlusuna ait tüm kimlik bilgilerini ve ilişkili bağlamları kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da6c-160">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="7da6c-161">Parametre olmadan çalıştırıldığında, `Disconnect-AzureRmAccount` cmdlet'i mevcut bağlamda Kullanıcı veya Hizmet Sorumlusu ile ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-161">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="7da6c-162">Belirli bir sorumluyu hedeflemek için bir Kullanıcı Adı, Hizmet Asıl Adı ya da bağlam geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da6c-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```powershell
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="7da6c-163">Bağlam kapsamlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="7da6c-163">Using context scopes</span></span>

<span data-ttu-id="7da6c-164">Bazı durumlarda, diğer oturumları etkilemeden bir PowerShell oturumundaki bağlamı seçmek, değiştirmek ya da kaldırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da6c-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="7da6c-165">Bağlam cmdlet'lerinin varsayılan davranışını değiştirmek için `Scope` parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7da6c-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="7da6c-166">`Process` kapsamı yalnızca mevcut oturum için geçerli olmasını sağlayarak varsayılan davranışı geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="7da6c-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="7da6c-167">Buna karşılık `CurrentUser` kapsamı, yalnızca mevcut oturum yerine tüm oturumlardaki bağlamı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="7da6c-168">Örnek olarak, diğer pencereleri etkilemeden mevcut PowerShell oturumundaki varsayılan bağlamı veya açılan bir sonraki oturumda kullanılan bağlamı değiştirmek için şunu kullanın:</span><span class="sxs-lookup"><span data-stu-id="7da6c-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="7da6c-169">Bağlam otomatik kaydetme ayarını hatırlama</span><span class="sxs-lookup"><span data-stu-id="7da6c-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="7da6c-170">Bağlam Otomatik Kaydetme ayarı, kullanıcının Azure PowerShell dizinine (`%AppData%\Roaming\Windows Azure PowerShell`) kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="7da6c-171">Bilgisayar hesaplarının bazı türleri bu dizine erişemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="7da6c-172">Bu tür senaryolar için ortam değişkenini kullanabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7da6c-172">For such scenarios, you can use the environment variable</span></span>

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="7da6c-173">Bağlam 'true' olarak ayarlanırsa otomatik olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="7da6c-174">Bağlam 'false' olarak ayarlanırsa kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="7da6c-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="7da6c-175">AzureRM.Profile modülündeki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7da6c-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="7da6c-176">Bağlam yönetmeye yönelik yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="7da6c-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="7da6c-177">[Enable-AzureRmContextAutosave][enable] - Powershell oturumları arasında bağlamı kaydetmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="7da6c-178">Her türlü değişiklik, genel bağlamı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="7da6c-179">[Disable-AzureRmContextAutosave][disable] - Bağlamı otomatik kaydetmeyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="7da6c-180">Her yeni PowerShell oturumunda yeniden oturum açmak gerekir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="7da6c-181">[Select-AzureRmContext][select] - Bir bağlamı varsayılan bağlam olarak seçer.</span><span class="sxs-lookup"><span data-stu-id="7da6c-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="7da6c-182">Sonraki tüm cmdlet'ler kimlik doğrulaması için bu bağlamdaki kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="7da6c-183">[Disconnect-AzureRmAccount][remove-cred] - Bir hesapla ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-183">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="7da6c-184">[Remove-AzureRmContext][remove-context] - Adlandırılmış bir bağlamı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="7da6c-185">[Rename-AzureRmContext][rename] - Mevcut bir bağlamı yeniden adlandırır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="7da6c-186">Mevcut profil cmdlet'lerinde yapılan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7da6c-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="7da6c-187">[Add-AzureRmAccount][login] - İşlem veya mevcut kullanıcı için oturum açma kapsamının ayarlanmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="7da6c-188">Oturum açtıktan sonra varsayılan bağlamı adlandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="7da6c-189">[Import-AzureRmContext][import] - İşlem veya mevcut kullanıcı için oturum açma kapsamının ayarlanmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="7da6c-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="7da6c-190">[Set-AzureRmContext][set-context] - Mevcut adlandırılmış bağlamların ve işlem ya da mevcut kullanıcıdaki kapsam değişikliklerinin seçilmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7da6c-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext