---
title: Azure PowerShell'i PowerShellGet ile yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/14/2020
ms.openlocfilehash: caa0c2fbba8b8b7e07424481360a60f3da163e66
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566551"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="1a2ab-103">Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="1a2ab-103">Install Azure PowerShell</span></span>

<span data-ttu-id="1a2ab-104">Bu makalede, [PowerShellGet](/powershell/scripting/gallery/installing-psget) kullanarak Azure PowerShell modüllerinin nasıl yüklendiği ele alınır.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="1a2ab-105">Bu yönergeler Windows, macOS ve Linux platformlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="1a2ab-106">Azure PowerShell, Azure [Cloud Shell](/azure/cloud-shell/overview)’de de sunulur ve şimdi, [Docker görüntülerine](azureps-in-docker.md) önceden yüklenir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview) and is now preinstalled in [Docker images](azureps-in-docker.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a2ab-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="1a2ab-107">Requirements</span></span>

> [!NOTE]
> <span data-ttu-id="1a2ab-108">PowerShell 7.x ve üzeri, tüm platformlarda Azure PowerShell ile kullanılması önerilen PowerShell sürümüdür.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-108">PowerShell 7.x and later is the recommended version of PowerShell for use with Azure PowerShell on all platforms.</span></span>

<span data-ttu-id="1a2ab-109">Azure PowerShell tüm platformlarda PowerShell 6.2.4 ve üzeri sürümlerle birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-109">Azure PowerShell works with PowerShell 6.2.4 and later on all platforms.</span></span> <span data-ttu-id="1a2ab-110">Ayrıca Windows üzerinde PowerShell 5.1 ile de desteklenir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-110">It is also supported with PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="1a2ab-111">İşletim sisteminiz için sunulan [en son PowerShell sürümünü](/powershell/scripting/install/installing-powershell) yükleyin.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-111">Install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="1a2ab-112">PowerShell 6.2.4 ve üzerinde çalıştırıldığında Azure PowerShell için ek gereksinim yoktur.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-112">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="1a2ab-113">PowerShell sürümünüzü denetlemek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-113">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="1a2ab-114">Azure PowerShell’i Windows üzerinde PowerShell 5.1’de kullanmak için:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-114">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="1a2ab-115">[Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell)’e güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-115">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="1a2ab-116">Windows 10 sürüm 1607 veya üzeri sürümü kullanıyorsanız, zaten PowerShell 5.1 yüklüdür.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-116">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="1a2ab-117">[.NET Framework 4.7.2 veya sonraki sürümünü](/dotnet/framework/install) yükleyin.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-117">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="1a2ab-118">En son PowerShellGet sürümünü kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-118">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="1a2ab-119">`Install-Module -Name PowerShellGet -Force` öğesini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-119">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="1a2ab-120">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="1a2ab-120">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="1a2ab-121">Windows üzerinde PowerShell 5.1’de aynı anda hem AzureRM hem de Az modülünün yüklenmesi desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-121">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="1a2ab-122">Sisteminizde AzureRM'yi kullanılabilir durumda tutmanız gerekiyorsa, PowerShell 6.2.4 veya sonraki sürümleri için Az modülünü yükleyin.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-122">If you need to keep AzureRM available on your system, install the Az module for PowerShell 6.2.4 or later.</span></span>

<span data-ttu-id="1a2ab-123">PowerShellGet cmdlet’lerinin kullanılması, tercih edilen yükleme yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-123">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="1a2ab-124">Az modülünü yalnızca geçerli kullanıcı için yükleyin.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-124">Install the Az module for the current user only.</span></span> <span data-ttu-id="1a2ab-125">Bu, önerilen yükleme kapsamıdır.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-125">This is the recommended installation scope.</span></span> <span data-ttu-id="1a2ab-126">Bu yöntem Windows, macOS ve Linux platformlarında aynı şekilde çalışır.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-126">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="1a2ab-127">Bir PowerShell oturumunda aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-127">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="1a2ab-128">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-128">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="1a2ab-129">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-129">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="1a2ab-130">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-130">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="1a2ab-131">Modülün bir sistemdeki tüm kullanıcılar için yüklenmesi, yükseltilmiş ayrıcalıklar gerektirir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-131">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="1a2ab-132">Windows’ta **Yönetici olarak çalıştır** seçeneğini kullanarak ya da macOS veya Linux’ta `sudo` komutunu kullanarak PowerShell oturumunu başlatın:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-132">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="1a2ab-133">Az modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-133">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1a2ab-134">Bunu yüklediğinizde genel olarak kullanılabilir durumdaki tüm Az PowerShell modülleri indirilir ve cmdlet'leri kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-134">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="1a2ab-135">Çevrimdışı yükleme</span><span class="sxs-lookup"><span data-stu-id="1a2ab-135">Install offline</span></span>

<span data-ttu-id="1a2ab-136">Bazı ortamlarda PowerShell Galerisi'ne bağlanmak mümkün olmaz.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-136">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="1a2ab-137">Bu durumlarda yine de aşağıdaki yöntemlerden birini kullanarak çevrimdışı yükleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-137">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="1a2ab-138">Modülleri ağınızdaki başka bir konuma indirin ve bu konumu yükleme kaynağı olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-138">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="1a2ab-139">Bu yöntem, PowerShell modüllerini PowerShellGet ile bağlantısız sistemlere dağıtmak üzere tek sunucuda veya dosya paylaşımında önbelleğe almanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-139">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="1a2ab-140">Yerel depoyu ayarlamayı ve bağlantısız sistemlerde yüklemeyi öğrenmek için [Yerel PowerShellGet depolarıyla çalışma](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) konusundan yararlanın.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-140">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="1a2ab-141">Ağa bağlı bir makineye [Azure PowerShell MSI'yi indirin](install-az-ps-msi.md) ve sonra PowerShell Galerisi'ne erişimi olmayan sistemlere yükleyiciyi kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-141">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="1a2ab-142">MSI yükleyicisinin yalnızca Windows üzerinde PowerShell 5.1 için kullanılabildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-142">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="1a2ab-143">Modülü [Save-Module](/powershell/module/PowershellGet/Save-Module) ile bir dosya paylaşımına kaydedin veya başka bir konuma kaydedin ve sonra el ile diğer makinelere kopyalayın:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-143">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="1a2ab-144">Sorun giderme</span><span class="sxs-lookup"><span data-stu-id="1a2ab-144">Troubleshooting</span></span>

<span data-ttu-id="1a2ab-145">Azure PowerShell modülünü yüklerken karşılaşılan yaygın sorunlardan bazıları burada verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-145">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="1a2ab-146">Burada listelenmeyen bir sorunla karşılaşırsanız [GitHub’da bir sorun oluşturun](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="1a2ab-146">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="1a2ab-147">Ara sunucu blokları bağlantısı</span><span class="sxs-lookup"><span data-stu-id="1a2ab-147">Proxy blocks connection</span></span>

<span data-ttu-id="1a2ab-148">`Install-Module` cmdlet'inden PowerShell Galerisi'ne ulaşılamadığını belirten hatalar alıyorsanız, bir ara sunucunun arkasında olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-148">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="1a2ab-149">Farklı işletim sistemlerinin ve ağ ortamlarının sistem genelinde ara sunucu yapılandırmaya ilişkin gereksinimleri farklıdır.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-149">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="1a2ab-150">Ara sunucu ayarlarınız ve ortamınızda bunları nasıl yapılandıracağınız konusunda sistem yöneticinize danışın.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-150">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="1a2ab-151">PowerShell'in kendisi otomatik olarak bu ara sunucuyu kullanacak şekilde yapılandırılamaz.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-151">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="1a2ab-152">Aşağıdaki komutları kullanarak PowerShell 5.1 ve sonraki sürümlerinde PowerShell oturumunu bir ara sunucu kullanacak şekilde yapılandırın:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-152">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="1a2ab-153">İşletim sistemi kimlik bilgileriniz doğru yapılandırıldıysa, bu yapılandırma PowerShell isteklerini ara sunucu üzerinden yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-153">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="1a2ab-154">Bu ayarın oturumlar arasında kalıcı olmasını sağlamak için, komutu [PowerShell profilinize](/powershell/module/microsoft.powershell.core/about/about_profiles) ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-154">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="1a2ab-155">Paketi yüklemek için ara sunucunuzun şu adrese yönelik HTTPS bağlantılarına izin vermesi gerekir:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-155">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="1a2ab-156">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="1a2ab-156">Sign in</span></span>

<span data-ttu-id="1a2ab-157">Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-157">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="1a2ab-158">Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module -Name Az` kullanarak modülü el ile içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-158">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="1a2ab-159">Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-159">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="1a2ab-160">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-160">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1a2ab-161">Azure oturum açma bilgilerinizin PowerShell oturumları arasında kalıcı hale getirilmesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumları arasında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ab-161">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="1a2ab-162">Azure PowerShell modülünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1a2ab-162">Update the Azure PowerShell module</span></span>

<span data-ttu-id="1a2ab-163">Bir PowerShell modülünü güncelleştirmek için modülü yüklerken kullandığınız yöntemi kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-163">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="1a2ab-164">Örneğin, ilk olarak `Install-Module` kullandıysanız en son sürümü edinmek için [Update-Module](/powershell/module/powershellget/update-module) kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-164">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="1a2ab-165">İlk olarak MSI paketini kullandıysanız yeni MSI paketini indirip yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-165">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="1a2ab-166">PowerShellGet cmdlet’leri bir MSI paketinden yüklenen modülleri güncelleştiremez.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-166">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="1a2ab-167">MSI paketleri PowerShellGet kullanılarak yüklenen modülleri güncelleştirmez.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-167">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="1a2ab-168">PowerShellGet kullanarak güncelleştirmeyle sorunlarıyla karşılaşıyorsanız **güncelleştirmek** yerine **yeniden yüklemeniz** gerekir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-168">If you have any issues updating using PowershellGet, then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="1a2ab-169">Yeniden yükleme, yükleme ile aynı şekilde yapılır ancak `-Force` parametresini eklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-169">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="1a2ab-170">MSI tabanlı yüklemelerin aksine, PowerShellGet kullanarak yükleme veya güncelleştirme yapmanız, sisteminizde bulunan eski sürümleri kaldırmaz.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-170">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="1a2ab-171">Sisteminizdeki eski Azure PowerShell sürümlerini kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ab-171">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="1a2ab-172">MSI tabanlı yüklemeler hakkında daha fazla bilgi edinmek için bkz. [MSI ile Azure PowerShell’i yükleme](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ab-172">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="1a2ab-173">Azure PowerShell'in birden çok sürümünü kullanma</span><span class="sxs-lookup"><span data-stu-id="1a2ab-173">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="1a2ab-174">Azure PowerShell'in birden çok sürümünü yüklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-174">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="1a2ab-175">Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-175">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="1a2ab-176">Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ab-176">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="1a2ab-177">Modülün birden çok sürümünü yüklediyseniz, modül otomatik yükleme ve `Import-Module` tarafından varsayılan olarak en son sürüm yüklenir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-177">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="1a2ab-178">`-RequiredVersion` parametresini kullanarak `Az` modülünün belirli bir sürümünü yükleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="1a2ab-178">You can install or load a specific version of the `Az` module using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="use-multiple-repositories-with-powershellget"></a><span data-ttu-id="1a2ab-179">PowerShellGet ile birden çok depo kullanma</span><span class="sxs-lookup"><span data-stu-id="1a2ab-179">Use multiple repositories with PowerShellGet</span></span>

<span data-ttu-id="1a2ab-180">**Repository** parametresi, PowerShellGet öğesine sisteminizde ek depolar eklediyseniz gereklidir ve Az modülü bunlardan birden fazlasında bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-180">The **Repository** parameter is required if you have added additional repositories to PowerShellGet on your system and the Az module can be found in more than one of them.</span></span>

```powershell-interactive
if ($PSVersionTable.PSEdition -eq 'Desktop' -and (Get-Module -Name AzureRM -ListAvailable)) {
    Write-Warning -Message 'Az module not installed. Having both the AzureRM and Az modules installed at the same time is not supported.'
} else {
    Install-Module -Name Az -Repository PSGallery -AllowClobber -Force
}
```

## <a name="provide-feedback"></a><span data-ttu-id="1a2ab-181">Geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="1a2ab-181">Provide feedback</span></span>

<span data-ttu-id="1a2ab-182">Azure PowerShell’de bir hata bulursanız [GitHub’da sorun bildirin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="1a2ab-182">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="1a2ab-183">Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1a2ab-183">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1a2ab-184">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="1a2ab-184">Next Steps</span></span>

<span data-ttu-id="1a2ab-185">Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ab-185">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="1a2ab-186">Azure PowerShell’i zaten biliyorsanız ve AzureRM’den geçiş yapmanız gerekiyorsa bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ab-186">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
