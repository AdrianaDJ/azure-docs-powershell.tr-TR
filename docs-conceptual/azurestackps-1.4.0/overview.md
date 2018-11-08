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
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211851"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="a510d-103">Azure Stack Modülü 1.4.0</span><span class="sxs-lookup"><span data-stu-id="a510d-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="a510d-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="a510d-104">Requirements:</span></span>
<span data-ttu-id="a510d-105">Desteklenen en düşük Azure Stack sürümü 1804’tür.</span><span class="sxs-lookup"><span data-stu-id="a510d-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="a510d-106">Not: Daha önceki bir sürümü kullanıyorsanız sürüm 1.2.11’i yükleyin</span><span class="sxs-lookup"><span data-stu-id="a510d-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="a510d-107">Bilinen sorunlar:</span><span class="sxs-lookup"><span data-stu-id="a510d-107">Known issues:</span></span>

- <span data-ttu-id="a510d-108">Uyarıyı Kapatma için Azure Stack sürümü 1803 gereklidir</span><span class="sxs-lookup"><span data-stu-id="a510d-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="a510d-109">New-AzsOffer komutu genel durumlu bir teklif oluşturmaya izin vermez.</span><span class="sxs-lookup"><span data-stu-id="a510d-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="a510d-110">Durumu değiştirmek için Set-AzsOffer cmdlet’inin sonradan çağrılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a510d-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="a510d-111">IP Havuzu, yeniden dağıtma olmadan kaldırılamaz</span><span class="sxs-lookup"><span data-stu-id="a510d-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="a510d-112">Hataya Neden Olan Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="a510d-112">Breaking Changes</span></span>
<span data-ttu-id="a510d-113">1.3.0 sürümünden sonra hataya neden olan değişiklik yapılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="a510d-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="a510d-114">1.2.11’den geçirilen tüm hataya neden olan değişiklikler burada https://aka.ms/azspowershellmigration belgelenmiştir</span><span class="sxs-lookup"><span data-stu-id="a510d-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="a510d-115">Yükleme</span><span class="sxs-lookup"><span data-stu-id="a510d-115">Install</span></span>
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
## <a name="release-notes"></a><span data-ttu-id="a510d-116">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="a510d-116">Release Notes</span></span>
    * <span data-ttu-id="a510d-117">Azurestack 1.4.0 sürümde, önceki 1.3.0 sürümüne göre hataya neden olan değişiklik yapılmamıştır</span><span class="sxs-lookup"><span data-stu-id="a510d-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="a510d-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="a510d-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="a510d-119">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a510d-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="a510d-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="a510d-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="a510d-121">Set-AzsBackupShare cmdlet’inde yeni BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="a510d-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="a510d-122">Şifreleme anahtarı oluşturmayı kolaylaştırmak için yeni bir New-EncyptionKeyBase64 cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="a510d-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="a510d-123">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a510d-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="a510d-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="a510d-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="a510d-125">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a510d-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="a510d-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="a510d-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="a510d-127">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a510d-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="a510d-128">Yöneticinin azurestack damgasına yeni ölçek birimleri ekleyebilmesi için yeni Add-AzsScaleUnitNode cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="a510d-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="a510d-129">Ölçek birimi parametre nesnelerinin oluşturulmasını kolaylaştırmak için cmdlet ve New-AzsScaleUnitNodeObject eklendi</span><span class="sxs-lookup"><span data-stu-id="a510d-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="a510d-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="a510d-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="a510d-131">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a510d-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="a510d-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="a510d-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="a510d-133">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a510d-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="a510d-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="a510d-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="a510d-135">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a510d-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="a510d-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="a510d-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="a510d-137">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a510d-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="a510d-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="a510d-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="a510d-139">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme</span><span class="sxs-lookup"><span data-stu-id="a510d-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="a510d-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="a510d-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="a510d-141">Abonelikleri temsilcili sağlayıcı teklifleri arasında taşıyabilmek için Move-AzsSubscription cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="a510d-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="a510d-142">Kullanıcı aboneliklerinin temsilcili sağlayıcı teklifleri arasında taşınabildiğini doğrulamak için Test-AzsMoveSubscription cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="a510d-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="a510d-143">Sayfalandırılmış sonuçlarda yalnızca bir sayfanın döndürülmesine neden olan hata için düzeltme'</span><span class="sxs-lookup"><span data-stu-id="a510d-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="a510d-144">İçerik:</span><span class="sxs-lookup"><span data-stu-id="a510d-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="a510d-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="a510d-145">Azure Bridge</span></span>
<span data-ttu-id="a510d-146">Resimleri Azure’dan genel olarak dağıtmaya olanak tanıyan Azure Stack AzureBridge yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="a510d-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="a510d-147">Backup</span><span class="sxs-lookup"><span data-stu-id="a510d-147">Backup</span></span>
<span data-ttu-id="a510d-148">Yöneticilerin şunları yapmasını sağlayan Yedekleme yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="a510d-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="a510d-149">Yedeklemelerin nerede depolandığını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a510d-149">Configure where backups are stored</span></span>
- <span data-ttu-id="a510d-150">yedekleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="a510d-150">Perform backups</span></span>
- <span data-ttu-id="a510d-151">Tamamlanan yedeklemeyi listeleme ve geri yükleme</span><span class="sxs-lookup"><span data-stu-id="a510d-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="a510d-152">Ticaret</span><span class="sxs-lookup"><span data-stu-id="a510d-152">Commerce</span></span>
<span data-ttu-id="a510d-153">Azure Stack sisteminde toplu veri kullanımını görüntülemenin bir yolunu sağlayan Azure Stack Ticaret yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="a510d-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="a510d-154">İşlem</span><span class="sxs-lookup"><span data-stu-id="a510d-154">Compute</span></span>
<span data-ttu-id="a510d-155">Kota işleme, platform resimleri ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="a510d-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="a510d-156">Fabric</span><span class="sxs-lookup"><span data-stu-id="a510d-156">Fabric</span></span>
<span data-ttu-id="a510d-157">Yöneticilerin altyapı bileşenlerini görüntülemesine ve yönetmesine olanak tanıyan Azure Stack Fabric yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="a510d-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="a510d-158">Ölçek birimi düğümlerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="a510d-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="a510d-159">FRU ilişkili etkinlikler için ölçek birimi düğümlerinin Boşaltılması ve Sürdürülmesi</span><span class="sxs-lookup"><span data-stu-id="a510d-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="a510d-160">Ölçek birimi düğümlerinin onarımı</span><span class="sxs-lookup"><span data-stu-id="a510d-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="a510d-161">Altyapı rolünün yeniden başlatılması</span><span class="sxs-lookup"><span data-stu-id="a510d-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="a510d-162">Altyapı rolü örneklerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="a510d-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="a510d-163">Yeni IP Havuzları oluşturma</span><span class="sxs-lookup"><span data-stu-id="a510d-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="a510d-164">Galeri</span><span class="sxs-lookup"><span data-stu-id="a510d-164">Gallery</span></span>
<span data-ttu-id="a510d-165">Azure Stack marketinde galeri öğelerini yönetme işlevini sunan Azure Stack Galeri yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="a510d-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="a510d-166">Altyapı Öngörüleri</span><span class="sxs-lookup"><span data-stu-id="a510d-166">Infrastructure Insights</span></span>
<span data-ttu-id="a510d-167">Yöneticilere şunları yapmasını sağlayan Infrastructure Insights yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="a510d-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="a510d-168">Azure Stack damga kaynaklarının sistem durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a510d-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="a510d-169">Uyarıları görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="a510d-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="a510d-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a510d-170">KeyVault</span></span>
<span data-ttu-id="a510d-171">Yöneticinin KeyVault kotalarını görüntülemesine oplanak tanıyan Azure Stack KeyVault yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="a510d-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="a510d-172">Ağ</span><span class="sxs-lookup"><span data-stu-id="a510d-172">Network</span></span>
<span data-ttu-id="a510d-173">Şunlara olanak tanıyan Ağ yöneticisi modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="a510d-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="a510d-174">Ağ kotalarının yönetimi</span><span class="sxs-lookup"><span data-stu-id="a510d-174">Management of network quotas</span></span>
- <span data-ttu-id="a510d-175">Genel IP adresleri, sanal ağlar, yük dengeleyicileri gibi ayrılan ağ kaynaklarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a510d-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="a510d-176">Yönetici genel bakışı gösteren bir cmdlet sunar</span><span class="sxs-lookup"><span data-stu-id="a510d-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="a510d-177">Depolama</span><span class="sxs-lookup"><span data-stu-id="a510d-177">Storage</span></span>
<span data-ttu-id="a510d-178">Azure Stack Depolama yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="a510d-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="a510d-179">Bu sürümde şunların yapılmasını sağlayan işlevleri sunuyoruz:</span><span class="sxs-lookup"><span data-stu-id="a510d-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="a510d-180">Depolama kotalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="a510d-180">Manage storage quotas</span></span>
- <span data-ttu-id="a510d-181">Silinen depolama kaynaklarına yönelik atık toplama</span><span class="sxs-lookup"><span data-stu-id="a510d-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="a510d-182">Silinen depolama hesaplarını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="a510d-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="a510d-183">Kapsayıcıları bir paydan diğerine geçirme</span><span class="sxs-lookup"><span data-stu-id="a510d-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="a510d-184">Bireysel depolama bileşenleri hakkında bilgileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a510d-184">View information about the individual storage components</span></span>
- <span data-ttu-id="a510d-185">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a510d-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="a510d-186">Abonelik Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="a510d-186">Subscription Admin</span></span>
<span data-ttu-id="a510d-187">Azure Stack Aboneliği yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="a510d-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="a510d-188">Bu modül yöneticilerin şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="a510d-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="a510d-189">Plan ve teklifleri yönetme</span><span class="sxs-lookup"><span data-stu-id="a510d-189">Manage plans and offers</span></span>
- <span data-ttu-id="a510d-190">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a510d-190">View usage and performance information</span></span>
- <span data-ttu-id="a510d-191">RBAC’yi yönetme</span><span class="sxs-lookup"><span data-stu-id="a510d-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="a510d-192">Abonelik</span><span class="sxs-lookup"><span data-stu-id="a510d-192">Subscription</span></span>
<span data-ttu-id="a510d-193">Azure Stack Aboneliği modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="a510d-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="a510d-194">Bu modül kullanıcıların şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="a510d-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="a510d-195">Abonelikleri Oluşturma, Silme ve Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a510d-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="a510d-196">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a510d-196">Update</span></span>
<span data-ttu-id="a510d-197">Azure Stack Güncelleştirme yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="a510d-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="a510d-198">Bu modülde yöneticiler şunları yapabilir:</span><span class="sxs-lookup"><span data-stu-id="a510d-198">In this module administrators can:</span></span>
- <span data-ttu-id="a510d-199">Kullanılabilir güncelleştirmeleri listeleme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="a510d-199">List and install available updates</span></span>
- <span data-ttu-id="a510d-200">Kesintiye uğrayan güncelleştirmeleri sürdürme</span><span class="sxs-lookup"><span data-stu-id="a510d-200">Resume interrupted updates</span></span>
- <span data-ttu-id="a510d-201">Yüklü güncelleştirmeleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a510d-201">View installed updates</span></span>
