---
title: Azure PowerShell'i kaldırma
description: Azure PowerShell'i tamamen kaldırmayı öğrenin
ms.date: 09/11/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: bf1f81b4929ec066eeb888da4ba1303430f026b4
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259901"
---
# <a name="uninstall-the-azure-powershell-module"></a>Azure PowerShell modülünü kaldırma

Bu makalede Azure PowerShell'in eski bir sürümünü veya tamamını sisteminizden kaldırmayı öğreneceksiniz. Azure PowerShell'i tamamen kaldırmaya karar verdiyseniz [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanarak geri bildirimlerinizi bizimle paylaşın.
Bir hatayla karşılaştığınızda [bir GitHub sorunu girerek](https://github.com/azure/azure-powershell/issues) bize bildirirseniz seviniriz.

## <a name="uninstall-from-powershell"></a>PowerShell'den kaldırma

Azure PowerShell'i PowerShellGet kullanarak yüklediyseniz [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet'ini kullanabilirsiniz. Ancak `Uninstall-Module` yalnızca bir modülü kaldırır. Azure PowerShell'i tamamen kaldırmak için her modülü ayrıca kaldırmanız gerekir. Birden çok Azure PowerShell sürümü yüklediyseniz kaldırma işlemi karmaşık hale gelebilir.

Aşağıdaki betik PowerShell Galerisi'ne sorgu göndererek bağımlı alt modüllerin listesini alır. Ardından her alt modülün doğru sürümünü kaldırır.

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
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.minimumVersion}
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

Bu işlevi kullanmak için kodu kopyalayıp PowerShell oturumunuza yapıştırın. Aşağıdaki örnekte bu işlevi Azure PowerShell'in eski bir sürümünü kaldırma amacıyla nasıl çalıştıracağınızı görebilirsiniz.

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

Betik çalışırken kaldırılan alt modüllerin adını ve sürümünü görüntüler.

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

## <a name="uninstall-msi"></a>MSI yüklemesini kaldırma

Azure PowerShell'i MSI paketini kullanarak yüklediyseniz kaldırma işlemini PowerShell yerine Windows sisteminden gerçekleştirmeniz gerekir.

| Platform | Yönergeler |
|----------|--------------|
| Windows 10 | Başlat > Ayarlar > Uygulamalar |
| Windows 7 </br>Windows 8 | Başlat > Denetim Masası > Programlar > Program kaldır |

Bu ekrandaki program listesinde "Azure PowerShell"i bulabilir ve kaldırabilirsiniz.
