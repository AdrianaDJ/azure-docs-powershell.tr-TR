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
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4b72bbd1bda93767251e0ba3d488f798575d9115
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244322"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="b50b7-103">AzureRM 2.5.0 Modulü</span><span class="sxs-lookup"><span data-stu-id="b50b7-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="b50b7-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="b50b7-104">Requirements:</span></span>
<span data-ttu-id="b50b7-105">Desteklenen en düşük Azure Stack sürümü 1904'dir.</span><span class="sxs-lookup"><span data-stu-id="b50b7-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="b50b7-106">Not: Daha önceki bir sürümü kullanıyorsanız sürüm 1.2.11’i yükleyin</span><span class="sxs-lookup"><span data-stu-id="b50b7-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="b50b7-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="b50b7-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="b50b7-108">Release Notes</span></span>
* <span data-ttu-id="b50b7-109">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b50b7-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="b50b7-110">2019-03-01-hybrid profiliyle 2018-05-01- api sürümünü destekleyen yeni Resources modülü</span><span class="sxs-lookup"><span data-stu-id="b50b7-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="b50b7-111">PolicyDefinition(2016-12-01) ve PolicyAssisgment(2017-06-01-preview) işlemleri halen eski api sürümlerine sahiptir</span><span class="sxs-lookup"><span data-stu-id="b50b7-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="b50b7-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="b50b7-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="b50b7-113">2017-12-01 API sürümünü destekleyen yeni işlem modülü.’</span><span class="sxs-lookup"><span data-stu-id="b50b7-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="b50b7-114">Bu sürüm özel Azure Stack API profili 2019-03-01-hybrid sürümüne karşılık gelmektedir</span><span class="sxs-lookup"><span data-stu-id="b50b7-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="b50b7-115">Tüm modüller AzureRm.Profile modülü bağımlılığı için daha büyük veya eşit hale geldi.</span><span class="sxs-lookup"><span data-stu-id="b50b7-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="b50b7-116">Modüller tarafından desteklenen API sürümleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="b50b7-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="b50b7-117">İşlem - 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="b50b7-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="b50b7-118">Ağ - 01.10.2017</span><span class="sxs-lookup"><span data-stu-id="b50b7-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="b50b7-119">Depolama - 01.01.2016</span><span class="sxs-lookup"><span data-stu-id="b50b7-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="b50b7-120">Kaynaklar - 01.02.2018</span><span class="sxs-lookup"><span data-stu-id="b50b7-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="b50b7-121">Anahtar Kasası - 01.10.2016</span><span class="sxs-lookup"><span data-stu-id="b50b7-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="b50b7-122">DNS - 01.04.2016</span><span class="sxs-lookup"><span data-stu-id="b50b7-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="b50b7-123">Bu kaynak türlerinin her biri için tam kapsamlı API sürümü eşlemesi için bkz. https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="b50b7-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="b50b7-124">İçerik:</span><span class="sxs-lookup"><span data-stu-id="b50b7-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="b50b7-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="b50b7-125">Azure Bridge</span></span>
<span data-ttu-id="b50b7-126">Resimleri Azure’dan genel olarak dağıtmaya olanak tanıyan Azure Stack AzureBridge yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="b50b7-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="b50b7-127">Backup</span><span class="sxs-lookup"><span data-stu-id="b50b7-127">Backup</span></span>
<span data-ttu-id="b50b7-128">Yöneticilerin şunları yapmasını sağlayan Yedekleme yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="b50b7-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="b50b7-129">Yedeklemelerin nerede depolandığını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b50b7-129">Configure where backups are stored</span></span>
- <span data-ttu-id="b50b7-130">yedekleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="b50b7-130">Perform backups</span></span>
- <span data-ttu-id="b50b7-131">Tamamlanan yedeklemeyi listeleme ve geri yükleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="b50b7-132">Ticaret</span><span class="sxs-lookup"><span data-stu-id="b50b7-132">Commerce</span></span>
<span data-ttu-id="b50b7-133">Azure Stack sisteminde toplu veri kullanımını görüntülemenin bir yolunu sağlayan Azure Stack Ticaret yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="b50b7-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="b50b7-134">İşlem</span><span class="sxs-lookup"><span data-stu-id="b50b7-134">Compute</span></span>
<span data-ttu-id="b50b7-135">Kota işleme, platform görüntüleri, yönetilen diskler ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="b50b7-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="b50b7-136">Fabric</span><span class="sxs-lookup"><span data-stu-id="b50b7-136">Fabric</span></span>
<span data-ttu-id="b50b7-137">Yöneticilerin altyapı bileşenlerini görüntülemesine ve yönetmesine olanak tanıyan Azure Stack Fabric yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="b50b7-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="b50b7-138">Ölçek birimi düğümlerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="b50b7-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="b50b7-139">FRU ilişkili etkinlikler için ölçek birimi düğümlerinin Boşaltılması ve Sürdürülmesi</span><span class="sxs-lookup"><span data-stu-id="b50b7-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="b50b7-140">Ölçek birimi düğümlerinin onarımı</span><span class="sxs-lookup"><span data-stu-id="b50b7-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="b50b7-141">Altyapı rolünün yeniden başlatılması</span><span class="sxs-lookup"><span data-stu-id="b50b7-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="b50b7-142">Altyapı rolü örneklerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="b50b7-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="b50b7-143">Yeni IP Havuzları oluşturma</span><span class="sxs-lookup"><span data-stu-id="b50b7-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="b50b7-144">Galeri</span><span class="sxs-lookup"><span data-stu-id="b50b7-144">Gallery</span></span>
<span data-ttu-id="b50b7-145">Azure Stack marketinde galeri öğelerini yönetme işlevini sunan Azure Stack Galeri yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="b50b7-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="b50b7-146">Altyapı Öngörüleri</span><span class="sxs-lookup"><span data-stu-id="b50b7-146">Infrastructure Insights</span></span>
<span data-ttu-id="b50b7-147">Yöneticilere şunları yapmasını sağlayan Infrastructure Insights yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="b50b7-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="b50b7-148">Azure Stack damga kaynaklarının sistem durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="b50b7-149">Uyarıları görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="b50b7-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="b50b7-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b50b7-150">KeyVault</span></span>
<span data-ttu-id="b50b7-151">Yöneticinin KeyVault kotalarını görüntülemesine oplanak tanıyan Azure Stack KeyVault yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="b50b7-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="b50b7-152">Ağ</span><span class="sxs-lookup"><span data-stu-id="b50b7-152">Network</span></span>
<span data-ttu-id="b50b7-153">Şunlara olanak tanıyan Ağ yöneticisi modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="b50b7-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="b50b7-154">Ağ kotalarının yönetimi</span><span class="sxs-lookup"><span data-stu-id="b50b7-154">Management of network quotas</span></span>
- <span data-ttu-id="b50b7-155">Genel IP adresleri, sanal ağlar, yük dengeleyicileri gibi ayrılan ağ kaynaklarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="b50b7-156">Yönetici genel bakışı gösteren bir cmdlet sunar</span><span class="sxs-lookup"><span data-stu-id="b50b7-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="b50b7-157">Depolama</span><span class="sxs-lookup"><span data-stu-id="b50b7-157">Storage</span></span>
<span data-ttu-id="b50b7-158">Azure Stack Depolama yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="b50b7-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="b50b7-159">Bu sürümde şunların yapılmasını sağlayan işlevleri sunuyoruz:</span><span class="sxs-lookup"><span data-stu-id="b50b7-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="b50b7-160">Depolama kotalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="b50b7-160">Manage storage quotas</span></span>
- <span data-ttu-id="b50b7-161">Silinen depolama kaynaklarına yönelik atık toplama</span><span class="sxs-lookup"><span data-stu-id="b50b7-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="b50b7-162">Silinen depolama hesaplarını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="b50b7-163">Kapsayıcıları bir paydan diğerine geçirme</span><span class="sxs-lookup"><span data-stu-id="b50b7-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="b50b7-164">Bireysel depolama bileşenleri hakkında bilgileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-164">View information about the individual storage components</span></span>
- <span data-ttu-id="b50b7-165">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="b50b7-166">Abonelik Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="b50b7-166">Subscription Admin</span></span>
<span data-ttu-id="b50b7-167">Azure Stack Aboneliği yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="b50b7-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="b50b7-168">Bu modül yöneticilerin şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="b50b7-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="b50b7-169">Plan ve teklifleri yönetme</span><span class="sxs-lookup"><span data-stu-id="b50b7-169">Manage plans and offers</span></span>
- <span data-ttu-id="b50b7-170">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-170">View usage and performance information</span></span>
- <span data-ttu-id="b50b7-171">RBAC’yi yönetme</span><span class="sxs-lookup"><span data-stu-id="b50b7-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="b50b7-172">Abonelik</span><span class="sxs-lookup"><span data-stu-id="b50b7-172">Subscription</span></span>
<span data-ttu-id="b50b7-173">Azure Stack Aboneliği modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="b50b7-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="b50b7-174">Bu modül kullanıcıların şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="b50b7-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="b50b7-175">Abonelikleri Oluşturma, Silme ve Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b50b7-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="b50b7-176">Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="b50b7-176">Update</span></span>
<span data-ttu-id="b50b7-177">Azure Stack Güncelleştirme yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="b50b7-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="b50b7-178">Bu modülde yöneticiler şunları yapabilir:</span><span class="sxs-lookup"><span data-stu-id="b50b7-178">In this module administrators can:</span></span>
- <span data-ttu-id="b50b7-179">Kullanılabilir güncelleştirmeleri listeleme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-179">List and install available updates</span></span>
- <span data-ttu-id="b50b7-180">Kesintiye uğrayan güncelleştirmeleri sürdürme</span><span class="sxs-lookup"><span data-stu-id="b50b7-180">Resume interrupted updates</span></span>
- <span data-ttu-id="b50b7-181">Yüklü güncelleştirmeleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b50b7-181">View installed updates</span></span>
