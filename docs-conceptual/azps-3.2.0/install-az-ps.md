---
title: Azure PowerShell'i PowerShellGet ile yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 7f22a420068db87fa2c3c007bd36f515384162fb
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182239"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="23596-103">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="23596-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="23596-104">Bu makalede, PowerShellGet kullanarak Azure PowerShell modüllerini nasıl yükleyeceğiniz anlatılır.</span><span class="sxs-lookup"><span data-stu-id="23596-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="23596-105">Bu yönergeler Windows, macOS ve Linux platformlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="23596-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="23596-106">Az modülü için şu anda başka desteklenen yükleme metodu yoktur.</span><span class="sxs-lookup"><span data-stu-id="23596-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="23596-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="23596-107">Requirements</span></span>

<span data-ttu-id="23596-108">Azure PowerShell, Windows’da PowerShell 5.1 veya sonraki sürümleriyle veya tüm platformlarda PowerShell 6.x ve sonraki sürümleriyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="23596-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="23596-109">PowerShell'iniz olup olmadığından veya macOS mu yoksa Linux mı kullandığınızdan emin değilseniz, [PowerShell Core'un en son sürümünü yükleyin](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="23596-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="23596-110">PowerShell sürümünüzü denetlemek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="23596-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="23596-111">Azure PowerShell'i Windows üzerinde PowerShell 5.1'de çalıştırmak için:</span><span class="sxs-lookup"><span data-stu-id="23596-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="23596-112">Gerekirse [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)'e güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="23596-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="23596-113">Windows 10 kullanıyorsanız, zaten PowerShell 5.1 yüklüdür.</span><span class="sxs-lookup"><span data-stu-id="23596-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="23596-114">[.NET Framework 4.7.2 veya sonraki sürümünü](/dotnet/framework/install) yükleyin.</span><span class="sxs-lookup"><span data-stu-id="23596-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="23596-115">PowerShell Core kullanıldığında, Azure PowerShell için ek gereksinimler yoktur.</span><span class="sxs-lookup"><span data-stu-id="23596-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="23596-116">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="23596-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="23596-117">Windows için PowerShell 5.1'de aynı anda hem AzureRM hem de Az modülünü __yükleyemezsiniz__.</span><span class="sxs-lookup"><span data-stu-id="23596-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="23596-118">Sisteminizde AzureRM'yi kullanılabilir durumda tutmanız gerekiyorsa, PowerShell Core 6.x veya sonraki sürümleri için Az modülünü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="23596-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="23596-119">Bunu yapmak için [PowerShell Core 6.x veya sonraki sürümünü yükleyin](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) ve ardından PowerShell Core terminalinde bu yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="23596-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="23596-120">Önerilen yükleme yöntemi, yalnızca etkin kullanıcı için yüklemeye yöneliktir:</span><span class="sxs-lookup"><span data-stu-id="23596-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="23596-121">Sistemdeki tüm kullanıcılar için yüklemek istiyorsanız yönetici ayrıcalıkları gerekir.</span><span class="sxs-lookup"><span data-stu-id="23596-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="23596-122">Yükseltilmiş bir PowerShell oturumundan, yönetici olarak veya MacOS ya da Linux’taki `sudo` komutuyla çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="23596-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="23596-123">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="23596-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="23596-124">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="23596-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="23596-125">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="23596-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="23596-126">Az modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="23596-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="23596-127">Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="23596-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="23596-128">Çevrimdışı yükleme</span><span class="sxs-lookup"><span data-stu-id="23596-128">Install offline</span></span>

<span data-ttu-id="23596-129">Bazı ortamlarda PowerShell Galerisi'ne bağlanmak mümkün olmaz.</span><span class="sxs-lookup"><span data-stu-id="23596-129">In some environments it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="23596-130">Bu durumlarda yine de aşağıdaki yöntemlerden birini kullanarak çevrimdışı yükleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="23596-130">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="23596-131">Modülleri başka bir konuma indirin ve bu konumu ağınızda yükleme kaynağı olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="23596-131">Download the modules to another location and use that as an installation source on your network.</span></span> <span data-ttu-id="23596-132">Bu karmaşık bir işlem olabilir ama PowerShell modüllerini PowerShellGet ile bağlantısız sistemlere dağıtmak üzere tek sunucu veya dosya paylaşımında önbelleğe almanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="23596-132">This can be a complicated process, but will let you cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="23596-133">Yerel depoyu ayarlamayı ve bağlantısız sistemlerde yüklemeyi öğrenmek için [Yerel PowerShellGet depolarıyla çalışma](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) konusundan yararlanın.</span><span class="sxs-lookup"><span data-stu-id="23596-133">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="23596-134">Ağa bağlı bir makineye [Azure PowerShell MSI'yi indirin](install-az-ps-msi.md) ve sonra PowerShell Galerisi'ne erişimi olmayan sistemlere yükleyiciyi kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="23596-134">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="23596-135">MSI yükleyicisinin yalnızca Windows üzerinde PowerShell 5.1 için kullanılabildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="23596-135">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="23596-136">Modülü [Save-Module](/powershell/module/PowershellGet/Save-Module) ile bir dosya paylaşımına kaydedin veya başka bir konuma kaydedin ve sonra el ile diğer makinelere kopyalayın:</span><span class="sxs-lookup"><span data-stu-id="23596-136">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="23596-137">Sorun giderme</span><span class="sxs-lookup"><span data-stu-id="23596-137">Troubleshooting</span></span>

<span data-ttu-id="23596-138">Azure PowerShell modülünü yüklerken karşılaşılan yaygın sorunlardan bazıları burada verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="23596-138">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="23596-139">Burada listelenmeyen bir sorunla karşılaşırsanız, [github’da bir sorun oluşturun](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="23596-139">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="23596-140">Ara sunucu blokları bağlantısı</span><span class="sxs-lookup"><span data-stu-id="23596-140">Proxy blocks connection</span></span>

<span data-ttu-id="23596-141">`Install-Module` cmdlet'inden PowerShell Galerisi'ne ulaşılamadığını belirten hatalar alıyorsanız, bir ara sunucunun arkasında olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23596-141">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="23596-142">Sistem genelinde ara sunucu yapılandırma konusunda farklı işletim sistemlerinin farklı gereksinimleri olacaktır ve burada bunlar ayrıntılı olarak ele alınmamıştır.</span><span class="sxs-lookup"><span data-stu-id="23596-142">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="23596-143">Ara sunucu ayarlarınız ve işletim sisteminiz için bunları nasıl yapılandıracağınız konusunda sistem yöneticinize danışın.</span><span class="sxs-lookup"><span data-stu-id="23596-143">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="23596-144">PowerShell'in kendisi otomatik olarak bu ara sunucuyu kullanacak şekilde yapılandırılamaz.</span><span class="sxs-lookup"><span data-stu-id="23596-144">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="23596-145">PowerShell 5.1 ve sonraki sürümleriyle, aşağıdaki komutu kullanarak PowerShell oturumunda kullanılacak ara sunucuyu yapılandırın:</span><span class="sxs-lookup"><span data-stu-id="23596-145">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="23596-146">İşletim sistemi kimlik bilgileriniz doğru yapılandırıldıysa, bu işlem PowerShell isteklerini ara sunucu üzerinden yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="23596-146">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="23596-147">Bu ayarın oturumlar arasında kalıcı olmasını sağlamak için, komutu [PowerShell profiline](/powershell/module/microsoft.powershell.core/about/about_profiles) ekleyin.</span><span class="sxs-lookup"><span data-stu-id="23596-147">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="23596-148">Paketi yüklemek için ara sunucunuzun şu adrese yönelik HTTPS bağlantılarına izin vermesi gerekir:</span><span class="sxs-lookup"><span data-stu-id="23596-148">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="23596-149">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="23596-149">Sign in</span></span>

<span data-ttu-id="23596-150">Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="23596-150">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="23596-151">Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module Az` kullanarak modülü el ile içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="23596-151">If you've disabled module autoloading, manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="23596-152">Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.</span><span class="sxs-lookup"><span data-stu-id="23596-152">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="23596-153">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="23596-153">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="23596-154">Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="23596-154">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="23596-155">Azure PowerShell modülünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="23596-155">Update the Azure PowerShell module</span></span>

<span data-ttu-id="23596-156">Az modülünün paketlenme şeklinden dolayı, [Update-Module](/powershell/module/powershellget/update-module) komutu yüklemenizi doğru güncelleştirmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="23596-156">Because of how the Az module is packaged, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="23596-157">Az modülünü yüklediğinizde aslında her hizmet için cmdlet’leri sağlayan tüm bağımlı alt modüllerini toplar ve yükler.</span><span class="sxs-lookup"><span data-stu-id="23596-157">When you install the Az module, it actually collects and installs all of its dependent submodules, and which provide the cmdlets for each service.</span></span>
<span data-ttu-id="23596-158">Başka bir deyişle, Azure PowerShell modülünü güncelleştirmek için yalnızca __güncelleştirmek__ yerine __yeniden yüklemeniz__ gerekir.</span><span class="sxs-lookup"><span data-stu-id="23596-158">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="23596-159">Bu işlem yüklemeyle aynı şekilde yapılır ama `-Force` bağımsız değişkenini eklemeniz gerekebilir:</span><span class="sxs-lookup"><span data-stu-id="23596-159">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="23596-160">Bu yüklü modüllerin üzerine yazabilse de, sisteminizde yine de eski sürümler kalabilir.</span><span class="sxs-lookup"><span data-stu-id="23596-160">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="23596-161">Sisteminizdeki eski Azure PowerShell sürümlerini nasıl kaldıracağınızı öğrenmek için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="23596-161">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="23596-162">Azure PowerShell'in birden çok sürümünü kullanma</span><span class="sxs-lookup"><span data-stu-id="23596-162">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="23596-163">Azure PowerShell'in birden çok sürümünü yüklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="23596-163">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="23596-164">Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="23596-164">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="23596-165">Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="23596-165">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="23596-166">`-RequiredVersion` bağımsız değişkenini kullanarak `Az` modülünün belirli bir sürümünü yükleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="23596-166">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="23596-167">Modülün birden çok sürümünü yüklediyseniz, modül otomatik yükleme ve `Import-Module` tarafından varsayılan olarak en son sürüm yüklenir.</span><span class="sxs-lookup"><span data-stu-id="23596-167">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="23596-168">Geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="23596-168">Provide feedback</span></span>

<span data-ttu-id="23596-169">Azure Powershell’de bir hata bulursanız [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="23596-169">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="23596-170">Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="23596-170">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="23596-171">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="23596-171">Next Steps</span></span>

<span data-ttu-id="23596-172">Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="23596-172">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="23596-173">Azure PowerShell’i zaten biliyorsanız ve AzureRM’den geçiş yapmanız gerekiyorsa bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="23596-173">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
