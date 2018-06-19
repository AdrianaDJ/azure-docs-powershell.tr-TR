---
title: Azure PowerShell'i PowerShellGet ile yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323110"
---
# <a name="install-azure-powershell-with-powershellget"></a>Azure PowerShell'i PowerShellGet ile yükleme

Bu makalede PowerShellGet kullanarak Azure PowerShell modüllerini Windows ortamına yüklemek için uygulanması gereken adımlar açıklanır.  Bu Azure PowerShell'i yüklemek için tercih edilen yoldur ama bunun yerine Web Platformu Yükleyicisi veya MSI paketi kullanarak yükleyecekseniz, bkz. [Diğer yükleme yöntemleri](other-install.md).

Azure PowerShell'i macOS veya Linux'a yüklemek istiyorsanız şu makaleye bakın: [Azure PowerShell'i macOS ve Linux'ta yükleme ve yapılandırma](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Sistem gereksinimleri

Azure PowerShell sürüm 6.1.0, PowerShell 5.0 (veya sonraki) sürümünü gerektirir. PowerShell 5.0'ı yükseltme hakkında bilgi için bkz. [Varolan Windows PowerShell'i yükseltme](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

PowerShellGet, PowerShell 5.0'ın parçası olarak otomatik olarak eklenir.

## <a name="install-or-update-the-azure-powershell-module"></a>Azure PowerShell modülünü yükleme veya güncelleştirme

Azure PowerShell’in PowerShell Galerisi’nden yüklenebilmesi için yükseltilmiş ayrıcalıklar gerekir. Yükseltilmiş bir PowerShell oturumunda aşağıdaki komutu çalıştırın:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> Bu komut sisteminizde varolan Azure PowerShell yüklemesini güncelleştirir. Birden çok sürümün yüklü olması gerekiyorsa, SSS bölümünde [Azure PowerShell'in birden çok sürümünü yükleyebilir miyim?](#multiple-versions) sorusunun yanıtına bakın.

PowerShell Galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır. PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Yükleme işlemine devam etmek için "Evet" veya "Tümüne Evet" yanıtını verin.

> [!NOTE]
> NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.

AzureRM modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür. AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş olan tüm Azure PowerShell modülleri PowerShell Galerisi'nden indirilir.

## <a name="load-the-azure-powershell-module"></a>Azure PowerShell modülünü yükleme

Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir. Bunu normal (yükseltilmiş olmayan) bir PowerShell oturumunda yapmanız gerekir. Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>Sorunları bildirme ve geri bildirimde bulunma

Araçta hatalarla karşılaşırsanız, lütfen [GitHub'a bir sorun girin](https://github.com/Azure/azure-powershell/issues). Komut satırından geri bildirim sağlamak için `Send-Feedback` cmdlet'ini kullanın.

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell kullanma hakkında daha fazla bilgi için aşağıdaki makalelere bakın:

* [Azure PowerShell’i kullanmaya başlama](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a id="helpmechoose"></a>Azure PowerShell'in sürümünü nasıl denetleyebilirim?

En son sürüme mümkün olan en kısa sürede yükseltme yapmanız önerilse de, Azure PowerShell’in birkaç sürümü desteklenmektedir. Azure PowerShell'in yüklü olan sürümünü belirlemek için komut satırından `Get-Module AzureRM` komutunu çalıştırın.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>Azure PowerShell'i Klasik Azure dağıtımlarında kullanabilir miyim?

Klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz. Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps). Azure ve AzureRM modülleri ortak bağımlılıklara sahiptir. Hem Azure hem de AzureRM modüllerini kullanıyorsanız her paket için aynı sürümü yüklemeniz gerekir.

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>Azure PowerShell'in birden çok sürümünü yükleyebilir miyim?

Birden çok sürümü destekleyen tek yükleme yöntemi PowerShellGet'tir. Birden çok sürümü yüklemek için, `Install-Module` cmdlet'ine `-RequiredVersion` parametresini ekleyebilirsiniz. Örneğin, hem 6.1.0 hem de 1.2.9 sürümlerini yüklemek için:

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Bir PowerShell oturumunda modülün yalnızca bir sürümü yüklenebilir. Azure PowerShell modülünün belirli bir sürümünü içeri aktarmak için yeni bir PowerShell penceresi açıp `Import-Module` parametresini kullanmanız gerekir.

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> Sürüm 2.1.0 ve sürüm 1.2.6, yan yana yüklenip kullanılmak üzere tasarlanmış ilk modül sürümleridir. Azure PowerShell'in önceki sürümlerinden biri yüklenirken **AzureRM.Profile** modülünün uyumlu olmayan sürümleri yüklenir. Bu işlemin sonucunda cmdlet'leri her çalıştırdığınızda oturum açmanız istenir.
