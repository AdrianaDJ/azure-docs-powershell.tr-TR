---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 1ab1690d3c5fccca2994abc4958f3cf7e6a4e52d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93750844"
---
# <span data-ttu-id="26428-101">Az. Storagesehd modülü</span><span class="sxs-lookup"><span data-stu-id="26428-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="26428-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="26428-102">Description</span></span>
<span data-ttu-id="26428-103">Depolama eşitleme modülündeki cmdlet 'ler, PowerShell 'de Azure dosya eşitlemesi ile ilgili işlemleri yönetmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="26428-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="26428-104">Az. Storagesehd cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="26428-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="26428-105">Get-Azstoragesynccloudenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="26428-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="26428-106">Bu komut, verilen eşitleme grubundaki tüm bulut uç noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="26428-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="26428-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="26428-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="26428-108">Bu komut, belirli bir depolama eşitleme hizmeti içindeki tüm eşitleme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="26428-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="26428-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="26428-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="26428-110">Bu komut, belirli bir depolama Eşitleme hizmetine kaydedilen tüm sunucuları listeler.</span><span class="sxs-lookup"><span data-stu-id="26428-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="26428-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="26428-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="26428-112">Bu komut, belirli bir eşitleme grubundaki tüm sunucu uç noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="26428-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="26428-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="26428-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="26428-114">Bu komut, belirli bir abonelik/kaynak grubu kapsamındaki tüm depolama eşitleme hizmetlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="26428-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="26428-115">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="26428-115">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="26428-116">Sisteminiz ile Azure dosya eşitlemesi arasındaki olası uyumluluk sorunlarını denetler.</span><span class="sxs-lookup"><span data-stu-id="26428-116">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="26428-117">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="26428-117">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="26428-118">Bu komut tüm katmanlı dosyaları yerel diske geri çeker.</span><span class="sxs-lookup"><span data-stu-id="26428-118">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="26428-119">Yeni-Azstoragesynccloudenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="26428-119">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="26428-120">Bu komut, eşitleme grubunda bir Azure dosya eşitlemesi bulut uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26428-120">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="26428-121">Yeni-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="26428-121">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="26428-122">Bu komut, belirtilen bir depolama eşitleme hizmeti içinde yeni bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26428-122">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="26428-123">Yeni-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="26428-123">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="26428-124">Bu komut, kaydedilmiş bir sunucuda yeni bir sunucu uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26428-124">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="26428-125">Bu, sunucudaki belirtilen yolun eşitleme grubundaki diğer uç noktalarla birlikte dosyaları eşitlemeye başlamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="26428-125">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="26428-126">Yeni-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="26428-126">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="26428-127">Bu komut, kaynak grubunda yeni bir depolama eşitleme hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="26428-127">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="26428-128">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="26428-128">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="26428-129">Bu komut, bir sunucuyu güven ilişkisi oluşturan bir depolama Eşitleme hizmetine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="26428-129">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="26428-130">PowerShell veya Azure portalı bu sunucuda eşitleme yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="26428-130">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="26428-131">Remove-Azstoragesynccloudenvseçpoint</span><span class="sxs-lookup"><span data-stu-id="26428-131">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="26428-132">Bu komut, belirtilen bulut uç noktasını bir eşitleme grubundan siler.</span><span class="sxs-lookup"><span data-stu-id="26428-132">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="26428-133">En az bir bulut uç noktası olmadan, bu eşitleme grubunda başka sunucu uç noktaları eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="26428-133">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="26428-134">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="26428-134">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="26428-135">Bu komut, belirtilen eşitleme grubunu silecek.</span><span class="sxs-lookup"><span data-stu-id="26428-135">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="26428-136">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="26428-136">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="26428-137">Bu komut belirtilen sunucu uç noktasını silecek.</span><span class="sxs-lookup"><span data-stu-id="26428-137">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="26428-138">Bu konuma eşitleme hemen durdurulur.</span><span class="sxs-lookup"><span data-stu-id="26428-138">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="26428-139">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="26428-139">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="26428-140">Bu komut, belirtilen depolama eşitleme hizmeti 'ni silecek.</span><span class="sxs-lookup"><span data-stu-id="26428-140">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="26428-141">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="26428-141">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="26428-142">Yalnızca sorun giderme için kullanın.</span><span class="sxs-lookup"><span data-stu-id="26428-142">Use for troubleshooting only.</span></span> <span data-ttu-id="26428-143">Bu komut, sunucu kimliğini depolama Eşitleme hizmetine açıklamak için kullanılan depolama eşitleme sunucusu sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="26428-143">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="26428-144">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="26428-144">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="26428-145">Bu komut, sunucu uç noktasının ayarlanabilir parametrelerinde değişiklik yapılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="26428-145">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="26428-146">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="26428-146">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="26428-147">Uyarı: sunucunun kaydı silindiğinde, bu sunucudaki tüm sunucu uç noktaları art arda silinir.</span><span class="sxs-lookup"><span data-stu-id="26428-147">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="26428-148">Bu komut, bir sunucunun depolama eşitleme hizmetinden kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26428-148">This command will unregister a server from it's storage sync service.</span></span>