---
title: Azure PowerShell'i PowerShellGet ile yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: ead6c48496c646b5184f88aeac64fbe650be17c4
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498299"
---
# <a name="install-the-azure-powershell-module"></a>Azure PowerShell modülünü yükleme

Bu makalede, PowerShellGet kullanarak Azure PowerShell modüllerini nasıl yükleyeceğiniz anlatılır. Bu yönergeler Windows, macOS ve Linux platformlarında kullanılabilir. Az modülü için şu anda başka desteklenen yükleme metodu yoktur.

## <a name="requirements"></a>Gereksinimler

Azure PowerShell, Windows’da PowerShell 5.1 veya sonraki sürümleriyle veya tüm platformlarda PowerShell 6.x ve sonraki sürümleriyle çalışır. PowerShell'iniz olup olmadığından veya macOS mu yoksa Linux mı kullandığınızdan emin değilseniz, [PowerShell Core'un en son sürümünü yükleyin](/powershell/scripting/install/installing-powershell#powershell-core).

PowerShell sürümünüzü denetlemek için şu komutu çalıştırın:

```powershell-interactive
$PSVersionTable.PSVersion
```

Azure PowerShell'i Windows üzerinde PowerShell 5.1'de çalıştırmak için:

1. Gerekirse [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)'e güncelleştirin. Windows 10 kullanıyorsanız, zaten PowerShell 5.1 yüklüdür.
2. [.NET Framework 4.7.2 veya sonraki sürümünü](/dotnet/framework/install) yükleyin.

PowerShell Core kullanıldığında, Azure PowerShell için ek gereksinimler yoktur.

## <a name="install-the-azure-powershell-module"></a>Azure PowerShell modülünü yükleme

> [!WARNING]
> Windows için PowerShell 5.1'de aynı anda hem AzureRM hem de Az modülünü __yükleyemezsiniz__. Sisteminizde AzureRM'yi kullanılabilir durumda tutmanız gerekiyorsa, PowerShell Core 6.x veya sonraki sürümleri için Az modülünü yükleyin. Bunu yapmak için [PowerShell Core 6.x veya sonraki sürümünü yükleyin](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows) ve ardından PowerShell Core terminalinde bu yönergeleri izleyin.

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

Az modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür. Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.

## <a name="troubleshooting"></a>Sorun giderme

Azure PowerShell modülünü yüklerken karşılaşılan yaygın sorunlardan bazıları burada verilmiştir. Burada listelenmeyen bir sorunla karşılaşırsanız, [github’da bir sorun oluşturun](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Ara sunucu blokları bağlantısı

`Install-Module` cmdlet'inden PowerShell Galerisi'ne ulaşılamadığını belirten hatalar alıyorsanız, bir ara sunucunun arkasında olabilirsiniz. Sistem genelinde ara sunucu yapılandırma konusunda farklı işletim sistemlerinin farklı gereksinimleri olacaktır ve burada bunlar ayrıntılı olarak ele alınmamıştır. Ara sunucu ayarlarınız ve işletim sisteminiz için bunları nasıl yapılandıracağınız konusunda sistem yöneticinize danışın.

PowerShell'in kendisi otomatik olarak bu ara sunucuyu kullanacak şekilde yapılandırılamaz. PowerShell 5.1 ve sonraki sürümleriyle, aşağıdaki komutu kullanarak PowerShell oturumunda kullanılacak ara sunucuyu yapılandırın:

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

İşletim sistemi kimlik bilgileriniz doğru yapılandırıldıysa, bu işlem PowerShell isteklerini ara sunucu üzerinden yönlendirir.
Bu ayarın oturumlar arasında kalıcı olmasını sağlamak için, komutu [PowerShell profiline](/powershell/module/microsoft.powershell.core/about/about_profiles) ekleyin.

Paketi yüklemek için ara sunucunuzun şu adrese yönelik HTTPS bağlantılarına izin vermesi gerekir:

* `https://www.powershellgallery.com`

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

Az modülünün paketlenme şeklinden dolayı, [Update-Module](/powershell/module/powershellget/update-module) komutu yüklemenizi doğru güncelleştirmeyecektir. Az modülü teknik olarak, Azure hizmetleriyle etkileşime yönelik cmdlet'lerin yer aldığı tüm alt modülleri kapsayan bir meta modülüdür. Başka bir deyişle, Azure PowerShell modülünü güncelleştirmek için yalnızca __güncelleştirmek__ yerine __yeniden yüklemeniz__ gerekir. Bu işlem yüklemeyle aynı şekilde yapılır ama `-Force` bağımsız değişkenini eklemeniz gerekebilir:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Bu yüklü modüllerin üzerine yazabilse de, sisteminizde yine de eski sürümler kalabilir.
Sisteminizdeki eski Azure PowerShell sürümlerini nasıl kaldıracağınızı öğrenmek için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Azure PowerShell'in birden çok sürümünü kullanma

Azure PowerShell'in birden çok sürümünü yüklemek mümkündür. Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).

`-RequiredVersion` bağımsız değişkenini kullanarak `Az` modülünün belirli bir sürümünü yükleyebilirsiniz:

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Modülün birden çok sürümünü yüklediyseniz, modül otomatik yükleme ve `Import-Module` tarafından varsayılan olarak en son sürüm yüklenir.

## <a name="provide-feedback"></a>Geri bildirimde bulunma

Azure Powershell’de bir hata bulursanız [GitHub'da sorun bildirin](https://github.com/Azure/azure-powershell/issues).
Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanın.

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md).
Azure PowerShell’i zaten biliyorsanız ve AzureRM’den geçiş yapmanız gerekiyorsa bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).