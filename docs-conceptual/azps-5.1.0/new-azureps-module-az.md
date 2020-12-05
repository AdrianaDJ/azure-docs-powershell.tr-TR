---
title: Azure Az PowerShell modülüne giriş
description: AzureRM PowerShell modülünün yerine gelen ve Azure ile etkileşim kurmak için önerilen Az PowerShell modülüne giriş.
ms.date: 12/1/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: a3b74531ff71ed0e9ac473831b71efb6f29d6e66
ms.sourcegitcommit: 7887e040bdeb2f55c035a3169cd0d9d807ab186e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2020
ms.locfileid: "96536553"
---
# <a name="introducing-the-azure-az-powershell-module"></a><span data-ttu-id="6c8b6-103">Azure Az PowerShell modülüne giriş</span><span class="sxs-lookup"><span data-stu-id="6c8b6-103">Introducing the Azure Az PowerShell module</span></span>

## <a name="overview"></a><span data-ttu-id="6c8b6-104">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="6c8b6-104">Overview</span></span>

<span data-ttu-id="6c8b6-105">Az PowerShell modülü, Azure kaynaklarını doğrudan PowerShell’den yönetmeye yönelik bir dizi cmdlet’ten oluşur.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-105">The Az PowerShell module is a set of cmdlets for managing Azure resources directly from PowerShell.</span></span> <span data-ttu-id="6c8b6-106">PowerShell, bir CI/CD işlem hattı bağlamındakiler gibi örneklere yönelik Azure kaynaklarınızın yönetilmesi için kullanılabilen güçlü otomasyon özellikleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-106">PowerShell provides powerful features for automation that can be leveraged for managing your Azure resources for examples in the context of a CI/CD pipeline.</span></span>

<span data-ttu-id="6c8b6-107">AzureRM’nin yerini alan Az PowerShell modülü, Azure ile etkileşim kurmak için kullanılması önerilen sürümdür.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-107">The Az PowerShell module is the replacement of AzureRM and is the recommended version to use for interacting with Azure.</span></span>

<span data-ttu-id="6c8b6-108">Az PowerShell modülünü aşağıdaki yöntemlerden biriyle kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6c8b6-108">You can use the Az PowerShell module with one of the following methods:</span></span>

* <span data-ttu-id="6c8b6-109">[Az PowerShell modülünü PowerShellGet aracılığıyla yükleme](install-az-ps.md) (önerilen seçenek).</span><span class="sxs-lookup"><span data-stu-id="6c8b6-109">[Install the Az PowerShell module via PowerShellGet](install-az-ps.md) (recommended option).</span></span>
* <span data-ttu-id="6c8b6-110">[Az PowerShell modülünü MSI ile yükleme](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="6c8b6-110">[Install the Az PowerShell module with MSI](install-az-ps-msi.md).</span></span>
* <span data-ttu-id="6c8b6-111">[Azure Cloud Shell’i kullanma](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="6c8b6-111">[Use Azure Cloud Shell](/azure/cloud-shell/overview).</span></span>
* <span data-ttu-id="6c8b6-112">[Az PowerShell Docker kapsayıcısını kullanma](azureps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="6c8b6-112">[Use the Az PowerShell Docker container](azureps-in-docker.md).</span></span>

## <a name="features"></a><span data-ttu-id="6c8b6-113">Özellikler</span><span class="sxs-lookup"><span data-stu-id="6c8b6-113">Features</span></span>

<span data-ttu-id="6c8b6-114">Az PowerShell modülü şu avantajları sunar:</span><span class="sxs-lookup"><span data-stu-id="6c8b6-114">The Az PowerShell module features the following benefits:</span></span>

* <span data-ttu-id="6c8b6-115">Güvenlik ve kararlılık</span><span class="sxs-lookup"><span data-stu-id="6c8b6-115">Security and stability</span></span>
  * <span data-ttu-id="6c8b6-116">Belirteç önbelleği şifrelemesi</span><span class="sxs-lookup"><span data-stu-id="6c8b6-116">Token cache encryption</span></span>
  * <span data-ttu-id="6c8b6-117">ADFS 2019 için destek</span><span class="sxs-lookup"><span data-stu-id="6c8b6-117">Support for ADFS 2019</span></span>
  * <span data-ttu-id="6c8b6-118">Ortadaki adam saldırısı türlerini engelleyen güvenlik mekanizması</span><span class="sxs-lookup"><span data-stu-id="6c8b6-118">Security mechanism preventing man-in-the-middle attack types</span></span>
  * <span data-ttu-id="6c8b6-119">Sürekli erişim değerlendirmesi gibi özellikler için destek (2021’de sunulacak)</span><span class="sxs-lookup"><span data-stu-id="6c8b6-119">Support for features like continuous access evaluation (coming in 2021)</span></span>
* <span data-ttu-id="6c8b6-120">Tüm Azure hizmetleri için destek</span><span class="sxs-lookup"><span data-stu-id="6c8b6-120">Support for all Azure services</span></span>
  * <span data-ttu-id="6c8b6-121">Her Azure hizmeti için bir modül sunulur</span><span class="sxs-lookup"><span data-stu-id="6c8b6-121">A module is available for each Azure service</span></span>
  * <span data-ttu-id="6c8b6-122">AzureRM’den sonra yapılan birçok hata düzeltmesi ve API sürümü yükseltmeleri</span><span class="sxs-lookup"><span data-stu-id="6c8b6-122">Multiple bug fixes and API version upgrades since AzureRM</span></span>
* <span data-ttu-id="6c8b6-123">Birkaç ek yeni özellik</span><span class="sxs-lookup"><span data-stu-id="6c8b6-123">Several additional new capabilities</span></span>
  * <span data-ttu-id="6c8b6-124">Cloud Shell için ve platformlar arası destek</span><span class="sxs-lookup"><span data-stu-id="6c8b6-124">Support in Cloud Shell and cross-platform</span></span>
  * <span data-ttu-id="6c8b6-125">Azure kaynaklarına erişmek için erişim belirteci alınıp kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="6c8b6-125">Can get and use access token to access Azure resources</span></span>
  * <span data-ttu-id="6c8b6-126">Kaçış noktası türü işlemler için genel Az cmdlet’i</span><span class="sxs-lookup"><span data-stu-id="6c8b6-126">Generic Az cmdlet for escape hatch type operations</span></span>

> [!NOTE]
> <span data-ttu-id="6c8b6-127">PowerShell 7 ve üzeri, tüm platformlarda Az PowerShell ile kullanılması önerilen PowerShell sürümüdür.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-127">PowerShell 7 and later is the recommended version of PowerShell for use with Az PowerShell on all platforms.</span></span>

<span data-ttu-id="6c8b6-128">.NET Standard kitaplığını temel alan Az PowerShell modülü Windows, macOS ve Linux dahil tüm platformlarda PowerShell 7 ve üzeri sürümlerle birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-128">The Az PowerShell module is based on the .NET Standard library and works with PowerShell 7 and later on all platforms including Windows, macOS, and Linux.</span></span> <span data-ttu-id="6c8b6-129">Ayrıca Windows PowerShell 5.1 ile de uyumludur.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-129">It's also compatible with Windows PowerShell 5.1.</span></span>

<span data-ttu-id="6c8b6-130">Azure desteğini tüm platformlara getirmek için çalışıyoruz. Tüm Az PowerShell modülleri platformlar arası kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-130">We're committed to bringing Azure support to all platforms and all Az PowerShell modules are cross-platforms.</span></span>

## <a name="upgrade-your-environment-to-az"></a><span data-ttu-id="6c8b6-131">Ortamınızı Az’ye yükseltin</span><span class="sxs-lookup"><span data-stu-id="6c8b6-131">Upgrade your environment to Az</span></span>

<span data-ttu-id="6c8b6-132">PowerShell'de en son Azure özelliklerine sahip olmak için Az modülüne geçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-132">To keep up with the latest Azure features in PowerShell, you should migrate to the Az module.</span></span> <span data-ttu-id="6c8b6-133">AzureRM yerine Az modülünü yüklemeye hazır değilseniz, Az modülünü denemek için çeşitli seçenekleriniz vardır:</span><span class="sxs-lookup"><span data-stu-id="6c8b6-133">If you're not ready to install the Az module as a replacement for AzureRM, you have a couple of options available to experiment with Az:</span></span>

* <span data-ttu-id="6c8b6-134">[Azure Cloud Shell](/azure/cloud-shell/overview) ile bir `PowerShell` ortamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-134">Use a `PowerShell` environment with [Azure Cloud Shell](/azure/cloud-shell/overview).</span></span> <span data-ttu-id="6c8b6-135">Azure Cloud Shell, Az modülü yüklenmiş ve `Enable-AzureRM` uyumluluk diğer adları etkinleştirilmiş olarak gelen tarayıcı tabanlı bir kabuk ortamıdır.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-135">Azure Cloud Shell is a browser-based shell environment that comes with the Az module installed and `Enable-AzureRM` compatibility aliases enabled.</span></span>
* <span data-ttu-id="6c8b6-136">Windows PowerShell 5.1’de AzureRM modülünü yüklü bırakın ve PowerShell 7 veya sonraki sürümlerde Az modülünü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-136">Keep the AzureRM module installed in Windows PowerShell 5.1 and install the Az module in PowerShell 7 or later.</span></span> <span data-ttu-id="6c8b6-137">Windows PowerShell 5.1 ile PowerShell 7 ve üzeri, ayrı modül koleksiyonları kullanır.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-137">Windows PowerShell 5.1 and PowerShell 7 and later use separate collections of modules.</span></span> <span data-ttu-id="6c8b6-138">Yönergeleri izleyerek [PowerShell’in en son sürümünü](/powershell/scripting/install/installing-powershell) yükleyin ve ardından PowerShell 7 veya üzeri bir sürümden [Az modülünü yükleyin](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="6c8b6-138">Follow the instructions to install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) and then [install the Az module](install-az-ps.md) from PowerShell 7 or later.</span></span>

<span data-ttu-id="6c8b6-139">Mevcut AzureRM yüklemesinden yükseltmek için:</span><span class="sxs-lookup"><span data-stu-id="6c8b6-139">To upgrade from an existing AzureRM install:</span></span>

1. [<span data-ttu-id="6c8b6-140">Azure PowerShell AzureRM modülünü kaldırın</span><span class="sxs-lookup"><span data-stu-id="6c8b6-140">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [<span data-ttu-id="6c8b6-141">Azure PowerShell Az modülünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="6c8b6-141">Install the Azure PowerShell Az module</span></span>](install-az-ps.md)
1. <span data-ttu-id="6c8b6-142">**İSTEĞE BAĞLI**: Yeni komut kümesine alışırken [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) ile AzureRM cmdlet’lerine yönelik diğer adları eklemek için uyumluluk modunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-142">**OPTIONAL**: Enable compatibility mode to add aliases for AzureRM cmdlets with [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) while you become familiar with the new command set.</span></span> <span data-ttu-id="6c8b6-143">Daha fazla bilgi için sonraki bölüme veya [AzureRM'den Az’ye geçişi başlatma](migrate-from-azurerm-to-az.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-143">For more information, see the next section or [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a><span data-ttu-id="6c8b6-144">Mevcut betikleri AzureRM’den Az’ye geçirme</span><span class="sxs-lookup"><span data-stu-id="6c8b6-144">Migrate existing scripts from AzureRM to Az</span></span>

<span data-ttu-id="6c8b6-145">Hala AzureRM modülünü temel alan betiklerinizin geçişini gerçekleştirmenize yardımcı olacak birkaç kaynak hazırladık:</span><span class="sxs-lookup"><span data-stu-id="6c8b6-145">If your scripts are still based on the AzureRM module, we have several resources to help you with the migration:</span></span>

* [<span data-ttu-id="6c8b6-146">AzureRM'den Az modülüne geçişi başlatma</span><span class="sxs-lookup"><span data-stu-id="6c8b6-146">Get started with migration from AzureRM to Az</span></span>](migrate-from-azurerm-to-az.md)
* [<span data-ttu-id="6c8b6-147">AzureRM'den Az 1.0.0'a geçişte hataya neden olan değişikliklerin tam listesi</span><span class="sxs-lookup"><span data-stu-id="6c8b6-147">Full list of breaking changes from AzureRM to Az 1.0.0</span></span>](migrate-az-1.0.0.md)
* <span data-ttu-id="6c8b6-148">[Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet'i</span><span class="sxs-lookup"><span data-stu-id="6c8b6-148">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet</span></span>

## <a name="supportability"></a><span data-ttu-id="6c8b6-149">Desteklenebilirlik</span><span class="sxs-lookup"><span data-stu-id="6c8b6-149">Supportability</span></span>

<span data-ttu-id="6c8b6-150">Az, Azure için en güncel PowerShell modülüdür.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-150">Az is the most current PowerShell module for Azure.</span></span> <span data-ttu-id="6c8b6-151">Sorunları veya özellik isteklerini doğrudan [GitHub deposunda](https://github.com/Azure/azure-powershell) girebilir veya destek sözleşmeniz varsa Microsoft desteği aracılığıyla iletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-151">Issues or feature requests can be logged directly on the [GitHub repository](https://github.com/Azure/azure-powershell), or via Microsoft support if you have a support contract.</span></span> <span data-ttu-id="6c8b6-152">Özellik istekleri Az’nin en son sürümünde uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-152">Feature requests will be implemented in the latest version of Az.</span></span> <span data-ttu-id="6c8b6-153">Kritik sorunların çözümleri Az’nin son iki sürümünde uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-153">Critical issues will be implemented on the last two versions of Az.</span></span>

<span data-ttu-id="6c8b6-154">AzureRM için artık yeni cmdlet’ler veya özellikler sağlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-154">AzureRM will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="6c8b6-155">Bununla birlikte, AzureRM modülü hala resmi olarak bakım kapsamındadır ve Şubat 2020’ye kadar kritik düzeltmeleri alacaktır.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-155">However, the AzureRM module is still officially maintained and will receive critical fixes through February 2020.</span></span>

## <a name="data-collection"></a><span data-ttu-id="6c8b6-156">Veri toplama</span><span class="sxs-lookup"><span data-stu-id="6c8b6-156">Data collection</span></span>

<span data-ttu-id="6c8b6-157">Azure PowerShell varsayılan olarak telemetri verilerini toplar.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-157">Azure PowerShell collects telemetry data by default.</span></span> <span data-ttu-id="6c8b6-158">Microsoft, yaygın sorunları belirlemek ve Azure PowerShell deneyimini geliştirmek amacıyla kullanım desenlerini belirlemek için toplanan verileri kümeler.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-158">Microsoft aggregates collected data to identify patterns of usage to identify common issues and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="6c8b6-159">Microsoft Azure PowerShell özel veya kişisel verileri toplamaz.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-159">Microsoft Azure PowerShell does not collect any private or personal data.</span></span> <span data-ttu-id="6c8b6-160">Örneğin, kullanım verileri, düşük başarı oranına sahip cmdlet’ler gibi sorunların tanımlanmasına ve çalışmalarımızın önceliğinin belirlenmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-160">For example, the usage data helps identify issues such as cmdlets with low success and helps prioritize our work.</span></span>

<span data-ttu-id="6c8b6-161">Bu verilerin sağladığı içgörüler bizim için önemli olsa da herkesin kullanım verilerini göndermek istemeyebileceğini de anlıyoruz.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-161">While we appreciate the insights this data provides, we also understand that not everyone wants to send usage data.</span></span> <span data-ttu-id="6c8b6-162">Veri toplama işlemini [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) cmdlet’iyle devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-162">You can disable data collection with the [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) cmdlet.</span></span> <span data-ttu-id="6c8b6-163">Daha fazla bilgi edinmek için [gizlilik bildirimimizi](https://privacy.microsoft.com/privacystatement) de okuyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c8b6-163">You can also read our [privacy statement](https://privacy.microsoft.com/privacystatement) to learn more.</span></span>
