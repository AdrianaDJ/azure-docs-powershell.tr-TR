---
title: PowerShellGet ile Windows'da Azure PowerShell yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/08/2018
ms.openlocfilehash: af59df025c7a0fb41aacb1e83d6342c20033ee6d
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001397"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="e1f94-103">PowerShellGet ile Windows'da Azure PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="e1f94-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="e1f94-104">Bu makalede PowerShellGet kullanarak Azure PowerShell modüllerini Windows ortamına yüklemek için uygulanması gereken adımlar açıklanır.</span><span class="sxs-lookup"><span data-stu-id="e1f94-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="e1f94-105">PowerShellGet ve modül yönetimi, Azure PowerShell'i yüklemek için tercih edilen yoldur. Ancak bunun yerine Web Platformu Yükleyicisi veya MSI paketi kullanarak yükleyecekseniz bkz. [Diğer yükleme yöntemleri](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="e1f94-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="e1f94-106">Azure PowerShell'i farklı platformlara yükleme talimatları için bkz. [Azure PowerShell'i macOS ve Linux'ta yükleme ve yapılandırma](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="e1f94-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="e1f94-107">Azure klasik dağıtım modeli, Azure PowerShell'in bu sürümü tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="e1f94-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="e1f94-108">Klasik dağıtımlar için [Azure PowerShell Service Management modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps) talimatlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="e1f94-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f94-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="e1f94-109">Requirements</span></span>

<span data-ttu-id="e1f94-110">Azure PowerShell sürüm 6.0'dan başlayarak, Azure PowerShell için PowerShell sürüm 5.0 gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e1f94-110">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="e1f94-111">Makinenizde çalışan PowerShell sürümü kontrol etmek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="e1f94-111">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell
$PSVersionTable.PSVersion
```

<span data-ttu-id="e1f94-112">Sürümünüz eskiyse bkz. [Windows PowerShell'in mevcut sürümünü yükseltme](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="e1f94-112">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1f94-113">Bu belgede açıklanan AzureRM modülü .NET Framework kullanır.</span><span class="sxs-lookup"><span data-stu-id="e1f94-113">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="e1f94-114">Bu da, .NET Core kullanan PowerShell 6.0 ile uyumsuz olmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="e1f94-114">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="e1f94-115">PowerShell 6.0 kullanıyorsanız, [macOS ve Linux için yükleme yönergelerini](install-azurermps-maclinux.md) izleyin.</span><span class="sxs-lookup"><span data-stu-id="e1f94-115">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="e1f94-116">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="e1f94-116">Install the Azure PowerShell module</span></span>

<span data-ttu-id="e1f94-117">PowerShell Galerisi'ndeki modülleri yüklemek için yükseltilmiş ayrıcalıklara ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="e1f94-117">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="e1f94-118">Azure PowerShell'i yüklemek için yükseltilmiş oturumda şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="e1f94-118">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="e1f94-119">NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="e1f94-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="e1f94-120">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="e1f94-120">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="e1f94-121">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="e1f94-121">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="e1f94-122">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="e1f94-122">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="e1f94-123">`AzureRM` modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="e1f94-123">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="e1f94-124">Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="e1f94-124">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="e1f94-125">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="e1f94-125">Sign in</span></span>

<span data-ttu-id="e1f94-126">Azure PowerShell ile çalışmaya başlamak için `AzureRM` modülünü geçerli PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yüklemeniz ve Azure kimlik bilgilerinizle oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e1f94-126">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="e1f94-127">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e1f94-127">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="e1f94-128">`AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="e1f94-128">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="e1f94-129">Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="e1f94-129">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="e1f94-130">Azure PowerShell modülünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e1f94-130">Update the Azure PowerShell module</span></span>

<span data-ttu-id="e1f94-131">Azure PowerShell yüklemenizi güncelleştirmek için [Update-Module](/powershell/module/powershellget/update-module) cmdlet'ini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e1f94-131">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="e1f94-132">Bu komut önceki sürümleri __kaldırmaz__.</span><span class="sxs-lookup"><span data-stu-id="e1f94-132">This command does __not__ uninstall earlier versions.</span></span>

```powershell
Update-Module -Name AzureRM
```

<span data-ttu-id="e1f94-133">Sisteminizdeki eski Azure PowerShell sürümlerini kaldırmak isterseniz bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="e1f94-133">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="e1f94-134">Azure PowerShell'in birden çok sürümünü kullanma</span><span class="sxs-lookup"><span data-stu-id="e1f94-134">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="e1f94-135">Azure PowerShell'in birden çok sürümünü yüklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="e1f94-135">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="e1f94-136">Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="e1f94-136">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell
Get-Module -Name AzureRM -List | select Name,Version
```

<span data-ttu-id="e1f94-137">Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="e1f94-137">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="e1f94-138">Şirket içi Azure Stack kaynaklarıyla çalışıyorsanız, eski bir Windows sürümünü çalıştırıyorsanız veya Azure klasik dağıtım modelini kullanıyorsanız birden fazla sürüme ihtiyaç duyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e1f94-138">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="e1f94-139">Eski bir sürümü yüklemek için yükleme sırasında `-RequiredVersion` bağımsız değişkenini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e1f94-139">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="e1f94-140">Azure PowerShell modülünü yüklerken varsayılan olarak son sürüm yüklenir.</span><span class="sxs-lookup"><span data-stu-id="e1f94-140">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="e1f94-141">Farklı bir sürümü yüklemek için `-RequiredVersion` bağımsız değişkenini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e1f94-141">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="e1f94-142">Geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="e1f94-142">Provide feedback</span></span>

<span data-ttu-id="e1f94-143">Azure Powershell kullanırken bir hatayla karşılaşırsanız [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="e1f94-143">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="e1f94-144">Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e1f94-144">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e1f94-145">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="e1f94-145">Next Steps</span></span>

<span data-ttu-id="e1f94-146">Azure PowerShell'i kullanmaya başlamak için, [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) bölümünü inceleyerek modül ve özellikleri hakkında daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="e1f94-146">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>