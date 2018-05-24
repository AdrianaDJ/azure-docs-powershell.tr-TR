---
title: Azure PowerShell'i yükleme ve yapılandırma | Microsoft Docs
description: Azure PowerShell’i ilk kez kullanmak üzere yükleme ve yapılandırma.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 0df1208db69fedcb61ca7e3e8fcf5d05dfef5379
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="266af-103">Azure PowerShell'i yükleyip yapılandırma</span><span class="sxs-lookup"><span data-stu-id="266af-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="266af-104">Bu makalede Azure PowerShell modüllerini Windows ortamına yüklemek için uygulanması gereken adımlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="266af-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="266af-105">Azure PowerShell'i macOS veya Linux'a yüklemek istiyorsanız şu makaleye bakın: [Azure PowerShell'i macOS ve Linux'ta yükleme ve yapılandırma](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="266af-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="266af-106">Sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="266af-106">System requirements</span></span>

<span data-ttu-id="266af-107">Azure PowerShell sürüm 6.0.0, PowerShell 5.0 (veya daha yüksek) sürümünü gerektirir.</span><span class="sxs-lookup"><span data-stu-id="266af-107">Azure PowerShell version 6.0.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="266af-108">Önceki Azure PowerShell sürümlerinin herhangi bir cmdlet’i çalıştırması için _en az_ sürüm 3.0 gerekiyordu. PowerShell 5.0’a yükseltme hakkında bilgi için lütfen [bu tabloya bakın](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="266af-108">Previous versions of Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.For information on upgrading to PowerShell 5.0, please see [this table](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="266af-109">1. Adım: PowerShellGet yükleme</span><span class="sxs-lookup"><span data-stu-id="266af-109">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="266af-110">Azure PowerShell'in PowerShell Galerisi'nden yüklenmesi, tercih edilen yükleme yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="266af-110">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

<span data-ttu-id="266af-111">PowerShell Galerisi’nden yükleme yapabilmek için PowerShellGet modülü gerekir.</span><span class="sxs-lookup"><span data-stu-id="266af-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="266af-112">Uygun PowerShellGet sürümüne ve diğer sistem gereksinimlerine sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="266af-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="266af-113">PowerShellGet’in sisteminizde yüklü olup olmadığını görmek için aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="266af-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="266af-114">Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="266af-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="266af-115">PowerShellGet 1.1.2.0 veya üzeri bir sürüm gereklidir.</span><span class="sxs-lookup"><span data-stu-id="266af-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="266af-116">PowerShellGet’i güncelleştirmek için şu komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="266af-116">To update PowerShellGet, use the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="266af-117">PowerShellGet yüklü değilse bu makalenin [PowerShellGet edinme](#how-to-get-powershellget) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="266af-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="266af-118">PowerShellGet kullanımı, betikleri çalıştırmanıza olanak tanıyan bir Yürütme İlkesi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="266af-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="266af-119">PowerShell'in Yürütme İlkesi hakkında daha fazla bilgi için bkz. [Yürütme İlkeleri Hakkında](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="266af-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="266af-120">2. Adım: Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="266af-120">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="266af-121">Azure PowerShell’in PowerShell Galerisi’nden yüklenebilmesi için yükseltilmiş ayrıcalıklar gerekir.</span><span class="sxs-lookup"><span data-stu-id="266af-121">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="266af-122">Yükseltilmiş bir PowerShell oturumunda aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="266af-122">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="266af-123">PowerShell Galerisi varsayılan olarak PowerShellGet için Güvenilir depo şeklinde yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="266af-123">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="266af-124">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="266af-124">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="266af-125">Yükleme işlemine devam etmek için "Evet" veya "Tümüne Evet" yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="266af-125">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="266af-126">NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="266af-126">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="266af-127">AzureRM modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="266af-127">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="266af-128">AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş diğer Azure PowerShell modülleri PowerShell Galerisi'nden indirilir.</span><span class="sxs-lookup"><span data-stu-id="266af-128">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="266af-129">Azure PowerShell'in önceki sürümlerinden biri sisteminizde yüklüyse hata iletisiyle karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="266af-129">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="266af-130">Bu sorunu çözmek için bu makalenin [Azure PowerShell'in yeni bir sürümüne güncelleştirme](#update-azps) bölümünü inceleyin.</span><span class="sxs-lookup"><span data-stu-id="266af-130">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="266af-131">3. Adım: AzureRM modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="266af-131">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="266af-132">Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="266af-132">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="266af-133">Bunu normal (yükseltilmiş olmayan) bir PowerShell oturumunda yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="266af-133">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="266af-134">Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:</span><span class="sxs-lookup"><span data-stu-id="266af-134">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="266af-135">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="266af-135">Next Steps</span></span>

<span data-ttu-id="266af-136">Azure PowerShell kullanma hakkında daha fazla bilgi için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="266af-136">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="266af-137">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="266af-137">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="266af-138">Sorunları bildirme ve geri bildirimde bulunma</span><span class="sxs-lookup"><span data-stu-id="266af-138">Reporting issues and feedback</span></span>

<span data-ttu-id="266af-139">Araçla ilgili bir hatayla karşılaşırsanız, GitHub deposunun [Sorunlar](https://github.com/Azure/azure-powershell/issues) bölümünden sorunu bildirin.</span><span class="sxs-lookup"><span data-stu-id="266af-139">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="266af-140">Komut satırından geri bildirim sağlamak için `Send-Feedback` cmdlet'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="266af-140">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="266af-141">Sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="266af-141">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="266af-142">PowerShellGet edinme</span><span class="sxs-lookup"><span data-stu-id="266af-142">How to get PowerShellGet</span></span>

|<span data-ttu-id="266af-143">Senaryo</span><span class="sxs-lookup"><span data-stu-id="266af-143">Scenario</span></span>|<span data-ttu-id="266af-144">Yükleme yönergeleri</span><span class="sxs-lookup"><span data-stu-id="266af-144">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="266af-145">Windows 10</span><span class="sxs-lookup"><span data-stu-id="266af-145">Windows 10</span></span><br/><span data-ttu-id="266af-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="266af-146">Windows Server 2016</span></span>|<span data-ttu-id="266af-147">İşletim sisteminde bulunan Windows Management Framework (WMF) 5.0’da yerleşiktir</span><span class="sxs-lookup"><span data-stu-id="266af-147">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="266af-148">PowerShell 5'e yükseltme yapmak istiyorum</span><span class="sxs-lookup"><span data-stu-id="266af-148">I want to upgrade to PowerShell 5</span></span>|<ol><li>[<span data-ttu-id="266af-149">WMF’nin en son sürümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="266af-149">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="266af-150">Şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="266af-150">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="266af-151">Windows’un PowerShell 3 veya PowerShell 4 içeren bir sürümünü çalıştırıyorum</span><span class="sxs-lookup"><span data-stu-id="266af-151">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="266af-152"><il>[PackageManagement modüllerini alın](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="266af-152"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="266af-153">Şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="266af-153">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="266af-154">Azure PowerShell sürümünü denetleme</span><span class="sxs-lookup"><span data-stu-id="266af-154">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="266af-155">En son sürüme mümkün olan en kısa sürede yükseltme yapmanız önerilse de, Azure PowerShell’in birkaç sürümü desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="266af-155">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="266af-156">Azure PowerShell'in yüklü olan sürümünü belirlemek için komut satırından `Get-Module AzureRM` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="266af-156">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="266af-157">Klasik dağıtım yöntemleri için destek</span><span class="sxs-lookup"><span data-stu-id="266af-157">Support for classic deployment methods</span></span>

<span data-ttu-id="266af-158">Klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="266af-158">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="266af-159">Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="266af-159">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="266af-160">Azure ve AzureRM modülleri ortak bağımlılıklara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="266af-160">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="266af-161">Hem Azure hem de AzureRM modüllerini kullanıyorsanız her paket için aynı sürümü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="266af-161">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="266af-162">Azure PowerShell'in yeni bir sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="266af-162">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="266af-163">Hizmet Yönetimi modülünü içeren eski bir Azure PowerShell sürümü yüklüyse şu hata iletisiyle karşılaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="266af-163">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

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

<span data-ttu-id="266af-164">Hata iletisinde de belirtildiği üzere modülü yüklemek için -AllowClobber parametresini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="266af-164">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="266af-165">Aşağıdaki komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="266af-165">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="266af-166">Daha fazla bilgi için [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) yardım konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="266af-166">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="266af-167">Modül sürümlerini yan yana yükleme</span><span class="sxs-lookup"><span data-stu-id="266af-167">Installing module versions side by side</span></span>

<span data-ttu-id="266af-168">PowerShellGet yükleme yöntemi, birden fazla sürümün yüklenmesini destekleyen tek yöntemdir.</span><span class="sxs-lookup"><span data-stu-id="266af-168">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="266af-169">Örneğin, güncelleştirmek için zaman veya kaynaklara sahip olmadığınız önceki bir Azure PowerShell sürümünü kullanarak yazdığınız betikler olabilir.</span><span class="sxs-lookup"><span data-stu-id="266af-169">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="266af-170">Aşağıdaki komutlar birden fazla Azure PowerShell sürümünün nasıl yükleneceğini göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="266af-170">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="266af-171">Bir PowerShell oturumunda modülün yalnızca bir sürümü yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="266af-171">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="266af-172">AzureRM cmdlet’lerinin belirli bir sürümünü içeri aktarmak için yeni bir PowerShell penceresi açıp `Import-Module` seçeneğini kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="266af-172">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="266af-173">Sürüm 2.1.0 ve sürüm 1.2.6, yan yana yüklenip kullanılmak üzere tasarlanmış ilk modül sürümleridir.</span><span class="sxs-lookup"><span data-stu-id="266af-173">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="266af-174">Azure PowerShell'in önceki sürümlerinden biri yüklenirken **AzureRM.Profile** modülünün uyumlu olmayan sürümleri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="266af-174">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="266af-175">Bu işlemin sonucunda cmdlet'leri her çalıştırdığınızda oturum açmanız istenir.</span><span class="sxs-lookup"><span data-stu-id="266af-175">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="266af-176">Diğer yükleme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="266af-176">Other installation methods</span></span>

<span data-ttu-id="266af-177">Web Platformu Yükleyicisi veya MSI Paketi kullanarak yükleme hakkında bilgi için bkz. [Diğer yükleme yöntemleri](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="266af-177">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
