---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 88e9c622ef3608b17e6cd8d4ce8c193812a97520
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/14/2020
ms.locfileid: "86382353"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="110a1-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="110a1-103">Azure PowerShell release notes</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="110a1-104">4.4.0 - Temmuz 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-104">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-105">Az.Accounts</span></span>
* <span data-ttu-id="110a1-106">“Invoke-AzRestMethod” adlı yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-106">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="110a1-107">“Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]</span><span class="sxs-lookup"><span data-stu-id="110a1-107">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="110a1-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="110a1-108">Az.Aks</span></span>
* <span data-ttu-id="110a1-109">“Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]</span><span class="sxs-lookup"><span data-stu-id="110a1-109">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="110a1-110">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="110a1-110">Az.AnalysisServices</span></span>
* <span data-ttu-id="110a1-111">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-111">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-112">Az.Automation</span></span>
* <span data-ttu-id="110a1-113">Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-113">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-114">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-114">Az.Compute</span></span>
* <span data-ttu-id="110a1-115">“En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-115">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-116">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-117">Data Factory’ye genel parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-117">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="110a1-118">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="110a1-118">Az.EventGrid</span></span>
* <span data-ttu-id="110a1-119">2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-119">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="110a1-120">Yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-120">Added new features:</span></span>
    - <span data-ttu-id="110a1-121">Giriş eşleme</span><span class="sxs-lookup"><span data-stu-id="110a1-121">Input mapping</span></span>
    - <span data-ttu-id="110a1-122">Olay Teslim Şeması</span><span class="sxs-lookup"><span data-stu-id="110a1-122">Event Delivery Schema</span></span>
    - <span data-ttu-id="110a1-123">Özel Bağlantı</span><span class="sxs-lookup"><span data-stu-id="110a1-123">Private Link</span></span>
    - <span data-ttu-id="110a1-124">Bulut Olayı V10 Şeması</span><span class="sxs-lookup"><span data-stu-id="110a1-124">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="110a1-125">Hedef Olarak Service Bus Konu Başlığı</span><span class="sxs-lookup"><span data-stu-id="110a1-125">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="110a1-126">Hedef Olarak Azure İşlevi</span><span class="sxs-lookup"><span data-stu-id="110a1-126">Azure Function As Destination</span></span>
    - <span data-ttu-id="110a1-127">Web Kancası Toplu İş</span><span class="sxs-lookup"><span data-stu-id="110a1-127">WebHook Batching</span></span>
    - <span data-ttu-id="110a1-128">Güvenli web kancası (AAD desteği)</span><span class="sxs-lookup"><span data-stu-id="110a1-128">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="110a1-129">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="110a1-129">IpFiltering</span></span>
* <span data-ttu-id="110a1-130">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-130">Updated cmdlets:</span></span>
    - <span data-ttu-id="110a1-131">“New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="110a1-131">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="110a1-132">Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-132">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="110a1-133">AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-133">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="110a1-134">Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-134">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="110a1-135">Teslim şeması için yeni, isteğe bağlı parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-135">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="110a1-136">“New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="110a1-136">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="110a1-137">IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-137">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="110a1-138">“New-AzEventGridTopic'/'New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="110a1-138">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="110a1-139">Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-139">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="110a1-140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="110a1-140">Az.FrontDoor</span></span>
* <span data-ttu-id="110a1-141">Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-141">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="110a1-142">Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-142">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="110a1-143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-143">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-144">Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-144">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-145">Az.Monitor</span></span>
* <span data-ttu-id="110a1-146">Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]</span><span class="sxs-lookup"><span data-stu-id="110a1-146">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-147">Az.Network</span></span>
* <span data-ttu-id="110a1-148">VWan HubVnet bağlantısında değişen parametreler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-148">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="110a1-149">Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-149">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="110a1-150">“Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="110a1-150">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="110a1-151">“New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="110a1-151">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="110a1-152">“Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="110a1-152">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="110a1-153">“Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="110a1-153">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="110a1-154">“New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="110a1-154">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="110a1-155">Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-155">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="110a1-156">“Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="110a1-156">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="110a1-157">“New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="110a1-157">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="110a1-158">“Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="110a1-158">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="110a1-159">“Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="110a1-159">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="110a1-160">“Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="110a1-160">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="110a1-161">“New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="110a1-161">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="110a1-162">Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-162">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="110a1-163">Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-163">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="110a1-164">Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-164">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-166">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-166">Removed project reference to Authentication</span></span>
* <span data-ttu-id="110a1-167">Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı</span><span class="sxs-lookup"><span data-stu-id="110a1-167">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="110a1-168">Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="110a1-168">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-169">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-169">Az.Resources</span></span>
* <span data-ttu-id="110a1-170">“Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-170">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="110a1-171">“Unregister-AzResourceProvider” cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-171">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-172">Az.Sql</span></span>
* <span data-ttu-id="110a1-173">“Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-173">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="110a1-174">Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-174">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="110a1-175">Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="110a1-175">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-176">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-176">Az.Storage</span></span>
* <span data-ttu-id="110a1-177">Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-177">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="110a1-178">MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-178">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="110a1-179">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="110a1-179">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="110a1-180">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="110a1-180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="110a1-181">Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-181">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="110a1-182">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="110a1-182">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="110a1-183">Blob sürümlerini içeren destek listesi blobları</span><span class="sxs-lookup"><span data-stu-id="110a1-183">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="110a1-184">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="110a1-184">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="110a1-185">Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-185">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="110a1-186">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="110a1-186">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="110a1-187">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="110a1-187">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="110a1-188">Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-188">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="110a1-189">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="110a1-189">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="110a1-190">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="110a1-190">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="110a1-191">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="110a1-191">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="110a1-192">“Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="110a1-192">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="110a1-193">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="110a1-193">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="110a1-194">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="110a1-194">Az.StorageSync</span></span>
* <span data-ttu-id="110a1-195">ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-195">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="110a1-196">“UpdateStorageSyncService” cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-196">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="110a1-197">“Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="110a1-197">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="110a1-198">StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-198">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-199">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-199">Az.Websites</span></span>
* <span data-ttu-id="110a1-200">App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-200">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="110a1-201">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-201">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-202">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-202">Az.Accounts</span></span>
* <span data-ttu-id="110a1-203">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-203">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="110a1-204">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="110a1-204">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="110a1-205">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-205">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="110a1-206">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="110a1-206">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="110a1-207">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="110a1-207">Az.Aks</span></span>
* <span data-ttu-id="110a1-208">Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-208">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="110a1-209">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="110a1-209">Az.Batch</span></span>
* <span data-ttu-id="110a1-210">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-210">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="110a1-211">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-211">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-212">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-212">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-213">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-213">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="110a1-214">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-214">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-215">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-215">Az.Compute</span></span>
* <span data-ttu-id="110a1-216">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-216">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="110a1-217">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-217">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="110a1-218">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="110a1-218">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="110a1-219">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-219">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="110a1-220">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-220">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-221">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-221">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-222">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-222">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="110a1-223">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="110a1-223">Az.EventHub</span></span>
* <span data-ttu-id="110a1-224">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-224">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="110a1-225">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="110a1-225">Az.Functions</span></span>
* <span data-ttu-id="110a1-226">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-226">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="110a1-227">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-227">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-228">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-228">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="110a1-229">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="110a1-229">Az.HealthcareApis</span></span>
* <span data-ttu-id="110a1-230">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-230">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="110a1-231">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-231">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-232">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-232">Az.Monitor</span></span>
* <span data-ttu-id="110a1-233">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-233">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="110a1-234">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="110a1-234">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-235">Az.Network</span></span>
* <span data-ttu-id="110a1-236">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-236">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="110a1-237">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-237">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="110a1-238">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="110a1-238">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="110a1-239">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-239">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="110a1-240">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-240">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="110a1-241">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="110a1-241">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="110a1-242">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="110a1-242">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="110a1-243">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="110a1-243">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="110a1-244">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="110a1-244">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="110a1-245">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="110a1-245">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="110a1-246">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-246">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="110a1-247">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-247">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="110a1-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="110a1-248">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="110a1-249">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="110a1-249">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="110a1-250">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-250">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="110a1-251">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-251">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="110a1-252">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-252">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="110a1-253">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-253">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="110a1-254">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-254">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="110a1-255">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="110a1-255">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="110a1-256">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-256">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="110a1-257">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-257">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="110a1-258">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-258">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="110a1-259">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-259">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="110a1-260">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-260">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="110a1-261">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-261">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="110a1-262">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="110a1-262">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="110a1-263">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-263">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="110a1-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-264">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="110a1-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-265">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="110a1-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-266">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="110a1-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-267">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="110a1-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-268">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="110a1-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-269">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="110a1-270">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-270">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="110a1-271">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="110a1-271">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="110a1-272">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="110a1-272">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="110a1-273">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="110a1-273">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="110a1-274">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="110a1-274">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="110a1-275">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="110a1-275">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="110a1-276">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-276">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="110a1-277">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="110a1-277">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="110a1-278">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="110a1-278">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="110a1-279">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="110a1-279">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="110a1-280">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="110a1-280">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="110a1-281">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="110a1-281">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="110a1-282">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="110a1-282">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="110a1-283">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="110a1-283">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="110a1-284">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="110a1-284">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-285">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-285">Az.OperationalInsights</span></span>
* <span data-ttu-id="110a1-286">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="110a1-286">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="110a1-287">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-287">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="110a1-288">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-288">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="110a1-289">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="110a1-289">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="110a1-290">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="110a1-290">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-291">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-291">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-292">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-292">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="110a1-293">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="110a1-293">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-294">Az.Resources</span></span>
* <span data-ttu-id="110a1-295">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="110a1-295">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="110a1-296">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="110a1-296">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="110a1-297">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-297">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="110a1-298">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-298">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="110a1-299">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-299">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="110a1-300">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-300">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-301">Az.Sql</span></span>
* <span data-ttu-id="110a1-302">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-302">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="110a1-303">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-303">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="110a1-304">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="110a1-304">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-305">Az.Storage</span></span>
* <span data-ttu-id="110a1-306">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-306">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="110a1-307">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="110a1-307">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="110a1-308">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="110a1-308">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-309">Az.Websites</span></span>
* <span data-ttu-id="110a1-310">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-310">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="110a1-311">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-311">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="110a1-312">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-312">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="110a1-313">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-313">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="110a1-314">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-314">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="110a1-315">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-315">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="110a1-316">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-316">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-317">Az.Accounts</span></span>
* <span data-ttu-id="110a1-318">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="110a1-318">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="110a1-319">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="110a1-319">Az.AnalysisServices</span></span>
* <span data-ttu-id="110a1-320">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-320">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="110a1-321">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-321">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-322">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-322">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="110a1-323">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="110a1-323">Az.Billing</span></span>
* <span data-ttu-id="110a1-324">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-324">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-325">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-325">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-326">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-326">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-327">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-327">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-328">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-328">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="110a1-329">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="110a1-329">Az.DataShare</span></span>
* <span data-ttu-id="110a1-330">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-330">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="110a1-331">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="110a1-331">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="110a1-332">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-332">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-333">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-333">Az.OperationalInsights</span></span>
* <span data-ttu-id="110a1-334">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-334">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="110a1-335">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-335">Added optional parameters to</span></span> 
    - <span data-ttu-id="110a1-336">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="110a1-336">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="110a1-337">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="110a1-337">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="110a1-338">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-338">Az.PolicyInsights</span></span>
* <span data-ttu-id="110a1-339">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-339">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="110a1-340">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="110a1-340">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="110a1-341">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-341">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="110a1-342">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="110a1-342">Az.PrivateDns</span></span>
* <span data-ttu-id="110a1-343">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-343">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-344">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-345">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-345">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="110a1-346">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-346">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-347">Az.Resources</span></span>
* <span data-ttu-id="110a1-348">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-348">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="110a1-349">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="110a1-349">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="110a1-350">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-350">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="110a1-351">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-351">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="110a1-352">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-352">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-353">Az.Sql</span></span>
* <span data-ttu-id="110a1-354">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-354">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="110a1-355">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-355">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="110a1-356">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-356">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-357">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-357">Az.Storage</span></span>
* <span data-ttu-id="110a1-358">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-358">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="110a1-359">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-359">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="110a1-360">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="110a1-360">Highlights since the last release</span></span>
* <span data-ttu-id="110a1-361">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="110a1-361">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="110a1-362">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-362">General availability of Az.Functions</span></span> 
* <span data-ttu-id="110a1-363">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="110a1-363">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-364">Az.Accounts</span></span>
* <span data-ttu-id="110a1-365">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-365">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="110a1-366">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="110a1-366">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="110a1-367">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="110a1-367">Az.Aks</span></span>
* <span data-ttu-id="110a1-368">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-368">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="110a1-369">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-369">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="110a1-370">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="110a1-370">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="110a1-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-371">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-372">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-372">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="110a1-373">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="110a1-373">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="110a1-374">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-374">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="110a1-375">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-375">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="110a1-376">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-376">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="110a1-377">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-377">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="110a1-378">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-378">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="110a1-379">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-379">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="110a1-380">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-380">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="110a1-381">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-381">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="110a1-382">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="110a1-382">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="110a1-383">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="110a1-383">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="110a1-384">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="110a1-384">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="110a1-385">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="110a1-385">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="110a1-386">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="110a1-386">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="110a1-387">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="110a1-387">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="110a1-388">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-388">Az.ApplicationInsights</span></span>
* <span data-ttu-id="110a1-389">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="110a1-389">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="110a1-390">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-390">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="110a1-391">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-391">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="110a1-392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="110a1-392">Az.Batch</span></span>
* <span data-ttu-id="110a1-393">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-393">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="110a1-394">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-394">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="110a1-395">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-395">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="110a1-396">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-396">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="110a1-397">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="110a1-397">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="110a1-398">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-398">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="110a1-399">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-399">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="110a1-400">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="110a1-400">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="110a1-401">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-401">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-402">Az.Compute</span></span>
* <span data-ttu-id="110a1-403">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-403">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="110a1-404">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-404">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="110a1-405">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="110a1-405">Breaking changes</span></span>
    - <span data-ttu-id="110a1-406">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-406">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="110a1-407">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-407">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="110a1-408">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-408">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="110a1-409">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-409">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="110a1-410">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-410">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="110a1-411">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-411">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="110a1-412">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-412">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-413">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-413">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-414">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-414">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="110a1-415">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="110a1-415">Az.FrontDoor</span></span>
* <span data-ttu-id="110a1-416">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-416">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="110a1-417">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-417">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="110a1-418">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-418">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="110a1-419">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-419">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="110a1-420">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="110a1-420">Az.Functions</span></span>
* <span data-ttu-id="110a1-421">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-421">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="110a1-422">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-422">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-423">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="110a1-423">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="110a1-424">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="110a1-424">Az.HealthcareApis</span></span>
* <span data-ttu-id="110a1-425">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="110a1-425">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-426">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-426">Az.IotHub</span></span>
* <span data-ttu-id="110a1-427">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-427">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="110a1-428">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="110a1-428">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="110a1-429">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-429">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="110a1-430">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-430">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="110a1-431">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="110a1-431">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="110a1-432">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-432">New cmdlets are:</span></span>
    - <span data-ttu-id="110a1-433">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="110a1-433">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="110a1-434">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="110a1-434">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="110a1-435">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="110a1-435">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="110a1-436">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="110a1-436">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="110a1-437">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-437">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="110a1-438">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-438">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-439">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-440">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="110a1-440">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="110a1-441">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-441">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="110a1-442">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="110a1-442">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="110a1-443">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-443">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="110a1-444">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="110a1-444">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="110a1-445">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="110a1-445">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="110a1-446">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-446">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-447">Az.Monitor</span></span>
* <span data-ttu-id="110a1-448">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="110a1-448">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="110a1-449">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-449">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="110a1-450">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-450">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="110a1-451">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="110a1-451">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="110a1-452">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="110a1-452">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="110a1-453">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="110a1-453">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="110a1-454">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-454">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-455">Az.Network</span></span>
* <span data-ttu-id="110a1-456">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-456">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="110a1-457">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="110a1-457">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="110a1-458">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="110a1-458">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="110a1-459">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="110a1-459">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="110a1-460">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-460">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="110a1-461">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-461">New cmdlets added:</span></span>
        - <span data-ttu-id="110a1-462">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="110a1-462">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="110a1-463">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="110a1-463">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="110a1-464">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="110a1-464">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="110a1-465">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="110a1-465">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="110a1-466">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-466">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="110a1-467">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-467">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="110a1-468">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-468">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="110a1-469">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="110a1-469">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="110a1-470">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="110a1-470">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="110a1-471">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-471">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="110a1-472">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="110a1-472">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="110a1-473">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="110a1-473">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="110a1-474">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="110a1-474">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="110a1-475">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="110a1-475">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="110a1-476">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="110a1-476">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="110a1-477">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-477">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="110a1-478">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-478">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="110a1-479">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-479">Updated cmdlet:</span></span>
        - <span data-ttu-id="110a1-480">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="110a1-480">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-481">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-481">Az.OperationalInsights</span></span>
* <span data-ttu-id="110a1-482">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-482">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="110a1-483">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-483">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="110a1-484">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="110a1-484">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="110a1-485">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="110a1-485">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="110a1-486">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="110a1-486">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="110a1-487">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-487">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="110a1-488">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-488">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="110a1-489">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-489">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-490">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-491">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-491">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="110a1-492">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-492">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="110a1-493">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-493">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="110a1-494">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-494">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="110a1-495">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-495">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-496">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-496">Az.Resources</span></span>
* <span data-ttu-id="110a1-497">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-497">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="110a1-498">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-498">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="110a1-499">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="110a1-499">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="110a1-500">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="110a1-500">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="110a1-501">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="110a1-501">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="110a1-502">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="110a1-502">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="110a1-503">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="110a1-503">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="110a1-504">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="110a1-504">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="110a1-505">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-505">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="110a1-506">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-506">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="110a1-507">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-507">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="110a1-508">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-508">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="110a1-509">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-509">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="110a1-510">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-510">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="110a1-511">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-511">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="110a1-512">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-512">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="110a1-513">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="110a1-513">'New-AzDeployment'</span></span>
    - <span data-ttu-id="110a1-514">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="110a1-514">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="110a1-515">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="110a1-515">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="110a1-516">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="110a1-516">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="110a1-517">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-517">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-518">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-518">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-519">Az.Sql</span></span>
* <span data-ttu-id="110a1-520">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-520">Enhance performance of:</span></span>
    - <span data-ttu-id="110a1-521">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="110a1-521">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="110a1-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="110a1-522">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="110a1-523">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="110a1-523">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="110a1-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="110a1-524">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="110a1-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="110a1-525">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="110a1-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="110a1-526">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="110a1-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="110a1-527">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="110a1-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="110a1-528">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="110a1-529">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-529">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="110a1-530">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-530">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-531">Az.Storage</span></span>
* <span data-ttu-id="110a1-532">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-532">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="110a1-533">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-533">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="110a1-534">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="110a1-534">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="110a1-535">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-535">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="110a1-536">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="110a1-536">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="110a1-537">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-537">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="110a1-538">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="110a1-538">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="110a1-539">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="110a1-539">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="110a1-540">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="110a1-540">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="110a1-541">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="110a1-541">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="110a1-542">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-542">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="110a1-543">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="110a1-543">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="110a1-544">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="110a1-544">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="110a1-545">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-545">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="110a1-546">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="110a1-546">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="110a1-547">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="110a1-547">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="110a1-548">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-548">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="110a1-549">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="110a1-549">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="110a1-550">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="110a1-550">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="110a1-551">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-551">Supported failover Storage account</span></span>
    - <span data-ttu-id="110a1-552">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="110a1-552">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="110a1-553">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-553">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="110a1-554">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-554">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="110a1-555">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-555">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="110a1-556">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="110a1-556">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="110a1-557">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="110a1-557">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="110a1-558">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="110a1-558">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="110a1-559">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="110a1-559">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="110a1-560">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="110a1-560">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="110a1-561">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="110a1-561">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="110a1-562">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="110a1-562">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="110a1-563">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="110a1-563">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="110a1-564">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="110a1-564">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="110a1-565">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="110a1-565">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="110a1-566">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="110a1-566">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="110a1-567">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="110a1-567">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="110a1-568">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="110a1-568">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="110a1-569">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="110a1-569">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="110a1-570">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="110a1-570">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="110a1-571">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="110a1-571">Az.TrafficManager</span></span>
* <span data-ttu-id="110a1-572">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-572">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-573">Az.Websites</span></span>
* <span data-ttu-id="110a1-574">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-574">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="110a1-575">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-575">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="110a1-576">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="110a1-576">Highlights since the last release</span></span>
* <span data-ttu-id="110a1-577">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="110a1-577">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-578">Az.Accounts</span></span>
* <span data-ttu-id="110a1-579">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="110a1-579">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="110a1-580">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-580">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-581">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-581">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="110a1-582">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-582">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="110a1-583">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="110a1-583">Az.Cdn</span></span>
* <span data-ttu-id="110a1-584">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-584">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-585">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-585">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-586">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="110a1-586">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-587">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-587">Az.Compute</span></span>
* <span data-ttu-id="110a1-588">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-588">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="110a1-589">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-589">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-590">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-590">Az.IotHub</span></span>
* <span data-ttu-id="110a1-591">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-591">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="110a1-592">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="110a1-592">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="110a1-593">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="110a1-593">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="110a1-594">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-594">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="110a1-595">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-595">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="110a1-596">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="110a1-596">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="110a1-597">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="110a1-597">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="110a1-598">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="110a1-598">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="110a1-599">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-599">New cmdlets are:</span></span>
    - <span data-ttu-id="110a1-600">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-600">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="110a1-601">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-601">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="110a1-602">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-602">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="110a1-603">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="110a1-603">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="110a1-604">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-604">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-605">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-605">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-606">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-606">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="110a1-607">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="110a1-607">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="110a1-608">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="110a1-608">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="110a1-609">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-609">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="110a1-610">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="110a1-610">Az.Maintenance</span></span>
* <span data-ttu-id="110a1-611">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="110a1-611">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-612">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-612">Az.Monitor</span></span>
* <span data-ttu-id="110a1-613">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-613">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="110a1-614">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="110a1-614">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="110a1-615">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="110a1-615">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="110a1-616">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="110a1-616">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="110a1-617">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="110a1-617">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="110a1-618">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="110a1-618">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="110a1-619">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="110a1-619">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="110a1-620">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="110a1-620">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-621">Az.Network</span></span>
* <span data-ttu-id="110a1-622">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-622">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="110a1-623">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="110a1-623">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="110a1-624">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="110a1-624">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="110a1-625">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="110a1-625">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="110a1-626">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="110a1-626">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="110a1-627">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-627">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="110a1-628">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="110a1-628">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="110a1-629">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="110a1-629">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="110a1-630">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-630">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="110a1-631">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-631">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="110a1-632">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="110a1-632">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="110a1-633">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-633">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="110a1-634">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-634">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="110a1-635">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-635">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="110a1-636">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-636">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="110a1-637">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-637">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="110a1-638">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-638">Az.PolicyInsights</span></span>
* <span data-ttu-id="110a1-639">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-639">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="110a1-640">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-640">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="110a1-641">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-641">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-642">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-642">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-643">Az.Sql</span></span>
* <span data-ttu-id="110a1-644">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-644">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="110a1-645">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-645">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-646">Az.Storage</span></span>
* <span data-ttu-id="110a1-647">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-647">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="110a1-648">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-648">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="110a1-649">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="110a1-649">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="110a1-650">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="110a1-650">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="110a1-651">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-651">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="110a1-652">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="110a1-652">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="110a1-653">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="110a1-653">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="110a1-654">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="110a1-654">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="110a1-655">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="110a1-655">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="110a1-656">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="110a1-656">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="110a1-657">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="110a1-657">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="110a1-658">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="110a1-658">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="110a1-659">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="110a1-659">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="110a1-660">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-660">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="110a1-661">Genel</span><span class="sxs-lookup"><span data-stu-id="110a1-661">General</span></span>
* <span data-ttu-id="110a1-662">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-662">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="110a1-663">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="110a1-663">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="110a1-664">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="110a1-664">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="110a1-665">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="110a1-665">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="110a1-666">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="110a1-666">Az.Billing</span></span>
  - <span data-ttu-id="110a1-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-667">Az.Compute</span></span>
  - <span data-ttu-id="110a1-668">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="110a1-668">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="110a1-669">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="110a1-669">Az.EventHub</span></span>
  - <span data-ttu-id="110a1-670">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-670">Az.IotHub</span></span>
  - <span data-ttu-id="110a1-671">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-671">Az.KeyVault</span></span>
  - <span data-ttu-id="110a1-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-672">Az.Monitor</span></span>
  - <span data-ttu-id="110a1-673">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-673">Az.Network</span></span>
  - <span data-ttu-id="110a1-674">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-674">Az.Resources</span></span>
  - <span data-ttu-id="110a1-675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-675">Az.Storage</span></span>
  - <span data-ttu-id="110a1-676">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-676">Az.Websites</span></span>
* <span data-ttu-id="110a1-677">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-677">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="110a1-678">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="110a1-678">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="110a1-679">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="110a1-679">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="110a1-680">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-680">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-681">Az.Accounts</span></span>
* <span data-ttu-id="110a1-682">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="110a1-682">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-683">Az.Compute</span></span>
* <span data-ttu-id="110a1-684">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-684">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="110a1-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="110a1-685">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="110a1-686">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-686">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="110a1-687">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-687">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="110a1-688">[#11354]</span><span class="sxs-lookup"><span data-stu-id="110a1-688">[#11354]</span></span>
* <span data-ttu-id="110a1-689">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-689">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="110a1-690">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="110a1-690">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="110a1-691">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="110a1-691">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="110a1-692">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="110a1-692">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="110a1-693">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="110a1-693">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="110a1-694">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-694">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="110a1-695">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-695">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="110a1-696">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-696">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="110a1-697">[#11257]</span><span class="sxs-lookup"><span data-stu-id="110a1-697">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-698">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-699">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-699">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="110a1-700">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-700">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-701">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-701">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-702">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-702">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="110a1-703">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-703">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="110a1-704">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-704">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-705">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-705">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-706">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-706">Az.IotHub</span></span>
* <span data-ttu-id="110a1-707">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-707">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="110a1-708">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-708">New Cmdlets are:</span></span>
    - <span data-ttu-id="110a1-709">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="110a1-709">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="110a1-710">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="110a1-710">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-711">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-711">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-712">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-712">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-713">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-713">Az.Monitor</span></span>
* <span data-ttu-id="110a1-714">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-714">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-715">Az.Network</span></span>
* <span data-ttu-id="110a1-716">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-716">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="110a1-717">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="110a1-717">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="110a1-718">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="110a1-718">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="110a1-719">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="110a1-719">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="110a1-720">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="110a1-720">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="110a1-721">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-721">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="110a1-722">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-722">Az.PolicyInsights</span></span>
* <span data-ttu-id="110a1-723">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-723">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-724">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-724">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-725">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-725">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="110a1-726">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-726">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="110a1-727">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-727">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="110a1-728">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-728">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="110a1-729">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-729">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="110a1-730">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-730">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-731">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-731">Az.Resources</span></span>
* <span data-ttu-id="110a1-732">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="110a1-732">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="110a1-733">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-733">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="110a1-734">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-734">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="110a1-735">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-735">Added example.</span></span>
* <span data-ttu-id="110a1-736">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="110a1-736">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="110a1-737">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="110a1-737">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-738">Az.Sql</span></span>
* <span data-ttu-id="110a1-739">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-739">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="110a1-740">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-740">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="110a1-741">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-741">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="110a1-742">Az.Support</span><span class="sxs-lookup"><span data-stu-id="110a1-742">Az.Support</span></span>
* <span data-ttu-id="110a1-743">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-743">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-744">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-744">Az.Websites</span></span>
* <span data-ttu-id="110a1-745">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-745">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="110a1-746">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="110a1-746">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="110a1-747">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="110a1-747">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="110a1-748">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="110a1-748">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="110a1-749">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="110a1-749">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="110a1-750">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-750">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-751">Az.Accounts</span></span>
* <span data-ttu-id="110a1-752">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="110a1-752">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="110a1-753">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="110a1-753">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="110a1-754">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-754">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="110a1-755">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-755">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-756">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="110a1-756">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="110a1-757">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="110a1-757">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="110a1-758">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-758">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="110a1-759">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="110a1-759">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-760">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-760">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-761">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-761">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-762">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-762">Az.IotHub</span></span>
* <span data-ttu-id="110a1-763">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-763">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="110a1-764">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-764">New Cmdlets are:</span></span>
    - <span data-ttu-id="110a1-765">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="110a1-765">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="110a1-766">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="110a1-766">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="110a1-767">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="110a1-767">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="110a1-768">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="110a1-768">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="110a1-769">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-769">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="110a1-770">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-770">New Cmdlets are:</span></span>
    - <span data-ttu-id="110a1-771">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="110a1-771">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="110a1-772">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="110a1-772">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="110a1-773">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="110a1-773">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="110a1-774">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="110a1-774">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="110a1-775">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-775">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="110a1-776">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-776">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="110a1-777">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-777">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="110a1-778">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-778">New Cmdlets are:</span></span>
    - <span data-ttu-id="110a1-779">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="110a1-779">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="110a1-780">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="110a1-780">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="110a1-781">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-781">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-782">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-782">Az.Monitor</span></span>
* <span data-ttu-id="110a1-783">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="110a1-783">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-784">Az.Network</span></span>
* <span data-ttu-id="110a1-785">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-785">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="110a1-786">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-786">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="110a1-787">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-787">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="110a1-788">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-788">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-789">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-789">Az.Resources</span></span>
* <span data-ttu-id="110a1-790">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-790">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="110a1-791">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="110a1-791">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="110a1-792">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="110a1-792">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="110a1-793">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="110a1-793">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="110a1-794">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-794">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="110a1-795">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-795">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="110a1-796">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-796">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="110a1-797">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="110a1-797">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="110a1-798">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="110a1-798">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="110a1-799">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="110a1-799">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="110a1-800">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="110a1-800">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="110a1-801">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-801">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="110a1-802">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="110a1-802">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="110a1-803">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-803">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-804">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-804">Az.Sql</span></span>
* <span data-ttu-id="110a1-805">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-805">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="110a1-806">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-806">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="110a1-807">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="110a1-807">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="110a1-808">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="110a1-808">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="110a1-809">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="110a1-809">Remove an LTR backup</span></span>
    - <span data-ttu-id="110a1-810">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="110a1-810">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="110a1-811">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-811">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="110a1-812">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-812">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="110a1-813">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-813">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-814">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-814">Az.Storage</span></span>
* <span data-ttu-id="110a1-815">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-815">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="110a1-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="110a1-816">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="110a1-817">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-817">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="110a1-818">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="110a1-818">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="110a1-819">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="110a1-819">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-820">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-820">Az.Websites</span></span>
* <span data-ttu-id="110a1-821">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-821">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="110a1-822">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="110a1-822">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="110a1-823">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-823">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="110a1-824">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="110a1-824">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="110a1-825">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-825">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="110a1-826">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-826">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="110a1-827">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="110a1-827">Highlights since the last major release</span></span>
* <span data-ttu-id="110a1-828">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-828">Updated client side telemetry.</span></span>
* <span data-ttu-id="110a1-829">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-829">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="110a1-830">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-830">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-831">Az.Accounts</span></span>
* <span data-ttu-id="110a1-832">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-832">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-833">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-833">Az.Automation</span></span>
* <span data-ttu-id="110a1-834">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-834">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-835">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-835">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-836">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-836">Updated SDK to 7.0</span></span>
* <span data-ttu-id="110a1-837">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-837">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-838">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-838">Az.Compute</span></span>
* <span data-ttu-id="110a1-839">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="110a1-839">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="110a1-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="110a1-840">Az.FrontDoor</span></span>
* <span data-ttu-id="110a1-841">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-841">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-842">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-842">Az.IotHub</span></span>
* <span data-ttu-id="110a1-843">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-843">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="110a1-844">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-844">New Cmdlets are:</span></span>
    - <span data-ttu-id="110a1-845">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="110a1-845">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="110a1-846">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="110a1-846">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="110a1-847">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="110a1-847">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="110a1-848">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="110a1-848">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-849">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-849">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-850">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-850">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-851">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-851">Az.Monitor</span></span>
* <span data-ttu-id="110a1-852">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-852">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="110a1-853">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-853">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="110a1-854">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-854">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-855">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-855">Az.Network</span></span>
* <span data-ttu-id="110a1-856">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-856">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="110a1-857">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-857">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="110a1-858">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-858">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="110a1-859">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="110a1-859">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="110a1-860">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="110a1-860">No new cmdlets are added.</span></span> <span data-ttu-id="110a1-861">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="110a1-861">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-862">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-862">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-863">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-863">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-864">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-864">Az.Resources</span></span>
* <span data-ttu-id="110a1-865">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="110a1-865">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="110a1-866">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="110a1-866">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="110a1-867">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="110a1-867">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="110a1-868">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="110a1-868">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="110a1-869">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-869">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="110a1-870">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-870">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="110a1-871">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-871">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="110a1-872">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-872">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-873">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-873">Az.Sql</span></span>
* <span data-ttu-id="110a1-874">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-874">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="110a1-875">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-875">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="110a1-876">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="110a1-876">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="110a1-877">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="110a1-877">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="110a1-878">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-878">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="110a1-879">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="110a1-879">Az.StorageSync</span></span>
* <span data-ttu-id="110a1-880">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-880">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="110a1-881">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-881">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="110a1-882">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="110a1-882">Highlights since the last major release</span></span>
* <span data-ttu-id="110a1-883">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="110a1-883">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="110a1-884">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-884">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-885">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-885">Az.Accounts</span></span>
* <span data-ttu-id="110a1-886">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="110a1-886">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="110a1-887">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-887">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="110a1-888">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-888">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-889">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="110a1-889">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="110a1-890">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="110a1-890">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="110a1-891">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-891">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="110a1-892">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-892">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-893">Az.Compute</span></span>
* <span data-ttu-id="110a1-894">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="110a1-894">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="110a1-895">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-895">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="110a1-896">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-896">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="110a1-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-897">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="110a1-898">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-898">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-899">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-899">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-900">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-900">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="110a1-901">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="110a1-901">Az.DeploymentManager</span></span>
* <span data-ttu-id="110a1-902">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="110a1-902">Adds LIST operations for resources</span></span>
* <span data-ttu-id="110a1-903">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="110a1-903">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="110a1-904">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-904">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-905">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-905">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-906">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-907">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-907">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-908">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-908">Az.Network</span></span>
* <span data-ttu-id="110a1-909">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-909">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="110a1-910">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="110a1-910">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="110a1-911">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-911">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="110a1-912">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-912">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="110a1-913">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="110a1-913">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="110a1-914">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-914">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="110a1-915">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-915">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="110a1-916">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-916">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="110a1-917">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-917">New cmdlets added:</span></span>
        - <span data-ttu-id="110a1-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="110a1-918">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="110a1-919">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-919">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="110a1-920">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="110a1-920">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="110a1-921">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-921">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="110a1-922">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-922">Az.PolicyInsights</span></span>
* <span data-ttu-id="110a1-923">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="110a1-923">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="110a1-924">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-924">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="110a1-925">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-925">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="110a1-926">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-926">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-927">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-927">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-928">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-928">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="110a1-929">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="110a1-929">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-930">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-930">Az.Resources</span></span>
* <span data-ttu-id="110a1-931">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-931">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="110a1-932">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-932">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-933">Az.Sql</span></span>
<span data-ttu-id="110a1-934">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-934">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-935">Az.Storage</span></span>
* <span data-ttu-id="110a1-936">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="110a1-936">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="110a1-937">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-937">New-AzStorageAccount</span></span>
* <span data-ttu-id="110a1-938">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="110a1-938">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="110a1-939">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-939">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-940">Az.Websites</span></span>
* <span data-ttu-id="110a1-941">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="110a1-941">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="110a1-942">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-942">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="110a1-943">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="110a1-943">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-944">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-944">Az.Accounts</span></span>
* <span data-ttu-id="110a1-945">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-945">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="110a1-946">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="110a1-946">Az.Cdn</span></span>
* <span data-ttu-id="110a1-947">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="110a1-947">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-948">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-948">Az.Compute</span></span>
* <span data-ttu-id="110a1-949">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-949">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="110a1-950">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="110a1-950">Az.ContainerInstance</span></span>
* <span data-ttu-id="110a1-951">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-951">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="110a1-952">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="110a1-952">Az.DataBoxEdge</span></span>
* <span data-ttu-id="110a1-953">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-953">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="110a1-954">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="110a1-954">Get the Edge Storage Container</span></span>
* <span data-ttu-id="110a1-955">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-955">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="110a1-956">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="110a1-956">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="110a1-957">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-957">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="110a1-958">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="110a1-958">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="110a1-959">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-959">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="110a1-960">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="110a1-960">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="110a1-961">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-961">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="110a1-962">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="110a1-962">Get the Edge Storage Account</span></span>
* <span data-ttu-id="110a1-963">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-963">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="110a1-964">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="110a1-964">Create new Edge Storage Account</span></span>
* <span data-ttu-id="110a1-965">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-965">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="110a1-966">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="110a1-966">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="110a1-967">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="110a1-967">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="110a1-968">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="110a1-968">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="110a1-969">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-969">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="110a1-970">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="110a1-970">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-971">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-971">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-972">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-972">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="110a1-973">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-973">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="110a1-974">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-974">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="110a1-975">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="110a1-975">Az.DevTestLabs</span></span>
* <span data-ttu-id="110a1-976">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-976">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="110a1-977">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="110a1-977">Az.EventHub</span></span>
* <span data-ttu-id="110a1-978">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-978">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="110a1-979">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-979">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-980">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-980">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="110a1-981">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="110a1-981">Az.MachineLearning</span></span>
* <span data-ttu-id="110a1-982">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-982">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="110a1-983">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="110a1-983">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="110a1-984">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="110a1-984">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="110a1-985">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="110a1-985">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="110a1-986">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="110a1-986">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="110a1-987">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="110a1-987">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="110a1-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="110a1-988">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="110a1-989">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="110a1-989">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-990">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-990">Az.Network</span></span>
* <span data-ttu-id="110a1-991">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-991">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-992">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-993">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-993">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="110a1-994">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-994">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="110a1-995">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-995">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="110a1-996">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-996">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-997">Az.Resources</span></span>
* <span data-ttu-id="110a1-998">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-998">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-999">Az.Sql</span></span>
* <span data-ttu-id="110a1-1000">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1000">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="110a1-1001">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1001">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="110a1-1002">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="110a1-1002">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="110a1-1003">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1003">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-1004">Az.Storage</span></span>
* <span data-ttu-id="110a1-1005">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1005">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="110a1-1006">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="110a1-1006">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="110a1-1007">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="110a1-1007">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="110a1-1008">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-1008">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="110a1-1009">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1009">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="110a1-1010">Genel</span><span class="sxs-lookup"><span data-stu-id="110a1-1010">General</span></span>
* <span data-ttu-id="110a1-1011">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1011">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-1012">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-1012">Az.Accounts</span></span>
* <span data-ttu-id="110a1-1013">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="110a1-1013">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="110a1-1014">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="110a1-1014">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="110a1-1015">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="110a1-1015">Az.Batch</span></span>
* <span data-ttu-id="110a1-1016">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1016">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-1017">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-1017">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-1018">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1018">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="110a1-1019">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="110a1-1019">Az.FrontDoor</span></span>
* <span data-ttu-id="110a1-1020">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1020">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="110a1-1021">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1021">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="110a1-1022">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="110a1-1022">Az.HealthcareApis</span></span>
* <span data-ttu-id="110a1-1023">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="110a1-1023">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-1024">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-1025">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1025">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="110a1-1026">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="110a1-1026">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="110a1-1027">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1027">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-1028">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-1028">Az.Monitor</span></span>
* <span data-ttu-id="110a1-1029">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1029">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="110a1-1030">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="110a1-1030">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="110a1-1031">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="110a1-1031">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1032">Az.Network</span></span>
* <span data-ttu-id="110a1-1033">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1033">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-1034">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-1034">Az.Resources</span></span>
* <span data-ttu-id="110a1-1035">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1035">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="110a1-1036">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1036">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1037">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1037">Az.Sql</span></span>
* <span data-ttu-id="110a1-1038">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1038">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-1039">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-1039">Az.Storage</span></span>
* <span data-ttu-id="110a1-1040">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-1040">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="110a1-1041">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="110a1-1041">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="110a1-1042">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="110a1-1042">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="110a1-1043">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-1043">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="110a1-1044">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="110a1-1044">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="110a1-1045">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1045">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="110a1-1046">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1046">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="110a1-1047">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="110a1-1047">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="110a1-1048">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="110a1-1048">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="110a1-1049">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1049">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="110a1-1050">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="110a1-1050">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="110a1-1051">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1051">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="110a1-1052">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="110a1-1052">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="110a1-1053">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1053">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="110a1-1054">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="110a1-1054">Highlights since the last major release</span></span>
* <span data-ttu-id="110a1-1055">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="110a1-1055">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="110a1-1056">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="110a1-1056">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1057">Az.Compute</span></span>
* <span data-ttu-id="110a1-1058">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="110a1-1058">VM Reapply feature</span></span>
    - <span data-ttu-id="110a1-1059">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="110a1-1059">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="110a1-1060">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="110a1-1060">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="110a1-1061">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="110a1-1061">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="110a1-1062">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-1062">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="110a1-1063">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1063">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="110a1-1064">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1064">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="110a1-1065">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1065">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="110a1-1066">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1066">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="110a1-1067">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1067">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="110a1-1068">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1068">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="110a1-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="110a1-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="110a1-1070">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1070">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="110a1-1071">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="110a1-1071">Get the Order</span></span>
* <span data-ttu-id="110a1-1072">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1072">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="110a1-1073">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="110a1-1073">Create new Order</span></span>
* <span data-ttu-id="110a1-1074">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1074">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="110a1-1075">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="110a1-1075">Remove the Order</span></span>
* <span data-ttu-id="110a1-1076">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="110a1-1076">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="110a1-1077">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="110a1-1077">Now creates Local Share</span></span>
* <span data-ttu-id="110a1-1078">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1078">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="110a1-1079">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="110a1-1079">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="110a1-1080">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1080">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="110a1-1081">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="110a1-1081">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="110a1-1082">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1082">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="110a1-1083">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="110a1-1083">Gets the information about Triggers</span></span>
* <span data-ttu-id="110a1-1084">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1084">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="110a1-1085">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="110a1-1085">Create new Triggers</span></span>
* <span data-ttu-id="110a1-1086">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1086">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="110a1-1087">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="110a1-1087">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-1088">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-1089">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1089">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="110a1-1090">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1090">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-1091">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-1091">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-1092">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1092">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="110a1-1093">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="110a1-1093">Az.EventHub</span></span>
* <span data-ttu-id="110a1-1094">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1094">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="110a1-1095">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="110a1-1095">Az.FrontDoor</span></span>
* <span data-ttu-id="110a1-1096">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1096">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="110a1-1097">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1097">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="110a1-1098">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1098">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="110a1-1099">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="110a1-1099">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1100">Az.Network</span></span>
* <span data-ttu-id="110a1-1101">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1101">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="110a1-1102">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="110a1-1102">Az.PrivateDns</span></span>
* <span data-ttu-id="110a1-1103">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1103">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-1104">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-1104">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-1105">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1105">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="110a1-1106">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1106">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="110a1-1107">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1107">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="110a1-1108">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="110a1-1108">Az.RedisCache</span></span>
* <span data-ttu-id="110a1-1109">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1109">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="110a1-1110">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1110">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="110a1-1111">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1111">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-1112">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-1112">Az.Resources</span></span>
- <span data-ttu-id="110a1-1113">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1113">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="110a1-1114">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1114">Updated create policy definition help example</span></span>
- <span data-ttu-id="110a1-1115">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1115">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="110a1-1116">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1116">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="110a1-1117">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1117">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1118">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1118">Az.Sql</span></span>
* <span data-ttu-id="110a1-1119">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1119">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="110a1-1120">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1120">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="110a1-1121">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1121">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="110a1-1122">Genel</span><span class="sxs-lookup"><span data-stu-id="110a1-1122">General</span></span>
* <span data-ttu-id="110a1-1123">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="110a1-1123">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-1124">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-1124">Az.Accounts</span></span>
* <span data-ttu-id="110a1-1125">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="110a1-1125">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="110a1-1126">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="110a1-1126">Az.Advisor</span></span>
* <span data-ttu-id="110a1-1127">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1127">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="110a1-1128">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="110a1-1128">Az.Batch</span></span>
* <span data-ttu-id="110a1-1129">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1129">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="110a1-1130">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="110a1-1130">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="110a1-1131">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1131">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="110a1-1132">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1132">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="110a1-1133">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="110a1-1133">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="110a1-1134">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-1134">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="110a1-1135">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="110a1-1135">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="110a1-1136">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1136">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="110a1-1137">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1137">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="110a1-1138">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1138">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="110a1-1139">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-1139">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="110a1-1140">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="110a1-1140">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="110a1-1141">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1141">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="110a1-1142">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="110a1-1142">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="110a1-1143">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1143">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="110a1-1144">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1144">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="110a1-1145">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1145">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="110a1-1146">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1146">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="110a1-1147">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1147">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="110a1-1148">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1148">This operation is no longer supported.</span></span>
* <span data-ttu-id="110a1-1149">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1149">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="110a1-1150">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1150">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="110a1-1151">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1151">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="110a1-1152">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1152">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="110a1-1153">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1153">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="110a1-1154">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1154">New non-verified images are also now returned.</span></span> <span data-ttu-id="110a1-1155">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1155">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="110a1-1156">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1156">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="110a1-1157">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1157">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="110a1-1158">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1158">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="110a1-1159">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1159">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="110a1-1160">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1160">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="110a1-1161">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1161">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="110a1-1162">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1162">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="110a1-1163">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="110a1-1163">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="110a1-1164">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="110a1-1164">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="110a1-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="110a1-1165">Az.Cdn</span></span>
* <span data-ttu-id="110a1-1166">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1166">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="110a1-1167">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1167">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1168">Az.Compute</span></span>
* <span data-ttu-id="110a1-1169">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="110a1-1169">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="110a1-1170">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="110a1-1170">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="110a1-1171">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="110a1-1171">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="110a1-1172">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1172">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="110a1-1173">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1173">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="110a1-1174">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="110a1-1174">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="110a1-1175">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1175">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="110a1-1176">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="110a1-1176">Breaking changes</span></span>
    - <span data-ttu-id="110a1-1177">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="110a1-1177">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="110a1-1178">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="110a1-1178">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-1179">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-1179">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-1180">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1180">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-1181">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-1181">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-1182">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="110a1-1182">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="110a1-1183">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="110a1-1183">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="110a1-1184">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="110a1-1184">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="110a1-1185">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="110a1-1185">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="110a1-1186">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="110a1-1186">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="110a1-1187">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="110a1-1187">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="110a1-1188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="110a1-1188">Az.FrontDoor</span></span>
* <span data-ttu-id="110a1-1189">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1189">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="110a1-1190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-1190">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-1191">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1191">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="110a1-1192">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1192">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="110a1-1193">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1193">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="110a1-1194">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="110a1-1194">Removed five cmdlets:</span></span>
    - <span data-ttu-id="110a1-1195">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="110a1-1195">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="110a1-1196">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="110a1-1196">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="110a1-1197">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="110a1-1197">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="110a1-1198">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="110a1-1198">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="110a1-1199">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="110a1-1199">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="110a1-1200">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1200">Added three cmdlets:</span></span>
    - <span data-ttu-id="110a1-1201">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="110a1-1201">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="110a1-1202">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="110a1-1202">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="110a1-1203">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="110a1-1203">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="110a1-1204">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1204">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="110a1-1205">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1205">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="110a1-1206">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1206">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="110a1-1207">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1207">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="110a1-1208">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1208">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="110a1-1209">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1209">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="110a1-1210">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1210">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="110a1-1211">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1211">Added some scenario test cases.</span></span>
* <span data-ttu-id="110a1-1212">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="110a1-1212">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-1213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-1213">Az.IotHub</span></span>
* <span data-ttu-id="110a1-1214">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="110a1-1214">Breaking changes:</span></span>
    - <span data-ttu-id="110a1-1215">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1215">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="110a1-1216">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1216">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="110a1-1217">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1217">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="110a1-1218">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1218">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="110a1-1219">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1219">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="110a1-1220">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1220">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="110a1-1221">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1221">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="110a1-1222">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1222">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="110a1-1223">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1223">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="110a1-1224">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1224">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="110a1-1225">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1225">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="110a1-1226">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1226">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-1227">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-1227">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-1228">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1228">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="110a1-1229">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1229">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="110a1-1230">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1230">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="110a1-1231">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1231">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="110a1-1232">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1232">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="110a1-1233">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1233">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="110a1-1234">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1234">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="110a1-1235">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1235">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="110a1-1236">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1236">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-1237">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-1237">Az.Resources</span></span>
* <span data-ttu-id="110a1-1238">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1238">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1239">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1239">Az.Network</span></span>
* <span data-ttu-id="110a1-1240">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1240">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="110a1-1241">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1241">Updated cmdlet:</span></span>
        - <span data-ttu-id="110a1-1242">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1242">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="110a1-1243">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1243">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="110a1-1244">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1244">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="110a1-1245">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1245">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="110a1-1246">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1246">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="110a1-1247">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1247">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="110a1-1248">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="110a1-1248">New cmdlet:</span></span>
        - <span data-ttu-id="110a1-1249">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="110a1-1249">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="110a1-1250">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1250">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="110a1-1251">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1251">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="110a1-1252">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1252">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="110a1-1253">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1253">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="110a1-1254">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1254">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="110a1-1255">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1255">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="110a1-1256">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1256">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="110a1-1257">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1257">New cmdlets added:</span></span>
        - <span data-ttu-id="110a1-1258">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="110a1-1258">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="110a1-1259">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="110a1-1259">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="110a1-1260">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="110a1-1260">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="110a1-1261">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="110a1-1261">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="110a1-1262">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="110a1-1262">Set-AzVirtualHub</span></span>
* <span data-ttu-id="110a1-1263">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1263">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="110a1-1264">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1264">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="110a1-1265">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1265">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="110a1-1266">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1266">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="110a1-1267">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1267">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="110a1-1268">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1268">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="110a1-1269">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1269">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="110a1-1270">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1270">New cmdlets added:</span></span>
        - <span data-ttu-id="110a1-1271">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1271">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="110a1-1272">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1272">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="110a1-1273">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1273">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="110a1-1274">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1274">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="110a1-1275">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1275">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="110a1-1276">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1276">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="110a1-1277">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1277">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="110a1-1278">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1278">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="110a1-1279">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1279">New cmdlets added:</span></span>
        - <span data-ttu-id="110a1-1280">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="110a1-1280">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="110a1-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="110a1-1281">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="110a1-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="110a1-1282">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="110a1-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="110a1-1283">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="110a1-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="110a1-1284">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="110a1-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="110a1-1285">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="110a1-1286">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1286">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="110a1-1287">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1287">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="110a1-1288">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1288">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="110a1-1289">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1289">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="110a1-1290">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1290">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="110a1-1291">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1291">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="110a1-1292">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1292">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="110a1-1293">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1293">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="110a1-1294">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1294">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="110a1-1295">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="110a1-1295">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="110a1-1296">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1296">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="110a1-1297">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1297">New cmdlets added:</span></span>
        - <span data-ttu-id="110a1-1298">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="110a1-1298">New-AzIpGroup</span></span>
        - <span data-ttu-id="110a1-1299">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="110a1-1299">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="110a1-1300">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="110a1-1300">Get-AzIpGroup</span></span>
        - <span data-ttu-id="110a1-1301">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="110a1-1301">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="110a1-1302">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-1302">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-1303">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1303">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1304">Az.Sql</span></span>
* <span data-ttu-id="110a1-1305">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1305">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="110a1-1306">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1306">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="110a1-1307">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="110a1-1307">Removed deprecated aliases:</span></span>
* <span data-ttu-id="110a1-1308">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="110a1-1308">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="110a1-1309">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="110a1-1309">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="110a1-1310">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1310">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="110a1-1311">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1311">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="110a1-1312">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1312">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="110a1-1313">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1313">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-1314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-1314">Az.Storage</span></span>
* <span data-ttu-id="110a1-1315">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-1315">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="110a1-1316">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-1316">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="110a1-1317">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-1317">Set-AzStorageAccount</span></span>
* <span data-ttu-id="110a1-1318">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="110a1-1318">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="110a1-1319">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="110a1-1319">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="110a1-1320">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="110a1-1320">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="110a1-1321">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1321">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="110a1-1322">Genel</span><span class="sxs-lookup"><span data-stu-id="110a1-1322">General</span></span>
* <span data-ttu-id="110a1-1323">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="110a1-1323">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-1324">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-1324">Az.Accounts</span></span>
* <span data-ttu-id="110a1-1325">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1325">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="110a1-1326">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-1326">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-1327">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1327">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="110a1-1328">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1328">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-1329">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-1329">Az.Automation</span></span>
* <span data-ttu-id="110a1-1330">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1330">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="110a1-1331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="110a1-1331">Az.Batch</span></span>
* <span data-ttu-id="110a1-1332">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="110a1-1332">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1333">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1333">Az.Compute</span></span>
* <span data-ttu-id="110a1-1334">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1334">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="110a1-1335">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1335">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="110a1-1336">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1336">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="110a1-1337">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1337">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-1338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-1338">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-1339">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="110a1-1339">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="110a1-1340">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="110a1-1340">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="110a1-1341">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1341">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-1343">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1343">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="110a1-1344">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="110a1-1344">Az.HealthcareApis</span></span>
* <span data-ttu-id="110a1-1345">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1345">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="110a1-1346">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1346">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="110a1-1347">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1347">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="110a1-1348">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1348">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-1349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-1349">Az.IotHub</span></span>
* <span data-ttu-id="110a1-1350">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="110a1-1350">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="110a1-1351">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="110a1-1351">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-1352">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-1352">Az.Monitor</span></span>
* <span data-ttu-id="110a1-1353">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1353">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="110a1-1354">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="110a1-1354">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="110a1-1355">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="110a1-1355">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="110a1-1356">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1356">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1357">Az.Network</span></span>
* <span data-ttu-id="110a1-1358">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1358">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="110a1-1359">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1359">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="110a1-1360">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1360">New cmdlets added:</span></span>
        - <span data-ttu-id="110a1-1361">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="110a1-1361">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="110a1-1362">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1362">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="110a1-1363">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1363">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="110a1-1364">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1364">Updated cmdlets:</span></span>
        - <span data-ttu-id="110a1-1365">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1365">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="110a1-1366">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1366">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="110a1-1367">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1367">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="110a1-1368">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1368">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="110a1-1369">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="110a1-1369">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="110a1-1370">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="110a1-1370">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="110a1-1371">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="110a1-1371">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="110a1-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="110a1-1372">Az.RedisCache</span></span>
* <span data-ttu-id="110a1-1373">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1373">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1374">Az.Sql</span></span>
* <span data-ttu-id="110a1-1375">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1375">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-1376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-1376">Az.Storage</span></span>
* <span data-ttu-id="110a1-1377">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1377">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="110a1-1378">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="110a1-1378">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="110a1-1379">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="110a1-1379">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="110a1-1380">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="110a1-1380">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="110a1-1381">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-1381">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="110a1-1382">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="110a1-1382">Az.StorageSync</span></span>
* <span data-ttu-id="110a1-1383">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1383">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-1384">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-1384">Az.Websites</span></span>
* <span data-ttu-id="110a1-1385">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="110a1-1385">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="110a1-1386">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1386">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="110a1-1387">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-1387">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-1388">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1388">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="110a1-1389">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1389">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="110a1-1390">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="110a1-1390">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-1391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-1391">Az.Automation</span></span>
* <span data-ttu-id="110a1-1392">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1392">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="110a1-1393">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1393">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="110a1-1394">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1394">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1395">Az.Compute</span></span>
* <span data-ttu-id="110a1-1396">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1396">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="110a1-1397">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1397">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="110a1-1398">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1398">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="110a1-1399">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1399">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="110a1-1400">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1400">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="110a1-1401">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1401">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="110a1-1402">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1402">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="110a1-1403">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1403">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="110a1-1404">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1404">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-1405">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-1405">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-1406">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="110a1-1406">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="110a1-1407">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1407">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="110a1-1408">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-1408">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-1409">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="110a1-1409">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-1410">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-1410">Az.IotHub</span></span>
* <span data-ttu-id="110a1-1411">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1411">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="110a1-1412">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1412">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="110a1-1413">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="110a1-1413">New cmdlets are:</span></span>
    - <span data-ttu-id="110a1-1414">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="110a1-1414">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="110a1-1415">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="110a1-1415">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="110a1-1416">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="110a1-1416">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="110a1-1417">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="110a1-1417">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-1418">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-1418">Az.Monitor</span></span>
* <span data-ttu-id="110a1-1419">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="110a1-1419">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="110a1-1420">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-1420">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="110a1-1421">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="110a1-1421">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="110a1-1422">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="110a1-1422">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="110a1-1423">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1423">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="110a1-1424">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1424">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="110a1-1425">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1425">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="110a1-1426">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="110a1-1426">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="110a1-1427">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1427">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="110a1-1428">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="110a1-1428">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="110a1-1429">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1429">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="110a1-1430">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="110a1-1430">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="110a1-1431">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1431">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="110a1-1432">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="110a1-1432">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="110a1-1433">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="110a1-1433">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="110a1-1434">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="110a1-1434">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="110a1-1435">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="110a1-1435">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="110a1-1436">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="110a1-1436">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="110a1-1437">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1437">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="110a1-1438">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1438">Overall improved help files</span></span>
* <span data-ttu-id="110a1-1439">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1439">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1440">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1440">Az.Network</span></span>
* <span data-ttu-id="110a1-1441">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1441">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="110a1-1442">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1442">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="110a1-1443">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1443">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="110a1-1444">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1444">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="110a1-1445">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1445">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="110a1-1446">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1446">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="110a1-1447">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1447">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="110a1-1448">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1448">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="110a1-1449">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1449">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="110a1-1450">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1450">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="110a1-1451">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1451">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="110a1-1452">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-1452">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="110a1-1453">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-1453">New cmdlets</span></span>
        - <span data-ttu-id="110a1-1454">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="110a1-1454">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="110a1-1455">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1455">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="110a1-1456">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1456">Updated cmdlet:</span></span>
        - <span data-ttu-id="110a1-1457">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="110a1-1457">New-VpnSite</span></span>
        - <span data-ttu-id="110a1-1458">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="110a1-1458">Update-VpnSite</span></span>
        - <span data-ttu-id="110a1-1459">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1459">New-VpnConnection</span></span>
        - <span data-ttu-id="110a1-1460">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1460">Update-VpnConnection</span></span>
* <span data-ttu-id="110a1-1461">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1461">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-1463">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1463">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="110a1-1464">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1464">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-1465">Az.Resources</span></span>
* <span data-ttu-id="110a1-1466">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1466">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="110a1-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-1468">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1468">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="110a1-1469">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="110a1-1469">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="110a1-1470">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="110a1-1470">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="110a1-1471">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="110a1-1471">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="110a1-1472">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="110a1-1472">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="110a1-1473">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="110a1-1473">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="110a1-1474">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="110a1-1474">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="110a1-1475">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="110a1-1475">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="110a1-1476">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="110a1-1476">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="110a1-1477">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="110a1-1477">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="110a1-1478">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="110a1-1478">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="110a1-1479">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="110a1-1479">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="110a1-1480">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="110a1-1480">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="110a1-1481">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="110a1-1481">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="110a1-1482">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="110a1-1482">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="110a1-1483">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1483">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="110a1-1484">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="110a1-1484">Az.SignalR</span></span>
* <span data-ttu-id="110a1-1485">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1485">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1486">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1486">Az.Sql</span></span>
* <span data-ttu-id="110a1-1487">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1487">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="110a1-1488">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1488">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="110a1-1489">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1489">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="110a1-1490">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1490">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="110a1-1491">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1491">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-1492">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-1492">Az.Storage</span></span>
* <span data-ttu-id="110a1-1493">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1493">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="110a1-1494">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1494">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="110a1-1495">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="110a1-1495">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="110a1-1496">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="110a1-1496">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="110a1-1497">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1497">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="110a1-1498">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="110a1-1498">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="110a1-1499">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1499">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="110a1-1500">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="110a1-1500">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="110a1-1501">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="110a1-1501">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="110a1-1502">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="110a1-1502">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="110a1-1503">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="110a1-1503">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-1504">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-1504">Az.Websites</span></span>
* <span data-ttu-id="110a1-1505">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="110a1-1505">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="110a1-1506">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="110a1-1506">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="110a1-1507">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1507">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="110a1-1508">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1508">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="110a1-1509">Genel</span><span class="sxs-lookup"><span data-stu-id="110a1-1509">General</span></span>
* <span data-ttu-id="110a1-1510">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1510">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-1511">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-1511">Az.Accounts</span></span>
* <span data-ttu-id="110a1-1512">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="110a1-1512">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="110a1-1513">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="110a1-1513">Az.Aks</span></span>
* <span data-ttu-id="110a1-1514">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1514">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="110a1-1515">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="110a1-1515">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="110a1-1516">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-1516">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-1517">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1517">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="110a1-1518">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1518">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="110a1-1519">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1519">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="110a1-1520">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="110a1-1520">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="110a1-1521">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1521">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="110a1-1522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="110a1-1522">Az.Batch</span></span>
* <span data-ttu-id="110a1-1523">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1523">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="110a1-1524">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="110a1-1524">Az.Cdn</span></span>
* <span data-ttu-id="110a1-1525">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1525">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1526">Az.Compute</span></span>
* <span data-ttu-id="110a1-1527">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1527">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="110a1-1528">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1528">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="110a1-1529">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1529">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="110a1-1530">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1530">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="110a1-1531">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="110a1-1531">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="110a1-1532">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1532">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="110a1-1533">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1533">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="110a1-1534">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1534">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-1535">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-1535">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-1536">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1536">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="110a1-1537">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1537">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="110a1-1538">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1538">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="110a1-1539">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1539">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-1540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-1540">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-1541">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1541">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="110a1-1542">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="110a1-1542">Az.EventHub</span></span>
* <span data-ttu-id="110a1-1543">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="110a1-1543">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="110a1-1544">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="110a1-1544">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="110a1-1545">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1545">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="110a1-1546">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="110a1-1546">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="110a1-1547">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="110a1-1547">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="110a1-1548">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1548">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-1549">Az.Monitor</span></span>
* <span data-ttu-id="110a1-1550">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1550">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1551">Az.Network</span></span>
* <span data-ttu-id="110a1-1552">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1552">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="110a1-1553">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1553">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="110a1-1554">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1554">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="110a1-1555">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="110a1-1555">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="110a1-1556">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1556">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="110a1-1557">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1557">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="110a1-1558">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1558">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-1559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-1559">Az.OperationalInsights</span></span>
* <span data-ttu-id="110a1-1560">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1560">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="110a1-1561">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1561">Added example</span></span>
    - <span data-ttu-id="110a1-1562">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1562">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="110a1-1563">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1563">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="110a1-1564">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1564">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-1565">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-1565">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-1566">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1566">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-1567">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-1567">Az.Resources</span></span>
* <span data-ttu-id="110a1-1568">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1568">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="110a1-1569">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1569">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="110a1-1570">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="110a1-1570">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="110a1-1571">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1571">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="110a1-1572">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="110a1-1572">Az.ServiceBus</span></span>
* <span data-ttu-id="110a1-1573">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="110a1-1573">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="110a1-1574">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="110a1-1574">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="110a1-1575">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1575">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="110a1-1576">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-1576">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-1577">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1577">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="110a1-1578">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="110a1-1578">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="110a1-1579">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="110a1-1579">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="110a1-1580">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1580">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="110a1-1581">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="110a1-1581">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="110a1-1582">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1582">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1583">Az.Sql</span></span>
* <span data-ttu-id="110a1-1584">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1584">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-1585">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-1585">Az.Storage</span></span>
* <span data-ttu-id="110a1-1586">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1586">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="110a1-1587">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="110a1-1587">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="110a1-1588">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="110a1-1588">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="110a1-1589">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="110a1-1589">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="110a1-1590">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-1590">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="110a1-1591">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="110a1-1591">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-1592">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-1592">Az.Websites</span></span>
* <span data-ttu-id="110a1-1593">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1593">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="110a1-1594">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1594">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-1595">Az.Accounts</span></span>
* <span data-ttu-id="110a1-1596">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1596">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="110a1-1597">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-1597">Az.ApplicationInsights</span></span>
* <span data-ttu-id="110a1-1598">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1598">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-1599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-1599">Az.Automation</span></span>
* <span data-ttu-id="110a1-1600">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1600">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-1601">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-1601">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-1602">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1602">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1603">Az.Compute</span></span>
* <span data-ttu-id="110a1-1604">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1604">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="110a1-1605">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="110a1-1605">Az.ContainerRegistry</span></span>
* <span data-ttu-id="110a1-1606">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1606">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="110a1-1607">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="110a1-1607">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-1608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-1608">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-1609">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1609">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="110a1-1610">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1610">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="110a1-1611">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="110a1-1611">Az.EventHub</span></span>
* <span data-ttu-id="110a1-1612">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="110a1-1612">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="110a1-1613">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1613">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-1614">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-1614">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-1615">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1615">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="110a1-1616">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="110a1-1616">Az.LogicApp</span></span>
* <span data-ttu-id="110a1-1617">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="110a1-1617">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="110a1-1618">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1618">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="110a1-1619">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="110a1-1619">Az.ManagedServices</span></span>
* <span data-ttu-id="110a1-1620">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="110a1-1620">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1621">Az.Network</span></span>
* <span data-ttu-id="110a1-1622">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1622">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="110a1-1623">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-1623">New cmdlets</span></span>
        - <span data-ttu-id="110a1-1624">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="110a1-1624">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="110a1-1625">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="110a1-1625">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="110a1-1626">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1626">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="110a1-1627">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1627">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="110a1-1628">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1628">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="110a1-1629">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1629">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="110a1-1630">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="110a1-1630">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="110a1-1631">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="110a1-1631">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="110a1-1632">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="110a1-1632">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="110a1-1633">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1633">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="110a1-1634">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1634">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="110a1-1635">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1635">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="110a1-1636">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1636">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="110a1-1637">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1637">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="110a1-1638">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1638">Updated cmdlets</span></span>
        - <span data-ttu-id="110a1-1639">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1639">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="110a1-1640">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1640">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="110a1-1641">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1641">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="110a1-1642">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1642">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="110a1-1643">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1643">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="110a1-1644">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1644">Updated cmdlet:</span></span>
        - <span data-ttu-id="110a1-1645">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1645">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="110a1-1646">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1646">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="110a1-1647">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1647">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="110a1-1648">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1648">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="110a1-1649">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1649">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="110a1-1650">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="110a1-1650">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-1651">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-1651">Az.OperationalInsights</span></span>
* <span data-ttu-id="110a1-1652">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1652">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="110a1-1653">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1653">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-1654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-1654">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-1655">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1655">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="110a1-1656">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1656">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="110a1-1657">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1657">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="110a1-1658">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1658">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="110a1-1659">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1659">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="110a1-1660">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1660">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="110a1-1661">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1661">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="110a1-1662">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1662">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="110a1-1663">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1663">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="110a1-1664">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1664">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-1665">Az.Resources</span></span>
- <span data-ttu-id="110a1-1666">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1666">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="110a1-1667">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1667">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="110a1-1668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="110a1-1668">Az.ServiceBus</span></span>
* <span data-ttu-id="110a1-1669">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="110a1-1669">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="110a1-1670">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1670">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1671">Az.Sql</span></span>
* <span data-ttu-id="110a1-1672">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1672">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="110a1-1673">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1673">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="110a1-1674">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1674">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-1675">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-1675">Az.Storage</span></span>
* <span data-ttu-id="110a1-1676">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1676">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="110a1-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="110a1-1677">Az.StorageSync</span></span>
* <span data-ttu-id="110a1-1678">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1678">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="110a1-1679">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1679">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-1680">Az.Websites</span></span>
* <span data-ttu-id="110a1-1681">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1681">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="110a1-1682">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1682">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="110a1-1683">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1683">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="110a1-1684">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1684">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-1685">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-1685">Az.Accounts</span></span>
* <span data-ttu-id="110a1-1686">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1686">Add support for profile cmdlets</span></span>
* <span data-ttu-id="110a1-1687">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1687">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="110a1-1688">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1688">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="110a1-1689">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="110a1-1689">Az.Advisor</span></span>
* <span data-ttu-id="110a1-1690">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-1690">GA release of Az.Advisor</span></span>
* <span data-ttu-id="110a1-1691">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="110a1-1691">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="110a1-1692">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-1692">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-1693">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1693">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="110a1-1694">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="110a1-1694">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="110a1-1695">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1695">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="110a1-1696">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="110a1-1696">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="110a1-1697">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="110a1-1697">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="110a1-1698">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="110a1-1698">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="110a1-1699">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1699">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-1700">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-1700">Az.Automation</span></span>
* <span data-ttu-id="110a1-1701">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1701">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1702">Az.Compute</span></span>
* <span data-ttu-id="110a1-1703">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1703">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-1704">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-1704">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-1705">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1705">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="110a1-1706">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="110a1-1706">Az.EventGrid</span></span>
* <span data-ttu-id="110a1-1707">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1707">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-1708">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-1708">Az.IotHub</span></span>
* <span data-ttu-id="110a1-1709">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1709">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1710">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1710">Az.Network</span></span>
* <span data-ttu-id="110a1-1711">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1711">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="110a1-1712">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1712">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="110a1-1713">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-1713">Az.PolicyInsights</span></span>
* <span data-ttu-id="110a1-1714">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1714">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="110a1-1715">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="110a1-1715">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-1716">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-1716">Az.OperationalInsights</span></span>
* <span data-ttu-id="110a1-1717">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1717">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-1718">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-1718">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-1719">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="110a1-1719">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-1720">Az.Resources</span></span>
    - <span data-ttu-id="110a1-1721">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="110a1-1721">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="110a1-1722">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1722">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="110a1-1723">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1723">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="110a1-1724">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1724">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="110a1-1725">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="110a1-1725">Az.ServiceBus</span></span>
* <span data-ttu-id="110a1-1726">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1726">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1727">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1727">Az.Sql</span></span>
* <span data-ttu-id="110a1-1728">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1728">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="110a1-1729">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1729">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="110a1-1730">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="110a1-1730">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="110a1-1731">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="110a1-1731">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="110a1-1732">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="110a1-1732">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="110a1-1733">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="110a1-1733">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="110a1-1734">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="110a1-1734">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="110a1-1735">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="110a1-1735">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="110a1-1736">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1736">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-1737">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-1737">Az.Storage</span></span>
* <span data-ttu-id="110a1-1738">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1738">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="110a1-1739">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="110a1-1739">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="110a1-1740">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1740">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="110a1-1741">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="110a1-1741">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="110a1-1742">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1742">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="110a1-1743">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-1743">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="110a1-1744">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-1744">Set-AzStorageAccount</span></span>
* <span data-ttu-id="110a1-1745">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1745">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="110a1-1746">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="110a1-1746">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="110a1-1747">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="110a1-1747">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="110a1-1748">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="110a1-1748">Az.StorageSync</span></span>
* <span data-ttu-id="110a1-1749">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="110a1-1749">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="110a1-1750">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1750">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-1751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-1751">Az.Accounts</span></span>
* <span data-ttu-id="110a1-1752">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1752">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="110a1-1753">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="110a1-1753">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="110a1-1754">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1754">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="110a1-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="110a1-1755">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="110a1-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="110a1-1756">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1757">Az.Compute</span></span>
* <span data-ttu-id="110a1-1758">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1758">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="110a1-1759">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1759">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="110a1-1760">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="110a1-1760">Az.Dns</span></span>
* <span data-ttu-id="110a1-1761">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1761">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="110a1-1762">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="110a1-1762">Az.EventGrid</span></span>
* <span data-ttu-id="110a1-1763">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1763">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="110a1-1764">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="110a1-1764">New cmdlets:</span></span>
    - <span data-ttu-id="110a1-1765">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="110a1-1765">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="110a1-1766">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="110a1-1766">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="110a1-1767">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="110a1-1767">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="110a1-1768">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="110a1-1768">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="110a1-1769">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="110a1-1769">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="110a1-1770">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="110a1-1770">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="110a1-1771">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="110a1-1771">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="110a1-1772">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="110a1-1772">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="110a1-1773">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="110a1-1773">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="110a1-1774">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="110a1-1774">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="110a1-1775">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="110a1-1775">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="110a1-1776">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="110a1-1776">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="110a1-1777">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="110a1-1777">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="110a1-1778">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="110a1-1778">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="110a1-1779">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="110a1-1779">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="110a1-1780">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="110a1-1780">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="110a1-1781">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1781">Updated cmdlets:</span></span>
    - <span data-ttu-id="110a1-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="110a1-1782">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="110a1-1783">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-1783">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="110a1-1784">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-1784">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="110a1-1785">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-1785">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="110a1-1786">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1786">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="110a1-1787">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="110a1-1787">Event subscription expiration date,</span></span>
            - <span data-ttu-id="110a1-1788">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="110a1-1788">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="110a1-1789">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-1789">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="110a1-1790">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="110a1-1790">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="110a1-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="110a1-1791">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="110a1-1792">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-1792">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="110a1-1793">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="110a1-1793">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="110a1-1794">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-1794">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="110a1-1795">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-1795">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="110a1-1796">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="110a1-1796">Az.FrontDoor</span></span>
* <span data-ttu-id="110a1-1797">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="110a1-1797">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="110a1-1798">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="110a1-1798">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="110a1-1799">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="110a1-1799">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="110a1-1800">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="110a1-1800">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1801">Az.Network</span></span>
* <span data-ttu-id="110a1-1802">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="110a1-1802">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="110a1-1803">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-1803">New cmdlets</span></span>
        - <span data-ttu-id="110a1-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="110a1-1804">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="110a1-1805">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="110a1-1805">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="110a1-1806">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-1806">New cmdlets</span></span>
        - <span data-ttu-id="110a1-1807">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="110a1-1807">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="110a1-1808">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="110a1-1808">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="110a1-1809">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-1809">New cmdlets</span></span>
        - <span data-ttu-id="110a1-1810">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="110a1-1810">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="110a1-1811">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="110a1-1811">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="110a1-1812">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="110a1-1812">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="110a1-1813">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-1813">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="110a1-1814">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1814">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="110a1-1815">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="110a1-1815">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="110a1-1816">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-1816">New cmdlets</span></span>
        - <span data-ttu-id="110a1-1817">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="110a1-1817">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="110a1-1818">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="110a1-1818">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="110a1-1819">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="110a1-1819">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="110a1-1820">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="110a1-1820">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="110a1-1821">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="110a1-1821">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="110a1-1822">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1822">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="110a1-1823">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1823">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="110a1-1824">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1824">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="110a1-1825">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1825">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="110a1-1826">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1826">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="110a1-1827">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1827">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="110a1-1828">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1828">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="110a1-1829">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1829">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="110a1-1830">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1830">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="110a1-1831">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1831">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="110a1-1832">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1832">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="110a1-1833">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1833">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="110a1-1834">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1834">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="110a1-1835">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1835">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="110a1-1836">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1836">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="110a1-1837">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1837">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="110a1-1838">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="110a1-1838">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="110a1-1839">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="110a1-1839">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="110a1-1840">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1840">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="110a1-1841">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1841">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="110a1-1842">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1842">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="110a1-1843">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1843">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-1844">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-1844">Az.OperationalInsights</span></span>
* <span data-ttu-id="110a1-1845">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1845">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-1846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-1846">Az.Resources</span></span>
* <span data-ttu-id="110a1-1847">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="110a1-1847">Support for additional Template Export options</span></span>
    - <span data-ttu-id="110a1-1848">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1848">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="110a1-1849">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1849">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="110a1-1850">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1850">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="110a1-1851">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-1851">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-1852">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1852">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1853">Az.Sql</span></span>
* <span data-ttu-id="110a1-1854">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1854">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="110a1-1855">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1855">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="110a1-1856">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-1856">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="110a1-1857">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="110a1-1857">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="110a1-1858">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="110a1-1858">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="110a1-1859">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="110a1-1859">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="110a1-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="110a1-1860">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="110a1-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="110a1-1861">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-1862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-1862">Az.Storage</span></span>
* <span data-ttu-id="110a1-1863">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="110a1-1863">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="110a1-1864">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-1864">New-AzStorageAccount</span></span>
* <span data-ttu-id="110a1-1865">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1865">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="110a1-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="110a1-1866">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-1867">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-1867">Az.Websites</span></span>
* <span data-ttu-id="110a1-1868">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="110a1-1868">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="110a1-1869">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="110a1-1869">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="110a1-1870">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1870">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="110a1-1871">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="110a1-1871">Az.Cdn</span></span>
* <span data-ttu-id="110a1-1872">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1872">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1873">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1873">Az.Compute</span></span>
* <span data-ttu-id="110a1-1874">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1874">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="110a1-1875">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="110a1-1875">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="110a1-1876">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="110a1-1876">Az.EventHub</span></span>
* <span data-ttu-id="110a1-1877">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="110a1-1877">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="110a1-1878">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="110a1-1878">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1879">Az.Network</span></span>
* <span data-ttu-id="110a1-1880">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1880">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="110a1-1881">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1881">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="110a1-1882">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-1882">Az.PolicyInsights</span></span>
* <span data-ttu-id="110a1-1883">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1883">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-1884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-1884">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-1885">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1885">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="110a1-1886">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="110a1-1886">Az.ServiceBus</span></span>
* <span data-ttu-id="110a1-1887">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="110a1-1887">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="110a1-1888">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-1888">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-1889">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1889">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="110a1-1890">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1890">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1891">Az.Sql</span></span>
* <span data-ttu-id="110a1-1892">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1892">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="110a1-1893">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1893">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="110a1-1894">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-1894">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="110a1-1895">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="110a1-1895">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-1896">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-1896">Az.Websites</span></span>
* <span data-ttu-id="110a1-1897">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1897">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="110a1-1898">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-1898">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="110a1-1899">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-1899">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-1900">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-1900">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="110a1-1901">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="110a1-1901">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="110a1-1902">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="110a1-1902">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="110a1-1903">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="110a1-1903">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="110a1-1904">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="110a1-1904">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="110a1-1905">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="110a1-1905">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="110a1-1906">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="110a1-1906">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="110a1-1907">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="110a1-1907">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="110a1-1908">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-1908">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="110a1-1909">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="110a1-1909">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="110a1-1910">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="110a1-1910">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="110a1-1911">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="110a1-1911">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="110a1-1912">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="110a1-1912">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="110a1-1913">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-1913">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="110a1-1914">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="110a1-1914">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="110a1-1915">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="110a1-1915">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="110a1-1916">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="110a1-1916">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="110a1-1917">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="110a1-1917">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="110a1-1918">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="110a1-1918">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="110a1-1919">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="110a1-1919">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="110a1-1920">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-1920">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="110a1-1921">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="110a1-1921">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="110a1-1922">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="110a1-1922">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="110a1-1923">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1923">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="110a1-1924">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1924">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="110a1-1925">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1925">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="110a1-1926">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="110a1-1926">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="110a1-1927">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-1927">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="110a1-1928">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1928">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="110a1-1929">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1929">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="110a1-1930">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1930">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="110a1-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="110a1-1931">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="110a1-1932">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1932">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="110a1-1933">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1933">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="110a1-1934">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="110a1-1934">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="110a1-1935">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="110a1-1935">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="110a1-1936">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="110a1-1936">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="110a1-1937">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1937">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="110a1-1938">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1938">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="110a1-1939">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1939">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="110a1-1940">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="110a1-1940">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="110a1-1941">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="110a1-1941">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="110a1-1942">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="110a1-1942">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="110a1-1943">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1943">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="110a1-1944">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1944">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="110a1-1945">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="110a1-1945">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="110a1-1946">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="110a1-1946">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="110a1-1947">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="110a1-1947">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="110a1-1948">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1948">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="110a1-1949">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="110a1-1949">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="110a1-1950">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="110a1-1950">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="110a1-1951">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="110a1-1951">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="110a1-1952">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="110a1-1952">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="110a1-1953">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1953">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="110a1-1954">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="110a1-1954">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="110a1-1955">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="110a1-1955">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="110a1-1956">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1956">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="110a1-1957">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="110a1-1957">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="110a1-1958">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="110a1-1958">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="110a1-1959">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1959">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="110a1-1960">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1960">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="110a1-1961">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="110a1-1961">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="110a1-1962">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="110a1-1962">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="110a1-1963">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1963">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="110a1-1964">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1964">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="110a1-1965">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="110a1-1965">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="110a1-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="110a1-1966">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="110a1-1967">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="110a1-1967">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="110a1-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="110a1-1968">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="110a1-1969">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="110a1-1969">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="110a1-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="110a1-1970">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="110a1-1971">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="110a1-1971">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="110a1-1972">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="110a1-1972">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="110a1-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="110a1-1973">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="110a1-1974">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="110a1-1974">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="110a1-1975">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="110a1-1975">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="110a1-1976">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="110a1-1976">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-1977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-1977">Az.Automation</span></span>
* <span data-ttu-id="110a1-1978">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1978">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="110a1-1979">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1979">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="110a1-1980">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1980">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="110a1-1981">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1981">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="110a1-1982">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1982">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="110a1-1983">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1983">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="110a1-1984">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-1984">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-1985">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-1985">Az.Compute</span></span>
* <span data-ttu-id="110a1-1986">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-1986">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="110a1-1987">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="110a1-1987">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-1989">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1989">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-1990">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-1990">Az.Monitor</span></span>
* <span data-ttu-id="110a1-1991">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1991">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-1992">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-1992">Az.Network</span></span>
* <span data-ttu-id="110a1-1993">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1993">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="110a1-1994">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="110a1-1994">Updated cmdlet:</span></span>
        - <span data-ttu-id="110a1-1995">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="110a1-1995">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="110a1-1996">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-1996">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-1997">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-1997">Az.Resources</span></span>
* <span data-ttu-id="110a1-1998">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-1998">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-1999">Az.Sql</span></span>
* <span data-ttu-id="110a1-2000">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="110a1-2000">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="110a1-2001">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2001">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-2002">Az.Accounts</span></span>
* <span data-ttu-id="110a1-2003">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="110a1-2003">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-2004">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2004">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-2005">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="110a1-2005">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="110a1-2006">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="110a1-2006">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2007">Az.Compute</span></span>
* <span data-ttu-id="110a1-2008">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="110a1-2008">Proximity placement group feature.</span></span>
    - <span data-ttu-id="110a1-2009">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="110a1-2009">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="110a1-2010">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-2010">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="110a1-2011">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2011">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="110a1-2012">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-2012">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="110a1-2013">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2013">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="110a1-2014">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="110a1-2014">Breaking changes</span></span>
    - <span data-ttu-id="110a1-2015">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2015">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="110a1-2016">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2016">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="110a1-2017">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="110a1-2017">Az.DeploymentManager</span></span>
* <span data-ttu-id="110a1-2018">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="110a1-2018">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="110a1-2019">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="110a1-2019">Az.Dns</span></span>
* <span data-ttu-id="110a1-2020">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="110a1-2020">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="110a1-2021">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="110a1-2021">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="110a1-2022">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-2022">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="110a1-2023">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="110a1-2023">Az.FrontDoor</span></span>
* <span data-ttu-id="110a1-2024">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="110a1-2024">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="110a1-2025">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="110a1-2025">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="110a1-2026">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-2026">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-2027">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="110a1-2027">Removed two cmdlets:</span></span>
    - <span data-ttu-id="110a1-2028">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="110a1-2028">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="110a1-2029">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="110a1-2029">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="110a1-2030">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2030">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="110a1-2031">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="110a1-2031">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="110a1-2032">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="110a1-2032">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="110a1-2033">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="110a1-2033">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-2034">Az.Monitor</span></span>
* <span data-ttu-id="110a1-2035">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="110a1-2035">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="110a1-2036">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="110a1-2036">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="110a1-2037">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="110a1-2037">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="110a1-2038">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="110a1-2038">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="110a1-2039">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="110a1-2039">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="110a1-2040">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="110a1-2040">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="110a1-2041">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="110a1-2041">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="110a1-2042">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="110a1-2042">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="110a1-2043">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="110a1-2043">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="110a1-2044">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="110a1-2044">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="110a1-2045">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="110a1-2045">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="110a1-2046">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="110a1-2046">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="110a1-2047">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="110a1-2047">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="110a1-2048">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2048">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-2049">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2049">Az.Network</span></span>
* <span data-ttu-id="110a1-2050">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="110a1-2050">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="110a1-2051">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-2051">New cmdlets</span></span>
        - <span data-ttu-id="110a1-2052">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="110a1-2052">New-AzNatGateway</span></span>
        - <span data-ttu-id="110a1-2053">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="110a1-2053">Get-AzNatGateway</span></span>
        - <span data-ttu-id="110a1-2054">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="110a1-2054">Set-AzNatGateway</span></span>
        - <span data-ttu-id="110a1-2055">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="110a1-2055">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="110a1-2056">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2056">Updated cmdlets</span></span>
        - <span data-ttu-id="110a1-2057">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="110a1-2057">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="110a1-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="110a1-2058">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="110a1-2059">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="110a1-2059">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="110a1-2060">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2060">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="110a1-2061">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2061">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="110a1-2062">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-2062">Az.PolicyInsights</span></span>
* <span data-ttu-id="110a1-2063">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-2063">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="110a1-2064">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="110a1-2064">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="110a1-2065">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="110a1-2065">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-2066">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2066">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-2067">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-2067">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="110a1-2068">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="110a1-2068">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="110a1-2069">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="110a1-2069">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="110a1-2070">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="110a1-2070">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="110a1-2071">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="110a1-2071">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="110a1-2072">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="110a1-2072">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="110a1-2073">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="110a1-2073">Az.Relay</span></span>
* <span data-ttu-id="110a1-2074">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="110a1-2074">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="110a1-2075">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="110a1-2075">Az.ServiceBus</span></span>
* <span data-ttu-id="110a1-2076">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2076">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-2077">Az.Storage</span></span>
* <span data-ttu-id="110a1-2078">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="110a1-2078">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="110a1-2079">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="110a1-2079">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="110a1-2080">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="110a1-2080">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="110a1-2081">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-2081">New-AzStorageAccount</span></span>
* <span data-ttu-id="110a1-2082">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="110a1-2082">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="110a1-2083">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-2083">New-AzStorageAccount</span></span>
    - <span data-ttu-id="110a1-2084">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-2084">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="110a1-2085">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-2085">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-2086">Az.Websites</span></span>
* <span data-ttu-id="110a1-2087">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="110a1-2087">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="110a1-2088">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2088">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="110a1-2089">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2089">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="110a1-2090">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="110a1-2090">Highlights since the last major release</span></span>
* <span data-ttu-id="110a1-2091">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-2091">General availability of `Az` module</span></span>
* <span data-ttu-id="110a1-2092">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="110a1-2092">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="110a1-2093">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="110a1-2093">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="110a1-2094">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2094">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="110a1-2095">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2095">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="110a1-2096">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2096">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="110a1-2097">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-2097">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-2098">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-2098">Az.Accounts</span></span>
* <span data-ttu-id="110a1-2099">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2099">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="110a1-2100">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="110a1-2100">Az.Batch</span></span>
* <span data-ttu-id="110a1-2101">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2101">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="110a1-2102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="110a1-2102">Az.Cdn</span></span>
* <span data-ttu-id="110a1-2103">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2103">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-2104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2104">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-2105">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2105">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2106">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2106">Az.Compute</span></span>
* <span data-ttu-id="110a1-2107">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2107">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="110a1-2108">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2108">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="110a1-2109">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2109">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-2110">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-2110">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-2111">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2111">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-2112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-2112">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-2113">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="110a1-2114">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="110a1-2114">Az.EventGrid</span></span>
* <span data-ttu-id="110a1-2115">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2115">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="110a1-2116">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="110a1-2116">Az.EventHub</span></span>
* <span data-ttu-id="110a1-2117">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2117">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="110a1-2118">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="110a1-2118">Az.HDInsight</span></span>
* <span data-ttu-id="110a1-2119">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-2120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-2120">Az.IotHub</span></span>
* <span data-ttu-id="110a1-2121">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-2122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-2122">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-2123">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="110a1-2124">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2124">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="110a1-2125">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="110a1-2125">Az.MachineLearning</span></span>
* <span data-ttu-id="110a1-2126">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="110a1-2127">Az.Media</span><span class="sxs-lookup"><span data-stu-id="110a1-2127">Az.Media</span></span>
* <span data-ttu-id="110a1-2128">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-2129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-2129">Az.Monitor</span></span>
  * <span data-ttu-id="110a1-2130">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="110a1-2130">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="110a1-2131">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="110a1-2131">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="110a1-2132">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="110a1-2132">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="110a1-2133">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="110a1-2133">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="110a1-2134">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="110a1-2134">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="110a1-2135">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="110a1-2135">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="110a1-2136">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2136">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-2137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2137">Az.Network</span></span>
* <span data-ttu-id="110a1-2138">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="110a1-2139">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2139">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="110a1-2140">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="110a1-2140">Az.NotificationHubs</span></span>
* <span data-ttu-id="110a1-2141">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-2142">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-2142">Az.OperationalInsights</span></span>
* <span data-ttu-id="110a1-2143">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="110a1-2144">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="110a1-2144">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="110a1-2145">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2145">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-2146">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2146">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-2147">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2147">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="110a1-2148">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="110a1-2148">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="110a1-2149">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2149">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="110a1-2150">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2150">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="110a1-2151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="110a1-2151">Az.RedisCache</span></span>
* <span data-ttu-id="110a1-2152">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2153">Az.Resources</span></span>
* <span data-ttu-id="110a1-2154">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2154">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2155">Az.Sql</span></span>
* <span data-ttu-id="110a1-2156">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2156">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="110a1-2157">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="110a1-2158">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2158">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="110a1-2159">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2159">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="110a1-2160">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2160">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="110a1-2161">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-2161">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="110a1-2162">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2162">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-2163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-2163">Az.Websites</span></span>
* <span data-ttu-id="110a1-2164">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2164">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="110a1-2165">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="110a1-2166">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2166">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="110a1-2167">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2167">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="110a1-2168">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2168">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="110a1-2169">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="110a1-2169">Highlights since the last major release</span></span>
* <span data-ttu-id="110a1-2170">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-2170">General availability of `Az` module</span></span>
* <span data-ttu-id="110a1-2171">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="110a1-2171">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="110a1-2172">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="110a1-2172">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="110a1-2173">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2173">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="110a1-2174">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2174">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="110a1-2175">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2175">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="110a1-2176">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-2176">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="110a1-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-2177">Az.Accounts</span></span>
* <span data-ttu-id="110a1-2178">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2178">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="110a1-2179">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2179">Az.AnalysisServices</span></span>
* <span data-ttu-id="110a1-2180">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="110a1-2180">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="110a1-2181">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="110a1-2181">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-2182">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-2182">Az.Automation</span></span>
* <span data-ttu-id="110a1-2183">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2183">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="110a1-2184">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-2184">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="110a1-2185">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="110a1-2185">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2186">Az.Compute</span></span>
* <span data-ttu-id="110a1-2187">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2187">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="110a1-2188">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2188">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="110a1-2189">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="110a1-2189">Az.ContainerInstance</span></span>
* <span data-ttu-id="110a1-2190">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2190">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-2191">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-2191">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-2192">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2192">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="110a1-2193">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2193">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2194">Az.Resources</span></span>
* <span data-ttu-id="110a1-2195">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2195">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="110a1-2196">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2196">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="110a1-2197">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2197">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="110a1-2198">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="110a1-2198">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="110a1-2199">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2199">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="110a1-2200">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="110a1-2200">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-2201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2201">Az.Sql</span></span>
* <span data-ttu-id="110a1-2202">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-2202">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-2203">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-2203">Az.Storage</span></span>
* <span data-ttu-id="110a1-2204">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="110a1-2204">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="110a1-2205">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="110a1-2205">New-AzStorageContext</span></span>
* <span data-ttu-id="110a1-2206">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-2206">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="110a1-2207">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="110a1-2207">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="110a1-2208">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="110a1-2208">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="110a1-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="110a1-2209">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="110a1-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="110a1-2210">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="110a1-2211">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-2211">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="110a1-2212">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="110a1-2212">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="110a1-2213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="110a1-2213">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="110a1-2214">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="110a1-2214">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="110a1-2215">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="110a1-2215">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="110a1-2216">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2216">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="110a1-2217">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="110a1-2217">Highlights since the last major release</span></span>
* <span data-ttu-id="110a1-2218">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-2218">General availability of `Az` module</span></span>
* <span data-ttu-id="110a1-2219">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="110a1-2219">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="110a1-2220">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="110a1-2220">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="110a1-2221">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2221">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="110a1-2222">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2222">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="110a1-2223">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2223">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="110a1-2224">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-2224">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-2225">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-2225">Az.Automation</span></span>
* <span data-ttu-id="110a1-2226">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="110a1-2226">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="110a1-2227">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="110a1-2227">Dynamic grouping</span></span>
    * <span data-ttu-id="110a1-2228">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="110a1-2228">Pre-Post script</span></span>
    * <span data-ttu-id="110a1-2229">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="110a1-2229">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2230">Az.Compute</span></span>
* <span data-ttu-id="110a1-2231">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="110a1-2231">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="110a1-2232">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2232">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-2233">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-2233">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-2234">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2234">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-2235">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2235">Az.Network</span></span>
* <span data-ttu-id="110a1-2236">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2236">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="110a1-2237">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2237">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-2238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2238">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-2239">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2239">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="110a1-2240">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2240">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2241">Az.Resources</span></span>
* <span data-ttu-id="110a1-2242">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2242">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="110a1-2243">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2243">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-2244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2244">Az.Sql</span></span>
* <span data-ttu-id="110a1-2245">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2245">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-2246">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-2246">Az.Storage</span></span>
* <span data-ttu-id="110a1-2247">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-2247">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="110a1-2248">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="110a1-2248">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="110a1-2249">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="110a1-2249">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="110a1-2250">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="110a1-2250">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="110a1-2251">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="110a1-2251">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="110a1-2252">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="110a1-2252">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="110a1-2253">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="110a1-2253">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-2254">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-2254">Az.Websites</span></span>
* <span data-ttu-id="110a1-2255">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2255">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="110a1-2256">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2256">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-2257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-2257">Az.Accounts</span></span>
* <span data-ttu-id="110a1-2258">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2258">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="110a1-2259">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2259">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-2260">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-2260">Az.Automation</span></span>
* <span data-ttu-id="110a1-2261">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2261">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="110a1-2262">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2262">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="110a1-2263">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="110a1-2263">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="110a1-2264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="110a1-2264">Az.Cdn</span></span>
* <span data-ttu-id="110a1-2265">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-2265">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2266">Az.Compute</span></span>
* <span data-ttu-id="110a1-2267">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2267">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-2268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-2268">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-2269">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2269">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="110a1-2270">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="110a1-2270">Az.LogicApp</span></span>
* <span data-ttu-id="110a1-2271">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="110a1-2271">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-2272">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2272">Az.Network</span></span>
* <span data-ttu-id="110a1-2273">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2273">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-2274">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2274">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-2275">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2275">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="110a1-2276">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="110a1-2276">SDK Update</span></span>
* <span data-ttu-id="110a1-2277">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-2277">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="110a1-2278">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2278">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2279">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2279">Az.Resources</span></span>
* <span data-ttu-id="110a1-2280">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2280">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="110a1-2281">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="110a1-2281">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="110a1-2282">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2282">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="110a1-2283">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="110a1-2283">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="110a1-2284">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2284">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="110a1-2285">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="110a1-2285">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-2286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2286">Az.Sql</span></span>
* <span data-ttu-id="110a1-2287">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-2287">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="110a1-2288">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-2288">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-2289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-2289">Az.Storage</span></span>
* <span data-ttu-id="110a1-2290">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="110a1-2290">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="110a1-2291">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2291">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="110a1-2292">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2292">Az.AnalysisServices</span></span>
* <span data-ttu-id="110a1-2293">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-2293">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-2294">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-2294">Az.Automation</span></span>
* <span data-ttu-id="110a1-2295">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2295">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="110a1-2296">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2296">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="110a1-2297">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2297">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-2298">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2298">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-2299">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2299">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2300">Az.Compute</span></span>
* <span data-ttu-id="110a1-2301">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2301">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="110a1-2302">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2302">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="110a1-2303">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2303">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="110a1-2304">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="110a1-2304">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-2305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-2305">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-2306">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2306">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="110a1-2307">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="110a1-2307">Az.EventHub</span></span>
* <span data-ttu-id="110a1-2308">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2308">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-2309">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-2309">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-2310">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2310">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="110a1-2311">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="110a1-2311">Az.LogicApp</span></span>
* <span data-ttu-id="110a1-2312">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2312">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="110a1-2313">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2313">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="110a1-2314">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-2314">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="110a1-2315">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="110a1-2315">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="110a1-2316">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="110a1-2316">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="110a1-2317">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="110a1-2317">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="110a1-2318">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="110a1-2318">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="110a1-2319">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="110a1-2319">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="110a1-2320">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="110a1-2320">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="110a1-2321">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="110a1-2321">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="110a1-2322">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="110a1-2322">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="110a1-2323">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="110a1-2323">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="110a1-2324">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2324">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="110a1-2325">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-2325">Az.Monitor</span></span>
* <span data-ttu-id="110a1-2326">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2326">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-2327">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2327">Az.Network</span></span>
* <span data-ttu-id="110a1-2328">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2328">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="110a1-2330">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="110a1-2330">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="110a1-2331">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2331">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="110a1-2332">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2332">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2333">Az.Resources</span></span>
* <span data-ttu-id="110a1-2334">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2334">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="110a1-2335">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2335">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="110a1-2336">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2336">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="110a1-2337">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2337">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2338">Az.Sql</span></span>
* <span data-ttu-id="110a1-2339">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2339">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="110a1-2340">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2340">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-2341">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-2341">Az.Websites</span></span>
* <span data-ttu-id="110a1-2342">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2342">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="110a1-2343">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2343">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-2344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-2344">Az.Accounts</span></span>
* <span data-ttu-id="110a1-2345">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="110a1-2345">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="110a1-2346">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2346">Az.AnalysisServices</span></span>
<span data-ttu-id="110a1-2347">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="110a1-2347">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2348">Az.Compute</span></span>
* <span data-ttu-id="110a1-2349">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2349">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="110a1-2350">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2350">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="110a1-2351">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2351">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2352">Az.RecoveryServices</span></span>
<span data-ttu-id="110a1-2353">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="110a1-2353">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2354">Az.Resources</span></span>
* <span data-ttu-id="110a1-2355">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2355">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="110a1-2356">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="110a1-2356">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="110a1-2357">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2357">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="110a1-2358">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="110a1-2358">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-2359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2359">Az.Sql</span></span>
* <span data-ttu-id="110a1-2360">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="110a1-2360">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="110a1-2361">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2361">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="110a1-2362">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2362">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="110a1-2363">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2363">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-2364">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-2364">Az.Accounts</span></span>
* <span data-ttu-id="110a1-2365">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="110a1-2365">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="110a1-2366">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2366">Az.AnalysisServices</span></span>
* <span data-ttu-id="110a1-2367">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="110a1-2367">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="110a1-2369">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="110a1-2369">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="110a1-2370">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2370">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-2371">Az.Accounts</span></span>
* <span data-ttu-id="110a1-2372">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2372">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="110a1-2373">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2373">Update incorrect online help URLs</span></span>
* <span data-ttu-id="110a1-2374">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2374">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="110a1-2375">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="110a1-2375">Az.Aks</span></span>
* <span data-ttu-id="110a1-2376">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2376">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="110a1-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-2377">Az.Automation</span></span>
* <span data-ttu-id="110a1-2378">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2378">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="110a1-2379">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2379">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="110a1-2380">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="110a1-2380">Az.Cdn</span></span>
* <span data-ttu-id="110a1-2381">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2381">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2382">Az.Compute</span></span>
* <span data-ttu-id="110a1-2383">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2383">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="110a1-2384">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2384">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="110a1-2385">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2385">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="110a1-2386">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="110a1-2386">Az.ContainerRegistry</span></span>
* <span data-ttu-id="110a1-2387">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2387">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="110a1-2388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="110a1-2388">Az.DataFactory</span></span>
* <span data-ttu-id="110a1-2389">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2389">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-2390">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-2390">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-2391">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2391">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="110a1-2392">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="110a1-2392">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="110a1-2393">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2393">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-2394">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-2394">Az.IotHub</span></span>
* <span data-ttu-id="110a1-2395">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2395">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="110a1-2396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-2396">Az.KeyVault</span></span>
* <span data-ttu-id="110a1-2397">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2397">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-2398">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2398">Az.Network</span></span>
* <span data-ttu-id="110a1-2399">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2399">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2400">Az.Resources</span></span>
* <span data-ttu-id="110a1-2401">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2401">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="110a1-2402">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2402">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="110a1-2403">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2403">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="110a1-2404">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2404">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="110a1-2405">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2405">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="110a1-2406">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2406">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="110a1-2407">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="110a1-2407">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="110a1-2408">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-2408">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-2409">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="110a1-2409">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="110a1-2410">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2410">Fix some error messages.</span></span>
* <span data-ttu-id="110a1-2411">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2411">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="110a1-2412">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2412">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="110a1-2413">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="110a1-2413">Az.SignalR</span></span>
* <span data-ttu-id="110a1-2414">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2414">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-2415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2415">Az.Sql</span></span>
* <span data-ttu-id="110a1-2416">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2416">Update incorrect online help URLs</span></span>
* <span data-ttu-id="110a1-2417">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2417">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="110a1-2418">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2418">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="110a1-2419">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-2419">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-2420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-2420">Az.Storage</span></span>
* <span data-ttu-id="110a1-2421">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2421">Update incorrect online help URLs</span></span>
* <span data-ttu-id="110a1-2422">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-2422">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="110a1-2423">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="110a1-2423">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="110a1-2424">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="110a1-2424">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="110a1-2425">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="110a1-2425">Az.TrafficManager</span></span>
* <span data-ttu-id="110a1-2426">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2426">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-2427">Az.Websites</span></span>
* <span data-ttu-id="110a1-2428">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="110a1-2429">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2429">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="110a1-2430">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2430">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="110a1-2431">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="110a1-2431">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="110a1-2432">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-2432">Az.Accounts</span></span>
* <span data-ttu-id="110a1-2433">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2433">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2434">Az.Compute</span></span>
* <span data-ttu-id="110a1-2435">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="110a1-2435">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="110a1-2436">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2436">Updated the description of ID in help files</span></span>
* <span data-ttu-id="110a1-2437">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="110a1-2437">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-2438">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-2438">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-2439">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2439">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="110a1-2440">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2440">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="110a1-2441">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="110a1-2441">Az.EventGrid</span></span>
* <span data-ttu-id="110a1-2442">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2442">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="110a1-2443">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2443">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="110a1-2444">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-2444">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="110a1-2445">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="110a1-2445">Event Time-To-Live,</span></span>
        - <span data-ttu-id="110a1-2446">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="110a1-2446">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="110a1-2447">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="110a1-2447">Dead letter endpoint.</span></span>
    - <span data-ttu-id="110a1-2448">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-2448">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="110a1-2449">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="110a1-2449">Event Time-To-Live,</span></span>
        - <span data-ttu-id="110a1-2450">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="110a1-2450">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="110a1-2451">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="110a1-2451">Dead letter endpoint.</span></span>
* <span data-ttu-id="110a1-2452">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2452">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="110a1-2453">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-2453">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="110a1-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="110a1-2454">Az.IotHub</span></span>
* <span data-ttu-id="110a1-2455">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2455">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="110a1-2456">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="110a1-2456">Az.LogicApp</span></span>
* <span data-ttu-id="110a1-2457">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="110a1-2457">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2458">Az.Resources</span></span>
* <span data-ttu-id="110a1-2459">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2459">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="110a1-2460">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="110a1-2460">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="110a1-2461">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2461">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="110a1-2462">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2462">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="110a1-2463">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2463">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="110a1-2464">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="110a1-2464">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="110a1-2465">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="110a1-2465">Az.SignalR</span></span>
* <span data-ttu-id="110a1-2466">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="110a1-2466">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-2467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2467">Az.Sql</span></span>
* <span data-ttu-id="110a1-2468">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="110a1-2468">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="110a1-2469">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-2469">Az.Storage</span></span>
* <span data-ttu-id="110a1-2470">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="110a1-2470">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="110a1-2471">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="110a1-2471">New-AzStorageContext</span></span>
* <span data-ttu-id="110a1-2472">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2472">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="110a1-2473">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="110a1-2473">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-2474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-2474">Az.Websites</span></span>
* <span data-ttu-id="110a1-2475">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2475">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="110a1-2476">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="110a1-2476">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="110a1-2477">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="110a1-2477">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="110a1-2478">Genel</span><span class="sxs-lookup"><span data-stu-id="110a1-2478">General</span></span>

- <span data-ttu-id="110a1-2479">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-2479">General Availability of Az Module</span></span>
- <span data-ttu-id="110a1-2480">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="110a1-2480">Online help for each module</span></span>
- <span data-ttu-id="110a1-2481">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="110a1-2481">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="110a1-2482">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2482">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="110a1-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="110a1-2483">Az.Accounts</span></span>
- <span data-ttu-id="110a1-2484">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="110a1-2484">Changed from Az.Profile</span></span>
- <span data-ttu-id="110a1-2485">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2485">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="110a1-2486">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-2486">Az.ApiManagement</span></span>
- <span data-ttu-id="110a1-2487">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="110a1-2487">Fixes for #7002</span></span>
- <span data-ttu-id="110a1-2488">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2488">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="110a1-2489">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="110a1-2489">Az.Batch</span></span>
- <span data-ttu-id="110a1-2490">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2490">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="110a1-2491">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="110a1-2491">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="110a1-2492">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2492">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="110a1-2493">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="110a1-2493">Az.Billing</span></span>
- <span data-ttu-id="110a1-2494">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2494">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="110a1-2495">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2495">Az.CognitivServices</span></span>
- <span data-ttu-id="110a1-2496">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2496">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="110a1-2497">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-2497">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="110a1-2498">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="110a1-2498">Az.ContainerInstance</span></span>
- <span data-ttu-id="110a1-2499">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2499">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="110a1-2500">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="110a1-2500">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="110a1-2501">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2501">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="110a1-2502">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-2502">Az.DataLakeStore</span></span>
- <span data-ttu-id="110a1-2503">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="110a1-2504">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="110a1-2504">Az.Monitor</span></span>
- <span data-ttu-id="110a1-2505">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2505">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="110a1-2506">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="110a1-2506">Az.KeyVault</span></span>
- <span data-ttu-id="110a1-2507">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-2507">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="110a1-2508">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="110a1-2508">Az.MachineLearning</span></span>
- <span data-ttu-id="110a1-2509">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2509">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="110a1-2510">Az.Media</span><span class="sxs-lookup"><span data-stu-id="110a1-2510">Az.Media</span></span>
- <span data-ttu-id="110a1-2511">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="110a1-2511">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="110a1-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2512">Az.Network</span></span>
<span data-ttu-id="110a1-2513">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2513">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="110a1-2514">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="110a1-2514">New cmdlets added:</span></span>
        - <span data-ttu-id="110a1-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110a1-2515">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="110a1-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110a1-2516">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="110a1-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110a1-2517">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="110a1-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110a1-2518">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="110a1-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="110a1-2519">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="110a1-2520">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="110a1-2520">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="110a1-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="110a1-2521">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="110a1-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="110a1-2522">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="110a1-2523">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2523">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="110a1-2524">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="110a1-2524">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="110a1-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="110a1-2525">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="110a1-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="110a1-2526">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="110a1-2527">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-2527">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="110a1-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-2528">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="110a1-2529">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2529">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="110a1-2530">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2530">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="110a1-2531">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="110a1-2531">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="110a1-2532">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="110a1-2532">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="110a1-2533">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="110a1-2533">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="110a1-2534">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2534">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="110a1-2535">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="110a1-2536">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-2536">Az.OperationalInsights</span></span>
- <span data-ttu-id="110a1-2537">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="110a1-2538">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="110a1-2538">Az.Profile</span></span>
- <span data-ttu-id="110a1-2539">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2539">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-2540">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2540">Az.RecoveryServices</span></span>
- <span data-ttu-id="110a1-2541">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2541">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="110a1-2542">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2542">Az.Resources</span></span>
- <span data-ttu-id="110a1-2543">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="110a1-2544">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-2544">Az.ServiceFabric</span></span>
- <span data-ttu-id="110a1-2545">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="110a1-2545">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="110a1-2546">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2546">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="110a1-2547">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="110a1-2547">Az.SIgnalR</span></span>
- <span data-ttu-id="110a1-2548">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="110a1-2548">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="110a1-2549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2549">Az.Sql</span></span>
- <span data-ttu-id="110a1-2550">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2550">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="110a1-2551">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2551">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="110a1-2552">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="110a1-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-2553">Az.Storage</span></span>
- <span data-ttu-id="110a1-2554">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="110a1-2555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-2555">Az.Websites</span></span>
- <span data-ttu-id="110a1-2556">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="110a1-2556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="110a1-2557">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="110a1-2557">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="110a1-2558">Genel</span><span class="sxs-lookup"><span data-stu-id="110a1-2558">General</span></span>

* <span data-ttu-id="110a1-2559">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="110a1-2559">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="110a1-2560">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2560">Az.Compute</span></span>

* <span data-ttu-id="110a1-2561">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2561">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="110a1-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-2562">Az.DataLakeStore</span></span>

* <span data-ttu-id="110a1-2563">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2563">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="110a1-2564">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="110a1-2564">Az.FrontDoor</span></span>

* <span data-ttu-id="110a1-2565">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2565">Fixed some broken links</span></span>
    - <span data-ttu-id="110a1-2566">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2566">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="110a1-2567">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2567">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="110a1-2568">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2568">Az.RecoveryServices</span></span>

* <span data-ttu-id="110a1-2569">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2569">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="110a1-2570">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2570">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="110a1-2571">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2571">Az.Resources</span></span>

* <span data-ttu-id="110a1-2572">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="110a1-2572">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="110a1-2573">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2573">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="110a1-2574">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2574">Az.Sql</span></span>

* <span data-ttu-id="110a1-2575">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="110a1-2575">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="110a1-2576">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2576">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="110a1-2577">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2577">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="110a1-2578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="110a1-2578">Az.Storage</span></span>

* <span data-ttu-id="110a1-2579">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2579">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="110a1-2580">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2580">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="110a1-2581">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="110a1-2581">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="110a1-2582">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2582">Support Static Website configuration</span></span>
    - <span data-ttu-id="110a1-2583">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="110a1-2583">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="110a1-2584">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="110a1-2584">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="110a1-2585">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-2585">Az.Websites</span></span>

* <span data-ttu-id="110a1-2586">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="110a1-2586">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="110a1-2587">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2587">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="110a1-2588">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="110a1-2588">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="110a1-2589">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="110a1-2589">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="110a1-2590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="110a1-2590">Az.ApiManagement</span></span>
* <span data-ttu-id="110a1-2591">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="110a1-2591">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="110a1-2592">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="110a1-2592">Az.Automation</span></span>
* <span data-ttu-id="110a1-2593">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="110a1-2593">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="110a1-2594">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2594">Added Update Management cmdlets</span></span>
* <span data-ttu-id="110a1-2595">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2595">Added Source Control cmdlets</span></span>
* <span data-ttu-id="110a1-2596">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2596">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="110a1-2597">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2597">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="110a1-2598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2598">Az.Compute</span></span>
* <span data-ttu-id="110a1-2599">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2599">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="110a1-2600">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="110a1-2600">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="110a1-2601">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="110a1-2601">Az.ContainerInstance</span></span>
* <span data-ttu-id="110a1-2602">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="110a1-2602">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="110a1-2603">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="110a1-2603">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="110a1-2604">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2604">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="110a1-2605">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2605">Az.Network</span></span>
* <span data-ttu-id="110a1-2606">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2606">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="110a1-2607">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2607">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="110a1-2608">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2608">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="110a1-2609">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2609">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="110a1-2610">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="110a1-2610">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="110a1-2611">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2611">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="110a1-2612">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="110a1-2612">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="110a1-2613">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="110a1-2613">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="110a1-2614">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2614">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="110a1-2615">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="110a1-2615">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="110a1-2616">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="110a1-2616">Az.Relay</span></span>
* <span data-ttu-id="110a1-2617">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2617">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="110a1-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2618">Az.Resources</span></span>
* <span data-ttu-id="110a1-2619">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2619">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="110a1-2620">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2620">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="110a1-2621">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="110a1-2621">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="110a1-2622">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-2622">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-2623">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2623">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="110a1-2624">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2624">Az.Sql</span></span>
* <span data-ttu-id="110a1-2625">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2625">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="110a1-2626">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="110a1-2626">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="110a1-2627">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="110a1-2627">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="110a1-2628">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="110a1-2628">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="110a1-2629">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="110a1-2629">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="110a1-2630">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="110a1-2630">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="110a1-2631">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="110a1-2631">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="110a1-2632">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="110a1-2632">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="110a1-2633">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="110a1-2633">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="110a1-2634">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2634">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="110a1-2635">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2635">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="110a1-2636">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2636">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="110a1-2637">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="110a1-2637">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="110a1-2638">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="110a1-2638">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="110a1-2639">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="110a1-2639">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="110a1-2640">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="110a1-2640">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="110a1-2641">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2641">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="110a1-2642">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="110a1-2642">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="110a1-2643">Genel</span><span class="sxs-lookup"><span data-stu-id="110a1-2643">General</span></span>
* <span data-ttu-id="110a1-2644">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="110a1-2644">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="110a1-2645">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="110a1-2645">Az.Profile</span></span>
* <span data-ttu-id="110a1-2646">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2646">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="110a1-2647">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2647">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="110a1-2648">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2648">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="110a1-2649">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2649">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="110a1-2650">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2650">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="110a1-2651">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2651">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="110a1-2652">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2652">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-2653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2653">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-2654">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2654">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2655">Az.Compute</span></span>
* <span data-ttu-id="110a1-2656">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2656">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="110a1-2657">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="110a1-2657">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="110a1-2658">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2658">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-2659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-2659">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-2660">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2660">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="110a1-2661">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2661">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="110a1-2662">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="110a1-2662">Az.Insights</span></span>
* <span data-ttu-id="110a1-2663">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2663">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="110a1-2664">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="110a1-2664">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="110a1-2665">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2665">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="110a1-2666">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="110a1-2666">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-2667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2667">Az.Network</span></span>
* <span data-ttu-id="110a1-2668">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="110a1-2668">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="110a1-2669">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="110a1-2669">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="110a1-2670">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="110a1-2670">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="110a1-2671">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="110a1-2671">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="110a1-2672">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="110a1-2672">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="110a1-2673">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="110a1-2673">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="110a1-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="110a1-2674">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="110a1-2675">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="110a1-2675">Az.PolicyInsights</span></span>
* <span data-ttu-id="110a1-2676">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2676">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2677">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2677">Az.Resources</span></span>
* <span data-ttu-id="110a1-2678">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="110a1-2678">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="110a1-2679">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="110a1-2679">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="110a1-2680">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="110a1-2680">Az.ServiceBus</span></span>
* <span data-ttu-id="110a1-2681">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2681">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="110a1-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="110a1-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="110a1-2683">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2683">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="110a1-2684">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2684">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="110a1-2685">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="110a1-2685">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="110a1-2686">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="110a1-2686">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="110a1-2687">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2687">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="110a1-2688">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="110a1-2688">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="110a1-2689">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="110a1-2689">Az.Profile</span></span>
* <span data-ttu-id="110a1-2690">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="110a1-2690">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="110a1-2691">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2692">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2692">Az.Compute</span></span>
* <span data-ttu-id="110a1-2693">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2693">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="110a1-2694">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2694">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="110a1-2695">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="110a1-2695">Az.DataLakeStore</span></span>
* <span data-ttu-id="110a1-2696">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="110a1-2696">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="110a1-2697">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="110a1-2697">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="110a1-2698">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="110a1-2698">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="110a1-2699">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="110a1-2699">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="110a1-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="110a1-2700">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-2701">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2701">Az.Network</span></span>
* <span data-ttu-id="110a1-2702">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-2702">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="110a1-2703">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2703">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2704">Az.Resources</span></span>
* <span data-ttu-id="110a1-2705">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2705">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="110a1-2706">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2706">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="110a1-2707">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="110a1-2707">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="110a1-2708">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="110a1-2708">Azure.Storage</span></span>
* <span data-ttu-id="110a1-2709">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="110a1-2709">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="110a1-2710">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="110a1-2710">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="110a1-2711">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="110a1-2711">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="110a1-2712">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="110a1-2712">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="110a1-2713">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="110a1-2713">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="110a1-2714">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="110a1-2714">Az.CognitiveServices</span></span>
* <span data-ttu-id="110a1-2715">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="110a1-2715">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="110a1-2716">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="110a1-2716">Az.Compute</span></span>
* <span data-ttu-id="110a1-2717">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2717">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="110a1-2718">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2718">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="110a1-2719">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2719">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="110a1-2720">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="110a1-2720">Az.DataFactoryV2</span></span>
* <span data-ttu-id="110a1-2721">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2721">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="110a1-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="110a1-2722">Az.Network</span></span>
* <span data-ttu-id="110a1-2723">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="110a1-2723">Added NetworkProfile functionality.</span></span> <span data-ttu-id="110a1-2724">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2724">new cmdlets added</span></span>
    - <span data-ttu-id="110a1-2725">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="110a1-2725">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="110a1-2726">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="110a1-2726">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="110a1-2727">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="110a1-2727">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="110a1-2728">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="110a1-2728">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="110a1-2729">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-2729">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="110a1-2730">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="110a1-2730">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="110a1-2731">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2731">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="110a1-2732">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2732">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="110a1-2733">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2733">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="110a1-2734">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="110a1-2734">Az.RedisCache</span></span>
* <span data-ttu-id="110a1-2735">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="110a1-2735">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="110a1-2736">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2736">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="110a1-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="110a1-2737">Az.Resources</span></span>
* <span data-ttu-id="110a1-2738">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="110a1-2738">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="110a1-2739">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2739">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="110a1-2740">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="110a1-2740">Az.Sql</span></span>
* <span data-ttu-id="110a1-2741">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="110a1-2741">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="110a1-2742">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="110a1-2742">Az.Websites</span></span>
* <span data-ttu-id="110a1-2743">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="110a1-2743">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="110a1-2744">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="110a1-2744">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="110a1-2745">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="110a1-2745">0.2.0 - September 2018</span></span>
 <span data-ttu-id="110a1-2746">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="110a1-2746">Initial Release</span></span>
