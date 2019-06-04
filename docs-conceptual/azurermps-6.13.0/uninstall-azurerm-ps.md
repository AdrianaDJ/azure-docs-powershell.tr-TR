---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 11/30/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 79c34ea74887113be3683e32ab9a03ed4c7daa7c
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534480"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="d0ecb-103">Azure PowerShell modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="d0ecb-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="d0ecb-104">Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="d0ecb-105">Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="d0ecb-106">Bir hatayla karşılaştığınızda [bir GitHub sorunu girerek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>


## <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="d0ecb-107">Azure PowerShell MSI'yi kaldırma</span><span class="sxs-lookup"><span data-stu-id="d0ecb-107">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="d0ecb-108">Azure PowerShell'i MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="d0ecb-109">Platform</span><span class="sxs-lookup"><span data-stu-id="d0ecb-109">Platform</span></span> | <span data-ttu-id="d0ecb-110">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="d0ecb-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="d0ecb-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d0ecb-111">Windows 10</span></span> | <span data-ttu-id="d0ecb-112">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="d0ecb-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="d0ecb-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d0ecb-113">Windows 7</span></span> </br><span data-ttu-id="d0ecb-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d0ecb-114">Windows 8</span></span> | <span data-ttu-id="d0ecb-115">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="d0ecb-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="d0ecb-116">Bu ekrandaki program listesinde __Azure PowerShell__'i görebilmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="d0ecb-117">Kaldırılacak olan uygulama budur.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-117">This is the app to uninstall.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="d0ecb-118">PowerShell'den kaldırma</span><span class="sxs-lookup"><span data-stu-id="d0ecb-118">Uninstall from PowerShell</span></span>

<span data-ttu-id="d0ecb-119">Azure PowerShell'i PowerShellGet kullanarak yüklediyseniz [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-119">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="d0ecb-120">Ancak `Uninstall-Module` yalnızca bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-120">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="d0ecb-121">Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-121">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="d0ecb-122">Birden çok Azure PowerShell sürümü yüklediyseniz kaldırma işlemi karmaşık hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-122">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="d0ecb-123">Şu anda sahip olduğunuz Azure PowerShell sürümlerini öğrenmek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="d0ecb-123">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="d0ecb-124">Aşağıdaki betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-124">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="d0ecb-125">Ardından her alt modülün doğru sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-125">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="d0ecb-126">Bu betiği `Process` veya `CurrentUser` haricinde başka bir kapsamda çalıştırmak için yönetici erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-126">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="d0ecb-127">Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-127">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="d0ecb-128">Aşağıdaki örnekte bu işlevi Azure PowerShell'in eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-128">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="d0ecb-129">Betik çalışırken kaldırılan alt modüllerin adını ve sürümünü görüntüler.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-129">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="d0ecb-130">Bu işlem sonucunda nelerin silineceğini bu öğeleri silmeden öğrenmek için `-WhatIf` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-130">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="d0ecb-131">Bu komutu kaldırmak istediğiniz her Azure PowerShell sürümü için çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-131">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="d0ecb-132">Kolaylık sağlamak için, aşağıdaki betik AzureRM'nin en son sürümü __dışındaki__ tüm sürümlerini kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="d0ecb-132">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
