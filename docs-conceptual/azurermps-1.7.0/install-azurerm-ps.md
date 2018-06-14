---
title: Azure PowerShell'i yükleme ve yapılandırma | Microsoft Docs
description: Azure PowerShell’i ilk kez kullanmak üzere yükleme ve yapılandırma.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/17/2017
ms.openlocfilehash: f35f6a01d4a287fff535c8c34423d470479ff854
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853908"
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="873bd-103">Azure PowerShell'i yükleyip yapılandırma</span><span class="sxs-lookup"><span data-stu-id="873bd-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="873bd-104">Azure PowerShell'in PowerShell Galerisi'nden yüklenmesi, tercih edilen yükleme yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="873bd-104">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="873bd-105">1. Adım: PowerShellGet yükleme</span><span class="sxs-lookup"><span data-stu-id="873bd-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="873bd-106">PowerShell Galerisi’nden yükleme yapabilmek için PowerShellGet modülü gerekir.</span><span class="sxs-lookup"><span data-stu-id="873bd-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="873bd-107">Uygun PowerShellGet sürümüne ve diğer sistem gereksinimlerine sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="873bd-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="873bd-108">PowerShellGet’in sisteminizde yüklü olup olmadığını görmek için aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="873bd-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="873bd-109">Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="873bd-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="873bd-110">PowerShellGet yüklü değilse bu makalenin [PowerShellGet edinme](#how-to-get-powershellget) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="873bd-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="873bd-111">PowerShellGet kullanımı, betikleri çalıştırmanıza olanak tanıyan bir Yürütme İlkesi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="873bd-111">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="873bd-112">PowerShell'in Yürütme İlkesi hakkında daha fazla bilgi için bkz. [Yürütme İlkeleri Hakkında](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span><span class="sxs-lookup"><span data-stu-id="873bd-112">For more information about PowerShell's Execution Policy, see [About Execution Policies](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="873bd-113">2. Adım: Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="873bd-113">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="873bd-114">Azure PowerShell’in PowerShell Galerisi’nden yüklenebilmesi için yükseltilmiş ayrıcalıklar gerekir.</span><span class="sxs-lookup"><span data-stu-id="873bd-114">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="873bd-115">Yükseltilmiş bir PowerShell oturumunda aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="873bd-115">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM
```

<span data-ttu-id="873bd-116">PowerShell Galerisi varsayılan olarak PowerShellGet için Güvenilir depo şeklinde yapılandırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="873bd-116">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="873bd-117">PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:</span><span class="sxs-lookup"><span data-stu-id="873bd-117">The first time you use the PSGallery you see the following prompt:</span></span>

```
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="873bd-118">Yükleme işlemine devam etmek için "Evet" veya "Tümüne Evet" yanıtını verin.</span><span class="sxs-lookup"><span data-stu-id="873bd-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="873bd-119">NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="873bd-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="873bd-120">AzureRM modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="873bd-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="873bd-121">AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş diğer Azure PowerShell modülleri PowerShell Galerisi'nden indirilir.</span><span class="sxs-lookup"><span data-stu-id="873bd-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="873bd-122">Azure PowerShell'in önceki sürümlerinden biri sisteminizde yüklüyse hata iletisiyle karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="873bd-122">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="873bd-123">Bu sorunu çözmek için bu makalenin [Azure PowerShell'in yeni bir sürümüne güncelleştirme](#update-azps) bölümünü inceleyin.</span><span class="sxs-lookup"><span data-stu-id="873bd-123">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="873bd-124">3. Adım: AzureRM modülünü yükleme</span><span class="sxs-lookup"><span data-stu-id="873bd-124">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="873bd-125">Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="873bd-125">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="873bd-126">Bunu normal (yükseltilmiş olmayan) bir PowerShell oturumunda yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="873bd-126">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="873bd-127">Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:</span><span class="sxs-lookup"><span data-stu-id="873bd-127">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="873bd-128">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="873bd-128">Next Steps</span></span>

<span data-ttu-id="873bd-129">Azure PowerShell kullanma hakkında daha fazla bilgi için aşağıdaki makalelere bakın:</span><span class="sxs-lookup"><span data-stu-id="873bd-129">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="873bd-130">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="873bd-130">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="873bd-131">Sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="873bd-131">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="873bd-132">PowerShellGet edinme</span><span class="sxs-lookup"><span data-stu-id="873bd-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="873bd-133">İşletim Sistemi Sürümü</span><span class="sxs-lookup"><span data-stu-id="873bd-133">OS Version</span></span>|<span data-ttu-id="873bd-134">Yükleme yönergeleri</span><span class="sxs-lookup"><span data-stu-id="873bd-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="873bd-135">Bilgisayarımda Windows 10 veya Windows Server 2016 yüklü</span><span class="sxs-lookup"><span data-stu-id="873bd-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="873bd-136">İşletim sisteminde bulunan Windows Management Framework (WMF) 5.0’da yerleşiktir</span><span class="sxs-lookup"><span data-stu-id="873bd-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="873bd-137">PowerShell 5'e yükseltme yapmak istiyorum</span><span class="sxs-lookup"><span data-stu-id="873bd-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="873bd-138">WMF’nin en son sürümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="873bd-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="873bd-139">Windows’un PowerShell 3 veya PowerShell 4 içeren bir sürümünü çalıştırıyorum</span><span class="sxs-lookup"><span data-stu-id="873bd-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="873bd-140">PackageManagement modüllerini alın</span><span class="sxs-lookup"><span data-stu-id="873bd-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="873bd-141">Azure PowerShell sürümünü denetleme</span><span class="sxs-lookup"><span data-stu-id="873bd-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="873bd-142">En son sürüme mümkün olan en kısa sürede yükseltme yapmanız önerilse de, Azure PowerShell’in birkaç sürümü desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="873bd-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="873bd-143">Azure PowerShell'in yüklü olan sürümünü belirlemek için komut satırından `Get-Module AzureRM` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="873bd-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="873bd-144">Klasik dağıtım yöntemleri için destek</span><span class="sxs-lookup"><span data-stu-id="873bd-144">Support for classic deployment methods</span></span>

<span data-ttu-id="873bd-145">Klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="873bd-145">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="873bd-146">Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="873bd-146">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="873bd-147">Azure ve AzureRM modülleri ortak bağımlılıklara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="873bd-147">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="873bd-148">Hem Azure hem de AzureRM modüllerini kullanıyorsanız her paket için aynı sürümü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="873bd-148">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="873bd-149">Azure PowerShell'in yeni bir sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="873bd-149">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="873bd-150">Hizmet Yönetimi modülünü içeren eski bir Azure PowerShell sürümü yüklüyse şu hata iletisiyle karşılaşabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="873bd-150">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="873bd-151">Hata iletisinde de belirtildiği üzere modülü yüklemek için -AllowClobber parametresini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="873bd-151">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="873bd-152">Aşağıdaki komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="873bd-152">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

<span data-ttu-id="873bd-153">Daha fazla bilgi için [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) yardım konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="873bd-153">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="873bd-154">Modül sürümlerini yan yana yükleme</span><span class="sxs-lookup"><span data-stu-id="873bd-154">Installing module versions side by side</span></span>

<span data-ttu-id="873bd-155">PowerShellGet yükleme yöntemi, birden fazla sürümün yüklenmesini destekleyen tek yöntemdir.</span><span class="sxs-lookup"><span data-stu-id="873bd-155">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="873bd-156">Örneğin, güncelleştirmek için zaman veya kaynaklara sahip olmadığınız önceki bir Azure PowerShell sürümünü kullanarak yazdığınız betikler olabilir.</span><span class="sxs-lookup"><span data-stu-id="873bd-156">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="873bd-157">Aşağıdaki komutlar birden fazla Azure PowerShell sürümünün nasıl yükleneceğini göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="873bd-157">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="873bd-158">Bir PowerShell oturumunda modülün yalnızca bir sürümü yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="873bd-158">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="873bd-159">AzureRM cmdlet’lerinin belirli bir sürümünü içeri aktarmak için yeni bir PowerShell penceresi açıp `Import-Module` seçeneğini kullanmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="873bd-159">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="873bd-160">Sürüm 2.1.0 ve sürüm 1.2.6, yan yana yüklenip kullanılmak üzere tasarlanmış ilk modül sürümleridir.</span><span class="sxs-lookup"><span data-stu-id="873bd-160">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="873bd-161">Azure PowerShell'in önceki sürümlerinden biri yüklenirken **AzureRM.Profile** modülünün uyumlu olmayan sürümleri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="873bd-161">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="873bd-162">Bu işlemin sonucunda cmdlet'leri her çalıştırdığınızda oturum açmanız istenir.</span><span class="sxs-lookup"><span data-stu-id="873bd-162">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="873bd-163">Diğer yükleme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="873bd-163">Other installation methods</span></span>

<span data-ttu-id="873bd-164">Web Platformu Yükleyicisi veya MSI Paketi kullanarak yükleme hakkında bilgi için bkz. [Diğer yükleme yöntemleri](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="873bd-164">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
