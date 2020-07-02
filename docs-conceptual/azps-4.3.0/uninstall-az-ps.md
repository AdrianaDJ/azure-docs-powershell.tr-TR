---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 4b40a3aebab84176a48bcdb0ef818cfa05dea269
ms.sourcegitcommit: 747769a143ddebff39e78c2cc62a182401adddb9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2020
ms.locfileid: "85268347"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="89697-103">Azure PowerShell modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="89697-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="89697-104">Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="89697-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="89697-105">Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.</span><span class="sxs-lookup"><span data-stu-id="89697-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="89697-106">Bir hatayla karşılaştıysanız, bunun düzeltilebilmesi için [bir GitHub sorunu kaydederek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.</span><span class="sxs-lookup"><span data-stu-id="89697-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="89697-107">Azure PowerShell'i MSI'den kaldırma</span><span class="sxs-lookup"><span data-stu-id="89697-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="89697-108">Azure PowerShell'i MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="89697-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="89697-109">Platform</span><span class="sxs-lookup"><span data-stu-id="89697-109">Platform</span></span>         |                      <span data-ttu-id="89697-110">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="89697-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="89697-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="89697-111">Windows 10</span></span>               | <span data-ttu-id="89697-112">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="89697-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="89697-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89697-113">Windows 7</span></span> </br><span data-ttu-id="89697-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="89697-114">Windows 8</span></span> | <span data-ttu-id="89697-115">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="89697-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="89697-116">Bu ekrandaki program listesinde **Azure PowerShell**'i görebilmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="89697-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="89697-117">Kaldırılacak olan uygulama budur.</span><span class="sxs-lookup"><span data-stu-id="89697-117">This is the app to uninstall.</span></span> <span data-ttu-id="89697-118">Listede bu programı görmüyorsanız, PowerShellGet aracılığıyla yüklemiş olmalısınız ve sonraki yönergeleri izlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="89697-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershellget"></a><span data-ttu-id="89697-119">Azure PowerShell'i PowerShellGet'ten kaldırma</span><span class="sxs-lookup"><span data-stu-id="89697-119">Uninstall Azure PowerShell from PowerShellGet</span></span>

<span data-ttu-id="89697-120">Az modüllerini kaldırmak için [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet’ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89697-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="89697-121">Ancak `Uninstall-Module` yalnızca bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89697-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="89697-122">Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="89697-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="89697-123">Birden çok Azure PowerShell sürümü yüklediyseniz kaldırma işlemi karmaşık hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="89697-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="89697-124">Sahip olduğunuz Azure PowerShell sürümlerini öğrenmek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="89697-124">To check which versions of Azure PowerShell you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<a name="uninstall-script"/>

<span data-ttu-id="89697-125">Aşağıdaki betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="89697-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="89697-126">Ardından her alt modülün doğru sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89697-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="89697-127">Bu betiği **Process** veya **CurrentUser** haricinde başka bir kapsamda çalıştırmak için yönetici erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="89697-127">You need to have administrator access to run this script in a scope other than **Process** or **CurrentUser**.</span></span>

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

<span data-ttu-id="89697-128">Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="89697-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="89697-129">Aşağıdaki örnekte bu işlevi Azure PowerShell'in eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89697-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="89697-130">Betik çalışırken kaldırılan alt modüllerin **Adını**, **Sürümünü** ve **Durumunu** görüntüler.</span><span class="sxs-lookup"><span data-stu-id="89697-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="89697-131">Bu işlem sonucunda nelerin silineceğini bu öğeleri silmeden öğrenmek için `-WhatIf` parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="89697-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> <span data-ttu-id="89697-132">Bu betik, kaldırmak için bağımlılığın aynı sürümüyle tam olarak eşleşemezse, o bağımlılığın _hiçbir_ sürümünü kaldırmaz.</span><span class="sxs-lookup"><span data-stu-id="89697-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="89697-133">Bunun sebebi, sisteminizde hedef bağımlılıkları kullanan diğer hedef modülü sürümlerinin bulunması olabilir.</span><span class="sxs-lookup"><span data-stu-id="89697-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="89697-134">Aşağıdaki örneği kaldırmak istediğiniz her Azure PowerShell sürümü için çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="89697-134">Run the following example for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="89697-135">Kolaylık sağlamak için, aşağıdaki betik Az'nin en son sürümü **dışındaki** tüm sürümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89697-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions | 
    Sort-Object -Property Version -Descending | 
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="89697-136">AzureRM modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="89697-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="89697-137">Sisteminizde Az modülü yüklüyse ve AzureRM’yi kaldırmak istiyorsanız, yukarıdaki `Uninstall-AzModule` betiğini çalıştırmanızı gerektirmeyen iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="89697-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AzModule` script above.</span></span> <span data-ttu-id="89697-138">Hangi yöntemi kullanacağınız, AzureRM modülünü nasıl yüklediğinize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="89697-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="89697-139">Başlangıçta hangi yükleme yöntemini kullandığınızdan emin değilseniz önce MSI kaldırma adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="89697-139">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="89697-140">Azure PowerShell MSI'yi kaldırma</span><span class="sxs-lookup"><span data-stu-id="89697-140">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="89697-141">Azure PowerShell AzureRM modüllerini MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="89697-141">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="89697-142">Platform</span><span class="sxs-lookup"><span data-stu-id="89697-142">Platform</span></span>         |                      <span data-ttu-id="89697-143">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="89697-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="89697-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="89697-144">Windows 10</span></span>               | <span data-ttu-id="89697-145">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="89697-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="89697-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89697-146">Windows 7</span></span> </br><span data-ttu-id="89697-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="89697-147">Windows 8</span></span> | <span data-ttu-id="89697-148">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="89697-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="89697-149">Bu ekrandaki program listesinde **Azure PowerShell**'i veya **Microsoft Azure PowerShell - Ay Yıl**'ı görebilmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="89697-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="89697-150">Kaldırılacak olan uygulama budur.</span><span class="sxs-lookup"><span data-stu-id="89697-150">This is the app to uninstall.</span></span> <span data-ttu-id="89697-151">Listede bu programı görmüyorsanız, PowerShellGet aracılığıyla yüklemiş olmalısınız ve sonraki yönergeleri izlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="89697-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="89697-152">PowerShell'den kaldırma</span><span class="sxs-lookup"><span data-stu-id="89697-152">Uninstall from PowerShell</span></span>

<span data-ttu-id="89697-153">AzureRM'yi PowerShellGet ile yüklediyseniz modülleri `Az.Accounts` modülünün bir parçası olan [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet’iyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89697-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="89697-154">Aşağıdaki örnek _tüm_ AzureRM modüllerini makinenizden kaldırır, ancak bunun için yönetici ayrıcalıkları gerekir.</span><span class="sxs-lookup"><span data-stu-id="89697-154">The following example removes _all_ AzureRM modules from your machine but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="89697-155">`Uninstall-AzureRM` komutunu başarılı bir şekilde çalıştıramazsanız aşağıdaki çağrıyla bu makalede sağlanan [`Uninstall-AzModule` betiğini](#uninstall-script) kullanın:</span><span class="sxs-lookup"><span data-stu-id="89697-155">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AzModule` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name AzureRM -AllVersions
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```
