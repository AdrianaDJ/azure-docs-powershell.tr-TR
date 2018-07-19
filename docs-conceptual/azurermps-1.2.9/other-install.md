---
title: Azure PowerShell'i yüklemenin diğer yolları | Microsoft Docs
description: Azure PowerShell’i MSI paketini veya Web Platformu Yükleyicisi’ni kullanarak yükleme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: abf6aad6a04ffcf15b8fc38b47477caa1a04e015
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/13/2018
ms.locfileid: "39025234"
---
# <a name="other-installation-methods"></a>Diğer yükleme yöntemleri

Azure PowerShell’i yüklemek için birden çok yöntem vardır. Tercih edilen yöntem, PowerShell Galerisi ile PowerShellGet’i kullanmaktır. Azure PowerShell, Web Platformu Yükleyicisi (WebPI) ya da GitHub'dan indirilebilen MSI dosyası kullanılarak Windows'a yüklenebilir. Azure PowerShell bir Docker kapsayıcısına da yüklenebilir.

## <a name="install-on-windows-using-the-web-platform-installer"></a>Web Platformu Yükleyicisini kullanarak Windows'a yükleme

WebPI’dan en son Azure PowerShell’i yükleme işlemi, önceki sürümlerde olduğu gibidir.
[Azure PowerShell WebPI paketini](http://aka.ms/webpi-azps) indirin ve yükleme işlemini başlatın.

> [!NOTE]
> Daha önce PowerShell Galerisi'nden Azure modülleri yüklediyseniz, yükleyici bunları otomatik olarak kaldırır. Bu, Azure PowerShell’in yalnızca bir sürümünün yüklü olmasını sağlayarak ortamınızı basitleştirir. Bununla birlikte, aynı anda birden çok sürümün yüklü olmasını gerektiren senaryolar da vardır.
>
> PowerShell Galerisi modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yüklenir. Buna karşılık, WebPI yükleyicisi Azure modüllerini `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` konumuna yükler.
>
> Yükleme sırasında bir hata oluşursa, `$env:ProgramFiles\WindowsPowerShell\Modules` klasörünüzdeki Azure* klasörlerini el ile kaldırabilir ve yüklemeyi yeniden deneyebilirsiniz.

Yükleme tamamlandığında, `$env:PSModulePath` ayarınız Azure PowerShell cmdlet’lerini içeren dizinleri içermelidir. Azure PowerShell’in düzgün yüklendiğini doğrulamak için aşağıdaki komut kullanılabilir.

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> PowerShell’i WebPI’dan yüklerken karşılaşabileceğiniz bilinen bir sorun vardır. Bilgisayarınızın sistem güncelleştirmeleri veya başka yüklemeler nedeniyle yeniden başlatılması gerekiyorsa, `$env:PSModulePath` güncelleştirmeleri Azure PowerShell’in yüklü olduğu yolu içermeyebilir.

Yükleme işleminden sonra cmdlet’leri yüklemeye veya yürütmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Bu hata, makine yeniden başlatılarak ya da tam yol ile modül içeri aktarılarak düzeltilebilir. Örnek:

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>MSI Paketini kullanarak Windows'a yükleme

Azure PowerShell, [GitHub](https://github.com/Azure/azure-powershell/releases/latest)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir. Azure modüllerinin önceki sürümlerini yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır. MSI paketi, modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yükler ancak sürüme özel klasörler oluşturmaz.

## <a name="install-in-a-docker-container"></a>Bir Docker kapsayıcısına yükleme

Azure PowerShell ile önceden yapılandırılmış bir Docker görüntüsü sunuyoruz.

Kapsayıcıyı `docker run` komutuyla çalıştırın.

```powershell
docker run azuresdk/azure-powershell
```

Ayrıca, bir PowerShell Core kapsayıcısı olarak bir cmdlet alt kümesi sunarız.

Mac/Linux için `latest` görüntüsünü kullanın.

```bash
docker run azuresdk/azure-powershell-core:latest
```

Windows için `nanoserver` görüntüsünü kullanın.

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

Azure PowerShell, [PowerShell Galerisi](https://www.powershellgallery.com/)’nden `Install-Module` aracılığıyla görüntüye yüklenir.