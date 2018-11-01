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
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2018
ms.locfileid: "50738521"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="40fc8-103">Azure Stack Modülü 1.3.0</span><span class="sxs-lookup"><span data-stu-id="40fc8-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="40fc8-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="40fc8-104">Requirements:</span></span>
<span data-ttu-id="40fc8-105">Desteklenen en düşük Azure Stack sürümü 1804’tür.</span><span class="sxs-lookup"><span data-stu-id="40fc8-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="40fc8-106">Not: Daha önceki bir sürümü kullanıyorsanız sürüm 1.2.11’i yükleyin</span><span class="sxs-lookup"><span data-stu-id="40fc8-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="40fc8-107">Bilinen sorunlar:</span><span class="sxs-lookup"><span data-stu-id="40fc8-107">Known issues:</span></span>

- <span data-ttu-id="40fc8-108">Uyarıyı Kapatma için Azure Stack sürümü 1803 gereklidir</span><span class="sxs-lookup"><span data-stu-id="40fc8-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="40fc8-109">Bazı Depolama cmdlet’leri için Azure Stack sürümü 1804 gereklidir</span><span class="sxs-lookup"><span data-stu-id="40fc8-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="40fc8-110">New-AzsOffer komutu genel durumlu bir teklif oluşturmaya izin vermez.</span><span class="sxs-lookup"><span data-stu-id="40fc8-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="40fc8-111">Durumu değiştirmek için Set-AzsOffer cmdlet’inin sonradan çağrılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="40fc8-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="40fc8-112">IP Havuzu, yeniden dağıtma olmadan kaldırılamaz</span><span class="sxs-lookup"><span data-stu-id="40fc8-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="40fc8-113">Hataya Neden Olan Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="40fc8-113">Breaking Changes</span></span>
<span data-ttu-id="40fc8-114">1.2.11’den geçirilen tüm hataya neden olan değişiklikler burada https://aka.ms/azspowershellmigration belgelenmiştir</span><span class="sxs-lookup"><span data-stu-id="40fc8-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="40fc8-115">Yükleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-115">Install</span></span>
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
## <a name="content"></a><span data-ttu-id="40fc8-116">İçerik:</span><span class="sxs-lookup"><span data-stu-id="40fc8-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="40fc8-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="40fc8-117">Azure Bridge</span></span>
<span data-ttu-id="40fc8-118">Resimleri Azure’dan genel olarak dağıtmaya olanak tanıyan Azure Stack AzureBridge yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="40fc8-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="40fc8-119">Backup</span><span class="sxs-lookup"><span data-stu-id="40fc8-119">Backup</span></span>
<span data-ttu-id="40fc8-120">Yöneticilerin şunları yapmasını sağlayan Yedekleme yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="40fc8-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="40fc8-121">Yedeklemelerin nerede depolandığını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="40fc8-121">Configure where backups are stored</span></span>
- <span data-ttu-id="40fc8-122">yedekleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="40fc8-122">Perform backups</span></span>
- <span data-ttu-id="40fc8-123">Tamamlanan yedeklemeyi listeleme ve geri yükleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="40fc8-124">Ticaret</span><span class="sxs-lookup"><span data-stu-id="40fc8-124">Commerce</span></span>
<span data-ttu-id="40fc8-125">Azure Stack sisteminde toplu veri kullanımını görüntülemenin bir yolunu sağlayan Azure Stack Ticaret yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="40fc8-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="40fc8-126">İşlem</span><span class="sxs-lookup"><span data-stu-id="40fc8-126">Compute</span></span>
<span data-ttu-id="40fc8-127">Kota işleme, platform resimleri ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="40fc8-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="40fc8-128">Fabric</span><span class="sxs-lookup"><span data-stu-id="40fc8-128">Fabric</span></span>
<span data-ttu-id="40fc8-129">Yöneticilerin altyapı bileşenlerini görüntülemesine ve yönetmesine olanak tanıyan Azure Stack Fabric yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="40fc8-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="40fc8-130">Ölçek birimi düğümlerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="40fc8-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="40fc8-131">FRU ilişkili etkinlikler için ölçek birimi düğümlerinin Boşaltılması ve Sürdürülmesi</span><span class="sxs-lookup"><span data-stu-id="40fc8-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="40fc8-132">Ölçek birimi düğümlerinin onarımı</span><span class="sxs-lookup"><span data-stu-id="40fc8-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="40fc8-133">Altyapı rolünün yeniden başlatılması</span><span class="sxs-lookup"><span data-stu-id="40fc8-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="40fc8-134">Altyapı rolü örneklerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="40fc8-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="40fc8-135">Yeni IP Havuzları oluşturma</span><span class="sxs-lookup"><span data-stu-id="40fc8-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="40fc8-136">Galeri</span><span class="sxs-lookup"><span data-stu-id="40fc8-136">Gallery</span></span>
<span data-ttu-id="40fc8-137">Azure Stack marketinde galeri öğelerini yönetme işlevini sunan Azure Stack Galeri yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="40fc8-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="40fc8-138">Altyapı Öngörüleri</span><span class="sxs-lookup"><span data-stu-id="40fc8-138">Infrastructure Insights</span></span>
<span data-ttu-id="40fc8-139">Yöneticilere şunları yapmasını sağlayan Infrastructure Insights yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="40fc8-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="40fc8-140">Azure Stack damga kaynaklarının sistem durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="40fc8-141">Uyarıları görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="40fc8-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="40fc8-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="40fc8-142">KeyVault</span></span>
<span data-ttu-id="40fc8-143">Yöneticinin KeyVault kotalarını görüntülemesine oplanak tanıyan Azure Stack KeyVault yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="40fc8-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="40fc8-144">Ağ</span><span class="sxs-lookup"><span data-stu-id="40fc8-144">Network</span></span>
<span data-ttu-id="40fc8-145">Şunlara olanak tanıyan Ağ yöneticisi modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="40fc8-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="40fc8-146">Ağ kotalarının yönetimi</span><span class="sxs-lookup"><span data-stu-id="40fc8-146">Management of network quotas</span></span>
- <span data-ttu-id="40fc8-147">Genel IP adresleri, sanal ağlar, yük dengeleyicileri gibi ayrılan ağ kaynaklarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="40fc8-148">Yönetici genel bakışı gösteren bir cmdlet sunar</span><span class="sxs-lookup"><span data-stu-id="40fc8-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="40fc8-149">Depolama</span><span class="sxs-lookup"><span data-stu-id="40fc8-149">Storage</span></span>
<span data-ttu-id="40fc8-150">Azure Stack Depolama yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="40fc8-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="40fc8-151">Bu sürümde şunların yapılmasını sağlayan işlevleri sunuyoruz:</span><span class="sxs-lookup"><span data-stu-id="40fc8-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="40fc8-152">Depolama kotalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="40fc8-152">Manage storage quotas</span></span>
- <span data-ttu-id="40fc8-153">Silinen depolama kaynaklarına yönelik atık toplama</span><span class="sxs-lookup"><span data-stu-id="40fc8-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="40fc8-154">Silinen depolama hesaplarını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="40fc8-155">Kapsayıcıları bir paydan diğerine geçirme</span><span class="sxs-lookup"><span data-stu-id="40fc8-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="40fc8-156">Bireysel depolama bileşenleri hakkında bilgileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-156">View information about the individual storage components</span></span>
- <span data-ttu-id="40fc8-157">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="40fc8-158">Abonelik Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="40fc8-158">Subscription Admin</span></span>
<span data-ttu-id="40fc8-159">Azure Stack Aboneliği yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="40fc8-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="40fc8-160">Bu modül yöneticilerin şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="40fc8-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="40fc8-161">Plan ve teklifleri yönetme</span><span class="sxs-lookup"><span data-stu-id="40fc8-161">Manage plans and offers</span></span>
- <span data-ttu-id="40fc8-162">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-162">View usage and performance information</span></span>
- <span data-ttu-id="40fc8-163">RBAC’yi yönetme</span><span class="sxs-lookup"><span data-stu-id="40fc8-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="40fc8-164">Abonelik</span><span class="sxs-lookup"><span data-stu-id="40fc8-164">Subscription</span></span>
<span data-ttu-id="40fc8-165">Azure Stack Aboneliği modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="40fc8-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="40fc8-166">Bu modül kullanıcıların şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="40fc8-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="40fc8-167">Abonelikleri Oluşturma, Silme ve Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="40fc8-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="40fc8-168">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="40fc8-168">Update</span></span>
<span data-ttu-id="40fc8-169">Azure Stack Güncelleştirme yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="40fc8-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="40fc8-170">Bu modülde yöneticiler şunları yapabilir:</span><span class="sxs-lookup"><span data-stu-id="40fc8-170">In this module administrators can:</span></span>
- <span data-ttu-id="40fc8-171">Kullanılabilir güncelleştirmeleri listeleme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-171">List and install available updates</span></span>
- <span data-ttu-id="40fc8-172">Kesintiye uğrayan güncelleştirmeleri sürdürme</span><span class="sxs-lookup"><span data-stu-id="40fc8-172">Resume interrupted updates</span></span>
- <span data-ttu-id="40fc8-173">Yüklü güncelleştirmeleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="40fc8-173">View installed updates</span></span>
