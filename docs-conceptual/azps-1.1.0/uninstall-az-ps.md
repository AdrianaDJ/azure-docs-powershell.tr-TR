---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 9d1f1b6550c39b8c65662cf0150f477392747708
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342192"
---
# <a name="uninstall-the-azure-powershell-module"></a>Azure PowerShell modülünü kaldırma

Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz. Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.
Bir hatayla karşılaştığınızda [bir GitHub sorunu girerek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.

## <a name="uninstall-the-az-module"></a>Az modülünü kaldırma

Az modüllerini kaldırmak için [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet’ini kullanın. Ancak `Uninstall-Module` yalnızca bir modülü kaldırır. Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir. Birden çok Azure PowerShell sürümü yüklediyseniz kaldırma işlemi karmaşık hale gelebilir.

Şu anda sahip olduğunuz Azure PowerShell sürümlerini öğrenmek için şu komutu çalıştırın:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

Aşağıdaki betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır. Ardından her alt modülün doğru sürümünü kaldırır. Bu betiği `Process` veya `CurrentUser` haricinde başka bir kapsamda çalıştırmak için yönetici erişimine sahip olmanız gerekir.

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

Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın. Aşağıdaki örnekte bu işlevi Azure PowerShell'in eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

Betik çalışırken kaldırılan alt modüllerin adını ve sürümünü görüntüler. Bu işlem sonucunda nelerin silineceğini bu öğeleri silmeden öğrenmek için `-WhatIf` seçeneğini kullanın.

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

Bu komutu kaldırmak istediğiniz her Azure PowerShell sürümü için çalıştırın. Kolaylık sağlamak için, aşağıdaki betik Az'nin en son sürümü __dışındaki__ tüm sürümlerini kaldıracak.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>AzureRM modülünü kaldırma

Sisteminizde Az modülü yüklüyse ve AzureRM’yi kaldırmak istiyorsanız, yukarıdaki `Uninstall-AllModules` betiğini çalıştırmanızı gerektirmeyen iki basit seçenek vardır. Hangi metodu kullanacağınız, AzureRM’yi nasıl yüklediğinize bağlıdır.
Emin değilseniz önce MSI kaldırma adımlarını inceleyin.

### <a name="uninstall-msi"></a>MSI yüklemesini kaldırma

Azure PowerShell AzureRM modüllerini MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.

| Platform | Yönergeler |
|----------|--------------|
| Windows 10 | Başlat > Ayarlar > Uygulamalar |
| Windows 7 </br>Windows 8 | Başlat > Denetim Masası > Programlar > Program kaldır |

Bu ekrandaki program listesinde "Azure PowerShell"i bulabilir ve kaldırabilirsiniz.

### <a name="uninstall-from-powershell"></a>PowerShell'den kaldırma

AzureRM’yi PowerShellGet’ten yüklediyseniz modülleri yeni `Uninstall-AzureRM` komutuyla kaldırabilirsiniz. Bu işlem _tüm_ AzureRM modüllerini makinenizden kaldırır, ancak yönetici ayrıcalıkları gerektirir.

```powershell-interactive
Uninstall-AzureRm
```

`Uninstall-AzureRM` komutunu başarılı bir şekilde çalıştıramazsanız onun yerine bu makalede sağlanan `Uninstall-AllModules` betiğini kullanın.