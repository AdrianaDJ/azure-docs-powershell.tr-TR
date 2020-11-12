---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ea374b23e85c16393e5de16b043ae0c28545cb61
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408080"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="48421-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="48421-103">Azure PowerShell release notes</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="48421-104">4.8.0 - Ekim 2020</span><span class="sxs-lookup"><span data-stu-id="48421-104">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-105">Az.Accounts</span></span>
* <span data-ttu-id="48421-106">Ortak kitaplıklardaki DateTime ayrıştırma sorunu düzeltildi [#13045]</span><span class="sxs-lookup"><span data-stu-id="48421-106">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-107">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-107">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-108">'New-AzCognitiveServicesAccountApiProperty' cmdlet'i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-108">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="48421-109">'New-AzCognitiveServicesAccount' ve 'Set-AzCognitiveServicesAccount' için 'ApiProperty' parametresi destekleniyor</span><span class="sxs-lookup"><span data-stu-id="48421-109">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-110">Az.Compute</span></span>
* <span data-ttu-id="48421-111">'Update-ASRRecoveryPlan' cmdlet'indeki sorun Yük Devretme Türleri doldurularak düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-111">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="48421-112">'Get-AzVmImage' cmdlet'ine isteğe bağlı '-Top' ve '-OrderBy' parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-112">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="48421-113">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="48421-113">Az.Databricks</span></span>
* <span data-ttu-id="48421-114">'Az.Databricks' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-114">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="48421-115">Sanal ağ eşlemesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-115">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-116">Az.DataFactory</span></span>
* <span data-ttu-id="48421-117">Çıkış iletilerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-117">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-118">Az.EventHub</span></span>
* <span data-ttu-id="48421-119">'Set-AzEventHubNetworkRuleSet' cmdlet'ine isteğe bağlı 'TrustedServiceAccessEnabled' anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-119">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-120">Az.HDInsight</span></span>
* <span data-ttu-id="48421-121">'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametrelerini kullanımdan kaldırma planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-121">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="48421-122">'DefaultStorageAccountName' parametresini 'StorageAccountResourceId' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-122">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="48421-123">'DefaultStorageAccountKey' parametresini 'StorageAccountKey' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-123">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="48421-124">'DefaultStorageAccountType' parametresini 'StorageAccountType' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-124">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="48421-125">'DefaultStorageContainer' parametresini 'StorageContainer' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-125">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="48421-126">'DefaultStorageRootPath' parametresini 'StorageRootPath' ile değiştirme planlaması için uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-126">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-127">Az.IotHub</span></span>
* <span data-ttu-id="48421-128">Cihazların sdk'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-128">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-129">Az.KeyVault</span></span>
* <span data-ttu-id="48421-130">SecretValueText özelliğinin kaldırılacağı ayrıntılı tarih sağlandı</span><span class="sxs-lookup"><span data-stu-id="48421-130">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="48421-131">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="48421-131">Az.ManagedServices</span></span>
* <span data-ttu-id="48421-132">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-132">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-133">Az.Monitor</span></span>
* <span data-ttu-id="48421-134">Uyarı iletisinin gizlenememesi hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-134">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="48421-135">[#12889]</span><span class="sxs-lookup"><span data-stu-id="48421-135">[#12889]</span></span>
* <span data-ttu-id="48421-136">Uyarı kuralı ölçütlerinde 'SkipMetricValidation' parametresi destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="48421-136">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="48421-137">Ölçüm doğrulamasının atlanmasına neden olarak henüz yayılmamış özel bir ölçümle ilgili uyarı kuralı oluşturmaya olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="48421-137">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-138">Az.Network</span></span>
* <span data-ttu-id="48421-139">VPNSite Kaynağına Office365 İlkesi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-139">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="48421-140">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="48421-140">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-141">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-142">İş yükü yedeklemesi için kapsayıcı adı doğrulaması eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-142">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="48421-143">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="48421-143">Az.RedisCache</span></span>
* <span data-ttu-id="48421-144">Microsoft.Cache RP kaydıyla ilgili izin sorunundan dolayı 'New-AzRedisCache' ve 'Set-AzRedisCache' cmdlet'lerinin başarısız olmaması sağlandı</span><span class="sxs-lookup"><span data-stu-id="48421-144">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-145">Az.Sql</span></span>
* <span data-ttu-id="48421-146">Aşağıdakilere BackupStorageRedundancy eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-146">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="48421-147">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="48421-147">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="48421-148">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="48421-148">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="48421-149">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="48421-149">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="48421-150">Tüm SQL DB başvurularında BackupStorageRedundancy parametresi için büyük/küçük harf duyarlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-150">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="48421-151">BackupStorageRedundancy uyarı iletisi adları güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-151">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-152">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-152">Az.Storage</span></span>
* <span data-ttu-id="48421-153">Depolama hesabının dosya hizmetinde paylaşımı etkinleştirme/devre dışı bırakma/alma geçici silme özellikleri destekleniyor</span><span class="sxs-lookup"><span data-stu-id="48421-153">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="48421-154">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="48421-154">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="48421-155">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="48421-155">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="48421-156">Desteklenen liste dosya paylaşımları Depolama hesabının silinmiş olan dosyalarını içeriyor ve Tek dosya paylaşımı kullanımı alınıyor</span><span class="sxs-lookup"><span data-stu-id="48421-156">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="48421-157">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="48421-157">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="48421-158">Silinmiş dosya paylaşımını geri yükleme destekleniyor</span><span class="sxs-lookup"><span data-stu-id="48421-158">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="48421-159">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="48421-159">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="48421-160">Blob hizmeti özelliklerini değiştirmeye yönelik cmdlet'ler değiştirildi. Sunucudan ilk özellikler alınmayacak, yalnızca değiştirilen özellikler sunucuya ayarlanacak.</span><span class="sxs-lookup"><span data-stu-id="48421-160">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="48421-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="48421-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="48421-163">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-163">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="48421-164">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-164">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="48421-165">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="48421-165">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="48421-166">New-AzStorageAccount parametresi -Kind varsayılan değeri için yardım sorunu düzeltildi [#12189]</span><span class="sxs-lookup"><span data-stu-id="48421-166">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="48421-167">Blob karşıya yüklemesinde doğru ContentType ayarlama işlemini göstermek için örnek eklenerek sorun düzeltildi [#12989]</span><span class="sxs-lookup"><span data-stu-id="48421-167">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="48421-168">4.7.0 - Eylül 2020</span><span class="sxs-lookup"><span data-stu-id="48421-168">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-169">Az.Accounts</span></span>
* <span data-ttu-id="48421-170">Yaklaşan yeni değişiklik iletileri biçimlendirildi</span><span class="sxs-lookup"><span data-stu-id="48421-170">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="48421-171">Azure.Core 1.4.1 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-171">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="48421-172">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="48421-172">Az.Aks</span></span>
* <span data-ttu-id="48421-173">'New-AzAksCluster', 'Set-AzAksCluster' ve 'New-AzAksNodePool' için istemci tarafı parametre doğrulama mantığı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-173">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="48421-174">[#12372]</span><span class="sxs-lookup"><span data-stu-id="48421-174">[#12372]</span></span>
* <span data-ttu-id="48421-175">'New-AzAksCluster' cmdlet’inde eklentilere yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-175">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="48421-176">[#11239]</span><span class="sxs-lookup"><span data-stu-id="48421-176">[#11239]</span></span>
* <span data-ttu-id="48421-177">Eklentiler için 'Enable-AzAksAddOn' ve 'Disable-AzAksAddOn' cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-177">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="48421-178">[#11239]</span><span class="sxs-lookup"><span data-stu-id="48421-178">[#11239]</span></span>
* <span data-ttu-id="48421-179">'New-AzAksCluster' için 'GenerateSshKey' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-179">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="48421-180">[#12371]</span><span class="sxs-lookup"><span data-stu-id="48421-180">[#12371]</span></span>
* <span data-ttu-id="48421-181">API sürümü 2020-06-01 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-181">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-182">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-183">Belirli API’ler için ek yasal koşullar gösterildi.</span><span class="sxs-lookup"><span data-stu-id="48421-183">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-184">Az.Compute</span></span>
* <span data-ttu-id="48421-185">'New-AzVmDiskEncryptionSetConfig' için isteğe bağlı '-EncryptionType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-185">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="48421-186">Yeni kaynak türü için yeni cmdlet’ler: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="48421-186">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="48421-187">'New-AzSnapshotConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-187">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="48421-188">'New-AzDiskConfig' cmdlet’ine isteğe bağlı '-DiskAccessId' ve '-NetworkAccessPolicy' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-188">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="48421-189">VirtualMachine Örnek Görünümüne 'PatchStatus' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-189">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="48421-190">'Get-AzVm' cmdlet’i '-Status' ile çağrıldığında döndürülen nesne olan 'VMHealth' özelliği, sanal makinenin örnek görünümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-190">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="48421-191">'Get-AzVM' ve 'Get-AzVmss' örnek görünümlerine 'AssignedHost' alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-191">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="48421-192">Alan, sanal makine örneğinin kaynak kimliğini gösterir</span><span class="sxs-lookup"><span data-stu-id="48421-192">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="48421-193">'New-AzHostGroup' cmdlet’ine isteğe bağlı '-SupportAutomaticPlacement' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-193">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="48421-194">'New-AzVm' ve 'New-AzVmss' cmdlet’lerine '-HostGroupId' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-194">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-195">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-195">Az.DataFactory</span></span>
* <span data-ttu-id="48421-196">ADF .NET SDK’sı 4.11.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-196">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-197">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-197">Az.EventHub</span></span>
* <span data-ttu-id="48421-198">Yeni 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions' Cluster cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-198">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="48421-199">#10722 numaralı soruna yönelik aşağıdaki düzeltmeler yapıldı: AuthorizationRule haklarına yalnızca 'Listen' atanabilecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-199">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="48421-200">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="48421-200">Az.Functions</span></span>
* <span data-ttu-id="48421-201">Desteklemeyen bölgelerde v2 İşlevleri oluşturma özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-201">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="48421-202">PowerShell 6.2 sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-202">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="48421-203">Kullanıcı PowerShell 6.2 işlev uygulaması oluşturduğunda, bunun yerine PowerShell 7.0 işlev uygulaması oluşturmasını öneren bir uyarı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-203">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-204">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-204">Az.HDInsight</span></span>
* <span data-ttu-id="48421-205">Otomatik ölçeklendirme yapılandırmasıyla küme oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-205">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="48421-206">'New-AzHDInsightCluster' cmdlet’ine yeni 'AutoscaleConfiguration' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-206">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="48421-207">Kümenin Otomatik ölçeklendirme yapılandırmasını çalıştırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-207">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="48421-208">Yeni 'Get-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-208">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="48421-209">Yeni 'New-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-209">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="48421-210">Yeni 'Set-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-210">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="48421-211">Yeni 'Remove-AzHDInsihgtClusterAutoscaleConfiguration' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-211">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="48421-212">Yeni 'New-AzHDInsihgtClusterAutoscaleScheduleCondition' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-212">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-213">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-213">Az.KeyVault</span></span>
* <span data-ttu-id="48421-214">RBAC yetkilendirmesi desteği eklendi [#10557]</span><span class="sxs-lookup"><span data-stu-id="48421-214">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="48421-215">'Set-AzKeyVaultAccessPolicy' cmdlet’indeki hata işleme özelliği iyileştirildi [#4007]</span><span class="sxs-lookup"><span data-stu-id="48421-215">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="48421-216">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="48421-216">Az.Kusto</span></span>
* <span data-ttu-id="48421-217">'Az.Kusto' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-217">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-218">Az.Network</span></span>
* <span data-ttu-id="48421-219">[Yeni Değişiklik] Aşağıdaki cmdlet’ler, kaynak sanal yönlendiricisini ve sanal merkezi uyumlu hale getirecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-219">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="48421-220">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="48421-220">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="48421-221">IP yapılandırması alt kaynağını desteklemek için -HostedSubnet parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-221">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="48421-222">-HostedGateway ve -HostedGatewayId parametreleri silindi</span><span class="sxs-lookup"><span data-stu-id="48421-222">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="48421-223">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="48421-223">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="48421-224">Abonelik düzeyi parametre kümesi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-224">Added subscription level parameter set</span></span>
    - <span data-ttu-id="48421-225">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="48421-225">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="48421-226">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="48421-226">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="48421-227">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="48421-227">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="48421-228">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="48421-228">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="48421-229">Azure ExpressRoute Bağlantı Noktası için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-229">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="48421-230">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="48421-230">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="48421-231">VirtualNetwork Eşleme Kaynağına RemoteBgpCommunities özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-231">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="48421-232">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-232">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="48421-233">'Get-AzVpnGateway' çıkışına VpnGatewayIpConfigurations eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-233">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="48421-234">'Set-AzApplicationGatewaySslCertificate' ile ilgili hata düzeltildi [#9488]</span><span class="sxs-lookup"><span data-stu-id="48421-234">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="48421-235">'AzureFirewall' öğesine 'AllowActiveFTP' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-235">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="48421-236">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde internet güvenliğini ayarlama/kaldırma özelliği etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-236">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="48421-237">'New-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirmek için true olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-237">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="48421-238">'Update-AzP2sVpnGateway' güncelleştirildi: Müşterilerin P2SVpnGateway üzerinde internet güvenliğini etkinleştirip devre dışı bırakmak için true/false olarak ayarlayacakları, Noktadan siteye istemcilere uygulanacak olan isteğe bağlı 'EnableInternetSecurityFlag' veya 'DisableInternetSecurityFlag' anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-238">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="48421-239">Müşterilerin sorun giderme amacıyla VirtualWan P2SVpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzP2sVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-239">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="48421-240">Müşterilerin sorun giderme amacıyla VirtualWan VpnGateway’lerini sıfırlamalarını/yeniden başlatmalarını sağlayan yeni 'Reset-AzVpnGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-240">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="48421-241">'Set-AzVirtualNetworkSubnetConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-241">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="48421-242">Parametrelerde açıkça ayarlanmışsa alt ağın NSG ve Yönlendirme Tablosu özelliklerinin null olarak ayarlanması [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="48421-242">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-243">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-243">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-244">İş yükü Yedekleme Öğeleri için Silme Durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-244">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-245">Az.Resources</span></span>
* <span data-ttu-id="48421-246">Eksik olan denetim Set-AzRoleAssignment cmdlet’ine eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-246">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="48421-247">'Get-AzResourceGroupDeploymentOperation' cmdlet’inin 'SubscriptionId' parametresine hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-247">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="48421-248">ARM şablonu What-If cmdlet’leri 'Ignore' kaynak değişiklikleri son olarak gösterilecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-248">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="48421-249">Dağıtım cmdlet’lerindeki güvenlik ve dizi parametresi serileştirme sorunları düzeltildi [#12773]</span><span class="sxs-lookup"><span data-stu-id="48421-249">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-250">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-250">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-251">Yönetilen kümeler ve düğüm türleri için yeni cmdlet’ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-251">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="48421-252">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="48421-252">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="48421-253">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="48421-253">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="48421-254">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="48421-254">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="48421-255">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="48421-255">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="48421-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="48421-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="48421-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="48421-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="48421-258">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="48421-258">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="48421-259">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="48421-259">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="48421-260">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="48421-260">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="48421-261">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="48421-261">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="48421-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="48421-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="48421-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="48421-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="48421-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="48421-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="48421-265">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="48421-265">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="48421-266">Service Fabric SDK’sı, geçerli model için Service Fabric kaynak sağlayıcısı 2020-03-01 API sürümünü kullanan 1.2.0 sürümüne, yönetilen kümeler için 2020-01-01-preview sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-266">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-267">Az.Sql</span></span>
* <span data-ttu-id="48421-268">'New-AzSqlInstance' ve 'Get-AzSqlInstance' cmdlet’lerine BackupStorageRedundancy eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-268">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="48421-269">'Get-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-269">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="48421-270">'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-270">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="48421-271">'New-AzSqlInstance' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-271">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="48421-272">Yönetilen Veritabanı Günlük Yeniden Oynatma hizmetine cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-272">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="48421-273">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="48421-273">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="48421-274">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="48421-274">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="48421-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="48421-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="48421-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="48421-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="48421-277">'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-277">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="48421-278">'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-278">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="48421-279">'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-279">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="48421-280">Ağ yalıtım işlevselliğini desteklemek için 'New-AzSqlDatabaseImport' ve 'New-AzSqlDatabaseExport' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-280">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="48421-281">'New-AzSqlDatabaseImportExisting' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-281">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="48421-282">Database cmdlet’leri yedekleme alanı tür belirtimini destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-282">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="48421-283">'New-AzSqlDatabase' cmdlet’ine Force parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-283">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="48421-284">'New-AzSqlDatabase' cmdlet’indeki seçili bölgelerde yer alan BackupStorageRedundancy yapılandırmasına yönelik uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-284">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="48421-285">Sunucu ve örneğe yönelik ActiveDirectoryOnlyAuthentication cmdlet’leri, ResourceId ve InputObject’i içerek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-285">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-286">Az.Storage</span></span>
* <span data-ttu-id="48421-287">Microsoft.Azure.Storage.DataMovement 2.0.0 sürümüne yükseltme sırasında blob karşıya yüklenirken oluşan hata düzeltildi [#12220]</span><span class="sxs-lookup"><span data-stu-id="48421-287">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="48421-288">Belirli Bir Noktaya Geri Yükleme Desteği Eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-288">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="48421-289">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-289">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="48421-290">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-290">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="48421-291">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="48421-291">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="48421-292">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="48421-292">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="48421-293">get-AzureRMStorageAccount cmdlet’ini -IncludeBlobRestoreStatus parametresiyle çalıştırarak Depolama hesabının blobu geri yükleme durumunu almaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-293">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="48421-294">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="48421-294">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="48421-295">Yaklaşan cmdlet çıkış değişikliği için hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-295">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="48421-296">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-296">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="48421-297">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-297">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="48421-298">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-298">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="48421-299">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-299">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="48421-300">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="48421-300">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="48421-301">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="48421-301">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="48421-302">Microsoft.Azure.Cosmos.Table SDK 1.0.8 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="48421-302">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="48421-303">Topluluğumuzdan katkıda bulunanlara teşekkür ederiz</span><span class="sxs-lookup"><span data-stu-id="48421-303">Thanks to our community contributors</span></span>
* <span data-ttu-id="48421-304">Thomas Van Laere (@ThomVanL), Dockerfile-alpine-3.10’u ekledi (#12911)</span><span class="sxs-lookup"><span data-stu-id="48421-304">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="48421-305">Lohith Chowdary Chilukuri (@Lochiluk), Remove-AzNetworkInterfaceIpConfig.md dosyasını güncelleştirdi (#12807)</span><span class="sxs-lookup"><span data-stu-id="48421-305">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="48421-306">Roberth Strand (@roberthstrand), Get-AzResourceGroup-New örneği ve temizleme (#12828)</span><span class="sxs-lookup"><span data-stu-id="48421-306">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="48421-307">Ravi Mishra (@inmishrar), Azure Web App çalışma zamanı yığınını DOTNETCORE’a güncelleştirdi (#12833)</span><span class="sxs-lookup"><span data-stu-id="48421-307">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="48421-308">@jack-education, Set-AzVirtualNetworkSubnetConfig cmdlet’i NSG ve Rota Tablosunu alt ağdan kaldıracak şekilde güncelleştirdi (#12351)</span><span class="sxs-lookup"><span data-stu-id="48421-308">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="48421-309">@hagop-globanet, Add-AzApplicationGatewayCustomError.md dosyasını güncelleştirdi (#12784)</span><span class="sxs-lookup"><span data-stu-id="48421-309">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="48421-310">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="48421-310">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="48421-311">Özellikten Özelliğe yazımını güncelleştirdi (#12821)</span><span class="sxs-lookup"><span data-stu-id="48421-311">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="48421-312">New-AzResourceLock.md örneklerini güncelleştirdi (#12806)</span><span class="sxs-lookup"><span data-stu-id="48421-312">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="48421-313">Eragon Riddle (@eragonriddle), örnekteki parametre alanı adını düzeltti (#12825)</span><span class="sxs-lookup"><span data-stu-id="48421-313">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="48421-314">@rossifumax, New-AzConfigurationAssignment.md dosyasındaki yazım hatasını düzeltti (#12701)</span><span class="sxs-lookup"><span data-stu-id="48421-314">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="48421-315">4.6.1 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="48421-315">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="48421-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-316">Az.Compute</span></span>
* <span data-ttu-id="48421-317">False değerinin varsayılan değerini kaldırmak için 'New-AzVm' içindeki '-EncryptionAtHost' parametresine yama uygulandı [#12776]</span><span class="sxs-lookup"><span data-stu-id="48421-317">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="48421-318">4.6.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="48421-318">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-319">Az.Accounts</span></span>
* <span data-ttu-id="48421-320">Bulma uç noktası varsayılan AzureCloud ortamını veya diğer genel ortamları döndürmediğinden tüm genel bulut ortamları yüklendi (#12633)</span><span class="sxs-lookup"><span data-stu-id="48421-320">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="48421-321">SubscriptionPolicies, 'Get-AzSubscription' cmdlet’inde kullanıma sunuldu [#12551]</span><span class="sxs-lookup"><span data-stu-id="48421-321">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-322">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-322">Az.Automation</span></span>
* <span data-ttu-id="48421-323">Karma Çalışanı Grubu belirtmek için 'Set-AzAutomationWebhook' cmdlet’ine '-RunOn' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-323">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-324">Az.Compute</span></span>
* <span data-ttu-id="48421-325">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' ve 'Update-AzVmss' cmdlet’lerine '-EncryptionAtHost' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-325">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="48421-326">'Get-AzVM' ve 'Get-AzVmss' cmdlet’lerinin dönüş nesnesine 'SecurityProfile' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-326">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="48421-327">'-InstanceView' anahtarı 'Get-AzHostGroup' cmdlet’ine isteğe bağlı parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-327">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="48421-328">Yeni 'Invoke-AzVmPatchAssessment' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-328">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-329">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-329">Az.DataFactory</span></span>
* <span data-ttu-id="48421-330">PSPipelineRun sınıfındaki eksik özellikler eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-330">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-331">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-331">Az.HDInsight</span></span>
* <span data-ttu-id="48421-332">Konakta şifreleme özelliğiyle küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-332">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-333">Az.KeyVault</span></span>
* <span data-ttu-id="48421-334">Geçici silmeyi devre dışı bırakma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-334">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="48421-335">SecretValueText özniteliğini kaldırma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-335">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="48421-336">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="48421-336">Az.Maintenance</span></span>
* <span data-ttu-id="48421-337">'New-AzMaintenanceConfiguration' cmdlet’ine isteğe bağlı zamanlamayla ilgili alanlar eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-337">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="48421-338">'Get-AzMaintenancePublicConfiguration' için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-338">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="48421-339">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="48421-339">Az.ManagedServices</span></span>
* <span data-ttu-id="48421-340">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-340">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-341">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-341">Az.Monitor</span></span>
* <span data-ttu-id="48421-342">Günlüklerin ve Ölçümlerin ayrılmasını etkinleştirmek için 'Set-AzDiagnosticSetting' cmdlet’indeki parametre kümesi genişletildi [#12482]</span><span class="sxs-lookup"><span data-stu-id="48421-342">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="48421-343">'Add-AzMetricAlertRuleV2' cmdlet’inde işlem hattından ölçüm uyarısı alınırken oluşan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-343">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-344">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-344">Az.Resources</span></span>
* <span data-ttu-id="48421-345">'Get-AzPolicyAlias' cmdlet’i, diğer adın Azure İlkesi tarafından değiştirilebilir olup olmadığını belirten bilgiler içerek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-345">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="48421-346">Yeni 'Set-AzRoleAssignment' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-346">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="48421-347">Yönetim grubu kapsamındaki ARM şablonu Durum sonuçlarını almak için 'Get-AzDeploymentManagementGroupWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-347">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="48421-348">Kiracı kapsamındaki ARM şablonu Durum sonuçlarını almaya yönelik yeni 'Get-AzTenantWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-348">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="48421-349">'New-AzManagementGroupDeployment' ve 'New-AzTenantDeployment' için '-WhatIf' ve '-Confirm' parametreleri, ARM şablonu Durum sonuçlarını kullanacak şekilde geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="48421-349">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="48421-350">Yeni dağıtım cmdlet’lerindeki '-WhatIf' ve '-Confirm' parametrelerinin davranışları False ile uyumlu olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-350">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="48421-351">'-TemplateObject' ve 'TemplateParameterObject' için serileştirme hatası düzeltildi [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="48421-351">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="48421-352">'Get-AzResourceGroupDeploymentOperation' cmdlet’ine, yaklaşan çıkış türü değişikliğine yönelik hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-352">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="48421-353">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="48421-353">Az.SignalR</span></span>
* <span data-ttu-id="48421-354">'Restart-AzSignalR' ve 'Update-AzSignalR' yardım dosyalarındaki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-354">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="48421-355">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-355">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-356">Az.Storage</span></span>
* <span data-ttu-id="48421-357">Blob sorgu hızlandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-357">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="48421-358">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="48421-358">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="48421-359">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="48421-359">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="48421-360">Yardım dosyası güncelleştirildi, daha fazla açıklama eklendi ve yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-360">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="48421-361">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="48421-361">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="48421-362">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="48421-362">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="48421-363">İlgili alt dizin mevcut olmadığında blobu indirme işleminin başarısız olmasıyla ilgili sorun düzeltildi [#12592]</span><span class="sxs-lookup"><span data-stu-id="48421-363">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="48421-364">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="48421-364">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="48421-365">Depolama hesaplarında Set/Get/Remove Nesne Çoğaltma İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-365">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="48421-366">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="48421-366">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="48421-367">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-367">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="48421-368">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-368">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="48421-369">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-369">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="48421-370">Bir Depolama hesabının Blob Hizmeti üzerinde ChangeFeed’i etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-370">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="48421-371">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="48421-371">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="48421-372">4.5.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="48421-372">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-373">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-373">Az.Accounts</span></span>
* <span data-ttu-id="48421-374">'Connect-AzAccount' cmdlet’i 'MaxContextPopulation' parametresini kabul edecek şekilde güncelleştirildi [#9865]</span><span class="sxs-lookup"><span data-stu-id="48421-374">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="48421-375">SubscriptionClient sürümü 2019-06-01 olarak ve kiracı etki alanlarını görüntüleyecek şekilde güncelleştirildi [#9838]</span><span class="sxs-lookup"><span data-stu-id="48421-375">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="48421-376">Aboneliğin giriş kiracısı ve yöneten kiracısı bilgilerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-376">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="48421-377">Telemetri verilerindeki modül adı ve sürüm bilgileri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-377">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="48421-378">SqlDatabaseDnsSuffix ve ServiceManagementUrl, ortam meta verileri uç noktasının uyumsuz değer döndürdüğü durumlar için ayarlandı</span><span class="sxs-lookup"><span data-stu-id="48421-378">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="48421-379">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="48421-379">Az.Aks</span></span>
* <span data-ttu-id="48421-380">'ClientIdAndSecret' kaldırılarak 'ServicePrincipalIdAndSecret' eklendi ve 'ClientIdAndSecret' bir diğer ad olarak ayarlandı [#12381].</span><span class="sxs-lookup"><span data-stu-id="48421-380">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="48421-381">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' cmdlet’leri kaldırılarak 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' eklendi ve özgün olanlar diğer ad olarak ayarlandı [#12373].</span><span class="sxs-lookup"><span data-stu-id="48421-381">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="48421-382">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-382">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-383">Yeni 'Add-AzApiManagementApiToGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-383">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="48421-384">Yeni 'Get-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-384">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="48421-385">Yeni 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-385">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="48421-386">Yeni 'Get-AzApiManagementGatewayKey' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-386">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="48421-387">Yeni 'New-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-387">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="48421-388">Yeni 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-388">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="48421-389">Yeni 'New-AzApiManagementResourceLocationObject' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-389">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="48421-390">Yeni 'Remove-AzApiManagementApiFromGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-390">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="48421-391">Yeni 'Remove-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-391">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="48421-392">Yeni 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-392">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="48421-393">Yeni 'Update-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-393">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="48421-394">'Get-AzApiManagementApi' cmdlet’ine yeni ve isteğe bağlı [-GatewayId] parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-394">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-395">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-395">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-396">'Deny', özellikle NetworkRules varsayılan eylemi olarak kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-396">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="48421-397">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-397">Az.FrontDoor</span></span>
* <span data-ttu-id="48421-398">Enum.Parse metodu, bir null değeri Enabled veya Disabled sabit listesi değerlerine zorladığında özel durum oluşturulmasıyla ilgili bir sorun düzeltildi [#12344]</span><span class="sxs-lookup"><span data-stu-id="48421-398">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-399">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-399">Az.HDInsight</span></span>
* <span data-ttu-id="48421-400">Aktarma özelliğinde şifrelemeye sahip küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-400">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="48421-401">'New-AzHDInsightCluster' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-401">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="48421-402">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-402">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="48421-403">Özel bağlantı özelliğine sahip küme oluşturma desteği eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-403">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="48421-404">'New-AzHDInsightCluster' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-404">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="48421-405">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-405">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="48421-406">'New-AzHDInsightCluster' veya 'Get-AzHDInsightCluster' çağrıldığında sanal ağ bilgileri döndürüldü</span><span class="sxs-lookup"><span data-stu-id="48421-406">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-407">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-407">Az.Network</span></span>
* <span data-ttu-id="48421-408">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-408">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="48421-409">Hataya neden olmayan değişiklikler eklendi: 'Remove-AzExpressRouteCircutPeeringConfig' cmdlet’inde Özel Eşleme’ye yönelik PeerAddressType işlevi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-409">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="48421-410">AddressPrefixType ve PeerAddressType parametresindeki kodlar büyük/küçük harfi yoksayacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-410">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="48421-411">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-411">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-412">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-412">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-413">'Remove-AzOperationalInsightsworkspace' için '-ForceDelete' seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-413">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="48421-414">Yeni 'Get-AzOperationalInsightsDeletedWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-414">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="48421-415">Yeni 'Restore-AzOperationalInsightsWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-415">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-417">Azure Backup kapsayıcı/öğe keşif deneyimi iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-417">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-418">Az.Resources</span></span>
* <span data-ttu-id="48421-419">'New-AzRoleAssignment' cmdlet’ine 'Condition', 'ConditionVersion' ve 'Description' özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-419">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="48421-420">Bu, veri modellerinde yapılan tüm ilgili değişiklikleri içerir</span><span class="sxs-lookup"><span data-stu-id="48421-420">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-421">Az.Sql</span></span>
* <span data-ttu-id="48421-422">'New-AzSqlServer' ve 'Set-AzSqlServer' cmdlet’lerindeki sunucu adının olası büyük/küçük harfe duyarsızlık hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-422">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="48421-423">'New-AzSqlDatabaseSecondary' cmdlet’indeki mevcut veritabanına yanlış veritabanı adının döndürülmesi hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-423">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-424">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-424">Az.Storage</span></span>
* <span data-ttu-id="48421-425">Yeni x,t izniyle kapsayıcı/blob Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-425">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="48421-426">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="48421-426">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="48421-427">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="48421-427">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="48421-428">Yeni x,t,f izniyle hesap Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-428">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="48421-429">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="48421-429">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="48421-430">Tek dosya paylaşımı kullanımını alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-430">Supported get single file share usage</span></span>
    - <span data-ttu-id="48421-431">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="48421-431">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="48421-432">4.4.0 - Temmuz 2020</span><span class="sxs-lookup"><span data-stu-id="48421-432">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-433">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-433">Az.Accounts</span></span>
* <span data-ttu-id="48421-434">“Invoke-AzRestMethod” adlı yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-434">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="48421-435">“Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]</span><span class="sxs-lookup"><span data-stu-id="48421-435">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="48421-436">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="48421-436">Az.Aks</span></span>
* <span data-ttu-id="48421-437">“Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]</span><span class="sxs-lookup"><span data-stu-id="48421-437">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="48421-438">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48421-438">Az.AnalysisServices</span></span>
* <span data-ttu-id="48421-439">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-439">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-440">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-440">Az.Automation</span></span>
* <span data-ttu-id="48421-441">Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-441">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-442">Az.Compute</span></span>
* <span data-ttu-id="48421-443">“En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-443">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-444">Az.DataFactory</span></span>
* <span data-ttu-id="48421-445">Data Factory’ye genel parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-445">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="48421-446">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="48421-446">Az.EventGrid</span></span>
* <span data-ttu-id="48421-447">2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-447">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="48421-448">Yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-448">Added new features:</span></span>
    - <span data-ttu-id="48421-449">Giriş eşleme</span><span class="sxs-lookup"><span data-stu-id="48421-449">Input mapping</span></span>
    - <span data-ttu-id="48421-450">Olay Teslim Şeması</span><span class="sxs-lookup"><span data-stu-id="48421-450">Event Delivery Schema</span></span>
    - <span data-ttu-id="48421-451">Özel Bağlantı</span><span class="sxs-lookup"><span data-stu-id="48421-451">Private Link</span></span>
    - <span data-ttu-id="48421-452">Bulut Olayı V10 Şeması</span><span class="sxs-lookup"><span data-stu-id="48421-452">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="48421-453">Hedef Olarak Service Bus Konu Başlığı</span><span class="sxs-lookup"><span data-stu-id="48421-453">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="48421-454">Hedef Olarak Azure İşlevi</span><span class="sxs-lookup"><span data-stu-id="48421-454">Azure Function As Destination</span></span>
    - <span data-ttu-id="48421-455">Web Kancası Toplu İş</span><span class="sxs-lookup"><span data-stu-id="48421-455">WebHook Batching</span></span>
    - <span data-ttu-id="48421-456">Güvenli web kancası (AAD desteği)</span><span class="sxs-lookup"><span data-stu-id="48421-456">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="48421-457">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="48421-457">IpFiltering</span></span>
* <span data-ttu-id="48421-458">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-458">Updated cmdlets:</span></span>
    - <span data-ttu-id="48421-459">“New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="48421-459">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="48421-460">Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-460">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="48421-461">AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-461">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="48421-462">Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-462">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="48421-463">Teslim şeması için yeni, isteğe bağlı parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-463">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="48421-464">“New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="48421-464">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="48421-465">IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-465">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="48421-466">“New-AzEventGridTopic'/'New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="48421-466">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="48421-467">Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-467">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="48421-468">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-468">Az.FrontDoor</span></span>
* <span data-ttu-id="48421-469">Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-469">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="48421-470">Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-470">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-471">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-471">Az.HDInsight</span></span>
* <span data-ttu-id="48421-472">Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-472">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-473">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-473">Az.Monitor</span></span>
* <span data-ttu-id="48421-474">Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]</span><span class="sxs-lookup"><span data-stu-id="48421-474">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-475">Az.Network</span></span>
* <span data-ttu-id="48421-476">VWan HubVnet bağlantısında değişen parametreler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-476">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="48421-477">Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-477">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="48421-478">“Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="48421-478">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="48421-479">“New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="48421-479">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="48421-480">“Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="48421-480">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="48421-481">“Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="48421-481">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="48421-482">“New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="48421-482">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="48421-483">Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-483">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="48421-484">“Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="48421-484">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="48421-485">“New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="48421-485">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="48421-486">“Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="48421-486">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="48421-487">“Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="48421-487">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="48421-488">“Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="48421-488">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="48421-489">“New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="48421-489">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="48421-490">Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-490">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="48421-491">Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-491">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="48421-492">Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-492">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-493">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-493">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-494">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-494">Removed project reference to Authentication</span></span>
* <span data-ttu-id="48421-495">Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı</span><span class="sxs-lookup"><span data-stu-id="48421-495">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="48421-496">Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="48421-496">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-497">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-497">Az.Resources</span></span>
* <span data-ttu-id="48421-498">“Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-498">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="48421-499">“Unregister-AzResourceProvider” cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-499">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-500">Az.Sql</span></span>
* <span data-ttu-id="48421-501">“Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-501">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="48421-502">Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-502">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="48421-503">Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="48421-503">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-504">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-504">Az.Storage</span></span>
* <span data-ttu-id="48421-505">Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-505">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="48421-506">MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-506">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="48421-507">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="48421-507">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="48421-508">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="48421-508">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="48421-509">Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-509">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="48421-510">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="48421-510">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="48421-511">Blob sürümlerini içeren destek listesi blobları</span><span class="sxs-lookup"><span data-stu-id="48421-511">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="48421-512">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="48421-512">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="48421-513">Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-513">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="48421-514">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="48421-514">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="48421-515">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="48421-515">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="48421-516">Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-516">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="48421-517">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="48421-517">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="48421-518">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="48421-518">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="48421-519">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="48421-519">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="48421-520">“Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="48421-520">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="48421-521">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="48421-521">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="48421-522">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="48421-522">Az.StorageSync</span></span>
* <span data-ttu-id="48421-523">ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-523">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="48421-524">“UpdateStorageSyncService” cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-524">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="48421-525">“Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="48421-525">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="48421-526">StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-526">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-527">Az.Websites</span></span>
* <span data-ttu-id="48421-528">App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-528">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="48421-529">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="48421-529">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-530">Az.Accounts</span></span>
* <span data-ttu-id="48421-531">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-531">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="48421-532">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="48421-532">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="48421-533">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-533">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="48421-534">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="48421-534">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="48421-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="48421-535">Az.Aks</span></span>
* <span data-ttu-id="48421-536">Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-536">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="48421-537">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="48421-537">Az.Batch</span></span>
* <span data-ttu-id="48421-538">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-538">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="48421-539">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-539">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-540">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-540">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-541">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-541">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="48421-542">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-542">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-543">Az.Compute</span></span>
* <span data-ttu-id="48421-544">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-544">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="48421-545">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-545">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="48421-546">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="48421-546">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="48421-547">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-547">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="48421-548">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-548">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-549">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-549">Az.DataFactory</span></span>
* <span data-ttu-id="48421-550">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-550">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-551">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-551">Az.EventHub</span></span>
* <span data-ttu-id="48421-552">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-552">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="48421-553">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="48421-553">Az.Functions</span></span>
* <span data-ttu-id="48421-554">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-554">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-555">Az.HDInsight</span></span>
* <span data-ttu-id="48421-556">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-556">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="48421-557">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="48421-557">Az.HealthcareApis</span></span>
* <span data-ttu-id="48421-558">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-558">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="48421-559">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-559">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-560">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-560">Az.Monitor</span></span>
* <span data-ttu-id="48421-561">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-561">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="48421-562">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="48421-562">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-563">Az.Network</span></span>
* <span data-ttu-id="48421-564">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="48421-565">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-565">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="48421-566">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="48421-566">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="48421-567">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="48421-567">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="48421-568">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-568">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="48421-569">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="48421-569">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="48421-570">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="48421-570">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="48421-571">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="48421-571">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="48421-572">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="48421-572">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="48421-573">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="48421-573">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="48421-574">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-574">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="48421-575">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-575">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="48421-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="48421-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="48421-577">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="48421-577">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="48421-578">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-578">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="48421-579">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-579">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="48421-580">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-580">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="48421-581">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-581">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="48421-582">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-582">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="48421-583">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="48421-583">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="48421-584">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-584">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="48421-585">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-585">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="48421-586">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-586">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="48421-587">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-587">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="48421-588">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-588">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="48421-589">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-589">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="48421-590">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="48421-590">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="48421-591">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-591">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="48421-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="48421-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="48421-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="48421-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="48421-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="48421-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="48421-598">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-598">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="48421-599">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="48421-599">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="48421-600">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="48421-600">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="48421-601">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="48421-601">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="48421-602">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="48421-602">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="48421-603">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="48421-603">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="48421-604">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-604">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="48421-605">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="48421-605">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="48421-606">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="48421-606">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="48421-607">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="48421-607">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="48421-608">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="48421-608">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="48421-609">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="48421-609">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="48421-610">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="48421-610">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="48421-611">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="48421-611">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="48421-612">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="48421-612">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-613">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-613">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-614">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="48421-614">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="48421-615">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-615">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="48421-616">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-616">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="48421-617">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="48421-617">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="48421-618">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="48421-618">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-619">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-620">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-620">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="48421-621">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="48421-621">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-622">Az.Resources</span></span>
* <span data-ttu-id="48421-623">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="48421-623">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="48421-624">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="48421-624">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="48421-625">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-625">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="48421-626">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-626">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="48421-627">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-627">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="48421-628">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-628">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-629">Az.Sql</span></span>
* <span data-ttu-id="48421-630">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-630">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="48421-631">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-631">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="48421-632">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="48421-632">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-633">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-633">Az.Storage</span></span>
* <span data-ttu-id="48421-634">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-634">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="48421-635">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="48421-635">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="48421-636">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="48421-636">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-637">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-637">Az.Websites</span></span>
* <span data-ttu-id="48421-638">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-638">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="48421-639">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-639">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="48421-640">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-640">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="48421-641">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-641">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="48421-642">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-642">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="48421-643">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-643">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="48421-644">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="48421-644">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-645">Az.Accounts</span></span>
* <span data-ttu-id="48421-646">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="48421-646">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="48421-647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48421-647">Az.AnalysisServices</span></span>
* <span data-ttu-id="48421-648">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-648">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="48421-649">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-649">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-650">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-650">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="48421-651">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="48421-651">Az.Billing</span></span>
* <span data-ttu-id="48421-652">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-652">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-653">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-654">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="48421-654">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="48421-655">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-655">Az.DataFactory</span></span>
* <span data-ttu-id="48421-656">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-656">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="48421-657">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="48421-657">Az.DataShare</span></span>
* <span data-ttu-id="48421-658">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-658">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="48421-659">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="48421-659">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="48421-660">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-660">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-661">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-661">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-662">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-662">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="48421-663">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-663">Added optional parameters to</span></span> 
    - <span data-ttu-id="48421-664">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="48421-664">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="48421-665">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="48421-665">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="48421-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48421-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="48421-667">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-667">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="48421-668">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="48421-668">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="48421-669">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-669">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="48421-670">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="48421-670">Az.PrivateDns</span></span>
* <span data-ttu-id="48421-671">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-671">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-673">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-673">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="48421-674">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-674">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-675">Az.Resources</span></span>
* <span data-ttu-id="48421-676">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-676">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="48421-677">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="48421-677">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="48421-678">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-678">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="48421-679">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-679">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="48421-680">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-680">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-681">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-681">Az.Sql</span></span>
* <span data-ttu-id="48421-682">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-682">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="48421-683">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-683">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="48421-684">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-684">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-685">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-685">Az.Storage</span></span>
* <span data-ttu-id="48421-686">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-686">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="48421-687">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="48421-687">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="48421-688">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="48421-688">Highlights since the last release</span></span>
* <span data-ttu-id="48421-689">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="48421-689">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="48421-690">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-690">General availability of Az.Functions</span></span> 
* <span data-ttu-id="48421-691">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="48421-691">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-692">Az.Accounts</span></span>
* <span data-ttu-id="48421-693">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-693">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="48421-694">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="48421-694">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="48421-695">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="48421-695">Az.Aks</span></span>
* <span data-ttu-id="48421-696">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="48421-696">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="48421-697">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-697">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="48421-698">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="48421-698">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="48421-699">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-699">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-700">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-700">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="48421-701">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="48421-701">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="48421-702">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-702">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="48421-703">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-703">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="48421-704">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-704">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="48421-705">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-705">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="48421-706">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-706">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="48421-707">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-707">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="48421-708">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-708">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="48421-709">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-709">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="48421-710">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="48421-710">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="48421-711">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="48421-711">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="48421-712">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="48421-712">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="48421-713">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="48421-713">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="48421-714">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="48421-714">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="48421-715">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="48421-715">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="48421-716">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="48421-716">Az.ApplicationInsights</span></span>
* <span data-ttu-id="48421-717">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="48421-717">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="48421-718">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-718">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="48421-719">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-719">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="48421-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="48421-720">Az.Batch</span></span>
* <span data-ttu-id="48421-721">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-721">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="48421-722">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-722">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="48421-723">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-723">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="48421-724">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="48421-724">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="48421-725">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="48421-725">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="48421-726">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="48421-726">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="48421-727">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="48421-727">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="48421-728">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="48421-728">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="48421-729">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="48421-729">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-730">Az.Compute</span></span>
* <span data-ttu-id="48421-731">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-731">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="48421-732">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-732">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="48421-733">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="48421-733">Breaking changes</span></span>
    - <span data-ttu-id="48421-734">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-734">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="48421-735">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-735">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="48421-736">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-736">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="48421-737">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-737">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="48421-738">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-738">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="48421-739">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-739">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="48421-740">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-740">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="48421-741">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-741">Az.DataFactory</span></span>
* <span data-ttu-id="48421-742">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-742">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="48421-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-743">Az.FrontDoor</span></span>
* <span data-ttu-id="48421-744">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-744">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="48421-745">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-745">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="48421-746">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-746">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="48421-747">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-747">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="48421-748">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="48421-748">Az.Functions</span></span>
* <span data-ttu-id="48421-749">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-749">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-750">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-750">Az.HDInsight</span></span>
* <span data-ttu-id="48421-751">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="48421-751">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="48421-752">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="48421-752">Az.HealthcareApis</span></span>
* <span data-ttu-id="48421-753">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="48421-753">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-754">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-754">Az.IotHub</span></span>
* <span data-ttu-id="48421-755">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-755">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="48421-756">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="48421-756">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="48421-757">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-757">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="48421-758">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-758">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="48421-759">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="48421-759">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="48421-760">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-760">New cmdlets are:</span></span>
    - <span data-ttu-id="48421-761">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="48421-761">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="48421-762">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="48421-762">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="48421-763">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="48421-763">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="48421-764">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="48421-764">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="48421-765">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-765">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="48421-766">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-766">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-767">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-767">Az.KeyVault</span></span>
* <span data-ttu-id="48421-768">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="48421-768">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="48421-769">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-769">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="48421-770">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="48421-770">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="48421-771">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-771">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="48421-772">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="48421-772">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="48421-773">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="48421-773">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="48421-774">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-774">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-775">Az.Monitor</span></span>
* <span data-ttu-id="48421-776">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="48421-776">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="48421-777">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-777">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="48421-778">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-778">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="48421-779">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="48421-779">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="48421-780">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="48421-780">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="48421-781">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="48421-781">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="48421-782">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-782">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-783">Az.Network</span></span>
* <span data-ttu-id="48421-784">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-784">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="48421-785">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="48421-785">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="48421-786">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="48421-786">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="48421-787">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="48421-787">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="48421-788">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-788">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="48421-789">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-789">New cmdlets added:</span></span>
        - <span data-ttu-id="48421-790">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="48421-790">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="48421-791">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="48421-791">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="48421-792">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="48421-792">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="48421-793">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="48421-793">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="48421-794">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-794">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="48421-795">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-795">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="48421-796">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-796">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="48421-797">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="48421-797">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="48421-798">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="48421-798">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="48421-799">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-799">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="48421-800">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="48421-800">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="48421-801">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="48421-801">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="48421-802">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="48421-802">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="48421-803">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="48421-803">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="48421-804">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="48421-804">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="48421-805">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-805">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="48421-806">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-806">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="48421-807">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-807">Updated cmdlet:</span></span>
        - <span data-ttu-id="48421-808">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="48421-808">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-809">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-809">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-810">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-810">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="48421-811">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-811">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="48421-812">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="48421-812">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="48421-813">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="48421-813">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="48421-814">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="48421-814">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="48421-815">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-815">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="48421-816">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-816">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="48421-817">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-817">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-818">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-818">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-819">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-819">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="48421-820">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-820">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="48421-821">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-821">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="48421-822">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-822">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="48421-823">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-823">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-824">Az.Resources</span></span>
* <span data-ttu-id="48421-825">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-825">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="48421-826">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-826">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="48421-827">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="48421-827">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="48421-828">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="48421-828">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="48421-829">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="48421-829">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="48421-830">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="48421-830">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="48421-831">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="48421-831">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="48421-832">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="48421-832">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="48421-833">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-833">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="48421-834">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-834">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="48421-835">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-835">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="48421-836">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-836">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="48421-837">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-837">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="48421-838">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-838">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="48421-839">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="48421-839">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="48421-840">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-840">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="48421-841">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="48421-841">'New-AzDeployment'</span></span>
    - <span data-ttu-id="48421-842">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="48421-842">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="48421-843">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="48421-843">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="48421-844">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="48421-844">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-845">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-845">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-846">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-846">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-847">Az.Sql</span></span>
* <span data-ttu-id="48421-848">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-848">Enhance performance of:</span></span>
    - <span data-ttu-id="48421-849">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="48421-849">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="48421-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="48421-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="48421-851">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="48421-851">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="48421-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="48421-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="48421-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="48421-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="48421-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="48421-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="48421-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="48421-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="48421-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="48421-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="48421-857">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-857">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="48421-858">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-858">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-859">Az.Storage</span></span>
* <span data-ttu-id="48421-860">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-860">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="48421-861">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="48421-861">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="48421-862">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="48421-862">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="48421-863">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-863">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="48421-864">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="48421-864">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="48421-865">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-865">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="48421-866">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="48421-866">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="48421-867">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="48421-867">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="48421-868">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="48421-868">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="48421-869">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="48421-869">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="48421-870">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="48421-870">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="48421-871">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="48421-871">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="48421-872">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="48421-872">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="48421-873">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-873">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="48421-874">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="48421-874">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="48421-875">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="48421-875">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="48421-876">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-876">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="48421-877">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="48421-877">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="48421-878">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="48421-878">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="48421-879">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-879">Supported failover Storage account</span></span>
    - <span data-ttu-id="48421-880">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="48421-880">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="48421-881">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-881">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="48421-882">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-882">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="48421-883">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-883">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="48421-884">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="48421-884">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="48421-885">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="48421-885">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="48421-886">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="48421-886">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="48421-887">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="48421-887">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="48421-888">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="48421-888">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="48421-889">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="48421-889">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="48421-890">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="48421-890">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="48421-891">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="48421-891">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="48421-892">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="48421-892">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="48421-893">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="48421-893">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="48421-894">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="48421-894">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="48421-895">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="48421-895">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="48421-896">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="48421-896">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="48421-897">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="48421-897">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="48421-898">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="48421-898">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="48421-899">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="48421-899">Az.TrafficManager</span></span>
* <span data-ttu-id="48421-900">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-900">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-901">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-901">Az.Websites</span></span>
* <span data-ttu-id="48421-902">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-902">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="48421-903">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="48421-903">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="48421-904">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="48421-904">Highlights since the last release</span></span>
* <span data-ttu-id="48421-905">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="48421-905">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-906">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-906">Az.Accounts</span></span>
* <span data-ttu-id="48421-907">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="48421-907">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="48421-908">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-908">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-909">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-909">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="48421-910">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-910">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="48421-911">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="48421-911">Az.Cdn</span></span>
* <span data-ttu-id="48421-912">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-912">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-913">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-913">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-914">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="48421-914">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-915">Az.Compute</span></span>
* <span data-ttu-id="48421-916">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-916">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="48421-917">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="48421-917">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-918">Az.IotHub</span></span>
* <span data-ttu-id="48421-919">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-919">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="48421-920">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="48421-920">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="48421-921">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="48421-921">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="48421-922">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-922">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="48421-923">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-923">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="48421-924">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="48421-924">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="48421-925">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="48421-925">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="48421-926">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="48421-926">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="48421-927">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-927">New cmdlets are:</span></span>
    - <span data-ttu-id="48421-928">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-928">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="48421-929">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-929">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="48421-930">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-930">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="48421-931">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="48421-931">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="48421-932">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-932">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-933">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-933">Az.KeyVault</span></span>
* <span data-ttu-id="48421-934">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-934">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="48421-935">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="48421-935">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="48421-936">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="48421-936">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="48421-937">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-937">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="48421-938">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="48421-938">Az.Maintenance</span></span>
* <span data-ttu-id="48421-939">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="48421-939">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-940">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-940">Az.Monitor</span></span>
* <span data-ttu-id="48421-941">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-941">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="48421-942">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="48421-942">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="48421-943">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="48421-943">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="48421-944">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="48421-944">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="48421-945">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="48421-945">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="48421-946">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="48421-946">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="48421-947">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="48421-947">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="48421-948">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="48421-948">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-949">Az.Network</span></span>
* <span data-ttu-id="48421-950">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-950">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="48421-951">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="48421-951">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="48421-952">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="48421-952">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="48421-953">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="48421-953">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="48421-954">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="48421-954">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="48421-955">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-955">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="48421-956">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="48421-956">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="48421-957">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="48421-957">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="48421-958">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-958">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="48421-959">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-959">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="48421-960">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="48421-960">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="48421-961">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-961">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="48421-962">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-962">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="48421-963">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-963">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="48421-964">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="48421-964">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="48421-965">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="48421-965">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="48421-966">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48421-966">Az.PolicyInsights</span></span>
* <span data-ttu-id="48421-967">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-967">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="48421-968">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-968">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-969">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-969">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-970">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-970">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-971">Az.Sql</span></span>
* <span data-ttu-id="48421-972">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-972">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="48421-973">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-973">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-974">Az.Storage</span></span>
* <span data-ttu-id="48421-975">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-975">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="48421-976">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-976">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="48421-977">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="48421-977">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="48421-978">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="48421-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="48421-979">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="48421-979">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="48421-980">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="48421-980">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="48421-981">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="48421-981">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="48421-982">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="48421-982">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="48421-983">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="48421-983">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="48421-984">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="48421-984">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="48421-985">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="48421-985">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="48421-986">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="48421-986">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="48421-987">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="48421-987">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="48421-988">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="48421-988">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="48421-989">Genel</span><span class="sxs-lookup"><span data-stu-id="48421-989">General</span></span>
* <span data-ttu-id="48421-990">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="48421-990">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="48421-991">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="48421-991">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="48421-992">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="48421-992">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="48421-993">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="48421-993">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="48421-994">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="48421-994">Az.Billing</span></span>
  - <span data-ttu-id="48421-995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-995">Az.Compute</span></span>
  - <span data-ttu-id="48421-996">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="48421-996">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="48421-997">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-997">Az.EventHub</span></span>
  - <span data-ttu-id="48421-998">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-998">Az.IotHub</span></span>
  - <span data-ttu-id="48421-999">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-999">Az.KeyVault</span></span>
  - <span data-ttu-id="48421-1000">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-1000">Az.Monitor</span></span>
  - <span data-ttu-id="48421-1001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1001">Az.Network</span></span>
  - <span data-ttu-id="48421-1002">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1002">Az.Resources</span></span>
  - <span data-ttu-id="48421-1003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-1003">Az.Storage</span></span>
  - <span data-ttu-id="48421-1004">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-1004">Az.Websites</span></span>
* <span data-ttu-id="48421-1005">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-1005">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="48421-1006">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="48421-1006">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="48421-1007">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="48421-1007">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="48421-1008">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="48421-1008">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-1009">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1009">Az.Accounts</span></span>
* <span data-ttu-id="48421-1010">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="48421-1010">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1011">Az.Compute</span></span>
* <span data-ttu-id="48421-1012">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1012">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="48421-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="48421-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="48421-1014">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1014">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="48421-1015">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1015">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="48421-1016">[#11354]</span><span class="sxs-lookup"><span data-stu-id="48421-1016">[#11354]</span></span>
* <span data-ttu-id="48421-1017">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1017">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="48421-1018">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="48421-1018">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="48421-1019">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="48421-1019">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="48421-1020">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="48421-1020">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="48421-1021">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="48421-1021">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="48421-1022">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1022">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="48421-1023">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1023">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="48421-1024">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1024">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="48421-1025">[#11257]</span><span class="sxs-lookup"><span data-stu-id="48421-1025">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1026">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1026">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1027">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1027">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="48421-1028">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1028">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-1029">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-1029">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-1030">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1030">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="48421-1031">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1031">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-1032">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-1032">Az.HDInsight</span></span>
* <span data-ttu-id="48421-1033">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1033">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-1034">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-1034">Az.IotHub</span></span>
* <span data-ttu-id="48421-1035">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1035">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="48421-1036">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-1036">New Cmdlets are:</span></span>
    - <span data-ttu-id="48421-1037">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="48421-1037">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="48421-1038">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="48421-1038">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-1039">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-1039">Az.KeyVault</span></span>
* <span data-ttu-id="48421-1040">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1040">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-1041">Az.Monitor</span></span>
* <span data-ttu-id="48421-1042">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1042">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1043">Az.Network</span></span>
* <span data-ttu-id="48421-1044">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1044">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="48421-1045">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="48421-1045">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="48421-1046">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="48421-1046">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="48421-1047">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="48421-1047">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="48421-1048">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="48421-1048">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="48421-1049">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1049">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="48421-1050">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48421-1050">Az.PolicyInsights</span></span>
* <span data-ttu-id="48421-1051">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1051">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-1053">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1053">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="48421-1054">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1054">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="48421-1055">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1055">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="48421-1056">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1056">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="48421-1057">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1057">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="48421-1058">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1058">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1059">Az.Resources</span></span>
* <span data-ttu-id="48421-1060">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="48421-1060">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="48421-1061">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1061">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="48421-1062">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1062">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="48421-1063">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1063">Added example.</span></span>
* <span data-ttu-id="48421-1064">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="48421-1064">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="48421-1065">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="48421-1065">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1066">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1066">Az.Sql</span></span>
* <span data-ttu-id="48421-1067">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1067">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="48421-1068">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1068">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="48421-1069">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1069">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="48421-1070">Az.Support</span><span class="sxs-lookup"><span data-stu-id="48421-1070">Az.Support</span></span>
* <span data-ttu-id="48421-1071">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-1071">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-1072">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-1072">Az.Websites</span></span>
* <span data-ttu-id="48421-1073">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1073">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="48421-1074">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="48421-1074">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="48421-1075">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="48421-1075">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="48421-1076">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="48421-1076">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="48421-1077">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="48421-1077">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="48421-1078">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="48421-1078">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1079">Az.Accounts</span></span>
* <span data-ttu-id="48421-1080">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="48421-1080">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="48421-1081">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="48421-1081">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="48421-1082">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1082">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="48421-1083">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-1083">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-1084">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="48421-1084">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="48421-1085">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="48421-1085">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="48421-1086">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1086">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="48421-1087">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="48421-1087">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-1088">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-1088">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-1089">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1089">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-1090">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-1090">Az.IotHub</span></span>
* <span data-ttu-id="48421-1091">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1091">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="48421-1092">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-1092">New Cmdlets are:</span></span>
    - <span data-ttu-id="48421-1093">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="48421-1093">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="48421-1094">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="48421-1094">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="48421-1095">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="48421-1095">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="48421-1096">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="48421-1096">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="48421-1097">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1097">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="48421-1098">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-1098">New Cmdlets are:</span></span>
    - <span data-ttu-id="48421-1099">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="48421-1099">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="48421-1100">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="48421-1100">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="48421-1101">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="48421-1101">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="48421-1102">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="48421-1102">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="48421-1103">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1103">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="48421-1104">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1104">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="48421-1105">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1105">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="48421-1106">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-1106">New Cmdlets are:</span></span>
    - <span data-ttu-id="48421-1107">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="48421-1107">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="48421-1108">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="48421-1108">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="48421-1109">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1109">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-1110">Az.Monitor</span></span>
* <span data-ttu-id="48421-1111">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="48421-1111">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1112">Az.Network</span></span>
* <span data-ttu-id="48421-1113">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1113">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="48421-1114">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1114">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="48421-1115">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1115">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="48421-1116">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1116">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1117">Az.Resources</span></span>
* <span data-ttu-id="48421-1118">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1118">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="48421-1119">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="48421-1119">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="48421-1120">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="48421-1120">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="48421-1121">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="48421-1121">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="48421-1122">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1122">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="48421-1123">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1123">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="48421-1124">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1124">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="48421-1125">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="48421-1125">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="48421-1126">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="48421-1126">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="48421-1127">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="48421-1127">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="48421-1128">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="48421-1128">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="48421-1129">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1129">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="48421-1130">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="48421-1130">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="48421-1131">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1131">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1132">Az.Sql</span></span>
* <span data-ttu-id="48421-1133">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1133">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="48421-1134">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1134">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="48421-1135">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="48421-1135">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="48421-1136">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="48421-1136">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="48421-1137">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="48421-1137">Remove an LTR backup</span></span>
    - <span data-ttu-id="48421-1138">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="48421-1138">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="48421-1139">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1139">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="48421-1140">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1140">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="48421-1141">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1141">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-1142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-1142">Az.Storage</span></span>
* <span data-ttu-id="48421-1143">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1143">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="48421-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="48421-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="48421-1145">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1145">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="48421-1146">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="48421-1146">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="48421-1147">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="48421-1147">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-1148">Az.Websites</span></span>
* <span data-ttu-id="48421-1149">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1149">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="48421-1150">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="48421-1150">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="48421-1151">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1151">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="48421-1152">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="48421-1152">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="48421-1153">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1153">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="48421-1154">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="48421-1154">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="48421-1155">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="48421-1155">Highlights since the last major release</span></span>
* <span data-ttu-id="48421-1156">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1156">Updated client side telemetry.</span></span>
* <span data-ttu-id="48421-1157">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1157">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="48421-1158">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1158">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-1159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1159">Az.Accounts</span></span>
* <span data-ttu-id="48421-1160">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1160">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-1161">Az.Automation</span></span>
* <span data-ttu-id="48421-1162">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1162">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-1163">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-1163">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-1164">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1164">Updated SDK to 7.0</span></span>
* <span data-ttu-id="48421-1165">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1165">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1166">Az.Compute</span></span>
* <span data-ttu-id="48421-1167">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="48421-1167">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="48421-1168">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-1168">Az.FrontDoor</span></span>
* <span data-ttu-id="48421-1169">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1169">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-1170">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-1170">Az.IotHub</span></span>
* <span data-ttu-id="48421-1171">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1171">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="48421-1172">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-1172">New Cmdlets are:</span></span>
    - <span data-ttu-id="48421-1173">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="48421-1173">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="48421-1174">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="48421-1174">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="48421-1175">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="48421-1175">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="48421-1176">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="48421-1176">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-1177">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-1177">Az.KeyVault</span></span>
* <span data-ttu-id="48421-1178">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1178">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-1179">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-1179">Az.Monitor</span></span>
* <span data-ttu-id="48421-1180">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1180">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="48421-1181">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1181">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="48421-1182">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="48421-1182">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1183">Az.Network</span></span>
* <span data-ttu-id="48421-1184">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1184">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="48421-1185">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1185">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="48421-1186">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1186">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="48421-1187">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="48421-1187">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="48421-1188">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="48421-1188">No new cmdlets are added.</span></span> <span data-ttu-id="48421-1189">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="48421-1189">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-1190">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-1190">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-1191">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1191">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1192">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1192">Az.Resources</span></span>
* <span data-ttu-id="48421-1193">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="48421-1193">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="48421-1194">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="48421-1194">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="48421-1195">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="48421-1195">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="48421-1196">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="48421-1196">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="48421-1197">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-1197">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="48421-1198">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1198">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="48421-1199">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1199">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="48421-1200">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-1200">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1201">Az.Sql</span></span>
* <span data-ttu-id="48421-1202">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1202">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="48421-1203">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1203">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="48421-1204">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="48421-1204">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="48421-1205">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="48421-1205">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="48421-1206">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1206">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="48421-1207">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="48421-1207">Az.StorageSync</span></span>
* <span data-ttu-id="48421-1208">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1208">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="48421-1209">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="48421-1209">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="48421-1210">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="48421-1210">Highlights since the last major release</span></span>
* <span data-ttu-id="48421-1211">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="48421-1211">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="48421-1212">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1212">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-1213">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1213">Az.Accounts</span></span>
* <span data-ttu-id="48421-1214">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="48421-1214">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="48421-1215">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1215">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="48421-1216">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-1216">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-1217">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="48421-1217">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="48421-1218">**New-AzApiManagementProduct** _ ve _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="48421-1218">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="48421-1219"> https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1219">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="48421-1220">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1220">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1221">Az.Compute</span></span>
* <span data-ttu-id="48421-1222">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="48421-1222">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="48421-1223">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1223">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="48421-1224">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1224">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="48421-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="48421-1226">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1226">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1227">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1228">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1228">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="48421-1229">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="48421-1229">Az.DeploymentManager</span></span>
* <span data-ttu-id="48421-1230">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="48421-1230">Adds LIST operations for resources</span></span>
* <span data-ttu-id="48421-1231">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="48421-1231">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-1232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-1232">Az.HDInsight</span></span>
* <span data-ttu-id="48421-1233">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1233">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-1234">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-1234">Az.KeyVault</span></span>
* <span data-ttu-id="48421-1235">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1235">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1236">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1236">Az.Network</span></span>
* <span data-ttu-id="48421-1237">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1237">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="48421-1238">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="48421-1238">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="48421-1239">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1239">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="48421-1240">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1240">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="48421-1241">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="48421-1241">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="48421-1242">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1242">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="48421-1243">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1243">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="48421-1244">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1244">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="48421-1245">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1245">New cmdlets added:</span></span>
        - <span data-ttu-id="48421-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="48421-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="48421-1247">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1247">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="48421-1248">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="48421-1248">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="48421-1249">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1249">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="48421-1250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48421-1250">Az.PolicyInsights</span></span>
* <span data-ttu-id="48421-1251">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="48421-1251">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="48421-1252">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1252">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="48421-1253">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1253">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="48421-1254">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1254">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-1255">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-1256">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1256">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="48421-1257">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="48421-1257">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1258">Az.Resources</span></span>
* <span data-ttu-id="48421-1259">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1259">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="48421-1260">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1260">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1261">Az.Sql</span></span>
<span data-ttu-id="48421-1262">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1262">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-1263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-1263">Az.Storage</span></span>
* <span data-ttu-id="48421-1264">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="48421-1264">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="48421-1265">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-1265">New-AzStorageAccount</span></span>
* <span data-ttu-id="48421-1266">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="48421-1266">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="48421-1267">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1267">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-1268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-1268">Az.Websites</span></span>
* <span data-ttu-id="48421-1269">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="48421-1269">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="48421-1270">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1270">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="48421-1271">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="48421-1271">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1272">Az.Accounts</span></span>
* <span data-ttu-id="48421-1273">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="48421-1274">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="48421-1274">Az.Cdn</span></span>
* <span data-ttu-id="48421-1275">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="48421-1275">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1276">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1276">Az.Compute</span></span>
* <span data-ttu-id="48421-1277">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1277">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="48421-1278">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="48421-1278">Az.ContainerInstance</span></span>
* <span data-ttu-id="48421-1279">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1279">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="48421-1280">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="48421-1280">Az.DataBoxEdge</span></span>
* <span data-ttu-id="48421-1281">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1281">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="48421-1282">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="48421-1282">Get the Edge Storage Container</span></span>
* <span data-ttu-id="48421-1283">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1283">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="48421-1284">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="48421-1284">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="48421-1285">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1285">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="48421-1286">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="48421-1286">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="48421-1287">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1287">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="48421-1288">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="48421-1288">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="48421-1289">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1289">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="48421-1290">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="48421-1290">Get the Edge Storage Account</span></span>
* <span data-ttu-id="48421-1291">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1291">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="48421-1292">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="48421-1292">Create new Edge Storage Account</span></span>
* <span data-ttu-id="48421-1293">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1293">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="48421-1294">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="48421-1294">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="48421-1295">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="48421-1295">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="48421-1296">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="48421-1296">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="48421-1297">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1297">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="48421-1298">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="48421-1298">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1299">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1299">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1300">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1300">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="48421-1301">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1301">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="48421-1302">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1302">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="48421-1303">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="48421-1303">Az.DevTestLabs</span></span>
* <span data-ttu-id="48421-1304">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1304">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-1305">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-1305">Az.EventHub</span></span>
* <span data-ttu-id="48421-1306">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1306">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-1307">Az.HDInsight</span></span>
* <span data-ttu-id="48421-1308">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1308">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="48421-1309">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="48421-1309">Az.MachineLearning</span></span>
* <span data-ttu-id="48421-1310">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1310">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="48421-1311">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="48421-1311">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="48421-1312">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="48421-1312">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="48421-1313">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="48421-1313">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="48421-1314">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="48421-1314">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="48421-1315">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="48421-1315">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="48421-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="48421-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="48421-1317">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="48421-1317">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1318">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1318">Az.Network</span></span>
* <span data-ttu-id="48421-1319">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1319">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-1320">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-1320">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-1321">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1321">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="48421-1322">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1322">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="48421-1323">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1323">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="48421-1324">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1324">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1325">Az.Resources</span></span>
* <span data-ttu-id="48421-1326">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1326">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1327">Az.Sql</span></span>
* <span data-ttu-id="48421-1328">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1328">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="48421-1329">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1329">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="48421-1330">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="48421-1330">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="48421-1331">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1331">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-1332">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-1332">Az.Storage</span></span>
* <span data-ttu-id="48421-1333">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1333">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="48421-1334">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="48421-1334">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="48421-1335">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="48421-1335">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="48421-1336">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-1336">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="48421-1337">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="48421-1337">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="48421-1338">Genel</span><span class="sxs-lookup"><span data-stu-id="48421-1338">General</span></span>
* <span data-ttu-id="48421-1339">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1339">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1340">Az.Accounts</span></span>
* <span data-ttu-id="48421-1341">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="48421-1341">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="48421-1342">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="48421-1342">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="48421-1343">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="48421-1343">Az.Batch</span></span>
* <span data-ttu-id="48421-1344">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1344">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1345">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1346">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1346">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="48421-1347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-1347">Az.FrontDoor</span></span>
* <span data-ttu-id="48421-1348">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1348">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="48421-1349">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1349">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="48421-1350">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="48421-1350">Az.HealthcareApis</span></span>
* <span data-ttu-id="48421-1351">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="48421-1351">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-1352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-1352">Az.KeyVault</span></span>
* <span data-ttu-id="48421-1353">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1353">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="48421-1354">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="48421-1354">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="48421-1355">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1355">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-1356">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-1356">Az.Monitor</span></span>
* <span data-ttu-id="48421-1357">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1357">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="48421-1358">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="48421-1358">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="48421-1359">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="48421-1359">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1360">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1360">Az.Network</span></span>
* <span data-ttu-id="48421-1361">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1361">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1362">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1362">Az.Resources</span></span>
* <span data-ttu-id="48421-1363">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1363">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="48421-1364">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1364">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1365">Az.Sql</span></span>
* <span data-ttu-id="48421-1366">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1366">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-1367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-1367">Az.Storage</span></span>
* <span data-ttu-id="48421-1368">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="48421-1368">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="48421-1369">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="48421-1369">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="48421-1370">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="48421-1370">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="48421-1371">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="48421-1371">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="48421-1372">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="48421-1372">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="48421-1373">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1373">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="48421-1374">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1374">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="48421-1375">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="48421-1375">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="48421-1376">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="48421-1376">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="48421-1377">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1377">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="48421-1378">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="48421-1378">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="48421-1379">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1379">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="48421-1380">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="48421-1380">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="48421-1381">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="48421-1381">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="48421-1382">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="48421-1382">Highlights since the last major release</span></span>
* <span data-ttu-id="48421-1383">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="48421-1383">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="48421-1384">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="48421-1384">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1385">Az.Compute</span></span>
* <span data-ttu-id="48421-1386">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="48421-1386">VM Reapply feature</span></span>
    - <span data-ttu-id="48421-1387">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="48421-1387">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="48421-1388">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="48421-1388">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="48421-1389">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="48421-1389">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="48421-1390">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="48421-1390">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="48421-1391">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1391">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="48421-1392">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1392">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="48421-1393">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1393">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="48421-1394">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1394">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="48421-1395">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1395">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="48421-1396">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1396">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="48421-1397">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="48421-1397">Az.DataBoxEdge</span></span>
* <span data-ttu-id="48421-1398">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1398">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="48421-1399">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="48421-1399">Get the Order</span></span>
* <span data-ttu-id="48421-1400">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1400">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="48421-1401">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="48421-1401">Create new Order</span></span>
* <span data-ttu-id="48421-1402">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1402">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="48421-1403">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="48421-1403">Remove the Order</span></span>
* <span data-ttu-id="48421-1404">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="48421-1404">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="48421-1405">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="48421-1405">Now creates Local Share</span></span>
* <span data-ttu-id="48421-1406">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1406">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="48421-1407">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="48421-1407">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="48421-1408">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1408">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="48421-1409">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="48421-1409">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="48421-1410">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1410">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="48421-1411">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="48421-1411">Gets the information about Triggers</span></span>
* <span data-ttu-id="48421-1412">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1412">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="48421-1413">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="48421-1413">Create new Triggers</span></span>
* <span data-ttu-id="48421-1414">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1414">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="48421-1415">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="48421-1415">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1416">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1416">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1417">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1417">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="48421-1418">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1418">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-1419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-1419">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-1420">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1420">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-1421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-1421">Az.EventHub</span></span>
* <span data-ttu-id="48421-1422">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1422">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="48421-1423">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-1423">Az.FrontDoor</span></span>
* <span data-ttu-id="48421-1424">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1424">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="48421-1425">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1425">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="48421-1426">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1426">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="48421-1427">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="48421-1427">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1428">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1428">Az.Network</span></span>
* <span data-ttu-id="48421-1429">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1429">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="48421-1430">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="48421-1430">Az.PrivateDns</span></span>
* <span data-ttu-id="48421-1431">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1431">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-1432">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-1432">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-1433">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1433">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="48421-1434">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="48421-1434">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="48421-1435">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1435">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="48421-1436">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="48421-1436">Az.RedisCache</span></span>
* <span data-ttu-id="48421-1437">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1437">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="48421-1438">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1438">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="48421-1439">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1439">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1440">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1440">Az.Resources</span></span>
- <span data-ttu-id="48421-1441">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1441">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="48421-1442">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1442">Updated create policy definition help example</span></span>
- <span data-ttu-id="48421-1443">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1443">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="48421-1444">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1444">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="48421-1445">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1445">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1446">Az.Sql</span></span>
* <span data-ttu-id="48421-1447">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1447">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="48421-1448">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1448">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="48421-1449">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="48421-1449">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="48421-1450">Genel</span><span class="sxs-lookup"><span data-stu-id="48421-1450">General</span></span>
* <span data-ttu-id="48421-1451">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="48421-1451">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1452">Az.Accounts</span></span>
* <span data-ttu-id="48421-1453">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="48421-1453">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="48421-1454">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="48421-1454">Az.Advisor</span></span>
* <span data-ttu-id="48421-1455">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1455">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="48421-1456">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="48421-1456">Az.Batch</span></span>
* <span data-ttu-id="48421-1457">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1457">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="48421-1458">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="48421-1458">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="48421-1459">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1459">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="48421-1460">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1460">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="48421-1461">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="48421-1461">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="48421-1462">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="48421-1462">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="48421-1463">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="48421-1463">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="48421-1464">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1464">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="48421-1465">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1465">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="48421-1466">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1466">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="48421-1467">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="48421-1467">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="48421-1468">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="48421-1468">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="48421-1469">**Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1469">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="48421-1470">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="48421-1470">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="48421-1471">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1471">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="48421-1472">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1472">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="48421-1473">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1473">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="48421-1474">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1474">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="48421-1475">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1475">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="48421-1476">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1476">This operation is no longer supported.</span></span>
* <span data-ttu-id="48421-1477">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1477">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="48421-1478">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1478">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="48421-1479">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1479">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="48421-1480">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1480">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="48421-1481">**Get-AzBatchSupportedImage** , **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1481">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="48421-1482">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1482">New non-verified images are also now returned.</span></span> <span data-ttu-id="48421-1483">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1483">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="48421-1484">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1484">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="48421-1485">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1485">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="48421-1486">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1486">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="48421-1487">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1487">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="48421-1488">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1488">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="48421-1489">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1489">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="48421-1490">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1490">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="48421-1491">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="48421-1491">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="48421-1492">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="48421-1492">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="48421-1493">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="48421-1493">Az.Cdn</span></span>
* <span data-ttu-id="48421-1494">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1494">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="48421-1495">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1495">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1496">Az.Compute</span></span>
* <span data-ttu-id="48421-1497">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="48421-1497">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="48421-1498">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="48421-1498">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="48421-1499">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="48421-1499">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="48421-1500">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1500">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="48421-1501">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1501">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="48421-1502">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="48421-1502">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="48421-1503">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1503">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="48421-1504">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="48421-1504">Breaking changes</span></span>
    - <span data-ttu-id="48421-1505">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="48421-1505">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="48421-1506">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="48421-1506">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1507">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1507">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1508">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1508">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-1509">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-1509">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-1510">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="48421-1510">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="48421-1511">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="48421-1511">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="48421-1512">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="48421-1512">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="48421-1513">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="48421-1513">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="48421-1514">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="48421-1514">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="48421-1515">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="48421-1515">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="48421-1516">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-1516">Az.FrontDoor</span></span>
* <span data-ttu-id="48421-1517">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1517">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-1518">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-1518">Az.HDInsight</span></span>
* <span data-ttu-id="48421-1519">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1519">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="48421-1520">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1520">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="48421-1521">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1521">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="48421-1522">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="48421-1522">Removed five cmdlets:</span></span>
    - <span data-ttu-id="48421-1523">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="48421-1523">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="48421-1524">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="48421-1524">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="48421-1525">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="48421-1525">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="48421-1526">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="48421-1526">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="48421-1527">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="48421-1527">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="48421-1528">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1528">Added three cmdlets:</span></span>
    - <span data-ttu-id="48421-1529">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="48421-1529">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="48421-1530">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="48421-1530">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="48421-1531">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="48421-1531">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="48421-1532">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1532">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="48421-1533">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1533">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="48421-1534">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1534">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="48421-1535">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1535">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="48421-1536">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1536">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="48421-1537">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1537">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="48421-1538">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1538">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="48421-1539">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1539">Added some scenario test cases.</span></span>
* <span data-ttu-id="48421-1540">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="48421-1540">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-1541">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-1541">Az.IotHub</span></span>
* <span data-ttu-id="48421-1542">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="48421-1542">Breaking changes:</span></span>
    - <span data-ttu-id="48421-1543">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="48421-1543">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="48421-1544">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1544">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="48421-1545">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="48421-1545">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="48421-1546">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1546">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="48421-1547">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1547">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="48421-1548">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1548">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="48421-1549">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1549">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="48421-1550">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1550">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="48421-1551">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="48421-1551">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="48421-1552">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1552">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="48421-1553">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="48421-1553">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="48421-1554">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1554">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-1555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-1555">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-1556">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1556">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="48421-1557">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1557">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="48421-1558">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1558">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="48421-1559">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1559">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="48421-1560">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1560">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="48421-1561">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1561">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="48421-1562">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1562">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="48421-1563">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-1563">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="48421-1564">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1564">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1565">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1565">Az.Resources</span></span>
* <span data-ttu-id="48421-1566">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1566">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1567">Az.Network</span></span>
* <span data-ttu-id="48421-1568">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1568">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="48421-1569">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1569">Updated cmdlet:</span></span>
        - <span data-ttu-id="48421-1570">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1570">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="48421-1571">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1571">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="48421-1572">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1572">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="48421-1573">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1573">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="48421-1574">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1574">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="48421-1575">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1575">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="48421-1576">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="48421-1576">New cmdlet:</span></span>
        - <span data-ttu-id="48421-1577">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="48421-1577">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="48421-1578">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1578">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="48421-1579">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1579">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="48421-1580">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1580">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="48421-1581">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1581">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="48421-1582">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1582">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="48421-1583">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1583">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="48421-1584">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1584">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="48421-1585">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1585">New cmdlets added:</span></span>
        - <span data-ttu-id="48421-1586">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="48421-1586">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="48421-1587">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="48421-1587">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="48421-1588">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="48421-1588">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="48421-1589">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="48421-1589">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="48421-1590">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="48421-1590">Set-AzVirtualHub</span></span>
* <span data-ttu-id="48421-1591">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1591">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="48421-1592">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1592">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="48421-1593">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1593">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="48421-1594">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1594">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="48421-1595">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1595">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="48421-1596">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1596">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="48421-1597">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1597">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="48421-1598">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1598">New cmdlets added:</span></span>
        - <span data-ttu-id="48421-1599">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1599">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="48421-1600">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1600">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="48421-1601">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1601">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="48421-1602">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1602">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="48421-1603">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1603">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="48421-1604">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1604">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="48421-1605">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1605">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="48421-1606">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1606">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="48421-1607">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1607">New cmdlets added:</span></span>
        - <span data-ttu-id="48421-1608">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="48421-1608">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="48421-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="48421-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="48421-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="48421-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="48421-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="48421-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="48421-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="48421-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="48421-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="48421-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="48421-1614">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1614">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="48421-1615">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1615">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="48421-1616">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1616">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="48421-1617">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1617">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="48421-1618">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1618">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="48421-1619">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="48421-1620">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1620">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="48421-1621">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1621">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="48421-1622">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1622">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="48421-1623">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="48421-1623">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="48421-1624">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1624">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="48421-1625">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1625">New cmdlets added:</span></span>
        - <span data-ttu-id="48421-1626">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="48421-1626">New-AzIpGroup</span></span>
        - <span data-ttu-id="48421-1627">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="48421-1627">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="48421-1628">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="48421-1628">Get-AzIpGroup</span></span>
        - <span data-ttu-id="48421-1629">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="48421-1629">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-1630">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-1630">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-1631">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1631">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1632">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1632">Az.Sql</span></span>
* <span data-ttu-id="48421-1633">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1633">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="48421-1634">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1634">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="48421-1635">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="48421-1635">Removed deprecated aliases:</span></span>
* <span data-ttu-id="48421-1636">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="48421-1636">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="48421-1637">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="48421-1637">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="48421-1638">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1638">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="48421-1639">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1639">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="48421-1640">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1640">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="48421-1641">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1641">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-1642">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-1642">Az.Storage</span></span>
* <span data-ttu-id="48421-1643">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="48421-1643">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="48421-1644">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-1644">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="48421-1645">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-1645">Set-AzStorageAccount</span></span>
* <span data-ttu-id="48421-1646">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="48421-1646">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="48421-1647">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="48421-1647">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="48421-1648">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="48421-1648">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="48421-1649">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="48421-1649">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="48421-1650">Genel</span><span class="sxs-lookup"><span data-stu-id="48421-1650">General</span></span>
* <span data-ttu-id="48421-1651">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="48421-1651">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-1652">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1652">Az.Accounts</span></span>
* <span data-ttu-id="48421-1653">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1653">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="48421-1654">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-1654">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-1655">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1655">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="48421-1656">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1656">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-1657">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-1657">Az.Automation</span></span>
* <span data-ttu-id="48421-1658">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1658">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="48421-1659">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="48421-1659">Az.Batch</span></span>
* <span data-ttu-id="48421-1660">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="48421-1660">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1661">Az.Compute</span></span>
* <span data-ttu-id="48421-1662">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1662">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="48421-1663">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1663">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="48421-1664">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1664">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="48421-1665">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1665">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1666">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1666">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1667">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="48421-1667">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="48421-1668">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="48421-1668">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="48421-1669">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1669">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-1670">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-1670">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-1671">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1671">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="48421-1672">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="48421-1672">Az.HealthcareApis</span></span>
* <span data-ttu-id="48421-1673">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1673">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="48421-1674">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1674">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="48421-1675">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1675">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="48421-1676">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1676">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-1677">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-1677">Az.IotHub</span></span>
* <span data-ttu-id="48421-1678">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="48421-1678">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="48421-1679">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="48421-1679">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-1680">Az.Monitor</span></span>
* <span data-ttu-id="48421-1681">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1681">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="48421-1682">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="48421-1682">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="48421-1683">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="48421-1683">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="48421-1684">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-1684">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1685">Az.Network</span></span>
* <span data-ttu-id="48421-1686">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1686">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="48421-1687">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1687">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="48421-1688">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1688">New cmdlets added:</span></span>
        - <span data-ttu-id="48421-1689">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="48421-1689">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="48421-1690">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1690">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="48421-1691">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1691">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="48421-1692">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1692">Updated cmdlets:</span></span>
        - <span data-ttu-id="48421-1693">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1693">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="48421-1694">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1694">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="48421-1695">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1695">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="48421-1696">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1696">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="48421-1697">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="48421-1697">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="48421-1698">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="48421-1698">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="48421-1699">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="48421-1699">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="48421-1700">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="48421-1700">Az.RedisCache</span></span>
* <span data-ttu-id="48421-1701">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1701">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1702">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1702">Az.Sql</span></span>
* <span data-ttu-id="48421-1703">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1703">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-1704">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-1704">Az.Storage</span></span>
* <span data-ttu-id="48421-1705">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1705">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="48421-1706">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="48421-1706">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="48421-1707">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="48421-1707">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="48421-1708">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="48421-1708">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="48421-1709">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-1709">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="48421-1710">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="48421-1710">Az.StorageSync</span></span>
* <span data-ttu-id="48421-1711">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1711">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-1712">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-1712">Az.Websites</span></span>
* <span data-ttu-id="48421-1713">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="48421-1713">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="48421-1714">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="48421-1714">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="48421-1715">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-1715">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-1716">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1716">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="48421-1717">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1717">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="48421-1718">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="48421-1718">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-1719">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-1719">Az.Automation</span></span>
* <span data-ttu-id="48421-1720">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1720">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="48421-1721">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1721">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="48421-1722">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1722">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1723">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1723">Az.Compute</span></span>
* <span data-ttu-id="48421-1724">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1724">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="48421-1725">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1725">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="48421-1726">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-1726">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="48421-1727">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1727">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="48421-1728">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1728">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="48421-1729">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1729">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="48421-1730">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1730">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="48421-1731">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1731">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="48421-1732">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1732">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1733">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1733">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1734">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="48421-1734">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="48421-1735">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1735">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-1736">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-1736">Az.HDInsight</span></span>
* <span data-ttu-id="48421-1737">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="48421-1737">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-1738">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-1738">Az.IotHub</span></span>
* <span data-ttu-id="48421-1739">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1739">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="48421-1740">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1740">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="48421-1741">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="48421-1741">New cmdlets are:</span></span>
    - <span data-ttu-id="48421-1742">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="48421-1742">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="48421-1743">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="48421-1743">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="48421-1744">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="48421-1744">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="48421-1745">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="48421-1745">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-1746">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-1746">Az.Monitor</span></span>
* <span data-ttu-id="48421-1747">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="48421-1747">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="48421-1748">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="48421-1748">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="48421-1749">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="48421-1749">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="48421-1750">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="48421-1750">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="48421-1751">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1751">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="48421-1752">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken ( **useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1752">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="48421-1753">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="48421-1753">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="48421-1754">**NOT** : Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="48421-1754">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="48421-1755">**Kaynak** ( **ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1755">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="48421-1756">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="48421-1756">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="48421-1757">**AlertingAction** ( **ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1757">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="48421-1758">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="48421-1758">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="48421-1759">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1759">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="48421-1760">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="48421-1760">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="48421-1761">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="48421-1761">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="48421-1762">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="48421-1762">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="48421-1763">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="48421-1763">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="48421-1764">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="48421-1764">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="48421-1765">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1765">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="48421-1766">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1766">Overall improved help files</span></span>
* <span data-ttu-id="48421-1767">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1767">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1768">Az.Network</span></span>
* <span data-ttu-id="48421-1769">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1769">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="48421-1770">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1770">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="48421-1771">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1771">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="48421-1772">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1772">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="48421-1773">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1773">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="48421-1774">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1774">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="48421-1775">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1775">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="48421-1776">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1776">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="48421-1777">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1777">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="48421-1778">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1778">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="48421-1779">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1779">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="48421-1780">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="48421-1780">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="48421-1781">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-1781">New cmdlets</span></span>
        - <span data-ttu-id="48421-1782">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="48421-1782">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="48421-1783">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1783">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="48421-1784">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1784">Updated cmdlet:</span></span>
        - <span data-ttu-id="48421-1785">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="48421-1785">New-VpnSite</span></span>
        - <span data-ttu-id="48421-1786">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="48421-1786">Update-VpnSite</span></span>
        - <span data-ttu-id="48421-1787">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1787">New-VpnConnection</span></span>
        - <span data-ttu-id="48421-1788">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1788">Update-VpnConnection</span></span>
* <span data-ttu-id="48421-1789">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1789">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-1791">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1791">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="48421-1792">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1792">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1793">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1793">Az.Resources</span></span>
* <span data-ttu-id="48421-1794">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1794">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-1795">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-1795">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-1796">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1796">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="48421-1797">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="48421-1797">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="48421-1798">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="48421-1798">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="48421-1799">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="48421-1799">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="48421-1800">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="48421-1800">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="48421-1801">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="48421-1801">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="48421-1802">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="48421-1802">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="48421-1803">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="48421-1803">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="48421-1804">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="48421-1804">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="48421-1805">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="48421-1805">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="48421-1806">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="48421-1806">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="48421-1807">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="48421-1807">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="48421-1808">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="48421-1808">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="48421-1809">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="48421-1809">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="48421-1810">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="48421-1810">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="48421-1811">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1811">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="48421-1812">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="48421-1812">Az.SignalR</span></span>
* <span data-ttu-id="48421-1813">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1813">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1814">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1814">Az.Sql</span></span>
* <span data-ttu-id="48421-1815">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1815">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="48421-1816">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1816">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="48421-1817">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1817">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="48421-1818">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1818">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="48421-1819">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1819">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-1820">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-1820">Az.Storage</span></span>
* <span data-ttu-id="48421-1821">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1821">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="48421-1822">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1822">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="48421-1823">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="48421-1823">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="48421-1824">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="48421-1824">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="48421-1825">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1825">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="48421-1826">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="48421-1826">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="48421-1827">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1827">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="48421-1828">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="48421-1828">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="48421-1829">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="48421-1829">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="48421-1830">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="48421-1830">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="48421-1831">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="48421-1831">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-1832">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-1832">Az.Websites</span></span>
* <span data-ttu-id="48421-1833">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="48421-1833">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="48421-1834">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="48421-1834">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="48421-1835">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1835">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="48421-1836">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="48421-1836">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="48421-1837">Genel</span><span class="sxs-lookup"><span data-stu-id="48421-1837">General</span></span>
* <span data-ttu-id="48421-1838">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1838">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-1839">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1839">Az.Accounts</span></span>
* <span data-ttu-id="48421-1840">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="48421-1840">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="48421-1841">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="48421-1841">Az.Aks</span></span>
* <span data-ttu-id="48421-1842">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1842">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="48421-1843">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="48421-1843">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="48421-1844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-1844">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-1845">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1845">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="48421-1846">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1846">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="48421-1847">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1847">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="48421-1848">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="48421-1848">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="48421-1849">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1849">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="48421-1850">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="48421-1850">Az.Batch</span></span>
* <span data-ttu-id="48421-1851">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1851">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="48421-1852">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="48421-1852">Az.Cdn</span></span>
* <span data-ttu-id="48421-1853">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1853">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1854">Az.Compute</span></span>
* <span data-ttu-id="48421-1855">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1855">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="48421-1856">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1856">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="48421-1857">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1857">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="48421-1858">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1858">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="48421-1859">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="48421-1859">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="48421-1860">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1860">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="48421-1861">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1861">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="48421-1862">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1862">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1863">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1863">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1864">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1864">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="48421-1865">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1865">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="48421-1866">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1866">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="48421-1867">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1867">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-1868">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-1868">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-1869">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1869">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-1870">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-1870">Az.EventHub</span></span>
* <span data-ttu-id="48421-1871">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="48421-1871">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="48421-1872">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="48421-1872">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="48421-1873">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1873">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="48421-1874">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="48421-1874">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="48421-1875">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="48421-1875">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="48421-1876">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1876">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-1877">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-1877">Az.Monitor</span></span>
* <span data-ttu-id="48421-1878">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1878">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1879">Az.Network</span></span>
* <span data-ttu-id="48421-1880">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1880">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="48421-1881">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-1881">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="48421-1882">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1882">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="48421-1883">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="48421-1883">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="48421-1884">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="48421-1884">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="48421-1885">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1885">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="48421-1886">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1886">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-1888">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1888">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="48421-1889">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1889">Added example</span></span>
    - <span data-ttu-id="48421-1890">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1890">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="48421-1891">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1891">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="48421-1892">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1892">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-1893">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-1893">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-1894">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1894">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1895">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1895">Az.Resources</span></span>
* <span data-ttu-id="48421-1896">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1896">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="48421-1897">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1897">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="48421-1898">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="48421-1898">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="48421-1899">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1899">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="48421-1900">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48421-1900">Az.ServiceBus</span></span>
* <span data-ttu-id="48421-1901">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="48421-1901">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="48421-1902">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="48421-1902">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="48421-1903">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1903">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-1904">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-1904">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-1905">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1905">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="48421-1906">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="48421-1906">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="48421-1907">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="48421-1907">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="48421-1908">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1908">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="48421-1909">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="48421-1909">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="48421-1910">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1910">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1911">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1911">Az.Sql</span></span>
* <span data-ttu-id="48421-1912">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1912">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-1913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-1913">Az.Storage</span></span>
* <span data-ttu-id="48421-1914">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1914">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="48421-1915">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="48421-1915">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="48421-1916">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="48421-1916">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="48421-1917">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="48421-1917">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="48421-1918">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="48421-1918">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="48421-1919">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="48421-1919">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-1920">Az.Websites</span></span>
* <span data-ttu-id="48421-1921">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1921">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="48421-1922">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="48421-1922">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-1923">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-1923">Az.Accounts</span></span>
* <span data-ttu-id="48421-1924">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1924">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="48421-1925">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="48421-1925">Az.ApplicationInsights</span></span>
* <span data-ttu-id="48421-1926">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1926">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-1927">Az.Automation</span></span>
* <span data-ttu-id="48421-1928">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1928">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-1929">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-1929">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-1930">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1930">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-1931">Az.Compute</span></span>
* <span data-ttu-id="48421-1932">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1932">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="48421-1933">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="48421-1933">Az.ContainerRegistry</span></span>
* <span data-ttu-id="48421-1934">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1934">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="48421-1935">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="48421-1935">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-1936">Az.DataFactory</span></span>
* <span data-ttu-id="48421-1937">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1937">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="48421-1938">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1938">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-1939">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-1939">Az.EventHub</span></span>
* <span data-ttu-id="48421-1940">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="48421-1940">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="48421-1941">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1941">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-1942">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-1942">Az.KeyVault</span></span>
* <span data-ttu-id="48421-1943">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1943">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="48421-1944">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="48421-1944">Az.LogicApp</span></span>
* <span data-ttu-id="48421-1945">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="48421-1945">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="48421-1946">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1946">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="48421-1947">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="48421-1947">Az.ManagedServices</span></span>
* <span data-ttu-id="48421-1948">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="48421-1948">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-1949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-1949">Az.Network</span></span>
* <span data-ttu-id="48421-1950">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1950">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="48421-1951">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-1951">New cmdlets</span></span>
        - <span data-ttu-id="48421-1952">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="48421-1952">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="48421-1953">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="48421-1953">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="48421-1954">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1954">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="48421-1955">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1955">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="48421-1956">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1956">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="48421-1957">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-1957">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="48421-1958">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="48421-1958">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="48421-1959">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="48421-1959">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="48421-1960">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="48421-1960">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="48421-1961">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1961">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="48421-1962">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1962">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="48421-1963">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1963">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="48421-1964">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1964">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="48421-1965">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1965">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="48421-1966">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1966">Updated cmdlets</span></span>
        - <span data-ttu-id="48421-1967">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1967">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="48421-1968">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1968">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="48421-1969">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1969">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="48421-1970">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1970">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="48421-1971">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1971">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="48421-1972">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-1972">Updated cmdlet:</span></span>
        - <span data-ttu-id="48421-1973">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1973">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="48421-1974">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1974">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="48421-1975">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="48421-1975">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="48421-1976">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1976">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="48421-1977">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-1977">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="48421-1978">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="48421-1978">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-1979">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-1979">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-1980">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-1980">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="48421-1981">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-1981">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-1983">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1983">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="48421-1984">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1984">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="48421-1985">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1985">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="48421-1986">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1986">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="48421-1987">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1987">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="48421-1988">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1988">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="48421-1989">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1989">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="48421-1990">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1990">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="48421-1991">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1991">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="48421-1992">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1992">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-1993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-1993">Az.Resources</span></span>
- <span data-ttu-id="48421-1994">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-1994">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="48421-1995">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-1995">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="48421-1996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48421-1996">Az.ServiceBus</span></span>
* <span data-ttu-id="48421-1997">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="48421-1997">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="48421-1998">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-1998">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-1999">Az.Sql</span></span>
* <span data-ttu-id="48421-2000">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2000">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="48421-2001">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2001">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="48421-2002">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2002">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-2003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2003">Az.Storage</span></span>
* <span data-ttu-id="48421-2004">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2004">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="48421-2005">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="48421-2005">Az.StorageSync</span></span>
* <span data-ttu-id="48421-2006">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="48421-2006">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="48421-2007">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2007">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-2008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2008">Az.Websites</span></span>
* <span data-ttu-id="48421-2009">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2009">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="48421-2010">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2010">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="48421-2011">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2011">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="48421-2012">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2012">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-2013">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2013">Az.Accounts</span></span>
* <span data-ttu-id="48421-2014">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2014">Add support for profile cmdlets</span></span>
* <span data-ttu-id="48421-2015">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2015">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="48421-2016">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2016">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="48421-2017">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="48421-2017">Az.Advisor</span></span>
* <span data-ttu-id="48421-2018">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2018">GA release of Az.Advisor</span></span>
* <span data-ttu-id="48421-2019">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="48421-2019">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="48421-2020">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-2020">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-2021">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2021">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="48421-2022">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="48421-2022">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="48421-2023">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2023">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="48421-2024">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="48421-2024">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="48421-2025">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="48421-2025">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="48421-2026">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="48421-2026">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="48421-2027">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2027">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-2028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-2028">Az.Automation</span></span>
* <span data-ttu-id="48421-2029">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2029">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2030">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2030">Az.Compute</span></span>
* <span data-ttu-id="48421-2031">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2031">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-2032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-2032">Az.DataFactory</span></span>
* <span data-ttu-id="48421-2033">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-2033">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="48421-2034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="48421-2034">Az.EventGrid</span></span>
* <span data-ttu-id="48421-2035">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2035">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-2036">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-2036">Az.IotHub</span></span>
* <span data-ttu-id="48421-2037">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2037">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2038">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2038">Az.Network</span></span>
* <span data-ttu-id="48421-2039">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2039">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="48421-2040">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2040">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="48421-2041">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48421-2041">Az.PolicyInsights</span></span>
* <span data-ttu-id="48421-2042">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2042">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="48421-2043">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="48421-2043">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-2045">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2045">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2046">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-2047">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="48421-2047">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2048">Az.Resources</span></span>
    - <span data-ttu-id="48421-2049">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="48421-2049">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="48421-2050">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2050">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="48421-2051">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2051">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="48421-2052">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2052">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="48421-2053">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48421-2053">Az.ServiceBus</span></span>
* <span data-ttu-id="48421-2054">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2054">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2055">Az.Sql</span></span>
* <span data-ttu-id="48421-2056">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2056">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="48421-2057">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-2057">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="48421-2058">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="48421-2058">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="48421-2059">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="48421-2059">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="48421-2060">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="48421-2060">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="48421-2061">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="48421-2061">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="48421-2062">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="48421-2062">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="48421-2063">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="48421-2063">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="48421-2064">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-2064">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-2065">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2065">Az.Storage</span></span>
* <span data-ttu-id="48421-2066">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-2066">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="48421-2067">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="48421-2067">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="48421-2068">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2068">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="48421-2069">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="48421-2069">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="48421-2070">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2070">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="48421-2071">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-2071">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="48421-2072">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-2072">Set-AzStorageAccount</span></span>
* <span data-ttu-id="48421-2073">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2073">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="48421-2074">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="48421-2074">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="48421-2075">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="48421-2075">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="48421-2076">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="48421-2076">Az.StorageSync</span></span>
* <span data-ttu-id="48421-2077">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="48421-2077">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="48421-2078">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2078">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2079">Az.Accounts</span></span>
* <span data-ttu-id="48421-2080">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2080">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="48421-2081">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="48421-2081">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="48421-2082">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2082">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="48421-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="48421-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="48421-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="48421-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2085">Az.Compute</span></span>
* <span data-ttu-id="48421-2086">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="48421-2086">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="48421-2087">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2087">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="48421-2088">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="48421-2088">Az.Dns</span></span>
* <span data-ttu-id="48421-2089">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2089">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="48421-2090">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="48421-2090">Az.EventGrid</span></span>
* <span data-ttu-id="48421-2091">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2091">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="48421-2092">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="48421-2092">New cmdlets:</span></span>
    - <span data-ttu-id="48421-2093">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="48421-2093">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="48421-2094">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48421-2094">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="48421-2095">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="48421-2095">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="48421-2096">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="48421-2096">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="48421-2097">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="48421-2097">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="48421-2098">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="48421-2098">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="48421-2099">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="48421-2099">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="48421-2100">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="48421-2100">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="48421-2101">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="48421-2101">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="48421-2102">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="48421-2102">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="48421-2103">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="48421-2103">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="48421-2104">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48421-2104">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="48421-2105">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="48421-2105">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="48421-2106">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="48421-2106">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="48421-2107">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="48421-2107">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="48421-2108">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="48421-2108">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="48421-2109">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-2109">Updated cmdlets:</span></span>
    - <span data-ttu-id="48421-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="48421-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="48421-2111">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="48421-2111">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="48421-2112">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="48421-2112">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="48421-2113">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="48421-2113">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="48421-2114">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-2114">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="48421-2115">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="48421-2115">Event subscription expiration date,</span></span>
            - <span data-ttu-id="48421-2116">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="48421-2116">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="48421-2117">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="48421-2117">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="48421-2118">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="48421-2118">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="48421-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="48421-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="48421-2120">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="48421-2120">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="48421-2121">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="48421-2121">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="48421-2122">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="48421-2122">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="48421-2123">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="48421-2123">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="48421-2124">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-2124">Az.FrontDoor</span></span>
* <span data-ttu-id="48421-2125">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="48421-2125">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="48421-2126">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="48421-2126">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="48421-2127">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="48421-2127">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="48421-2128">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="48421-2128">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2129">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2129">Az.Network</span></span>
* <span data-ttu-id="48421-2130">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="48421-2130">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="48421-2131">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2131">New cmdlets</span></span>
        - <span data-ttu-id="48421-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="48421-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="48421-2133">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="48421-2133">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="48421-2134">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2134">New cmdlets</span></span>
        - <span data-ttu-id="48421-2135">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="48421-2135">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="48421-2136">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="48421-2136">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="48421-2137">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2137">New cmdlets</span></span>
        - <span data-ttu-id="48421-2138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="48421-2138">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="48421-2139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="48421-2139">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="48421-2140">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="48421-2140">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="48421-2141">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="48421-2141">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="48421-2142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="48421-2142">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="48421-2143">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="48421-2143">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="48421-2144">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2144">New cmdlets</span></span>
        - <span data-ttu-id="48421-2145">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="48421-2145">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="48421-2146">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="48421-2146">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="48421-2147">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="48421-2147">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="48421-2148">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="48421-2148">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="48421-2149">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="48421-2149">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="48421-2150">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2150">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="48421-2151">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2151">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="48421-2152">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2152">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="48421-2153">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2153">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="48421-2154">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2154">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="48421-2155">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2155">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="48421-2156">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2156">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="48421-2157">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2157">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="48421-2158">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2158">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="48421-2159">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2159">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="48421-2160">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2160">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="48421-2161">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2161">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="48421-2162">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2162">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="48421-2163">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-2163">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="48421-2164">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2164">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="48421-2165">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2165">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="48421-2166">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="48421-2166">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="48421-2167">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="48421-2167">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="48421-2168">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="48421-2168">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="48421-2169">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2169">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="48421-2170">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2170">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="48421-2171">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2171">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-2172">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-2172">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-2173">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2173">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2174">Az.Resources</span></span>
* <span data-ttu-id="48421-2175">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="48421-2175">Support for additional Template Export options</span></span>
    - <span data-ttu-id="48421-2176">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2176">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="48421-2177">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2177">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="48421-2178">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2178">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-2179">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-2179">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-2180">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2180">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2181">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2181">Az.Sql</span></span>
* <span data-ttu-id="48421-2182">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2182">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="48421-2183">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2183">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="48421-2184">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2184">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="48421-2185">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="48421-2185">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="48421-2186">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="48421-2186">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="48421-2187">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="48421-2187">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="48421-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="48421-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="48421-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="48421-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-2190">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2190">Az.Storage</span></span>
* <span data-ttu-id="48421-2191">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="48421-2191">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="48421-2192">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-2192">New-AzStorageAccount</span></span>
* <span data-ttu-id="48421-2193">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2193">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="48421-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="48421-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-2195">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2195">Az.Websites</span></span>
* <span data-ttu-id="48421-2196">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="48421-2196">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="48421-2197">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="48421-2197">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="48421-2198">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2198">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="48421-2199">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="48421-2199">Az.Cdn</span></span>
* <span data-ttu-id="48421-2200">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2200">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2201">Az.Compute</span></span>
* <span data-ttu-id="48421-2202">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2202">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="48421-2203">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="48421-2203">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-2204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-2204">Az.EventHub</span></span>
* <span data-ttu-id="48421-2205">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="48421-2205">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="48421-2206">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="48421-2206">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2207">Az.Network</span></span>
* <span data-ttu-id="48421-2208">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2208">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="48421-2209">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2209">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="48421-2210">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48421-2210">Az.PolicyInsights</span></span>
* <span data-ttu-id="48421-2211">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2211">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2212">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2212">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-2213">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2213">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="48421-2214">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48421-2214">Az.ServiceBus</span></span>
* <span data-ttu-id="48421-2215">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="48421-2215">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-2216">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-2216">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-2217">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2217">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="48421-2218">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2218">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2219">Az.Sql</span></span>
* <span data-ttu-id="48421-2220">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2220">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="48421-2221">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="48421-2221">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="48421-2222">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-2222">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="48421-2223">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="48421-2223">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-2224">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2224">Az.Websites</span></span>
* <span data-ttu-id="48421-2225">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="48421-2225">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="48421-2226">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2226">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="48421-2227">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-2227">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-2228">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2228">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="48421-2229">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="48421-2229">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="48421-2230">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="48421-2230">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="48421-2231">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="48421-2231">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="48421-2232">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48421-2232">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="48421-2233">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="48421-2233">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="48421-2234">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="48421-2234">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="48421-2235">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="48421-2235">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="48421-2236">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2236">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="48421-2237">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="48421-2237">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="48421-2238">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="48421-2238">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="48421-2239">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="48421-2239">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="48421-2240">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="48421-2240">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="48421-2241">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2241">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="48421-2242">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="48421-2242">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="48421-2243">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="48421-2243">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="48421-2244">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="48421-2244">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="48421-2245">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="48421-2245">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="48421-2246">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="48421-2246">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="48421-2247">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="48421-2247">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="48421-2248">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2248">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="48421-2249">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="48421-2249">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="48421-2250">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="48421-2250">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="48421-2251">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2251">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="48421-2252">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2252">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="48421-2253">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2253">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="48421-2254">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="48421-2254">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="48421-2255">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="48421-2255">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="48421-2256">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2256">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="48421-2257">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2257">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="48421-2258">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2258">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="48421-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="48421-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="48421-2260">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2260">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="48421-2261">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2261">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="48421-2262">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="48421-2262">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="48421-2263">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="48421-2263">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="48421-2264">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="48421-2264">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="48421-2265">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2265">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="48421-2266">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2266">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="48421-2267">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2267">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="48421-2268">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="48421-2268">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="48421-2269">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="48421-2269">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="48421-2270">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="48421-2270">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="48421-2271">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="48421-2271">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="48421-2272">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2272">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="48421-2273">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="48421-2273">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="48421-2274">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="48421-2274">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="48421-2275">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="48421-2275">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="48421-2276">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2276">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="48421-2277">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="48421-2277">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="48421-2278">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="48421-2278">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="48421-2279">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="48421-2279">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="48421-2280">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="48421-2280">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="48421-2281">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2281">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="48421-2282">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="48421-2282">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="48421-2283">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="48421-2283">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="48421-2284">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2284">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="48421-2285">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="48421-2285">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="48421-2286">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="48421-2286">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="48421-2287">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2287">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="48421-2288">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2288">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="48421-2289">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="48421-2289">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="48421-2290">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="48421-2290">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="48421-2291">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2291">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="48421-2292">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2292">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="48421-2293">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="48421-2293">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="48421-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="48421-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="48421-2295">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="48421-2295">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="48421-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="48421-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="48421-2297">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="48421-2297">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="48421-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="48421-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="48421-2299">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="48421-2299">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="48421-2300">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="48421-2300">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="48421-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="48421-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="48421-2302">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="48421-2302">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="48421-2303">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="48421-2303">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="48421-2304">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="48421-2304">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-2305">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-2305">Az.Automation</span></span>
* <span data-ttu-id="48421-2306">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2306">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="48421-2307">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2307">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="48421-2308">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2308">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="48421-2309">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2309">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="48421-2310">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2310">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="48421-2311">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2311">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="48421-2312">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="48421-2312">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2313">Az.Compute</span></span>
* <span data-ttu-id="48421-2314">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2314">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="48421-2315">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="48421-2315">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-2316">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-2316">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-2317">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2317">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-2318">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-2318">Az.Monitor</span></span>
* <span data-ttu-id="48421-2319">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2319">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2320">Az.Network</span></span>
* <span data-ttu-id="48421-2321">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2321">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="48421-2322">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="48421-2322">Updated cmdlet:</span></span>
        - <span data-ttu-id="48421-2323">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="48421-2323">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="48421-2324">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2324">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2325">Az.Resources</span></span>
* <span data-ttu-id="48421-2326">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2326">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2327">Az.Sql</span></span>
* <span data-ttu-id="48421-2328">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="48421-2328">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="48421-2329">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2329">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-2330">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2330">Az.Accounts</span></span>
* <span data-ttu-id="48421-2331">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="48421-2331">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-2332">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-2332">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-2333">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="48421-2333">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="48421-2334">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="48421-2334">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2335">Az.Compute</span></span>
* <span data-ttu-id="48421-2336">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="48421-2336">Proximity placement group feature.</span></span>
    - <span data-ttu-id="48421-2337">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="48421-2337">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="48421-2338">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="48421-2338">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="48421-2339">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2339">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="48421-2340">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="48421-2340">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="48421-2341">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2341">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="48421-2342">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="48421-2342">Breaking changes</span></span>
    - <span data-ttu-id="48421-2343">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2343">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="48421-2344">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2344">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="48421-2345">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="48421-2345">Az.DeploymentManager</span></span>
* <span data-ttu-id="48421-2346">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="48421-2346">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="48421-2347">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="48421-2347">Az.Dns</span></span>
* <span data-ttu-id="48421-2348">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="48421-2348">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="48421-2349">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="48421-2349">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="48421-2350">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="48421-2350">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="48421-2351">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-2351">Az.FrontDoor</span></span>
* <span data-ttu-id="48421-2352">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="48421-2352">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="48421-2353">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="48421-2353">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="48421-2354">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-2354">Az.HDInsight</span></span>
* <span data-ttu-id="48421-2355">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="48421-2355">Removed two cmdlets:</span></span>
    - <span data-ttu-id="48421-2356">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="48421-2356">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="48421-2357">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="48421-2357">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="48421-2358">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2358">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="48421-2359">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="48421-2359">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="48421-2360">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="48421-2360">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="48421-2361">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="48421-2361">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-2362">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-2362">Az.Monitor</span></span>
* <span data-ttu-id="48421-2363">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="48421-2363">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="48421-2364">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="48421-2364">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="48421-2365">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="48421-2365">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="48421-2366">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="48421-2366">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="48421-2367">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="48421-2367">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="48421-2368">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="48421-2368">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="48421-2369">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="48421-2369">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="48421-2370">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="48421-2370">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="48421-2371">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="48421-2371">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="48421-2372">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="48421-2372">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="48421-2373">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="48421-2373">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="48421-2374">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="48421-2374">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="48421-2375">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="48421-2375">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="48421-2376">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2376">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2377">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2377">Az.Network</span></span>
* <span data-ttu-id="48421-2378">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="48421-2378">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="48421-2379">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2379">New cmdlets</span></span>
        - <span data-ttu-id="48421-2380">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="48421-2380">New-AzNatGateway</span></span>
        - <span data-ttu-id="48421-2381">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="48421-2381">Get-AzNatGateway</span></span>
        - <span data-ttu-id="48421-2382">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="48421-2382">Set-AzNatGateway</span></span>
        - <span data-ttu-id="48421-2383">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="48421-2383">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="48421-2384">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2384">Updated cmdlets</span></span>
        - <span data-ttu-id="48421-2385">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="48421-2385">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="48421-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="48421-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="48421-2387">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="48421-2387">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="48421-2388">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2388">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="48421-2389">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2389">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="48421-2390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48421-2390">Az.PolicyInsights</span></span>
* <span data-ttu-id="48421-2391">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-2391">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="48421-2392">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="48421-2392">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="48421-2393">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="48421-2393">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2394">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2394">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-2395">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-2395">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="48421-2396">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="48421-2396">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="48421-2397">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="48421-2397">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="48421-2398">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="48421-2398">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="48421-2399">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="48421-2399">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="48421-2400">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="48421-2400">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="48421-2401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="48421-2401">Az.Relay</span></span>
* <span data-ttu-id="48421-2402">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="48421-2402">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="48421-2403">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48421-2403">Az.ServiceBus</span></span>
* <span data-ttu-id="48421-2404">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2404">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-2405">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2405">Az.Storage</span></span>
* <span data-ttu-id="48421-2406">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="48421-2406">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="48421-2407">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="48421-2407">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="48421-2408">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="48421-2408">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="48421-2409">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-2409">New-AzStorageAccount</span></span>
* <span data-ttu-id="48421-2410">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="48421-2410">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="48421-2411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-2411">New-AzStorageAccount</span></span>
    - <span data-ttu-id="48421-2412">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-2412">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="48421-2413">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-2413">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-2414">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2414">Az.Websites</span></span>
* <span data-ttu-id="48421-2415">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="48421-2415">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="48421-2416">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="48421-2416">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="48421-2417">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2417">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="48421-2418">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="48421-2418">Highlights since the last major release</span></span>
* <span data-ttu-id="48421-2419">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2419">General availability of `Az` module</span></span>
* <span data-ttu-id="48421-2420">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="48421-2420">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="48421-2421">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="48421-2421">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="48421-2422">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2422">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="48421-2423">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2423">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="48421-2424">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2424">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="48421-2425">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2425">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-2426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2426">Az.Accounts</span></span>
* <span data-ttu-id="48421-2427">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2427">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="48421-2428">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="48421-2428">Az.Batch</span></span>
* <span data-ttu-id="48421-2429">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="48421-2430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="48421-2430">Az.Cdn</span></span>
* <span data-ttu-id="48421-2431">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-2432">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-2432">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-2433">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2433">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2434">Az.Compute</span></span>
* <span data-ttu-id="48421-2435">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2435">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="48421-2436">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="48421-2437">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2437">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-2438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-2438">Az.DataFactory</span></span>
* <span data-ttu-id="48421-2439">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2439">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-2441">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2441">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="48421-2442">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="48421-2442">Az.EventGrid</span></span>
* <span data-ttu-id="48421-2443">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2443">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-2444">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-2444">Az.EventHub</span></span>
* <span data-ttu-id="48421-2445">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2445">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="48421-2446">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48421-2446">Az.HDInsight</span></span>
* <span data-ttu-id="48421-2447">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2447">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-2448">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-2448">Az.IotHub</span></span>
* <span data-ttu-id="48421-2449">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2449">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-2450">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-2450">Az.KeyVault</span></span>
* <span data-ttu-id="48421-2451">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2451">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="48421-2452">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2452">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="48421-2453">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="48421-2453">Az.MachineLearning</span></span>
* <span data-ttu-id="48421-2454">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2454">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="48421-2455">Az.Media</span><span class="sxs-lookup"><span data-stu-id="48421-2455">Az.Media</span></span>
* <span data-ttu-id="48421-2456">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-2457">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-2457">Az.Monitor</span></span>
  * <span data-ttu-id="48421-2458">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="48421-2458">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="48421-2459">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="48421-2459">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="48421-2460">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="48421-2460">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="48421-2461">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="48421-2461">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="48421-2462">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="48421-2462">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="48421-2463">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="48421-2463">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="48421-2464">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2464">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2465">Az.Network</span></span>
* <span data-ttu-id="48421-2466">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2466">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="48421-2467">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2467">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="48421-2468">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="48421-2468">Az.NotificationHubs</span></span>
* <span data-ttu-id="48421-2469">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2469">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-2470">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-2470">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-2471">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2471">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="48421-2472">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="48421-2472">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="48421-2473">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2474">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2474">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-2475">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="48421-2476">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="48421-2476">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="48421-2477">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2477">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="48421-2478">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2478">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="48421-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="48421-2479">Az.RedisCache</span></span>
* <span data-ttu-id="48421-2480">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2481">Az.Resources</span></span>
* <span data-ttu-id="48421-2482">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2482">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2483">Az.Sql</span></span>
* <span data-ttu-id="48421-2484">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2484">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="48421-2485">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2485">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="48421-2486">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2486">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="48421-2487">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2487">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="48421-2488">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2488">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="48421-2489">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-2489">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="48421-2490">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2490">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-2491">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2491">Az.Websites</span></span>
* <span data-ttu-id="48421-2492">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2492">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="48421-2493">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="48421-2494">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2494">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="48421-2495">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="48421-2495">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="48421-2496">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2496">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="48421-2497">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="48421-2497">Highlights since the last major release</span></span>
* <span data-ttu-id="48421-2498">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2498">General availability of `Az` module</span></span>
* <span data-ttu-id="48421-2499">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="48421-2499">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="48421-2500">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="48421-2500">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="48421-2501">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2501">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="48421-2502">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2502">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="48421-2503">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2503">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="48421-2504">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2504">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="48421-2505">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2505">Az.Accounts</span></span>
* <span data-ttu-id="48421-2506">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2506">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="48421-2507">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48421-2507">Az.AnalysisServices</span></span>
* <span data-ttu-id="48421-2508">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="48421-2508">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="48421-2509">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="48421-2509">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-2510">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-2510">Az.Automation</span></span>
* <span data-ttu-id="48421-2511">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2511">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="48421-2512">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="48421-2512">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="48421-2513">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="48421-2513">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2514">Az.Compute</span></span>
* <span data-ttu-id="48421-2515">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2515">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="48421-2516">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2516">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="48421-2517">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="48421-2517">Az.ContainerInstance</span></span>
* <span data-ttu-id="48421-2518">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2518">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-2519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-2519">Az.DataFactory</span></span>
* <span data-ttu-id="48421-2520">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2520">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="48421-2521">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2521">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2522">Az.Resources</span></span>
* <span data-ttu-id="48421-2523">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2523">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="48421-2524">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2524">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="48421-2525">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="48421-2525">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="48421-2526">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="48421-2526">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="48421-2527">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2527">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="48421-2528">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="48421-2528">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2529">Az.Sql</span></span>
* <span data-ttu-id="48421-2530">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-2530">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-2531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2531">Az.Storage</span></span>
* <span data-ttu-id="48421-2532">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="48421-2532">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="48421-2533">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="48421-2533">New-AzStorageContext</span></span>
* <span data-ttu-id="48421-2534">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="48421-2534">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="48421-2535">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="48421-2535">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="48421-2536">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="48421-2536">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="48421-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="48421-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="48421-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="48421-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="48421-2539">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="48421-2539">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="48421-2540">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="48421-2540">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="48421-2541">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="48421-2541">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="48421-2542">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="48421-2542">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="48421-2543">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="48421-2543">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="48421-2544">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2544">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="48421-2545">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="48421-2545">Highlights since the last major release</span></span>
* <span data-ttu-id="48421-2546">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2546">General availability of `Az` module</span></span>
* <span data-ttu-id="48421-2547">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="48421-2547">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="48421-2548">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="48421-2548">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="48421-2549">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2549">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="48421-2550">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2550">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="48421-2551">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2551">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="48421-2552">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2552">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-2553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-2553">Az.Automation</span></span>
* <span data-ttu-id="48421-2554">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="48421-2554">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="48421-2555">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="48421-2555">Dynamic grouping</span></span>
    * <span data-ttu-id="48421-2556">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="48421-2556">Pre-Post script</span></span>
    * <span data-ttu-id="48421-2557">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="48421-2557">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2558">Az.Compute</span></span>
* <span data-ttu-id="48421-2559">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="48421-2559">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="48421-2560">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2560">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-2561">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-2561">Az.KeyVault</span></span>
* <span data-ttu-id="48421-2562">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2562">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2563">Az.Network</span></span>
* <span data-ttu-id="48421-2564">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2564">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="48421-2565">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2565">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2566">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2566">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-2567">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2567">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="48421-2568">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2568">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2569">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2569">Az.Resources</span></span>
* <span data-ttu-id="48421-2570">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2570">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="48421-2571">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2571">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2572">Az.Sql</span></span>
* <span data-ttu-id="48421-2573">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2573">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-2574">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2574">Az.Storage</span></span>
* <span data-ttu-id="48421-2575">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="48421-2575">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="48421-2576">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="48421-2576">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="48421-2577">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="48421-2577">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="48421-2578">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="48421-2578">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="48421-2579">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="48421-2579">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="48421-2580">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="48421-2580">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="48421-2581">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="48421-2581">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-2582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2582">Az.Websites</span></span>
* <span data-ttu-id="48421-2583">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2583">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="48421-2584">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2584">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-2585">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2585">Az.Accounts</span></span>
* <span data-ttu-id="48421-2586">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2586">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="48421-2587">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2587">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-2588">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-2588">Az.Automation</span></span>
* <span data-ttu-id="48421-2589">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2589">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="48421-2590">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2590">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="48421-2591">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="48421-2591">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="48421-2592">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="48421-2592">Az.Cdn</span></span>
* <span data-ttu-id="48421-2593">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="48421-2593">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2594">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2594">Az.Compute</span></span>
* <span data-ttu-id="48421-2595">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2595">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-2596">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-2596">Az.DataFactory</span></span>
* <span data-ttu-id="48421-2597">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2597">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="48421-2598">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="48421-2598">Az.LogicApp</span></span>
* <span data-ttu-id="48421-2599">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="48421-2599">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2600">Az.Network</span></span>
* <span data-ttu-id="48421-2601">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2601">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2602">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2602">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-2603">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2603">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="48421-2604">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="48421-2604">SDK Update</span></span>
* <span data-ttu-id="48421-2605">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-2605">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="48421-2606">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2606">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2607">Az.Resources</span></span>
* <span data-ttu-id="48421-2608">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2608">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="48421-2609">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="48421-2609">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="48421-2610">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2610">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="48421-2611">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="48421-2611">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="48421-2612">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2612">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="48421-2613">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="48421-2613">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2614">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2614">Az.Sql</span></span>
* <span data-ttu-id="48421-2615">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-2615">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="48421-2616">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-2616">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-2617">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2617">Az.Storage</span></span>
* <span data-ttu-id="48421-2618">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48421-2618">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="48421-2619">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2619">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="48421-2620">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48421-2620">Az.AnalysisServices</span></span>
* <span data-ttu-id="48421-2621">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="48421-2621">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-2622">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-2622">Az.Automation</span></span>
* <span data-ttu-id="48421-2623">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2623">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="48421-2624">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2624">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="48421-2625">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2625">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-2626">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-2626">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-2627">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2627">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2628">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2628">Az.Compute</span></span>
* <span data-ttu-id="48421-2629">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2629">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="48421-2630">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2630">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="48421-2631">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2631">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="48421-2632">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="48421-2632">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-2633">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-2633">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-2634">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2634">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="48421-2635">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="48421-2635">Az.EventHub</span></span>
* <span data-ttu-id="48421-2636">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2636">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-2637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-2637">Az.KeyVault</span></span>
* <span data-ttu-id="48421-2638">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2638">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="48421-2639">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="48421-2639">Az.LogicApp</span></span>
* <span data-ttu-id="48421-2640">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2640">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="48421-2641">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2641">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="48421-2642">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2642">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="48421-2643">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="48421-2643">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="48421-2644">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="48421-2644">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="48421-2645">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="48421-2645">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="48421-2646">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="48421-2646">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="48421-2647">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="48421-2647">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="48421-2648">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="48421-2648">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="48421-2649">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="48421-2649">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="48421-2650">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="48421-2650">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="48421-2651">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="48421-2651">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="48421-2652">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2652">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="48421-2653">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-2653">Az.Monitor</span></span>
* <span data-ttu-id="48421-2654">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2654">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2655">Az.Network</span></span>
* <span data-ttu-id="48421-2656">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2656">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="48421-2657">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-2657">Az.OperationalInsights</span></span>
* <span data-ttu-id="48421-2658">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="48421-2658">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="48421-2659">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2659">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="48421-2660">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2660">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2661">Az.Resources</span></span>
* <span data-ttu-id="48421-2662">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2662">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="48421-2663">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2663">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="48421-2664">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2664">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="48421-2665">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2665">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2666">Az.Sql</span></span>
* <span data-ttu-id="48421-2667">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2667">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="48421-2668">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2668">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2669">Az.Websites</span></span>
* <span data-ttu-id="48421-2670">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2670">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="48421-2671">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2671">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-2672">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2672">Az.Accounts</span></span>
* <span data-ttu-id="48421-2673">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="48421-2673">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="48421-2674">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48421-2674">Az.AnalysisServices</span></span>
<span data-ttu-id="48421-2675">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="48421-2675">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2676">Az.Compute</span></span>
* <span data-ttu-id="48421-2677">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2677">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="48421-2678">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2678">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="48421-2679">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2679">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2680">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2680">Az.RecoveryServices</span></span>
<span data-ttu-id="48421-2681">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="48421-2681">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2682">Az.Resources</span></span>
* <span data-ttu-id="48421-2683">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2683">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="48421-2684">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="48421-2684">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="48421-2685">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2685">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="48421-2686">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="48421-2686">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2687">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2687">Az.Sql</span></span>
* <span data-ttu-id="48421-2688">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="48421-2688">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="48421-2689">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2689">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="48421-2690">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2690">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="48421-2691">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2691">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-2692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2692">Az.Accounts</span></span>
* <span data-ttu-id="48421-2693">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="48421-2693">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="48421-2694">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48421-2694">Az.AnalysisServices</span></span>
* <span data-ttu-id="48421-2695">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="48421-2695">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2696">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2696">Az.RecoveryServices</span></span>
* <span data-ttu-id="48421-2697">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="48421-2697">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="48421-2698">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2698">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-2699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2699">Az.Accounts</span></span>
* <span data-ttu-id="48421-2700">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2700">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="48421-2701">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2701">Update incorrect online help URLs</span></span>
* <span data-ttu-id="48421-2702">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2702">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="48421-2703">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="48421-2703">Az.Aks</span></span>
* <span data-ttu-id="48421-2704">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2704">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="48421-2705">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-2705">Az.Automation</span></span>
* <span data-ttu-id="48421-2706">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2706">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="48421-2707">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2707">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="48421-2708">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="48421-2708">Az.Cdn</span></span>
* <span data-ttu-id="48421-2709">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2709">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2710">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2710">Az.Compute</span></span>
* <span data-ttu-id="48421-2711">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2711">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="48421-2712">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2712">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="48421-2713">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2713">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="48421-2714">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="48421-2714">Az.ContainerRegistry</span></span>
* <span data-ttu-id="48421-2715">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2715">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="48421-2716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="48421-2716">Az.DataFactory</span></span>
* <span data-ttu-id="48421-2717">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2717">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-2718">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-2718">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-2719">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2719">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="48421-2720">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="48421-2720">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="48421-2721">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2721">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-2722">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-2722">Az.IotHub</span></span>
* <span data-ttu-id="48421-2723">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2723">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="48421-2724">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-2724">Az.KeyVault</span></span>
* <span data-ttu-id="48421-2725">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2725">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2726">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2726">Az.Network</span></span>
* <span data-ttu-id="48421-2727">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2727">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2728">Az.Resources</span></span>
* <span data-ttu-id="48421-2729">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2729">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="48421-2730">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2730">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="48421-2731">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2731">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="48421-2732">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2732">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="48421-2733">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2733">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="48421-2734">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2734">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="48421-2735">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="48421-2735">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-2737">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="48421-2737">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="48421-2738">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2738">Fix some error messages.</span></span>
* <span data-ttu-id="48421-2739">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2739">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="48421-2740">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2740">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="48421-2741">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="48421-2741">Az.SignalR</span></span>
* <span data-ttu-id="48421-2742">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2742">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2743">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2743">Az.Sql</span></span>
* <span data-ttu-id="48421-2744">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2744">Update incorrect online help URLs</span></span>
* <span data-ttu-id="48421-2745">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2745">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="48421-2746">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2746">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="48421-2747">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="48421-2747">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-2748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2748">Az.Storage</span></span>
* <span data-ttu-id="48421-2749">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2749">Update incorrect online help URLs</span></span>
* <span data-ttu-id="48421-2750">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-2750">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="48421-2751">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="48421-2751">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="48421-2752">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="48421-2752">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="48421-2753">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="48421-2753">Az.TrafficManager</span></span>
* <span data-ttu-id="48421-2754">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2754">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-2755">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2755">Az.Websites</span></span>
* <span data-ttu-id="48421-2756">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2756">Update incorrect online help URLs</span></span>
* <span data-ttu-id="48421-2757">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2757">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="48421-2758">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2758">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="48421-2759">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="48421-2759">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="48421-2760">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2760">Az.Accounts</span></span>
* <span data-ttu-id="48421-2761">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2761">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2762">Az.Compute</span></span>
* <span data-ttu-id="48421-2763">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="48421-2763">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="48421-2764">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2764">Updated the description of ID in help files</span></span>
* <span data-ttu-id="48421-2765">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="48421-2765">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-2766">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-2767">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2767">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="48421-2768">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2768">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="48421-2769">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="48421-2769">Az.EventGrid</span></span>
* <span data-ttu-id="48421-2770">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2770">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="48421-2771">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2771">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="48421-2772">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-2772">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="48421-2773">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="48421-2773">Event Time-To-Live,</span></span>
        - <span data-ttu-id="48421-2774">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="48421-2774">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="48421-2775">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="48421-2775">Dead letter endpoint.</span></span>
    - <span data-ttu-id="48421-2776">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-2776">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="48421-2777">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="48421-2777">Event Time-To-Live,</span></span>
        - <span data-ttu-id="48421-2778">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="48421-2778">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="48421-2779">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="48421-2779">Dead letter endpoint.</span></span>
* <span data-ttu-id="48421-2780">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2780">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="48421-2781">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-2781">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="48421-2782">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="48421-2782">Az.IotHub</span></span>
* <span data-ttu-id="48421-2783">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2783">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="48421-2784">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="48421-2784">Az.LogicApp</span></span>
* <span data-ttu-id="48421-2785">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="48421-2785">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-2786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2786">Az.Resources</span></span>
* <span data-ttu-id="48421-2787">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2787">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="48421-2788">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="48421-2788">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="48421-2789">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2789">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="48421-2790">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2790">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="48421-2791">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2791">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="48421-2792">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="48421-2792">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="48421-2793">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="48421-2793">Az.SignalR</span></span>
* <span data-ttu-id="48421-2794">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="48421-2794">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-2795">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2795">Az.Sql</span></span>
* <span data-ttu-id="48421-2796">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="48421-2796">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="48421-2797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2797">Az.Storage</span></span>
* <span data-ttu-id="48421-2798">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="48421-2798">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="48421-2799">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="48421-2799">New-AzStorageContext</span></span>
* <span data-ttu-id="48421-2800">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2800">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="48421-2801">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="48421-2801">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2802">Az.Websites</span></span>
* <span data-ttu-id="48421-2803">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2803">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="48421-2804">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="48421-2804">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="48421-2805">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="48421-2805">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="48421-2806">Genel</span><span class="sxs-lookup"><span data-stu-id="48421-2806">General</span></span>

- <span data-ttu-id="48421-2807">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2807">General Availability of Az Module</span></span>
- <span data-ttu-id="48421-2808">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="48421-2808">Online help for each module</span></span>
- <span data-ttu-id="48421-2809">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="48421-2809">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="48421-2810">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2810">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="48421-2811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="48421-2811">Az.Accounts</span></span>
- <span data-ttu-id="48421-2812">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="48421-2812">Changed from Az.Profile</span></span>
- <span data-ttu-id="48421-2813">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2813">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="48421-2814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-2814">Az.ApiManagement</span></span>
- <span data-ttu-id="48421-2815">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="48421-2815">Fixes for #7002</span></span>
- <span data-ttu-id="48421-2816">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="48421-2817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="48421-2817">Az.Batch</span></span>
- <span data-ttu-id="48421-2818">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2818">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="48421-2819">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="48421-2819">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="48421-2820">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="48421-2821">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="48421-2821">Az.Billing</span></span>
- <span data-ttu-id="48421-2822">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2822">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="48421-2823">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="48421-2823">Az.CognitivServices</span></span>
- <span data-ttu-id="48421-2824">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2824">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="48421-2825">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-2825">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="48421-2826">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="48421-2826">Az.ContainerInstance</span></span>
- <span data-ttu-id="48421-2827">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2827">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="48421-2828">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="48421-2828">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="48421-2829">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2829">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="48421-2830">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-2830">Az.DataLakeStore</span></span>
- <span data-ttu-id="48421-2831">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="48421-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="48421-2832">Az.Monitor</span></span>
- <span data-ttu-id="48421-2833">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2833">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="48421-2834">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48421-2834">Az.KeyVault</span></span>
- <span data-ttu-id="48421-2835">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-2835">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="48421-2836">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="48421-2836">Az.MachineLearning</span></span>
- <span data-ttu-id="48421-2837">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2837">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="48421-2838">Az.Media</span><span class="sxs-lookup"><span data-stu-id="48421-2838">Az.Media</span></span>
- <span data-ttu-id="48421-2839">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="48421-2839">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="48421-2840">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2840">Az.Network</span></span>
<span data-ttu-id="48421-2841">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2841">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="48421-2842">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="48421-2842">New cmdlets added:</span></span>
        - <span data-ttu-id="48421-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48421-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="48421-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48421-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="48421-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48421-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="48421-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48421-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="48421-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="48421-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="48421-2848">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="48421-2848">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="48421-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="48421-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="48421-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="48421-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="48421-2851">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2851">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="48421-2852">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48421-2852">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="48421-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="48421-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="48421-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="48421-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="48421-2855">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="48421-2855">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="48421-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="48421-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="48421-2857">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="48421-2857">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="48421-2858">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2858">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="48421-2859">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="48421-2859">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="48421-2860">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="48421-2860">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="48421-2861">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="48421-2861">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="48421-2862">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2862">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="48421-2863">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2863">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="48421-2864">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48421-2864">Az.OperationalInsights</span></span>
- <span data-ttu-id="48421-2865">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2865">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="48421-2866">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="48421-2866">Az.Profile</span></span>
- <span data-ttu-id="48421-2867">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2867">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2868">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2868">Az.RecoveryServices</span></span>
- <span data-ttu-id="48421-2869">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2869">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="48421-2870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2870">Az.Resources</span></span>
- <span data-ttu-id="48421-2871">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2871">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="48421-2872">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-2872">Az.ServiceFabric</span></span>
- <span data-ttu-id="48421-2873">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="48421-2873">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="48421-2874">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2874">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="48421-2875">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="48421-2875">Az.SIgnalR</span></span>
- <span data-ttu-id="48421-2876">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="48421-2876">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="48421-2877">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2877">Az.Sql</span></span>
- <span data-ttu-id="48421-2878">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2878">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="48421-2879">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2879">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="48421-2880">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2880">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="48421-2881">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2881">Az.Storage</span></span>
- <span data-ttu-id="48421-2882">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2882">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="48421-2883">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2883">Az.Websites</span></span>
- <span data-ttu-id="48421-2884">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="48421-2884">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="48421-2885">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="48421-2885">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="48421-2886">Genel</span><span class="sxs-lookup"><span data-stu-id="48421-2886">General</span></span>

* <span data-ttu-id="48421-2887">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="48421-2887">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="48421-2888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2888">Az.Compute</span></span>

* <span data-ttu-id="48421-2889">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2889">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="48421-2890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-2890">Az.DataLakeStore</span></span>

* <span data-ttu-id="48421-2891">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2891">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="48421-2892">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="48421-2892">Az.FrontDoor</span></span>

* <span data-ttu-id="48421-2893">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2893">Fixed some broken links</span></span>
    - <span data-ttu-id="48421-2894">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2894">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="48421-2895">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2895">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="48421-2896">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48421-2896">Az.RecoveryServices</span></span>

* <span data-ttu-id="48421-2897">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2897">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="48421-2898">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2898">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="48421-2899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2899">Az.Resources</span></span>

* <span data-ttu-id="48421-2900"> https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="48421-2900">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="48421-2901">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2901">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="48421-2902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2902">Az.Sql</span></span>

* <span data-ttu-id="48421-2903">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="48421-2903">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="48421-2904">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2904">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="48421-2905">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2905">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="48421-2906">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="48421-2906">Az.Storage</span></span>

* <span data-ttu-id="48421-2907">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2907">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="48421-2908">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2908">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="48421-2909">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="48421-2909">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="48421-2910">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2910">Support Static Website configuration</span></span>
    - <span data-ttu-id="48421-2911">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="48421-2911">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="48421-2912">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="48421-2912">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="48421-2913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-2913">Az.Websites</span></span>

* <span data-ttu-id="48421-2914">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="48421-2914">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="48421-2915">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2915">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="48421-2916">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="48421-2916">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="48421-2917">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="48421-2917">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="48421-2918">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48421-2918">Az.ApiManagement</span></span>
* <span data-ttu-id="48421-2919">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="48421-2919">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="48421-2920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="48421-2920">Az.Automation</span></span>
* <span data-ttu-id="48421-2921">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="48421-2921">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="48421-2922">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2922">Added Update Management cmdlets</span></span>
* <span data-ttu-id="48421-2923">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2923">Added Source Control cmdlets</span></span>
* <span data-ttu-id="48421-2924">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2924">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="48421-2925">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2925">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="48421-2926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2926">Az.Compute</span></span>
* <span data-ttu-id="48421-2927">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2927">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="48421-2928">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="48421-2928">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="48421-2929">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="48421-2929">Az.ContainerInstance</span></span>
* <span data-ttu-id="48421-2930">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="48421-2930">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="48421-2931">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="48421-2931">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="48421-2932">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2932">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="48421-2933">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2933">Az.Network</span></span>
* <span data-ttu-id="48421-2934">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2934">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="48421-2935">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2935">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="48421-2936">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2936">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="48421-2937">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2937">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="48421-2938">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="48421-2938">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="48421-2939">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2939">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="48421-2940">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="48421-2940">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="48421-2941">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="48421-2941">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="48421-2942">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2942">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="48421-2943">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="48421-2943">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="48421-2944">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="48421-2944">Az.Relay</span></span>
* <span data-ttu-id="48421-2945">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2945">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="48421-2946">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-2946">Az.Resources</span></span>
* <span data-ttu-id="48421-2947">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2947">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="48421-2948">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2948">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="48421-2949">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="48421-2949">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="48421-2950">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-2950">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-2951">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2951">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="48421-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-2952">Az.Sql</span></span>
* <span data-ttu-id="48421-2953">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2953">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="48421-2954">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="48421-2954">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="48421-2955">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="48421-2955">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="48421-2956">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="48421-2956">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="48421-2957">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="48421-2957">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="48421-2958">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="48421-2958">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="48421-2959">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="48421-2959">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="48421-2960">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="48421-2960">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="48421-2961">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="48421-2961">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="48421-2962">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2962">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="48421-2963">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2963">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="48421-2964">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2964">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="48421-2965">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="48421-2965">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="48421-2966">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="48421-2966">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="48421-2967">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="48421-2967">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="48421-2968">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="48421-2968">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="48421-2969">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2969">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="48421-2970">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="48421-2970">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="48421-2971">Genel</span><span class="sxs-lookup"><span data-stu-id="48421-2971">General</span></span>
* <span data-ttu-id="48421-2972">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="48421-2972">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="48421-2973">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="48421-2973">Az.Profile</span></span>
* <span data-ttu-id="48421-2974">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2974">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="48421-2975">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2975">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="48421-2976">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-2976">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="48421-2977">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2977">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="48421-2978">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2978">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="48421-2979">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2979">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="48421-2980">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2980">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-2981">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-2981">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-2982">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2982">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-2983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-2983">Az.Compute</span></span>
* <span data-ttu-id="48421-2984">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-2984">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="48421-2985">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="48421-2985">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="48421-2986">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2986">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-2987">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-2988">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-2988">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="48421-2989">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-2989">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="48421-2990">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="48421-2990">Az.Insights</span></span>
* <span data-ttu-id="48421-2991">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2991">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="48421-2992">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="48421-2992">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="48421-2993">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-2993">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="48421-2994">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="48421-2994">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-2995">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-2995">Az.Network</span></span>
* <span data-ttu-id="48421-2996">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="48421-2996">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="48421-2997">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="48421-2997">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="48421-2998">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="48421-2998">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="48421-2999">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="48421-2999">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="48421-3000">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="48421-3000">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="48421-3001">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="48421-3001">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="48421-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="48421-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="48421-3003">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48421-3003">Az.PolicyInsights</span></span>
* <span data-ttu-id="48421-3004">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-3004">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-3005">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-3005">Az.Resources</span></span>
* <span data-ttu-id="48421-3006"> https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="48421-3006">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="48421-3007">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="48421-3007">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="48421-3008">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48421-3008">Az.ServiceBus</span></span>
* <span data-ttu-id="48421-3009">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-3009">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="48421-3010">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48421-3010">Az.ServiceFabric</span></span>
* <span data-ttu-id="48421-3011">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-3011">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="48421-3012">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-3012">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="48421-3013">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="48421-3013">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="48421-3014">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="48421-3014">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="48421-3015">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-3015">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="48421-3016">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="48421-3016">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="48421-3017">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="48421-3017">Az.Profile</span></span>
* <span data-ttu-id="48421-3018">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="48421-3018">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="48421-3019">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="48421-3019">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-3020">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-3020">Az.Compute</span></span>
* <span data-ttu-id="48421-3021">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-3021">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="48421-3022">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-3022">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="48421-3023">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48421-3023">Az.DataLakeStore</span></span>
* <span data-ttu-id="48421-3024">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="48421-3024">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="48421-3025">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="48421-3025">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="48421-3026">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="48421-3026">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="48421-3027">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="48421-3027">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="48421-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="48421-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-3029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-3029">Az.Network</span></span>
* <span data-ttu-id="48421-3030">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="48421-3030">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="48421-3031">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-3031">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-3032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-3032">Az.Resources</span></span>
* <span data-ttu-id="48421-3033">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="48421-3033">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="48421-3034">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="48421-3034">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="48421-3035">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="48421-3035">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="48421-3036">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="48421-3036">Azure.Storage</span></span>
* <span data-ttu-id="48421-3037">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="48421-3037">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="48421-3038">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="48421-3038">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="48421-3039">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="48421-3039">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="48421-3040">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="48421-3040">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="48421-3041">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="48421-3041">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="48421-3042">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48421-3042">Az.CognitiveServices</span></span>
* <span data-ttu-id="48421-3043">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="48421-3043">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="48421-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="48421-3044">Az.Compute</span></span>
* <span data-ttu-id="48421-3045">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-3045">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="48421-3046">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-3046">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="48421-3047">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-3047">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="48421-3048">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="48421-3048">Az.DataFactoryV2</span></span>
* <span data-ttu-id="48421-3049">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="48421-3049">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="48421-3050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="48421-3050">Az.Network</span></span>
* <span data-ttu-id="48421-3051">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="48421-3051">Added NetworkProfile functionality.</span></span> <span data-ttu-id="48421-3052">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-3052">new cmdlets added</span></span>
    - <span data-ttu-id="48421-3053">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="48421-3053">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="48421-3054">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="48421-3054">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="48421-3055">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="48421-3055">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="48421-3056">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="48421-3056">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="48421-3057">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="48421-3057">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="48421-3058">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="48421-3058">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="48421-3059">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-3059">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="48421-3060">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-3060">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="48421-3061">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-3061">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="48421-3062">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="48421-3062">Az.RedisCache</span></span>
* <span data-ttu-id="48421-3063">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="48421-3063">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="48421-3064">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-3064">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="48421-3065">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48421-3065">Az.Resources</span></span>
* <span data-ttu-id="48421-3066">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="48421-3066">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="48421-3067">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-3067">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="48421-3068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="48421-3068">Az.Sql</span></span>
* <span data-ttu-id="48421-3069">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="48421-3069">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="48421-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="48421-3070">Az.Websites</span></span>
* <span data-ttu-id="48421-3071">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="48421-3071">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="48421-3072">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="48421-3072">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="48421-3073">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="48421-3073">0.2.0 - September 2018</span></span>
 <span data-ttu-id="48421-3074">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="48421-3074">Initial Release</span></span>
