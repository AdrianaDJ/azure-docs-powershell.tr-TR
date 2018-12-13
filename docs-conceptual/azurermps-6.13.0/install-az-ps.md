---
title: Azure PowerShell 'Az' modülünü PowerShellGet ile yükleme
description: Windows, macOS ve Linux'ta Azure PowerShell PowerShellGet ile nasıl yüklenir?
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217006"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="f0b8a-103">Azure PowerShell 'Az' modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="f0b8a-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="f0b8a-104">Bu makalede, PowerShellGet kullanarak Azure PowerShell modüllerini nasıl yükleyeceğiniz anlatılır.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="f0b8a-105">Bu yönergeler Windows, macOS ve Linux platformlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="f0b8a-106">Az modülünün önizleme sürümünde başka yükleme yöntemleri desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="f0b8a-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="f0b8a-107">Requirements</span></span>

<span data-ttu-id="f0b8a-108">Azure PowerShell Windows üzerinde PowerShell 5.x ile veya herhangi bir platform üzerinde PowerShell 6.x ile çalışır.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="f0b8a-109">Makinenizde çalışan PowerShell sürümü kontrol etmek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="f0b8a-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="f0b8a-110">Eski bir sürümünüz varsa veya PowerShell'i yüklemeniz gerekiyorsa, bkz. [PowerShell'in çeşitli sürümlerini yükleme](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="f0b8a-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="f0b8a-111">Platformunuza yönelik yükleme bilgilerine bu sayfadan bağlantı verilir.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="f0b8a-112">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="f0b8a-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f0b8a-113">`AzureRM` ve `Az` modüllerini aynı anda yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-113">You can have both the `AzureRM` and `Az` modules installed at the same time.</span></span> <span data-ttu-id="f0b8a-114">İki modül de yüklüyse __diğer adları etkinleştirmeyin__.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-114">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="f0b8a-115">Diğer adların etkinleştirilmesi, `AzureRM` cmdlet’leri ile `Az` komut diğer adları arasında çakışmalara neden olur ve bu da beklenmeyen davranışlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-115">Enabling aliases will cause conflicts between `AzureRM` cmdlets and `Az` command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="f0b8a-116">`Az` modülünü yüklemeden önce `AzureRM` modülünü kaldırmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-116">It's recommended that before installing the `Az` module, you uninstall `AzureRM`.</span></span> <span data-ttu-id="f0b8a-117">Dilediğiniz zaman `AzureRM` modülünü kaldırabilir veya diğer adları etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-117">You can always uninstall `AzureRM` or enable aliases at any time.</span></span> <span data-ttu-id="f0b8a-118">Kaldırma yönergeleri için bkz. [Azure PowerShell modülünü (AzureRM) kaldırma](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="f0b8a-118">For uninstall instructions, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span> 

<span data-ttu-id="f0b8a-119">Modülleri genel kapsamda yüklemek için, PowerShell Galerisi'ndeki modülleri yüklemek üzere yükseltilmiş ayrıcalıklara ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-119">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="f0b8a-120">Azure PowerShell'i yüklemek için, aşağıdaki komutu yükseltilmiş oturumda çalıştırın (Windows'da "Yönetici Olarak Çalıştır" ile ya da macOS veya Linux'ta süper kullanıcı ayrıcalıklarıyla):</span><span class="sxs-lookup"><span data-stu-id="f0b8a-120">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="f0b8a-121">Yönetici ayrıcalıklarına erişiminiz yoksa, `-Scope` bağımsız değişkenini ekleyerek geçerli kullanıcı için yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-121">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="f0b8a-122">PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="f0b8a-123">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="f0b8a-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="f0b8a-124">Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="f0b8a-125">`Az` modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-125">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f0b8a-126">Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="f0b8a-127">Oturum aç</span><span class="sxs-lookup"><span data-stu-id="f0b8a-127">Sign in</span></span>

<span data-ttu-id="f0b8a-128">Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-128">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="f0b8a-129">Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module Az` kullanarak modülü el ile içeri aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-129">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="f0b8a-130">Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-130">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="f0b8a-131">Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-131">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="f0b8a-132">Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="f0b8a-132">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="f0b8a-133">Azure PowerShell modülünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f0b8a-133">Update the Azure PowerShell module</span></span>

<span data-ttu-id="f0b8a-134">Azure PowerShell yüklemenizi güncelleştirmek için [Update-Module](/powershell/module/powershellget/update-module) cmdlet'ini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-134">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="f0b8a-135">Bu komut önceki sürümleri __kaldırmaz__.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-135">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="f0b8a-136">Sisteminizdeki eski Azure PowerShell sürümlerini kaldırmak isterseniz bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="f0b8a-136">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="f0b8a-137">Azure PowerShell'in birden çok sürümünü kullanma</span><span class="sxs-lookup"><span data-stu-id="f0b8a-137">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="f0b8a-138">Azure PowerShell'in birden çok sürümünü yüklemek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-138">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="f0b8a-139">Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="f0b8a-139">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="f0b8a-140">Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="f0b8a-140">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="f0b8a-141">`Install-Module` ve `Import-Module` ile `-RequiredVersion` bağımsız değişkenini kullanarak `Az` modülünün belirli bir sürümünü yükleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f0b8a-141">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="f0b8a-142">Modülün birden çok sürümünü yüklediyseniz, varsayılan olarak en son sürüm yüklenir.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-142">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="f0b8a-143">Geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="f0b8a-143">Provide feedback</span></span>

<span data-ttu-id="f0b8a-144">Azure Powershell kullanırken bir hatayla karşılaşırsanız [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="f0b8a-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="f0b8a-145">Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f0b8a-146">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="f0b8a-146">Next Steps</span></span>

<span data-ttu-id="f0b8a-147">Azure PowerShell'i kullanmaya başlamak için, [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) bölümünü inceleyerek modül ve özellikleri hakkında daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="f0b8a-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
