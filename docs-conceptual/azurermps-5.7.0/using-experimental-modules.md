---
title: Deneysel Azure PowerShell modüllerini kullanma
description: Deneysel Azure PowerShell modüllerinin felsefesi ve kullanımı hakkında bilgi edinin.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: 4eb94644bb87e69ef6edc79d36189b453e45ecd0
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819975"
---
# <a name="using-experimental-azure-powershell-modules"></a><span data-ttu-id="b71ec-103">Deneysel Azure PowerShell modüllerini kullanma</span><span class="sxs-lookup"><span data-stu-id="b71ec-103">Using experimental Azure PowerShell modules</span></span>

<span data-ttu-id="b71ec-104">Azure PowerShell ekibi Azure’da geliştirici araçlarına (özellikle CLI’ler) vurgu yaparak Azure PowerShell deneyiminde çok sayıda geliştirmeyi denemektedir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="b71ec-105">Deneme yöntemi</span><span class="sxs-lookup"><span data-stu-id="b71ec-105">Experimentation methodology</span></span>

<span data-ttu-id="b71ec-106">Denemeyi kolaylaştırmak amacıyla, yeni ve kullanımı daha kolay yöntemlerle mevcut Azure SDK işlevselliğini uygulayan yeni Azure PowerShell modülleri oluşturuyoruz.</span><span class="sxs-lookup"><span data-stu-id="b71ec-106">To facilitate experimentation, we are creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="b71ec-107">Çoğu durumda, cmdlet'ler mevcut cmdlet'leri tam olarak yansıtır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="b71ec-108">Ancak, deneysel cmdlet’ler Azure kaynaklarını oluşturup yönetmeyi kolaylaştıran kısa bir gösterim ve daha akıllı varsayılan değerler sağlar.</span><span class="sxs-lookup"><span data-stu-id="b71ec-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="b71ec-109">Bu modüller mevcut Azure PowerShell modülleri ile yan yana yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-109">These modules can be installed side-by-side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="b71ec-110">Cmdlet adları, daha kısa adlar sağlamak ve deneysel olmayan mevcut cmdlet'lerle ad çakışmalarını önlemek için kısaltılmıştır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="b71ec-111">Deneysel modüller şu adlandırma kuralını kullanır: `AzureRM.*.Experiments`.</span><span class="sxs-lookup"><span data-stu-id="b71ec-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="b71ec-112">Bu adlandırma kuralı, Önizleme modüllerinin adlandırması ile benzerdir: `AzureRM.*.Preview`.</span><span class="sxs-lookup"><span data-stu-id="b71ec-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="b71ec-113">Önizleme modülleri, deneysel modüllerden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="b71ec-114">Önizleme modüller, Azure hizmetlerinin yalnızca Önizleme teklifi olarak kullanılabilen yeni işlevlerini uygular.</span><span class="sxs-lookup"><span data-stu-id="b71ec-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="b71ec-115">Önizleme modülleri, mevcut Azure PowerShell modüllerinin yerine geçer ve aynı cmdlet ve parametre adlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="b71ec-116">Deneysel modül yükleme</span><span class="sxs-lookup"><span data-stu-id="b71ec-116">How to install an experimental module</span></span>

<span data-ttu-id="b71ec-117">Deneysel modüller, tıpkı mevcut Azure PowerShell modülleri gibi PowerShell Galerisinde yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="b71ec-118">Deneysel modüllerin listesini görüntülemek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="b71ec-118">To see a list of experimental modules, run the following command:</span></span>

```powershell
Find-Module AzureRM.*.Experiments
```

```Output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="b71ec-119">Deneysel modülü yüklemek için, yükseltilmiş bir PowerShell oturumunda aşağıdaki komutları kullanın:</span><span class="sxs-lookup"><span data-stu-id="b71ec-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```powershell
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="b71ec-120">Belgeler ve destek</span><span class="sxs-lookup"><span data-stu-id="b71ec-120">Documentation and support</span></span>

<span data-ttu-id="b71ec-121">Belgeler yükleme paketine dahildir ve `Get-Help` cmdlet'i kullanılarak belgelere erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="b71ec-122">Deneysel modüller için resmi bir belge yayımlanmaz.</span><span class="sxs-lookup"><span data-stu-id="b71ec-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="b71ec-123">Bu modülleri test etmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="b71ec-123">We encourage you to test these modules.</span></span> <span data-ttu-id="b71ec-124">Görüşleriniz, kullanılabilirliği artırmamıza ve gereksinimlerinizi karşılamamıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="b71ec-125">Ancak, deneysel oldukları için, bu modüllere yönelik destek sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="b71ec-126">GitHub deposunda bir [sorun](https://github.com/Azure/azure-powershell/issues) oluşturularak sorunlar ya da sorun raporları gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="b71ec-127">Denemeler ve geliştirilecek alanlar</span><span class="sxs-lookup"><span data-stu-id="b71ec-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="b71ec-128">Bu geliştirmeler, rakip ürünlerindeki başlıca ayırt edici özelliklere göre seçilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="b71ec-129">Örneğin, Azure CLI 2.0, komutları _API yüzey alanı_ yerine _senaryolara_ dayandırmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="b71ec-130">Azure CLI 2.0, "kullanmaya başlama" senaryolarını son kullanıcılar için kolaylaştıran birkaç akıllı varsayılan değer kullanır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="b71ec-131">Temel iyileştirmeler</span><span class="sxs-lookup"><span data-stu-id="b71ec-131">Core improvements</span></span>

<span data-ttu-id="b71ec-132">Temel iyileştirmeler, "sağduyu" olarak kabul edilir ve bu güncelleştirmelerin uygulamaya geçirilmesi için az miktarda deneme gerekir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="b71ec-133">Senaryoya Dayalı Cmdlet’ler - \**All*- cmdlet’leri Azure REST hizmeti değil, senaryolar çevresinde tasarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-133">Scenario-based Cmdlets - \**All*- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="b71ec-134">Daha Kısa Adları - Cmdlet'lerin adlarını (örneğin, `New-AzureRmVM` => `New-AzVm`) ve parametrelerin adlarını (örneğin, `-ResourceGroupName` => `-Rg`) içerir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="b71ec-135">"Eski" cmdlet’lerle uyumluluk için diğer adları kullanın.</span><span class="sxs-lookup"><span data-stu-id="b71ec-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="b71ec-136">_Geriye doğru uyumlu_ parametre kümeleri sağlayın.</span><span class="sxs-lookup"><span data-stu-id="b71ec-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="b71ec-137">Akıllı Varsayılanlar - "Gerekli" bilgileri doldurmak için akıllı varsayılanlar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b71ec-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="b71ec-138">Örnek:</span><span class="sxs-lookup"><span data-stu-id="b71ec-138">For example:</span></span>
  - <span data-ttu-id="b71ec-139">Kaynak Grubu</span><span class="sxs-lookup"><span data-stu-id="b71ec-139">Resource Group</span></span>
  - <span data-ttu-id="b71ec-140">Konum</span><span class="sxs-lookup"><span data-stu-id="b71ec-140">Location</span></span>
  - <span data-ttu-id="b71ec-141">Bağımlı kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b71ec-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="b71ec-142">Deneysel geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="b71ec-142">Experimental improvements</span></span>

<span data-ttu-id="b71ec-143">Deneysel geliştirmeler, takımın deneme ile doğrulamayı istediği önemli bir değişikliği sunar.</span><span class="sxs-lookup"><span data-stu-id="b71ec-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="b71ec-144">Basit türler - Oluşturma senaryoları, karmaşık türlerden ve yapılandırma nesnelerinden uzaklaşmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="b71ec-145">Yapılandırmayı bir veya iki parametreye kadar basitleştirin.</span><span class="sxs-lookup"><span data-stu-id="b71ec-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="b71ec-146">"Akıllı Oluştur" - "Akıllı Oluşturma" özelliğini uygulayan oluşturma senaryolarında _hiçbir_ gerekli parametre yoktur: tüm gerekli bilgiler, Azure PowerShell tarafından sabit bir fikirle seçilir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="b71ec-147">Gri Parametreler - Çoğu durumda, bazı parametreler "gri" veya yarı isteğe bağlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="b71ec-148">Parametre belirtilmezse, kullanıcıya parametrenin oluşturulmasını isteyip istemediği sorulur.</span><span class="sxs-lookup"><span data-stu-id="b71ec-148">If the parameter is not specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="b71ec-149">Ayrıca, gri parametrelerin kullanıcı onayıyla bağlama dayalı bir değer çıkarması anlamlıdır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="b71ec-150">Örneğin, gri parametrenin en son kullanılan değeri kullanması mantıklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="b71ec-151">`-Auto` Anahtarı - `-Auto` anahtarı, kullanıcılar için ana yoldaki gerekli parametrelerin bütünlüğünü sürdürürken _her şeyi varsayılan yapmayı_ "kabul etme" seçeneği sunar.</span><span class="sxs-lookup"><span data-stu-id="b71ec-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="b71ec-152">Özelliğe özgü anahtarlar</span><span class="sxs-lookup"><span data-stu-id="b71ec-152">Feature-specific switches</span></span>

<span data-ttu-id="b71ec-153">Örneğin, "Web uygulaması oluşturma" senaryosunda mevcut bir git deposuna bir "azure" uzak birimini otomatik olarak ekleyen `-Git` veya `-AddRemote` olabilir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="b71ec-154">Ayarlanabilir Varsayılanlar - Kullanıcılar `-ResourceGroupName` ve `-Location` gibi bazı yaygın parametrelerin varsayılan değerlerini ayarlayabilmelidir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-154">Settable Defaults - Users should have the ability to default certain ubiquitous parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="b71ec-155">Boyut Varsayılanları - Birçok Kaynak Sağlayıcısı farklı adlar kullandığından, kaynak "boyutları" kafa karıştırıcı olabilir (örneğin, "Standard\_DS1\_v2" veya "S1").</span><span class="sxs-lookup"><span data-stu-id="b71ec-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="b71ec-156">Bununla birlikte, çoğu kullanıcı daha çok maliyetle ilgilenir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-156">However, most users care more about cost.</span></span> <span data-ttu-id="b71ec-157">Bu nedenle, bir fiyatlandırma zamanlamasına göre "evrensel" boyutlar tanımlamak mantıklıdır.</span><span class="sxs-lookup"><span data-stu-id="b71ec-157">Therefore, it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="b71ec-158">Kullanıcılar belirli bir boyutu seçebilir veya bütçe kaynağına göre _en iyi seçeneği_ Azure PowerShell’in seçmesine izin verebilir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="b71ec-159">Çıktı Biçimi - Azure PowerShell şu anda `PSObject` döndürmektedir ve çok az konsol çıktısı mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="b71ec-159">Output Format - Azure PowerShell currently returns `PSObject`s and there is little console output.</span></span> <span data-ttu-id="b71ec-160">Azure PowerShell’in kullanılan "akıllı varsayılanlar" ile ilgili bazı bilgileri kullanıcıya göstermesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="b71ec-160">Azure PowerShell may need to display some information to the user regarding the "smart defaults" used.</span></span>
