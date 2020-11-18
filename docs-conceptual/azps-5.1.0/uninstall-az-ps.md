---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ec4ecc9902f700e12ce6b22c32b4e07b13b4d4dc
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715616"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a><span data-ttu-id="2928c-103">Azure PowerShell modüllerini yükleme</span><span class="sxs-lookup"><span data-stu-id="2928c-103">How to uninstall Azure PowerShell modules</span></span>

<span data-ttu-id="2928c-104">Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="2928c-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="2928c-105">Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.</span><span class="sxs-lookup"><span data-stu-id="2928c-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="2928c-106">Bir hatayla karşılaştıysanız, bunun düzeltilebilmesi için [bir GitHub sorunu kaydederek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.</span><span class="sxs-lookup"><span data-stu-id="2928c-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="2928c-107">Az modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="2928c-107">Uninstall the Az module</span></span>

<span data-ttu-id="2928c-108">Sisteminizde Az modülü yüklüyse ve bunu kaldırmak istiyorsanız iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="2928c-108">If you have the Az module installed on your system and would like to uninstall it, there are two options.</span></span> <span data-ttu-id="2928c-109">Hangi yöntemi kullanacağınız, Az modülünü nasıl yüklediğinize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2928c-109">Which method you follow depends on how you installed the Az module.</span></span> <span data-ttu-id="2928c-110">Özgün yükleme yönteminizden emin değilseniz önce MSI kaldırma adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="2928c-110">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="2928c-111">1\. Seçenek: Az PowerShell modülünü MSI’dan kaldırma</span><span class="sxs-lookup"><span data-stu-id="2928c-111">Option 1: Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="2928c-112">Az PowerShell modülünü MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2928c-112">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="2928c-113">Platform</span><span class="sxs-lookup"><span data-stu-id="2928c-113">Platform</span></span>         |                      <span data-ttu-id="2928c-114">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="2928c-114">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="2928c-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2928c-115">Windows 10</span></span>               | <span data-ttu-id="2928c-116">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="2928c-116">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="2928c-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2928c-117">Windows 7</span></span> </br><span data-ttu-id="2928c-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2928c-118">Windows 8</span></span> | <span data-ttu-id="2928c-119">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="2928c-119">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="2928c-120">Bu ekrandaki program listesinde **Azure PowerShell**'i görebilmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2928c-120">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="2928c-121">Kaldırılacak olan uygulama budur.</span><span class="sxs-lookup"><span data-stu-id="2928c-121">This is the app to uninstall.</span></span> <span data-ttu-id="2928c-122">Listede bu programı görmüyorsanız, PowerShellGet aracılığıyla yüklemiş olmalısınız ve sonraki yönergeleri izlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2928c-122">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="2928c-123">2\. Seçenek: Az PowerShell modülünü PowerShellGet’ten kaldırma</span><span class="sxs-lookup"><span data-stu-id="2928c-123">Option 2: Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="2928c-124">Az modüllerini kaldırmak için [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet’ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2928c-124">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="2928c-125">Ancak `Uninstall-Module` yalnızca bir modülü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2928c-125">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="2928c-126">Az PowerShell modülünü tamamen kaldırmak için her modülü tek tek kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2928c-126">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="2928c-127">Birden çok Azure PowerShell sürümü yüklediyseniz kaldırma işlemi karmaşık hale gelebilir.</span><span class="sxs-lookup"><span data-stu-id="2928c-127">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="2928c-128">Sahip olduğunuz Az PowerShell modüllerinin sürümlerini öğrenmek için şu komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="2928c-128">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="2928c-129">Aşağıdaki betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2928c-129">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="2928c-130">Ardından her alt modülün doğru sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2928c-130">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="2928c-131">Bu betiği **İşlem** veya **Geçerli Kullanıcı** dışındaki bir kapsamda çalıştırmak için yönetici erişimine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2928c-131">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

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

<span data-ttu-id="2928c-132">Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="2928c-132">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="2928c-133">Aşağıdaki örnekte bu işlevi Az PowerShell modülünün ve alt modüllerinin eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2928c-133">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="2928c-134">Betik çalışırken kaldırılan alt modüllerin **Adını**, **Sürümünü** ve **Durumunu** görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2928c-134">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="2928c-135">Bu işlem sonucunda nelerin silineceğini bu öğeleri silmeden öğrenmek için `-WhatIf` parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="2928c-135">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="2928c-136">Bu betik, kaldırmak için bağımlılığın aynı sürümüyle tam olarak eşleşemezse, o bağımlılığın _hiçbir_ sürümünü kaldırmaz.</span><span class="sxs-lookup"><span data-stu-id="2928c-136">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="2928c-137">Bunun sebebi, sisteminizde hedef bağımlılıkları kullanan diğer hedef modülü sürümlerinin bulunması olabilir.</span><span class="sxs-lookup"><span data-stu-id="2928c-137">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="2928c-138">Aşağıdaki örneği, Az PowerShell modülünün kaldırmak istediğiniz her sürümü için çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2928c-138">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="2928c-139">Kolaylık sağlamak için, aşağıdaki betik Az'nin en son sürümü **dışındaki** tüm sürümlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2928c-139">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="2928c-140">AzureRM modülünü kaldırma</span><span class="sxs-lookup"><span data-stu-id="2928c-140">Uninstall the AzureRM module</span></span>

<span data-ttu-id="2928c-141">Sisteminizde Az modülü yüklüyse ve AzureRM’yi kaldırmak istiyorsanız iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="2928c-141">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="2928c-142">Hangi yöntemi kullanacağınız, AzureRM modülünü nasıl yüklediğinize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2928c-142">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="2928c-143">Özgün yükleme yönteminizden emin değilseniz önce MSI kaldırma adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="2928c-143">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="2928c-144">1\. Seçenek: AzureRM PowerShell modülünü MSI’dan kaldırma</span><span class="sxs-lookup"><span data-stu-id="2928c-144">Option 1: Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="2928c-145">AzureRM PowerShell modülünü MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2928c-145">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="2928c-146">Platform</span><span class="sxs-lookup"><span data-stu-id="2928c-146">Platform</span></span>         |                      <span data-ttu-id="2928c-147">Yönergeler</span><span class="sxs-lookup"><span data-stu-id="2928c-147">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="2928c-148">Windows 10</span><span class="sxs-lookup"><span data-stu-id="2928c-148">Windows 10</span></span>               | <span data-ttu-id="2928c-149">Başlat > Ayarlar > Uygulamalar</span><span class="sxs-lookup"><span data-stu-id="2928c-149">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="2928c-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2928c-150">Windows 7</span></span> </br><span data-ttu-id="2928c-151">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2928c-151">Windows 8</span></span> | <span data-ttu-id="2928c-152">Başlat > Denetim Masası > Programlar > Program kaldır</span><span class="sxs-lookup"><span data-stu-id="2928c-152">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="2928c-153">Bu ekrandaki program listesinde **Azure PowerShell**'i veya **Microsoft Azure PowerShell - Ay Yıl**'ı görebilmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2928c-153">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="2928c-154">Kaldırılacak olan uygulama budur.</span><span class="sxs-lookup"><span data-stu-id="2928c-154">This is the app to uninstall.</span></span> <span data-ttu-id="2928c-155">Listede bu programı görmüyorsanız, PowerShellGet aracılığıyla yüklemiş olmalısınız ve sonraki yönergeleri izlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2928c-155">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="2928c-156">2\. Seçenek: AzureRM PowerShell modülünü PowerShellGet’ten kaldırma</span><span class="sxs-lookup"><span data-stu-id="2928c-156">Option 2: Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="2928c-157">AzureRM'yi PowerShellGet ile yüklediyseniz modülleri `Az.Accounts` modülünün bir parçası olan [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet’iyle kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2928c-157">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span>

<span data-ttu-id="2928c-158">`Az.Accounts` modülünü kullanmak için Az modülünün yüklü olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2928c-158">In order to use the `Az.Accounts` module, you will need to have the Az module installed.</span></span>  <span data-ttu-id="2928c-159">Aynı anda AzureRM ve Az modüllerinin yüklü olması desteklenmez, ancak Az modülü AzureRM modülünün anında yüklenmesi için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2928c-159">Having both the AzureRM and the Az modules installed at the same time is not supported however the Az module can be used to immediately uninstall the AzureRM module.</span></span>  <span data-ttu-id="2928c-160">Az modülünü daha önce yüklemediyseniz aşağıdaki komutla bunu yükleyip AzureRM modülüne yönelik uyarıyı geçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="2928c-160">You can install the Az module and bypass the AzureRM module warning with the following command if you do not have the Az module installed already:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="2928c-161">Az modülü yüklendiğinde aşağıdaki komut _tüm_ AzureRM modüllerini makinenizden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2928c-161">Once the Az module is installed, the following command removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="2928c-162">Bunun için yönetici ayrıcalıkları gerekir.</span><span class="sxs-lookup"><span data-stu-id="2928c-162">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
