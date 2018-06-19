---
title: Azure PowerShell'i PowerShellGet ile yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323110"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="d4f9b-103">Azure PowerShell'i PowerShellGet ile yükleme</span><span class="sxs-lookup"><span data-stu-id="d4f9b-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="d4f9b-104">Bu makalede PowerShellGet kullanarak Azure PowerShell modüllerini Windows ortamına yüklemek için uygulanması gereken adımlar açıklanır.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="d4f9b-105">Bu Azure PowerShell'i yüklemek için tercih edilen yoldur ama bunun yerine Web Platformu Yükleyicisi veya MSI paketi kullanarak yükleyecekseniz, bkz. [Diğer yükleme yöntemleri](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="d4f9b-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="d4f9b-106">Azure PowerShell'i macOS veya Linux'a yüklemek istiyorsanız şu makaleye bakın: [Azure PowerShell'i macOS ve Linux'ta yükleme ve yapılandırma](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="d4f9b-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="d4f9b-107">Sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="d4f9b-107">System requirements</span></span>

<span data-ttu-id="d4f9b-108">Azure PowerShell sürüm 6.1.0, PowerShell 5.0 (veya sonraki) sürümünü gerektirir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="d4f9b-109">PowerShell 5.0'ı yükseltme hakkında bilgi için bkz. [Varolan Windows PowerShell'i yükseltme](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="d4f9b-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="d4f9b-110">PowerShellGet, PowerShell 5.0'ın parçası olarak otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="d4f9b-111">Azure PowerShell modülünü yükleme veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d4f9b-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="d4f9b-112">Azure PowerShell’in PowerShell Galerisi’nden yüklenebilmesi için yükseltilmiş ayrıcalıklar gerekir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="d4f9b-113">Yükseltilmiş bir PowerShell oturumunda aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="d4f9b-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="d4f9b-114">Bu komut sisteminizde varolan Azure PowerShell yüklemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="d4f9b-115">Birden çok sürümün yüklü olması gerekiyorsa, SSS bölümünde [Azure PowerShell'in birden çok sürümünü yükleyebilir miyim?](#multiple-versions) sorusunun yanıtına bakın.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="d4f9b-116">PowerShell Galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="d4f9b-117">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="d4f9b-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="d4f9b-118">Yükleme işlemine devam etmek için "Evet" veya "Tümüne Evet" yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="d4f9b-119">NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="d4f9b-120">AzureRM modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="d4f9b-121">AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş olan tüm Azure PowerShell modülleri PowerShell Galerisi'nden indirilir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="d4f9b-122">Azure PowerShell modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="d4f9b-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="d4f9b-123">Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="d4f9b-124">Bunu normal (yükseltilmiş olmayan) bir PowerShell oturumunda yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="d4f9b-125">Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:</span><span class="sxs-lookup"><span data-stu-id="d4f9b-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="d4f9b-126">Sorunları bildirme ve geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="d4f9b-126">Reporting issues and feedback</span></span>

<span data-ttu-id="d4f9b-127">Araçta hatalarla karşılaşırsanız, lütfen [GitHub'a bir sorun girin](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="d4f9b-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="d4f9b-128">Komut satırından geri bildirim sağlamak için `Send-Feedback` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d4f9b-129">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="d4f9b-129">Next Steps</span></span>

<span data-ttu-id="d4f9b-130">Azure PowerShell kullanma hakkında daha fazla bilgi için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="d4f9b-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="d4f9b-131">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="d4f9b-131">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="d4f9b-132">Sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="d4f9b-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="d4f9b-133">Azure PowerShell'in sürümünü nasıl denetleyebilirim?</span><span class="sxs-lookup"><span data-stu-id="d4f9b-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="d4f9b-134">En son sürüme mümkün olan en kısa sürede yükseltme yapmanız önerilse de, Azure PowerShell’in birkaç sürümü desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="d4f9b-135">Azure PowerShell'in yüklü olan sürümünü belirlemek için komut satırından `Get-Module AzureRM` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="d4f9b-136">Azure PowerShell'i Klasik Azure dağıtımlarında kullanabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="d4f9b-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="d4f9b-137">Klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="d4f9b-138">Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="d4f9b-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="d4f9b-139">Azure ve AzureRM modülleri ortak bağımlılıklara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="d4f9b-140">Hem Azure hem de AzureRM modüllerini kullanıyorsanız her paket için aynı sürümü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="d4f9b-141"><a name="multiple-versions"/>Azure PowerShell'in birden çok sürümünü yükleyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="d4f9b-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="d4f9b-142">Birden çok sürümü destekleyen tek yükleme yöntemi PowerShellGet'tir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="d4f9b-143">Birden çok sürümü yüklemek için, `Install-Module` cmdlet'ine `-RequiredVersion` parametresini ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="d4f9b-144">Örneğin, hem 6.1.0 hem de 1.2.9 sürümlerini yüklemek için:</span><span class="sxs-lookup"><span data-stu-id="d4f9b-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="d4f9b-145">Bir PowerShell oturumunda modülün yalnızca bir sürümü yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="d4f9b-146">Azure PowerShell modülünün belirli bir sürümünü içeri aktarmak için yeni bir PowerShell penceresi açıp `Import-Module` parametresini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="d4f9b-147">Sürüm 2.1.0 ve sürüm 1.2.6, yan yana yüklenip kullanılmak üzere tasarlanmış ilk modül sürümleridir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="d4f9b-148">Azure PowerShell'in önceki sürümlerinden biri yüklenirken **AzureRM.Profile** modülünün uyumlu olmayan sürümleri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="d4f9b-149">Bu işlemin sonucunda cmdlet'leri her çalıştırdığınızda oturum açmanız istenir.</span><span class="sxs-lookup"><span data-stu-id="d4f9b-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
