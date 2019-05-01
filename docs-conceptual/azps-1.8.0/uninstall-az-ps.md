---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 6a34ac1821c3cec359d0d64664d3f1689621b304
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068787"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="f3886-103">Azure PowerShell modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3886-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="f3886-104">Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="f3886-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="f3886-105">Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.</span><span class="sxs-lookup"><span data-stu-id="f3886-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="f3886-106">Bir hatayla karşılaştığınızda [bir GitHub sorunu girerek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.</span><span class="sxs-lookup"><span data-stu-id="f3886-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="f3886-107">Az modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3886-107">Uninstall the Az module</span></span>

<span data-ttu-id="f3886-108">Az modüllerini kaldırmak için [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet’ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3886-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="f3886-109">Ancak `Uninstall-Module` yalnızca bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3886-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="f3886-110">Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f3886-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="f3886-111">Birden çok Azure PowerShell sürümü yüklediyseniz kaldırma işlemi karmaşık hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="f3886-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="f3886-112">Şu anda sahip olduğunuz Azure PowerShell sürümlerini öğrenmek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="f3886-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="f3886-113">Aşağıdaki betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f3886-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="f3886-114">Ardından her alt modülün doğru sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3886-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="f3886-115">Bu betiği `Process` veya `CurrentUser` haricinde başka bir kapsamda çalıştırmak için yönetici erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f3886-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
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

<span data-ttu-id="f3886-116">Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="f3886-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="f3886-117">Aşağıdaki örnekte bu işlevi Azure PowerShell'in eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3886-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="f3886-118">Betik çalışırken kaldırılan alt modüllerin adını ve sürümünü görüntüler.</span><span class="sxs-lookup"><span data-stu-id="f3886-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="f3886-119">Bu işlem sonucunda nelerin silineceğini bu öğeleri silmeden öğrenmek için `-WhatIf` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3886-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="f3886-120">Bu komutu kaldırmak istediğiniz her Azure PowerShell sürümü için çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f3886-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="f3886-121">Kolaylık sağlamak için, aşağıdaki betik Az'nin en son sürümü __dışındaki__ tüm sürümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3886-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="f3886-122">AzureRM modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3886-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="f3886-123">Sisteminizde Az modülü yüklüyse ve AzureRM’yi kaldırmak istiyorsanız, yukarıdaki `Uninstall-AllModules` betiğini çalıştırmanızı gerektirmeyen iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="f3886-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="f3886-124">Hangi yöntemi kullanacağınız, AzureRM modülünü nasıl yüklediğinize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f3886-124">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="f3886-125">Nasıl yüklediğinizden emin değilseniz önce MSI kaldırma adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="f3886-125">If you're not sure, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="f3886-126">Azure PowerShell MSI'yi kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3886-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="f3886-127">Azure PowerShell AzureRM modüllerini MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f3886-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="f3886-128">Platform</span><span class="sxs-lookup"><span data-stu-id="f3886-128">Platform</span></span> | <span data-ttu-id="f3886-129">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="f3886-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="f3886-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f3886-130">Windows 10</span></span> | <span data-ttu-id="f3886-131">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="f3886-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="f3886-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3886-132">Windows 7</span></span> </br><span data-ttu-id="f3886-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f3886-133">Windows 8</span></span> | <span data-ttu-id="f3886-134">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="f3886-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="f3886-135">Bu ekrandaki program listesinde __Azure PowerShell__'i görebilmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f3886-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="f3886-136">Kaldırılacak olan uygulama budur.</span><span class="sxs-lookup"><span data-stu-id="f3886-136">This is the app to uninstall.</span></span> <span data-ttu-id="f3886-137">Listede bu programı görmüyorsanız, PowerShellGet aracılığıyla yüklemiş olmalısınız ve sonraki yönergeleri izlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f3886-137">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="f3886-138">PowerShell'den kaldırma</span><span class="sxs-lookup"><span data-stu-id="f3886-138">Uninstall from PowerShell</span></span>

<span data-ttu-id="f3886-139">AzureRM'yi PowerShellGet ile yüklediyseniz modülleri `Az.Accounts` modülünün bir parçası olan [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) komutuyla kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3886-139">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="f3886-140">Bu işlem _tüm_ AzureRM modüllerini makinenizden kaldırır, ancak yönetici ayrıcalıkları gerektirir.</span><span class="sxs-lookup"><span data-stu-id="f3886-140">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="f3886-141">`Uninstall-AzureRM` komutunu başarılı bir şekilde çalıştıramazsanız onun yerine bu makalede sağlanan `Uninstall-AllModules` betiğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3886-141">If you can't successfully run the `Uninstall-AzureRM` command, use the `Uninstall-AllModules` script provided in this article instead.</span></span>