---
title: Azure PowerShell'i yükleme ve yapılandırma | Microsoft Docs
description: Azure PowerShell’i ilk kez kullanmak üzere yükleme ve yapılandırma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: fac77e88612091c09106dffea6aa6d3765c1416b
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53983003"
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="9d970-103">Azure PowerShell'i yükleyip yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9d970-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="9d970-104">Bu makalede Azure PowerShell modüllerini Windows ortamına yüklemek için uygulanması gereken adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9d970-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="9d970-105">macOS veya Linux üzerinde Azure PowerShell kullanmak istiyorsanız aşağıdaki makaleye bakın: [Azure PowerShell’i macOS ve Linux’a yükleme ve yapılandırma](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="9d970-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="9d970-106">Azure PowerShell'in PowerShell Galerisi'nden yüklenmesi, tercih edilen yükleme yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="9d970-106">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

## <a name="step-1-install-powershellget"></a><span data-ttu-id="9d970-107">1. Adım: PowerShellGet yükleme</span><span class="sxs-lookup"><span data-stu-id="9d970-107">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="9d970-108">PowerShell Galerisi’nden yükleme yapabilmek için PowerShellGet modülü gerekir.</span><span class="sxs-lookup"><span data-stu-id="9d970-108">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="9d970-109">Uygun PowerShellGet sürümüne ve diğer sistem gereksinimlerine sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9d970-109">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="9d970-110">PowerShellGet’in sisteminizde yüklü olup olmadığını görmek için aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="9d970-110">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="9d970-111">Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="9d970-111">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="9d970-112">PowerShellGet 1.1.2.0 veya üzeri bir sürüm gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9d970-112">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="9d970-113">PowerShellGet’i güncelleştirmek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="9d970-113">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="9d970-114">PowerShellGet yüklü değilse bu makalenin [PowerShellGet edinme](#how-to-get-powershellget) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="9d970-114">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="9d970-115">PowerShellGet kullanımı, betikleri çalıştırmanıza olanak tanıyan bir Yürütme İlkesi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="9d970-115">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="9d970-116">PowerShell'in Yürütme İlkesi hakkında daha fazla bilgi için bkz. [Yürütme İlkeleri Hakkında](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="9d970-116">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="9d970-117">Bu belgede açıklanan AzureRM modülü .NET Framework kullanır.</span><span class="sxs-lookup"><span data-stu-id="9d970-117">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="9d970-118">Bu da, .NET Core kullanan PowerShell 6.0 ile uyumsuz olmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="9d970-118">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="9d970-119">PowerShell 6.0 kullanıyorsanız, [macOS ve Linux için yükleme yönergelerini](install-azurermps-maclinux.md) izleyin.</span><span class="sxs-lookup"><span data-stu-id="9d970-119">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="9d970-120">2. Adım: Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="9d970-120">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="9d970-121">Azure PowerShell’in PowerShell Galerisi’nden yüklenebilmesi için yükseltilmiş ayrıcalıklar gerekir.</span><span class="sxs-lookup"><span data-stu-id="9d970-121">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="9d970-122">Yükseltilmiş bir PowerShell oturumunda aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="9d970-122">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="9d970-123">PowerShell Galerisi varsayılan olarak PowerShellGet için Güvenilir depo şeklinde yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="9d970-123">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="9d970-124">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="9d970-124">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="9d970-125">Yükleme işlemine devam etmek için "Evet" veya "Tümüne Evet" yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="9d970-125">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="9d970-126">NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="9d970-126">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="9d970-127">AzureRM modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="9d970-127">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="9d970-128">AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş diğer Azure PowerShell modülleri PowerShell Galerisi'nden indirilir.</span><span class="sxs-lookup"><span data-stu-id="9d970-128">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="9d970-129">Azure PowerShell'in önceki sürümlerinden biri sisteminizde yüklüyse hata iletisiyle karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d970-129">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="9d970-130">Bu sorunu çözmek için bu makalenin [Azure PowerShell'in yeni bir sürümüne güncelleştirme](#update-azps) bölümünü inceleyin.</span><span class="sxs-lookup"><span data-stu-id="9d970-130">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="9d970-131">3. Adım: AzureRM modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="9d970-131">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="9d970-132">Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9d970-132">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="9d970-133">Bunu normal (yükseltilmiş olmayan) bir PowerShell oturumunda yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9d970-133">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="9d970-134">Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:</span><span class="sxs-lookup"><span data-stu-id="9d970-134">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="9d970-135">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="9d970-135">Next Steps</span></span>

<span data-ttu-id="9d970-136">Azure PowerShell kullanma hakkında daha fazla bilgi için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="9d970-136">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="9d970-137">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="9d970-137">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="9d970-138">Sorunları bildirme ve geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="9d970-138">Reporting issues and feedback</span></span>

<span data-ttu-id="9d970-139">Araçla ilgili bir hatayla karşılaşırsanız, GitHub deposunun [Sorunlar](https://github.com/Azure/azure-powershell/issues) bölümünden sorunu bildirin.</span><span class="sxs-lookup"><span data-stu-id="9d970-139">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="9d970-140">Komut satırından geri bildirim sağlamak için `Send-Feedback` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9d970-140">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="9d970-141">Sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="9d970-141">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="9d970-142">PowerShellGet edinme</span><span class="sxs-lookup"><span data-stu-id="9d970-142">How to get PowerShellGet</span></span>

|<span data-ttu-id="9d970-143">İşletim Sistemi Sürümü</span><span class="sxs-lookup"><span data-stu-id="9d970-143">OS Version</span></span>|<span data-ttu-id="9d970-144">Yükleme yönergeleri</span><span class="sxs-lookup"><span data-stu-id="9d970-144">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="9d970-145">Bilgisayarımda Windows 10 veya Windows Server 2016 yüklü</span><span class="sxs-lookup"><span data-stu-id="9d970-145">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="9d970-146">İşletim sisteminde bulunan Windows Management Framework (WMF) 5.0’da yerleşiktir</span><span class="sxs-lookup"><span data-stu-id="9d970-146">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="9d970-147">PowerShell 5'e yükseltme yapmak istiyorum</span><span class="sxs-lookup"><span data-stu-id="9d970-147">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="9d970-148">WMF’nin en son sürümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="9d970-148">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="9d970-149">Windows’un PowerShell 3 veya PowerShell 4 içeren bir sürümünü çalıştırıyorum</span><span class="sxs-lookup"><span data-stu-id="9d970-149">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="9d970-150">PackageManagement modüllerini alın</span><span class="sxs-lookup"><span data-stu-id="9d970-150">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="9d970-151">Azure PowerShell sürümünü denetleme</span><span class="sxs-lookup"><span data-stu-id="9d970-151">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="9d970-152">En son sürüme mümkün olan en kısa sürede yükseltme yapmanız önerilse de, Azure PowerShell’in birkaç sürümü desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="9d970-152">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="9d970-153">Azure PowerShell'in yüklü olan sürümünü belirlemek için komut satırından `Get-InstalledModule AzureRM` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="9d970-153">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule AzureRM` from your command line.</span></span>

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="9d970-154">Klasik dağıtım yöntemleri için destek</span><span class="sxs-lookup"><span data-stu-id="9d970-154">Support for classic deployment methods</span></span>

<span data-ttu-id="9d970-155">Klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d970-155">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="9d970-156">Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="9d970-156">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="9d970-157">Azure ve AzureRM modülleri ortak bağımlılıklara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="9d970-157">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="9d970-158">Hem Azure hem de AzureRM modüllerini kullanıyorsanız her paket için aynı sürümü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9d970-158">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="9d970-159">Azure PowerShell’in yeni bir sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="9d970-159">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="9d970-160">Hizmet Yönetimi modülünü içeren eski bir Azure PowerShell sürümü yüklüyse şu hata iletisiyle karşılaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="9d970-160">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="9d970-161">Hata iletisinde de belirtildiği üzere modülü yüklemek için -AllowClobber parametresini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9d970-161">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="9d970-162">Aşağıdaki komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="9d970-162">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="9d970-163">Daha fazla bilgi için [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) yardım konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="9d970-163">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="9d970-164">Modül sürümlerini yan yana yükleme</span><span class="sxs-lookup"><span data-stu-id="9d970-164">Installing module versions side by side</span></span>

<span data-ttu-id="9d970-165">PowerShellGet yükleme yöntemi, birden fazla sürümün yüklenmesini destekleyen tek yöntemdir.</span><span class="sxs-lookup"><span data-stu-id="9d970-165">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="9d970-166">Örneğin, güncelleştirmek için zaman veya kaynaklara sahip olmadığınız önceki bir Azure PowerShell sürümünü kullanarak yazdığınız betikler olabilir.</span><span class="sxs-lookup"><span data-stu-id="9d970-166">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="9d970-167">Aşağıdaki komutlar birden fazla Azure PowerShell sürümünün nasıl yükleneceğini göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="9d970-167">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="9d970-168">Bir PowerShell oturumunda modülün yalnızca bir sürümü yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="9d970-168">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="9d970-169">AzureRM cmdlet’lerinin belirli bir sürümünü içeri aktarmak için yeni bir PowerShell penceresi açıp `Import-Module` seçeneğini kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="9d970-169">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> <span data-ttu-id="9d970-170">Sürüm 2.1.0 ve sürüm 1.2.6, yan yana yüklenip kullanılmak üzere tasarlanmış ilk modül sürümleridir.</span><span class="sxs-lookup"><span data-stu-id="9d970-170">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="9d970-171">Azure PowerShell'in önceki sürümlerinden biri yüklenirken **AzureRM.Profile** modülünün uyumlu olmayan sürümleri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="9d970-171">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="9d970-172">Bu işlemin sonucunda cmdlet'leri her çalıştırdığınızda oturum açmanız istenir.</span><span class="sxs-lookup"><span data-stu-id="9d970-172">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="9d970-173">Diğer yükleme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="9d970-173">Other installation methods</span></span>

<span data-ttu-id="9d970-174">Web Platformu Yükleyicisi veya MSI Paketi kullanarak yükleme hakkında bilgi için bkz. [Diğer yükleme yöntemleri](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="9d970-174">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
