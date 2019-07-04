---
title: Azure Stack PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack için PowerShell’e genel bakış.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038202"
---
# <a name="azurerm-module-250"></a>AzureRM 2.5.0 Modulü

## <a name="requirements"></a>Gereksinimler:
Desteklenen en düşük Azure Stack sürümü 1904'dir.

Not: Daha önceki bir sürümü kullanıyorsanız 1.2.11 sürümünü yükleyin


## <a name="install"></a>Yükleme
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a>Sürüm Notları
* AzureRM.Resources
    * 2019-03-01-hybrid profiliyle 2018-05-01- api sürümünü destekleyen yeni Resources modülü
    * PolicyDefinition(2016-12-01) ve PolicyAssisgment(2017-06-01-preview) işlemleri halen eski api sürümlerine sahiptir
* AzureRm.Compute
    * 2017-12-01 API sürümünü destekleyen yeni işlem modülü.’


* Bu sürüm özel Azure Stack API profili 2019-03-01-hybrid sürümüne karşılık gelmektedir
* Tüm modüller AzureRm.Profile modülü bağımlılığı için daha büyük veya eşit hale geldi.
* Modüller tarafından desteklenen API sürümleri güncelleştirildi. 
    * İşlem - 2017-12-30
    * Ağ - 01.10.2017
    * Depolama - 01.01.2016
    * Kaynaklar - 01.02.2018
    * Anahtar Kasası - 01.10.2016
    * DNS - 01.04.2016
* Bu kaynak türlerinin her biri için tam kapsamlı API sürümü eşlemesi için bkz. https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json

## <a name="content"></a>İçerik:
### <a name="azure-bridge"></a>Azure Bridge
Resimleri Azure’dan genel olarak dağıtmaya olanak tanıyan Azure Stack AzureBridge yönetici modülünün önizleme sürümü.

### <a name="backup"></a>Backup
Yöneticilerin şunları yapmasını sağlayan Yedekleme yönetici modülünün önizleme sürümü:
- Yedeklemelerin nerede depolandığını yapılandırma
- yedekleme gerçekleştirme
- Tamamlanan yedeklemeyi listeleme ve geri yükleme

### <a name="commerce"></a>Ticaret
Azure Stack sisteminde toplu veri kullanımını görüntülemenin bir yolunu sağlayan Azure Stack Ticaret yönetici modülünün önizleme sürümü.

### <a name="compute"></a>İşlem
Kota işleme, platform görüntüleri, yönetilen diskler ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.

### <a name="fabric"></a>Fabric
Yöneticilerin altyapı bileşenlerini görüntülemesine ve yönetmesine olanak tanıyan Azure Stack Fabric yönetici modülünün önizleme sürümü:
- Ölçek birimi düğümlerinin Durdurulması, Başlatılması ve Kapatılması
- FRU ilişkili etkinlikler için ölçek birimi düğümlerinin Boşaltılması ve Sürdürülmesi
- Ölçek birimi düğümlerinin onarımı
- Altyapı rolünün yeniden başlatılması
- Altyapı rolü örneklerinin Durdurulması, Başlatılması ve Kapatılması
- Yeni IP Havuzları oluşturma


### <a name="gallery"></a>Galeri
Azure Stack marketinde galeri öğelerini yönetme işlevini sunan Azure Stack Galeri yönetici modülünün önizleme sürümü.

### <a name="infrastructure-insights"></a>Altyapı Öngörüleri
Yöneticilere şunları yapmasını sağlayan Infrastructure Insights yönetici modülünün önizleme sürümü:
- Azure Stack damga kaynaklarının sistem durumunu görüntüleme
- Uyarıları görüntüleme ve yönetme

### <a name="keyvault"></a>KeyVault
Yöneticinin KeyVault kotalarını görüntülemesine oplanak tanıyan Azure Stack KeyVault yönetici modülünün önizleme sürümü.

### <a name="network"></a>Ağ
Şunlara olanak tanıyan Ağ yöneticisi modülünün önizleme sürümü:
- Ağ kotalarının yönetimi
- Genel IP adresleri, sanal ağlar, yük dengeleyicileri gibi ayrılan ağ kaynaklarını görüntüleme
- Yönetici genel bakışı gösteren bir cmdlet sunar

### <a name="storage"></a>Depolama
Azure Stack Depolama yönetici modülünün önizleme sürümü.  Bu sürümde şunların yapılmasını sağlayan işlevleri sunuyoruz:
- Depolama kotalarını yönetme
- Silinen depolama kaynaklarına yönelik atık toplama
- Silinen depolama hesaplarını geri yükleme
- Kapsayıcıları bir paydan diğerine geçirme
- Bireysel depolama bileşenleri hakkında bilgileri görüntüleme
- Kullanım ve performans bilgilerini görüntüleme

### <a name="subscription-admin"></a>Abonelik Yöneticisi
Azure Stack Aboneliği yönetici modülünün önizleme sürümü.  Bu modül yöneticilerin şunları yapmasını sağlayan işlevler sunar:
- Plan ve teklifleri yönetme
- Kullanım ve performans bilgilerini görüntüleme
- RBAC’yi yönetme

### <a name="subscription"></a>Abonelik
Azure Stack Aboneliği modülünün önizleme sürümü.  Bu modül kullanıcıların şunları yapmasını sağlayan işlevler sunar:
- Abonelikleri Oluşturma, Silme ve Güncelleştirme

### <a name="update"></a>Güncelleştirme
Azure Stack Güncelleştirme yönetici modülünün önizleme sürümü.  Bu modülde yöneticiler şunları yapabilir:
- Kullanılabilir güncelleştirmeleri listeleme ve yükleme
- Kesintiye uğrayan güncelleştirmeleri sürdürme
- Yüklü güncelleştirmeleri görüntüleme
