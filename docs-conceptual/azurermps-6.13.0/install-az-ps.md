---
title: Azure PowerShell 'Az' modülünü PowerShellGet ile yükleme
description: Windows, macOS ve Linux'ta Azure PowerShell PowerShellGet ile nasıl yüklenir?
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588188"
---
# <a name="install-the-azure-powershell-az-module"></a>Azure PowerShell 'Az' modülünü yükleme

Bu makalede, PowerShellGet kullanarak Azure PowerShell modüllerini nasıl yükleyeceğiniz anlatılır. Bu yönergeler Windows, macOS ve Linux platformlarında kullanılabilir. Az modülünün önizleme sürümünde başka yükleme yöntemleri desteklenmez. 

## <a name="requirements"></a>Gereksinimler

Azure PowerShell Windows üzerinde PowerShell 5.x ile veya herhangi bir platform üzerinde PowerShell 6.x ile çalışır. Makinenizde çalışan PowerShell sürümü kontrol etmek için şu komutu çalıştırın:

```powershell-interactive
$PSVersionTable.PSVersion
```

Eski bir sürümünüz varsa veya PowerShell'i yüklemeniz gerekiyorsa, bkz. [PowerShell'in çeşitli sürümlerini yükleme](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6). Platformunuza yönelik yükleme bilgilerine bu sayfadan bağlantı verilir.

## <a name="install-the-azure-powershell-module"></a>Azure PowerShell modülünü yükleme

> [!IMPORTANT]
>
> `AzureRM` ve `Az` modüllerini aynı anda yükleyebilirsiniz. İki modül de yüklüyse __diğer adları etkinleştirmeyin__.
> Diğer adların etkinleştirilmesi, `AzureRM` cmdlet’leri ile `Az` komut diğer adları arasında çakışmalara neden olur ve bu da beklenmeyen davranışlara yol açabilir.
> `Az` modülünü yüklemeden önce `AzureRM` modülünü kaldırmanız önerilir. Dilediğiniz zaman `AzureRM` modülünü kaldırabilir veya diğer adları etkinleştirebilirsiniz. Kaldırma yönergeleri için bkz. [Azure PowerShell modülünü (AzureRM) kaldırma](uninstall-azurerm-ps.md). 

Modülleri genel kapsamda yüklemek için, PowerShell Galerisi'ndeki modülleri yüklemek üzere yükseltilmiş ayrıcalıklara ihtiyacınız vardır. Azure PowerShell'i yüklemek için, aşağıdaki komutu yükseltilmiş oturumda çalıştırın (Windows'da "Yönetici Olarak Çalıştır" ile ya da macOS veya Linux'ta süper kullanıcı ayrıcalıklarıyla):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Yönetici ayrıcalıklarına erişiminiz yoksa, `-Scope` bağımsız değişkenini ekleyerek geçerli kullanıcı için yükleyebilirsiniz.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır. PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.

`Az` modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür. Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.

## <a name="sign-in"></a>Oturum aç

Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module Az` kullanarak modülü el ile içeri aktarmanız gerekir. Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.

Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir. Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Azure PowerShell modülünü güncelleştirme

Azure PowerShell yüklemenizi güncelleştirmek için [Update-Module](/powershell/module/powershellget/update-module) cmdlet'ini çalıştırabilirsiniz. Bu komut önceki sürümleri __kaldırmaz__.

```powershell-interactive
Update-Module -Name Az
```

Sisteminizdeki eski Azure PowerShell sürümlerini kaldırmak isterseniz bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Azure PowerShell'in birden çok sürümünü kullanma

Azure PowerShell'in birden çok sürümünü yüklemek mümkündür. Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-azurerm-ps.md).

`Install-Module` ve `Import-Module` ile `-RequiredVersion` bağımsız değişkenini kullanarak `Az` modülünün belirli bir sürümünü yükleyebilirsiniz:

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

Modülün birden çok sürümünü yüklediyseniz, varsayılan olarak en son sürüm yüklenir.

## <a name="provide-feedback"></a>Geri bildirimde bulunma

Azure Powershell kullanırken bir hatayla karşılaşırsanız [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).
Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet'ini kullanın.

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell'i kullanmaya başlamak için, [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) bölümünü inceleyerek modül ve özellikleri hakkında daha fazla bilgi edinin.
