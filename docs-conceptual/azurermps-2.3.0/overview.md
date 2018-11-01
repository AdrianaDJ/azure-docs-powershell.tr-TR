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
ms.openlocfilehash: d514e43d82bcb51f65831dc506e58e8747db0381
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2018
ms.locfileid: "50737331"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="08c35-103">AzureRM Modülü 2.3.0</span><span class="sxs-lookup"><span data-stu-id="08c35-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="08c35-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="08c35-104">Requirements:</span></span>
<span data-ttu-id="08c35-105">Desteklenen en düşük Azure Stack sürümü 1808 sürümüdür.</span><span class="sxs-lookup"><span data-stu-id="08c35-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="08c35-106">Not: Daha önceki bir sürümü kullanıyorsanız sürüm 1.2.11’i yükleyin</span><span class="sxs-lookup"><span data-stu-id="08c35-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="08c35-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="08c35-107">Install</span></span>
```powershell
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

##<a name="release-notes"></a><span data-ttu-id="08c35-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="08c35-108">Release Notes</span></span>
* <span data-ttu-id="08c35-109">2.3.0 sürümünde birçok hataya neden olan değişiklik bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="08c35-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="08c35-110">1.2.11 sürümünden yükseltmek için https://aka.ms/azspowershellmigration sayfasındaki geçiş kılavuzuna bakabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="08c35-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="08c35-111">Bu sürüm özel Azure Stack API profili 2018-03-01-hybrid sürümüne karşılık gelmektedir</span><span class="sxs-lookup"><span data-stu-id="08c35-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="08c35-112">Tüm modüller AzureRm.Profile modülü bağımlılığı için daha büyük veya eşit hale geldi.</span><span class="sxs-lookup"><span data-stu-id="08c35-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="08c35-113">Modüller tarafından desteklenen API sürümleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="08c35-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="08c35-114">İşlem - 30.03.2017</span><span class="sxs-lookup"><span data-stu-id="08c35-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="08c35-115">Ağ - 01.10.2017</span><span class="sxs-lookup"><span data-stu-id="08c35-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="08c35-116">Depolama - 01.01.2016</span><span class="sxs-lookup"><span data-stu-id="08c35-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="08c35-117">Kaynaklar - 01.02.2018</span><span class="sxs-lookup"><span data-stu-id="08c35-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="08c35-118">Anahtar Kasası - 01.10.2016</span><span class="sxs-lookup"><span data-stu-id="08c35-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="08c35-119">DNS - 01.04.2016</span><span class="sxs-lookup"><span data-stu-id="08c35-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="08c35-120">Bu kaynak türlerinin her biri için tam kapsamlı API sürümü eşlemesi için bkz. https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="08c35-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="08c35-121">İçerik:</span><span class="sxs-lookup"><span data-stu-id="08c35-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="08c35-122">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="08c35-122">Azure Bridge</span></span>
<span data-ttu-id="08c35-123">Resimleri Azure’dan genel olarak dağıtmaya olanak tanıyan Azure Stack AzureBridge yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="08c35-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="08c35-124">Backup</span><span class="sxs-lookup"><span data-stu-id="08c35-124">Backup</span></span>
<span data-ttu-id="08c35-125">Yöneticilerin şunları yapmasını sağlayan Yedekleme yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="08c35-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="08c35-126">Yedeklemelerin nerede depolandığını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="08c35-126">Configure where backups are stored</span></span>
- <span data-ttu-id="08c35-127">yedekleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="08c35-127">Perform backups</span></span>
- <span data-ttu-id="08c35-128">Tamamlanan yedeklemeyi listeleme ve geri yükleme</span><span class="sxs-lookup"><span data-stu-id="08c35-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="08c35-129">Ticaret</span><span class="sxs-lookup"><span data-stu-id="08c35-129">Commerce</span></span>
<span data-ttu-id="08c35-130">Azure Stack sisteminde toplu veri kullanımını görüntülemenin bir yolunu sağlayan Azure Stack Ticaret yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="08c35-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="08c35-131">İşlem</span><span class="sxs-lookup"><span data-stu-id="08c35-131">Compute</span></span>
<span data-ttu-id="08c35-132">Kota işleme, platform görüntüleri, yönetilen diskler ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="08c35-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="08c35-133">Fabric</span><span class="sxs-lookup"><span data-stu-id="08c35-133">Fabric</span></span>
<span data-ttu-id="08c35-134">Yöneticilerin altyapı bileşenlerini görüntülemesine ve yönetmesine olanak tanıyan Azure Stack Fabric yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="08c35-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="08c35-135">Ölçek birimi düğümlerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="08c35-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="08c35-136">FRU ilişkili etkinlikler için ölçek birimi düğümlerinin Boşaltılması ve Sürdürülmesi</span><span class="sxs-lookup"><span data-stu-id="08c35-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="08c35-137">Ölçek birimi düğümlerinin onarımı</span><span class="sxs-lookup"><span data-stu-id="08c35-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="08c35-138">Altyapı rolünün yeniden başlatılması</span><span class="sxs-lookup"><span data-stu-id="08c35-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="08c35-139">Altyapı rolü örneklerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="08c35-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="08c35-140">Yeni IP Havuzları oluşturma</span><span class="sxs-lookup"><span data-stu-id="08c35-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="08c35-141">Galeri</span><span class="sxs-lookup"><span data-stu-id="08c35-141">Gallery</span></span>
<span data-ttu-id="08c35-142">Azure Stack marketinde galeri öğelerini yönetme işlevini sunan Azure Stack Galeri yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="08c35-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="08c35-143">Altyapı Öngörüleri</span><span class="sxs-lookup"><span data-stu-id="08c35-143">Infrastructure Insights</span></span>
<span data-ttu-id="08c35-144">Yöneticilere şunları yapmasını sağlayan Infrastructure Insights yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="08c35-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="08c35-145">Azure Stack damga kaynaklarının sistem durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="08c35-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="08c35-146">Uyarıları görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="08c35-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="08c35-147">KeyVault</span><span class="sxs-lookup"><span data-stu-id="08c35-147">KeyVault</span></span>
<span data-ttu-id="08c35-148">Yöneticinin KeyVault kotalarını görüntülemesine oplanak tanıyan Azure Stack KeyVault yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="08c35-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="08c35-149">Ağ</span><span class="sxs-lookup"><span data-stu-id="08c35-149">Network</span></span>
<span data-ttu-id="08c35-150">Şunlara olanak tanıyan Ağ yöneticisi modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="08c35-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="08c35-151">Ağ kotalarının yönetimi</span><span class="sxs-lookup"><span data-stu-id="08c35-151">Management of network quotas</span></span>
- <span data-ttu-id="08c35-152">Genel IP adresleri, sanal ağlar, yük dengeleyicileri gibi ayrılan ağ kaynaklarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="08c35-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="08c35-153">Yönetici genel bakışı gösteren bir cmdlet sunar</span><span class="sxs-lookup"><span data-stu-id="08c35-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="08c35-154">Depolama</span><span class="sxs-lookup"><span data-stu-id="08c35-154">Storage</span></span>
<span data-ttu-id="08c35-155">Azure Stack Depolama yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="08c35-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="08c35-156">Bu sürümde şunların yapılmasını sağlayan işlevleri sunuyoruz:</span><span class="sxs-lookup"><span data-stu-id="08c35-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="08c35-157">Depolama kotalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="08c35-157">Manage storage quotas</span></span>
- <span data-ttu-id="08c35-158">Silinen depolama kaynaklarına yönelik atık toplama</span><span class="sxs-lookup"><span data-stu-id="08c35-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="08c35-159">Silinen depolama hesaplarını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="08c35-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="08c35-160">Kapsayıcıları bir paydan diğerine geçirme</span><span class="sxs-lookup"><span data-stu-id="08c35-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="08c35-161">Bireysel depolama bileşenleri hakkında bilgileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="08c35-161">View information about the individual storage components</span></span>
- <span data-ttu-id="08c35-162">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="08c35-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="08c35-163">Abonelik Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="08c35-163">Subscription Admin</span></span>
<span data-ttu-id="08c35-164">Azure Stack Aboneliği yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="08c35-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="08c35-165">Bu modül yöneticilerin şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="08c35-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="08c35-166">Plan ve teklifleri yönetme</span><span class="sxs-lookup"><span data-stu-id="08c35-166">Manage plans and offers</span></span>
- <span data-ttu-id="08c35-167">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="08c35-167">View usage and performance information</span></span>
- <span data-ttu-id="08c35-168">RBAC’yi yönetme</span><span class="sxs-lookup"><span data-stu-id="08c35-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="08c35-169">Abonelik</span><span class="sxs-lookup"><span data-stu-id="08c35-169">Subscription</span></span>
<span data-ttu-id="08c35-170">Azure Stack Aboneliği modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="08c35-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="08c35-171">Bu modül kullanıcıların şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="08c35-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="08c35-172">Abonelikleri Oluşturma, Silme ve Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="08c35-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="08c35-173">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="08c35-173">Update</span></span>
<span data-ttu-id="08c35-174">Azure Stack Güncelleştirme yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="08c35-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="08c35-175">Bu modülde yöneticiler şunları yapabilir:</span><span class="sxs-lookup"><span data-stu-id="08c35-175">In this module administrators can:</span></span>
- <span data-ttu-id="08c35-176">Kullanılabilir güncelleştirmeleri listeleme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="08c35-176">List and install available updates</span></span>
- <span data-ttu-id="08c35-177">Kesintiye uğrayan güncelleştirmeleri sürdürme</span><span class="sxs-lookup"><span data-stu-id="08c35-177">Resume interrupted updates</span></span>
- <span data-ttu-id="08c35-178">Yüklü güncelleştirmeleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="08c35-178">View installed updates</span></span>
