---
title: Azure kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme
description: Farklı PowerShell oturumlarında Azure kimlik bilgilerini ve diğer bilgileri yeniden kullanmayı öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 02b8090aa1868f24445ddff3a95c0d0c376e2cb8
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2019
ms.locfileid: "72370408"
---
# <a name="persist-azure-user-credentials-across-powershell-sessions"></a><span data-ttu-id="740eb-103">Azure kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme</span><span class="sxs-lookup"><span data-stu-id="740eb-103">Persist Azure user credentials across PowerShell sessions</span></span>

<span data-ttu-id="740eb-104">Azure PowerShell aşağıdaki özellikleri getiren **Azure Context Autosave** adlı bir özellik sunar:</span><span class="sxs-lookup"><span data-stu-id="740eb-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="740eb-105">Yeni PowerShell oturumlarında yeniden kullanım için oturum açma bilgilerini tutma.</span><span class="sxs-lookup"><span data-stu-id="740eb-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="740eb-106">Uzun süre çalışan cmdlet'leri yürütmek için arka plan görevlerini daha kolay kullanma.</span><span class="sxs-lookup"><span data-stu-id="740eb-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="740eb-107">Ayrı bir oturum açma olmadan hesaplar, abonelikler ve ortamlar arasında geçiş yapma.</span><span class="sxs-lookup"><span data-stu-id="740eb-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="740eb-108">Farklı kimlik bilgileri ve abonelikler kullanarak, görevleri aynı PowerShell oturumundan aynı anda yürütme.</span><span class="sxs-lookup"><span data-stu-id="740eb-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="740eb-109">Tanımlanan Azure bağlamları</span><span class="sxs-lookup"><span data-stu-id="740eb-109">Azure contexts defined</span></span>

<span data-ttu-id="740eb-110">*Azure bağlamı*, Azure PowerShell cmdlet’lerinin hedefini tanımlayan bilgiler kümesidir.</span><span class="sxs-lookup"><span data-stu-id="740eb-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="740eb-111">Bağlam beş bölümden oluşur:</span><span class="sxs-lookup"><span data-stu-id="740eb-111">The context consists of five parts:</span></span>

- <span data-ttu-id="740eb-112">*Hesap* - Azure ile iletişimin kimliğini doğrulamak için kullanılan UserName veya Hizmet Sorumlusu</span><span class="sxs-lookup"><span data-stu-id="740eb-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="740eb-113">*Abonelik* - Üzerinde işlem yapılan Kaynakların bulunduğu Azure Aboneliği.</span><span class="sxs-lookup"><span data-stu-id="740eb-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="740eb-114">*Kiracı* - Aboneliğinizi içeren Azure Active Directory kiracısı.</span><span class="sxs-lookup"><span data-stu-id="740eb-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="740eb-115">Kiracılar ServicePrincipal kimlik doğrulaması için daha önemlidir.</span><span class="sxs-lookup"><span data-stu-id="740eb-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="740eb-116">*Ortam* - Hedeflenen Azure Bulutu, genellikle Azure genel bulutudur.</span><span class="sxs-lookup"><span data-stu-id="740eb-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="740eb-117">Ancak, ortamı ayarı Ulusal, Kamu ve şirket içi (Azure Stack) bulutları da hedeflemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="740eb-118">*Kimlik Bilgileri* - Kimliğinizi doğrulamak ve Azure’daki kaynaklara erişim yetkinizi onaylamak için Azure tarafından kullanılan bilgiler</span><span class="sxs-lookup"><span data-stu-id="740eb-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="740eb-119">Azure PowerShell’in son sürümüyle birlikte, her yeni PowerShell oturumunun açılışında Azure Bağlamları otomatik olarak kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="740eb-119">With the latest version of Azure PowerShell, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="740eb-120">Sonraki oturum için bağlamı otomatik olarak kaydetme</span><span class="sxs-lookup"><span data-stu-id="740eb-120">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="740eb-121">Azure PowerShell, oturumlar arasında bağlam bilgilerinizi otomatik olarak tutar.</span><span class="sxs-lookup"><span data-stu-id="740eb-121">Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="740eb-122">PowerShell’i bağlam ve kimlik bilgilerinizi unutacak şekilde ayarlamak için `Disable-AzContextAutoSave` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="740eb-122">To set PowerShell to forget your context and credentials, use `Disable-AzContextAutoSave`.</span></span> <span data-ttu-id="740eb-123">Bağlam kaydetme devre dışı bırakıldığında, açtığınız her PowerShell oturumunda Azure oturumu açmanız gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="740eb-123">With context saving disabled, you'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="740eb-124">Azure PowerShell’in PowerShell oturumu kapatıldıktan sonra bağlamınızı hatırlamasına izin vermek için `Enable-AzContextAutosave` kullanın.</span><span class="sxs-lookup"><span data-stu-id="740eb-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzContextAutosave`.</span></span> <span data-ttu-id="740eb-125">Bağlam ve kimlik bilgileri, kullanıcı dizininizdeki (Windows’da `$env:USERPROFILE\.Azure`, diğer platformlarda `$HOME/.Azure`) özel bir gizli klasöre otomatik olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="740eb-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="740eb-126">Her yeni PowerShell oturumu son oturumunuzda kullanılan bağlamı hedefler.</span><span class="sxs-lookup"><span data-stu-id="740eb-126">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="740eb-127">Azure bağlamlarını yönetmenizi sağlayan cmdlet’ler, hassas denetime de olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-127">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="740eb-128">Değişikliklerin yalnızca mevcut PowerShell oturumunda (`Process` kapsamı) veya her PowerShell oturumunda (`CurrentUser` kapsamı) geçerli olmasını istiyorsanız.</span><span class="sxs-lookup"><span data-stu-id="740eb-128">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="740eb-129">Bu seçenekler [Bağlam Kapsamlarını Kullanma](#using-context-scopes) bölümünde daha ayrıntılı olarak ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="740eb-129">These options are discussed in more detail in [Using Context Scopes](#using-context-scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="740eb-130">Azure PowerShell cmdlet'lerini arka plan işleri olarak çalıştırma</span><span class="sxs-lookup"><span data-stu-id="740eb-130">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="740eb-131">**Azure Bağlam Otomatik Kaydı** özelliği ayrıca bağlamınızı PowerShell arka plan işleri ile paylaşmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-131">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="740eb-132">PowerShell, uzun süre yürütülen görevlerin tamamlanmasını beklemek zorunda kalmadan görevleri arka plan işleri olarak başlatıp izlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="740eb-132">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="740eb-133">Kimlik bilgilerini arka plan işleri ile iki farklı şekilde paylaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="740eb-133">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="740eb-134">Bağlamı bağımsız değişken olarak geçirme</span><span class="sxs-lookup"><span data-stu-id="740eb-134">Passing the context as an argument</span></span>

  <span data-ttu-id="740eb-135">Birçok AzureRM cmdlet’i, bağlamı cmdlet’e parametre olarak geçirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-135">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="740eb-136">Bağlamı bir arka plan işine aşağıdaki örnekte gösterildiği gibi geçirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="740eb-136">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- <span data-ttu-id="740eb-137">Otomatik kaydetme etkinken varsayılan bağlamı kullanma</span><span class="sxs-lookup"><span data-stu-id="740eb-137">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="740eb-138">**Bağlam Otomatik Kaydı**’nı etkinleştirdiyseniz, arka plan işlerinde otomatik olarak kayıtlı varsayılan bağlam kullanılır.</span><span class="sxs-lookup"><span data-stu-id="740eb-138">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

<span data-ttu-id="740eb-139">Arka plan görevinin sonucunu öğrenmek istediğiniz, `Get-Job` seçeneğini kullanarak iş durumunu denetleyin ve `Wait-Job` ile İşin tamamlanmasını bekleyin.</span><span class="sxs-lookup"><span data-stu-id="740eb-139">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="740eb-140">Arka plan işinin çıktısını yakalamak veya görüntülemek için `Receive-Job` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="740eb-140">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="740eb-141">Daha fazla bilgi için bkz. [İşler hakkında](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="740eb-141">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="740eb-142">Bağlam oluşturma, seçme, yeniden adlandırma ve kaldırma</span><span class="sxs-lookup"><span data-stu-id="740eb-142">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="740eb-143">Bağlam oluşturmak için Azure'da oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="740eb-143">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="740eb-144">`Connect-AzAccount` cmdlet’i (veya diğer adıyla `Login-AzAccount`), Azure PowerShell cmdlet’leri tarafından kullanılan varsayılan bağlamı ayarlar ve kimlik bilgilerinizin izin verdiği tüm kiracı ya da aboneliklere erişmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-144">The `Connect-AzAccount` cmdlet (or its alias, `Login-AzAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="740eb-145">Oturum açtıktan sonra yeni bir bağlam eklemek için `Set-AzContext` (veya diğer adıyla `Select-AzSubscription`) cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="740eb-145">To add a new context after sign-in, use `Set-AzContext` (or its alias, `Select-AzSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="740eb-146">Önceki örnekte, mevcut kimlik bilgileriniz kullanılarak 'Contoso Aboneliği 1'’i hedefleyen yeni bir bağlam eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="740eb-146">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="740eb-147">Yeni bağlam 'Contoso1' olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="740eb-147">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="740eb-148">Bağlam için ad belirtmezseniz, hesap kimliği ve abonelik kimliğinin kullanıldığı varsayılan bir ad kullanılır.</span><span class="sxs-lookup"><span data-stu-id="740eb-148">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="740eb-149">Var olan bir bağlamı yeniden adlandırmak için `Rename-AzContext` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="740eb-149">To rename an existing context, use the `Rename-AzContext` cmdlet.</span></span> <span data-ttu-id="740eb-150">Örnek:</span><span class="sxs-lookup"><span data-stu-id="740eb-150">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="740eb-151">Bu örnekte, otomatik adı `[user1@contoso.org; 123456-7890-1234-564321]` olan bağlam 'Contoso2' basit adıyla yeniden adlandırılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="740eb-151">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="740eb-152">Bağlamları yöneten cmdlet’ler aynı zamanda sekme tamamlamayı kullanarak bağlamı hızlıca seçmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-152">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="740eb-153">Son olarak, bir bağlamı kaldırmak için `Remove-AzContext` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="740eb-153">Finally, to remove a context, use the `Remove-AzContext` cmdlet.</span></span>  <span data-ttu-id="740eb-154">Örnek:</span><span class="sxs-lookup"><span data-stu-id="740eb-154">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

<span data-ttu-id="740eb-155">'Contoso2' adlı bağlamı unutur.</span><span class="sxs-lookup"><span data-stu-id="740eb-155">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="740eb-156">Bu bağlamı `Set-AzContext` kullanarak yeniden oluşturabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="740eb-156">You can recreate this context using `Set-AzContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="740eb-157">Kimlik bilgilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="740eb-157">Removing credentials</span></span>

<span data-ttu-id="740eb-158">`Disconnect-AzAccount` (aynı zamanda `Logout-AzAccount` olarak bilinir) kullanarak bir kullanıcı ya da hizmet sorumlusuna ait tüm kimlik bilgilerini ve ilişkili bağlamları kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="740eb-158">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzAccount` (also known as `Logout-AzAccount`).</span></span> <span data-ttu-id="740eb-159">Parametre olmadan çalıştırıldığında, `Disconnect-AzAccount` cmdlet'i mevcut bağlamda Kullanıcı veya Hizmet Sorumlusu ile ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="740eb-159">When executed without parameters, the `Disconnect-AzAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="740eb-160">Belirli bir sorumluyu hedeflemek için bir Kullanıcı Adı, Hizmet Asıl Adı ya da bağlam geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="740eb-160">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="740eb-161">Bağlam kapsamlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="740eb-161">Using context scopes</span></span>

<span data-ttu-id="740eb-162">Bazı durumlarda, diğer oturumları etkilemeden bir PowerShell oturumundaki bağlamı seçmek, değiştirmek ya da kaldırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="740eb-162">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="740eb-163">Bağlam cmdlet'lerinin varsayılan davranışını değiştirmek için `Scope` parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="740eb-163">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="740eb-164">`Process` kapsamı yalnızca mevcut oturum için geçerli olmasını sağlayarak varsayılan davranışı geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="740eb-164">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="740eb-165">Buna karşılık `CurrentUser` kapsamı, yalnızca mevcut oturum yerine tüm oturumlardaki bağlamı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="740eb-165">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="740eb-166">Örnek olarak, diğer pencereleri etkilemeden mevcut PowerShell oturumundaki varsayılan bağlamı veya açılan bir sonraki oturumda kullanılan bağlamı değiştirmek için şunu kullanın:</span><span class="sxs-lookup"><span data-stu-id="740eb-166">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="740eb-167">Bağlam otomatik kaydetme ayarını hatırlama</span><span class="sxs-lookup"><span data-stu-id="740eb-167">How the context autosave setting is remembered</span></span>

<span data-ttu-id="740eb-168">Bağlam Otomatik Kaydetme ayarı, kullanıcının Azure PowerShell dizinine (Windows’da `$env:USERPROFILE\.Azure`, diğer platformlarda `$HOME/.Azure`) kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="740eb-168">The context AutoSave setting is saved to the user Azure PowerShell directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="740eb-169">Bilgisayar hesaplarının bazı türleri bu dizine erişemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="740eb-169">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="740eb-170">Bu tür senaryolar için ortam değişkenini kullanabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="740eb-170">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="740eb-171">Bağlam 'true' olarak ayarlandığında otomatik olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="740eb-171">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="740eb-172">Bağlam 'false' olarak ayarlanırsa kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="740eb-172">If set to 'false', the context isn't saved.</span></span>

## <a name="context-management-cmdlets"></a><span data-ttu-id="740eb-173">Bağlam yönetimi cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="740eb-173">Context management cmdlets</span></span>

- <span data-ttu-id="740eb-174">[Enable-AzContextAutosave][enable] - Powershell oturumları arasında bağlamı kaydetmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-174">[Enable-AzContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="740eb-175">Her türlü değişiklik, genel bağlamı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="740eb-175">Any changes alter the global context.</span></span>
- <span data-ttu-id="740eb-176">[Disable-AzContextAutosave][disable] - Bağlamı otomatik kaydetmeyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="740eb-176">[Disable-AzContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="740eb-177">Her yeni PowerShell oturumunda yeniden oturum açmak gerekir.</span><span class="sxs-lookup"><span data-stu-id="740eb-177">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="740eb-178">[Select-AzContext][select] - Bir bağlamı varsayılan bağlam olarak seçer.</span><span class="sxs-lookup"><span data-stu-id="740eb-178">[Select-AzContext][select] - Select a context as the default.</span></span> <span data-ttu-id="740eb-179">Tüm cmdlet'ler kimlik doğrulaması için bu bağlamdaki kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-179">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="740eb-180">[Disconnect-AzAccount][remove-cred] - Bir hesapla ilişkili tüm kimlik bilgilerini ve bağlamları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="740eb-180">[Disconnect-AzAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="740eb-181">[Remove-AzContext][remove-context] - Adlandırılmış bir bağlamı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="740eb-181">[Remove-AzContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="740eb-182">[Rename-AzContext][rename] - Mevcut bir bağlamı yeniden adlandırır.</span><span class="sxs-lookup"><span data-stu-id="740eb-182">[Rename-AzContext][rename] - Rename an existing context.</span></span>
- <span data-ttu-id="740eb-183">[Add-AzAccount][login] - İşlem veya geçerli kullanıcı için oturum açma kapsamının ayarlanmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="740eb-183">[Add-AzAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="740eb-184">Kimlik doğrulamasından sonra varsayılan bağlamı adlandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-184">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="740eb-185">[Import-AzContext][import] - İşlem veya geçerli kullanıcı için oturum açma kapsamının ayarlanmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="740eb-185">[Import-AzContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="740eb-186">[Set-AzContext][set-context] - Mevcut adlandırılmış bağlamların ve işlem ya da geçerli kullanıcı kapsam değişikliklerinin seçilmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="740eb-186">[Set-AzContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
