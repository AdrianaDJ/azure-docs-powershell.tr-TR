---
Module Name: AzureRM.Profile
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
ms.openlocfilehash: bc3ccc2c2b0574eee40357fb0079fe22124ea3e6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571181"
---
# <span data-ttu-id="5ae21-101">AzureRM. profil modülü</span><span class="sxs-lookup"><span data-stu-id="5ae21-101">AzureRM.Profile Module</span></span>
## <span data-ttu-id="5ae21-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ae21-102">Description</span></span>
<span data-ttu-id="5ae21-103">Tüm Azure modülleri için kimlik bilgilerini ve ortak yapılandırmayı yönetir.</span><span class="sxs-lookup"><span data-stu-id="5ae21-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="5ae21-104">AzureRM. profil cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="5ae21-104">AzureRM.Profile Cmdlets</span></span>
### [<span data-ttu-id="5ae21-105">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="5ae21-105">Add-AzureRmAccount</span></span>](Add-AzureRmAccount.md)
<span data-ttu-id="5ae21-106">Azure Resource Manager cmdlet isteklerinde kullanılmak üzere kimliği doğrulanmış bir hesap ekler.</span><span class="sxs-lookup"><span data-stu-id="5ae21-106">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="5ae21-107">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="5ae21-107">Add-AzureRmEnvironment</span></span>](Add-AzureRmEnvironment.md)
<span data-ttu-id="5ae21-108">Bir Azure Resource Manager örneğine uç noktalar ve meta veriler ekler.</span><span class="sxs-lookup"><span data-stu-id="5ae21-108">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="5ae21-109">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5ae21-109">Clear-AzureRmContext</span></span>](Clear-AzureRmContext.md)
<span data-ttu-id="5ae21-110">Tüm Azure kimlik bilgilerini, hesap ve abonelik bilgilerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5ae21-110">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="5ae21-111">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="5ae21-111">Disable-AzureRmContextAutosave</span></span>](Disable-AzureRmContextAutosave.md)
<span data-ttu-id="5ae21-112">Azure kimlik bilgilerini otomatik kaydetmeyi kapatma.</span><span class="sxs-lookup"><span data-stu-id="5ae21-112">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="5ae21-113">PowerShell penceresini bir sonraki açışınızda oturum açma bilgileriniz unutulan</span><span class="sxs-lookup"><span data-stu-id="5ae21-113">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="5ae21-114">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="5ae21-114">Disable-AzureRmDataCollection</span></span>](Disable-AzureRmDataCollection.md)
<span data-ttu-id="5ae21-115">AzurePowerShell cmdlet 'lerini geliştirmek için veri toplama dışında.</span><span class="sxs-lookup"><span data-stu-id="5ae21-115">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="5ae21-116">Açıkça kabul etmediğiniz sürece veriler toplanmaz.</span><span class="sxs-lookup"><span data-stu-id="5ae21-116">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="5ae21-117">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="5ae21-117">Enable-AzureRmContextAutosave</span></span>](Enable-AzureRmContextAutosave.md)
<span data-ttu-id="5ae21-118">Bir PowerShell penceresini açtığınızda Azure kimlik bilgilerinin, hesabın ve abonelik bilgilerinin kaydedilmesine ve otomatik olarak yüklenmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="5ae21-118">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="5ae21-119">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="5ae21-119">Enable-AzureRmDataCollection</span></span>](Enable-AzureRmDataCollection.md)
<span data-ttu-id="5ae21-120">AzurePowerShell cmdlet 'leriyle Kullanıcı deneyimini geliştirmek için Azure PowerShell 'in veri toplamasını olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="5ae21-120">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="5ae21-121">Geçerli bilgisayarda geçerli kullanıcının veri koleksiyonunda bu cmdlet 'i yürütme.</span><span class="sxs-lookup"><span data-stu-id="5ae21-121">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="5ae21-122">Açıkça kabul edilmedikçe veri toplanmaz.</span><span class="sxs-lookup"><span data-stu-id="5ae21-122">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="5ae21-123">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5ae21-123">Get-AzureRmContext</span></span>](Get-AzureRmContext.md)
<span data-ttu-id="5ae21-124">Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="5ae21-124">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="5ae21-125">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="5ae21-125">Get-AzureRmContextAutosaveSetting</span></span>](Get-AzureRmContextAutosaveSetting.md)
<span data-ttu-id="5ae21-126">Bağlam otomatik kaydetme özelliğiyle ilgili meta verileri görüntüler; Örneğin, bağlam otomatik olarak kaydedilir ve kaydedilen içeriğin ve kimlik bilgilerinin bulunabileceği yerlerde.</span><span class="sxs-lookup"><span data-stu-id="5ae21-126">Display metadata about the context autosave feature, including whterh the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="5ae21-127">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="5ae21-127">Get-AzureRmEnvironment</span></span>](Get-AzureRmEnvironment.md)
<span data-ttu-id="5ae21-128">Bir Azure hizmetleri örneğinin uç noktalarını ve meta verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="5ae21-128">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="5ae21-129">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="5ae21-129">Get-AzureRmSubscription</span></span>](Get-AzureRmSubscription.md)
<span data-ttu-id="5ae21-130">Geçerli hesabın erişebileceği abonelikleri alın.</span><span class="sxs-lookup"><span data-stu-id="5ae21-130">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="5ae21-131">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="5ae21-131">Get-AzureRmTenant</span></span>](Get-AzureRmTenant.md)
<span data-ttu-id="5ae21-132">Geçerli Kullanıcı için yetkilendirilmiş kiracıları alır.</span><span class="sxs-lookup"><span data-stu-id="5ae21-132">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="5ae21-133">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5ae21-133">Import-AzureRmContext</span></span>](Import-AzureRmContext.md)
<span data-ttu-id="5ae21-134">Azure kimlik doğrulama bilgilerini dosyadan yükler.</span><span class="sxs-lookup"><span data-stu-id="5ae21-134">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="5ae21-135">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="5ae21-135">Remove-AzureRmAccount</span></span>](Remove-AzureRmAccount.md)
<span data-ttu-id="5ae21-136">Bu hesapla ilişkili tüm kimlik bilgilerini ve bağlamları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5ae21-136">Remove all credentials and contexts associated with this account.</span></span>

### [<span data-ttu-id="5ae21-137">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5ae21-137">Remove-AzureRmContext</span></span>](Remove-AzureRmContext.md)
<span data-ttu-id="5ae21-138">Kullanılabilir içerik kümesinden bağlam kaldırma</span><span class="sxs-lookup"><span data-stu-id="5ae21-138">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="5ae21-139">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="5ae21-139">Remove-AzureRmEnvironment</span></span>](Remove-AzureRmEnvironment.md)
<span data-ttu-id="5ae21-140">Belirli bir Azure örneğine bağlanmak için uç noktaları ve meta verileri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5ae21-140">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="5ae21-141">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5ae21-141">Rename-AzureRmContext</span></span>](Rename-AzureRmContext.md)
<span data-ttu-id="5ae21-142">Azure bağlamını yeniden adlandırma.</span><span class="sxs-lookup"><span data-stu-id="5ae21-142">Rename an Azure context.</span></span>  <span data-ttu-id="5ae21-143">Varsayılan olarak, Kullanıcı hesabı ve abonelikle adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="5ae21-143">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="5ae21-144">Resolve-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="5ae21-144">Resolve-AzureRmError</span></span>](Resolve-AzureRmError.md)
<span data-ttu-id="5ae21-145">Azure PowerShell hatalarının genişletilmiş ayrıntılarını içeren PowerShell hatalarıyla ilgili ayrıntılı bilgileri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="5ae21-145">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="5ae21-146">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5ae21-146">Save-AzureRmContext</span></span>](Save-AzureRmContext.md)
<span data-ttu-id="5ae21-147">Geçerli kimlik doğrulama bilgilerini diğer PowerShell oturumlarında kullanılmak üzere kaydeder.</span><span class="sxs-lookup"><span data-stu-id="5ae21-147">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="5ae21-148">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5ae21-148">Select-AzureRmContext</span></span>](Select-AzureRmContext.md)
<span data-ttu-id="5ae21-149">Azure PowerShell cmdlet 'lerinin hedef (veya hesap, kiracı) aboneliğini seçin</span><span class="sxs-lookup"><span data-stu-id="5ae21-149">Select a subscription to target (or account, tenant) in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="5ae21-150">Gönderme</span><span class="sxs-lookup"><span data-stu-id="5ae21-150">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="5ae21-151">Bir dizi Kılavuzlu istem aracılığıyla Azure PowerShell ekibine görüşler gönderir.</span><span class="sxs-lookup"><span data-stu-id="5ae21-151">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="5ae21-152">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="5ae21-152">Set-AzureRmContext</span></span>](Set-AzureRmContext.md)
<span data-ttu-id="5ae21-153">Cmdlet 'lerin geçerli oturumda kullanması için kiracı, abonelik ve ortamı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5ae21-153">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="5ae21-154">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="5ae21-154">Set-AzureRmEnvironment</span></span>](Set-AzureRmEnvironment.md)
<span data-ttu-id="5ae21-155">Azure ortamının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5ae21-155">Sets properties for an Azure environment.</span></span>

