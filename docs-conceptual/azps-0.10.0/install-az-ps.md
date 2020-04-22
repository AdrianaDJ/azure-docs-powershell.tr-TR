---
title: Azure PowerShell'i PowerShellGet ile yükleme
description: Azure PowerShell PowerShellGet ile nasıl yüklenir
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.openlocfilehash: 7a25270566f5e856ee44c4c191a47a3e7334508b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "81445705"
---
# <a name="install-azure-powershell"></a>Azure PowerShell'i yükleme

Bu makalede, PowerShellGet kullanarak Azure PowerShell modüllerinin nasıl yüklendiği ele alınır. Bu yönergeler Windows, macOS ve Linux platformlarında kullanılabilir.

Azure PowerShell, Azure [Cloud Shell](/azure/cloud-shell/overview)’de de sunulur ve şimdi, [Docker görüntülerine](azureps-in-docker.md) önceden yüklenir.

## <a name="requirements"></a>Gereksinimler

Azure PowerShell, Windows’da PowerShell 5.1 veya sonraki sürümleriyle veya tüm platformlarda PowerShell 6.x ve sonraki sürümleriyle çalışır. İşletim sisteminiz için sunulan [en son PowerShell Core sürümünü](/powershell/scripting/install/installing-powershell#powershell-core) yüklemeniz gerekir. PowerShell Core’da çalıştırıldığında PowerShell için ek gereksinim yoktur.

PowerShell sürümünüzü denetlemek için şu komutu çalıştırın:

```powershell-interactive
$PSVersionTable.PSVersion
```

Azure PowerShell’i Windows üzerinde PowerShell 5.1’de kullanmak için:

1. Gerekirse [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell)'e güncelleştirin. Windows 10 kullanıyorsanız, zaten PowerShell 5.1 yüklüdür.
2. [.NET Framework 4.7.2 veya sonraki sürümünü](/dotnet/framework/install) yükleyin.
3. En son PowerShellGet sürümünü kullandığınızdan emin olun. `Update-Module PowerShellGet -Force` öğesini çalıştırın.

## <a name="install-the-azure-powershell-module"></a>Azure PowerShell modülünü yükleme

PowerShellGet cmdlet’lerinin kullanılması, tercih edilen yükleme yöntemidir. Bu yöntem Windows, macOS ve Linux platformlarında aynı şekilde çalışır. Bir PowerShell oturumunda aşağıdaki komutu çalıştırın:

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

PowerShell galerisi varsayılan olarak PowerShellGet için güvenilir depo olarak yapılandırılmamıştır. PSGallery'yi ilk kez kullandığınızda şu istemle karşılaşırsınız:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Yükleme işlemine devam etmek için `Yes` veya `Yes to All` yanıtını verin.

Az modülü, Azure PowerShell cmdlet’leri için toplu bir modüldür. Bu modülü yüklediğinizde kullanılabilir durumdaki tüm Azure Resource Manager modülleri indirilir ve cmdlet'leri kullanıma sunulur.

> [!WARNING]
> Windows için PowerShell 5.1’de aynı anda hem AzureRM hem de Az modülününün yüklenmesi desteklenmez. Sisteminizde AzureRM'yi kullanılabilir durumda tutmanız gerekiyorsa, PowerShell Core 6.x veya sonraki sürümleri için Az modülünü yükleyin.

İlk olarak, [PowerShell Core 6.x veya üstünü yükleyin](/powershell/scripting/install/installing-powershell-core-on-windows)

Ardından, bir PowerShell Core oturumundan yalnızca geçerli kullanıcı için Az modülünü yükleyin. Bu, önerilen yükleme kapsamıdır.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Modülün bir sistemdeki tüm kullanıcılar için yüklenmesi, yükseltilmiş ayrıcalıklar gerektirir. Windows’ta **Yönetici olarak çalıştır** seçeneğini kullanarak ya da macOS veya Linux’ta `sudo` komutunu kullanarak PowerShell oturumunu başlatın:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

## <a name="install-offline"></a>Çevrimdışı yükleme

Bazı ortamlarda PowerShell Galerisi'ne bağlanmak mümkün olmaz. Bu durumlarda yine de aşağıdaki yöntemlerden birini kullanarak çevrimdışı yükleyebilirsiniz:

* Modülleri ağınızdaki başka bir konuma indirin ve bu konumu yükleme kaynağı olarak kullanın.
  Bu, PowerShell modüllerini PowerShellGet ile bağlantısız sistemlere dağıtmak üzere tek sunucuda veya dosya paylaşımında önbelleğe almanızı sağlar. Yerel depoyu ayarlamayı ve bağlantısız sistemlerde yüklemeyi öğrenmek için [Yerel PowerShellGet depolarıyla çalışma](/powershell/scripting/gallery/how-to/working-with-local-psrepositories) konusundan yararlanın.
* Ağa bağlı bir makineye [Azure PowerShell MSI'yi indirin](install-az-ps-msi.md) ve sonra PowerShell Galerisi'ne erişimi olmayan sistemlere yükleyiciyi kopyalayın. MSI yükleyicisinin yalnızca Windows üzerinde PowerShell 5.1 için kullanılabildiğini unutmayın.
* Modülü [Save-Module](/powershell/module/PowershellGet/Save-Module) ile bir dosya paylaşımına kaydedin veya başka bir konuma kaydedin ve sonra el ile diğer makinelere kopyalayın:

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Sorun giderme

Azure PowerShell modülünü yüklerken karşılaşılan yaygın sorunlardan bazıları burada verilmiştir. Burada listelenmeyen bir sorunla karşılaşırsanız, [github’da bir sorun oluşturun](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Ara sunucu blokları bağlantısı

`Install-Module` cmdlet'inden PowerShell Galerisi'ne ulaşılamadığını belirten hatalar alıyorsanız, bir ara sunucunun arkasında olabilirsiniz. Farklı işletim sistemlerinin ve ağ ortamlarının sistem genelinde ara sunucu yapılandırmaya ilişkin gereksinimleri farklıdır. Ara sunucu ayarlarınız ve ortamınızda bunları nasıl yapılandıracağınız konusunda sistem yöneticinize danışın.

PowerShell'in kendisi otomatik olarak bu ara sunucuyu kullanacak şekilde yapılandırılamaz. Aşağıdaki komutları kullanarak PowerShell 5.1 ve sonraki sürümlerinde PowerShell oturumunu bir ara sunucu kullanacak şekilde yapılandırın:

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

İşletim sistemi kimlik bilgileriniz doğru yapılandırıldıysa, bu yapılandırma PowerShell isteklerini ara sunucu üzerinden yönlendirir. Bu ayarın oturumlar arasında kalıcı olmasını sağlamak için, komutu [PowerShell profilinize](/powershell/module/microsoft.powershell.core/about/about_profiles) ekleyin.

Paketi yüklemek için ara sunucunuzun şu adrese yönelik HTTPS bağlantılarına izin vermesi gerekir:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Oturum aç

Azure PowerShell ile çalışmaya başlamak için, Azure kimlik bilgilerinizle oturum açın.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> Modül otomatik yüklemesini devre dışı bıraktıysanız, `Import-Module Az` kullanarak modülü el ile içeri aktarın. Modülü yapısından dolayı, bu işlem birkaç saniye sürebilir.

Başlattığınız her yeni PowerShell oturumu için bu adımları tekrarlamanız gerekir. Azure oturum açma bilgilerinizin PowerShell oturumları arasında geçiş yaparken silinmemesi için bkz. [Kullanıcı kimlik bilgilerini PowerShell oturumlarında kalıcı hale getirme](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Azure PowerShell modülünü güncelleştirme

Bir PowerShell modülünü güncelleştirmek için modülü yüklerken kullandığınız yöntemi kullanmanız gerekir. Örneğin, ilk olarak `Install-Module` kullandıysanız en son sürümü edinmek için [Update-Module](/powershell/module/powershellget/update-module) kullanmanız gerekir. İlk olarak MSI paketini kullandıysanız yeni MSI paketini indirip yüklemeniz gerekir.

PowerShellGet cmdlet’leri bir MSI paketinden yüklenen modülleri güncelleştiremez. MSI paketleri PowerShellGet kullanılarak yüklenen modülleri güncelleştirmez. PowershellGet kullanarak güncelleştirmeyle ilgili sorun yaşıyorsanız, **güncelleştirme** yerine **yeniden yüklemeniz** gerekir. Yeniden yükleme, yükleme ile aynı şekilde yapılır ancak `-Force` parametresini eklemeniz gerekir:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

MSI tabanlı yüklemelerin aksine, PowerShellGet kullanarak yükleme veya güncelleştirme yapmanız, sisteminizde bulunan eski sürümleri kaldırmaz. Sisteminizdeki eski Azure PowerShell sürümlerini kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md). MSI tabanlı yüklemeler hakkında daha fazla bilgi edinmek için bkz. [MSI ile Azure PowerShell’i yükleme](install-az-ps-msi.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Azure PowerShell'in birden çok sürümünü kullanma

Azure PowerShell'in birden çok sürümünü yüklemek mümkündür. Birden fazla Azure PowerShell sürümünün yüklü olup olmadığını denetlemek için şu komutu kullanın:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Azure PowerShell'in bir sürümünü kaldırmak için bkz. [Azure PowerShell modülünü kaldırma](uninstall-az-ps.md).

Modülün birden çok sürümünü yüklediyseniz, modül otomatik yükleme ve `Import-Module` tarafından varsayılan olarak en son sürüm yüklenir.

`-RequiredVersion` parametresini kullanarak `Az` modülünün belirli bir sürümünü yükleyebilirsiniz:

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a>Geri bildirimde bulunma

Azure PowerShell’de bir hata bulursanız [GitHub’da sorun bildirin](https://github.com/Azure/azure-powershell/issues). Komut satırından geri bildirim sağlamak için [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet'ini kullanın.

## <a name="next-steps"></a>Sonraki Adımlar

Azure PowerShell modülleri ve bunların özellikleri hakkında daha fazla bilgi edinmek için bkz. [Azure PowerShell’i Kullanmaya Başlama](get-started-azureps.md). Azure PowerShell’i zaten biliyorsanız ve AzureRM’den geçiş yapmanız gerekiyorsa bkz. [AzureRM’den Az’ye geçiş](migrate-from-azurerm-to-az.md).
