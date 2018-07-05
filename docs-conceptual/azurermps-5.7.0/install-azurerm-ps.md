---
title: PowerShellGet ile Windows'da Azure PowerShell yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: dc5a1c59d23e37acf11aa7831ddc6e1edbd7f73e
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091427"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="6a0f2-103">PowerShellGet ile Windows'da Azure PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="6a0f2-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="6a0f2-104">Bu makalede PowerShellGet kullanarak Azure PowerShell modüllerini Windows ortamına yüklemek için uygulanması gereken adımlar açıklanır.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="6a0f2-105">PowerShellGet ve modül yönetimi, Azure PowerShell'i yüklemek için tercih edilen yoldur. Ancak bunun yerine Web Platformu Yükleyicisi veya MSI paketi kullanarak yükleyecekseniz bkz. [Diğer yükleme yöntemleri](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="6a0f2-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="6a0f2-106">Azure PowerShell'i farklı platformlara yükleme talimatları için bkz. [Azure PowerShell'i macOS ve Linux'ta yükleme ve yapılandırma](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="6a0f2-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="6a0f2-107">Azure klasik dağıtım modeli, Azure PowerShell'in bu sürümü tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="6a0f2-108">Klasik dağıtımlar için [Azure PowerShell Service Management modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps) talimatlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a0f2-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="6a0f2-109">Requirements</span></span>

<span data-ttu-id="6a0f2-110">Azure PowerShell'i yüklemek için PowerShellGet sürüm 1.1.2.0 veya üzeri gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-110">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="6a0f2-111">Sisteminizde mevcut olup olmadığını görmek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="6a0f2-111">To check if it is available on your system, run the following command:</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="6a0f2-112">Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="6a0f2-112">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="6a0f2-113">PowerShellGet yüklemenizi güncelleştirmeniz gerekiyorsa şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="6a0f2-113">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="6a0f2-114">PowerShellGet yüklü değilse aşağıdaki tablodan sisteminize özgü yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-114">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="6a0f2-115">Senaryo</span><span class="sxs-lookup"><span data-stu-id="6a0f2-115">Scenario</span></span>|<span data-ttu-id="6a0f2-116">Yükleme yönergeleri</span><span class="sxs-lookup"><span data-stu-id="6a0f2-116">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="6a0f2-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="6a0f2-117">Windows 10</span></span><br/><span data-ttu-id="6a0f2-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6a0f2-118">Windows Server 2016</span></span>|<span data-ttu-id="6a0f2-119">İşletim sisteminde bulunan Windows Management Framework (WMF) 5.0’da yerleşiktir</span><span class="sxs-lookup"><span data-stu-id="6a0f2-119">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="6a0f2-120">PowerShell 5'e yükseltme</span><span class="sxs-lookup"><span data-stu-id="6a0f2-120">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="6a0f2-121">WMF’nin en son sürümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="6a0f2-121">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="6a0f2-122">Şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="6a0f2-122">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="6a0f2-123">PowerShell 3 veya PowerShell 4 yüklü Windows</span><span class="sxs-lookup"><span data-stu-id="6a0f2-123">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="6a0f2-124"><il>[PackageManagement modüllerini alın](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="6a0f2-124"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="6a0f2-125">Şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="6a0f2-125">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="6a0f2-126">PowerShellGet kullanımı, betikleri çalıştırmanıza olanak tanıyan bir Yürütme İlkesi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-126">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="6a0f2-127">PowerShell'in Yürütme İlkesi hakkında daha fazla bilgi için bkz. [Yürütme İlkeleri Hakkında](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="6a0f2-127">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="6a0f2-128">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="6a0f2-128">Install the Azure PowerShell module</span></span>

<span data-ttu-id="6a0f2-129">PowerShell Galerisi'ndeki modülleri yüklemek için yükseltilmiş ayrıcalıklara ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-129">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="6a0f2-130">Azure PowerShell'i yüklemek için yükseltilmiş oturumda şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="6a0f2-130">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="6a0f2-131">NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-131">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="6a0f2-132">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-132">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="6a0f2-133">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="6a0f2-133">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="6a0f2-134">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-134">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="6a0f2-135">`AzureRM` modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-135">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="6a0f2-136">Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-136">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="6a0f2-137">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="6a0f2-137">Sign in</span></span>

<span data-ttu-id="6a0f2-138">Azure PowerShell ile çalışmaya başlamak için `AzureRM` modülünü geçerli PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yüklemeniz ve Azure kimlik bilgilerinizle oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-138">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="6a0f2-139">Bu adımları, başlattığınız her yeni PowerShell oturumu için tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-139">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="6a0f2-140">`AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="6a0f2-140">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="6a0f2-141">Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="6a0f2-141">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="6a0f2-142">Azure PowerShell modülünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6a0f2-142">Update the Azure PowerShell module</span></span>

<span data-ttu-id="6a0f2-143">Azure PowerShell yüklemenizi güncelleştirmek için [Update-Module](/powershell/module/powershellget/update-module) cmdlet'ini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-143">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="6a0f2-144">Bu komut önceki sürümleri __kaldırmaz__.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-144">This command does __not__ uninstall earlier versions.</span></span>

```powershell
Update-Module -Name AzureRM
```

<span data-ttu-id="6a0f2-145">Sisteminizdeki eski Azure PowerShell sürümlerini kaldırmak isterseniz bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="6a0f2-145">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="6a0f2-146">Azure PowerShell'in birden çok sürümünü kullanma</span><span class="sxs-lookup"><span data-stu-id="6a0f2-146">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="6a0f2-147">Azure PowerShell'in birden çok sürümünü yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-147">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="6a0f2-148">Şirket içi Azure Stack kaynaklarıyla çalışıyorsanız, PowerShell 5.0 güncelleştirmesini alamayan eski bir Windows sürümünü çalıştırıyorsanız veya Azure klasik dağıtım modelini kullanıyorsanız birden fazla sürüme ihtiyaç duyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-148">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="6a0f2-149">Eski bir sürümü yüklemek için yükleme sırasında `-RequiredVersion` bağımsız değişkenini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-149">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="6a0f2-150">Azure PowerShell modülünü yüklerken varsayılan olarak son sürüm yüklenir.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-150">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="6a0f2-151">Farklı bir sürümü yüklemek için `-RequiredVersion` bağımsız değişkenini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-151">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="6a0f2-152">Geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="6a0f2-152">Provide feedback</span></span>

<span data-ttu-id="6a0f2-153">Azure Powershell kullanırken bir hatayla karşılaşırsanız lütfen [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="6a0f2-153">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="6a0f2-154">Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-154">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6a0f2-155">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="6a0f2-155">Next Steps</span></span>

<span data-ttu-id="6a0f2-156">Azure PowerShell'i kullanmaya başlamak için, [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) bölümünü inceleyerek modül ve özellikleri hakkında daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="6a0f2-156">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>