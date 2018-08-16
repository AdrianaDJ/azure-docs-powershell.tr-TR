---
title: Azure PowerShell'i macOS veya Linux'a yükleme
description: Azure PowerShell'i macOS veya Linux'a yükleme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 6e7d447ea9672c174e3f1d103bc56c11a7f37192
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106795"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Azure PowerShell'i macOS veya Linux'a yükleme

Windows dışındaki platformlarda Azure PowerShell'i PowerShell Core v6 ile çalıştırmak mümkündür. PowerShell'in bu sürümü .NET Core destekli tüm platformlarda kullanılacak şekilde tasarlanmıştır. Bu platformlarda çalışmak için Azure PowerShell'in özel bir .NET Core sürümü mevcuttur.

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
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> Diğer makalelerde ayrıntıları verilen `AzureRM` modülü .NET Core için tasarlanmamıştır ve PowerShell Core ile çalışmaz. Hem `AzureRM` hem de `AzureRM.NetCore` aynı cmdlet adlarını kullandığından tek fark, toplu yükleme modülünün adı ve birlikte kullanmak üzere tasarlandıkları .NET sürümüdür.

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

Azure PowerShell ile çalışmaya başlamak için `AzureRM.Netcore` modülünü PowerShell oturumunuza [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet'iyle yükledikten sonra Azure kimlik bilgilerinizle oturum açmanız gerekir. Modülü içeri aktarmak için yükseltilmiş ayrıcalıklara __gerek yoktur__.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir. `AzureRM` modülünün otomatik olarak içeri aktarılması için bir PowerShell profili oluşturmanız gerekir. Ayrıntılı bilgi için bkz. [Profiller Hakkında](/powershell/module/microsoft.powershell.core/about/about_profiles).
macOS ve Linux'ta profilinizle `$Profile` ortam değişkeni üzerinden çalışmanız gerekir. Azure oturum açma bilgilerinizin oturumlar arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).

## <a name="available-cmdlets"></a>Kullanılabilen cmdlet'ler

.NET Core için Azure PowerShell modülleri geliştirme aşamasındadır. Bu modüller, Windows sürümünde kullanılabilecek tüm cmdlet'leri sağlamaz. AzureRM.Netcore modüllerine aşağıdaki işlevler uygulanmıştır:

* Hesap yönetimi
  * Microsoft hesabı, Kuruluş hesabı veya Microsoft Azure Active Directory aracılığıyla Hizmet Sorumlusu ile oturum açma
  * Kimlik Bilgilerini Save-AzureRmContext ile diske kaydetme ve kaydedilen kimlik bilgilerini Import-AzureRmContext ile yükleme
* Ortam
  * Farklı Microsoft Azure ilk çalıştırma ortamlarına ulaşma
  * Özelleştirilmiş ortamları (Azure Stack veya Windows Azure Paketi ortamlarınız gibi) Ekleme/Ayarlama/Kaldırma
* Azure hizmetleri için Resource Manager ve Hizmet Yönetim arabirimlerini kullanan yönetim düzlemi cmdlet'leri.
  * Sanal Makine
  * App Service (Web siteleri)
  * SQL Veritabanı
  * Depolama
  * Ağ

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell'i kullanma hakkında daha fazla bilgi için [Azure PowerShell'i kullanmaya başlama](get-started-azureps.md) makalesine bakın.
