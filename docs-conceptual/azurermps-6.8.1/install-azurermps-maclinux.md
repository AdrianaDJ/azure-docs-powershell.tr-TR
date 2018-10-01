---
title: Azure PowerShell'i macOS veya Linux'a yükleme
description: Azure PowerShell'i macOS veya Linux'a yükleme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560125"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Azure PowerShell'i macOS veya Linux'a yükleme

Windows dışındaki platformlarda Azure PowerShell'i PowerShell Core v6 ile çalıştırmak mümkündür. PowerShell'in bu sürümü .NET Core destekli tüm platformlarda kullanılacak şekilde tasarlanmıştır. Bu platformlarda çalışmak için Azure PowerShell'in bir .NET Standard sürümü mevcuttur.

> [!NOTE]
> PowerShell Core v6 ve .NET Core için Azure PowerShell hala beta sürümündedir.
> Bu ürünler için sınırlı destek sunulur. Herhangi bir sorunla karşılaşır veya hata bulursanız, lütfen GitHub üzerinden bir sorun girin.
>
> * [PowerShell Core v6 ile ilgili sorunlar](https://github.com/PowerShell/PowerShell/issues)
> * [Azure PowerShell ile ilgili sorunlar](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>PowerShell Core'u yükleme

PowerShell Core yükleme yönergeleri macOS ve birçok Linux dağıtımı için farklıdır.
Şu makalelerde ayrıntılı yönergeler bulunabilir:

* [macOS'ta PowerShell Core'u yükleme](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Linux'ta PowerShell Core'u yükleme](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>.NET Core için Azure PowerShell'i yükleme

PowerShell Core, PowerShellGet modülü önceden yüklü biçimde gelir. Modüllerin PowerShell'de yüklenebilmesi için yükseltilmiş ayrıcalıklar gerektiğinden oturumunuzu süper kullanıcı olarak başlatmanız gerekir:

```bash
sudo pwsh
```

Azure PowerShell'i yüklemek için şu komutu çalıştırın:

```powershell
Install-Module Az
```

> [!IMPORTANT]
> Diğer makalelerde ayrıntıları verilen `AzureRM` modülü .NET Core için tasarlanmamıştır ve PowerShell Core ile çalışmaz. `Az` modülleri tüm `AzureRM` cmdlet'leri için komut diğer adlarını içerdiğinden `AzureRM` belgelerinin tamamı geçerlidir.

PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır. PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.

## <a name="sign-in"></a>Oturum aç

Azure PowerShell ile çalışmaya başlamak için `Az` modülünü PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yükledikten sonra Azure kimlik bilgilerinizle oturum açmanız gerekir. Modülü içeri aktarmak için yükseltilmiş ayrıcalıklara __gerek yoktur__.

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir. `Az` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).
macOS ve Linux'ta profilinizle `$Profile` ortam değişkeni üzerinden çalışmanız gerekir. Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.
