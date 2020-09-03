---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 17a9b604da84f131c434e3001732a34f7d620fbd
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243591"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="a765b-103">Azure PowerShell modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="a765b-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="a765b-104">Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="a765b-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="a765b-105">Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz lütfen [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.</span><span class="sxs-lookup"><span data-stu-id="a765b-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="a765b-106">Bir hatayla karşılaştıysanız [bir GitHub sorunu girerek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.</span><span class="sxs-lookup"><span data-stu-id="a765b-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="a765b-107">MSI veya Web Platformu Yükleyicisi ile kaldırma</span><span class="sxs-lookup"><span data-stu-id="a765b-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="a765b-108">Azure PowerShell'i MSI paketini veya Web Platformu Yükleyicisi'ni kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a765b-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="a765b-109">Platform</span><span class="sxs-lookup"><span data-stu-id="a765b-109">Platform</span></span> | <span data-ttu-id="a765b-110">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="a765b-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="a765b-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a765b-111">Windows 10</span></span> | <span data-ttu-id="a765b-112">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="a765b-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="a765b-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a765b-113">Windows 7</span></span> </br><span data-ttu-id="a765b-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a765b-114">Windows 8</span></span> | <span data-ttu-id="a765b-115">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="a765b-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="a765b-116">Bu ekrandaki program listesinde "Azure PowerShell"i bulabilir ve kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a765b-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="a765b-117">PowerShell'den kaldırma</span><span class="sxs-lookup"><span data-stu-id="a765b-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="a765b-118">Azure PowerShell'i PowerShellGet kullanarak yüklediyseniz [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a765b-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="a765b-119">Ancak `Uninstall-Module` yalnızca bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a765b-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="a765b-120">Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a765b-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="a765b-121">Birden fazla Azure PowerShell sürümü yüklüyse kaldırma işlemi karmaşık hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="a765b-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="a765b-122">Azure PowerShell'in tek bir sürümünü tamamen kaldırmak için aşağıdaki betiği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a765b-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="a765b-123">Betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="a765b-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="a765b-124">Ardından her alt modülün doğru sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a765b-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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

<span data-ttu-id="a765b-125">Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="a765b-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="a765b-126">Aşağıdaki örnekte bu işlevi Azure PowerShell'in eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a765b-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="a765b-127">Betik çalışırken kaldırılan alt modüllerin adını ve sürümünü görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a765b-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="a765b-128">Bu işlem sonucunda nelerin silineceğini bu öğeleri silmeden öğrenmek için `-WhatIf` seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a765b-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="a765b-129">Bu betik, kaldırmak için bağımlılığın aynı sürümüyle tam olarak eşleşemezse, o bağımlılığın _hiçbir_ sürümünü kaldırmaz.</span><span class="sxs-lookup"><span data-stu-id="a765b-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="a765b-130">Bunun sebebi, sisteminizde hedef bağımlılıkları kullanan diğer hedef modülü sürümlerinin bulunması olabilir.</span><span class="sxs-lookup"><span data-stu-id="a765b-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="a765b-131">Bu durumda, bağımlılığın kullanılabilir sürümleri listelenir.</span><span class="sxs-lookup"><span data-stu-id="a765b-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="a765b-132">`Uninstall-Module` ile herhangi bir eski sürümü kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a765b-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="a765b-133">Bu komutu kaldırmak istediğiniz her Azure PowerShell sürümü için çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a765b-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="a765b-134">Kolaylık sağlamak için, aşağıdaki betik AzureRM'nin en son sürümü __dışındaki__ tüm sürümlerini kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="a765b-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
