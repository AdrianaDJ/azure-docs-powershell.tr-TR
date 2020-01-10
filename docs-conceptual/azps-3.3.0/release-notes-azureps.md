---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: fb934ed0f8bef5e2aff715debe5d406d54abf24f
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/07/2020
ms.locfileid: "75718993"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="94e3d-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="94e3d-103">Azure PowerShell release notes</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="94e3d-104">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="94e3d-104">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-105">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-106">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-106">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="94e3d-107">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94e3d-107">Az.Cdn</span></span>
* <span data-ttu-id="94e3d-108">New-AzCdnEndpoint cmdlet’inde yanıt ayrıntısını görüntüleme hatası</span><span class="sxs-lookup"><span data-stu-id="94e3d-108">Display error response deatil in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-109">Az.Compute</span></span>
* <span data-ttu-id="94e3d-110">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-110">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="94e3d-111">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="94e3d-111">Az.ContainerInstance</span></span>
* <span data-ttu-id="94e3d-112">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-112">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="94e3d-113">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="94e3d-113">Az.DataBoxEdge</span></span>
* <span data-ttu-id="94e3d-114">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-114">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="94e3d-115">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="94e3d-115">Get the Edge Stroage Container</span></span>
* <span data-ttu-id="94e3d-116">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-116">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="94e3d-117">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="94e3d-117">Create new Edge Stroage Container</span></span>
* <span data-ttu-id="94e3d-118">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-118">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="94e3d-119">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="94e3d-119">Remove the Edge Stroage Container</span></span>
* <span data-ttu-id="94e3d-120">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-120">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="94e3d-121">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="94e3d-121">Invoke action to refresh data on Edge Stroage Container</span></span>
* <span data-ttu-id="94e3d-122">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-122">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="94e3d-123">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="94e3d-123">Get the Edge Stroage Account</span></span>
* <span data-ttu-id="94e3d-124">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-124">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="94e3d-125">Yeni Edge Depolama Hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="94e3d-125">Create new Edge Stroage Account</span></span>
* <span data-ttu-id="94e3d-126">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-126">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="94e3d-127">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="94e3d-127">Remove the Edge Stroage Account</span></span>
* <span data-ttu-id="94e3d-128">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="94e3d-128">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="94e3d-129">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="94e3d-129">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="94e3d-130">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-130">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="94e3d-131">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="94e3d-131">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-132">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-132">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-133">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-133">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="94e3d-134">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-134">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="94e3d-135">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-135">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="94e3d-136">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="94e3d-136">Az.DevTestLabs</span></span>
* <span data-ttu-id="94e3d-137">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-137">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94e3d-138">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-138">Az.EventHub</span></span>
* <span data-ttu-id="94e3d-139">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-139">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="94e3d-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="94e3d-140">Az.HDInsight</span></span>
* <span data-ttu-id="94e3d-141">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-141">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="94e3d-142">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="94e3d-142">Az.MachineLearning</span></span>
* <span data-ttu-id="94e3d-143">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-143">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="94e3d-144">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="94e3d-144">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="94e3d-145">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="94e3d-145">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="94e3d-146">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="94e3d-146">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="94e3d-147">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="94e3d-147">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="94e3d-148">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="94e3d-148">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="94e3d-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="94e3d-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="94e3d-150">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="94e3d-150">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-151">Az.Network</span></span>
* <span data-ttu-id="94e3d-152">1\.36-önizleme olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-önizleme’ye yükseltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-152">Upgrade dependancy of Microsoft.Azure.Management.Sql from 1.36-preivew to 1.37-preivew</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-153">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-154">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-154">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed leys for Azure to Azure provider.</span></span>
* <span data-ttu-id="94e3d-155">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-155">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="94e3d-156">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-156">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="94e3d-157">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-157">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-158">Az.Resources</span></span>
* <span data-ttu-id="94e3d-159">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-159">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-160">Az.Sql</span></span>
* <span data-ttu-id="94e3d-161">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-161">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="94e3d-162">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-162">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="94e3d-163">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="94e3d-163">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="94e3d-164">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-164">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-165">Az.Storage</span></span>
* <span data-ttu-id="94e3d-166">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-166">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="94e3d-167">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="94e3d-167">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="94e3d-168">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="94e3d-168">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="94e3d-169">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-169">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="94e3d-170">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-170">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="94e3d-171">Genel</span><span class="sxs-lookup"><span data-stu-id="94e3d-171">General</span></span>
* <span data-ttu-id="94e3d-172">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-172">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="94e3d-173">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-173">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-174">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="94e3d-174">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="94e3d-175">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-175">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="94e3d-176">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="94e3d-176">Az.Batch</span></span>
* <span data-ttu-id="94e3d-177">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-177">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-178">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-178">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-179">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-179">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="94e3d-180">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="94e3d-180">Az.FrontDoor</span></span>
* <span data-ttu-id="94e3d-181">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-181">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="94e3d-182">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-182">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="94e3d-183">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="94e3d-183">Az.HealthcareApis</span></span>
* <span data-ttu-id="94e3d-184">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="94e3d-184">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="94e3d-185">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94e3d-185">Az.KeyVault</span></span>
* <span data-ttu-id="94e3d-186">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-186">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="94e3d-187">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="94e3d-187">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="94e3d-188">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-188">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94e3d-189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94e3d-189">Az.Monitor</span></span>
* <span data-ttu-id="94e3d-190">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-190">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="94e3d-191">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="94e3d-191">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="94e3d-192">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="94e3d-192">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-193">Az.Network</span></span>
* <span data-ttu-id="94e3d-194">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-194">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-195">Az.Resources</span></span>
* <span data-ttu-id="94e3d-196">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-196">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="94e3d-197">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-197">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-198">Az.Sql</span></span>
* <span data-ttu-id="94e3d-199">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-199">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-200">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-200">Az.Storage</span></span>
* <span data-ttu-id="94e3d-201">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-201">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="94e3d-202">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="94e3d-202">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="94e3d-203">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="94e3d-203">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="94e3d-204">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-204">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="94e3d-205">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="94e3d-205">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="94e3d-206">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-206">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="94e3d-207">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-207">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="94e3d-208">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="94e3d-208">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="94e3d-209">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="94e3d-209">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="94e3d-210">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-210">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="94e3d-211">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="94e3d-211">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="94e3d-212">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-212">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="94e3d-213">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="94e3d-213">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="94e3d-214">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-214">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="94e3d-215">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="94e3d-215">Highlights since the last major release</span></span>
* <span data-ttu-id="94e3d-216">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="94e3d-216">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="94e3d-217">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="94e3d-217">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-218">Az.Compute</span></span>
* <span data-ttu-id="94e3d-219">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="94e3d-219">VM Reapply feature</span></span>
    - <span data-ttu-id="94e3d-220">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="94e3d-220">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="94e3d-221">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="94e3d-221">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="94e3d-222">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="94e3d-222">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="94e3d-223">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-223">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="94e3d-224">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-224">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="94e3d-225">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-225">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="94e3d-226">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-226">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="94e3d-227">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-227">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="94e3d-228">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-228">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="94e3d-229">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-229">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="94e3d-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="94e3d-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="94e3d-231">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-231">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="94e3d-232">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="94e3d-232">Get the Order</span></span>
* <span data-ttu-id="94e3d-233">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-233">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="94e3d-234">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="94e3d-234">Create new Order</span></span>
* <span data-ttu-id="94e3d-235">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-235">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="94e3d-236">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="94e3d-236">Remove the Order</span></span>
* <span data-ttu-id="94e3d-237">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="94e3d-237">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="94e3d-238">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="94e3d-238">Now creates Local Share</span></span>
* <span data-ttu-id="94e3d-239">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-239">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="94e3d-240">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="94e3d-240">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="94e3d-241">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-241">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="94e3d-242">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="94e3d-242">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="94e3d-243">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-243">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="94e3d-244">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="94e3d-244">Gets the information about Triggers</span></span>
* <span data-ttu-id="94e3d-245">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-245">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="94e3d-246">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="94e3d-246">Create new Triggers</span></span>
* <span data-ttu-id="94e3d-247">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-247">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="94e3d-248">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="94e3d-248">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-249">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-250">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-250">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="94e3d-251">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-251">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-252">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-253">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-253">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94e3d-254">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-254">Az.EventHub</span></span>
* <span data-ttu-id="94e3d-255">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-255">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="94e3d-256">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="94e3d-256">Az.FrontDoor</span></span>
* <span data-ttu-id="94e3d-257">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-257">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="94e3d-258">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-258">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="94e3d-259">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-259">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="94e3d-260">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="94e3d-260">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-261">Az.Network</span></span>
* <span data-ttu-id="94e3d-262">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-262">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="94e3d-263">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="94e3d-263">Az.PrivateDns</span></span>
* <span data-ttu-id="94e3d-264">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-264">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-265">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-265">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-266">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-266">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="94e3d-267">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-267">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="94e3d-268">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-268">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="94e3d-269">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="94e3d-269">Az.RedisCache</span></span>
* <span data-ttu-id="94e3d-270">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-270">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="94e3d-271">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-271">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="94e3d-272">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-272">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-273">Az.Resources</span></span>
- <span data-ttu-id="94e3d-274">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-274">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="94e3d-275">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-275">Updated create policy definition help example</span></span>
- <span data-ttu-id="94e3d-276">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-276">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="94e3d-277">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-277">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="94e3d-278">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-278">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-279">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-279">Az.Sql</span></span>
* <span data-ttu-id="94e3d-280">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-280">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="94e3d-281">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-281">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="94e3d-282">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-282">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="94e3d-283">Genel</span><span class="sxs-lookup"><span data-stu-id="94e3d-283">General</span></span>
* <span data-ttu-id="94e3d-284">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="94e3d-284">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="94e3d-285">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-285">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-286">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="94e3d-286">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="94e3d-287">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="94e3d-287">Az.Advisor</span></span>
* <span data-ttu-id="94e3d-288">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-288">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="94e3d-289">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="94e3d-289">Az.Batch</span></span>
* <span data-ttu-id="94e3d-290">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-290">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="94e3d-291">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="94e3d-291">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="94e3d-292">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-292">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="94e3d-293">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-293">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="94e3d-294">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="94e3d-294">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="94e3d-295">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="94e3d-295">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="94e3d-296">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="94e3d-296">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="94e3d-297">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-297">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="94e3d-298">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-298">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="94e3d-299">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-299">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="94e3d-300">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="94e3d-300">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="94e3d-301">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="94e3d-301">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="94e3d-302">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-302">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="94e3d-303">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="94e3d-303">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="94e3d-304">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-304">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="94e3d-305">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-305">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="94e3d-306">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-306">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="94e3d-307">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-307">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="94e3d-308">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-308">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="94e3d-309">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-309">This operation is no longer supported.</span></span>
* <span data-ttu-id="94e3d-310">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-310">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="94e3d-311">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-311">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="94e3d-312">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-312">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="94e3d-313">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-313">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="94e3d-314">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-314">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="94e3d-315">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-315">New non-verified images are also now returned.</span></span> <span data-ttu-id="94e3d-316">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-316">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="94e3d-317">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-317">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="94e3d-318">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-318">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="94e3d-319">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-319">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="94e3d-320">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-320">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="94e3d-321">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-321">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="94e3d-322">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-322">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="94e3d-323">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-323">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="94e3d-324">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="94e3d-324">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="94e3d-325">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="94e3d-325">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="94e3d-326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94e3d-326">Az.Cdn</span></span>
* <span data-ttu-id="94e3d-327">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-327">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="94e3d-328">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-328">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-329">Az.Compute</span></span>
* <span data-ttu-id="94e3d-330">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="94e3d-330">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="94e3d-331">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="94e3d-331">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="94e3d-332">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="94e3d-332">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="94e3d-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="94e3d-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="94e3d-334">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-334">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="94e3d-335">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-335">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="94e3d-336">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="94e3d-336">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="94e3d-337">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-337">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="94e3d-338">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="94e3d-338">Breaking changes</span></span>
    - <span data-ttu-id="94e3d-339">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-339">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="94e3d-340">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="94e3d-340">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-341">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-342">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-342">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-344">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-344">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="94e3d-345">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="94e3d-345">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="94e3d-346">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="94e3d-346">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="94e3d-347">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="94e3d-347">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="94e3d-348">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="94e3d-348">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="94e3d-349">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="94e3d-349">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="94e3d-350">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="94e3d-350">Az.FrontDoor</span></span>
* <span data-ttu-id="94e3d-351">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-351">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="94e3d-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="94e3d-352">Az.HDInsight</span></span>
* <span data-ttu-id="94e3d-353">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-353">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="94e3d-354">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-354">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="94e3d-355">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-355">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="94e3d-356">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="94e3d-356">Removed five cmdlets:</span></span>
    - <span data-ttu-id="94e3d-357">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="94e3d-357">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="94e3d-358">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="94e3d-358">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="94e3d-359">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="94e3d-359">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="94e3d-360">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="94e3d-360">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="94e3d-361">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="94e3d-361">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="94e3d-362">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-362">Added three cmdlets:</span></span>
    - <span data-ttu-id="94e3d-363">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="94e3d-363">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="94e3d-364">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="94e3d-364">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="94e3d-365">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="94e3d-365">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="94e3d-366">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-366">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="94e3d-367">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-367">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="94e3d-368">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-368">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="94e3d-369">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-369">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="94e3d-370">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-370">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="94e3d-371">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-371">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="94e3d-372">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-372">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="94e3d-373">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-373">Added some scenario test cases.</span></span>
* <span data-ttu-id="94e3d-374">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="94e3d-374">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94e3d-375">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-375">Az.IotHub</span></span>
* <span data-ttu-id="94e3d-376">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="94e3d-376">Breaking changes:</span></span>
    - <span data-ttu-id="94e3d-377">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-377">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="94e3d-378">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-378">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="94e3d-379">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-379">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="94e3d-380">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-380">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="94e3d-381">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-381">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="94e3d-382">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-382">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="94e3d-383">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-383">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="94e3d-384">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-384">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="94e3d-385">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-385">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="94e3d-386">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-386">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="94e3d-387">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-387">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="94e3d-388">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-388">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-389">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-389">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-390">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-390">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="94e3d-391">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-391">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="94e3d-392">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-392">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="94e3d-393">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-393">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="94e3d-394">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-394">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="94e3d-395">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-395">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="94e3d-396">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-396">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="94e3d-397">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-397">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="94e3d-398">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-398">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-399">Az.Resources</span></span>
* <span data-ttu-id="94e3d-400">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-400">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-401">Az.Network</span></span>
* <span data-ttu-id="94e3d-402">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-402">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="94e3d-403">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-403">Updated cmdlet:</span></span>
        - <span data-ttu-id="94e3d-404">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-404">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="94e3d-405">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-405">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="94e3d-406">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-406">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="94e3d-407">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-407">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="94e3d-408">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-408">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="94e3d-409">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-409">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="94e3d-410">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="94e3d-410">New cmdlet:</span></span>
        - <span data-ttu-id="94e3d-411">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="94e3d-411">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="94e3d-412">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-412">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="94e3d-413">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-413">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="94e3d-414">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-414">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="94e3d-415">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-415">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="94e3d-416">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-416">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="94e3d-417">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-417">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="94e3d-418">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-418">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="94e3d-419">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-419">New cmdlets added:</span></span>
        - <span data-ttu-id="94e3d-420">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="94e3d-420">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="94e3d-421">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="94e3d-421">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="94e3d-422">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="94e3d-422">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="94e3d-423">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="94e3d-423">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="94e3d-424">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-424">Set-AzVirtualHub</span></span>
* <span data-ttu-id="94e3d-425">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-425">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="94e3d-426">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-426">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="94e3d-427">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-427">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="94e3d-428">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-428">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="94e3d-429">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-429">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="94e3d-430">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-430">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="94e3d-431">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-431">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="94e3d-432">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-432">New cmdlets added:</span></span>
        - <span data-ttu-id="94e3d-433">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-433">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="94e3d-434">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-434">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="94e3d-435">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-435">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="94e3d-436">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-436">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="94e3d-437">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-437">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="94e3d-438">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-438">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="94e3d-439">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-439">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="94e3d-440">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-440">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="94e3d-441">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-441">New cmdlets added:</span></span>
        - <span data-ttu-id="94e3d-442">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="94e3d-442">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="94e3d-443">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="94e3d-443">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="94e3d-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="94e3d-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="94e3d-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="94e3d-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="94e3d-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="94e3d-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="94e3d-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="94e3d-448">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-448">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="94e3d-449">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-449">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="94e3d-450">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-450">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="94e3d-451">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-451">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="94e3d-452">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-452">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="94e3d-453">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-453">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="94e3d-454">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-454">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="94e3d-455">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-455">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="94e3d-456">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-456">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="94e3d-457">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="94e3d-457">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="94e3d-458">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-458">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="94e3d-459">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-459">New cmdlets added:</span></span>
        - <span data-ttu-id="94e3d-460">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="94e3d-460">New-AzIpGroup</span></span>
        - <span data-ttu-id="94e3d-461">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="94e3d-461">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="94e3d-462">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="94e3d-462">Get-AzIpGroup</span></span>
        - <span data-ttu-id="94e3d-463">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="94e3d-463">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="94e3d-464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-464">Az.ServiceFabric</span></span>
* <span data-ttu-id="94e3d-465">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-465">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-466">Az.Sql</span></span>
* <span data-ttu-id="94e3d-467">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-467">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="94e3d-468">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-468">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="94e3d-469">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="94e3d-469">Removed deprecated aliases:</span></span>
* <span data-ttu-id="94e3d-470">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="94e3d-470">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="94e3d-471">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="94e3d-471">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="94e3d-472">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-472">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="94e3d-473">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-473">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="94e3d-474">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-474">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="94e3d-475">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-475">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-476">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-476">Az.Storage</span></span>
* <span data-ttu-id="94e3d-477">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-477">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="94e3d-478">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-478">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="94e3d-479">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-479">Set-AzStorageAccount</span></span>
* <span data-ttu-id="94e3d-480">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="94e3d-480">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="94e3d-481">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="94e3d-481">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="94e3d-482">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="94e3d-482">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="94e3d-483">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-483">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="94e3d-484">Genel</span><span class="sxs-lookup"><span data-stu-id="94e3d-484">General</span></span>
* <span data-ttu-id="94e3d-485">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="94e3d-485">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="94e3d-486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-486">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-487">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-487">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="94e3d-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94e3d-488">Az.ApiManagement</span></span>
* <span data-ttu-id="94e3d-489">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-489">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="94e3d-490">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-490">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94e3d-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-491">Az.Automation</span></span>
* <span data-ttu-id="94e3d-492">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-492">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="94e3d-493">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="94e3d-493">Az.Batch</span></span>
* <span data-ttu-id="94e3d-494">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="94e3d-494">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-495">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-495">Az.Compute</span></span>
* <span data-ttu-id="94e3d-496">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-496">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="94e3d-497">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-497">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="94e3d-498">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-498">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="94e3d-499">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-499">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-500">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-501">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="94e3d-501">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="94e3d-502">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="94e3d-502">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="94e3d-503">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-503">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-505">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-505">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="94e3d-506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="94e3d-506">Az.HealthcareApis</span></span>
* <span data-ttu-id="94e3d-507">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-507">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="94e3d-508">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-508">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="94e3d-509">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-509">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="94e3d-510">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-510">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94e3d-511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-511">Az.IotHub</span></span>
* <span data-ttu-id="94e3d-512">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="94e3d-512">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="94e3d-513">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-513">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="94e3d-514">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94e3d-514">Az.Monitor</span></span>
* <span data-ttu-id="94e3d-515">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-515">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="94e3d-516">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="94e3d-516">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="94e3d-517">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="94e3d-517">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="94e3d-518">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-518">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-519">Az.Network</span></span>
* <span data-ttu-id="94e3d-520">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-520">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="94e3d-521">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-521">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="94e3d-522">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-522">New cmdlets added:</span></span>
        - <span data-ttu-id="94e3d-523">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="94e3d-523">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="94e3d-524">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-524">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="94e3d-525">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-525">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="94e3d-526">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-526">Updated cmdlets:</span></span>
        - <span data-ttu-id="94e3d-527">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="94e3d-528">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="94e3d-529">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="94e3d-530">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-530">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="94e3d-531">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="94e3d-531">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="94e3d-532">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="94e3d-532">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="94e3d-533">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="94e3d-533">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="94e3d-534">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="94e3d-534">Az.RedisCache</span></span>
* <span data-ttu-id="94e3d-535">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-535">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-536">Az.Sql</span></span>
* <span data-ttu-id="94e3d-537">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-537">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-538">Az.Storage</span></span>
* <span data-ttu-id="94e3d-539">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-539">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="94e3d-540">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="94e3d-540">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="94e3d-541">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="94e3d-541">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="94e3d-542">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="94e3d-542">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="94e3d-543">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-543">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="94e3d-544">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="94e3d-544">Az.StorageSync</span></span>
* <span data-ttu-id="94e3d-545">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-545">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-546">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-546">Az.Websites</span></span>
* <span data-ttu-id="94e3d-547">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-547">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="94e3d-548">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-548">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="94e3d-549">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94e3d-549">Az.ApiManagement</span></span>
* <span data-ttu-id="94e3d-550">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-550">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="94e3d-551">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-551">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="94e3d-552">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="94e3d-552">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94e3d-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-553">Az.Automation</span></span>
* <span data-ttu-id="94e3d-554">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-554">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="94e3d-555">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-555">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="94e3d-556">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-556">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-557">Az.Compute</span></span>
* <span data-ttu-id="94e3d-558">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-558">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="94e3d-559">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-559">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="94e3d-560">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-560">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="94e3d-561">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-561">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="94e3d-562">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-562">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="94e3d-563">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-563">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="94e3d-564">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-564">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="94e3d-565">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-565">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="94e3d-566">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-566">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-567">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-567">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-568">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="94e3d-568">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="94e3d-569">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-569">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="94e3d-570">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="94e3d-570">Az.HDInsight</span></span>
* <span data-ttu-id="94e3d-571">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="94e3d-571">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94e3d-572">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-572">Az.IotHub</span></span>
* <span data-ttu-id="94e3d-573">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-573">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="94e3d-574">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-574">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="94e3d-575">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="94e3d-575">New cmdlets are:</span></span>
    - <span data-ttu-id="94e3d-576">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="94e3d-576">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="94e3d-577">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="94e3d-577">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="94e3d-578">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="94e3d-578">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="94e3d-579">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="94e3d-579">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94e3d-580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94e3d-580">Az.Monitor</span></span>
* <span data-ttu-id="94e3d-581">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="94e3d-581">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="94e3d-582">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-582">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="94e3d-583">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="94e3d-583">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="94e3d-584">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="94e3d-584">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="94e3d-585">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-585">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="94e3d-586">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-586">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="94e3d-587">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-587">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="94e3d-588">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="94e3d-588">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="94e3d-589">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-589">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="94e3d-590">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="94e3d-590">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="94e3d-591">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-591">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="94e3d-592">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="94e3d-592">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="94e3d-593">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-593">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="94e3d-594">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="94e3d-594">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="94e3d-595">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="94e3d-595">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="94e3d-596">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="94e3d-596">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="94e3d-597">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="94e3d-597">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="94e3d-598">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="94e3d-598">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="94e3d-599">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-599">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="94e3d-600">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-600">Overall improved help files</span></span>
* <span data-ttu-id="94e3d-601">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-601">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-602">Az.Network</span></span>
* <span data-ttu-id="94e3d-603">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-603">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="94e3d-604">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-604">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="94e3d-605">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-605">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="94e3d-606">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-606">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="94e3d-607">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-607">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="94e3d-608">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-608">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="94e3d-609">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-609">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="94e3d-610">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-610">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="94e3d-611">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-611">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="94e3d-612">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-612">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="94e3d-613">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-613">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="94e3d-614">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-614">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="94e3d-615">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-615">New cmdlets</span></span>
        - <span data-ttu-id="94e3d-616">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="94e3d-616">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="94e3d-617">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-617">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="94e3d-618">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-618">Updated cmdlet:</span></span>
        - <span data-ttu-id="94e3d-619">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="94e3d-619">New-VpnSite</span></span>
        - <span data-ttu-id="94e3d-620">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="94e3d-620">Update-VpnSite</span></span>
        - <span data-ttu-id="94e3d-621">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-621">New-VpnConnection</span></span>
        - <span data-ttu-id="94e3d-622">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-622">Update-VpnConnection</span></span>
* <span data-ttu-id="94e3d-623">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-623">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-624">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-624">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-625">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-625">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="94e3d-626">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-626">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-627">Az.Resources</span></span>
* <span data-ttu-id="94e3d-628">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-628">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="94e3d-629">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-629">Az.ServiceFabric</span></span>
* <span data-ttu-id="94e3d-630">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-630">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="94e3d-631">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="94e3d-631">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="94e3d-632">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="94e3d-632">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="94e3d-633">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="94e3d-633">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="94e3d-634">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="94e3d-634">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="94e3d-635">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="94e3d-635">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="94e3d-636">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="94e3d-636">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="94e3d-637">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="94e3d-637">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="94e3d-638">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="94e3d-638">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="94e3d-639">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="94e3d-639">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="94e3d-640">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="94e3d-640">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="94e3d-641">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="94e3d-641">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="94e3d-642">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="94e3d-642">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="94e3d-643">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="94e3d-643">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="94e3d-644">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="94e3d-644">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="94e3d-645">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-645">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="94e3d-646">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="94e3d-646">Az.SignalR</span></span>
* <span data-ttu-id="94e3d-647">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-647">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-648">Az.Sql</span></span>
* <span data-ttu-id="94e3d-649">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-649">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="94e3d-650">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-650">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="94e3d-651">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-651">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="94e3d-652">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-652">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="94e3d-653">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-653">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-654">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-654">Az.Storage</span></span>
* <span data-ttu-id="94e3d-655">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-655">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="94e3d-656">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-656">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="94e3d-657">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="94e3d-657">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="94e3d-658">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="94e3d-658">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="94e3d-659">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-659">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="94e3d-660">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="94e3d-660">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="94e3d-661">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-661">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="94e3d-662">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="94e3d-662">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="94e3d-663">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="94e3d-663">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="94e3d-664">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="94e3d-664">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="94e3d-665">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="94e3d-665">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-666">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-666">Az.Websites</span></span>
* <span data-ttu-id="94e3d-667">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-667">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="94e3d-668">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-668">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="94e3d-669">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-669">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="94e3d-670">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-670">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="94e3d-671">Genel</span><span class="sxs-lookup"><span data-stu-id="94e3d-671">General</span></span>
* <span data-ttu-id="94e3d-672">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-672">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="94e3d-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-673">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-674">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="94e3d-674">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="94e3d-675">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="94e3d-675">Az.Aks</span></span>
* <span data-ttu-id="94e3d-676">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-676">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="94e3d-677">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="94e3d-677">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="94e3d-678">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94e3d-678">Az.ApiManagement</span></span>
* <span data-ttu-id="94e3d-679">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-679">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="94e3d-680">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-680">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="94e3d-681">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-681">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="94e3d-682">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="94e3d-682">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="94e3d-683">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-683">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="94e3d-684">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="94e3d-684">Az.Batch</span></span>
* <span data-ttu-id="94e3d-685">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-685">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="94e3d-686">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94e3d-686">Az.Cdn</span></span>
* <span data-ttu-id="94e3d-687">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-687">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-688">Az.Compute</span></span>
* <span data-ttu-id="94e3d-689">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-689">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="94e3d-690">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-690">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="94e3d-691">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-691">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="94e3d-692">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-692">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="94e3d-693">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="94e3d-693">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="94e3d-694">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-694">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="94e3d-695">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-695">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="94e3d-696">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-696">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-697">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-698">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-698">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="94e3d-699">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-699">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="94e3d-700">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-700">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="94e3d-701">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-701">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-702">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-703">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-703">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94e3d-704">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-704">Az.EventHub</span></span>
* <span data-ttu-id="94e3d-705">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="94e3d-705">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="94e3d-706">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="94e3d-706">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="94e3d-707">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-707">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="94e3d-708">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="94e3d-708">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="94e3d-709">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="94e3d-709">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="94e3d-710">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-710">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94e3d-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94e3d-711">Az.Monitor</span></span>
* <span data-ttu-id="94e3d-712">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-712">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-713">Az.Network</span></span>
* <span data-ttu-id="94e3d-714">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-714">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="94e3d-715">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-715">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="94e3d-716">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-716">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="94e3d-717">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="94e3d-717">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="94e3d-718">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-718">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="94e3d-719">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-719">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="94e3d-720">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-720">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="94e3d-721">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-721">Az.OperationalInsights</span></span>
* <span data-ttu-id="94e3d-722">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-722">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="94e3d-723">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-723">Added example</span></span>
    - <span data-ttu-id="94e3d-724">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-724">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="94e3d-725">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-725">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="94e3d-726">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-726">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-727">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-727">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-728">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-728">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-729">Az.Resources</span></span>
* <span data-ttu-id="94e3d-730">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-730">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="94e3d-731">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-731">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="94e3d-732">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="94e3d-732">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="94e3d-733">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-733">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="94e3d-734">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="94e3d-734">Az.ServiceBus</span></span>
* <span data-ttu-id="94e3d-735">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="94e3d-735">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="94e3d-736">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="94e3d-736">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="94e3d-737">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-737">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="94e3d-738">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-738">Az.ServiceFabric</span></span>
* <span data-ttu-id="94e3d-739">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-739">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="94e3d-740">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="94e3d-740">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="94e3d-741">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="94e3d-741">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="94e3d-742">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-742">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="94e3d-743">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="94e3d-743">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="94e3d-744">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-744">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-745">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-745">Az.Sql</span></span>
* <span data-ttu-id="94e3d-746">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-746">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-747">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-747">Az.Storage</span></span>
* <span data-ttu-id="94e3d-748">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-748">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="94e3d-749">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="94e3d-749">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="94e3d-750">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="94e3d-750">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="94e3d-751">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="94e3d-751">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="94e3d-752">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-752">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="94e3d-753">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="94e3d-753">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-754">Az.Websites</span></span>
* <span data-ttu-id="94e3d-755">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-755">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="94e3d-756">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-756">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-757">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-758">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-758">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="94e3d-759">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-759">Az.ApplicationInsights</span></span>
* <span data-ttu-id="94e3d-760">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-760">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="94e3d-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-761">Az.Automation</span></span>
* <span data-ttu-id="94e3d-762">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-762">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="94e3d-763">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-763">Az.CognitiveServices</span></span>
* <span data-ttu-id="94e3d-764">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-764">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-765">Az.Compute</span></span>
* <span data-ttu-id="94e3d-766">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-766">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="94e3d-767">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="94e3d-767">Az.ContainerRegistry</span></span>
* <span data-ttu-id="94e3d-768">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-768">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="94e3d-769">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="94e3d-769">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-770">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-770">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-771">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-771">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="94e3d-772">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-772">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94e3d-773">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-773">Az.EventHub</span></span>
* <span data-ttu-id="94e3d-774">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="94e3d-774">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="94e3d-775">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-775">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="94e3d-776">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94e3d-776">Az.KeyVault</span></span>
* <span data-ttu-id="94e3d-777">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-777">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="94e3d-778">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="94e3d-778">Az.LogicApp</span></span>
* <span data-ttu-id="94e3d-779">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="94e3d-779">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="94e3d-780">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-780">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="94e3d-781">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-781">Az.ManagedServices</span></span>
* <span data-ttu-id="94e3d-782">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="94e3d-782">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-783">Az.Network</span></span>
* <span data-ttu-id="94e3d-784">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-784">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="94e3d-785">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-785">New cmdlets</span></span>
        - <span data-ttu-id="94e3d-786">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="94e3d-786">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="94e3d-787">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="94e3d-787">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="94e3d-788">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-788">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="94e3d-789">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-789">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="94e3d-790">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-790">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="94e3d-791">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-791">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="94e3d-792">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="94e3d-792">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="94e3d-793">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="94e3d-793">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="94e3d-794">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="94e3d-794">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="94e3d-795">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-795">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="94e3d-796">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-796">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="94e3d-797">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-797">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="94e3d-798">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-798">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="94e3d-799">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-799">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="94e3d-800">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-800">Updated cmdlets</span></span>
        - <span data-ttu-id="94e3d-801">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-801">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="94e3d-802">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-802">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="94e3d-803">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-803">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="94e3d-804">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-804">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="94e3d-805">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-805">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="94e3d-806">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-806">Updated cmdlet:</span></span>
        - <span data-ttu-id="94e3d-807">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-807">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="94e3d-808">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-808">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="94e3d-809">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-809">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="94e3d-810">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-810">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="94e3d-811">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-811">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="94e3d-812">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="94e3d-812">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="94e3d-813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-813">Az.OperationalInsights</span></span>
* <span data-ttu-id="94e3d-814">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-814">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="94e3d-815">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-815">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-817">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-817">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="94e3d-818">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-818">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="94e3d-819">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-819">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="94e3d-820">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-820">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="94e3d-821">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-821">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="94e3d-822">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-822">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="94e3d-823">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-823">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="94e3d-824">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-824">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="94e3d-825">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-825">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="94e3d-826">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-826">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-827">Az.Resources</span></span>
- <span data-ttu-id="94e3d-828">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-828">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="94e3d-829">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-829">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="94e3d-830">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="94e3d-830">Az.ServiceBus</span></span>
* <span data-ttu-id="94e3d-831">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="94e3d-831">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="94e3d-832">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-832">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-833">Az.Sql</span></span>
* <span data-ttu-id="94e3d-834">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-834">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="94e3d-835">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-835">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="94e3d-836">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-836">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-837">Az.Storage</span></span>
* <span data-ttu-id="94e3d-838">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-838">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="94e3d-839">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="94e3d-839">Az.StorageSync</span></span>
* <span data-ttu-id="94e3d-840">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-840">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="94e3d-841">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-841">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-842">Az.Websites</span></span>
* <span data-ttu-id="94e3d-843">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-843">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="94e3d-844">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-844">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="94e3d-845">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-845">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="94e3d-846">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-846">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-847">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-848">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-848">Add support for profile cmdlets</span></span>
* <span data-ttu-id="94e3d-849">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-849">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="94e3d-850">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-850">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="94e3d-851">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="94e3d-851">Az.Advisor</span></span>
* <span data-ttu-id="94e3d-852">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-852">GA release of Az.Advisor</span></span>
* <span data-ttu-id="94e3d-853">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="94e3d-853">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="94e3d-854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94e3d-854">Az.ApiManagement</span></span>
* <span data-ttu-id="94e3d-855">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-855">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="94e3d-856">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="94e3d-856">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="94e3d-857">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-857">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="94e3d-858">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="94e3d-858">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="94e3d-859">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="94e3d-859">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="94e3d-860">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="94e3d-860">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="94e3d-861">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-861">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94e3d-862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-862">Az.Automation</span></span>
* <span data-ttu-id="94e3d-863">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-863">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-864">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-864">Az.Compute</span></span>
* <span data-ttu-id="94e3d-865">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-865">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-866">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-866">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-867">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-867">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="94e3d-868">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="94e3d-868">Az.EventGrid</span></span>
* <span data-ttu-id="94e3d-869">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-869">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94e3d-870">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-870">Az.IotHub</span></span>
* <span data-ttu-id="94e3d-871">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-871">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-872">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-872">Az.Network</span></span>
* <span data-ttu-id="94e3d-873">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-873">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="94e3d-874">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-874">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="94e3d-875">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-875">Az.PolicyInsights</span></span>
* <span data-ttu-id="94e3d-876">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-876">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="94e3d-877">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="94e3d-877">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="94e3d-878">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-878">Az.OperationalInsights</span></span>
* <span data-ttu-id="94e3d-879">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-879">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-881">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="94e3d-881">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-882">Az.Resources</span></span>
    - <span data-ttu-id="94e3d-883">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="94e3d-883">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="94e3d-884">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-884">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="94e3d-885">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-885">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="94e3d-886">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-886">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="94e3d-887">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="94e3d-887">Az.ServiceBus</span></span>
* <span data-ttu-id="94e3d-888">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-888">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-889">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-889">Az.Sql</span></span>
* <span data-ttu-id="94e3d-890">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-890">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="94e3d-891">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-891">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="94e3d-892">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="94e3d-892">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="94e3d-893">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="94e3d-893">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="94e3d-894">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="94e3d-894">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="94e3d-895">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="94e3d-895">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="94e3d-896">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="94e3d-896">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="94e3d-897">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="94e3d-897">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="94e3d-898">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-898">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-899">Az.Storage</span></span>
* <span data-ttu-id="94e3d-900">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-900">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="94e3d-901">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="94e3d-901">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="94e3d-902">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-902">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="94e3d-903">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-903">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="94e3d-904">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-904">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="94e3d-905">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-905">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="94e3d-906">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-906">Set-AzStorageAccount</span></span>
* <span data-ttu-id="94e3d-907">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-907">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="94e3d-908">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="94e3d-908">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="94e3d-909">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="94e3d-909">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="94e3d-910">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="94e3d-910">Az.StorageSync</span></span>
* <span data-ttu-id="94e3d-911">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="94e3d-911">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="94e3d-912">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-912">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-913">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-913">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-914">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-914">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="94e3d-915">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="94e3d-915">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="94e3d-916">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-916">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="94e3d-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="94e3d-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="94e3d-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="94e3d-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-919">Az.Compute</span></span>
* <span data-ttu-id="94e3d-920">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-920">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="94e3d-921">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-921">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="94e3d-922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="94e3d-922">Az.Dns</span></span>
* <span data-ttu-id="94e3d-923">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-923">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="94e3d-924">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="94e3d-924">Az.EventGrid</span></span>
* <span data-ttu-id="94e3d-925">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-925">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="94e3d-926">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="94e3d-926">New cmdlets:</span></span>
    - <span data-ttu-id="94e3d-927">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="94e3d-927">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="94e3d-928">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94e3d-928">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="94e3d-929">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="94e3d-929">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="94e3d-930">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="94e3d-930">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="94e3d-931">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="94e3d-931">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="94e3d-932">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94e3d-932">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="94e3d-933">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="94e3d-933">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="94e3d-934">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="94e3d-934">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="94e3d-935">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="94e3d-935">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="94e3d-936">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="94e3d-936">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="94e3d-937">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="94e3d-937">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="94e3d-938">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94e3d-938">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="94e3d-939">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="94e3d-939">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="94e3d-940">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="94e3d-940">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="94e3d-941">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="94e3d-941">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="94e3d-942">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94e3d-942">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="94e3d-943">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-943">Updated cmdlets:</span></span>
    - <span data-ttu-id="94e3d-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="94e3d-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="94e3d-945">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-945">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="94e3d-946">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-946">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="94e3d-947">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-947">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="94e3d-948">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-948">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="94e3d-949">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="94e3d-949">Event subscription expiration date,</span></span>
            - <span data-ttu-id="94e3d-950">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="94e3d-950">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="94e3d-951">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-951">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="94e3d-952">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="94e3d-952">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="94e3d-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="94e3d-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="94e3d-954">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-954">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="94e3d-955">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="94e3d-955">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="94e3d-956">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-956">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="94e3d-957">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-957">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="94e3d-958">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="94e3d-958">Az.FrontDoor</span></span>
* <span data-ttu-id="94e3d-959">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="94e3d-959">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="94e3d-960">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="94e3d-960">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="94e3d-961">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="94e3d-961">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="94e3d-962">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="94e3d-962">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-963">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-963">Az.Network</span></span>
* <span data-ttu-id="94e3d-964">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="94e3d-964">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="94e3d-965">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-965">New cmdlets</span></span>
        - <span data-ttu-id="94e3d-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="94e3d-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="94e3d-967">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="94e3d-967">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="94e3d-968">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-968">New cmdlets</span></span> 
        - <span data-ttu-id="94e3d-969">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="94e3d-969">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="94e3d-970">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="94e3d-970">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="94e3d-971">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-971">New cmdlets</span></span> 
        - <span data-ttu-id="94e3d-972">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="94e3d-972">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="94e3d-973">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="94e3d-973">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="94e3d-974">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="94e3d-974">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="94e3d-975">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-975">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="94e3d-976">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-976">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="94e3d-977">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="94e3d-977">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="94e3d-978">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-978">New cmdlets</span></span>
        - <span data-ttu-id="94e3d-979">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="94e3d-979">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="94e3d-980">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="94e3d-980">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="94e3d-981">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="94e3d-981">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="94e3d-982">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="94e3d-982">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="94e3d-983">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="94e3d-983">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="94e3d-984">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-984">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="94e3d-985">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-985">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="94e3d-986">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-986">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="94e3d-987">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-987">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="94e3d-988">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-988">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="94e3d-989">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-989">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="94e3d-990">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-990">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="94e3d-991">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-991">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="94e3d-992">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-992">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="94e3d-993">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-993">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="94e3d-994">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-994">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="94e3d-995">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-995">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="94e3d-996">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-996">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="94e3d-997">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-997">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="94e3d-998">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-998">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="94e3d-999">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-999">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="94e3d-1000">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="94e3d-1000">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="94e3d-1001">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="94e3d-1001">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="94e3d-1002">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1002">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="94e3d-1003">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1003">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="94e3d-1004">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1004">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="94e3d-1005">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1005">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="94e3d-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="94e3d-1007">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1007">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1008">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1008">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1009">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="94e3d-1009">Support for additional Template Export options</span></span>
    - <span data-ttu-id="94e3d-1010">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1010">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="94e3d-1011">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1011">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="94e3d-1012">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1012">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="94e3d-1013">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-1013">Az.ServiceFabric</span></span>
* <span data-ttu-id="94e3d-1014">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1014">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1015">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1016">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1016">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="94e3d-1017">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1017">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="94e3d-1018">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1018">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="94e3d-1019">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94e3d-1019">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="94e3d-1020">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94e3d-1020">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="94e3d-1021">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94e3d-1021">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="94e3d-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="94e3d-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="94e3d-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="94e3d-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-1024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1024">Az.Storage</span></span>
* <span data-ttu-id="94e3d-1025">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="94e3d-1025">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="94e3d-1026">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-1026">New-AzStorageAccount</span></span>
* <span data-ttu-id="94e3d-1027">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1027">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="94e3d-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-1029">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1029">Az.Websites</span></span>
* <span data-ttu-id="94e3d-1030">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="94e3d-1030">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="94e3d-1031">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1031">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="94e3d-1032">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1032">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="94e3d-1033">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94e3d-1033">Az.Cdn</span></span>
* <span data-ttu-id="94e3d-1034">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1034">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1035">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1035">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1036">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1036">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="94e3d-1037">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="94e3d-1037">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94e3d-1038">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-1038">Az.EventHub</span></span>
* <span data-ttu-id="94e3d-1039">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1039">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="94e3d-1040">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1040">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1041">Az.Network</span></span>
* <span data-ttu-id="94e3d-1042">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1042">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="94e3d-1043">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1043">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="94e3d-1044">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-1044">Az.PolicyInsights</span></span>
* <span data-ttu-id="94e3d-1045">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1045">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-1046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1046">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-1047">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1047">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="94e3d-1048">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="94e3d-1048">Az.ServiceBus</span></span>
* <span data-ttu-id="94e3d-1049">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="94e3d-1049">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="94e3d-1050">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-1050">Az.ServiceFabric</span></span>
* <span data-ttu-id="94e3d-1051">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1051">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="94e3d-1052">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1052">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1053">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1054">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1054">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="94e3d-1055">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1055">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="94e3d-1056">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1056">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="94e3d-1057">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1057">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1058">Az.Websites</span></span>
* <span data-ttu-id="94e3d-1059">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1059">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="94e3d-1060">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1060">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="94e3d-1061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94e3d-1061">Az.ApiManagement</span></span>
* <span data-ttu-id="94e3d-1062">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1062">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="94e3d-1063">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="94e3d-1063">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="94e3d-1064">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="94e3d-1064">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="94e3d-1065">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="94e3d-1065">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="94e3d-1066">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1066">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="94e3d-1067">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="94e3d-1067">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="94e3d-1068">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="94e3d-1068">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="94e3d-1069">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="94e3d-1069">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="94e3d-1070">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1070">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="94e3d-1071">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="94e3d-1071">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="94e3d-1072">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="94e3d-1072">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="94e3d-1073">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="94e3d-1073">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="94e3d-1074">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="94e3d-1074">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="94e3d-1075">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1075">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="94e3d-1076">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="94e3d-1076">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="94e3d-1077">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="94e3d-1077">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="94e3d-1078">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="94e3d-1078">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="94e3d-1079">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="94e3d-1079">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="94e3d-1080">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1080">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="94e3d-1081">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="94e3d-1081">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="94e3d-1082">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1082">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="94e3d-1083">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1083">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="94e3d-1084">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1084">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="94e3d-1085">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1085">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="94e3d-1086">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1086">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="94e3d-1087">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1087">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="94e3d-1088">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1088">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="94e3d-1089">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1089">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="94e3d-1090">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1090">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="94e3d-1091">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1091">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="94e3d-1092">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1092">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="94e3d-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="94e3d-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="94e3d-1094">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1094">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="94e3d-1095">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1095">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="94e3d-1096">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1096">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="94e3d-1097">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1097">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="94e3d-1098">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1098">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="94e3d-1099">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1099">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="94e3d-1100">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1100">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="94e3d-1101">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1101">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="94e3d-1102">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1102">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="94e3d-1103">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1103">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="94e3d-1104">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1104">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="94e3d-1105">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1105">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="94e3d-1106">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1106">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="94e3d-1107">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1107">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="94e3d-1108">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1108">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="94e3d-1109">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1109">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="94e3d-1110">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1110">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="94e3d-1111">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1111">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="94e3d-1112">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1112">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="94e3d-1113">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1113">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="94e3d-1114">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1114">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="94e3d-1115">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1115">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="94e3d-1116">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1116">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="94e3d-1117">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1117">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="94e3d-1118">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1118">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="94e3d-1119">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1119">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="94e3d-1120">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1120">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="94e3d-1121">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1121">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="94e3d-1122">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1122">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="94e3d-1123">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1123">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="94e3d-1124">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="94e3d-1124">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="94e3d-1125">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1125">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="94e3d-1126">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1126">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="94e3d-1127">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="94e3d-1127">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="94e3d-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="94e3d-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="94e3d-1129">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="94e3d-1129">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="94e3d-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="94e3d-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="94e3d-1131">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="94e3d-1131">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="94e3d-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="94e3d-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="94e3d-1133">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="94e3d-1133">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="94e3d-1134">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="94e3d-1134">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="94e3d-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="94e3d-1136">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="94e3d-1136">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="94e3d-1137">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="94e3d-1137">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="94e3d-1138">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="94e3d-1138">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94e3d-1139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-1139">Az.Automation</span></span>
* <span data-ttu-id="94e3d-1140">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1140">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="94e3d-1141">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1141">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="94e3d-1142">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1142">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="94e3d-1143">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1143">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="94e3d-1144">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1144">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="94e3d-1145">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1145">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="94e3d-1146">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1146">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1147">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1148">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1148">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="94e3d-1149">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1149">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-1150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-1150">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-1151">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1151">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94e3d-1152">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1152">Az.Monitor</span></span>
* <span data-ttu-id="94e3d-1153">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1153">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1154">Az.Network</span></span>
* <span data-ttu-id="94e3d-1155">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1155">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="94e3d-1156">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-1156">Updated cmdlet:</span></span>
        - <span data-ttu-id="94e3d-1157">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="94e3d-1157">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="94e3d-1158">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1158">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1159">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1160">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1160">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1161">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1161">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1162">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1162">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="94e3d-1163">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1163">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-1164">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-1164">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-1165">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="94e3d-1165">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="94e3d-1166">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1166">Az.CognitiveServices</span></span>
* <span data-ttu-id="94e3d-1167">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1167">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="94e3d-1168">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1168">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1169">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1170">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1170">Proximity placement group feature.</span></span>
    - <span data-ttu-id="94e3d-1171">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="94e3d-1171">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="94e3d-1172">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-1172">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="94e3d-1173">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1173">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="94e3d-1174">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1174">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="94e3d-1175">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1175">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="94e3d-1176">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1176">Breaking changes</span></span>
    - <span data-ttu-id="94e3d-1177">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1177">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="94e3d-1178">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1178">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="94e3d-1179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="94e3d-1179">Az.DeploymentManager</span></span>
* <span data-ttu-id="94e3d-1180">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="94e3d-1180">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="94e3d-1181">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="94e3d-1181">Az.Dns</span></span>
* <span data-ttu-id="94e3d-1182">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1182">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="94e3d-1183">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1183">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="94e3d-1184">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1184">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="94e3d-1185">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1185">Az.FrontDoor</span></span>
* <span data-ttu-id="94e3d-1186">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="94e3d-1186">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="94e3d-1187">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="94e3d-1187">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="94e3d-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="94e3d-1188">Az.HDInsight</span></span>
* <span data-ttu-id="94e3d-1189">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="94e3d-1189">Removed two cmdlets:</span></span>
    - <span data-ttu-id="94e3d-1190">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="94e3d-1190">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="94e3d-1191">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="94e3d-1191">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="94e3d-1192">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1192">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="94e3d-1193">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="94e3d-1193">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="94e3d-1194">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1194">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="94e3d-1195">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1195">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94e3d-1196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1196">Az.Monitor</span></span>
* <span data-ttu-id="94e3d-1197">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1197">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="94e3d-1198">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="94e3d-1198">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="94e3d-1199">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="94e3d-1199">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="94e3d-1200">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="94e3d-1200">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="94e3d-1201">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1201">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="94e3d-1202">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="94e3d-1202">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="94e3d-1203">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="94e3d-1203">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="94e3d-1204">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1204">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94e3d-1205">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1205">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94e3d-1206">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1206">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94e3d-1207">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1207">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94e3d-1208">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1208">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="94e3d-1209">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1209">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="94e3d-1210">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1210">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1211">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1211">Az.Network</span></span>
* <span data-ttu-id="94e3d-1212">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="94e3d-1212">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="94e3d-1213">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1213">New cmdlets</span></span>
        - <span data-ttu-id="94e3d-1214">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="94e3d-1214">New-AzNatGateway</span></span>
        - <span data-ttu-id="94e3d-1215">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="94e3d-1215">Get-AzNatGateway</span></span>
        - <span data-ttu-id="94e3d-1216">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="94e3d-1216">Set-AzNatGateway</span></span>
        - <span data-ttu-id="94e3d-1217">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="94e3d-1217">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="94e3d-1218">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1218">Updated cmdlets</span></span>
        - <span data-ttu-id="94e3d-1219">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="94e3d-1219">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="94e3d-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="94e3d-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="94e3d-1221">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1221">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="94e3d-1222">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1222">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="94e3d-1223">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1223">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="94e3d-1224">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-1224">Az.PolicyInsights</span></span>
* <span data-ttu-id="94e3d-1225">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1225">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="94e3d-1226">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1226">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="94e3d-1227">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1227">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-1228">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1228">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-1229">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1229">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="94e3d-1230">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1230">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="94e3d-1231">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1231">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="94e3d-1232">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1232">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="94e3d-1233">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1233">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="94e3d-1234">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1234">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="94e3d-1235">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="94e3d-1235">Az.Relay</span></span>
* <span data-ttu-id="94e3d-1236">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="94e3d-1236">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="94e3d-1237">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="94e3d-1237">Az.ServiceBus</span></span>
* <span data-ttu-id="94e3d-1238">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1238">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-1239">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1239">Az.Storage</span></span>
* <span data-ttu-id="94e3d-1240">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1240">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="94e3d-1241">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1241">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="94e3d-1242">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="94e3d-1242">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="94e3d-1243">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-1243">New-AzStorageAccount</span></span>
* <span data-ttu-id="94e3d-1244">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="94e3d-1244">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="94e3d-1245">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-1245">New-AzStorageAccount</span></span>
    - <span data-ttu-id="94e3d-1246">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-1246">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="94e3d-1247">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-1247">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-1248">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1248">Az.Websites</span></span>
* <span data-ttu-id="94e3d-1249">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="94e3d-1249">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="94e3d-1250">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1250">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="94e3d-1251">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1251">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="94e3d-1252">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="94e3d-1252">Highlights since the last major release</span></span>
* <span data-ttu-id="94e3d-1253">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1253">General availability of `Az` module</span></span>
* <span data-ttu-id="94e3d-1254">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="94e3d-1254">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="94e3d-1255">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="94e3d-1255">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="94e3d-1256">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1256">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="94e3d-1257">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1257">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="94e3d-1258">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1258">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="94e3d-1259">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1259">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="94e3d-1260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-1260">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-1261">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1261">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="94e3d-1262">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="94e3d-1262">Az.Batch</span></span>
* <span data-ttu-id="94e3d-1263">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1263">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="94e3d-1264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94e3d-1264">Az.Cdn</span></span>
* <span data-ttu-id="94e3d-1265">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="94e3d-1266">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1266">Az.CognitiveServices</span></span>
* <span data-ttu-id="94e3d-1267">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1267">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1268">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1269">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1269">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="94e3d-1270">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1270">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94e3d-1271">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1271">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-1272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-1272">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-1273">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1273">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-1274">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-1274">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-1275">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1275">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="94e3d-1276">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="94e3d-1276">Az.EventGrid</span></span>
* <span data-ttu-id="94e3d-1277">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1277">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94e3d-1278">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-1278">Az.EventHub</span></span>
* <span data-ttu-id="94e3d-1279">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1279">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="94e3d-1280">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="94e3d-1280">Az.HDInsight</span></span>
* <span data-ttu-id="94e3d-1281">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1281">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94e3d-1282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-1282">Az.IotHub</span></span>
* <span data-ttu-id="94e3d-1283">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1283">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="94e3d-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94e3d-1284">Az.KeyVault</span></span>
* <span data-ttu-id="94e3d-1285">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1285">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94e3d-1286">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1286">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="94e3d-1287">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="94e3d-1287">Az.MachineLearning</span></span>
* <span data-ttu-id="94e3d-1288">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1288">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="94e3d-1289">Az.Media</span><span class="sxs-lookup"><span data-stu-id="94e3d-1289">Az.Media</span></span>
* <span data-ttu-id="94e3d-1290">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1290">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94e3d-1291">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1291">Az.Monitor</span></span>
  * <span data-ttu-id="94e3d-1292">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1292">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="94e3d-1293">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="94e3d-1293">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="94e3d-1294">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="94e3d-1294">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="94e3d-1295">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="94e3d-1295">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="94e3d-1296">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="94e3d-1296">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="94e3d-1297">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="94e3d-1297">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="94e3d-1298">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1298">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1299">Az.Network</span></span>
* <span data-ttu-id="94e3d-1300">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1300">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94e3d-1301">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1301">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="94e3d-1302">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="94e3d-1302">Az.NotificationHubs</span></span>
* <span data-ttu-id="94e3d-1303">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1303">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="94e3d-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="94e3d-1305">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1305">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="94e3d-1306">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="94e3d-1306">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="94e3d-1307">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1307">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-1309">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1309">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94e3d-1310">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1310">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="94e3d-1311">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1311">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="94e3d-1312">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1312">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="94e3d-1313">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="94e3d-1313">Az.RedisCache</span></span>
* <span data-ttu-id="94e3d-1314">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1314">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1315">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1315">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1316">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1316">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1317">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1318">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1318">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="94e3d-1319">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1319">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94e3d-1320">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1320">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="94e3d-1321">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1321">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="94e3d-1322">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1322">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="94e3d-1323">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1323">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="94e3d-1324">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1324">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-1325">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1325">Az.Websites</span></span>
* <span data-ttu-id="94e3d-1326">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1326">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="94e3d-1327">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="94e3d-1328">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1328">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="94e3d-1329">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1329">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="94e3d-1330">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1330">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="94e3d-1331">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="94e3d-1331">Highlights since the last major release</span></span>
* <span data-ttu-id="94e3d-1332">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1332">General availability of `Az` module</span></span>
* <span data-ttu-id="94e3d-1333">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="94e3d-1333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="94e3d-1334">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="94e3d-1334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="94e3d-1335">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="94e3d-1336">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="94e3d-1337">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="94e3d-1338">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="94e3d-1339">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-1339">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-1340">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1340">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="94e3d-1341">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1341">Az.AnalysisServices</span></span>
* <span data-ttu-id="94e3d-1342">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="94e3d-1342">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="94e3d-1343">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="94e3d-1343">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94e3d-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-1344">Az.Automation</span></span>
* <span data-ttu-id="94e3d-1345">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1345">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="94e3d-1346">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1346">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="94e3d-1347">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1347">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1348">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1349">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1349">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="94e3d-1350">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1350">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="94e3d-1351">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="94e3d-1351">Az.ContainerInstance</span></span>
* <span data-ttu-id="94e3d-1352">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1352">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-1353">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-1354">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1354">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="94e3d-1355">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1355">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1356">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1357">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1357">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="94e3d-1358">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1358">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="94e3d-1359">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1359">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="94e3d-1360">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="94e3d-1360">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="94e3d-1361">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1361">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="94e3d-1362">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="94e3d-1362">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1363">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1363">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1364">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1364">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-1365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1365">Az.Storage</span></span>
* <span data-ttu-id="94e3d-1366">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="94e3d-1366">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="94e3d-1367">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="94e3d-1367">New-AzStorageContext</span></span>
* <span data-ttu-id="94e3d-1368">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-1368">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="94e3d-1369">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="94e3d-1369">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="94e3d-1370">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="94e3d-1370">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="94e3d-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="94e3d-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="94e3d-1373">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-1373">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="94e3d-1374">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="94e3d-1374">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="94e3d-1375">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="94e3d-1375">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="94e3d-1376">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="94e3d-1376">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="94e3d-1377">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="94e3d-1377">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="94e3d-1378">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1378">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="94e3d-1379">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="94e3d-1379">Highlights since the last major release</span></span>
* <span data-ttu-id="94e3d-1380">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1380">General availability of `Az` module</span></span>
* <span data-ttu-id="94e3d-1381">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="94e3d-1381">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="94e3d-1382">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="94e3d-1382">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="94e3d-1383">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1383">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="94e3d-1384">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1384">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="94e3d-1385">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1385">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="94e3d-1386">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1386">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94e3d-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-1387">Az.Automation</span></span>
* <span data-ttu-id="94e3d-1388">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="94e3d-1388">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="94e3d-1389">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="94e3d-1389">Dynamic grouping</span></span>
    * <span data-ttu-id="94e3d-1390">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="94e3d-1390">Pre-Post script</span></span>
    * <span data-ttu-id="94e3d-1391">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1391">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1392">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1392">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1393">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="94e3d-1393">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="94e3d-1394">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1394">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="94e3d-1395">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94e3d-1395">Az.KeyVault</span></span>
* <span data-ttu-id="94e3d-1396">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1396">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1397">Az.Network</span></span>
* <span data-ttu-id="94e3d-1398">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1398">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="94e3d-1399">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1399">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-1400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1400">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-1401">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1401">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="94e3d-1402">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1402">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1403">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1404">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1404">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="94e3d-1405">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1405">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1406">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1407">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1407">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-1408">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1408">Az.Storage</span></span>
* <span data-ttu-id="94e3d-1409">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-1409">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="94e3d-1410">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1410">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="94e3d-1411">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1411">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="94e3d-1412">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1412">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="94e3d-1413">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="94e3d-1413">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="94e3d-1414">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="94e3d-1414">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="94e3d-1415">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1415">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-1416">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1416">Az.Websites</span></span>
* <span data-ttu-id="94e3d-1417">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1417">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="94e3d-1418">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1418">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-1419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-1419">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-1420">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1420">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="94e3d-1421">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1421">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94e3d-1422">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-1422">Az.Automation</span></span>
* <span data-ttu-id="94e3d-1423">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1423">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="94e3d-1424">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1424">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="94e3d-1425">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="94e3d-1425">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="94e3d-1426">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94e3d-1426">Az.Cdn</span></span>
* <span data-ttu-id="94e3d-1427">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1427">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1428">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1429">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1429">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-1430">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-1430">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-1431">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1431">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="94e3d-1432">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="94e3d-1432">Az.LogicApp</span></span>
* <span data-ttu-id="94e3d-1433">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="94e3d-1433">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1434">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1434">Az.Network</span></span>
* <span data-ttu-id="94e3d-1435">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1435">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-1436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1436">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-1437">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1437">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="94e3d-1438">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1438">SDK Update</span></span>
* <span data-ttu-id="94e3d-1439">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1439">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="94e3d-1440">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1440">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1441">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1442">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1442">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="94e3d-1443">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="94e3d-1443">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="94e3d-1444">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1444">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="94e3d-1445">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="94e3d-1445">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="94e3d-1446">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1446">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="94e3d-1447">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="94e3d-1447">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1448">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1449">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1449">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="94e3d-1450">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1450">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-1451">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1451">Az.Storage</span></span>
* <span data-ttu-id="94e3d-1452">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94e3d-1452">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="94e3d-1453">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1453">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="94e3d-1454">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1454">Az.AnalysisServices</span></span>
* <span data-ttu-id="94e3d-1455">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1455">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94e3d-1456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-1456">Az.Automation</span></span>
* <span data-ttu-id="94e3d-1457">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1457">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="94e3d-1458">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1458">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="94e3d-1459">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1459">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="94e3d-1460">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1460">Az.CognitiveServices</span></span>
* <span data-ttu-id="94e3d-1461">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1461">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1462">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1463">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1463">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="94e3d-1464">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1464">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="94e3d-1465">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1465">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="94e3d-1466">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1466">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-1468">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1468">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="94e3d-1469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-1469">Az.EventHub</span></span>
* <span data-ttu-id="94e3d-1470">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1470">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="94e3d-1471">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94e3d-1471">Az.KeyVault</span></span>
* <span data-ttu-id="94e3d-1472">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1472">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="94e3d-1473">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="94e3d-1473">Az.LogicApp</span></span>
* <span data-ttu-id="94e3d-1474">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1474">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="94e3d-1475">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1475">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="94e3d-1476">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1476">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="94e3d-1477">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="94e3d-1477">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="94e3d-1478">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="94e3d-1478">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="94e3d-1479">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="94e3d-1479">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="94e3d-1480">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="94e3d-1480">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="94e3d-1481">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1481">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="94e3d-1482">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="94e3d-1482">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="94e3d-1483">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="94e3d-1483">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="94e3d-1484">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="94e3d-1484">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="94e3d-1485">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="94e3d-1485">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="94e3d-1486">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1486">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="94e3d-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1487">Az.Monitor</span></span>
* <span data-ttu-id="94e3d-1488">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1488">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1489">Az.Network</span></span>
* <span data-ttu-id="94e3d-1490">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1490">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="94e3d-1491">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-1491">Az.OperationalInsights</span></span>
* <span data-ttu-id="94e3d-1492">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1492">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="94e3d-1493">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1493">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="94e3d-1494">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1494">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="94e3d-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1495">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1496">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1496">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="94e3d-1497">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1497">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="94e3d-1498">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1498">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="94e3d-1499">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1499">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1500">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1501">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1501">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="94e3d-1502">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1502">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-1503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1503">Az.Websites</span></span>
* <span data-ttu-id="94e3d-1504">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1504">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="94e3d-1505">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1505">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-1506">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-1506">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-1507">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="94e3d-1507">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="94e3d-1508">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1508">Az.AnalysisServices</span></span>
<span data-ttu-id="94e3d-1509">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1509">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1510">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1510">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1511">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1511">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="94e3d-1512">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1512">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="94e3d-1513">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1513">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-1514">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1514">Az.RecoveryServices</span></span>
<span data-ttu-id="94e3d-1515">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1515">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1516">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1517">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1517">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="94e3d-1518">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="94e3d-1518">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="94e3d-1519">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1519">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="94e3d-1520">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="94e3d-1520">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1521">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1522">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1522">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="94e3d-1523">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1523">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="94e3d-1524">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1524">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="94e3d-1525">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1525">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-1526">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-1526">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-1527">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="94e3d-1527">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="94e3d-1528">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1528">Az.AnalysisServices</span></span>
* <span data-ttu-id="94e3d-1529">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="94e3d-1529">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-1530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1530">Az.RecoveryServices</span></span>
* <span data-ttu-id="94e3d-1531">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="94e3d-1531">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="94e3d-1532">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1532">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-1533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-1533">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-1534">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1534">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="94e3d-1535">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="94e3d-1536">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1536">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="94e3d-1537">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="94e3d-1537">Az.Aks</span></span>
* <span data-ttu-id="94e3d-1538">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1538">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="94e3d-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-1539">Az.Automation</span></span>
* <span data-ttu-id="94e3d-1540">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1540">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="94e3d-1541">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1541">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="94e3d-1542">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="94e3d-1542">Az.Cdn</span></span>
* <span data-ttu-id="94e3d-1543">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1543">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1544">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1544">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1545">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1545">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="94e3d-1546">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1546">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="94e3d-1547">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1547">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="94e3d-1548">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="94e3d-1548">Az.ContainerRegistry</span></span>
* <span data-ttu-id="94e3d-1549">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1549">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="94e3d-1550">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="94e3d-1550">Az.DataFactory</span></span>
* <span data-ttu-id="94e3d-1551">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1551">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-1552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-1552">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-1553">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1553">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="94e3d-1554">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="94e3d-1554">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="94e3d-1555">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1555">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94e3d-1556">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-1556">Az.IotHub</span></span>
* <span data-ttu-id="94e3d-1557">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1557">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="94e3d-1558">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94e3d-1558">Az.KeyVault</span></span>
* <span data-ttu-id="94e3d-1559">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1559">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1560">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1560">Az.Network</span></span>
* <span data-ttu-id="94e3d-1561">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1561">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1562">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1563">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1563">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="94e3d-1564">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1564">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="94e3d-1565">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1565">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="94e3d-1566">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1566">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="94e3d-1567">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1567">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="94e3d-1568">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1568">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="94e3d-1569">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="94e3d-1569">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="94e3d-1570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-1570">Az.ServiceFabric</span></span>
* <span data-ttu-id="94e3d-1571">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="94e3d-1571">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="94e3d-1572">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1572">Fix some error messages.</span></span>
* <span data-ttu-id="94e3d-1573">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1573">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="94e3d-1574">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1574">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="94e3d-1575">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="94e3d-1575">Az.SignalR</span></span>
* <span data-ttu-id="94e3d-1576">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1576">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1577">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1578">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1578">Update incorrect online help URLs</span></span>
* <span data-ttu-id="94e3d-1579">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1579">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="94e3d-1580">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1580">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="94e3d-1581">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-1581">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-1582">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1582">Az.Storage</span></span>
* <span data-ttu-id="94e3d-1583">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1583">Update incorrect online help URLs</span></span>
* <span data-ttu-id="94e3d-1584">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1584">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="94e3d-1585">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="94e3d-1585">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="94e3d-1586">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="94e3d-1586">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="94e3d-1587">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="94e3d-1587">Az.TrafficManager</span></span>
* <span data-ttu-id="94e3d-1588">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1588">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-1589">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1589">Az.Websites</span></span>
* <span data-ttu-id="94e3d-1590">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1590">Update incorrect online help URLs</span></span>
* <span data-ttu-id="94e3d-1591">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1591">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="94e3d-1592">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1592">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="94e3d-1593">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="94e3d-1593">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="94e3d-1594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-1594">Az.Accounts</span></span>
* <span data-ttu-id="94e3d-1595">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1595">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1596">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1596">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1597">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1597">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="94e3d-1598">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1598">Updated the description of ID in help files</span></span>
* <span data-ttu-id="94e3d-1599">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="94e3d-1599">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-1601">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1601">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="94e3d-1602">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1602">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="94e3d-1603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="94e3d-1603">Az.EventGrid</span></span>
* <span data-ttu-id="94e3d-1604">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1604">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="94e3d-1605">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1605">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="94e3d-1606">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-1606">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="94e3d-1607">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="94e3d-1607">Event Time-To-Live,</span></span>
        - <span data-ttu-id="94e3d-1608">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="94e3d-1608">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="94e3d-1609">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1609">Dead letter endpoint.</span></span>
    - <span data-ttu-id="94e3d-1610">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-1610">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="94e3d-1611">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="94e3d-1611">Event Time-To-Live,</span></span>
        - <span data-ttu-id="94e3d-1612">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="94e3d-1612">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="94e3d-1613">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1613">Dead letter endpoint.</span></span>
* <span data-ttu-id="94e3d-1614">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1614">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="94e3d-1615">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1615">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="94e3d-1616">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="94e3d-1616">Az.IotHub</span></span>
* <span data-ttu-id="94e3d-1617">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1617">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="94e3d-1618">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="94e3d-1618">Az.LogicApp</span></span>
* <span data-ttu-id="94e3d-1619">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1619">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1620">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1620">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1621">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1621">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="94e3d-1622">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="94e3d-1622">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="94e3d-1623">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1623">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="94e3d-1624">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1624">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="94e3d-1625">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1625">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="94e3d-1626">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="94e3d-1626">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="94e3d-1627">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="94e3d-1627">Az.SignalR</span></span>
* <span data-ttu-id="94e3d-1628">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="94e3d-1628">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1629">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1630">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1630">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="94e3d-1631">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1631">Az.Storage</span></span>
* <span data-ttu-id="94e3d-1632">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1632">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="94e3d-1633">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="94e3d-1633">New-AzStorageContext</span></span>
* <span data-ttu-id="94e3d-1634">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1634">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="94e3d-1635">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="94e3d-1635">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1636">Az.Websites</span></span>
* <span data-ttu-id="94e3d-1637">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1637">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="94e3d-1638">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="94e3d-1638">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="94e3d-1639">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="94e3d-1639">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="94e3d-1640">Genel</span><span class="sxs-lookup"><span data-stu-id="94e3d-1640">General</span></span>

- <span data-ttu-id="94e3d-1641">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1641">General Availability of Az Module</span></span>
- <span data-ttu-id="94e3d-1642">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="94e3d-1642">Online help for each module</span></span>
- <span data-ttu-id="94e3d-1643">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1643">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="94e3d-1644">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1644">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="94e3d-1645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="94e3d-1645">Az.Accounts</span></span>
- <span data-ttu-id="94e3d-1646">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="94e3d-1646">Changed from Az.Profile</span></span>
- <span data-ttu-id="94e3d-1647">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1647">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="94e3d-1648">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94e3d-1648">Az.ApiManagement</span></span>
- <span data-ttu-id="94e3d-1649">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="94e3d-1649">Fixes for #7002</span></span>
- <span data-ttu-id="94e3d-1650">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1650">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="94e3d-1651">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="94e3d-1651">Az.Batch</span></span>
- <span data-ttu-id="94e3d-1652">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1652">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="94e3d-1653">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1653">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="94e3d-1654">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="94e3d-1655">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="94e3d-1655">Az.Billing</span></span>
- <span data-ttu-id="94e3d-1656">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1656">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="94e3d-1657">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1657">Az.CognitivServices</span></span>
- <span data-ttu-id="94e3d-1658">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1658">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="94e3d-1659">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1659">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="94e3d-1660">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="94e3d-1660">Az.ContainerInstance</span></span>
- <span data-ttu-id="94e3d-1661">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1661">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="94e3d-1662">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="94e3d-1662">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="94e3d-1663">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1663">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-1664">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-1664">Az.DataLakeStore</span></span>
- <span data-ttu-id="94e3d-1665">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1665">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="94e3d-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1666">Az.Monitor</span></span>
- <span data-ttu-id="94e3d-1667">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1667">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="94e3d-1668">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="94e3d-1668">Az.KeyVault</span></span>
- <span data-ttu-id="94e3d-1669">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1669">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="94e3d-1670">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="94e3d-1670">Az.MachineLearning</span></span>
- <span data-ttu-id="94e3d-1671">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1671">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="94e3d-1672">Az.Media</span><span class="sxs-lookup"><span data-stu-id="94e3d-1672">Az.Media</span></span>
- <span data-ttu-id="94e3d-1673">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1673">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="94e3d-1674">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1674">Az.Network</span></span>
<span data-ttu-id="94e3d-1675">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1675">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="94e3d-1676">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="94e3d-1676">New cmdlets added:</span></span>
        - <span data-ttu-id="94e3d-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94e3d-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94e3d-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94e3d-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94e3d-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94e3d-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94e3d-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94e3d-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94e3d-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="94e3d-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="94e3d-1682">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1682">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="94e3d-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="94e3d-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="94e3d-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="94e3d-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="94e3d-1685">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1685">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="94e3d-1686">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94e3d-1686">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="94e3d-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="94e3d-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="94e3d-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="94e3d-1689">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-1689">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="94e3d-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="94e3d-1691">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="94e3d-1692">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1692">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="94e3d-1693">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94e3d-1693">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="94e3d-1694">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94e3d-1694">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="94e3d-1695">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="94e3d-1695">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="94e3d-1696">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1696">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="94e3d-1697">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1697">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="94e3d-1698">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-1698">Az.OperationalInsights</span></span>
- <span data-ttu-id="94e3d-1699">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1699">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="94e3d-1700">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="94e3d-1700">Az.Profile</span></span>
- <span data-ttu-id="94e3d-1701">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1701">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-1702">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1702">Az.RecoveryServices</span></span>
- <span data-ttu-id="94e3d-1703">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1703">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="94e3d-1704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1704">Az.Resources</span></span>
- <span data-ttu-id="94e3d-1705">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1705">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="94e3d-1706">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-1706">Az.ServiceFabric</span></span>
- <span data-ttu-id="94e3d-1707">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="94e3d-1707">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="94e3d-1708">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1708">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="94e3d-1709">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="94e3d-1709">Az.SIgnalR</span></span>
- <span data-ttu-id="94e3d-1710">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1710">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="94e3d-1711">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1711">Az.Sql</span></span>
- <span data-ttu-id="94e3d-1712">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1712">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="94e3d-1713">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1713">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="94e3d-1714">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1714">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="94e3d-1715">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1715">Az.Storage</span></span>
- <span data-ttu-id="94e3d-1716">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="94e3d-1717">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1717">Az.Websites</span></span>
- <span data-ttu-id="94e3d-1718">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="94e3d-1718">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="94e3d-1719">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="94e3d-1719">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="94e3d-1720">Genel</span><span class="sxs-lookup"><span data-stu-id="94e3d-1720">General</span></span>

* <span data-ttu-id="94e3d-1721">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1721">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="94e3d-1722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1722">Az.Compute</span></span>

* <span data-ttu-id="94e3d-1723">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1723">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-1724">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-1724">Az.DataLakeStore</span></span>

* <span data-ttu-id="94e3d-1725">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1725">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="94e3d-1726">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1726">Az.FrontDoor</span></span>

* <span data-ttu-id="94e3d-1727">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1727">Fixed some broken links</span></span>
    - <span data-ttu-id="94e3d-1728">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1728">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="94e3d-1729">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1729">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="94e3d-1730">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1730">Az.RecoveryServices</span></span>

* <span data-ttu-id="94e3d-1731">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1731">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="94e3d-1732">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1732">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="94e3d-1733">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1733">Az.Resources</span></span>

* <span data-ttu-id="94e3d-1734">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1734">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="94e3d-1735">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1735">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="94e3d-1736">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1736">Az.Sql</span></span>

* <span data-ttu-id="94e3d-1737">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="94e3d-1737">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="94e3d-1738">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1738">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="94e3d-1739">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1739">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="94e3d-1740">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1740">Az.Storage</span></span>

* <span data-ttu-id="94e3d-1741">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1741">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="94e3d-1742">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1742">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="94e3d-1743">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1743">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="94e3d-1744">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1744">Support Static Website configuration</span></span>
    - <span data-ttu-id="94e3d-1745">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="94e3d-1745">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="94e3d-1746">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="94e3d-1746">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="94e3d-1747">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1747">Az.Websites</span></span>

* <span data-ttu-id="94e3d-1748">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="94e3d-1748">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="94e3d-1749">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1749">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="94e3d-1750">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1750">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="94e3d-1751">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="94e3d-1751">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="94e3d-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="94e3d-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="94e3d-1753">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1753">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="94e3d-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="94e3d-1754">Az.Automation</span></span>
* <span data-ttu-id="94e3d-1755">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="94e3d-1755">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="94e3d-1756">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1756">Added Update Management cmdlets</span></span>
* <span data-ttu-id="94e3d-1757">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1757">Added Source Control cmdlets</span></span>
* <span data-ttu-id="94e3d-1758">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1758">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="94e3d-1759">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1759">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="94e3d-1760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1760">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1761">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1761">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="94e3d-1762">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1762">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="94e3d-1763">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="94e3d-1763">Az.ContainerInstance</span></span>
* <span data-ttu-id="94e3d-1764">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1764">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="94e3d-1765">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="94e3d-1765">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="94e3d-1766">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1766">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="94e3d-1767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1767">Az.Network</span></span>
* <span data-ttu-id="94e3d-1768">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1768">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="94e3d-1769">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1769">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="94e3d-1770">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1770">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="94e3d-1771">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1771">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="94e3d-1772">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="94e3d-1772">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="94e3d-1773">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1773">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="94e3d-1774">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1774">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="94e3d-1775">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="94e3d-1775">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="94e3d-1776">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1776">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="94e3d-1777">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="94e3d-1777">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="94e3d-1778">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="94e3d-1778">Az.Relay</span></span>
* <span data-ttu-id="94e3d-1779">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1779">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="94e3d-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1780">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1781">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1781">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="94e3d-1782">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1782">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="94e3d-1783">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="94e3d-1783">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="94e3d-1784">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-1784">Az.ServiceFabric</span></span>
* <span data-ttu-id="94e3d-1785">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1785">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="94e3d-1786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1786">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1787">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1787">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="94e3d-1788">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="94e3d-1788">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="94e3d-1789">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="94e3d-1789">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="94e3d-1790">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="94e3d-1790">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="94e3d-1791">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="94e3d-1791">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="94e3d-1792">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="94e3d-1792">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="94e3d-1793">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="94e3d-1793">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="94e3d-1794">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="94e3d-1794">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="94e3d-1795">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="94e3d-1795">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="94e3d-1796">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1796">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="94e3d-1797">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1797">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="94e3d-1798">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1798">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="94e3d-1799">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1799">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="94e3d-1800">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1800">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="94e3d-1801">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1801">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="94e3d-1802">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1802">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="94e3d-1803">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1803">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="94e3d-1804">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="94e3d-1804">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="94e3d-1805">Genel</span><span class="sxs-lookup"><span data-stu-id="94e3d-1805">General</span></span>
* <span data-ttu-id="94e3d-1806">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="94e3d-1806">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="94e3d-1807">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="94e3d-1807">Az.Profile</span></span>
* <span data-ttu-id="94e3d-1808">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1808">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="94e3d-1809">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1809">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="94e3d-1810">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1810">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="94e3d-1811">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1811">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="94e3d-1812">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1812">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="94e3d-1813">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1813">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="94e3d-1814">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1814">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="94e3d-1815">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1815">Az.CognitiveServices</span></span>
* <span data-ttu-id="94e3d-1816">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1816">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1817">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1818">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1818">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="94e3d-1819">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1819">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="94e3d-1820">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1820">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-1821">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-1821">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-1822">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1822">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="94e3d-1823">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1823">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="94e3d-1824">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="94e3d-1824">Az.Insights</span></span>
* <span data-ttu-id="94e3d-1825">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1825">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="94e3d-1826">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="94e3d-1826">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="94e3d-1827">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1827">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="94e3d-1828">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1828">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1829">Az.Network</span></span>
* <span data-ttu-id="94e3d-1830">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="94e3d-1830">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="94e3d-1831">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="94e3d-1831">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="94e3d-1832">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="94e3d-1832">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="94e3d-1833">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="94e3d-1833">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="94e3d-1834">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="94e3d-1834">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="94e3d-1835">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="94e3d-1835">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="94e3d-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="94e3d-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="94e3d-1837">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="94e3d-1837">Az.PolicyInsights</span></span>
* <span data-ttu-id="94e3d-1838">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1838">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1839">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1840">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1840">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="94e3d-1841">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="94e3d-1841">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="94e3d-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="94e3d-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="94e3d-1843">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1843">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="94e3d-1844">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="94e3d-1844">Az.ServiceFabric</span></span>
* <span data-ttu-id="94e3d-1845">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1845">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="94e3d-1846">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1846">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="94e3d-1847">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="94e3d-1847">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="94e3d-1848">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="94e3d-1848">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="94e3d-1849">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1849">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="94e3d-1850">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="94e3d-1850">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="94e3d-1851">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="94e3d-1851">Az.Profile</span></span>
* <span data-ttu-id="94e3d-1852">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="94e3d-1852">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="94e3d-1853">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1853">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1854">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1855">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1855">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="94e3d-1856">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1856">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="94e3d-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="94e3d-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="94e3d-1858">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="94e3d-1858">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="94e3d-1859">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1859">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="94e3d-1860">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1860">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="94e3d-1861">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="94e3d-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1863">Az.Network</span></span>
* <span data-ttu-id="94e3d-1864">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1864">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="94e3d-1865">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1865">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1866">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1866">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1867">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1867">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="94e3d-1868">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1868">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="94e3d-1869">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="94e3d-1869">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="94e3d-1870">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="94e3d-1870">Azure.Storage</span></span>
* <span data-ttu-id="94e3d-1871">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="94e3d-1871">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="94e3d-1872">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1872">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="94e3d-1873">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="94e3d-1873">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="94e3d-1874">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1874">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="94e3d-1875">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="94e3d-1875">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="94e3d-1876">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="94e3d-1876">Az.CognitiveServices</span></span>
* <span data-ttu-id="94e3d-1877">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1877">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="94e3d-1878">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="94e3d-1878">Az.Compute</span></span>
* <span data-ttu-id="94e3d-1879">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1879">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="94e3d-1880">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1880">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="94e3d-1881">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1881">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="94e3d-1882">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="94e3d-1882">Az.DataFactoryV2</span></span>
* <span data-ttu-id="94e3d-1883">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1883">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="94e3d-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="94e3d-1884">Az.Network</span></span>
* <span data-ttu-id="94e3d-1885">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1885">Added NetworkProfile functionality.</span></span> <span data-ttu-id="94e3d-1886">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1886">new cmdlets added</span></span>
    - <span data-ttu-id="94e3d-1887">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94e3d-1887">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="94e3d-1888">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94e3d-1888">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="94e3d-1889">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94e3d-1889">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="94e3d-1890">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="94e3d-1890">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="94e3d-1891">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-1891">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="94e3d-1892">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="94e3d-1892">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="94e3d-1893">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1893">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="94e3d-1894">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1894">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="94e3d-1895">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1895">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="94e3d-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="94e3d-1896">Az.RedisCache</span></span>
* <span data-ttu-id="94e3d-1897">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="94e3d-1897">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="94e3d-1898">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1898">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="94e3d-1899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="94e3d-1899">Az.Resources</span></span>
* <span data-ttu-id="94e3d-1900">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1900">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="94e3d-1901">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1901">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="94e3d-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="94e3d-1902">Az.Sql</span></span>
* <span data-ttu-id="94e3d-1903">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="94e3d-1903">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="94e3d-1904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="94e3d-1904">Az.Websites</span></span>
* <span data-ttu-id="94e3d-1905">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1905">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="94e3d-1906">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="94e3d-1906">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="94e3d-1907">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="94e3d-1907">0.2.0 - September 2018</span></span>
 <span data-ttu-id="94e3d-1908">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="94e3d-1908">Initial Release</span></span>
