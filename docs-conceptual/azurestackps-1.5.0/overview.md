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
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275325"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="ab7c2-103">Azure Stack Modülü 1.5.0</span><span class="sxs-lookup"><span data-stu-id="ab7c2-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="ab7c2-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-104">Requirements:</span></span>
<span data-ttu-id="ab7c2-105">Desteklenen en düşük Azure Stack sürümü 1808 sürümüdür.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="ab7c2-106">Not: Daha önceki bir sürümü kullanıyorsanız 1.4.0 sürümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="ab7c2-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="ab7c2-107">Bilinen sorunlar:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-107">Known issues:</span></span>

- <span data-ttu-id="ab7c2-108">New-AzsOffer komutu genel durumlu bir teklif oluşturmaya izin vermez.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="ab7c2-109">Durumu değiştirmek için Set-AzsOffer cmdlet’inin sonradan çağrılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="ab7c2-110">IP Havuzu, yeniden dağıtma olmadan kaldırılamaz</span><span class="sxs-lookup"><span data-stu-id="ab7c2-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="ab7c2-111">Yükleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-111">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="ab7c2-112">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="ab7c2-112">Release Notes</span></span>
* <span data-ttu-id="ab7c2-113">Tüm Azure Stack Yönetici modülleri AzureRm.Profile modülü bağımlılığı için daha büyük veya eşit olacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="ab7c2-114">Tüm modüllere iç içe yerleştirilmiş kaynak adlarını işleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="ab7c2-115">Tüm modüllerde ErrorActionPreference değerinin durdurulacak şekilde geçersiz kılındığı hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="ab7c2-116">Azs.Compute.Admin modülü</span><span class="sxs-lookup"><span data-stu-id="ab7c2-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="ab7c2-117">Yönetilen diskleri desteklemek için yeni kota özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="ab7c2-118">Disk geçişiyle ilgili cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="ab7c2-119">Platform Görüntüsü ve VM uzantısı nesnelerine ek özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="ab7c2-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="ab7c2-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="ab7c2-121">Ölçek birimi düğümü eklemek için yeni cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab7c2-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="ab7c2-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="ab7c2-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="ab7c2-123">Set-AzsBackupShare artık Set-AzsBackupConfiguration cmdlet'inin diğer adı</span><span class="sxs-lookup"><span data-stu-id="ab7c2-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="ab7c2-124">Get-AzsBackupLocation artık Get-AzsBackupConfiguration cmdlet'inin diğer adı</span><span class="sxs-lookup"><span data-stu-id="ab7c2-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="ab7c2-125">Set-AzsBackupConfiguration için BackupShare parametresi artık parametre yolunun diğer adı</span><span class="sxs-lookup"><span data-stu-id="ab7c2-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="ab7c2-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="ab7c2-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="ab7c2-127">Get-AzsDelegatedProviderOffer için OfferName parametresi artık Offer parametresinin diğer adı</span><span class="sxs-lookup"><span data-stu-id="ab7c2-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="ab7c2-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="ab7c2-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="ab7c2-129">Get-AzsDelegatedProviderOffer için OfferName parametresi artık Offer parametresinin diğer adı</span><span class="sxs-lookup"><span data-stu-id="ab7c2-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="ab7c2-130">İçerik:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="ab7c2-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="ab7c2-131">Azure Bridge</span></span>
<span data-ttu-id="ab7c2-132">Resimleri Azure’dan genel olarak dağıtmaya olanak tanıyan Azure Stack AzureBridge yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="ab7c2-133">Backup</span><span class="sxs-lookup"><span data-stu-id="ab7c2-133">Backup</span></span>
<span data-ttu-id="ab7c2-134">Yöneticilerin şunları yapmasını sağlayan Yedekleme yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="ab7c2-135">Yedeklemelerin nerede depolandığını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ab7c2-135">Configure where backups are stored</span></span>
- <span data-ttu-id="ab7c2-136">yedekleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-136">Perform backups</span></span>
- <span data-ttu-id="ab7c2-137">Tamamlanan yedeklemeyi listeleme ve geri yükleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="ab7c2-138">Ticaret</span><span class="sxs-lookup"><span data-stu-id="ab7c2-138">Commerce</span></span>
<span data-ttu-id="ab7c2-139">Azure Stack sisteminde toplu veri kullanımını görüntülemenin bir yolunu sağlayan Azure Stack Ticaret yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="ab7c2-140">İşlem</span><span class="sxs-lookup"><span data-stu-id="ab7c2-140">Compute</span></span>
<span data-ttu-id="ab7c2-141">Kota işleme, platform görüntüleri, yönetilen diskler ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="ab7c2-142">Fabric</span><span class="sxs-lookup"><span data-stu-id="ab7c2-142">Fabric</span></span>
<span data-ttu-id="ab7c2-143">Yöneticilerin altyapı bileşenlerini görüntülemesine ve yönetmesine olanak tanıyan Azure Stack Fabric yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="ab7c2-144">Ölçek birimi düğümlerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="ab7c2-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="ab7c2-145">FRU ilişkili etkinlikler için ölçek birimi düğümlerinin Boşaltılması ve Sürdürülmesi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="ab7c2-146">Ölçek birimi düğümlerinin onarımı</span><span class="sxs-lookup"><span data-stu-id="ab7c2-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="ab7c2-147">Altyapı rolünün yeniden başlatılması</span><span class="sxs-lookup"><span data-stu-id="ab7c2-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="ab7c2-148">Altyapı rolü örneklerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="ab7c2-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="ab7c2-149">Yeni IP Havuzları oluşturma</span><span class="sxs-lookup"><span data-stu-id="ab7c2-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="ab7c2-150">Galeri</span><span class="sxs-lookup"><span data-stu-id="ab7c2-150">Gallery</span></span>
<span data-ttu-id="ab7c2-151">Azure Stack marketinde galeri öğelerini yönetme işlevini sunan Azure Stack Galeri yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="ab7c2-152">Altyapı Öngörüleri</span><span class="sxs-lookup"><span data-stu-id="ab7c2-152">Infrastructure Insights</span></span>
<span data-ttu-id="ab7c2-153">Yöneticilere şunları yapmasını sağlayan Infrastructure Insights yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="ab7c2-154">Azure Stack damga kaynaklarının sistem durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="ab7c2-155">Uyarıları görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="ab7c2-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab7c2-156">KeyVault</span></span>
<span data-ttu-id="ab7c2-157">Yöneticinin KeyVault kotalarını görüntülemesine oplanak tanıyan Azure Stack KeyVault yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="ab7c2-158">Ağ</span><span class="sxs-lookup"><span data-stu-id="ab7c2-158">Network</span></span>
<span data-ttu-id="ab7c2-159">Şunlara olanak tanıyan Ağ yöneticisi modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="ab7c2-160">Ağ kotalarının yönetimi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-160">Management of network quotas</span></span>
- <span data-ttu-id="ab7c2-161">Genel IP adresleri, sanal ağlar, yük dengeleyicileri gibi ayrılan ağ kaynaklarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="ab7c2-162">Yönetici genel bakışı gösteren bir cmdlet sunar</span><span class="sxs-lookup"><span data-stu-id="ab7c2-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="ab7c2-163">Depolama</span><span class="sxs-lookup"><span data-stu-id="ab7c2-163">Storage</span></span>
<span data-ttu-id="ab7c2-164">Azure Stack Depolama yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="ab7c2-165">Bu sürümde şunların yapılmasını sağlayan işlevleri sunuyoruz:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="ab7c2-166">Depolama kotalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-166">Manage storage quotas</span></span>
- <span data-ttu-id="ab7c2-167">Silinen depolama kaynaklarına yönelik atık toplama</span><span class="sxs-lookup"><span data-stu-id="ab7c2-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="ab7c2-168">Silinen depolama hesaplarını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="ab7c2-169">Kapsayıcıları bir paydan diğerine geçirme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="ab7c2-170">Bireysel depolama bileşenleri hakkında bilgileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-170">View information about the individual storage components</span></span>
- <span data-ttu-id="ab7c2-171">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="ab7c2-172">Abonelik Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="ab7c2-172">Subscription Admin</span></span>
<span data-ttu-id="ab7c2-173">Azure Stack Aboneliği yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="ab7c2-174">Bu modül yöneticilerin şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="ab7c2-175">Plan ve teklifleri yönetme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-175">Manage plans and offers</span></span>
- <span data-ttu-id="ab7c2-176">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-176">View usage and performance information</span></span>
- <span data-ttu-id="ab7c2-177">RBAC’yi yönetme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="ab7c2-178">Abonelik</span><span class="sxs-lookup"><span data-stu-id="ab7c2-178">Subscription</span></span>
<span data-ttu-id="ab7c2-179">Azure Stack Aboneliği modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="ab7c2-180">Bu modül kullanıcıların şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="ab7c2-181">Abonelikleri Oluşturma, Silme ve Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="ab7c2-182">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-182">Update</span></span>
<span data-ttu-id="ab7c2-183">Azure Stack Güncelleştirme yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="ab7c2-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="ab7c2-184">Bu modülde yöneticiler şunları yapabilir:</span><span class="sxs-lookup"><span data-stu-id="ab7c2-184">In this module administrators can:</span></span>
- <span data-ttu-id="ab7c2-185">Kullanılabilir güncelleştirmeleri listeleme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-185">List and install available updates</span></span>
- <span data-ttu-id="ab7c2-186">Kesintiye uğrayan güncelleştirmeleri sürdürme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-186">Resume interrupted updates</span></span>
- <span data-ttu-id="ab7c2-187">Yüklü güncelleştirmeleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ab7c2-187">View installed updates</span></span>
