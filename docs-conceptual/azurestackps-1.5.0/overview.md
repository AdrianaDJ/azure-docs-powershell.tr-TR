---
title: Azure Stack Yönetici için PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack Yönetici için PowerShell’e genel bakış.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 18861f0e5232e0b505767aa9609099afe88f9477
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399442"
---
# <a name="azure-stack-module-150"></a>Azure Stack Modülü 1.5.0

## <a name="requirements"></a>Gereksinimler:
Desteklenen en düşük Azure Stack sürümü 1808 sürümüdür.

Not: Daha önceki bir sürümü kullanıyorsanız 1.4.0 sürümünü yükleyin

## <a name="known-issues"></a>Bilinen sorunlar:

- New-AzsOffer komutu genel durumlu bir teklif oluşturmaya izin vermez. Durumu değiştirmek için Set-AzsOffer cmdlet’inin sonradan çağrılması gerekir.
- IP Havuzu, yeniden dağıtma olmadan kaldırılamaz

## <a name="install"></a>Yükleme
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

##<a name="release-notes"></a>Sürüm Notları
* Tüm Azure Stack Yönetici modülleri AzureRm.Profile modülü bağımlılığı için daha büyük veya eşit olacak şekilde güncelleştirildi
* Tüm modüllere iç içe yerleştirilmiş kaynak adlarını işleme desteği eklendi
* Tüm modüllerde ErrorActionPreference değerinin durdurulacak şekilde geçersiz kılındığı hata düzeltildi
* Azs.Compute.Admin modülü
    * Yönetilen diskleri desteklemek için yeni kota özellikleri eklendi
    * Disk geçişiyle ilgili cmdlet'ler eklendi
    * Platform Görüntüsü ve VM uzantısı nesnelerine ek özellikler eklendi
* Azs.Fabric.Admin 
    * Ölçek birimi düğümü eklemek için yeni cmdlet
* Azs.Backup.Admin
    * Set-AzsBackupShare artık Set-AzsBackupConfiguration cmdlet'inin diğer adı
    * Get-AzsBackupLocation artık Get-AzsBackupConfiguration cmdlet'inin diğer adı
    * Set-AzsBackupConfiguration için BackupShare parametresi artık parametre yolunun diğer adı
* Azs.Subscriptions
    * Get-AzsDelegatedProviderOffer için OfferName parametresi artık Offer parametresinin diğer adı
* Azs.Subscriptions.Admin
    * Get-AzsDelegatedProviderOffer için OfferName parametresi artık Offer parametresinin diğer adı

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
