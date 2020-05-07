---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cc0b6a4369116e92b8200ffbc0838d6ee2991263
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "67037683"
---
# <a name="uninstall-the-azure-powershell-module"></a>Azure PowerShell modülünü kaldırma

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz. Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz lütfen [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.
Bir hatayla karşılaştıysanız [bir GitHub sorunu girerek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.

## <a name="uninstall-msi-or-web-platform-installer"></a>MSI veya Web Platformu Yükleyicisi ile kaldırma

Azure PowerShell'i MSI paketini veya Web Platformu Yükleyicisi'ni kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.

| Platform | Yönergeler |
|----------|--------------|
| Windows 10 | Başlat > Ayarlar > Uygulamalar |
| Windows 7 </br>Windows 8 | Başlat > Denetim Masası > Programlar > Program kaldır |

Bu ekrandaki program listesinde "Azure PowerShell"i bulabilir ve kaldırabilirsiniz.

## <a name="uninstall-from-powershell"></a>PowerShell'den kaldırma

Azure PowerShell'i PowerShellGet kullanarak yüklediyseniz [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet'ini kullanabilirsiniz. Ancak `Uninstall-Module` yalnızca bir modülü kaldırır. Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir. Birden fazla Azure PowerShell sürümü yüklüyse kaldırma işlemi karmaşık hale gelebilir.

Azure PowerShell'in tek bir sürümünü tamamen kaldırmak için aşağıdaki betiği kullanabilirsiniz. Betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır. Ardından her alt modülün doğru sürümünü kaldırır.

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

> [!NOTE]
> Bu betik, kaldırmak için bağımlılığın aynı sürümüyle tam olarak eşleşemezse, o bağımlılığın _hiçbir_ sürümünü kaldırmaz. Bunun sebebi, sisteminizde hedef bağımlılıkları kullanan diğer hedef modülü sürümlerinin bulunması olabilir. Bu durumda, bağımlılığın kullanılabilir sürümleri listelenir.
> `Uninstall-Module` ile herhangi bir eski sürümü kaldırabilirsiniz.


Bu komutu kaldırmak istediğiniz her Azure PowerShell sürümü için çalıştırın. Kolaylık sağlamak için, aşağıdaki betik AzureRM'nin en son sürümü __dışındaki__ tüm sürümlerini kaldıracak.

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
