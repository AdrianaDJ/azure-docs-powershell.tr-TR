---
title: Azure PowerShell'i yüklemenin diğer yolları
description: Azure PowerShell’i MSI paketini veya Web Platformu Yükleyicisi’ni kullanarak yükleme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323280"
---
# <a name="other-installation-methods"></a>Diğer yükleme yöntemleri

Bu makalede MIS veya Web Platformu Yükleyicisi (WebPI) kullanarak Azure PowerShell'i yükleme işlemi açıklanır. Azure PowerShell'i Docker kapsayıcısının içinden de çalıştırabilirsiniz. Bu yükleme yöntemlerini ancak sisteminiz için gerekli olduğunda kullanın. Azure PowerShell'i yüklemenin kurallı yolu bu işlemi PowerShellGet aracılığıyla yapmaktır. PowerShellGet kullanarak Azure PowerShell'i yükleme yönergeleri için bkz. [Azure PowerShell'i PowerShellGet ile yükleme](install-azurerm-ps.md).

Linux veya macOS ortamlarına yüklemek için bkz. [Azure PowerShell'i macOS veya Linux'a yükleme](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Web Platformu Yükleyicisi'ni kullanarak Windows'a yükleme veya güncelleştirme

WebPI’dan en son Azure PowerShell’i yükleme işlemi, önceki sürümlerde olduğu gibidir.
[Azure PowerShell WebPI paketini](http://aka.ms/webpi-azps) indirin ve yükleme işlemini başlatın.

> [!NOTE]
> Daha önce PowerShell Galerisi'nden Azure modülleri yüklediyseniz, yükleyici bunları otomatik olarak kaldırır. Bu, Azure PowerShell’in yalnızca bir sürümünün yüklü olmasını sağlayarak ortamınızı basitleştirir. Bununla birlikte, aynı anda birden çok sürümün yüklü olmasını gerektiren senaryolar da vardır.
>
> PowerShell Galerisi modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yüklenir. Buna karşılık, WebPI yükleyicisi Azure modüllerini `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\` konumuna yükler.
>
> Yükleme sırasında bir hata oluşursa, `$env:ProgramFiles\WindowsPowerShell\Modules` klasörünüzdeki `Azure*` klasörlerini el ile kaldırabilir ve yüklemeyi yeniden deneyebilirsiniz.

Yükleme tamamlandığında, `$env:PSModulePath` ayarınız Azure PowerShell cmdlet’lerini içeren dizinleri içermelidir. Azure PowerShell’in düzgün yüklendiğini doğrulamak için aşağıdaki komut kullanılabilir:

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> PowerShell’i WebPI’dan yüklerken karşılaşabileceğiniz bilinen bir sorun vardır. Bilgisayarınızın sistem güncelleştirmeleri veya başka yüklemeler nedeniyle yeniden başlatılması gerekiyorsa, `$env:PSModulePath` güncelleştirmeleri Azure PowerShell’in yüklü olduğu yolu içermeyebilir.

Yükleme işleminden sonra cmdlet’leri yüklemeye veya yürütmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Bu hata, makine yeniden başlatılarak ya da tam yol ile modül içeri aktarılarak düzeltilebilir.

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a>MSI Paketini kullanarak Windows'a yükleme veya güncelleştirme

Azure PowerShell, [GitHub](https://aka.ms/azps-release)’dan indirilebilen MSI dosyası kullanılarak yüklenebilir. Azure modüllerinin önceki sürümlerini yüklediyseniz, bunlar yükleyici tarafından otomatik olarak kaldırılır. MSI paketi, modülleri `$env:ProgramFiles\WindowsPowerShell\Modules` konumuna yükler ancak sürüme özel klasörler oluşturmaz.

## <a name="run-in-a-docker-container"></a>Docker kapsayıcısında çalıştırma

Azure PowerShell ile önceden yapılandırılmış bir dizi Docker görüntüsü sunuyoruz. İki tür kapsayıcı sağlanıyor: Windows üzerinde geleneksel PowerShell'i çalıştıran kapsayıcılar ve Windows veya Linux üzerinde PowerShell Core çalıştıran bir kapsayıcı.

| Ortam | Docker görüntüsü |
|-------------|--------------|
| Windows'da PowerShell | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| Windows'da PowerShell Core | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| Linux'ta PowerShell Core | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Bu kapsayıcılardan herhangi birini çalıştırmak için, `docker run -it $ImageName` kullanıp etkileşimli bir terminal elde edersiniz. Örneğin, Linux kapsayıcısında PowerShell Core'u çalıştırmak için şunu kullanın:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Docker'da Windows kapsayıcısını çalıştırmak için, ana işletim sisteminiz Windows olmalı ve Docker, Windows kapsayıcılarını çalıştıracak şekilde ayarlanmalıdır. Docker'da Windows ile Linux ortamları arasında geçiş yapmayı öğrenmek için, Docker'ın [Windows ile Linux kapsayıcıları arasında geçiş yapma](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) belgelerine bakın.