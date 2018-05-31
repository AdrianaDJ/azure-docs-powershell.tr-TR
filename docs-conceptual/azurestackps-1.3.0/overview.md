# <a name="azure-stack-module-130"></a><span data-ttu-id="8c5f4-101">Azure Stack Modülü 1.3.0</span><span class="sxs-lookup"><span data-stu-id="8c5f4-101">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="8c5f4-102">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-102">Requirements:</span></span>
<span data-ttu-id="8c5f4-103">Desteklenen en düşük Azure Stack sürümü 1804’tür.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="8c5f4-104">Not: Daha önceki bir sürümü kullanıyorsanız sürüm 1.2.11’i yükleyin</span><span class="sxs-lookup"><span data-stu-id="8c5f4-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="8c5f4-105">Bilinen sorunlar:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-105">Known issues:</span></span>

- <span data-ttu-id="8c5f4-106">Uyarıyı Kapatma için Azure Stack sürümü 1803 gereklidir</span><span class="sxs-lookup"><span data-stu-id="8c5f4-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="8c5f4-107">Bazı Depolama cmdlet’leri için Azure Stack sürümü 1804 gereklidir</span><span class="sxs-lookup"><span data-stu-id="8c5f4-107">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="8c5f4-108">New-AzsOffer komutu genel durumlu bir teklif oluşturmaya izin vermez.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="8c5f4-109">Durumu değiştirmek için Set-AzsOffer cmdlet’inin sonradan çağrılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="8c5f4-110">IP Havuzu, yeniden dağıtma olmadan kaldırılamaz</span><span class="sxs-lookup"><span data-stu-id="8c5f4-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="8c5f4-111">Hataya Neden Olan Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="8c5f4-111">Breaking Changes</span></span>
<span data-ttu-id="8c5f4-112">1.2.11’den geçirilen tüm hataya neden olan değişiklikler burada https://aka.ms/azspowershellmigration belgelenmiştir</span><span class="sxs-lookup"><span data-stu-id="8c5f4-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="8c5f4-113">Yükleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-113">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="8c5f4-114">İçerik:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-114">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="8c5f4-115">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="8c5f4-115">Azure Bridge</span></span>
<span data-ttu-id="8c5f4-116">Resimleri Azure’dan genel olarak dağıtmaya olanak tanıyan Azure Stack AzureBridge yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-116">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="8c5f4-117">Backup</span><span class="sxs-lookup"><span data-stu-id="8c5f4-117">Backup</span></span>
<span data-ttu-id="8c5f4-118">Yöneticilerin şunları yapmasını sağlayan Yedekleme yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-118">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="8c5f4-119">Yedeklemelerin nerede depolandığını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8c5f4-119">Configure where backups are stored</span></span>
- <span data-ttu-id="8c5f4-120">yedekleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-120">Perform backups</span></span>
- <span data-ttu-id="8c5f4-121">Tamamlanan yedeklemeyi listeleme ve geri yükleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-121">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="8c5f4-122">Ticaret</span><span class="sxs-lookup"><span data-stu-id="8c5f4-122">Commerce</span></span>
<span data-ttu-id="8c5f4-123">Azure Stack sisteminde toplu veri kullanımını görüntülemenin bir yolunu sağlayan Azure Stack Ticaret yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-123">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="8c5f4-124">İşlem</span><span class="sxs-lookup"><span data-stu-id="8c5f4-124">Compute</span></span>
<span data-ttu-id="8c5f4-125">Kota işleme, platform resimleri ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-125">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="8c5f4-126">Fabric</span><span class="sxs-lookup"><span data-stu-id="8c5f4-126">Fabric</span></span>
<span data-ttu-id="8c5f4-127">Yöneticilerin altyapı bileşenlerini görüntülemesine ve yönetmesine olanak tanıyan Azure Stack Fabric yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-127">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="8c5f4-128">Ölçek birimi düğümlerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="8c5f4-128">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="8c5f4-129">FRU ilişkili etkinlikler için ölçek birimi düğümlerinin Boşaltılması ve Sürdürülmesi</span><span class="sxs-lookup"><span data-stu-id="8c5f4-129">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="8c5f4-130">Ölçek birimi düğümlerinin onarımı</span><span class="sxs-lookup"><span data-stu-id="8c5f4-130">Repair of scale unit nodes</span></span>
- <span data-ttu-id="8c5f4-131">Altyapı rolünün yeniden başlatılması</span><span class="sxs-lookup"><span data-stu-id="8c5f4-131">Restart of Infrastructure role</span></span>
- <span data-ttu-id="8c5f4-132">Altyapı rolü örneklerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="8c5f4-132">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="8c5f4-133">Yeni IP Havuzları oluşturma</span><span class="sxs-lookup"><span data-stu-id="8c5f4-133">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="8c5f4-134">Galeri</span><span class="sxs-lookup"><span data-stu-id="8c5f4-134">Gallery</span></span>
<span data-ttu-id="8c5f4-135">Azure Stack marketinde galeri öğelerini yönetme işlevini sunan Azure Stack Galeri yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-135">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="8c5f4-136">Altyapı Öngörüleri</span><span class="sxs-lookup"><span data-stu-id="8c5f4-136">Infrastructure Insights</span></span>
<span data-ttu-id="8c5f4-137">Yöneticilere şunları yapmasını sağlayan Infrastructure Insights yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-137">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="8c5f4-138">Azure Stack damga kaynaklarının sistem durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-138">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="8c5f4-139">Uyarıları görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-139">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="8c5f4-140">KeyVault</span><span class="sxs-lookup"><span data-stu-id="8c5f4-140">KeyVault</span></span>
<span data-ttu-id="8c5f4-141">Yöneticinin KeyVault kotalarını görüntülemesine oplanak tanıyan Azure Stack KeyVault yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-141">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="8c5f4-142">Ağ</span><span class="sxs-lookup"><span data-stu-id="8c5f4-142">Network</span></span>
<span data-ttu-id="8c5f4-143">Şunlara olanak tanıyan Ağ yöneticisi modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-143">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="8c5f4-144">Ağ kotalarının yönetimi</span><span class="sxs-lookup"><span data-stu-id="8c5f4-144">Management of network quotas</span></span>
- <span data-ttu-id="8c5f4-145">Genel IP adresleri, sanal ağlar, yük dengeleyicileri gibi ayrılan ağ kaynaklarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-145">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="8c5f4-146">Yönetici genel bakışı gösteren bir cmdlet sunar</span><span class="sxs-lookup"><span data-stu-id="8c5f4-146">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="8c5f4-147">Depolama</span><span class="sxs-lookup"><span data-stu-id="8c5f4-147">Storage</span></span>
<span data-ttu-id="8c5f4-148">Azure Stack Depolama yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-148">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="8c5f4-149">Bu sürümde şunların yapılmasını sağlayan işlevleri sunuyoruz:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-149">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="8c5f4-150">Depolama kotalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-150">Manage storage quotas</span></span>
- <span data-ttu-id="8c5f4-151">Silinen depolama kaynaklarına yönelik atık toplama</span><span class="sxs-lookup"><span data-stu-id="8c5f4-151">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="8c5f4-152">Silinen depolama hesaplarını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-152">Restore deleted storage accounts</span></span>
- <span data-ttu-id="8c5f4-153">Kapsayıcıları bir paydan diğerine geçirme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-153">Migrate containers from one share to another</span></span>
- <span data-ttu-id="8c5f4-154">Bireysel depolama bileşenleri hakkında bilgileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-154">View information about the individual storage components</span></span>
- <span data-ttu-id="8c5f4-155">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-155">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="8c5f4-156">Abonelik Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="8c5f4-156">Subscription Admin</span></span>
<span data-ttu-id="8c5f4-157">Azure Stack Aboneliği yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-157">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="8c5f4-158">Bu modül yöneticilerin şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-158">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="8c5f4-159">Plan ve teklifleri yönetme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-159">Manage plans and offers</span></span>
- <span data-ttu-id="8c5f4-160">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-160">View usage and performance information</span></span>
- <span data-ttu-id="8c5f4-161">RBAC’yi yönetme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-161">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="8c5f4-162">Abonelik</span><span class="sxs-lookup"><span data-stu-id="8c5f4-162">Subscription</span></span>
<span data-ttu-id="8c5f4-163">Azure Stack Aboneliği modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-163">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="8c5f4-164">Bu modül kullanıcıların şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-164">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="8c5f4-165">Abonelikleri Oluşturma, Silme ve Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-165">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="8c5f4-166">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-166">Update</span></span>
<span data-ttu-id="8c5f4-167">Azure Stack Güncelleştirme yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-167">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="8c5f4-168">Bu modülde yöneticiler şunları yapabilir:</span><span class="sxs-lookup"><span data-stu-id="8c5f4-168">In this module administrators can:</span></span>
- <span data-ttu-id="8c5f4-169">Kullanılabilir güncelleştirmeleri listeleme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-169">List and install available updates</span></span>
- <span data-ttu-id="8c5f4-170">Kesintiye uğrayan güncelleştirmeleri sürdürme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-170">Resume interrupted updates</span></span>
- <span data-ttu-id="8c5f4-171">Yüklü güncelleştirmeleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8c5f4-171">View installed updates</span></span>
