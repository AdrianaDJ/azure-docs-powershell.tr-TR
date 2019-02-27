---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 11/30/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: a0afae1ba51fdb34425c91049e08d7388f434d7d
ms.sourcegitcommit: 0b5b0434fba7a752b0199256e04fa34f06aaf33a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56464987"
---
# <a name="uninstall-the-azure-powershell-module"></a>Azure PowerShell modülünü kaldırma

Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz. Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.
Bir hatayla karşılaştığınızda [bir GitHub sorunu girerek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.


## <a name="uninstall-azure-powershell-msi"></a>Azure PowerShell MSI'yi kaldırma

Azure PowerShell'i MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.

| Platform | Yönergeler |
|----------|--------------|
| Windows 10 | Başlat > Ayarlar > Uygulamalar |
| Windows 7 </br>Windows 8 | Başlat > Denetim Masası > Programlar > Program kaldır |

Bu ekrandaki program listesinde __Azure PowerShell__'i görebilmelisiniz. Kaldırılacak olan uygulama budur.

## <a name="uninstall-from-powershell"></a>PowerShell'den kaldırma

Azure PowerShell'i PowerShellGet kullanarak yüklediyseniz [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet'ini kullanabilirsiniz. Ancak `Uninstall-Module` yalnızca bir modülü kaldırır. Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir. Birden çok Azure PowerShell sürümü yüklediyseniz kaldırma işlemi karmaşık hale gelebilir.

Şu anda sahip olduğunuz Azure PowerShell sürümlerini öğrenmek için şu komutu çalıştırın:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
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
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

Betik çalışırken kaldırılan alt modüllerin adını ve sürümünü görüntüler. Bu işlem sonucunda nelerin silineceğini bu öğeleri silmeden öğrenmek için `-WhatIf` seçeneğini kullanın.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Bu komutu kaldırmak istediğiniz her Azure PowerShell sürümü için çalıştırın. Kolaylık sağlamak için, aşağıdaki betik AzureRM'nin en son sürümü __dışındaki__ tüm sürümlerini kaldıracak.

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
