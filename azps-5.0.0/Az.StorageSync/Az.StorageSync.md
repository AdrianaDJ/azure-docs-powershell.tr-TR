---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324973"
---
# <span data-ttu-id="b605f-101">Az. Storagesehd modülü</span><span class="sxs-lookup"><span data-stu-id="b605f-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="b605f-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="b605f-102">Description</span></span>
<span data-ttu-id="b605f-103">Depolama eşitleme modülündeki cmdlet 'ler, PowerShell 'de Azure dosya eşitlemesi ile ilgili işlemleri yönetmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="b605f-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="b605f-104">Az. Storagesehd cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b605f-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="b605f-105">Get-Azstoragesynccloudenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="b605f-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="b605f-106">Bu komut, verilen eşitleme grubundaki tüm bulut uç noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b605f-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="b605f-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b605f-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="b605f-108">Bu komut, belirli bir depolama eşitleme hizmeti içindeki tüm eşitleme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b605f-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="b605f-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b605f-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="b605f-110">Bu komut, belirli bir depolama Eşitleme hizmetine kaydedilen tüm sunucuları listeler.</span><span class="sxs-lookup"><span data-stu-id="b605f-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="b605f-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b605f-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="b605f-112">Bu komut, belirli bir eşitleme grubundaki tüm sunucu uç noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b605f-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="b605f-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b605f-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="b605f-114">Bu komut, belirli bir abonelik/kaynak grubu kapsamındaki tüm depolama eşitleme hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="b605f-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="b605f-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="b605f-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="b605f-116">Bu komut, ad alanları değişikliklerinin algılanmasını el ile başlatmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b605f-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="b605f-117">Tüm paylaşım, alt klasör veya dosya kümesini hedeflenebilir.</span><span class="sxs-lookup"><span data-stu-id="b605f-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="b605f-118">Maksimum 10.000 değişiklik algılanabilir.</span><span class="sxs-lookup"><span data-stu-id="b605f-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="b605f-119">Değişiklik kapsamı sizin için biliniyorsa, bu komutun yürütülmesini ad alanının bölümleriyle sınırlandırın, böylece algılamanın hızla ve 10.000 değişiklik sınırının içinde tamamlanabilmesi için</span><span class="sxs-lookup"><span data-stu-id="b605f-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="b605f-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="b605f-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="b605f-121">Sisteminiz ile Azure dosya eşitlemesi arasındaki olası uyumluluk sorunlarını denetler.</span><span class="sxs-lookup"><span data-stu-id="b605f-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="b605f-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="b605f-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="b605f-123">Bu komut tüm katmanlı dosyaları yerel diske geri çeker.</span><span class="sxs-lookup"><span data-stu-id="b605f-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="b605f-124">Yeni-Azstoragesynccloudenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="b605f-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="b605f-125">Bu komut, eşitleme grubunda bir Azure dosya eşitlemesi bulut uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b605f-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="b605f-126">Yeni-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b605f-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="b605f-127">Bu komut, belirtilen bir depolama eşitleme hizmeti içinde yeni bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b605f-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="b605f-128">Yeni-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b605f-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="b605f-129">Bu komut, kaydedilmiş bir sunucuda yeni bir sunucu uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b605f-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="b605f-130">Bu, sunucudaki belirtilen yolun eşitleme grubundaki diğer uç noktalarla birlikte dosyaları eşitlemeye başlamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="b605f-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="b605f-131">Yeni-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b605f-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="b605f-132">Bu komut, kaynak grubunda yeni bir depolama eşitleme hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b605f-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="b605f-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b605f-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="b605f-134">Bu komut, kaynak grubunda bir depolama eşitleme hizmeti ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b605f-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="b605f-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b605f-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="b605f-136">Bu komut, bir sunucuyu güven ilişkisi oluşturan bir depolama Eşitleme hizmetine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b605f-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="b605f-137">PowerShell veya Azure portalı bu sunucuda eşitleme yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b605f-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="b605f-138">Remove-Azstoragesynccloudenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="b605f-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="b605f-139">Bu komut, belirtilen bulut uç noktasını bir eşitleme grubundan siler.</span><span class="sxs-lookup"><span data-stu-id="b605f-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="b605f-140">En az bir bulut uç noktası olmadan, bu eşitleme grubunda başka sunucu uç noktaları eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="b605f-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="b605f-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b605f-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="b605f-142">Bu komut, belirtilen eşitleme grubunu silecek.</span><span class="sxs-lookup"><span data-stu-id="b605f-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="b605f-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b605f-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="b605f-144">Bu komut belirtilen sunucu uç noktasını silecek.</span><span class="sxs-lookup"><span data-stu-id="b605f-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="b605f-145">Bu konuma eşitleme hemen durdurulur.</span><span class="sxs-lookup"><span data-stu-id="b605f-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="b605f-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b605f-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="b605f-147">Bu komut, belirtilen depolama eşitleme hizmeti 'ni silecek.</span><span class="sxs-lookup"><span data-stu-id="b605f-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="b605f-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="b605f-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="b605f-149">Yalnızca sorun giderme için kullanın.</span><span class="sxs-lookup"><span data-stu-id="b605f-149">Use for troubleshooting only.</span></span> <span data-ttu-id="b605f-150">Bu komut, sunucu kimliğini depolama Eşitleme hizmetine açıklamak için kullanılan depolama eşitleme sunucusu sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="b605f-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="b605f-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b605f-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="b605f-152">Bu komut, sunucu uç noktasının ayarlanabilir parametrelerinde değişiklik yapılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b605f-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="b605f-153">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b605f-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="b605f-154">Uyarı: sunucunun kaydı silindiğinde, bu sunucudaki tüm sunucu uç noktaları art arda silinir.</span><span class="sxs-lookup"><span data-stu-id="b605f-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="b605f-155">Bu komut, bir sunucunun depolama eşitleme hizmetinden kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b605f-155">This command will unregister a server from it's storage sync service.</span></span>

