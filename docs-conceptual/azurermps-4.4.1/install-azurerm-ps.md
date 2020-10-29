---
title: Azure PowerShell'i yükleme ve yapılandırma | Microsoft Docs
description: Azure PowerShell’i ilk kez kullanmak üzere yükleme ve yapılandırma.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3f4b05352ef5e5c7f32495d002a78aadd3e056e1
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523300"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="7cefb-103">PowerShellGet ile Windows'da Azure PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="7cefb-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="7cefb-104">Bu makalede PowerShellGet kullanarak Windows için PowerShell 5.x sürümlerine yönelik Azure PowerShell modüllerini yüklemek için uygulanması gereken adımlar açıklanır.</span><span class="sxs-lookup"><span data-stu-id="7cefb-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="7cefb-105">PowerShellGet ve modül yönetimi, Azure PowerShell'i yüklemek için tercih edilen yoldur. Ancak bunun yerine Web Platformu Yükleyicisi veya MSI paketi kullanarak yükleyecekseniz bkz. [Diğer yükleme yöntemleri](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="7cefb-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="7cefb-106">Azure klasik dağıtım modeli, Azure PowerShell'in bu sürümü tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="7cefb-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="7cefb-107">Klasik dağıtımlar için [Azure PowerShell Service Management modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps) talimatlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="7cefb-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7cefb-108">AzureRM modülü macOS veya Linux için desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="7cefb-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="7cefb-109">Azure PowerShell cmdlet'lerini bu platformlarda kullanmak için [Az modülünü yükleyin](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="7cefb-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="7cefb-110">1\. Adım: PowerShellGet yükleme</span><span class="sxs-lookup"><span data-stu-id="7cefb-110">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="7cefb-111">PowerShell Galerisi’nden yükleme yapabilmek için PowerShellGet modülü gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="7cefb-112">Uygun PowerShellGet sürümüne ve diğer sistem gereksinimlerine sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7cefb-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="7cefb-113">PowerShellGet’in sisteminizde yüklü olup olmadığını görmek için aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7cefb-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="7cefb-114">Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="7cefb-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="7cefb-115">PowerShellGet 1.1.2.0 veya üzeri bir sürüm gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="7cefb-116">PowerShellGet’i güncelleştirmek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="7cefb-116">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="7cefb-117">PowerShellGet yüklü değilse bu makalenin [PowerShellGet edinme](#how-to-get-powershellget) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="7cefb-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="7cefb-118">PowerShellGet kullanımı, betikleri çalıştırmanıza olanak tanıyan bir Yürütme İlkesi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="7cefb-119">PowerShell'in Yürütme İlkesi hakkında daha fazla bilgi için bkz. [Yürütme İlkeleri Hakkında](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="7cefb-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="7cefb-120">Bu belgede açıklanan AzureRM modülü .NET Framework kullanır.</span><span class="sxs-lookup"><span data-stu-id="7cefb-120">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="7cefb-121">Bu da, .NET Core kullanan PowerShell 6.0 ile uyumsuz olmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="7cefb-121">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="7cefb-122">PowerShell 6.0 kullanıyorsanız, [macOS ve Linux için yükleme yönergelerini](/powershell/azure/install-az-ps) izleyin.</span><span class="sxs-lookup"><span data-stu-id="7cefb-122">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="7cefb-123">2\. Adım: Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="7cefb-123">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="7cefb-124">Azure PowerShell’in PowerShell Galerisi’nden yüklenebilmesi için yükseltilmiş ayrıcalıklar gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-124">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="7cefb-125">Yükseltilmiş bir PowerShell oturumunda aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="7cefb-125">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="7cefb-126">PowerShell Galerisi varsayılan olarak PowerShellGet için Güvenilir depo şeklinde yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="7cefb-126">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="7cefb-127">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="7cefb-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="7cefb-128">Yükleme işlemine devam etmek için "Evet" veya "Tümüne Evet" yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="7cefb-128">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="7cefb-129">NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-129">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="7cefb-130">AzureRM modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="7cefb-130">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="7cefb-131">AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş diğer Azure PowerShell modülleri PowerShell Galerisi'nden indirilir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-131">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="7cefb-132">Azure PowerShell'in önceki sürümlerinden biri sisteminizde yüklüyse hata iletisiyle karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cefb-132">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="7cefb-133">Bu sorunu çözmek için bu makalenin [Azure PowerShell'in yeni bir sürümüne güncelleştirme](#update-azps) bölümünü inceleyin.</span><span class="sxs-lookup"><span data-stu-id="7cefb-133">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="7cefb-134">3\. Adım: AzureRM modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="7cefb-134">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="7cefb-135">Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-135">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="7cefb-136">Bunu normal (yükseltilmiş olmayan) bir PowerShell oturumunda yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-136">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="7cefb-137">Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:</span><span class="sxs-lookup"><span data-stu-id="7cefb-137">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="7cefb-138">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="7cefb-138">Next Steps</span></span>

<span data-ttu-id="7cefb-139">Azure PowerShell kullanma hakkında daha fazla bilgi için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="7cefb-139">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="7cefb-140">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="7cefb-140">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="7cefb-141">Sorunları bildirme ve geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="7cefb-141">Reporting issues and feedback</span></span>

<span data-ttu-id="7cefb-142">Araçla ilgili bir hatayla karşılaşırsanız, GitHub deposunun [Sorunlar](https://github.com/Azure/azure-powershell/issues) bölümünden sorunu bildirin.</span><span class="sxs-lookup"><span data-stu-id="7cefb-142">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="7cefb-143">Komut satırından geri bildirim sağlamak için `Send-Feedback` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7cefb-143">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="7cefb-144">Sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="7cefb-144">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="7cefb-145">PowerShellGet edinme</span><span class="sxs-lookup"><span data-stu-id="7cefb-145">How to get PowerShellGet</span></span>

|<span data-ttu-id="7cefb-146">İşletim Sistemi Sürümü</span><span class="sxs-lookup"><span data-stu-id="7cefb-146">OS Version</span></span>|<span data-ttu-id="7cefb-147">Yükleme yönergeleri</span><span class="sxs-lookup"><span data-stu-id="7cefb-147">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="7cefb-148">Bilgisayarımda Windows 10 veya Windows Server 2016 yüklü</span><span class="sxs-lookup"><span data-stu-id="7cefb-148">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="7cefb-149">İşletim sisteminde bulunan Windows Management Framework (WMF) 5.0’da yerleşiktir</span><span class="sxs-lookup"><span data-stu-id="7cefb-149">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="7cefb-150">PowerShell 5'e yükseltme yapmak istiyorum</span><span class="sxs-lookup"><span data-stu-id="7cefb-150">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="7cefb-151">WMF’nin en son sürümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="7cefb-151">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="7cefb-152">Azure PowerShell sürümünü denetleme</span><span class="sxs-lookup"><span data-stu-id="7cefb-152">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="7cefb-153">En son sürüme mümkün olan en kısa sürede yükseltme yapmanız önerilse de, Azure PowerShell’in birkaç sürümü desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-153">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="7cefb-154">Azure PowerShell'in yüklü olan sürümünü belirlemek için komut satırından `Get-InstalledModule AzureRM` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7cefb-154">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule AzureRM` from your command line.</span></span>

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="7cefb-155">Klasik dağıtım yöntemleri için destek</span><span class="sxs-lookup"><span data-stu-id="7cefb-155">Support for classic deployment methods</span></span>

<span data-ttu-id="7cefb-156">Klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cefb-156">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="7cefb-157">Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="7cefb-157">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="7cefb-158">Azure ve AzureRM modülleri ortak bağımlılıklara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-158">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="7cefb-159">Hem Azure hem de AzureRM modüllerini kullanıyorsanız her paket için aynı sürümü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-159">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="7cefb-160">Azure PowerShell’in yeni bir sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7cefb-160">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="7cefb-161">Hizmet Yönetimi modülünü içeren eski bir Azure PowerShell sürümü yüklüyse şu hata iletisiyle karşılaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7cefb-161">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="7cefb-162">Hata iletisinde de belirtildiği üzere modülü yüklemek için -AllowClobber parametresini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-162">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="7cefb-163">Aşağıdaki komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="7cefb-163">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="7cefb-164">Daha fazla bilgi için [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) yardım konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7cefb-164">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="7cefb-165">Modül sürümlerini yan yana yükleme</span><span class="sxs-lookup"><span data-stu-id="7cefb-165">Installing module versions side by side</span></span>

<span data-ttu-id="7cefb-166">PowerShellGet yükleme yöntemi, birden fazla sürümün yüklenmesini destekleyen tek yöntemdir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-166">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="7cefb-167">Örneğin, güncelleştirmek için zaman veya kaynaklara sahip olmadığınız önceki bir Azure PowerShell sürümünü kullanarak yazdığınız betikler olabilir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-167">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="7cefb-168">Aşağıdaki komutlar birden fazla Azure PowerShell sürümünün nasıl yükleneceğini göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="7cefb-168">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="7cefb-169">Bir PowerShell oturumunda modülün yalnızca bir sürümü yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-169">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="7cefb-170">AzureRM cmdlet’lerinin belirli bir sürümünü içeri aktarmak için yeni bir PowerShell penceresi açıp `Import-Module` seçeneğini kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="7cefb-170">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> <span data-ttu-id="7cefb-171">Sürüm 2.1.0 ve sürüm 1.2.6, yan yana yüklenip kullanılmak üzere tasarlanmış ilk modül sürümleridir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-171">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="7cefb-172">Azure PowerShell'in önceki sürümlerinden biri yüklenirken **AzureRM.Profile** modülünün uyumlu olmayan sürümleri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-172">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="7cefb-173">Bu işlemin sonucunda cmdlet'leri her çalıştırdığınızda oturum açmanız istenir.</span><span class="sxs-lookup"><span data-stu-id="7cefb-173">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="7cefb-174">Diğer yükleme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="7cefb-174">Other installation methods</span></span>

<span data-ttu-id="7cefb-175">Web Platformu Yükleyicisi veya MSI Paketi kullanarak yükleme hakkında bilgi için bkz. [Diğer yükleme yöntemleri](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="7cefb-175">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
