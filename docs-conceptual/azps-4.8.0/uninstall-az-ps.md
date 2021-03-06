---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ec4ecc9902f700e12ce6b22c32b4e07b13b4d4dc
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407791"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a>Azure PowerShell modüllerini yükleme

Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz. Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın. Bir hatayla karşılaştıysanız, bunun düzeltilebilmesi için [bir GitHub sorunu kaydederek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.

## <a name="uninstall-the-az-module"></a>Az modülünü kaldırma

Sisteminizde Az modülü yüklüyse ve bunu kaldırmak istiyorsanız iki seçenek vardır. Hangi yöntemi kullanacağınız, Az modülünü nasıl yüklediğinize bağlıdır. Özgün yükleme yönteminizden emin değilseniz önce MSI kaldırma adımlarını izleyin.

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a>1\. Seçenek: Az PowerShell modülünü MSI’dan kaldırma

Az PowerShell modülünü MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.

|         Platform         |                      Yönergeler                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Başlat > Ayarlar > Uygulamalar                                |
| Windows 7 </br>Windows 8 | Başlat > Denetim Masası > Programlar > Program kaldır |

Bu ekrandaki program listesinde **Azure PowerShell** 'i görebilmelisiniz. Kaldırılacak olan uygulama budur. Listede bu programı görmüyorsanız, PowerShellGet aracılığıyla yüklemiş olmalısınız ve sonraki yönergeleri izlemelisiniz.

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a>2\. Seçenek: Az PowerShell modülünü PowerShellGet’ten kaldırma

Az modüllerini kaldırmak için [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet’ini kullanabilirsiniz. Ancak `Uninstall-Module` yalnızca bir modülü kaldırır. Az PowerShell modülünü tamamen kaldırmak için her modülü tek tek kaldırmanız gerekir. Birden çok Azure PowerShell sürümü yüklediyseniz kaldırma işlemi karmaşık hale gelebilir.

Sahip olduğunuz Az PowerShell modüllerinin sürümlerini öğrenmek için şu komutu çalıştırın:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

Aşağıdaki betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır. Ardından her alt modülün doğru sürümünü kaldırır. Bu betiği **İşlem** veya **Geçerli Kullanıcı** dışındaki bir kapsamda çalıştırmak için yönetici erişimine sahip olmanız gerekir.

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

Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın. Aşağıdaki örnekte bu işlevi Az PowerShell modülünün ve alt modüllerinin eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

Betik çalışırken kaldırılan alt modüllerin **Adını** , **Sürümünü** ve **Durumunu** görüntüler. Bu işlem sonucunda nelerin silineceğini bu öğeleri silmeden öğrenmek için `-WhatIf` parametresini belirtin.

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
> Bu betik, kaldırmak için bağımlılığın aynı sürümüyle tam olarak eşleşemezse, o bağımlılığın _hiçbir_ sürümünü kaldırmaz. Bunun sebebi, sisteminizde hedef bağımlılıkları kullanan diğer hedef modülü sürümlerinin bulunması olabilir.

Aşağıdaki örneği, Az PowerShell modülünün kaldırmak istediğiniz her sürümü için çalıştırın.
Kolaylık sağlamak için, aşağıdaki betik Az'nin en son sürümü **dışındaki** tüm sürümlerini kaldırır.

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a>AzureRM modülünü kaldırma

Sisteminizde Az modülü yüklüyse ve AzureRM’yi kaldırmak istiyorsanız iki seçenek vardır. Hangi yöntemi kullanacağınız, AzureRM modülünü nasıl yüklediğinize bağlıdır. Özgün yükleme yönteminizden emin değilseniz önce MSI kaldırma adımlarını izleyin.

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a>1\. Seçenek: AzureRM PowerShell modülünü MSI’dan kaldırma

AzureRM PowerShell modülünü MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.

|         Platform         |                      Yönergeler                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Başlat > Ayarlar > Uygulamalar                                |
| Windows 7 </br>Windows 8 | Başlat > Denetim Masası > Programlar > Program kaldır |

Bu ekrandaki program listesinde **Azure PowerShell** 'i veya **Microsoft Azure PowerShell - Ay Yıl** 'ı görebilmelisiniz. Kaldırılacak olan uygulama budur. Listede bu programı görmüyorsanız, PowerShellGet aracılığıyla yüklemiş olmalısınız ve sonraki yönergeleri izlemelisiniz.

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a>2\. Seçenek: AzureRM PowerShell modülünü PowerShellGet’ten kaldırma

AzureRM'yi PowerShellGet ile yüklediyseniz modülleri `Az.Accounts` modülünün bir parçası olan [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet’iyle kaldırabilirsiniz.

`Az.Accounts` modülünü kullanmak için Az modülünün yüklü olması gerekir.  Aynı anda AzureRM ve Az modüllerinin yüklü olması desteklenmez, ancak Az modülü AzureRM modülünün anında yüklenmesi için kullanılabilir.  Az modülünü daha önce yüklemediyseniz aşağıdaki komutla bunu yükleyip AzureRM modülüne yönelik uyarıyı geçebilirsiniz:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Az modülü yüklendiğinde aşağıdaki komut _tüm_ AzureRM modüllerini makinenizden kaldırır. Bunun için yönetici ayrıcalıkları gerekir.

```powershell-interactive
Uninstall-AzureRm
```
