---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 3828a6f9d60a68c2837cc201a50d8707324f4f0a
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587236"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="8e056-103">Azure PowerShell modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e056-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="8e056-104">Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="8e056-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="8e056-105">Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz lütfen [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.</span><span class="sxs-lookup"><span data-stu-id="8e056-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="8e056-106">Bir hatayla karşılaştıysanız [bir GitHub sorunu girerek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.</span><span class="sxs-lookup"><span data-stu-id="8e056-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="8e056-107">MSI veya Web Platformu Yükleyicisi ile kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e056-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="8e056-108">Azure PowerShell'i MSI paketini veya Web Platformu Yükleyicisi'ni kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e056-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="8e056-109">Platform</span><span class="sxs-lookup"><span data-stu-id="8e056-109">Platform</span></span> | <span data-ttu-id="8e056-110">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="8e056-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="8e056-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8e056-111">Windows 10</span></span> | <span data-ttu-id="8e056-112">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="8e056-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="8e056-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e056-113">Windows 7</span></span> </br><span data-ttu-id="8e056-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8e056-114">Windows 8</span></span> | <span data-ttu-id="8e056-115">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="8e056-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="8e056-116">Bu ekrandaki program listesinde "Azure PowerShell"i bulabilir ve kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e056-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="8e056-117">PowerShell'den kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e056-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="8e056-118">Azure PowerShell'i PowerShellGet kullanarak yüklediyseniz [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e056-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="8e056-119">Ancak `Uninstall-Module` yalnızca bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e056-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="8e056-120">Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e056-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="8e056-121">Birden fazla Azure PowerShell sürümü yüklüyse kaldırma işlemi karmaşık hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="8e056-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="8e056-122">Azure PowerShell'in tek bir sürümünü tamamen kaldırmak için aşağıdaki betiği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e056-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="8e056-123">Betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8e056-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="8e056-124">Ardından her alt modülün doğru sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e056-124">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="8e056-125">Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="8e056-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="8e056-126">Aşağıdaki örnekte bu işlevi Azure PowerShell'in eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e056-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="8e056-127">Betik çalışırken kaldırılan alt modüllerin adını ve sürümünü görüntüler.</span><span class="sxs-lookup"><span data-stu-id="8e056-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="8e056-128">Bu komutu kaldırmak istediğiniz her Azure PowerShell sürümü için çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="8e056-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>