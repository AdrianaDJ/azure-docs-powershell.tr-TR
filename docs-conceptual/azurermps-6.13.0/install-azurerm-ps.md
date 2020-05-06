---
title: PowerShellGet ile Windows'da Azure PowerShell yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 5de386bde1b8be5a4455b85d4f5fcdf38e4fcea2
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65535008"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="135a4-103">PowerShellGet ile Windows'da Azure PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="135a4-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="135a4-104">Bu makalede PowerShellGet kullanarak Windows için PowerShell 5.x sürümlerine yönelik Azure PowerShell modüllerini yüklemek için uygulanması gereken adımlar açıklanır.</span><span class="sxs-lookup"><span data-stu-id="135a4-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="135a4-105">PowerShellGet ve modül yönetimi, Azure PowerShell'i yüklemek için tercih edilen yoldur. Ancak bunun yerine Web Platformu Yükleyicisi veya MSI paketi kullanarak yükleyecekseniz bkz. [Diğer yükleme yöntemleri](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="135a4-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="135a4-106">Azure klasik dağıtım modeli, Azure PowerShell'in bu sürümü tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="135a4-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="135a4-107">Klasik dağıtımlar için [Azure PowerShell Service Management modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps) talimatlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="135a4-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="135a4-108">AzureRM modülü macOS veya Linux için desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="135a4-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="135a4-109">Azure PowerShell cmdlet'lerini bu platformlarda kullanmak için [Az modülünü yükleyin](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="135a4-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="135a4-110">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="135a4-110">Requirements</span></span>

<span data-ttu-id="135a4-111">Azure PowerShell sürüm 6.0'dan başlayarak, Azure PowerShell için PowerShell sürüm 5.0 gereklidir.</span><span class="sxs-lookup"><span data-stu-id="135a4-111">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="135a4-112">Makinenizde çalışan PowerShell sürümü kontrol etmek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="135a4-112">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="135a4-113">Sürümünüz eskiyse bkz. [Windows PowerShell'in mevcut sürümünü yükseltme](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="135a4-113">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="135a4-114">Bu belgede açıklanan AzureRM modülü .NET Framework kullanır.</span><span class="sxs-lookup"><span data-stu-id="135a4-114">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="135a4-115">Bu da, .NET Core kullanan PowerShell 6.0 ile uyumsuz olmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="135a4-115">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="135a4-116">PowerShell 6.0 kullanıyorsanız, [macOS ve Linux için yükleme yönergelerini](install-azurermps-maclinux.md) izleyin.</span><span class="sxs-lookup"><span data-stu-id="135a4-116">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="135a4-117">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="135a4-117">Install the Azure PowerShell module</span></span>

<span data-ttu-id="135a4-118">PowerShell Galerisi'ndeki modülleri yüklemek için yükseltilmiş ayrıcalıklara ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="135a4-118">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="135a4-119">Azure PowerShell'i yüklemek için yükseltilmiş oturumda şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="135a4-119">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="135a4-120">NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="135a4-120">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="135a4-121">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="135a4-121">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="135a4-122">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="135a4-122">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="135a4-123">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="135a4-123">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="135a4-124">`AzureRM` modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="135a4-124">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="135a4-125">Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="135a4-125">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="135a4-126">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="135a4-126">Sign in</span></span>

<span data-ttu-id="135a4-127">Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="135a4-127">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="135a4-128">Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module AzureRM` kullanarak modülü el ile içeri aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="135a4-128">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="135a4-129">Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.</span><span class="sxs-lookup"><span data-stu-id="135a4-129">Because of the way the module is structured, this can take a few seconds.</span></span>


<span data-ttu-id="135a4-130">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="135a4-130">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="135a4-131">Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="135a4-131">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="135a4-132">Azure PowerShell modülünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="135a4-132">Update the Azure PowerShell module</span></span>

<span data-ttu-id="135a4-133">Azure PowerShell yüklemenizi güncelleştirmek için [Update-Module](/powershell/module/powershellget/update-module) cmdlet'ini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="135a4-133">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="135a4-134">Bu komut önceki sürümleri __kaldırmaz__.</span><span class="sxs-lookup"><span data-stu-id="135a4-134">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="135a4-135">Sisteminizdeki eski Azure PowerShell sürümlerini kaldırmak isterseniz bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="135a4-135">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="135a4-136">Azure PowerShell'in birden çok sürümünü kullanma</span><span class="sxs-lookup"><span data-stu-id="135a4-136">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="135a4-137">Azure PowerShell'in birden çok sürümünü yüklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="135a4-137">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="135a4-138">Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="135a4-138">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

<span data-ttu-id="135a4-139">Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="135a4-139">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="135a4-140">Şirket içi Azure Stack kaynaklarıyla çalışıyorsanız, eski bir Windows sürümünü çalıştırıyorsanız veya Azure klasik dağıtım modelini kullanıyorsanız birden fazla sürüme ihtiyaç duyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="135a4-140">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="135a4-141">Eski bir sürümü yüklemek için yükleme sırasında `-RequiredVersion` bağımsız değişkenini belirtin.</span><span class="sxs-lookup"><span data-stu-id="135a4-141">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="135a4-142">Azure PowerShell modülünü yüklerken varsayılan olarak son sürüm yüklenir.</span><span class="sxs-lookup"><span data-stu-id="135a4-142">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="135a4-143">Farklı bir sürümü yüklemek için `-RequiredVersion` bağımsız değişkenini belirtin.</span><span class="sxs-lookup"><span data-stu-id="135a4-143">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="135a4-144">Geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="135a4-144">Provide feedback</span></span>

<span data-ttu-id="135a4-145">Azure Powershell kullanırken bir hatayla karşılaşırsanız [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="135a4-145">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="135a4-146">Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="135a4-146">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="135a4-147">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="135a4-147">Next Steps</span></span>

<span data-ttu-id="135a4-148">Azure PowerShell'i kullanmaya başlamak için, [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) bölümünü inceleyerek modül ve özellikleri hakkında daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="135a4-148">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
