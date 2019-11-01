---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 10/22/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 772667032d421e32c6cd63abbcb686b4eab308e2
ms.sourcegitcommit: ad7677d703a8512d371d3123dc7e541156b95cb8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2019
ms.locfileid: "72814350"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="147db-103">Azure PowerShell modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="147db-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="147db-104">Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="147db-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="147db-105">Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.</span><span class="sxs-lookup"><span data-stu-id="147db-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="147db-106">Bir hatayla karşılaştıysanız, bunun düzeltilebilmesi için [bir GitHub sorunu kaydederek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.</span><span class="sxs-lookup"><span data-stu-id="147db-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="147db-107">Azure PowerShell'i MSI'den kaldırma</span><span class="sxs-lookup"><span data-stu-id="147db-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="147db-108">Azure PowerShell'i MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="147db-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="147db-109">Platform</span><span class="sxs-lookup"><span data-stu-id="147db-109">Platform</span></span> | <span data-ttu-id="147db-110">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="147db-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="147db-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="147db-111">Windows 10</span></span> | <span data-ttu-id="147db-112">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="147db-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="147db-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="147db-113">Windows 7</span></span> </br><span data-ttu-id="147db-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="147db-114">Windows 8</span></span> | <span data-ttu-id="147db-115">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="147db-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="147db-116">Bu ekrandaki program listesinde __Azure PowerShell__'i görebilmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="147db-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="147db-117">Kaldırılacak olan uygulama budur.</span><span class="sxs-lookup"><span data-stu-id="147db-117">This is the app to uninstall.</span></span> <span data-ttu-id="147db-118">Listede bu programı görmüyorsanız, PowerShellGet aracılığıyla yüklemiş olmalısınız ve sonraki yönergeleri izlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="147db-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershell-get"></a><span data-ttu-id="147db-119">Azure PowerShell'i PowerShell Get'ten kaldırma</span><span class="sxs-lookup"><span data-stu-id="147db-119">Uninstall Azure PowerShell from PowerShell Get</span></span>

<span data-ttu-id="147db-120">Az modüllerini kaldırmak için [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="147db-120">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="147db-121">Ancak `Uninstall-Module` yalnızca bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="147db-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="147db-122">Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="147db-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="147db-123">Birden çok Azure PowerShell sürümü yüklediyseniz kaldırma işlemi karmaşık hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="147db-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="147db-124">Şu anda sahip olduğunuz Azure PowerShell sürümlerini öğrenmek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="147db-124">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="147db-125">Aşağıdaki betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="147db-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="147db-126">Ardından her alt modülün doğru sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="147db-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="147db-127">Bu betiği `Process` veya `CurrentUser` haricinde başka bir kapsamda çalıştırmak için yönetici erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="147db-127">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="147db-128">Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="147db-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="147db-129">Aşağıdaki örnekte bu işlevi Azure PowerShell'in eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="147db-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="147db-130">Betik çalışırken kaldırılan alt modüllerin adını ve sürümünü görüntüler.</span><span class="sxs-lookup"><span data-stu-id="147db-130">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="147db-131">Bu işlem sonucunda nelerin silineceğini bu öğeleri silmeden öğrenmek için `-WhatIf` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="147db-131">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="147db-132">Bu betik, kaldırmak için bağımlılığın aynı sürümüyle tam olarak eşleşemezse, o bağımlılığın _hiçbir_ sürümünü kaldırmaz.</span><span class="sxs-lookup"><span data-stu-id="147db-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="147db-133">Bunun sebebi, sisteminizde hedef bağımlılıkları kullanan diğer hedef modülü sürümlerinin bulunması olabilir.</span><span class="sxs-lookup"><span data-stu-id="147db-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="147db-134">Bu durumda, bağımlılığın kullanılabilir sürümleri listelenir.</span><span class="sxs-lookup"><span data-stu-id="147db-134">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="147db-135">`Uninstall-Module` ile herhangi bir eski sürümü kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="147db-135">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="147db-136">Bu komutu kaldırmak istediğiniz her Azure PowerShell sürümü için çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="147db-136">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="147db-137">Kolaylık sağlamak için, aşağıdaki betik Az'nin en son sürümü __dışındaki__ tüm sürümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="147db-137">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="147db-138">AzureRM modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="147db-138">Uninstall the AzureRM module</span></span>

<span data-ttu-id="147db-139">Sisteminizde Az modülü yüklüyse ve AzureRM’yi kaldırmak istiyorsanız, yukarıdaki `Uninstall-AllModules` betiğini çalıştırmanızı gerektirmeyen iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="147db-139">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="147db-140">Hangi yöntemi kullanacağınız, AzureRM modülünü nasıl yüklediğinize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="147db-140">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="147db-141">Başlangıçta hangi yükleme yöntemini kullandığınızdan emin değilseniz önce MSI kaldırma adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="147db-141">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="147db-142">Azure PowerShell MSI'yi kaldırma</span><span class="sxs-lookup"><span data-stu-id="147db-142">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="147db-143">Azure PowerShell AzureRM modüllerini MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="147db-143">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="147db-144">Platform</span><span class="sxs-lookup"><span data-stu-id="147db-144">Platform</span></span> | <span data-ttu-id="147db-145">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="147db-145">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="147db-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="147db-146">Windows 10</span></span> | <span data-ttu-id="147db-147">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="147db-147">Start > Settings > Apps</span></span> |
| <span data-ttu-id="147db-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="147db-148">Windows 7</span></span> </br><span data-ttu-id="147db-149">Windows 8</span><span class="sxs-lookup"><span data-stu-id="147db-149">Windows 8</span></span> | <span data-ttu-id="147db-150">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="147db-150">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="147db-151">Bu ekrandaki program listesinde __Azure PowerShell__'i görebilmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="147db-151">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="147db-152">Kaldırılacak olan uygulama budur.</span><span class="sxs-lookup"><span data-stu-id="147db-152">This is the app to uninstall.</span></span> <span data-ttu-id="147db-153">Listede bu programı görmüyorsanız, PowerShellGet aracılığıyla yüklemiş olmalısınız ve sonraki yönergeleri izlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="147db-153">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="147db-154">PowerShell'den kaldırma</span><span class="sxs-lookup"><span data-stu-id="147db-154">Uninstall from PowerShell</span></span>

<span data-ttu-id="147db-155">AzureRM'yi PowerShellGet ile yüklediyseniz modülleri `Az.Accounts` modülünün bir parçası olan [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) komutuyla kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="147db-155">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="147db-156">Bu işlem _tüm_ AzureRM modüllerini makinenizden kaldırır, ancak yönetici ayrıcalıkları gerektirir.</span><span class="sxs-lookup"><span data-stu-id="147db-156">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="147db-157">`Uninstall-AzureRM` komutunu başarılı bir şekilde çalıştıramazsanız aşağıdaki çağrıyla bu makalede sağlanan [`Uninstall-AllModules` betiğini](#uninstall-script) kullanın:</span><span class="sxs-lookup"><span data-stu-id="147db-157">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```