---
title: Azure PowerShell'i PowerShellGet ile yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365740"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="9750c-103">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="9750c-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="9750c-104">Bu makalede, PowerShellGet kullanarak Azure PowerShell modüllerini nasıl yükleyeceğiniz anlatılır.</span><span class="sxs-lookup"><span data-stu-id="9750c-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="9750c-105">Bu yönergeler Windows, macOS ve Linux platformlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9750c-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="9750c-106">Az modülü için şu anda başka desteklenen yükleme metodu yoktur.</span><span class="sxs-lookup"><span data-stu-id="9750c-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9750c-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="9750c-107">Requirements</span></span>

<span data-ttu-id="9750c-108">Azure PowerShell, Windows’da PowerShell 5.1 veya sonraki sürümleriyle veya tüm platformlarda PowerShell 6.x ve sonraki sürümleriyle çalışır.</span><span class="sxs-lookup"><span data-stu-id="9750c-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="9750c-109">PowerShell'iniz olup olmadığından veya macOS mu yoksa Linux mı kullandığınızdan emin değilseniz, [PowerShell Core'un en son sürümünü yükleyin](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="9750c-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="9750c-110">PowerShell sürümünüzü denetlemek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="9750c-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="9750c-111">Azure PowerShell'i Windows üzerinde PowerShell 5.1'de çalıştırmak için:</span><span class="sxs-lookup"><span data-stu-id="9750c-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="9750c-112">Gerekirse [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)'e güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="9750c-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="9750c-113">Windows 10 kullanıyorsanız, zaten PowerShell 5.1 yüklüdür.</span><span class="sxs-lookup"><span data-stu-id="9750c-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="9750c-114">[.NET Framework 4.7.2 veya sonraki sürümünü](/dotnet/framework/install) yükleyin.</span><span class="sxs-lookup"><span data-stu-id="9750c-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="9750c-115">PowerShell Core kullanıldığında, Azure PowerShell için ek gereksinimler yoktur.</span><span class="sxs-lookup"><span data-stu-id="9750c-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="9750c-116">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="9750c-116">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="9750c-117">AzureRM ve Az modülü aynı anda yüklü olabilir.</span><span class="sxs-lookup"><span data-stu-id="9750c-117">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="9750c-118">İki modül de yüklüyse __diğer adları etkinleştirmeyin__.</span><span class="sxs-lookup"><span data-stu-id="9750c-118">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="9750c-119">Diğer adların etkinleştirilmesi, AzureRM cmdlet’leri ile Az komut diğer adları arasında çakışmalara neden olur ve bu da beklenmeyen davranışlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="9750c-119">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="9750c-120">Az modülünü yüklemeden önce AzureRM modülünü kaldırmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="9750c-120">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="9750c-121">Dilediğiniz zaman AzureRM modülünü kaldırabilir veya diğer adları etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9750c-121">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="9750c-122">AzureRM komut diğer adları hakkında bilgi edinmek için bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="9750c-122">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="9750c-123">Kaldırma yönergeleri için bkz. [AzureRM modülünü kaldırma](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="9750c-123">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="9750c-124">Modülleri genel kapsamda yüklemek için, PowerShell Galerisi'ndeki modülleri yüklemek üzere yükseltilmiş ayrıcalıklara ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="9750c-124">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="9750c-125">Azure PowerShell'i yüklemek için, aşağıdaki komutu yükseltilmiş oturumda çalıştırın (Windows'da "Yönetici Olarak Çalıştır" ile ya da macOS veya Linux'ta süper kullanıcı ayrıcalıklarıyla):</span><span class="sxs-lookup"><span data-stu-id="9750c-125">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="9750c-126">Yönetici ayrıcalıklarına erişiminiz yoksa, `-Scope` bağımsız değişkenini ekleyerek geçerli kullanıcı için yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9750c-126">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="9750c-127">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="9750c-127">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="9750c-128">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="9750c-128">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="9750c-129">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="9750c-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="9750c-130">Az modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="9750c-130">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="9750c-131">Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="9750c-131">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="9750c-132">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="9750c-132">Sign in</span></span>

<span data-ttu-id="9750c-133">Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="9750c-133">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="9750c-134">Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module Az` kullanarak modülü el ile içeri aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9750c-134">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="9750c-135">Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.</span><span class="sxs-lookup"><span data-stu-id="9750c-135">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="9750c-136">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9750c-136">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="9750c-137">Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="9750c-137">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="9750c-138">Azure PowerShell modülünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="9750c-138">Update the Azure PowerShell module</span></span>

<span data-ttu-id="9750c-139">Az modülünün paketlenme şeklinden dolayı, [Update-Module](/powershell/module/powershellget/update-module) komutu yüklemenizi doğru güncelleştirmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="9750c-139">Because of how the Az module is package, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="9750c-140">Az modülü teknik olarak, Azure hizmetleriyle etkileşime yönelik cmdlet'lerin yer aldığı tüm alt modülleri kapsayan bir meta modülüdür.</span><span class="sxs-lookup"><span data-stu-id="9750c-140">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="9750c-141">Başka bir deyişle, Azure PowerShell modülünü güncelleştirmek için yalnızca __güncelleştirmek__ yerine __yeniden yüklemeniz__ gerekir.</span><span class="sxs-lookup"><span data-stu-id="9750c-141">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="9750c-142">Bu işlem yüklemeyle aynı şekilde yapılır ama `-Force` bağımsız değişkenini eklemeniz gerekebilir:</span><span class="sxs-lookup"><span data-stu-id="9750c-142">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="9750c-143">Bu yüklü modüllerin üzerine yazabilse de, sisteminizde yine de eski sürümler kalabilir.</span><span class="sxs-lookup"><span data-stu-id="9750c-143">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="9750c-144">Sisteminizdeki eski Azure PowerShell sürümlerini nasıl kaldıracağınızı öğrenmek için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="9750c-144">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="9750c-145">Azure PowerShell'in birden çok sürümünü kullanma</span><span class="sxs-lookup"><span data-stu-id="9750c-145">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="9750c-146">Azure PowerShell'in birden çok sürümünü yüklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="9750c-146">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="9750c-147">Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="9750c-147">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="9750c-148">Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="9750c-148">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="9750c-149">`-RequiredVersion` bağımsız değişkenini kullanarak `Az` modülünün belirli bir sürümünü yükleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9750c-149">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="9750c-150">Modülün birden çok sürümünü yüklediyseniz, modül otomatik yükleme ve `Import-Module` tarafından varsayılan olarak en son sürüm yüklenir.</span><span class="sxs-lookup"><span data-stu-id="9750c-150">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="9750c-151">Geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="9750c-151">Provide feedback</span></span>

<span data-ttu-id="9750c-152">Azure Powershell’de bir hata bulursanız [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="9750c-152">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="9750c-153">Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9750c-153">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9750c-154">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="9750c-154">Next Steps</span></span>

<span data-ttu-id="9750c-155">Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9750c-155">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="9750c-156">Azure PowerShell’i zaten biliyorsanız ve AzureRM’den geçiş yapmanız gerekiyorsa bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="9750c-156">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
