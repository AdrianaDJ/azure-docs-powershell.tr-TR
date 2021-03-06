---
title: PowerShellGet ile Windows'da Azure PowerShell yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c03c6ee3782b68de8a237b3c215405ff6513dbca
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523249"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>PowerShellGet ile Windows'da Azure PowerShell yükleme

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Bu makalede PowerShellGet kullanarak Windows için PowerShell 5.x sürümlerine yönelik Azure PowerShell modüllerini yüklemek için uygulanması gereken adımlar açıklanır. PowerShellGet ve modül yönetimi, Azure PowerShell'i yüklemek için tercih edilen yoldur. Ancak bunun yerine Web Platformu Yükleyicisi veya MSI paketi kullanarak yükleyecekseniz bkz. [Diğer yükleme yöntemleri](other-install.md).

Azure klasik dağıtım modeli, Azure PowerShell'in bu sürümü tarafından desteklenmez. Klasik dağıtımlar için [Azure PowerShell Service Management modülünü yükleme](/powershell/azure/servicemanagement/install-azure-ps) talimatlarını izleyin.

> [!IMPORTANT]
> AzureRM modülü macOS veya Linux için desteklenmiyor. Azure PowerShell cmdlet'lerini bu platformlarda kullanmak için [Az modülünü yükleyin](/powershell/azure/install-az-ps).

## <a name="requirements"></a>Gereksinimler

Azure PowerShell'i yüklemek için PowerShellGet sürüm 1.1.2.0 veya üzeri gerekir. Sisteminizde mevcut olup olmadığını görmek için şu komutu çalıştırın:

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

Aşağıdaki çıktıya benzer bir sonuç görmeniz gerekir:

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

PowerShellGet yüklemenizi güncelleştirmeniz gerekiyorsa şu komutu çalıştırın:

```powershell-interactive
Install-Module PowerShellGet -Force
```

PowerShellGet yüklü değilse aşağıdaki tablodan sisteminize özgü yönergeleri izleyin.

|Senaryo|Yükleme yönergeleri|
|---|---|
|Windows 10<br/>Windows Server 2016|İşletim sisteminde bulunan Windows Management Framework (WMF) 5.0’da yerleşiktir|
|PowerShell 5'e yükseltme| <ol><li>[WMF’nin en son sürümünü yükleyin](https://www.microsoft.com/download/details.aspx?id=54616)</li><li>Şu komutu çalıştırın:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> PowerShellGet kullanımı, betikleri çalıştırmanıza olanak tanıyan bir Yürütme İlkesi gerektirir. PowerShell'in Yürütme İlkesi hakkında daha fazla bilgi için bkz. [Yürütme İlkeleri Hakkında](/powershell/module/microsoft.powershell.core/about/about_execution_policies).
>
> [!IMPORTANT]
> Bu belgede açıklanan AzureRM modülü .NET Framework kullanır. Bu da, .NET Core kullanan PowerShell 6.0 ile uyumsuz olmasına neden olur. PowerShell 6.0 kullanıyorsanız, [macOS ve Linux için yükleme yönergelerini](/powershell/azure/install-az-ps) izleyin.

## <a name="install-the-azure-powershell-module"></a>Azure PowerShell modülünü yükleme

PowerShell Galerisi'ndeki modülleri yüklemek için yükseltilmiş ayrıcalıklara ihtiyacınız vardır. Azure PowerShell'i yüklemek için yükseltilmiş oturumda şu komutu çalıştırın:

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> NuGet sürümünüz 2.8.5.201'den eskiyse, en son NuGet sürümünü indirip yüklemeniz istenir.

PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır. PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.

`AzureRM` modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür. Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.

## <a name="sign-in"></a>Oturum aç

Azure PowerShell ile çalışmaya başlamak için `AzureRM` modülünü geçerli PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yüklemeniz ve Azure kimlik bilgilerinizle oturum açmanız gerekir.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir. `AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).
Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Azure PowerShell modülünü güncelleştirme

Azure PowerShell yüklemenizi güncelleştirmek için [Update-Module](/powershell/module/powershellget/update-module) cmdlet'ini çalıştırabilirsiniz. Bu komut önceki sürümleri __kaldırmaz__ .

```powershell-interactive
Update-Module -Name AzureRM
```

Sisteminizdeki eski Azure PowerShell sürümlerini kaldırmak isterseniz bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Azure PowerShell'in birden çok sürümünü kullanma

Azure PowerShell'in birden çok sürümünü yükleyebilirsiniz. Şirket içi Azure Stack kaynaklarıyla çalışıyorsanız, PowerShell 5.0 güncelleştirmesini alamayan eski bir Windows sürümünü çalıştırıyorsanız veya Azure klasik dağıtım modelini kullanıyorsanız birden fazla sürüme ihtiyaç duyabilirsiniz. Eski bir sürümü yüklemek için yükleme sırasında `-RequiredVersion` bağımsız değişkenini belirtin.

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Azure PowerShell modülünü yüklerken varsayılan olarak son sürüm yüklenir. Farklı bir sürümü yüklemek için `-RequiredVersion` bağımsız değişkenini belirtin.

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Geri bildirimde bulunma

Azure Powershell kullanırken bir hatayla karşılaşırsanız lütfen [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).
Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet'ini kullanın.

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell'i kullanmaya başlamak için, [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) bölümünü inceleyerek modül ve özellikleri hakkında daha fazla bilgi edinin.
