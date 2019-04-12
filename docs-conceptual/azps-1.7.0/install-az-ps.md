---
title: Azure PowerShell'i PowerShellGet ile yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363809"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="43bce-103">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="43bce-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="43bce-104">Bu makalede, PowerShellGet kullanarak Azure PowerShell modüllerini nasıl yükleyeceğiniz anlatılır.</span><span class="sxs-lookup"><span data-stu-id="43bce-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="43bce-105">Bu yönergeler Windows, macOS ve Linux platformlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="43bce-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="43bce-106">Az modülü için şu anda başka desteklenen yükleme metodu yoktur.</span><span class="sxs-lookup"><span data-stu-id="43bce-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="43bce-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="43bce-107">Requirements</span></span>

<span data-ttu-id="43bce-108">Azure PowerShell, Windows’da PowerShell 5.1 veya sonraki sürümleriyle, diğer platformlarda PowerShell 6 ile çalışır.</span><span class="sxs-lookup"><span data-stu-id="43bce-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell 6 on any platform.</span></span>
<span data-ttu-id="43bce-109">PowerShell sürümünüzü denetlemek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="43bce-109">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="43bce-110">Eski bir sürümünüz varsa veya PowerShell'i yüklemeniz gerekiyorsa, bkz. [PowerShell'in çeşitli sürümlerini yükleme](/powershell/scripting/setup/installing-powershell).</span><span class="sxs-lookup"><span data-stu-id="43bce-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](/powershell/scripting/setup/installing-powershell).</span></span> <span data-ttu-id="43bce-111">Platformunuza yönelik yükleme bilgilerine bu sayfadan bağlantı verilir.</span><span class="sxs-lookup"><span data-stu-id="43bce-111">Install information for your platform is linked from that page.</span></span>

<span data-ttu-id="43bce-112">Windows’da PowerShell 5 kullanıyorsanız .NET Framework 4.7.2’nin de yüklü olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="43bce-112">If you are using PowerShell 5 on Windows, you also need .NET Framework 4.7.2 installed.</span></span> <span data-ttu-id="43bce-113">.NET Framework’ü güncelleştirme veya yeni bir sürümünü yükleme hakkındaki yönergeler için [.NET Framework yükleme kılavuzuna](/dotnet/framework/install) bakın.</span><span class="sxs-lookup"><span data-stu-id="43bce-113">For instructions on updating or installing a new version of .NET Framework, see the [.NET Framework installation guide](/dotnet/framework/install).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="43bce-114">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="43bce-114">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="43bce-115">AzureRM ve Az modülü aynı anda yüklü olabilir.</span><span class="sxs-lookup"><span data-stu-id="43bce-115">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="43bce-116">İki modül de yüklüyse __diğer adları etkinleştirmeyin__.</span><span class="sxs-lookup"><span data-stu-id="43bce-116">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="43bce-117">Diğer adların etkinleştirilmesi, AzureRM cmdlet’leri ile Az komut diğer adları arasında çakışmalara neden olur ve bu da beklenmeyen davranışlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="43bce-117">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="43bce-118">Az modülünü yüklemeden önce AzureRM modülünü kaldırmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="43bce-118">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="43bce-119">Dilediğiniz zaman AzureRM modülünü kaldırabilir veya diğer adları etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43bce-119">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="43bce-120">AzureRM komut diğer adları hakkında bilgi edinmek için bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="43bce-120">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="43bce-121">Kaldırma yönergeleri için bkz. [AzureRM modülünü kaldırma](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="43bce-121">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="43bce-122">Modülleri genel kapsamda yüklemek için, PowerShell Galerisi'ndeki modülleri yüklemek üzere yükseltilmiş ayrıcalıklara ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="43bce-122">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="43bce-123">Azure PowerShell'i yüklemek için, aşağıdaki komutu yükseltilmiş oturumda çalıştırın (Windows'da "Yönetici Olarak Çalıştır" ile ya da macOS veya Linux'ta süper kullanıcı ayrıcalıklarıyla):</span><span class="sxs-lookup"><span data-stu-id="43bce-123">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="43bce-124">Yönetici ayrıcalıklarına erişiminiz yoksa, `-Scope` bağımsız değişkenini ekleyerek geçerli kullanıcı için yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43bce-124">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="43bce-125">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="43bce-125">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="43bce-126">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="43bce-126">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="43bce-127">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="43bce-127">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="43bce-128">Az modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="43bce-128">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="43bce-129">Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="43bce-129">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="43bce-130">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="43bce-130">Sign in</span></span>

<span data-ttu-id="43bce-131">Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="43bce-131">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="43bce-132">Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module Az` kullanarak modülü el ile içeri aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="43bce-132">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="43bce-133">Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.</span><span class="sxs-lookup"><span data-stu-id="43bce-133">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="43bce-134">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="43bce-134">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="43bce-135">Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="43bce-135">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="43bce-136">Azure PowerShell modülünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="43bce-136">Update the Azure PowerShell module</span></span>

<span data-ttu-id="43bce-137">Azure PowerShell yüklemenizi güncelleştirmek için [Update-Module](/powershell/module/powershellget/update-module) cmdlet'ini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43bce-137">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="43bce-138">Bu komut eski sürümleri __kaldırmaz__.</span><span class="sxs-lookup"><span data-stu-id="43bce-138">This command does __not__ uninstall older versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="43bce-139">Sisteminizdeki eski Azure PowerShell sürümlerini nasıl kaldıracağınızı öğrenmek için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="43bce-139">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="43bce-140">Azure PowerShell'in birden çok sürümünü kullanma</span><span class="sxs-lookup"><span data-stu-id="43bce-140">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="43bce-141">Azure PowerShell'in birden çok sürümünü yüklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="43bce-141">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="43bce-142">Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="43bce-142">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="43bce-143">Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="43bce-143">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="43bce-144">`-RequiredVersion` bağımsız değişkenini kullanarak `Az` modülünün belirli bir sürümünü yükleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="43bce-144">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="43bce-145">Modülün birden çok sürümünü yüklediyseniz, modül otomatik yükleme ve `Import-Module` tarafından varsayılan olarak en son sürüm yüklenir.</span><span class="sxs-lookup"><span data-stu-id="43bce-145">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="43bce-146">Geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="43bce-146">Provide feedback</span></span>

<span data-ttu-id="43bce-147">Azure Powershell’de bir hata bulursanız [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="43bce-147">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="43bce-148">Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="43bce-148">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="43bce-149">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="43bce-149">Next Steps</span></span>

<span data-ttu-id="43bce-150">Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="43bce-150">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="43bce-151">Azure PowerShell’i zaten biliyorsanız ve AzureRM’den geçiş yapmanız gerekiyorsa bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="43bce-151">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
