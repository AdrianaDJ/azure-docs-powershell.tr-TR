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
ms.openlocfilehash: cd415e862bfaa2b767cce108689ebaf34ef74305
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586930"
---
# <a name="azurerm-module-230"></a>AzureRM Modülü 2.3.0

## <a name="requirements"></a>Gereksinimler:
Desteklenen en düşük Azure Stack sürümü 1808 sürümüdür.

Not: Daha önceki bir sürümü kullanıyorsanız sürüm 1.2.11’i yükleyin


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
* 2.3.0 sürümünde birçok hataya neden olan değişiklik bulunmaktadır. 1.2.11 sürümünden yükseltmek için https://aka.ms/azspowershellmigration sayfasındaki geçiş kılavuzuna bakabilirsiniz
* Bu sürüm özel Azure Stack API profili 2018-03-01-hybrid sürümüne karşılık gelmektedir
* Tüm modüller AzureRm.Profile modülü bağımlılığı için daha büyük veya eşit hale geldi.
* Modüller tarafından desteklenen API sürümleri güncelleştirildi. 
    * İşlem - 30.03.2017
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
