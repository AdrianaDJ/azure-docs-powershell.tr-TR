# <a name="azure-stack-module-140"></a>Azure Stack Modülü 1.4.0

## <a name="requirements"></a>Gereksinimler:
Desteklenen en düşük Azure Stack sürümü 1804’tür.

Not: Daha önceki bir sürümü kullanıyorsanız sürüm 1.2.11’i yükleyin

## <a name="known-issues"></a>Bilinen sorunlar:

- Uyarıyı Kapatma için Azure Stack sürümü 1803 gereklidir
- New-AzsOffer komutu genel durumlu bir teklif oluşturmaya izin vermez. Durumu değiştirmek için Set-AzsOffer cmdlet’inin sonradan çağrılması gerekir.
- IP Havuzu, yeniden dağıtma olmadan kaldırılamaz

## <a name="breaking-changes"></a>Hataya Neden Olan Değişiklikler
1.3.0 sürümünden sonra hataya neden olan değişiklik yapılmamıştır. 1.2.11’den geçirilen tüm hataya neden olan değişiklikler burada https://aka.ms/azspowershellmigration belgelenmiştir

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
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a>Sürüm Notları
    * Azurestack 1.4.0 sürümde, önceki 1.3.0 sürümüne göre hataya neden olan değişiklik yapılmamıştır
    * Azs.AzureBridge.Admin
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme
    * Azs.Backup.Admin
        - Set-AzsBackupShare cmdlet’inde yeni BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays parametreleri eklendi
        - Şifreleme anahtarı oluşturmayı kolaylaştırmak için yeni bir New-EncyptionKeyBase64 cmdlet’i eklendi
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme
    * Azs.Commerce.Admin
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme
    * Azs.Fabric.Admin
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme
        - Yöneticinin azurestack damgasına yeni ölçek birimleri ekleyebilmesi için yeni Add-AzsScaleUnitNode cmdlet’i eklendi
        - Ölçek birimi parametre nesnelerinin oluşturulmasını kolaylaştırmak için cmdlet ve New-AzsScaleUnitNodeObject eklendi
    * Azs.Gallery.Admin
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme
    * Azs.InfrastructureInsights.Admin
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme
    * Azs.Network.Admin
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme
    * Azs.Update.Admin
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme
    * Azs.Subscriptions
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme
    * Azs.Subscriptions.Admin
        - Abonelikleri temsilcili sağlayıcı teklifleri arasında taşıyabilmek için Move-AzsSubscription cmdlet’i eklendi
        - Kullanıcı aboneliklerinin temsilcili sağlayıcı teklifleri arasında taşınabildiğini doğrulamak için Test-AzsMoveSubscription cmdlet’i eklendi
        - Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme'

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
Kota işleme, platform resimleri ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.

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
