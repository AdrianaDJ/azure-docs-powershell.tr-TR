---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853466"
---
# <a name="release-notes"></a><span data-ttu-id="6a66d-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="6a66d-103">Release notes</span></span>

<span data-ttu-id="6a66d-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6a66d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="6a66d-105">6.2.0 - Haziran 2018</span><span class="sxs-lookup"><span data-stu-id="6a66d-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6a66d-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a66d-106">AzureRM.Profile</span></span>
* <span data-ttu-id="6a66d-107">Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6a66d-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6a66d-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6a66d-108">AzureRM.Compute</span></span>
* <span data-ttu-id="6a66d-109">VMSS VM Güncelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="6a66d-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6a66d-110">'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6a66d-111">VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="6a66d-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6a66d-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6a66d-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6a66d-113">ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="6a66d-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6a66d-114">Fabrika deposunu yapılandırma işlemi eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6a66d-115">QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6a66d-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6a66d-116">SecretBase’ten Object’e birkaç model türü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6a66d-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6a66d-117">Blob Etkinliklerini tetikleme eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6a66d-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a66d-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6a66d-119">Belgeler örnek çıktı ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6a66d-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6a66d-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6a66d-120">AzureRM.Network</span></span>
* <span data-ttu-id="6a66d-121">Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="6a66d-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6a66d-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6a66d-122">AzureRM.Resources</span></span>
* <span data-ttu-id="6a66d-123">'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6a66d-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6a66d-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6a66d-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6a66d-125">Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6a66d-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6a66d-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6a66d-126">AzureRM.Sql</span></span>
* <span data-ttu-id="6a66d-127">Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="6a66d-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6a66d-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a66d-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6a66d-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6a66d-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6a66d-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6a66d-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6a66d-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6a66d-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6a66d-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a66d-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6a66d-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6a66d-133">AzureRM.Websites</span></span>
* <span data-ttu-id="6a66d-134">'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="6a66d-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6a66d-135">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="6a66d-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6a66d-136">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a66d-136">AzureRM.Profile</span></span>
* <span data-ttu-id="6a66d-137">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="6a66d-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6a66d-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6a66d-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6a66d-139">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6a66d-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6a66d-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6a66d-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6a66d-141">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6a66d-142">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6a66d-143">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6a66d-144">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6a66d-145">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6a66d-146">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6a66d-147">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-147">Added support for MSI identity</span></span>
* <span data-ttu-id="6a66d-148">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="6a66d-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6a66d-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6a66d-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6a66d-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a66d-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6a66d-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6a66d-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6a66d-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6a66d-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6a66d-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6a66d-153">AzureRM.Batch</span></span>
* <span data-ttu-id="6a66d-154">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="6a66d-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6a66d-155">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="6a66d-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6a66d-156">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6a66d-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="6a66d-157">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="6a66d-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6a66d-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a66d-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6a66d-159">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="6a66d-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6a66d-160">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="6a66d-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6a66d-161">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="6a66d-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6a66d-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6a66d-162">AzureRM.Network</span></span>
* <span data-ttu-id="6a66d-163">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="6a66d-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6a66d-164">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6a66d-165">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a66d-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6a66d-166">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="6a66d-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6a66d-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a66d-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6a66d-168">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="6a66d-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6a66d-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a66d-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6a66d-170">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="6a66d-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6a66d-171">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a66d-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6a66d-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a66d-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6a66d-173">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="6a66d-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6a66d-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6a66d-174">AzureRM.Sql</span></span>
* <span data-ttu-id="6a66d-175">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="6a66d-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6a66d-176">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a66d-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6a66d-177">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="6a66d-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6a66d-178">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="6a66d-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6a66d-179">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="6a66d-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6a66d-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a66d-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6a66d-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6a66d-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6a66d-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6a66d-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6a66d-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6a66d-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6a66d-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a66d-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6a66d-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6a66d-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6a66d-186">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="6a66d-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>