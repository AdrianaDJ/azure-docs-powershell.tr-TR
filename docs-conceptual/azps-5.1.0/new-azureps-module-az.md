---
title: Azure Az PowerShell modülüne giriş
description: AzureRM PowerShell modülünün yerine gelen ve Azure ile etkileşim kurmak için önerilen Az PowerShell modülüne giriş.
ms.date: 12/1/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: a3b74531ff71ed0e9ac473831b71efb6f29d6e66
ms.sourcegitcommit: 7887e040bdeb2f55c035a3169cd0d9d807ab186e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2020
ms.locfileid: "96536553"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Azure Az PowerShell modülüne giriş

## <a name="overview"></a>Genel Bakış

Az PowerShell modülü, Azure kaynaklarını doğrudan PowerShell’den yönetmeye yönelik bir dizi cmdlet’ten oluşur. PowerShell, bir CI/CD işlem hattı bağlamındakiler gibi örneklere yönelik Azure kaynaklarınızın yönetilmesi için kullanılabilen güçlü otomasyon özellikleri sağlar.

AzureRM’nin yerini alan Az PowerShell modülü, Azure ile etkileşim kurmak için kullanılması önerilen sürümdür.

Az PowerShell modülünü aşağıdaki yöntemlerden biriyle kullanabilirsiniz:

* [Az PowerShell modülünü PowerShellGet aracılığıyla yükleme](install-az-ps.md) (önerilen seçenek).
* [Az PowerShell modülünü MSI ile yükleme](install-az-ps-msi.md).
* [Azure Cloud Shell’i kullanma](/azure/cloud-shell/overview).
* [Az PowerShell Docker kapsayıcısını kullanma](azureps-in-docker.md).

## <a name="features"></a>Özellikler

Az PowerShell modülü şu avantajları sunar:

* Güvenlik ve kararlılık
  * Belirteç önbelleği şifrelemesi
  * ADFS 2019 için destek
  * Ortadaki adam saldırısı türlerini engelleyen güvenlik mekanizması
  * Sürekli erişim değerlendirmesi gibi özellikler için destek (2021’de sunulacak)
* Tüm Azure hizmetleri için destek
  * Her Azure hizmeti için bir modül sunulur
  * AzureRM’den sonra yapılan birçok hata düzeltmesi ve API sürümü yükseltmeleri
* Birkaç ek yeni özellik
  * Cloud Shell için ve platformlar arası destek
  * Azure kaynaklarına erişmek için erişim belirteci alınıp kullanılabilir
  * Kaçış noktası türü işlemler için genel Az cmdlet’i

> [!NOTE]
> PowerShell 7 ve üzeri, tüm platformlarda Az PowerShell ile kullanılması önerilen PowerShell sürümüdür.

.NET Standard kitaplığını temel alan Az PowerShell modülü Windows, macOS ve Linux dahil tüm platformlarda PowerShell 7 ve üzeri sürümlerle birlikte çalışır. Ayrıca Windows PowerShell 5.1 ile de uyumludur.

Azure desteğini tüm platformlara getirmek için çalışıyoruz. Tüm Az PowerShell modülleri platformlar arası kullanılabilir.

## <a name="upgrade-your-environment-to-az"></a>Ortamınızı Az’ye yükseltin

PowerShell'de en son Azure özelliklerine sahip olmak için Az modülüne geçmelisiniz. AzureRM yerine Az modülünü yüklemeye hazır değilseniz, Az modülünü denemek için çeşitli seçenekleriniz vardır:

* [Azure Cloud Shell](/azure/cloud-shell/overview) ile bir `PowerShell` ortamı kullanın. Azure Cloud Shell, Az modülü yüklenmiş ve `Enable-AzureRM` uyumluluk diğer adları etkinleştirilmiş olarak gelen tarayıcı tabanlı bir kabuk ortamıdır.
* Windows PowerShell 5.1’de AzureRM modülünü yüklü bırakın ve PowerShell 7 veya sonraki sürümlerde Az modülünü yükleyin. Windows PowerShell 5.1 ile PowerShell 7 ve üzeri, ayrı modül koleksiyonları kullanır. Yönergeleri izleyerek [PowerShell’in en son sürümünü](/powershell/scripting/install/installing-powershell) yükleyin ve ardından PowerShell 7 veya üzeri bir sürümden [Az modülünü yükleyin](install-az-ps.md).

Mevcut AzureRM yüklemesinden yükseltmek için:

1. [Azure PowerShell AzureRM modülünü kaldırın](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [Azure PowerShell Az modülünü yükleyin](install-az-ps.md)
1. **İSTEĞE BAĞLI**: Yeni komut kümesine alışırken [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) ile AzureRM cmdlet’lerine yönelik diğer adları eklemek için uyumluluk modunu etkinleştirin. Daha fazla bilgi için sonraki bölüme veya [AzureRM'den Az’ye geçişi başlatma](migrate-from-azurerm-to-az.md) konusuna bakın.

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>Mevcut betikleri AzureRM’den Az’ye geçirme

Hala AzureRM modülünü temel alan betiklerinizin geçişini gerçekleştirmenize yardımcı olacak birkaç kaynak hazırladık:

* [AzureRM'den Az modülüne geçişi başlatma](migrate-from-azurerm-to-az.md)
* [AzureRM'den Az 1.0.0'a geçişte hataya neden olan değişikliklerin tam listesi](migrate-az-1.0.0.md)
* [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet'i

## <a name="supportability"></a>Desteklenebilirlik

Az, Azure için en güncel PowerShell modülüdür. Sorunları veya özellik isteklerini doğrudan [GitHub deposunda](https://github.com/Azure/azure-powershell) girebilir veya destek sözleşmeniz varsa Microsoft desteği aracılığıyla iletebilirsiniz. Özellik istekleri Az’nin en son sürümünde uygulanacaktır. Kritik sorunların çözümleri Az’nin son iki sürümünde uygulanacaktır.

AzureRM için artık yeni cmdlet’ler veya özellikler sağlanmayacaktır. Bununla birlikte, AzureRM modülü hala resmi olarak bakım kapsamındadır ve Şubat 2020’ye kadar kritik düzeltmeleri alacaktır.

## <a name="data-collection"></a>Veri toplama

Azure PowerShell varsayılan olarak telemetri verilerini toplar. Microsoft, yaygın sorunları belirlemek ve Azure PowerShell deneyimini geliştirmek amacıyla kullanım desenlerini belirlemek için toplanan verileri kümeler.
Microsoft Azure PowerShell özel veya kişisel verileri toplamaz. Örneğin, kullanım verileri, düşük başarı oranına sahip cmdlet’ler gibi sorunların tanımlanmasına ve çalışmalarımızın önceliğinin belirlenmesine yardımcı olur.

Bu verilerin sağladığı içgörüler bizim için önemli olsa da herkesin kullanım verilerini göndermek istemeyebileceğini de anlıyoruz. Veri toplama işlemini [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) cmdlet’iyle devre dışı bırakabilirsiniz. Daha fazla bilgi edinmek için [gizlilik bildirimimizi](https://privacy.microsoft.com/privacystatement) de okuyabilirsiniz.
