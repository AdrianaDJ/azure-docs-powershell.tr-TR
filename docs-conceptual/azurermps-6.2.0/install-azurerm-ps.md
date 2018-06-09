---
title: Azure PowerShell'i yükleme ve yapılandırma | Microsoft Docs
description: Azure PowerShell’i ilk kez kullanmak üzere yükleme ve yapılandırma.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 9f737201f13c07565b95a20227c75794b624e99c
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821981"
---
# <a name="install-and-configure-azure-powershell"></a>Azure PowerShell'i yükleyip yapılandırma

Bu makalede Azure PowerShell modüllerini Windows ortamına yüklemek için uygulanması gereken adımlar açıklanmaktadır.
Azure PowerShell'i macOS veya Linux'a yüklemek istiyorsanız şu makaleye bakın: [Azure PowerShell'i macOS ve Linux'ta yükleme ve yapılandırma](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Sistem gereksinimleri

Azure PowerShell sürüm 6.0.0, PowerShell 5.0 (veya daha yüksek) sürümünü gerektirir. Önceki Azure PowerShell sürümlerinin herhangi bir cmdlet’i çalıştırması için _en az_ sürüm 3.0 gerekiyordu. PowerShell 5.0’a yükseltme hakkında bilgi için lütfen [bu tabloya bakın](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

## <a name="step-1-install-powershellget"></a>1. Adım: PowerShellGet yükleme

Azure PowerShell'in PowerShell Galerisi'nden yüklenmesi, tercih edilen yükleme yöntemidir.

PowerShell Galerisi’nden yükleme yapabilmek için PowerShellGet modülü gerekir. Uygun PowerShellGet sürümüne ve diğer sistem gereksinimlerine sahip olduğunuzdan emin olun. PowerShellGet’in sisteminizde yüklü olup olmadığını görmek için aşağıdaki komutu çalıştırın.

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

PowerShellGet 1.1.2.0 veya üzeri bir sürüm gereklidir. PowerShellGet’i güncelleştirmek için şu komutu kullanın:

```powershell
Install-Module PowerShellGet -Force
```

PowerShellGet yüklü değilse bu makalenin [PowerShellGet edinme](#how-to-get-powershellget) bölümüne bakın.

> [!NOTE]
> PowerShellGet kullanımı, betikleri çalıştırmanıza olanak tanıyan bir Yürütme İlkesi gerektirir. PowerShell'in Yürütme İlkesi hakkında daha fazla bilgi için bkz. [Yürütme İlkeleri Hakkında](/powershell/module/microsoft.powershell.core/about/about_execution_policies).

## <a name="step-2-install-azure-powershell"></a>2. Adım: Azure PowerShell'i yükleme

Azure PowerShell’in PowerShell Galerisi’nden yüklenebilmesi için yükseltilmiş ayrıcalıklar gerekir. Yükseltilmiş bir PowerShell oturumunda aşağıdaki komutu çalıştırın:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

PowerShell Galerisi varsayılan olarak PowerShellGet için Güvenilir depo şeklinde yapılandırılmamıştır. PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

Yükleme işlemine devam etmek için "Evet" veya "Tümüne Evet" yanıtını verin.

> [!NOTE]
> NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.

AzureRM modülü, Azure Resource Manager cmdlet’leri için toplu bir modüldür. AzureRM modülünü yüklediğinizde, daha önce yüklenmemiş diğer Azure PowerShell modülleri PowerShell Galerisi'nden indirilir.

Azure PowerShell'in önceki sürümlerinden biri sisteminizde yüklüyse hata iletisiyle karşılaşabilirsiniz. Bu sorunu çözmek için bu makalenin [Azure PowerShell'in yeni bir sürümüne güncelleştirme](#update-azps) bölümünü inceleyin.

## <a name="step-3-load-the-azurerm-module"></a>3. Adım: AzureRM modülünü yükleme
Modül yüklendikten sonra modülü PowerShell oturumunuza yüklemeniz gerekir. Bunu normal (yükseltilmiş olmayan) bir PowerShell oturumunda yapmanız gerekir. Modüller `Import-Module` cmdlet’i kullanılarak aşağıdaki gibi yüklenir:

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell kullanma hakkında daha fazla bilgi için aşağıdaki makalelere bakın:

* [Azure PowerShell’i kullanmaya başlama](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>Sorunları bildirme ve geri bildirimde bulunma

Araçla ilgili bir hatayla karşılaşırsanız, GitHub deposunun [Sorunlar](https://github.com/Azure/azure-powershell/issues) bölümünden sorunu bildirin. Komut satırından geri bildirim sağlamak için `Send-Feedback` cmdlet'ini kullanın.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="how-to-get-powershellget"></a>PowerShellGet edinme

|Senaryo|Yükleme yönergeleri|
|---|---|
|Windows 10<br/>Windows Server 2016|İşletim sisteminde bulunan Windows Management Framework (WMF) 5.0’da yerleşiktir|
|PowerShell 5'e yükseltme yapmak istiyorum|<ol><li>[WMF’nin en son sürümünü yükleyin](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>Şu komutu çalıştırın:<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|Windows’un PowerShell 3 veya PowerShell 4 içeren bir sürümünü çalıştırıyorum|<ol><il>[PackageManagement modüllerini alın](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>Şu komutu çalıştırın:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>Azure PowerShell sürümünü denetleme

En son sürüme mümkün olan en kısa sürede yükseltme yapmanız önerilse de, Azure PowerShell’in birkaç sürümü desteklenmektedir. Azure PowerShell'in yüklü olan sürümünü belirlemek için komut satırından `Get-Module AzureRM` komutunu çalıştırın.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Klasik dağıtım yöntemleri için destek

Klasik dağıtım modelini kullanan dağıtımlarınız varsa, Azure PowerShell'in Hizmet Yönetimi sürümünü yükleyebilirsiniz. Daha fazla bilgi için bkz. [Azure PowerShell Hizmet Yönetimi modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps). Azure ve AzureRM modülleri ortak bağımlılıklara sahiptir. Hem Azure hem de AzureRM modüllerini kullanıyorsanız her paket için aynı sürümü yüklemeniz gerekir.

### <a id="update-azps"></a>Azure PowerShell'in yeni bir sürümüne güncelleştirme

Hizmet Yönetimi modülünü içeren eski bir Azure PowerShell sürümü yüklüyse şu hata iletisiyle karşılaşabilirsiniz:

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Hata iletisinde de belirtildiği üzere modülü yüklemek için -AllowClobber parametresini kullanmanız gerekir. Aşağıdaki komutu kullanın:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Daha fazla bilgi için [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module) yardım konusuna bakın.

### <a name="installing-module-versions-side-by-side"></a>Modül sürümlerini yan yana yükleme

PowerShellGet yükleme yöntemi, birden fazla sürümün yüklenmesini destekleyen tek yöntemdir. Örneğin, güncelleştirmek için zaman veya kaynaklara sahip olmadığınız önceki bir Azure PowerShell sürümünü kullanarak yazdığınız betikler olabilir. Aşağıdaki komutlar birden fazla Azure PowerShell sürümünün nasıl yükleneceğini göstermektedir:

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Bir PowerShell oturumunda modülün yalnızca bir sürümü yüklenebilir. AzureRM cmdlet’lerinin belirli bir sürümünü içeri aktarmak için yeni bir PowerShell penceresi açıp `Import-Module` seçeneğini kullanmanız gerekir:

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> Sürüm 2.1.0 ve sürüm 1.2.6, yan yana yüklenip kullanılmak üzere tasarlanmış ilk modül sürümleridir. Azure PowerShell'in önceki sürümlerinden biri yüklenirken **AzureRM.Profile** modülünün uyumlu olmayan sürümleri yüklenir. Bu işlemin sonucunda cmdlet'leri her çalıştırdığınızda oturum açmanız istenir.

### <a name="other-installation-methods"></a>Diğer yükleme yöntemleri

Web Platformu Yükleyicisi veya MSI Paketi kullanarak yükleme hakkında bilgi için bkz. [Diğer yükleme yöntemleri](other-install.md)