# <a name="azure-stack-module-140"></a><span data-ttu-id="5848d-101">Azure Stack Modülü 1.4.0</span><span class="sxs-lookup"><span data-stu-id="5848d-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="5848d-102">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="5848d-102">Requirements:</span></span>
<span data-ttu-id="5848d-103">Desteklenen en düşük Azure Stack sürümü 1804’tür.</span><span class="sxs-lookup"><span data-stu-id="5848d-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="5848d-104">Not: Daha önceki bir sürümü kullanıyorsanız sürüm 1.2.11’i yükleyin</span><span class="sxs-lookup"><span data-stu-id="5848d-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="5848d-105">Bilinen sorunlar:</span><span class="sxs-lookup"><span data-stu-id="5848d-105">Known issues:</span></span>

- <span data-ttu-id="5848d-106">Uyarıyı Kapatma için Azure Stack sürümü 1803 gereklidir</span><span class="sxs-lookup"><span data-stu-id="5848d-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="5848d-107">New-AzsOffer komutu genel durumlu bir teklif oluşturmaya izin vermez.</span><span class="sxs-lookup"><span data-stu-id="5848d-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="5848d-108">Durumu değiştirmek için Set-AzsOffer cmdlet’inin sonradan çağrılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5848d-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="5848d-109">IP Havuzu, yeniden dağıtma olmadan kaldırılamaz</span><span class="sxs-lookup"><span data-stu-id="5848d-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="5848d-110">Hataya Neden Olan Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5848d-110">Breaking Changes</span></span>
<span data-ttu-id="5848d-111">1.3.0 sürümünden sonra hataya neden olan değişiklik yapılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="5848d-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="5848d-112">1.2.11’den geçirilen tüm hataya neden olan değişiklikler burada https://aka.ms/azspowershellmigration belgelenmiştir</span><span class="sxs-lookup"><span data-stu-id="5848d-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="5848d-113">Yükleme</span><span class="sxs-lookup"><span data-stu-id="5848d-113">Install</span></span>
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
## <a name="release-notes"></a><span data-ttu-id="5848d-114">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="5848d-114">Release Notes</span></span>
    * <span data-ttu-id="5848d-115">Azurestack 1.4.0 sürümde, önceki 1.3.0 sürümüne göre hataya neden olan değişiklik yapılmamıştır</span><span class="sxs-lookup"><span data-stu-id="5848d-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="5848d-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="5848d-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="5848d-117">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="5848d-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5848d-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="5848d-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="5848d-119">Set-AzsBackupShare cmdlet’inde yeni BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="5848d-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="5848d-120">Şifreleme anahtarı oluşturmayı kolaylaştırmak için yeni bir New-EncyptionKeyBase64 cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="5848d-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="5848d-121">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="5848d-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5848d-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="5848d-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="5848d-123">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="5848d-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5848d-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="5848d-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="5848d-125">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="5848d-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="5848d-126">Yöneticinin azurestack damgasına yeni ölçek birimleri ekleyebilmesi için yeni Add-AzsScaleUnitNode cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="5848d-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="5848d-127">Ölçek birimi parametre nesnelerinin oluşturulmasını kolaylaştırmak için cmdlet ve New-AzsScaleUnitNodeObject eklendi</span><span class="sxs-lookup"><span data-stu-id="5848d-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="5848d-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="5848d-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="5848d-129">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="5848d-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5848d-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="5848d-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="5848d-131">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="5848d-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5848d-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="5848d-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="5848d-133">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="5848d-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5848d-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="5848d-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="5848d-135">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="5848d-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5848d-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="5848d-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="5848d-137">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="5848d-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="5848d-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="5848d-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="5848d-139">Abonelikleri temsilcili sağlayıcı teklifleri arasında taşıyabilmek için Move-AzsSubscription cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="5848d-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="5848d-140">Kullanıcı aboneliklerinin temsilcili sağlayıcı teklifleri arasında taşınabildiğini doğrulamak için Test-AzsMoveSubscription cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="5848d-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="5848d-141">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme'</span><span class="sxs-lookup"><span data-stu-id="5848d-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="5848d-142">İçerik:</span><span class="sxs-lookup"><span data-stu-id="5848d-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="5848d-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="5848d-143">Azure Bridge</span></span>
<span data-ttu-id="5848d-144">Resimleri Azure’dan genel olarak dağıtmaya olanak tanıyan Azure Stack AzureBridge yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="5848d-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="5848d-145">Backup</span><span class="sxs-lookup"><span data-stu-id="5848d-145">Backup</span></span>
<span data-ttu-id="5848d-146">Yöneticilerin şunları yapmasını sağlayan Yedekleme yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="5848d-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="5848d-147">Yedeklemelerin nerede depolandığını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5848d-147">Configure where backups are stored</span></span>
- <span data-ttu-id="5848d-148">yedekleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="5848d-148">Perform backups</span></span>
- <span data-ttu-id="5848d-149">Tamamlanan yedeklemeyi listeleme ve geri yükleme</span><span class="sxs-lookup"><span data-stu-id="5848d-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="5848d-150">Ticaret</span><span class="sxs-lookup"><span data-stu-id="5848d-150">Commerce</span></span>
<span data-ttu-id="5848d-151">Azure Stack sisteminde toplu veri kullanımını görüntülemenin bir yolunu sağlayan Azure Stack Ticaret yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="5848d-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="5848d-152">İşlem</span><span class="sxs-lookup"><span data-stu-id="5848d-152">Compute</span></span>
<span data-ttu-id="5848d-153">Kota işleme, platform resimleri ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="5848d-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="5848d-154">Fabric</span><span class="sxs-lookup"><span data-stu-id="5848d-154">Fabric</span></span>
<span data-ttu-id="5848d-155">Yöneticilerin altyapı bileşenlerini görüntülemesine ve yönetmesine olanak tanıyan Azure Stack Fabric yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="5848d-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="5848d-156">Ölçek birimi düğümlerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="5848d-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="5848d-157">FRU ilişkili etkinlikler için ölçek birimi düğümlerinin Boşaltılması ve Sürdürülmesi</span><span class="sxs-lookup"><span data-stu-id="5848d-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="5848d-158">Ölçek birimi düğümlerinin onarımı</span><span class="sxs-lookup"><span data-stu-id="5848d-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="5848d-159">Altyapı rolünün yeniden başlatılması</span><span class="sxs-lookup"><span data-stu-id="5848d-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="5848d-160">Altyapı rolü örneklerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="5848d-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="5848d-161">Yeni IP Havuzları oluşturma</span><span class="sxs-lookup"><span data-stu-id="5848d-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="5848d-162">Galeri</span><span class="sxs-lookup"><span data-stu-id="5848d-162">Gallery</span></span>
<span data-ttu-id="5848d-163">Azure Stack marketinde galeri öğelerini yönetme işlevini sunan Azure Stack Galeri yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="5848d-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="5848d-164">Altyapı Öngörüleri</span><span class="sxs-lookup"><span data-stu-id="5848d-164">Infrastructure Insights</span></span>
<span data-ttu-id="5848d-165">Yöneticilere şunları yapmasını sağlayan Infrastructure Insights yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="5848d-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="5848d-166">Azure Stack damga kaynaklarının sistem durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5848d-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="5848d-167">Uyarıları görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="5848d-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="5848d-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="5848d-168">KeyVault</span></span>
<span data-ttu-id="5848d-169">Yöneticinin KeyVault kotalarını görüntülemesine oplanak tanıyan Azure Stack KeyVault yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="5848d-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="5848d-170">Ağ</span><span class="sxs-lookup"><span data-stu-id="5848d-170">Network</span></span>
<span data-ttu-id="5848d-171">Şunlara olanak tanıyan Ağ yöneticisi modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="5848d-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="5848d-172">Ağ kotalarının yönetimi</span><span class="sxs-lookup"><span data-stu-id="5848d-172">Management of network quotas</span></span>
- <span data-ttu-id="5848d-173">Genel IP adresleri, sanal ağlar, yük dengeleyicileri gibi ayrılan ağ kaynaklarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5848d-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="5848d-174">Yönetici genel bakışı gösteren bir cmdlet sunar</span><span class="sxs-lookup"><span data-stu-id="5848d-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="5848d-175">Depolama</span><span class="sxs-lookup"><span data-stu-id="5848d-175">Storage</span></span>
<span data-ttu-id="5848d-176">Azure Stack Depolama yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="5848d-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="5848d-177">Bu sürümde şunların yapılmasını sağlayan işlevleri sunuyoruz:</span><span class="sxs-lookup"><span data-stu-id="5848d-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="5848d-178">Depolama kotalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="5848d-178">Manage storage quotas</span></span>
- <span data-ttu-id="5848d-179">Silinen depolama kaynaklarına yönelik atık toplama</span><span class="sxs-lookup"><span data-stu-id="5848d-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="5848d-180">Silinen depolama hesaplarını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="5848d-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="5848d-181">Kapsayıcıları bir paydan diğerine geçirme</span><span class="sxs-lookup"><span data-stu-id="5848d-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="5848d-182">Bireysel depolama bileşenleri hakkında bilgileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5848d-182">View information about the individual storage components</span></span>
- <span data-ttu-id="5848d-183">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5848d-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="5848d-184">Abonelik Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="5848d-184">Subscription Admin</span></span>
<span data-ttu-id="5848d-185">Azure Stack Aboneliği yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="5848d-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="5848d-186">Bu modül yöneticilerin şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="5848d-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="5848d-187">Plan ve teklifleri yönetme</span><span class="sxs-lookup"><span data-stu-id="5848d-187">Manage plans and offers</span></span>
- <span data-ttu-id="5848d-188">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5848d-188">View usage and performance information</span></span>
- <span data-ttu-id="5848d-189">RBAC’yi yönetme</span><span class="sxs-lookup"><span data-stu-id="5848d-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="5848d-190">Abonelik</span><span class="sxs-lookup"><span data-stu-id="5848d-190">Subscription</span></span>
<span data-ttu-id="5848d-191">Azure Stack Aboneliği modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="5848d-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="5848d-192">Bu modül kullanıcıların şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="5848d-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="5848d-193">Abonelikleri Oluşturma, Silme ve Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5848d-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="5848d-194">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5848d-194">Update</span></span>
<span data-ttu-id="5848d-195">Azure Stack Güncelleştirme yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="5848d-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="5848d-196">Bu modülde yöneticiler şunları yapabilir:</span><span class="sxs-lookup"><span data-stu-id="5848d-196">In this module administrators can:</span></span>
- <span data-ttu-id="5848d-197">Kullanılabilir güncelleştirmeleri listeleme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="5848d-197">List and install available updates</span></span>
- <span data-ttu-id="5848d-198">Kesintiye uğrayan güncelleştirmeleri sürdürme</span><span class="sxs-lookup"><span data-stu-id="5848d-198">Resume interrupted updates</span></span>
- <span data-ttu-id="5848d-199">Yüklü güncelleştirmeleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5848d-199">View installed updates</span></span>
