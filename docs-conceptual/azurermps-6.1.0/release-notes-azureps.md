---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2018
ms.locfileid: "34462142"
---
# <a name="release-notes"></a><span data-ttu-id="a789d-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="a789d-103">Release notes</span></span>

<span data-ttu-id="a789d-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a789d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="a789d-105">6.1.0 - Mayıs 2018</span><span class="sxs-lookup"><span data-stu-id="a789d-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a789d-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a789d-106">AzureRM.Profile</span></span>
* <span data-ttu-id="a789d-107">'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="a789d-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a789d-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a789d-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a789d-109">AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="a789d-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a789d-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a789d-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a789d-111">ApiVersions, ApiReleases ve ApiRevisions desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a789d-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a789d-112">ServiceFabric Arka Ucu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a789d-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a789d-113">Application Insights Günlükçüsü desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a789d-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a789d-114">‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a789d-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a789d-115">Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a789d-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a789d-116">Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a789d-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a789d-117">MSI kimliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="a789d-117">Added support for MSI identity</span></span>
* <span data-ttu-id="a789d-118">İlkeleri Url ile kabul etme desteği eklendi NOT: Aşağıdaki cmdlet’ler gelecekteki sürümlerde kullanım dışı kalacaktır</span><span class="sxs-lookup"><span data-stu-id="a789d-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a789d-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a789d-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a789d-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a789d-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a789d-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a789d-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a789d-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a789d-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a789d-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a789d-123">AzureRM.Batch</span></span>
* <span data-ttu-id="a789d-124">Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="a789d-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a789d-125">Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama</span><span class="sxs-lookup"><span data-stu-id="a789d-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a789d-126">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a789d-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="a789d-127">Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme</span><span class="sxs-lookup"><span data-stu-id="a789d-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a789d-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a789d-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a789d-129">Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği</span><span class="sxs-lookup"><span data-stu-id="a789d-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a789d-130">Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme</span><span class="sxs-lookup"><span data-stu-id="a789d-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a789d-131">Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="a789d-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a789d-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a789d-132">AzureRM.Network</span></span>
* <span data-ttu-id="a789d-133">Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme</span><span class="sxs-lookup"><span data-stu-id="a789d-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a789d-134">Protokol yapılandırması oluşturma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="a789d-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a789d-135">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a789d-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a789d-136">Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="a789d-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a789d-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a789d-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a789d-138">Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="a789d-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a789d-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a789d-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a789d-140">Bağlantı hattı bağlantısı alma cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="a789d-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a789d-141">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a789d-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a789d-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a789d-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a789d-143">Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)</span><span class="sxs-lookup"><span data-stu-id="a789d-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a789d-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a789d-144">AzureRM.Sql</span></span>
* <span data-ttu-id="a789d-145">AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="a789d-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a789d-146">Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a789d-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a789d-147">komutuna ilişkin sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="a789d-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a789d-148">Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure Sql Database/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a789d-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a789d-149">Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="a789d-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a789d-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a789d-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a789d-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a789d-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a789d-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a789d-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a789d-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a789d-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a789d-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a789d-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a789d-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a789d-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a789d-156">-Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a789d-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>