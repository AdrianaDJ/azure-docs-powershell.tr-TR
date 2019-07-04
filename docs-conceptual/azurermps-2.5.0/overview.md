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
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038202"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="d7999-103">AzureRM 2.5.0 Modulü</span><span class="sxs-lookup"><span data-stu-id="d7999-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="d7999-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="d7999-104">Requirements:</span></span>
<span data-ttu-id="d7999-105">Desteklenen en düşük Azure Stack sürümü 1904'dir.</span><span class="sxs-lookup"><span data-stu-id="d7999-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="d7999-106">Not: Daha önceki bir sürümü kullanıyorsanız 1.2.11 sürümünü yükleyin</span><span class="sxs-lookup"><span data-stu-id="d7999-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="d7999-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="d7999-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="d7999-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="d7999-108">Release Notes</span></span>
* <span data-ttu-id="d7999-109">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d7999-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="d7999-110">2019-03-01-hybrid profiliyle 2018-05-01- api sürümünü destekleyen yeni Resources modülü</span><span class="sxs-lookup"><span data-stu-id="d7999-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="d7999-111">PolicyDefinition(2016-12-01) ve PolicyAssisgment(2017-06-01-preview) işlemleri halen eski api sürümlerine sahiptir</span><span class="sxs-lookup"><span data-stu-id="d7999-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="d7999-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="d7999-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="d7999-113">2017-12-01 API sürümünü destekleyen yeni işlem modülü.’</span><span class="sxs-lookup"><span data-stu-id="d7999-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="d7999-114">Bu sürüm özel Azure Stack API profili 2019-03-01-hybrid sürümüne karşılık gelmektedir</span><span class="sxs-lookup"><span data-stu-id="d7999-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="d7999-115">Tüm modüller AzureRm.Profile modülü bağımlılığı için daha büyük veya eşit hale geldi.</span><span class="sxs-lookup"><span data-stu-id="d7999-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="d7999-116">Modüller tarafından desteklenen API sürümleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="d7999-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="d7999-117">İşlem - 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="d7999-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="d7999-118">Ağ - 01.10.2017</span><span class="sxs-lookup"><span data-stu-id="d7999-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="d7999-119">Depolama - 01.01.2016</span><span class="sxs-lookup"><span data-stu-id="d7999-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="d7999-120">Kaynaklar - 01.02.2018</span><span class="sxs-lookup"><span data-stu-id="d7999-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="d7999-121">Anahtar Kasası - 01.10.2016</span><span class="sxs-lookup"><span data-stu-id="d7999-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="d7999-122">DNS - 01.04.2016</span><span class="sxs-lookup"><span data-stu-id="d7999-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="d7999-123">Bu kaynak türlerinin her biri için tam kapsamlı API sürümü eşlemesi için bkz. https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="d7999-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="d7999-124">İçerik:</span><span class="sxs-lookup"><span data-stu-id="d7999-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="d7999-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="d7999-125">Azure Bridge</span></span>
<span data-ttu-id="d7999-126">Resimleri Azure’dan genel olarak dağıtmaya olanak tanıyan Azure Stack AzureBridge yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d7999-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="d7999-127">Backup</span><span class="sxs-lookup"><span data-stu-id="d7999-127">Backup</span></span>
<span data-ttu-id="d7999-128">Yöneticilerin şunları yapmasını sağlayan Yedekleme yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="d7999-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="d7999-129">Yedeklemelerin nerede depolandığını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d7999-129">Configure where backups are stored</span></span>
- <span data-ttu-id="d7999-130">yedekleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="d7999-130">Perform backups</span></span>
- <span data-ttu-id="d7999-131">Tamamlanan yedeklemeyi listeleme ve geri yükleme</span><span class="sxs-lookup"><span data-stu-id="d7999-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="d7999-132">Ticaret</span><span class="sxs-lookup"><span data-stu-id="d7999-132">Commerce</span></span>
<span data-ttu-id="d7999-133">Azure Stack sisteminde toplu veri kullanımını görüntülemenin bir yolunu sağlayan Azure Stack Ticaret yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d7999-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="d7999-134">İşlem</span><span class="sxs-lookup"><span data-stu-id="d7999-134">Compute</span></span>
<span data-ttu-id="d7999-135">Kota işleme, platform görüntüleri, yönetilen diskler ve sanal makine eklentilerini yönetme işlevini sunan Azure Stack İşlem yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d7999-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="d7999-136">Fabric</span><span class="sxs-lookup"><span data-stu-id="d7999-136">Fabric</span></span>
<span data-ttu-id="d7999-137">Yöneticilerin altyapı bileşenlerini görüntülemesine ve yönetmesine olanak tanıyan Azure Stack Fabric yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="d7999-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="d7999-138">Ölçek birimi düğümlerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="d7999-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="d7999-139">FRU ilişkili etkinlikler için ölçek birimi düğümlerinin Boşaltılması ve Sürdürülmesi</span><span class="sxs-lookup"><span data-stu-id="d7999-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="d7999-140">Ölçek birimi düğümlerinin onarımı</span><span class="sxs-lookup"><span data-stu-id="d7999-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="d7999-141">Altyapı rolünün yeniden başlatılması</span><span class="sxs-lookup"><span data-stu-id="d7999-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="d7999-142">Altyapı rolü örneklerinin Durdurulması, Başlatılması ve Kapatılması</span><span class="sxs-lookup"><span data-stu-id="d7999-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="d7999-143">Yeni IP Havuzları oluşturma</span><span class="sxs-lookup"><span data-stu-id="d7999-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="d7999-144">Galeri</span><span class="sxs-lookup"><span data-stu-id="d7999-144">Gallery</span></span>
<span data-ttu-id="d7999-145">Azure Stack marketinde galeri öğelerini yönetme işlevini sunan Azure Stack Galeri yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d7999-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="d7999-146">Altyapı Öngörüleri</span><span class="sxs-lookup"><span data-stu-id="d7999-146">Infrastructure Insights</span></span>
<span data-ttu-id="d7999-147">Yöneticilere şunları yapmasını sağlayan Infrastructure Insights yönetici modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="d7999-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="d7999-148">Azure Stack damga kaynaklarının sistem durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d7999-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="d7999-149">Uyarıları görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="d7999-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="d7999-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d7999-150">KeyVault</span></span>
<span data-ttu-id="d7999-151">Yöneticinin KeyVault kotalarını görüntülemesine oplanak tanıyan Azure Stack KeyVault yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d7999-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="d7999-152">Ağ</span><span class="sxs-lookup"><span data-stu-id="d7999-152">Network</span></span>
<span data-ttu-id="d7999-153">Şunlara olanak tanıyan Ağ yöneticisi modülünün önizleme sürümü:</span><span class="sxs-lookup"><span data-stu-id="d7999-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="d7999-154">Ağ kotalarının yönetimi</span><span class="sxs-lookup"><span data-stu-id="d7999-154">Management of network quotas</span></span>
- <span data-ttu-id="d7999-155">Genel IP adresleri, sanal ağlar, yük dengeleyicileri gibi ayrılan ağ kaynaklarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d7999-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="d7999-156">Yönetici genel bakışı gösteren bir cmdlet sunar</span><span class="sxs-lookup"><span data-stu-id="d7999-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="d7999-157">Depolama</span><span class="sxs-lookup"><span data-stu-id="d7999-157">Storage</span></span>
<span data-ttu-id="d7999-158">Azure Stack Depolama yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d7999-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="d7999-159">Bu sürümde şunların yapılmasını sağlayan işlevleri sunuyoruz:</span><span class="sxs-lookup"><span data-stu-id="d7999-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="d7999-160">Depolama kotalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="d7999-160">Manage storage quotas</span></span>
- <span data-ttu-id="d7999-161">Silinen depolama kaynaklarına yönelik atık toplama</span><span class="sxs-lookup"><span data-stu-id="d7999-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="d7999-162">Silinen depolama hesaplarını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="d7999-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="d7999-163">Kapsayıcıları bir paydan diğerine geçirme</span><span class="sxs-lookup"><span data-stu-id="d7999-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="d7999-164">Bireysel depolama bileşenleri hakkında bilgileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d7999-164">View information about the individual storage components</span></span>
- <span data-ttu-id="d7999-165">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d7999-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="d7999-166">Abonelik Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="d7999-166">Subscription Admin</span></span>
<span data-ttu-id="d7999-167">Azure Stack Aboneliği yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d7999-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="d7999-168">Bu modül yöneticilerin şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="d7999-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="d7999-169">Plan ve teklifleri yönetme</span><span class="sxs-lookup"><span data-stu-id="d7999-169">Manage plans and offers</span></span>
- <span data-ttu-id="d7999-170">Kullanım ve performans bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d7999-170">View usage and performance information</span></span>
- <span data-ttu-id="d7999-171">RBAC’yi yönetme</span><span class="sxs-lookup"><span data-stu-id="d7999-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="d7999-172">Abonelik</span><span class="sxs-lookup"><span data-stu-id="d7999-172">Subscription</span></span>
<span data-ttu-id="d7999-173">Azure Stack Aboneliği modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d7999-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="d7999-174">Bu modül kullanıcıların şunları yapmasını sağlayan işlevler sunar:</span><span class="sxs-lookup"><span data-stu-id="d7999-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="d7999-175">Abonelikleri Oluşturma, Silme ve Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d7999-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="d7999-176">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d7999-176">Update</span></span>
<span data-ttu-id="d7999-177">Azure Stack Güncelleştirme yönetici modülünün önizleme sürümü.</span><span class="sxs-lookup"><span data-stu-id="d7999-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="d7999-178">Bu modülde yöneticiler şunları yapabilir:</span><span class="sxs-lookup"><span data-stu-id="d7999-178">In this module administrators can:</span></span>
- <span data-ttu-id="d7999-179">Kullanılabilir güncelleştirmeleri listeleme ve yükleme</span><span class="sxs-lookup"><span data-stu-id="d7999-179">List and install available updates</span></span>
- <span data-ttu-id="d7999-180">Kesintiye uğrayan güncelleştirmeleri sürdürme</span><span class="sxs-lookup"><span data-stu-id="d7999-180">Resume interrupted updates</span></span>
- <span data-ttu-id="d7999-181">Yüklü güncelleştirmeleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="d7999-181">View installed updates</span></span>
