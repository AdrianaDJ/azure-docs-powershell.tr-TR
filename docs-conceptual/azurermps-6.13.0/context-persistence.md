---
title: Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme
description: Farklı PowerShell oturumlarında Azure kimlik bilgilerini ve diğer bilgileri yeniden kullanmayı öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: a07b5fe8cd532f99038d7f0ce10b3b891c896da1
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52827216"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="dc773-103">Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme</span><span class="sxs-lookup"><span data-stu-id="dc773-103">Persist user credentials across PowerShell sessions</span></span>

<span data-ttu-id="dc773-104">Azure PowerShell aşağıdaki özellikleri getiren **Azure Context Autosave** adlı bir özellik sunar:</span><span class="sxs-lookup"><span data-stu-id="dc773-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="dc773-105">Yeni PowerShell oturumlarında yeniden kullanım için oturum açma bilgilerini tutma.</span><span class="sxs-lookup"><span data-stu-id="dc773-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="dc773-106">Uzun süre çalışan cmdlet'leri yürütmek için arka plan görevlerini daha kolay kullanma.</span><span class="sxs-lookup"><span data-stu-id="dc773-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="dc773-107">Ayrı bir oturum açma olmadan hesaplar, abonelikler ve ortamlar arasında geçiş yapma.</span><span class="sxs-lookup"><span data-stu-id="dc773-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="dc773-108">Farklı kimlik bilgileri ve abonelikler kullanarak, görevleri aynı PowerShell oturumundan aynı anda yürütme.</span><span class="sxs-lookup"><span data-stu-id="dc773-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="dc773-109">Tanımlanan Azure bağlamları</span><span class="sxs-lookup"><span data-stu-id="dc773-109">Azure contexts defined</span></span>

<span data-ttu-id="dc773-110">*Azure bağlamı*, Azure PowerShell cmdlet’lerinin hedefini tanımlayan bilgiler kümesidir.</span><span class="sxs-lookup"><span data-stu-id="dc773-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="dc773-111">Bağlam beş bölümden oluşur:</span><span class="sxs-lookup"><span data-stu-id="dc773-111">The context consists of five parts:</span></span>

- <span data-ttu-id="dc773-112">*Hesap* - Azure ile iletişimin kimliğini doğrulamak için kullanılan UserName veya Hizmet Sorumlusu</span><span class="sxs-lookup"><span data-stu-id="dc773-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="dc773-113">*Abonelik* - Üzerinde işlem yapılan Kaynakların bulunduğu Azure Aboneliği.</span><span class="sxs-lookup"><span data-stu-id="dc773-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="dc773-114">*Kiracı* - Aboneliğinizi içeren Azure Active Directory kiracısı.</span><span class="sxs-lookup"><span data-stu-id="dc773-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="dc773-115">Kiracılar ServicePrincipal kimlik doğrulaması için daha önemlidir.</span><span class="sxs-lookup"><span data-stu-id="dc773-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="dc773-116">*Ortam* - Hedeflenen Azure Bulutu, genellikle Azure genel bulutudur.</span><span class="sxs-lookup"><span data-stu-id="dc773-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="dc773-117">Ancak, ortamı ayarı Ulusal, Kamu ve şirket içi (Azure Stack) bulutları da hedeflemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="dc773-118">*Kimlik Bilgileri* - Kimliğinizi doğrulamak ve Azure’daki kaynaklara erişim yetkinizi onaylamak için Azure tarafından kullanılan bilgiler</span><span class="sxs-lookup"><span data-stu-id="dc773-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="dc773-119">Önceki sürümlerde, Azure Bağlamının yeni bir PowerShell oturumu açtığınız her durumda oluşturulması gerekiyordu.</span><span class="sxs-lookup"><span data-stu-id="dc773-119">In previous releases, an Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="dc773-120">Azure PowerShell v4.4.0'dan başlayarak, her yeni PowerShell oturumunun açılışında Azure Bağlamları otomatik olarak kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="dc773-120">Beginning with Azure PowerShell v4.4.0, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="dc773-121">Sonraki oturum için bağlamı otomatik olarak kaydetme</span><span class="sxs-lookup"><span data-stu-id="dc773-121">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="dc773-122">6.3.0 ve sonraki sürümlerde, Azure PowerShell oturumlar arasında bağlam bilgilerinizi otomatik olarak tutar.</span><span class="sxs-lookup"><span data-stu-id="dc773-122">In versions 6.3.0 and later, Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="dc773-123">PowerShell’i bağlam ve kimlik bilgilerinizi unutacak şekilde ayarlamak için `Disable-AzureRmContextAutoSave` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc773-123">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="dc773-124">Açtığınız her PowerShell oturumunda Azure oturumu açmanız gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="dc773-124">You'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="dc773-125">Azure PowerShell’in PowerShell oturumu kapatıldıktan sonra bağlamınızı hatırlamasına izin vermek için `Enable-AzureRmContextAutosave` kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc773-125">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="dc773-126">Bağlam ve kimlik bilgileri, kullanıcı dizininizdeki (`%AppData%\Roaming\Windows Azure PowerShell`) özel bir gizli klasöre otomatik olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="dc773-126">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="dc773-127">Her yeni PowerShell oturumu son oturumunuzda kullanılan bağlamı hedefler.</span><span class="sxs-lookup"><span data-stu-id="dc773-127">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="dc773-128">Azure bağlamlarını yönetmenizi sağlayan cmdlet’ler, hassas denetime de olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="dc773-129">Değişikliklerin yalnızca mevcut PowerShell oturumunda (`Process` kapsamı) veya her PowerShell oturumunda (`CurrentUser` kapsamı) geçerli olmasını istiyorsanız.</span><span class="sxs-lookup"><span data-stu-id="dc773-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="dc773-130">Bu seçenekler [Bağlam Kapsamlarını Kullanma](#Using-Context-Scopes) bölümünde daha ayrıntılı olarak ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="dc773-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="dc773-131">Azure PowerShell cmdlet'lerini arka plan işleri olarak çalıştırma</span><span class="sxs-lookup"><span data-stu-id="dc773-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="dc773-132">**Azure Bağlam Otomatik Kaydı** özelliği ayrıca bağlamınızı PowerShell arka plan işleri ile paylaşmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="dc773-133">PowerShell, uzun süre yürütülen görevlerin tamamlanmasını beklemek zorunda kalmadan görevleri arka plan işleri olarak başlatıp izlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="dc773-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="dc773-134">Kimlik bilgilerini arka plan işleri ile iki farklı şekilde paylaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="dc773-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="dc773-135">Bağlamı bağımsız değişken olarak geçirme</span><span class="sxs-lookup"><span data-stu-id="dc773-135">Passing the context as an argument</span></span>

  <span data-ttu-id="dc773-136">Birçok AzureRM cmdlet’i, bağlamı cmdlet’e parametre olarak geçirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="dc773-137">Bağlamı bir arka plan işine aşağıdaki örnekte gösterildiği gibi geçirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="dc773-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="dc773-138">Otomatik kaydetme etkinken varsayılan bağlamı kullanma</span><span class="sxs-lookup"><span data-stu-id="dc773-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="dc773-139">**Bağlam Otomatik Kaydı**’nı etkinleştirdiyseniz, arka plan işlerinde otomatik olarak kayıtlı varsayılan bağlam kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc773-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="dc773-140">Arka plan görevinin sonucunu öğrenmek istediğiniz, `Get-Job` seçeneğini kullanarak iş durumunu denetleyin ve `Wait-Job` ile İşin tamamlanmasını bekleyin.</span><span class="sxs-lookup"><span data-stu-id="dc773-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="dc773-141">Arka plan işinin çıktısını yakalamak veya görüntülemek için `Receive-Job` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc773-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="dc773-142">Daha fazla bilgi için bkz. [İşler hakkında](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="dc773-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="dc773-143">Bağlam oluşturma, seçme, yeniden adlandırma ve kaldırma</span><span class="sxs-lookup"><span data-stu-id="dc773-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="dc773-144">Bağlam oluşturmak için Azure'da oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc773-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="dc773-145">`Connect-AzureRmAccount` cmdlet’i (veya diğer adıyla `Login-AzureRmAccount`), Azure PowerShell cmdlet’leri tarafından kullanılan varsayılan bağlamı ayarlar ve kimlik bilgilerinizin izin verdiği tüm kiracı ya da aboneliklere erişmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-145">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="dc773-146">Oturum açtıktan sonra yeni bir bağlam eklemek için `Set-AzureRmContext` (veya diğer adıyla `Select-AzureRmSubscription`) cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc773-146">To add a new context after sign-in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="dc773-147">Önceki örnekte, mevcut kimlik bilgileriniz kullanılarak 'Contoso Aboneliği 1'’i hedefleyen yeni bir bağlam eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="dc773-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="dc773-148">Yeni bağlam 'Contoso1' olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="dc773-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="dc773-149">Bağlam için ad belirtmezseniz, hesap kimliği ve abonelik kimliğinin kullanıldığı varsayılan bir ad kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc773-149">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="dc773-150">Var olan bir bağlamı yeniden adlandırmak için `Rename-AzureRmContext` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc773-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="dc773-151">Örnek:</span><span class="sxs-lookup"><span data-stu-id="dc773-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="dc773-152">Bu örnekte, otomatik adı `[user1@contoso.org; 123456-7890-1234-564321]` olan bağlam 'Contoso2' basit adıyla yeniden adlandırılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dc773-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="dc773-153">Bağlamları yöneten cmdlet’ler aynı zamanda sekme tamamlamayı kullanarak bağlamı hızlıca seçmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="dc773-154">Son olarak, bir bağlamı kaldırmak için `Remove-AzureRmContext` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc773-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="dc773-155">Örnek:</span><span class="sxs-lookup"><span data-stu-id="dc773-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="dc773-156">'Contoso2' adlı bağlamı unutur.</span><span class="sxs-lookup"><span data-stu-id="dc773-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="dc773-157">Bu bağlamı `Set-AzureRmContext` kullanarak yeniden oluşturabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dc773-157">You can recreate this context using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="dc773-158">Kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="dc773-158">Removing credentials</span></span>

<span data-ttu-id="dc773-159">`Disconnect-AzureRmAccount` (aynı zamanda `Logout-AzureRmAccount` olarak bilinir) kullanarak bir kullanıcı ya da hizmet sorumlusuna ait tüm kimlik bilgilerini ve ilişkili bağlamları kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc773-159">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="dc773-160">Parametre olmadan çalıştırıldığında, `Disconnect-AzureRmAccount` cmdlet'i mevcut bağlamda Kullanıcı veya Hizmet Sorumlusu ile ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dc773-160">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="dc773-161">Belirli bir sorumluyu hedeflemek için bir Kullanıcı Adı, Hizmet Asıl Adı ya da bağlam geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc773-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="dc773-162">Bağlam kapsamlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="dc773-162">Using context scopes</span></span>

<span data-ttu-id="dc773-163">Bazı durumlarda, diğer oturumları etkilemeden bir PowerShell oturumundaki bağlamı seçmek, değiştirmek ya da kaldırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc773-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="dc773-164">Bağlam cmdlet'lerinin varsayılan davranışını değiştirmek için `Scope` parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc773-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="dc773-165">`Process` kapsamı yalnızca mevcut oturum için geçerli olmasını sağlayarak varsayılan davranışı geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="dc773-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="dc773-166">Buna karşılık `CurrentUser` kapsamı, yalnızca mevcut oturum yerine tüm oturumlardaki bağlamı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dc773-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="dc773-167">Örnek olarak, diğer pencereleri etkilemeden mevcut PowerShell oturumundaki varsayılan bağlamı veya açılan bir sonraki oturumda kullanılan bağlamı değiştirmek için şunu kullanın:</span><span class="sxs-lookup"><span data-stu-id="dc773-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="dc773-168">Bağlam otomatik kaydetme ayarını hatırlama</span><span class="sxs-lookup"><span data-stu-id="dc773-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="dc773-169">Bağlam Otomatik Kaydetme ayarı, kullanıcının Azure PowerShell dizinine (`%AppData%\Roaming\Windows Azure PowerShell`) kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="dc773-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="dc773-170">Bilgisayar hesaplarının bazı türleri bu dizine erişemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="dc773-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="dc773-171">Bu tür senaryolar için ortam değişkenini kullanabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dc773-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="dc773-172">Bağlam 'true' olarak ayarlandığında otomatik olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="dc773-172">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="dc773-173">Bağlam 'false' olarak ayarlanırsa kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="dc773-173">If set to 'false', the context isn't saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="dc773-174">AzureRM.Profile modülündeki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="dc773-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="dc773-175">Bağlam yönetmeye yönelik yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="dc773-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="dc773-176">[Enable-AzureRmContextAutosave][enable] - Powershell oturumları arasında bağlamı kaydetmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="dc773-177">Her türlü değişiklik, genel bağlamı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dc773-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="dc773-178">[Disable-AzureRmContextAutosave][disable] - Bağlamı otomatik kaydetmeyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="dc773-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="dc773-179">Her yeni PowerShell oturumunda yeniden oturum açmak gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc773-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="dc773-180">[Select-AzureRmContext][select] - Bir bağlamı varsayılan bağlam olarak seçer.</span><span class="sxs-lookup"><span data-stu-id="dc773-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="dc773-181">Tüm cmdlet'ler kimlik doğrulaması için bu bağlamdaki kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-181">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="dc773-182">[Disconnect-AzureRmAccount][remove-cred] - Bir hesapla ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dc773-182">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="dc773-183">[Remove-AzureRmContext][remove-context] - Adlandırılmış bir bağlamı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dc773-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="dc773-184">[Rename-AzureRmContext][rename] - Mevcut bir bağlamı yeniden adlandırır.</span><span class="sxs-lookup"><span data-stu-id="dc773-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="dc773-185">Mevcut profil cmdlet'lerinde yapılan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="dc773-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="dc773-186">[Add-AzureRmAccount][login] - İşlem veya mevcut kullanıcı için oturum açma kapsamının ayarlanmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="dc773-186">[Add-AzureRmAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="dc773-187">Kimlik doğrulamasından sonra varsayılan bağlamı adlandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="dc773-188">[Import-AzureRmContext][import] - İşlem veya mevcut kullanıcı için oturum açma kapsamının ayarlanmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="dc773-188">[Import-AzureRmContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="dc773-189">[Set-AzureRmContext][set-context] - Mevcut adlandırılmış bağlamların ve işlem ya da mevcut kullanıcıdaki kapsam değişikliklerinin seçilmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dc773-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext
