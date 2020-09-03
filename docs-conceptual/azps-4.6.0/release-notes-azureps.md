---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8892d11dafef724f499a7766836d23f30b2be24f
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239528"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="46e91-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="46e91-103">Azure PowerShell release notes</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="46e91-104">4.6.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-104">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-105">Az.Accounts</span></span>
* <span data-ttu-id="46e91-106">Bulma uç noktası varsayılan AzureCloud ortamını veya diğer genel ortamları döndürmediğinden tüm genel bulut ortamları yüklendi (#12633)</span><span class="sxs-lookup"><span data-stu-id="46e91-106">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="46e91-107">SubscriptionPolicies, 'Get-AzSubscription' cmdlet’inde kullanıma sunuldu [#12551]</span><span class="sxs-lookup"><span data-stu-id="46e91-107">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-108">Az.Automation</span></span>
* <span data-ttu-id="46e91-109">Karma Çalışanı Grubu belirtmek için 'Set-AzAutomationWebhook' cmdlet’ine '-RunOn' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-109">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-110">Az.Compute</span></span>
* <span data-ttu-id="46e91-111">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' ve 'Update-AzVmss' cmdlet’lerine '-EncryptionAtHost' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-111">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="46e91-112">'Get-AzVM' ve 'Get-AzVmss' cmdlet’lerinin dönüş nesnesine 'SecurityProfile' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-112">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="46e91-113">'-InstanceView' anahtarı 'Get-AzHostGroup' cmdlet’ine isteğe bağlı parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-113">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="46e91-114">Yeni 'Invoke-AzVmPatchAssessment' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-114">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-115">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-116">PSPipelineRun sınıfındaki eksik özellikler eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-116">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-117">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-117">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-118">Konakta şifreleme özelliğiyle küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-118">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-119">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-120">Geçici silmeyi devre dışı bırakma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-120">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="46e91-121">SecretValueText özniteliğini kaldırma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-121">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="46e91-122">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="46e91-122">Az.Maintenance</span></span>
* <span data-ttu-id="46e91-123">'New-AzMaintenanceConfiguration' cmdlet’ine isteğe bağlı zamanlamayla ilgili alanlar eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-123">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="46e91-124">'Get-AzMaintenancePublicConfiguration' için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-124">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="46e91-125">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="46e91-125">Az.ManagedServices</span></span>
* <span data-ttu-id="46e91-126">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-126">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-127">Az.Monitor</span></span>
* <span data-ttu-id="46e91-128">Günlüklerin ve Ölçümlerin ayrılmasını etkinleştirmek için 'Set-AzDiagnosticSetting' cmdlet’indeki parametre kümesi genişletildi [#12482]</span><span class="sxs-lookup"><span data-stu-id="46e91-128">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="46e91-129">'Add-AzMetricAlertRuleV2' cmdlet’inde işlem hattından ölçüm uyarısı alınırken oluşan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-129">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-130">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-130">Az.Resources</span></span>
* <span data-ttu-id="46e91-131">'Get-AzPolicyAlias' cmdlet’i, diğer adın Azure İlkesi tarafından değiştirilebilir olup olmadığını belirten bilgiler içerek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-131">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="46e91-132">Yeni 'Set-AzRoleAssignment' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-132">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="46e91-133">Yönetim grubu kapsamındaki ARM şablonu Durum sonuçlarını almak için 'Get-AzDeploymentManagementGroupWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-133">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="46e91-134">Kiracı kapsamındaki ARM şablonu Durum sonuçlarını almaya yönelik yeni 'Get-AzTenantWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-134">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="46e91-135">'New-AzManagementGroupDeployment' ve 'New-AzTenantDeployment' için '-WhatIf' ve '-Confirm' parametreleri, ARM şablonu Durum sonuçlarını kullanacak şekilde geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="46e91-135">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="46e91-136">Yeni dağıtım cmdlet’lerindeki '-WhatIf' ve '-Confirm' parametrelerinin davranışları False ile uyumlu olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-136">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="46e91-137">'-TemplateObject' ve 'TemplateParameterObject' için serileştirme hatası düzeltildi [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="46e91-137">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="46e91-138">'Get-AzResourceGroupDeploymentOperation' cmdlet’ine, yaklaşan çıkış türü değişikliğine yönelik hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-138">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46e91-139">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46e91-139">Az.SignalR</span></span>
* <span data-ttu-id="46e91-140">'Restart-AzSignalR' ve 'Update-AzSignalR' yardım dosyalarındaki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-140">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="46e91-141">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-141">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-142">Az.Storage</span></span>
* <span data-ttu-id="46e91-143">Blob sorgu hızlandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-143">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="46e91-144">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="46e91-144">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="46e91-145">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="46e91-145">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="46e91-146">Yardım dosyası güncelleştirildi, daha fazla açıklama eklendi ve yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-146">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="46e91-147">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="46e91-147">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="46e91-148">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46e91-148">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="46e91-149">İlgili alt dizin mevcut olmadığında blobu indirme işleminin başarısız olmasıyla ilgili sorun düzeltildi [#12592]</span><span class="sxs-lookup"><span data-stu-id="46e91-149">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="46e91-150">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="46e91-150">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="46e91-151">Depolama hesaplarında Set/Get/Remove Nesne Çoğaltma İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-151">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="46e91-152">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="46e91-152">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="46e91-153">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="46e91-153">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="46e91-154">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="46e91-154">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="46e91-155">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="46e91-155">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="46e91-156">Bir Depolama hesabının Blob Hizmeti üzerinde ChangeFeed’i etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-156">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="46e91-157">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="46e91-157">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="46e91-158">4.5.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-158">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-159">Az.Accounts</span></span>
* <span data-ttu-id="46e91-160">'Connect-AzAccount' cmdlet’i 'MaxContextPopulation' parametresini kabul edecek şekilde güncelleştirildi [#9865]</span><span class="sxs-lookup"><span data-stu-id="46e91-160">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="46e91-161">SubscriptionClient sürümü 2019-06-01 olarak ve kiracı etki alanlarını görüntüleyecek şekilde güncelleştirildi [#9838]</span><span class="sxs-lookup"><span data-stu-id="46e91-161">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="46e91-162">Aboneliğin giriş kiracısı ve yöneten kiracısı bilgilerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-162">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="46e91-163">Telemetri verilerindeki modül adı ve sürüm bilgileri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-163">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="46e91-164">SqlDatabaseDnsSuffix ve ServiceManagementUrl, ortam meta verileri uç noktasının uyumsuz değer döndürdüğü durumlar için ayarlandı</span><span class="sxs-lookup"><span data-stu-id="46e91-164">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="46e91-165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46e91-165">Az.Aks</span></span>
* <span data-ttu-id="46e91-166">'ClientIdAndSecret' kaldırılarak 'ServicePrincipalIdAndSecret' eklendi ve 'ClientIdAndSecret' bir diğer ad olarak ayarlandı [#12381].</span><span class="sxs-lookup"><span data-stu-id="46e91-166">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="46e91-167">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' cmdlet’leri kaldırılarak 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' eklendi ve özgün olanlar diğer ad olarak ayarlandı [#12373].</span><span class="sxs-lookup"><span data-stu-id="46e91-167">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46e91-168">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-168">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-169">Yeni 'Add-AzApiManagementApiToGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-169">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="46e91-170">Yeni 'Get-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-170">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="46e91-171">Yeni 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-171">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="46e91-172">Yeni 'Get-AzApiManagementGatewayKey' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-172">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="46e91-173">Yeni 'New-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-173">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="46e91-174">Yeni 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-174">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="46e91-175">Yeni 'New-AzApiManagementResourceLocationObject' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-175">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="46e91-176">Yeni 'Remove-AzApiManagementApiFromGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-176">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="46e91-177">Yeni 'Remove-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-177">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="46e91-178">Yeni 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-178">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="46e91-179">Yeni 'Update-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-179">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="46e91-180">'Get-AzApiManagementApi' cmdlet’ine yeni ve isteğe bağlı [-GatewayId] parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-180">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-181">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-181">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-182">'Deny', özellikle NetworkRules varsayılan eylemi olarak kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-182">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46e91-183">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-183">Az.FrontDoor</span></span>
* <span data-ttu-id="46e91-184">Enum.Parse metodu, bir null değeri Enabled veya Disabled sabit listesi değerlerine zorladığında özel durum oluşturulmasıyla ilgili bir sorun düzeltildi [#12344]</span><span class="sxs-lookup"><span data-stu-id="46e91-184">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-185">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-185">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-186">Aktarma özelliğinde şifrelemeye sahip küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-186">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="46e91-187">'New-AzHDInsightCluster' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-187">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="46e91-188">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-188">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="46e91-189">Özel bağlantı özelliğine sahip küme oluşturma desteği eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-189">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="46e91-190">'New-AzHDInsightCluster' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-190">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="46e91-191">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-191">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="46e91-192">'New-AzHDInsightCluster' veya 'Get-AzHDInsightCluster' çağrıldığında sanal ağ bilgileri döndürüldü</span><span class="sxs-lookup"><span data-stu-id="46e91-192">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-193">Az.Network</span></span>
* <span data-ttu-id="46e91-194">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-194">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="46e91-195">Hataya neden olmayan değişiklikler eklendi: 'Remove-AzExpressRouteCircutPeeringConfig' cmdlet’inde Özel Eşleme’ye yönelik PeerAddressType işlevi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-195">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="46e91-196">AddressPrefixType ve PeerAddressType parametresindeki kodlar büyük/küçük harfi yoksayacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-196">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="46e91-197">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-197">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-198">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-199">'Remove-AzOperationalInsightsworkspace' için '-ForceDelete' seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-199">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="46e91-200">Yeni 'Get-AzOperationalInsightsDeletedWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-200">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="46e91-201">Yeni 'Restore-AzOperationalInsightsWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-201">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-202">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-203">Azure Backup kapsayıcı/öğe keşif deneyimi iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-203">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-204">Az.Resources</span></span>
* <span data-ttu-id="46e91-205">'New-AzRoleAssignment' cmdlet’ine 'Condition', 'ConditionVersion' ve 'Description' özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-205">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="46e91-206">Bu, veri modellerinde yapılan tüm ilgili değişiklikleri içerir</span><span class="sxs-lookup"><span data-stu-id="46e91-206">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-207">Az.Sql</span></span>
* <span data-ttu-id="46e91-208">'New-AzSqlServer' ve 'Set-AzSqlServer' cmdlet’lerindeki sunucu adının olası büyük/küçük harfe duyarsızlık hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-208">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="46e91-209">'New-AzSqlDatabaseSecondary' cmdlet’indeki mevcut veritabanına yanlış veritabanı adının döndürülmesi hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-209">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-210">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-210">Az.Storage</span></span>
* <span data-ttu-id="46e91-211">Yeni x,t izniyle kapsayıcı/blob Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-211">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="46e91-212">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="46e91-212">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="46e91-213">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="46e91-213">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="46e91-214">Yeni x,t,f izniyle hesap Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-214">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="46e91-215">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="46e91-215">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="46e91-216">Tek dosya paylaşımı kullanımını alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-216">Supported get single file share usage</span></span>
    - <span data-ttu-id="46e91-217">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="46e91-217">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="46e91-218">4.4.0 - Temmuz 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-218">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-219">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-219">Az.Accounts</span></span>
* <span data-ttu-id="46e91-220">“Invoke-AzRestMethod” adlı yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-220">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="46e91-221">“Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]</span><span class="sxs-lookup"><span data-stu-id="46e91-221">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="46e91-222">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46e91-222">Az.Aks</span></span>
* <span data-ttu-id="46e91-223">“Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]</span><span class="sxs-lookup"><span data-stu-id="46e91-223">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46e91-224">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46e91-224">Az.AnalysisServices</span></span>
* <span data-ttu-id="46e91-225">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-225">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-226">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-226">Az.Automation</span></span>
* <span data-ttu-id="46e91-227">Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-227">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-228">Az.Compute</span></span>
* <span data-ttu-id="46e91-229">“En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-229">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-230">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-231">Data Factory’ye genel parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-231">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46e91-232">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46e91-232">Az.EventGrid</span></span>
* <span data-ttu-id="46e91-233">2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-233">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="46e91-234">Yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-234">Added new features:</span></span>
    - <span data-ttu-id="46e91-235">Giriş eşleme</span><span class="sxs-lookup"><span data-stu-id="46e91-235">Input mapping</span></span>
    - <span data-ttu-id="46e91-236">Olay Teslim Şeması</span><span class="sxs-lookup"><span data-stu-id="46e91-236">Event Delivery Schema</span></span>
    - <span data-ttu-id="46e91-237">Özel Bağlantı</span><span class="sxs-lookup"><span data-stu-id="46e91-237">Private Link</span></span>
    - <span data-ttu-id="46e91-238">Bulut Olayı V10 Şeması</span><span class="sxs-lookup"><span data-stu-id="46e91-238">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="46e91-239">Hedef Olarak Service Bus Konu Başlığı</span><span class="sxs-lookup"><span data-stu-id="46e91-239">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="46e91-240">Hedef Olarak Azure İşlevi</span><span class="sxs-lookup"><span data-stu-id="46e91-240">Azure Function As Destination</span></span>
    - <span data-ttu-id="46e91-241">Web Kancası Toplu İş</span><span class="sxs-lookup"><span data-stu-id="46e91-241">WebHook Batching</span></span>
    - <span data-ttu-id="46e91-242">Güvenli web kancası (AAD desteği)</span><span class="sxs-lookup"><span data-stu-id="46e91-242">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="46e91-243">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="46e91-243">IpFiltering</span></span>
* <span data-ttu-id="46e91-244">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-244">Updated cmdlets:</span></span>
    - <span data-ttu-id="46e91-245">“New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="46e91-245">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="46e91-246">Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-246">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="46e91-247">AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-247">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="46e91-248">Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-248">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="46e91-249">Teslim şeması için yeni, isteğe bağlı parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-249">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="46e91-250">“New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="46e91-250">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="46e91-251">IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-251">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="46e91-252">“New-AzEventGridTopic'/'New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="46e91-252">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="46e91-253">Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-253">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46e91-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-254">Az.FrontDoor</span></span>
* <span data-ttu-id="46e91-255">Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-255">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="46e91-256">Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-256">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-257">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-258">Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-258">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-259">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-259">Az.Monitor</span></span>
* <span data-ttu-id="46e91-260">Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]</span><span class="sxs-lookup"><span data-stu-id="46e91-260">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-261">Az.Network</span></span>
* <span data-ttu-id="46e91-262">VWan HubVnet bağlantısında değişen parametreler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-262">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="46e91-263">Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-263">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="46e91-264">“Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="46e91-264">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="46e91-265">“New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="46e91-265">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="46e91-266">“Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="46e91-266">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="46e91-267">“Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="46e91-267">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="46e91-268">“New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="46e91-268">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="46e91-269">Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-269">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="46e91-270">“Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="46e91-270">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="46e91-271">“New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="46e91-271">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="46e91-272">“Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="46e91-272">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="46e91-273">“Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="46e91-273">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="46e91-274">“Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="46e91-274">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="46e91-275">“New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="46e91-275">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="46e91-276">Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-276">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="46e91-277">Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-277">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="46e91-278">Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-278">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-279">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-279">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-280">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-280">Removed project reference to Authentication</span></span>
* <span data-ttu-id="46e91-281">Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı</span><span class="sxs-lookup"><span data-stu-id="46e91-281">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="46e91-282">Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="46e91-282">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-283">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-283">Az.Resources</span></span>
* <span data-ttu-id="46e91-284">“Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-284">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="46e91-285">“Unregister-AzResourceProvider” cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-285">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-286">Az.Sql</span></span>
* <span data-ttu-id="46e91-287">“Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-287">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="46e91-288">Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-288">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="46e91-289">Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="46e91-289">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-290">Az.Storage</span></span>
* <span data-ttu-id="46e91-291">Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-291">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="46e91-292">MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-292">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="46e91-293">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46e91-293">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="46e91-294">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46e91-294">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="46e91-295">Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-295">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="46e91-296">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="46e91-296">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="46e91-297">Blob sürümlerini içeren destek listesi blobları</span><span class="sxs-lookup"><span data-stu-id="46e91-297">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="46e91-298">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="46e91-298">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="46e91-299">Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-299">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="46e91-300">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="46e91-300">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="46e91-301">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="46e91-301">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="46e91-302">Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-302">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="46e91-303">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="46e91-303">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="46e91-304">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="46e91-304">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="46e91-305">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="46e91-305">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="46e91-306">“Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="46e91-306">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="46e91-307">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="46e91-307">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46e91-308">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46e91-308">Az.StorageSync</span></span>
* <span data-ttu-id="46e91-309">ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-309">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="46e91-310">“UpdateStorageSyncService” cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-310">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="46e91-311">“Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="46e91-311">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="46e91-312">StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-312">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-313">Az.Websites</span></span>
* <span data-ttu-id="46e91-314">App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-314">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="46e91-315">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-315">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-316">Az.Accounts</span></span>
* <span data-ttu-id="46e91-317">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-317">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="46e91-318">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="46e91-318">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="46e91-319">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-319">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="46e91-320">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="46e91-320">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="46e91-321">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46e91-321">Az.Aks</span></span>
* <span data-ttu-id="46e91-322">Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-322">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46e91-323">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46e91-323">Az.Batch</span></span>
* <span data-ttu-id="46e91-324">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-324">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="46e91-325">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-325">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-326">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-326">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-327">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-327">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="46e91-328">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-328">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-329">Az.Compute</span></span>
* <span data-ttu-id="46e91-330">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-330">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="46e91-331">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-331">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="46e91-332">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="46e91-332">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="46e91-333">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-333">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="46e91-334">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-334">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-335">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-335">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-336">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-336">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46e91-337">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46e91-337">Az.EventHub</span></span>
* <span data-ttu-id="46e91-338">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-338">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="46e91-339">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="46e91-339">Az.Functions</span></span>
* <span data-ttu-id="46e91-340">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-340">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-341">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-341">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-342">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-342">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="46e91-343">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="46e91-343">Az.HealthcareApis</span></span>
* <span data-ttu-id="46e91-344">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-344">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="46e91-345">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-345">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-346">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-346">Az.Monitor</span></span>
* <span data-ttu-id="46e91-347">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-347">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="46e91-348">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="46e91-348">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-349">Az.Network</span></span>
* <span data-ttu-id="46e91-350">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-350">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="46e91-351">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-351">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="46e91-352">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="46e91-352">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="46e91-353">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-353">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="46e91-354">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-354">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="46e91-355">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="46e91-355">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="46e91-356">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="46e91-356">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="46e91-357">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="46e91-357">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="46e91-358">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="46e91-358">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="46e91-359">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="46e91-359">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="46e91-360">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-360">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="46e91-361">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-361">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="46e91-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="46e91-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="46e91-363">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="46e91-363">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="46e91-364">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-364">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="46e91-365">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-365">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="46e91-366">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-366">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="46e91-367">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-367">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="46e91-368">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-368">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="46e91-369">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="46e91-369">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="46e91-370">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-370">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="46e91-371">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-371">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="46e91-372">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-372">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="46e91-373">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-373">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="46e91-374">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-374">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="46e91-375">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-375">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="46e91-376">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="46e91-376">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="46e91-377">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-377">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="46e91-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="46e91-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="46e91-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="46e91-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="46e91-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="46e91-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="46e91-384">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-384">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="46e91-385">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="46e91-385">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="46e91-386">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="46e91-386">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="46e91-387">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="46e91-387">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="46e91-388">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="46e91-388">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="46e91-389">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="46e91-389">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="46e91-390">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-390">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="46e91-391">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="46e91-391">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="46e91-392">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="46e91-392">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="46e91-393">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="46e91-393">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="46e91-394">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="46e91-394">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="46e91-395">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="46e91-395">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="46e91-396">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="46e91-396">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="46e91-397">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="46e91-397">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="46e91-398">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="46e91-398">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-399">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-399">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-400">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="46e91-400">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="46e91-401">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-401">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="46e91-402">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-402">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="46e91-403">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="46e91-403">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="46e91-404">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="46e91-404">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-405">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-405">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-406">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-406">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="46e91-407">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="46e91-407">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-408">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-408">Az.Resources</span></span>
* <span data-ttu-id="46e91-409">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="46e91-409">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="46e91-410">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="46e91-410">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="46e91-411">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-411">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="46e91-412">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-412">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="46e91-413">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-413">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="46e91-414">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-414">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-415">Az.Sql</span></span>
* <span data-ttu-id="46e91-416">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-416">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="46e91-417">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-417">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="46e91-418">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="46e91-418">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-419">Az.Storage</span></span>
* <span data-ttu-id="46e91-420">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-420">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="46e91-421">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46e91-421">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="46e91-422">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="46e91-422">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-423">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-423">Az.Websites</span></span>
* <span data-ttu-id="46e91-424">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-424">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="46e91-425">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-425">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="46e91-426">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-426">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="46e91-427">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-427">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="46e91-428">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-428">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="46e91-429">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-429">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="46e91-430">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-430">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-431">Az.Accounts</span></span>
* <span data-ttu-id="46e91-432">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="46e91-432">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46e91-433">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46e91-433">Az.AnalysisServices</span></span>
* <span data-ttu-id="46e91-434">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-434">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46e91-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-435">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-436">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-436">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="46e91-437">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="46e91-437">Az.Billing</span></span>
* <span data-ttu-id="46e91-438">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-438">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-439">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-439">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-440">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-440">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-441">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-442">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-442">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="46e91-443">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="46e91-443">Az.DataShare</span></span>
* <span data-ttu-id="46e91-444">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-444">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="46e91-445">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="46e91-445">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="46e91-446">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-446">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-447">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-448">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-448">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="46e91-449">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-449">Added optional parameters to</span></span> 
    - <span data-ttu-id="46e91-450">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="46e91-450">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="46e91-451">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="46e91-451">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46e91-452">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-452">Az.PolicyInsights</span></span>
* <span data-ttu-id="46e91-453">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-453">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="46e91-454">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="46e91-454">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="46e91-455">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-455">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="46e91-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="46e91-456">Az.PrivateDns</span></span>
* <span data-ttu-id="46e91-457">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-457">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-459">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-459">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="46e91-460">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-460">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-461">Az.Resources</span></span>
* <span data-ttu-id="46e91-462">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-462">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="46e91-463">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="46e91-463">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="46e91-464">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-464">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="46e91-465">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-465">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="46e91-466">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-466">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-467">Az.Sql</span></span>
* <span data-ttu-id="46e91-468">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-468">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="46e91-469">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-469">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="46e91-470">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-470">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-471">Az.Storage</span></span>
* <span data-ttu-id="46e91-472">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-472">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="46e91-473">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-473">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="46e91-474">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="46e91-474">Highlights since the last release</span></span>
* <span data-ttu-id="46e91-475">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="46e91-475">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="46e91-476">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-476">General availability of Az.Functions</span></span> 
* <span data-ttu-id="46e91-477">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="46e91-477">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-478">Az.Accounts</span></span>
* <span data-ttu-id="46e91-479">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-479">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="46e91-480">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="46e91-480">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="46e91-481">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46e91-481">Az.Aks</span></span>
* <span data-ttu-id="46e91-482">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-482">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="46e91-483">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-483">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="46e91-484">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="46e91-484">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46e91-485">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-485">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-486">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-486">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="46e91-487">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="46e91-487">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="46e91-488">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-488">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="46e91-489">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-489">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="46e91-490">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-490">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="46e91-491">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-491">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="46e91-492">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-492">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="46e91-493">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-493">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="46e91-494">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-494">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="46e91-495">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-495">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="46e91-496">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="46e91-496">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="46e91-497">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="46e91-497">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="46e91-498">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="46e91-498">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="46e91-499">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="46e91-499">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="46e91-500">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="46e91-500">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="46e91-501">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="46e91-501">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="46e91-502">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-502">Az.ApplicationInsights</span></span>
* <span data-ttu-id="46e91-503">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="46e91-503">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="46e91-504">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-504">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="46e91-505">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-505">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46e91-506">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46e91-506">Az.Batch</span></span>
* <span data-ttu-id="46e91-507">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-507">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="46e91-508">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-508">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="46e91-509">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-509">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="46e91-510">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-510">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="46e91-511">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="46e91-511">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="46e91-512">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-512">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="46e91-513">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-513">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="46e91-514">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="46e91-514">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="46e91-515">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-515">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-516">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-516">Az.Compute</span></span>
* <span data-ttu-id="46e91-517">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-517">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="46e91-518">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-518">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="46e91-519">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="46e91-519">Breaking changes</span></span>
    - <span data-ttu-id="46e91-520">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-520">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="46e91-521">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-521">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="46e91-522">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-522">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="46e91-523">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-523">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="46e91-524">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-524">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="46e91-525">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-525">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="46e91-526">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-526">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-527">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-528">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-528">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46e91-529">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-529">Az.FrontDoor</span></span>
* <span data-ttu-id="46e91-530">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-530">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="46e91-531">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-531">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="46e91-532">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-532">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="46e91-533">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-533">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="46e91-534">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="46e91-534">Az.Functions</span></span>
* <span data-ttu-id="46e91-535">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-535">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-536">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-536">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-537">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="46e91-537">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="46e91-538">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="46e91-538">Az.HealthcareApis</span></span>
* <span data-ttu-id="46e91-539">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="46e91-539">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-540">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-540">Az.IotHub</span></span>
* <span data-ttu-id="46e91-541">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-541">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="46e91-542">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="46e91-542">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="46e91-543">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-543">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="46e91-544">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-544">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="46e91-545">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="46e91-545">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="46e91-546">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-546">New cmdlets are:</span></span>
    - <span data-ttu-id="46e91-547">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="46e91-547">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="46e91-548">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="46e91-548">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="46e91-549">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="46e91-549">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="46e91-550">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="46e91-550">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="46e91-551">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-551">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="46e91-552">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-552">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-553">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-554">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="46e91-554">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="46e91-555">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-555">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="46e91-556">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="46e91-556">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="46e91-557">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-557">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="46e91-558">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="46e91-558">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="46e91-559">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="46e91-559">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="46e91-560">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-560">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-561">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-561">Az.Monitor</span></span>
* <span data-ttu-id="46e91-562">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="46e91-562">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="46e91-563">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-563">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="46e91-564">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-564">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="46e91-565">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="46e91-565">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="46e91-566">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="46e91-566">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="46e91-567">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="46e91-567">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="46e91-568">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-568">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-569">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-569">Az.Network</span></span>
* <span data-ttu-id="46e91-570">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-570">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="46e91-571">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="46e91-571">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="46e91-572">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="46e91-572">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="46e91-573">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="46e91-573">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="46e91-574">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-574">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="46e91-575">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-575">New cmdlets added:</span></span>
        - <span data-ttu-id="46e91-576">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="46e91-576">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="46e91-577">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="46e91-577">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="46e91-578">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="46e91-578">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="46e91-579">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="46e91-579">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="46e91-580">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-580">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="46e91-581">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-581">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="46e91-582">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-582">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="46e91-583">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="46e91-583">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="46e91-584">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="46e91-584">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="46e91-585">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-585">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="46e91-586">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="46e91-586">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="46e91-587">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="46e91-587">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="46e91-588">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="46e91-588">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="46e91-589">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="46e91-589">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="46e91-590">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="46e91-590">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="46e91-591">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-591">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="46e91-592">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-592">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="46e91-593">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-593">Updated cmdlet:</span></span>
        - <span data-ttu-id="46e91-594">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="46e91-594">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-595">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-595">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-596">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-596">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="46e91-597">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-597">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="46e91-598">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="46e91-598">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="46e91-599">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="46e91-599">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="46e91-600">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="46e91-600">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="46e91-601">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-601">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="46e91-602">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-602">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="46e91-603">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-603">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-604">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-604">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-605">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-605">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="46e91-606">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-606">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="46e91-607">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-607">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="46e91-608">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-608">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="46e91-609">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-609">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-610">Az.Resources</span></span>
* <span data-ttu-id="46e91-611">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-611">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="46e91-612">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-612">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="46e91-613">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="46e91-613">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="46e91-614">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="46e91-614">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="46e91-615">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="46e91-615">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="46e91-616">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="46e91-616">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="46e91-617">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="46e91-617">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="46e91-618">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="46e91-618">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="46e91-619">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-619">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="46e91-620">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-620">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="46e91-621">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-621">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="46e91-622">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-622">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="46e91-623">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-623">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="46e91-624">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-624">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="46e91-625">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-625">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="46e91-626">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-626">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="46e91-627">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="46e91-627">'New-AzDeployment'</span></span>
    - <span data-ttu-id="46e91-628">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="46e91-628">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="46e91-629">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="46e91-629">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="46e91-630">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="46e91-630">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46e91-631">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-631">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-632">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-632">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-633">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-633">Az.Sql</span></span>
* <span data-ttu-id="46e91-634">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-634">Enhance performance of:</span></span>
    - <span data-ttu-id="46e91-635">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="46e91-635">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="46e91-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="46e91-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="46e91-637">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="46e91-637">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="46e91-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="46e91-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="46e91-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="46e91-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="46e91-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="46e91-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="46e91-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="46e91-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="46e91-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="46e91-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="46e91-643">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-643">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="46e91-644">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-644">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-645">Az.Storage</span></span>
* <span data-ttu-id="46e91-646">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-646">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="46e91-647">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-647">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="46e91-648">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46e91-648">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="46e91-649">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-649">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="46e91-650">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="46e91-650">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="46e91-651">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-651">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="46e91-652">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="46e91-652">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="46e91-653">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="46e91-653">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="46e91-654">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="46e91-654">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="46e91-655">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="46e91-655">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="46e91-656">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-656">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="46e91-657">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="46e91-657">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="46e91-658">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="46e91-658">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="46e91-659">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-659">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="46e91-660">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46e91-660">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="46e91-661">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46e91-661">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="46e91-662">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-662">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="46e91-663">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="46e91-663">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="46e91-664">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="46e91-664">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="46e91-665">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-665">Supported failover Storage account</span></span>
    - <span data-ttu-id="46e91-666">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="46e91-666">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="46e91-667">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-667">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="46e91-668">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-668">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="46e91-669">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-669">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="46e91-670">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="46e91-670">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="46e91-671">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="46e91-671">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="46e91-672">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="46e91-672">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="46e91-673">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="46e91-673">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="46e91-674">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="46e91-674">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="46e91-675">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="46e91-675">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="46e91-676">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="46e91-676">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="46e91-677">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="46e91-677">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="46e91-678">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="46e91-678">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="46e91-679">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="46e91-679">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="46e91-680">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="46e91-680">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="46e91-681">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="46e91-681">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="46e91-682">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="46e91-682">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="46e91-683">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="46e91-683">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="46e91-684">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="46e91-684">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="46e91-685">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46e91-685">Az.TrafficManager</span></span>
* <span data-ttu-id="46e91-686">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-686">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-687">Az.Websites</span></span>
* <span data-ttu-id="46e91-688">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-688">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="46e91-689">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-689">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="46e91-690">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="46e91-690">Highlights since the last release</span></span>
* <span data-ttu-id="46e91-691">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="46e91-691">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-692">Az.Accounts</span></span>
* <span data-ttu-id="46e91-693">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="46e91-693">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46e91-694">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-694">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-695">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-695">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="46e91-696">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-696">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46e91-697">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46e91-697">Az.Cdn</span></span>
* <span data-ttu-id="46e91-698">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-698">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-699">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-699">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-700">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="46e91-700">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-701">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-701">Az.Compute</span></span>
* <span data-ttu-id="46e91-702">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-702">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="46e91-703">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-703">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-704">Az.IotHub</span></span>
* <span data-ttu-id="46e91-705">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-705">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="46e91-706">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="46e91-706">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="46e91-707">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="46e91-707">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="46e91-708">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-708">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="46e91-709">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-709">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="46e91-710">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="46e91-710">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="46e91-711">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="46e91-711">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="46e91-712">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="46e91-712">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="46e91-713">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-713">New cmdlets are:</span></span>
    - <span data-ttu-id="46e91-714">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-714">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="46e91-715">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-715">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="46e91-716">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-716">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="46e91-717">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46e91-717">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="46e91-718">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-718">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-719">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-719">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-720">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-720">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="46e91-721">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="46e91-721">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="46e91-722">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="46e91-722">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="46e91-723">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-723">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="46e91-724">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="46e91-724">Az.Maintenance</span></span>
* <span data-ttu-id="46e91-725">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="46e91-725">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-726">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-726">Az.Monitor</span></span>
* <span data-ttu-id="46e91-727">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-727">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="46e91-728">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="46e91-728">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="46e91-729">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="46e91-729">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="46e91-730">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="46e91-730">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="46e91-731">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="46e91-731">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="46e91-732">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="46e91-732">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="46e91-733">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="46e91-733">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="46e91-734">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="46e91-734">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-735">Az.Network</span></span>
* <span data-ttu-id="46e91-736">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-736">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="46e91-737">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="46e91-737">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="46e91-738">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="46e91-738">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="46e91-739">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="46e91-739">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="46e91-740">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="46e91-740">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="46e91-741">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-741">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="46e91-742">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="46e91-742">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="46e91-743">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="46e91-743">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="46e91-744">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-744">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="46e91-745">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-745">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="46e91-746">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="46e91-746">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="46e91-747">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-747">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="46e91-748">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-748">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="46e91-749">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-749">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="46e91-750">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-750">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="46e91-751">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-751">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46e91-752">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-752">Az.PolicyInsights</span></span>
* <span data-ttu-id="46e91-753">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-753">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="46e91-754">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-754">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46e91-755">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-755">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-756">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-756">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-757">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-757">Az.Sql</span></span>
* <span data-ttu-id="46e91-758">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-758">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="46e91-759">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-759">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-760">Az.Storage</span></span>
* <span data-ttu-id="46e91-761">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-761">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="46e91-762">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-762">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="46e91-763">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46e91-763">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="46e91-764">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46e91-764">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="46e91-765">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-765">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="46e91-766">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46e91-766">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="46e91-767">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46e91-767">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="46e91-768">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="46e91-768">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="46e91-769">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46e91-769">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="46e91-770">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="46e91-770">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="46e91-771">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46e91-771">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="46e91-772">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="46e91-772">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="46e91-773">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46e91-773">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="46e91-774">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-774">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="46e91-775">Genel</span><span class="sxs-lookup"><span data-stu-id="46e91-775">General</span></span>
* <span data-ttu-id="46e91-776">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-776">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="46e91-777">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="46e91-777">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="46e91-778">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="46e91-778">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="46e91-779">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="46e91-779">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="46e91-780">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="46e91-780">Az.Billing</span></span>
  - <span data-ttu-id="46e91-781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-781">Az.Compute</span></span>
  - <span data-ttu-id="46e91-782">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="46e91-782">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="46e91-783">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46e91-783">Az.EventHub</span></span>
  - <span data-ttu-id="46e91-784">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-784">Az.IotHub</span></span>
  - <span data-ttu-id="46e91-785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-785">Az.KeyVault</span></span>
  - <span data-ttu-id="46e91-786">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-786">Az.Monitor</span></span>
  - <span data-ttu-id="46e91-787">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-787">Az.Network</span></span>
  - <span data-ttu-id="46e91-788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-788">Az.Resources</span></span>
  - <span data-ttu-id="46e91-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-789">Az.Storage</span></span>
  - <span data-ttu-id="46e91-790">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-790">Az.Websites</span></span>
* <span data-ttu-id="46e91-791">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-791">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="46e91-792">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="46e91-792">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="46e91-793">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="46e91-793">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="46e91-794">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-794">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-795">Az.Accounts</span></span>
* <span data-ttu-id="46e91-796">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="46e91-796">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-797">Az.Compute</span></span>
* <span data-ttu-id="46e91-798">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-798">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="46e91-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="46e91-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="46e91-800">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-800">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="46e91-801">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-801">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="46e91-802">[#11354]</span><span class="sxs-lookup"><span data-stu-id="46e91-802">[#11354]</span></span>
* <span data-ttu-id="46e91-803">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-803">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="46e91-804">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="46e91-804">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="46e91-805">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="46e91-805">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="46e91-806">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="46e91-806">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="46e91-807">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="46e91-807">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="46e91-808">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-808">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="46e91-809">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-809">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="46e91-810">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-810">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="46e91-811">[#11257]</span><span class="sxs-lookup"><span data-stu-id="46e91-811">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-812">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-813">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-813">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="46e91-814">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-814">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-815">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-815">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-816">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-816">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="46e91-817">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-817">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-818">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-818">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-819">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-819">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-820">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-820">Az.IotHub</span></span>
* <span data-ttu-id="46e91-821">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-821">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="46e91-822">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-822">New Cmdlets are:</span></span>
    - <span data-ttu-id="46e91-823">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="46e91-823">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="46e91-824">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="46e91-824">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-825">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-825">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-826">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-826">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-827">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-827">Az.Monitor</span></span>
* <span data-ttu-id="46e91-828">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-828">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-829">Az.Network</span></span>
* <span data-ttu-id="46e91-830">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-830">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="46e91-831">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="46e91-831">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="46e91-832">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="46e91-832">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="46e91-833">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="46e91-833">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="46e91-834">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="46e91-834">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="46e91-835">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-835">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46e91-836">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-836">Az.PolicyInsights</span></span>
* <span data-ttu-id="46e91-837">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-837">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-838">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-838">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-839">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-839">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="46e91-840">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-840">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="46e91-841">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-841">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="46e91-842">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-842">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="46e91-843">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-843">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="46e91-844">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-844">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-845">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-845">Az.Resources</span></span>
* <span data-ttu-id="46e91-846">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="46e91-846">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="46e91-847">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-847">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="46e91-848">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-848">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="46e91-849">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-849">Added example.</span></span>
* <span data-ttu-id="46e91-850">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="46e91-850">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="46e91-851">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="46e91-851">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-852">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-852">Az.Sql</span></span>
* <span data-ttu-id="46e91-853">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-853">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="46e91-854">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-854">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="46e91-855">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-855">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="46e91-856">Az.Support</span><span class="sxs-lookup"><span data-stu-id="46e91-856">Az.Support</span></span>
* <span data-ttu-id="46e91-857">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-857">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-858">Az.Websites</span></span>
* <span data-ttu-id="46e91-859">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-859">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="46e91-860">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="46e91-860">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="46e91-861">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="46e91-861">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="46e91-862">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="46e91-862">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="46e91-863">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="46e91-863">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="46e91-864">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-864">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-865">Az.Accounts</span></span>
* <span data-ttu-id="46e91-866">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="46e91-866">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="46e91-867">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="46e91-867">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="46e91-868">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-868">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46e91-869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-869">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-870">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="46e91-870">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="46e91-871">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="46e91-871">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="46e91-872">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-872">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="46e91-873">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="46e91-873">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-874">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-875">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-875">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-876">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-876">Az.IotHub</span></span>
* <span data-ttu-id="46e91-877">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-877">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="46e91-878">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-878">New Cmdlets are:</span></span>
    - <span data-ttu-id="46e91-879">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46e91-879">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46e91-880">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46e91-880">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46e91-881">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46e91-881">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46e91-882">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46e91-882">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="46e91-883">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-883">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="46e91-884">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-884">New Cmdlets are:</span></span>
    - <span data-ttu-id="46e91-885">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="46e91-885">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="46e91-886">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="46e91-886">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="46e91-887">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="46e91-887">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="46e91-888">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="46e91-888">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="46e91-889">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-889">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="46e91-890">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-890">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="46e91-891">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-891">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="46e91-892">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-892">New Cmdlets are:</span></span>
    - <span data-ttu-id="46e91-893">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="46e91-893">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="46e91-894">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="46e91-894">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="46e91-895">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-895">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-896">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-896">Az.Monitor</span></span>
* <span data-ttu-id="46e91-897">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="46e91-897">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-898">Az.Network</span></span>
* <span data-ttu-id="46e91-899">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-899">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="46e91-900">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-900">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="46e91-901">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-901">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="46e91-902">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-902">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-903">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-903">Az.Resources</span></span>
* <span data-ttu-id="46e91-904">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-904">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="46e91-905">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="46e91-905">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="46e91-906">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="46e91-906">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="46e91-907">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="46e91-907">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="46e91-908">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-908">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="46e91-909">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-909">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="46e91-910">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-910">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="46e91-911">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="46e91-911">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="46e91-912">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46e91-912">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="46e91-913">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46e91-913">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="46e91-914">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46e91-914">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="46e91-915">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-915">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="46e91-916">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46e91-916">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="46e91-917">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-917">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-918">Az.Sql</span></span>
* <span data-ttu-id="46e91-919">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-919">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="46e91-920">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-920">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="46e91-921">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="46e91-921">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="46e91-922">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="46e91-922">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="46e91-923">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="46e91-923">Remove an LTR backup</span></span>
    - <span data-ttu-id="46e91-924">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="46e91-924">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="46e91-925">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-925">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="46e91-926">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-926">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="46e91-927">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-927">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-928">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-928">Az.Storage</span></span>
* <span data-ttu-id="46e91-929">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-929">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="46e91-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="46e91-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="46e91-931">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-931">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="46e91-932">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="46e91-932">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="46e91-933">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="46e91-933">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-934">Az.Websites</span></span>
* <span data-ttu-id="46e91-935">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-935">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="46e91-936">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="46e91-936">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="46e91-937">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-937">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="46e91-938">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="46e91-938">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="46e91-939">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-939">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="46e91-940">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-940">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46e91-941">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="46e91-941">Highlights since the last major release</span></span>
* <span data-ttu-id="46e91-942">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-942">Updated client side telemetry.</span></span>
* <span data-ttu-id="46e91-943">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-943">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="46e91-944">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-944">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-945">Az.Accounts</span></span>
* <span data-ttu-id="46e91-946">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-946">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-947">Az.Automation</span></span>
* <span data-ttu-id="46e91-948">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-948">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-949">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-949">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-950">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-950">Updated SDK to 7.0</span></span>
* <span data-ttu-id="46e91-951">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-951">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-952">Az.Compute</span></span>
* <span data-ttu-id="46e91-953">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="46e91-953">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46e91-954">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-954">Az.FrontDoor</span></span>
* <span data-ttu-id="46e91-955">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-955">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-956">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-956">Az.IotHub</span></span>
* <span data-ttu-id="46e91-957">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-957">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="46e91-958">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-958">New Cmdlets are:</span></span>
    - <span data-ttu-id="46e91-959">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46e91-959">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46e91-960">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46e91-960">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46e91-961">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46e91-961">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46e91-962">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46e91-962">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-963">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-963">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-964">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-964">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-965">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-965">Az.Monitor</span></span>
* <span data-ttu-id="46e91-966">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-966">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="46e91-967">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-967">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="46e91-968">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-968">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-969">Az.Network</span></span>
* <span data-ttu-id="46e91-970">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-970">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="46e91-971">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-971">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="46e91-972">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-972">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="46e91-973">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="46e91-973">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="46e91-974">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="46e91-974">No new cmdlets are added.</span></span> <span data-ttu-id="46e91-975">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="46e91-975">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-977">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-977">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-978">Az.Resources</span></span>
* <span data-ttu-id="46e91-979">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="46e91-979">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="46e91-980">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46e91-980">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="46e91-981">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="46e91-981">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="46e91-982">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="46e91-982">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="46e91-983">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-983">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="46e91-984">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-984">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="46e91-985">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-985">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="46e91-986">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-986">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-987">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-987">Az.Sql</span></span>
* <span data-ttu-id="46e91-988">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-988">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="46e91-989">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-989">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="46e91-990">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="46e91-990">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="46e91-991">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46e91-991">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="46e91-992">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-992">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46e91-993">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46e91-993">Az.StorageSync</span></span>
* <span data-ttu-id="46e91-994">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-994">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="46e91-995">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-995">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46e91-996">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="46e91-996">Highlights since the last major release</span></span>
* <span data-ttu-id="46e91-997">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="46e91-997">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="46e91-998">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-998">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-999">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-999">Az.Accounts</span></span>
* <span data-ttu-id="46e91-1000">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="46e91-1000">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="46e91-1001">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1001">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46e91-1002">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-1002">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-1003">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="46e91-1003">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="46e91-1004">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="46e91-1004">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="46e91-1005">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1005">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="46e91-1006">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1006">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1007">Az.Compute</span></span>
* <span data-ttu-id="46e91-1008">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="46e91-1008">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="46e91-1009">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1009">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="46e91-1010">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1010">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="46e91-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="46e91-1012">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1012">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1013">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1014">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1014">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="46e91-1015">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="46e91-1015">Az.DeploymentManager</span></span>
* <span data-ttu-id="46e91-1016">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="46e91-1016">Adds LIST operations for resources</span></span>
* <span data-ttu-id="46e91-1017">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="46e91-1017">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-1018">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-1018">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-1019">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1019">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-1020">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-1020">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-1021">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1021">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1022">Az.Network</span></span>
* <span data-ttu-id="46e91-1023">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1023">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="46e91-1024">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="46e91-1024">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="46e91-1025">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1025">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="46e91-1026">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1026">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="46e91-1027">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="46e91-1027">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="46e91-1028">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1028">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="46e91-1029">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1029">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="46e91-1030">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1030">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="46e91-1031">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1031">New cmdlets added:</span></span>
        - <span data-ttu-id="46e91-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="46e91-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="46e91-1033">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1033">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="46e91-1034">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="46e91-1034">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="46e91-1035">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1035">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46e91-1036">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-1036">Az.PolicyInsights</span></span>
* <span data-ttu-id="46e91-1037">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="46e91-1037">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="46e91-1038">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1038">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="46e91-1039">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1039">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="46e91-1040">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1040">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-1041">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1041">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-1042">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1042">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="46e91-1043">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1043">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1044">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1044">Az.Resources</span></span>
* <span data-ttu-id="46e91-1045">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1045">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="46e91-1046">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1046">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1047">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1047">Az.Sql</span></span>
<span data-ttu-id="46e91-1048">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1048">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1049">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1049">Az.Storage</span></span>
* <span data-ttu-id="46e91-1050">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="46e91-1050">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="46e91-1051">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-1051">New-AzStorageAccount</span></span>
* <span data-ttu-id="46e91-1052">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="46e91-1052">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="46e91-1053">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1053">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-1054">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-1054">Az.Websites</span></span>
* <span data-ttu-id="46e91-1055">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="46e91-1055">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="46e91-1056">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1056">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="46e91-1057">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="46e91-1057">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-1058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-1058">Az.Accounts</span></span>
* <span data-ttu-id="46e91-1059">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1059">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46e91-1060">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46e91-1060">Az.Cdn</span></span>
* <span data-ttu-id="46e91-1061">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="46e91-1061">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1062">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1062">Az.Compute</span></span>
* <span data-ttu-id="46e91-1063">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1063">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="46e91-1064">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46e91-1064">Az.ContainerInstance</span></span>
* <span data-ttu-id="46e91-1065">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1065">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="46e91-1066">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="46e91-1066">Az.DataBoxEdge</span></span>
* <span data-ttu-id="46e91-1067">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1067">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46e91-1068">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="46e91-1068">Get the Edge Storage Container</span></span>
* <span data-ttu-id="46e91-1069">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1069">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46e91-1070">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="46e91-1070">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="46e91-1071">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1071">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46e91-1072">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="46e91-1072">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="46e91-1073">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1073">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46e91-1074">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="46e91-1074">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="46e91-1075">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1075">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="46e91-1076">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="46e91-1076">Get the Edge Storage Account</span></span>
* <span data-ttu-id="46e91-1077">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1077">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="46e91-1078">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="46e91-1078">Create new Edge Storage Account</span></span>
* <span data-ttu-id="46e91-1079">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1079">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="46e91-1080">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="46e91-1080">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="46e91-1081">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="46e91-1081">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="46e91-1082">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="46e91-1082">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="46e91-1083">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1083">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="46e91-1084">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="46e91-1084">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1085">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1085">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1086">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1086">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="46e91-1087">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1087">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="46e91-1088">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1088">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="46e91-1089">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="46e91-1089">Az.DevTestLabs</span></span>
* <span data-ttu-id="46e91-1090">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1090">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46e91-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1091">Az.EventHub</span></span>
* <span data-ttu-id="46e91-1092">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1092">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-1093">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-1094">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1094">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="46e91-1095">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46e91-1095">Az.MachineLearning</span></span>
* <span data-ttu-id="46e91-1096">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1096">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="46e91-1097">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46e91-1097">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="46e91-1098">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="46e91-1098">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="46e91-1099">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46e91-1099">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="46e91-1100">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46e91-1100">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="46e91-1101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46e91-1101">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="46e91-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="46e91-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="46e91-1103">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="46e91-1103">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1104">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1104">Az.Network</span></span>
* <span data-ttu-id="46e91-1105">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1105">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-1106">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1106">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-1107">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1107">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="46e91-1108">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1108">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="46e91-1109">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1109">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="46e91-1110">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1110">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1111">Az.Resources</span></span>
* <span data-ttu-id="46e91-1112">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1112">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1113">Az.Sql</span></span>
* <span data-ttu-id="46e91-1114">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1114">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="46e91-1115">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1115">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="46e91-1116">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46e91-1116">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="46e91-1117">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1117">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1118">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1118">Az.Storage</span></span>
* <span data-ttu-id="46e91-1119">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1119">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="46e91-1120">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="46e91-1120">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="46e91-1121">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="46e91-1121">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="46e91-1122">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-1122">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="46e91-1123">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1123">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="46e91-1124">Genel</span><span class="sxs-lookup"><span data-stu-id="46e91-1124">General</span></span>
* <span data-ttu-id="46e91-1125">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1125">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-1126">Az.Accounts</span></span>
* <span data-ttu-id="46e91-1127">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="46e91-1127">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="46e91-1128">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="46e91-1128">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46e91-1129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46e91-1129">Az.Batch</span></span>
* <span data-ttu-id="46e91-1130">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1130">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1131">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1132">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1132">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46e91-1133">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-1133">Az.FrontDoor</span></span>
* <span data-ttu-id="46e91-1134">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1134">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="46e91-1135">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1135">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="46e91-1136">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="46e91-1136">Az.HealthcareApis</span></span>
* <span data-ttu-id="46e91-1137">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="46e91-1137">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-1138">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-1138">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-1139">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1139">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="46e91-1140">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="46e91-1140">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="46e91-1141">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1141">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-1142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-1142">Az.Monitor</span></span>
* <span data-ttu-id="46e91-1143">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1143">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="46e91-1144">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="46e91-1144">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="46e91-1145">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="46e91-1145">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1146">Az.Network</span></span>
* <span data-ttu-id="46e91-1147">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1147">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1148">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1148">Az.Resources</span></span>
* <span data-ttu-id="46e91-1149">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1149">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="46e91-1150">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1150">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1151">Az.Sql</span></span>
* <span data-ttu-id="46e91-1152">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1152">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1153">Az.Storage</span></span>
* <span data-ttu-id="46e91-1154">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-1154">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="46e91-1155">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="46e91-1155">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="46e91-1156">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="46e91-1156">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="46e91-1157">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-1157">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="46e91-1158">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="46e91-1158">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="46e91-1159">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1159">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="46e91-1160">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1160">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="46e91-1161">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46e91-1161">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="46e91-1162">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46e91-1162">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="46e91-1163">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1163">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="46e91-1164">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="46e91-1164">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="46e91-1165">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1165">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="46e91-1166">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="46e91-1166">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="46e91-1167">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1167">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46e91-1168">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="46e91-1168">Highlights since the last major release</span></span>
* <span data-ttu-id="46e91-1169">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="46e91-1169">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="46e91-1170">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="46e91-1170">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1171">Az.Compute</span></span>
* <span data-ttu-id="46e91-1172">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="46e91-1172">VM Reapply feature</span></span>
    - <span data-ttu-id="46e91-1173">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="46e91-1173">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="46e91-1174">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="46e91-1174">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="46e91-1175">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46e91-1175">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="46e91-1176">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-1176">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="46e91-1177">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1177">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="46e91-1178">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1178">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="46e91-1179">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1179">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="46e91-1180">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1180">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="46e91-1181">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1181">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="46e91-1182">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1182">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="46e91-1183">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="46e91-1183">Az.DataBoxEdge</span></span>
* <span data-ttu-id="46e91-1184">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1184">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="46e91-1185">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="46e91-1185">Get the Order</span></span>
* <span data-ttu-id="46e91-1186">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1186">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="46e91-1187">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="46e91-1187">Create new Order</span></span>
* <span data-ttu-id="46e91-1188">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1188">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="46e91-1189">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="46e91-1189">Remove the Order</span></span>
* <span data-ttu-id="46e91-1190">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="46e91-1190">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="46e91-1191">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="46e91-1191">Now creates Local Share</span></span>
* <span data-ttu-id="46e91-1192">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1192">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="46e91-1193">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="46e91-1193">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="46e91-1194">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1194">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="46e91-1195">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="46e91-1195">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="46e91-1196">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1196">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="46e91-1197">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="46e91-1197">Gets the information about Triggers</span></span>
* <span data-ttu-id="46e91-1198">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1198">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="46e91-1199">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="46e91-1199">Create new Triggers</span></span>
* <span data-ttu-id="46e91-1200">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1200">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="46e91-1201">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="46e91-1201">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1202">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1202">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1203">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1203">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="46e91-1204">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1204">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-1205">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-1205">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-1206">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1206">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46e91-1207">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1207">Az.EventHub</span></span>
* <span data-ttu-id="46e91-1208">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1208">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46e91-1209">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-1209">Az.FrontDoor</span></span>
* <span data-ttu-id="46e91-1210">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1210">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="46e91-1211">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1211">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="46e91-1212">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1212">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="46e91-1213">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="46e91-1213">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1214">Az.Network</span></span>
* <span data-ttu-id="46e91-1215">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1215">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="46e91-1216">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="46e91-1216">Az.PrivateDns</span></span>
* <span data-ttu-id="46e91-1217">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1217">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-1218">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1218">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-1219">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1219">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="46e91-1220">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1220">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="46e91-1221">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1221">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46e91-1222">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46e91-1222">Az.RedisCache</span></span>
* <span data-ttu-id="46e91-1223">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1223">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="46e91-1224">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1224">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="46e91-1225">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1225">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1226">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1226">Az.Resources</span></span>
- <span data-ttu-id="46e91-1227">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1227">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="46e91-1228">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1228">Updated create policy definition help example</span></span>
- <span data-ttu-id="46e91-1229">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1229">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="46e91-1230">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1230">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="46e91-1231">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1231">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1232">Az.Sql</span></span>
* <span data-ttu-id="46e91-1233">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1233">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="46e91-1234">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1234">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="46e91-1235">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1235">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="46e91-1236">Genel</span><span class="sxs-lookup"><span data-stu-id="46e91-1236">General</span></span>
* <span data-ttu-id="46e91-1237">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="46e91-1237">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-1238">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-1238">Az.Accounts</span></span>
* <span data-ttu-id="46e91-1239">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="46e91-1239">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="46e91-1240">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="46e91-1240">Az.Advisor</span></span>
* <span data-ttu-id="46e91-1241">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1241">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46e91-1242">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46e91-1242">Az.Batch</span></span>
* <span data-ttu-id="46e91-1243">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1243">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="46e91-1244">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="46e91-1244">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="46e91-1245">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1245">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="46e91-1246">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1246">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="46e91-1247">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="46e91-1247">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="46e91-1248">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-1248">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="46e91-1249">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="46e91-1249">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="46e91-1250">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1250">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="46e91-1251">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1251">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="46e91-1252">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1252">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="46e91-1253">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-1253">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="46e91-1254">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="46e91-1254">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="46e91-1255">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1255">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="46e91-1256">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="46e91-1256">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="46e91-1257">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1257">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="46e91-1258">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1258">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="46e91-1259">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1259">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="46e91-1260">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1260">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="46e91-1261">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1261">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="46e91-1262">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1262">This operation is no longer supported.</span></span>
* <span data-ttu-id="46e91-1263">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1263">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="46e91-1264">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1264">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="46e91-1265">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1265">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="46e91-1266">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1266">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="46e91-1267">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1267">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="46e91-1268">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1268">New non-verified images are also now returned.</span></span> <span data-ttu-id="46e91-1269">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1269">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="46e91-1270">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1270">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="46e91-1271">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1271">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="46e91-1272">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1272">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="46e91-1273">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1273">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="46e91-1274">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1274">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="46e91-1275">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1275">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="46e91-1276">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1276">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="46e91-1277">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="46e91-1277">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="46e91-1278">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="46e91-1278">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46e91-1279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46e91-1279">Az.Cdn</span></span>
* <span data-ttu-id="46e91-1280">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1280">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="46e91-1281">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1281">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1282">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1282">Az.Compute</span></span>
* <span data-ttu-id="46e91-1283">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="46e91-1283">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="46e91-1284">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="46e91-1284">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="46e91-1285">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="46e91-1285">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="46e91-1286">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1286">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="46e91-1287">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1287">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="46e91-1288">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="46e91-1288">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="46e91-1289">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1289">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="46e91-1290">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="46e91-1290">Breaking changes</span></span>
    - <span data-ttu-id="46e91-1291">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="46e91-1291">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="46e91-1292">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="46e91-1292">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1293">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1294">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1294">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-1295">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-1295">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-1296">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="46e91-1296">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="46e91-1297">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="46e91-1297">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="46e91-1298">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="46e91-1298">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="46e91-1299">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="46e91-1299">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="46e91-1300">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="46e91-1300">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="46e91-1301">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="46e91-1301">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46e91-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="46e91-1303">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1303">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-1304">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-1304">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-1305">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1305">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="46e91-1306">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1306">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="46e91-1307">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1307">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="46e91-1308">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="46e91-1308">Removed five cmdlets:</span></span>
    - <span data-ttu-id="46e91-1309">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="46e91-1309">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="46e91-1310">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="46e91-1310">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="46e91-1311">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="46e91-1311">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="46e91-1312">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46e91-1312">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="46e91-1313">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46e91-1313">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="46e91-1314">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1314">Added three cmdlets:</span></span>
    - <span data-ttu-id="46e91-1315">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="46e91-1315">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="46e91-1316">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="46e91-1316">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="46e91-1317">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="46e91-1317">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="46e91-1318">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1318">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="46e91-1319">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1319">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="46e91-1320">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1320">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="46e91-1321">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1321">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="46e91-1322">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1322">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="46e91-1323">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1323">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="46e91-1324">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1324">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="46e91-1325">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1325">Added some scenario test cases.</span></span>
* <span data-ttu-id="46e91-1326">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="46e91-1326">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1327">Az.IotHub</span></span>
* <span data-ttu-id="46e91-1328">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="46e91-1328">Breaking changes:</span></span>
    - <span data-ttu-id="46e91-1329">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1329">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46e91-1330">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1330">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="46e91-1331">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1331">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46e91-1332">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1332">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="46e91-1333">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1333">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="46e91-1334">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1334">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="46e91-1335">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1335">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="46e91-1336">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1336">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="46e91-1337">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1337">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46e91-1338">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1338">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="46e91-1339">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1339">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46e91-1340">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1340">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-1341">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1341">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-1342">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1342">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="46e91-1343">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1343">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="46e91-1344">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1344">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="46e91-1345">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1345">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="46e91-1346">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1346">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="46e91-1347">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1347">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="46e91-1348">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1348">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="46e91-1349">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1349">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="46e91-1350">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1350">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1351">Az.Resources</span></span>
* <span data-ttu-id="46e91-1352">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1352">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1353">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1353">Az.Network</span></span>
* <span data-ttu-id="46e91-1354">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1354">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="46e91-1355">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1355">Updated cmdlet:</span></span>
        - <span data-ttu-id="46e91-1356">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1356">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46e91-1357">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1357">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46e91-1358">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1358">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46e91-1359">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1359">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46e91-1360">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1360">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="46e91-1361">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1361">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="46e91-1362">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="46e91-1362">New cmdlet:</span></span>
        - <span data-ttu-id="46e91-1363">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="46e91-1363">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="46e91-1364">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1364">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="46e91-1365">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1365">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="46e91-1366">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1366">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="46e91-1367">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1367">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="46e91-1368">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1368">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="46e91-1369">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1369">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="46e91-1370">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1370">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="46e91-1371">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1371">New cmdlets added:</span></span>
        - <span data-ttu-id="46e91-1372">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="46e91-1372">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="46e91-1373">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="46e91-1373">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="46e91-1374">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="46e91-1374">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="46e91-1375">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="46e91-1375">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="46e91-1376">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1376">Set-AzVirtualHub</span></span>
* <span data-ttu-id="46e91-1377">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1377">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="46e91-1378">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1378">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46e91-1379">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1379">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="46e91-1380">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1380">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="46e91-1381">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1381">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="46e91-1382">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1382">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="46e91-1383">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1383">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="46e91-1384">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1384">New cmdlets added:</span></span>
        - <span data-ttu-id="46e91-1385">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1385">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="46e91-1386">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46e91-1387">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1387">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46e91-1388">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1388">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46e91-1389">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1389">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46e91-1390">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1390">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46e91-1391">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1391">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="46e91-1392">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1392">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="46e91-1393">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1393">New cmdlets added:</span></span>
        - <span data-ttu-id="46e91-1394">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="46e91-1394">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="46e91-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="46e91-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="46e91-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="46e91-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="46e91-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="46e91-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="46e91-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="46e91-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="46e91-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="46e91-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="46e91-1400">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1400">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46e91-1401">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1401">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="46e91-1402">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1402">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="46e91-1403">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1403">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="46e91-1404">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1404">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="46e91-1405">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1405">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46e91-1406">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1406">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="46e91-1407">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1407">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="46e91-1408">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1408">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="46e91-1409">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="46e91-1409">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="46e91-1410">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1410">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="46e91-1411">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1411">New cmdlets added:</span></span>
        - <span data-ttu-id="46e91-1412">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46e91-1412">New-AzIpGroup</span></span>
        - <span data-ttu-id="46e91-1413">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46e91-1413">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="46e91-1414">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46e91-1414">Get-AzIpGroup</span></span>
        - <span data-ttu-id="46e91-1415">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46e91-1415">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46e91-1416">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-1416">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-1417">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1417">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1418">Az.Sql</span></span>
* <span data-ttu-id="46e91-1419">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1419">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="46e91-1420">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1420">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="46e91-1421">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="46e91-1421">Removed deprecated aliases:</span></span>
* <span data-ttu-id="46e91-1422">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="46e91-1422">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="46e91-1423">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="46e91-1423">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="46e91-1424">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1424">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="46e91-1425">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1425">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="46e91-1426">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1426">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="46e91-1427">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1427">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1428">Az.Storage</span></span>
* <span data-ttu-id="46e91-1429">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-1429">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="46e91-1430">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-1430">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="46e91-1431">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-1431">Set-AzStorageAccount</span></span>
* <span data-ttu-id="46e91-1432">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="46e91-1432">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="46e91-1433">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46e91-1433">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="46e91-1434">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46e91-1434">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="46e91-1435">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1435">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="46e91-1436">Genel</span><span class="sxs-lookup"><span data-stu-id="46e91-1436">General</span></span>
* <span data-ttu-id="46e91-1437">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="46e91-1437">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-1438">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-1438">Az.Accounts</span></span>
* <span data-ttu-id="46e91-1439">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1439">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46e91-1440">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-1440">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-1441">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1441">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="46e91-1442">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-1443">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-1443">Az.Automation</span></span>
* <span data-ttu-id="46e91-1444">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1444">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46e91-1445">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46e91-1445">Az.Batch</span></span>
* <span data-ttu-id="46e91-1446">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="46e91-1446">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1447">Az.Compute</span></span>
* <span data-ttu-id="46e91-1448">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1448">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="46e91-1449">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1449">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="46e91-1450">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1450">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="46e91-1451">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1451">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1452">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1452">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1453">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="46e91-1453">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="46e91-1454">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="46e91-1454">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="46e91-1455">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1455">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-1456">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-1456">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-1457">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1457">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="46e91-1458">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="46e91-1458">Az.HealthcareApis</span></span>
* <span data-ttu-id="46e91-1459">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1459">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="46e91-1460">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1460">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="46e91-1461">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1461">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="46e91-1462">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1462">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-1463">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1463">Az.IotHub</span></span>
* <span data-ttu-id="46e91-1464">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="46e91-1464">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="46e91-1465">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="46e91-1465">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-1466">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-1466">Az.Monitor</span></span>
* <span data-ttu-id="46e91-1467">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1467">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="46e91-1468">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="46e91-1468">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="46e91-1469">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="46e91-1469">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="46e91-1470">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1470">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1471">Az.Network</span></span>
* <span data-ttu-id="46e91-1472">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1472">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="46e91-1473">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1473">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="46e91-1474">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1474">New cmdlets added:</span></span>
        - <span data-ttu-id="46e91-1475">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="46e91-1475">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="46e91-1476">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1476">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="46e91-1477">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1477">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="46e91-1478">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1478">Updated cmdlets:</span></span>
        - <span data-ttu-id="46e91-1479">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1479">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46e91-1480">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1480">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46e91-1481">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1481">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="46e91-1482">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1482">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="46e91-1483">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="46e91-1483">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="46e91-1484">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="46e91-1484">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="46e91-1485">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="46e91-1485">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46e91-1486">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46e91-1486">Az.RedisCache</span></span>
* <span data-ttu-id="46e91-1487">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1487">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1488">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1488">Az.Sql</span></span>
* <span data-ttu-id="46e91-1489">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1489">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1490">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1490">Az.Storage</span></span>
* <span data-ttu-id="46e91-1491">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1491">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="46e91-1492">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="46e91-1492">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="46e91-1493">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46e91-1493">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="46e91-1494">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="46e91-1494">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="46e91-1495">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-1495">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46e91-1496">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46e91-1496">Az.StorageSync</span></span>
* <span data-ttu-id="46e91-1497">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1497">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-1498">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-1498">Az.Websites</span></span>
* <span data-ttu-id="46e91-1499">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="46e91-1499">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="46e91-1500">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1500">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="46e91-1501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-1501">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-1502">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1502">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="46e91-1503">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1503">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="46e91-1504">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="46e91-1504">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-1505">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-1505">Az.Automation</span></span>
* <span data-ttu-id="46e91-1506">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1506">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="46e91-1507">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1507">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="46e91-1508">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1508">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1509">Az.Compute</span></span>
* <span data-ttu-id="46e91-1510">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1510">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="46e91-1511">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1511">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="46e91-1512">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1512">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="46e91-1513">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1513">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="46e91-1514">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1514">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="46e91-1515">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1515">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="46e91-1516">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1516">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="46e91-1517">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1517">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="46e91-1518">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1518">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1519">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1520">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="46e91-1520">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="46e91-1521">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1521">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-1522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-1522">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-1523">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="46e91-1523">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-1524">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1524">Az.IotHub</span></span>
* <span data-ttu-id="46e91-1525">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1525">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="46e91-1526">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1526">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="46e91-1527">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46e91-1527">New cmdlets are:</span></span>
    - <span data-ttu-id="46e91-1528">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46e91-1528">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="46e91-1529">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46e91-1529">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="46e91-1530">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46e91-1530">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="46e91-1531">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46e91-1531">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-1532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-1532">Az.Monitor</span></span>
* <span data-ttu-id="46e91-1533">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="46e91-1533">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="46e91-1534">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-1534">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="46e91-1535">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="46e91-1535">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="46e91-1536">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="46e91-1536">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="46e91-1537">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1537">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="46e91-1538">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1538">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="46e91-1539">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1539">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="46e91-1540">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="46e91-1540">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="46e91-1541">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1541">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="46e91-1542">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="46e91-1542">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="46e91-1543">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1543">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="46e91-1544">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="46e91-1544">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="46e91-1545">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1545">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="46e91-1546">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="46e91-1546">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="46e91-1547">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="46e91-1547">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="46e91-1548">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="46e91-1548">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="46e91-1549">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="46e91-1549">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="46e91-1550">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="46e91-1550">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="46e91-1551">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1551">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="46e91-1552">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1552">Overall improved help files</span></span>
* <span data-ttu-id="46e91-1553">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1553">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1554">Az.Network</span></span>
* <span data-ttu-id="46e91-1555">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1555">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="46e91-1556">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1556">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="46e91-1557">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1557">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="46e91-1558">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1558">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="46e91-1559">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1559">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="46e91-1560">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1560">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="46e91-1561">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1561">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="46e91-1562">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1562">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="46e91-1563">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1563">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="46e91-1564">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1564">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="46e91-1565">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1565">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="46e91-1566">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-1566">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="46e91-1567">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-1567">New cmdlets</span></span>
        - <span data-ttu-id="46e91-1568">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="46e91-1568">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="46e91-1569">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1569">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="46e91-1570">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1570">Updated cmdlet:</span></span>
        - <span data-ttu-id="46e91-1571">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="46e91-1571">New-VpnSite</span></span>
        - <span data-ttu-id="46e91-1572">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="46e91-1572">Update-VpnSite</span></span>
        - <span data-ttu-id="46e91-1573">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1573">New-VpnConnection</span></span>
        - <span data-ttu-id="46e91-1574">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1574">Update-VpnConnection</span></span>
* <span data-ttu-id="46e91-1575">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1575">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1576">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-1577">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1577">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="46e91-1578">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1578">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1579">Az.Resources</span></span>
* <span data-ttu-id="46e91-1580">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1580">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46e91-1581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-1581">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-1582">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1582">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="46e91-1583">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="46e91-1583">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="46e91-1584">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46e91-1584">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46e91-1585">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="46e91-1585">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="46e91-1586">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46e91-1586">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="46e91-1587">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="46e91-1587">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="46e91-1588">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46e91-1588">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46e91-1589">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46e91-1589">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46e91-1590">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="46e91-1590">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="46e91-1591">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46e91-1591">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="46e91-1592">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="46e91-1592">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="46e91-1593">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46e91-1593">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46e91-1594">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="46e91-1594">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="46e91-1595">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46e91-1595">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="46e91-1596">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="46e91-1596">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="46e91-1597">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1597">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46e91-1598">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46e91-1598">Az.SignalR</span></span>
* <span data-ttu-id="46e91-1599">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1599">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1600">Az.Sql</span></span>
* <span data-ttu-id="46e91-1601">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1601">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="46e91-1602">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1602">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="46e91-1603">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1603">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="46e91-1604">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1604">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="46e91-1605">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1605">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1606">Az.Storage</span></span>
* <span data-ttu-id="46e91-1607">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1607">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="46e91-1608">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1608">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="46e91-1609">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46e91-1609">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="46e91-1610">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46e91-1610">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="46e91-1611">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1611">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="46e91-1612">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46e91-1612">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="46e91-1613">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1613">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="46e91-1614">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46e91-1614">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="46e91-1615">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46e91-1615">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="46e91-1616">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46e91-1616">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="46e91-1617">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46e91-1617">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-1618">Az.Websites</span></span>
* <span data-ttu-id="46e91-1619">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="46e91-1619">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="46e91-1620">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="46e91-1620">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="46e91-1621">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1621">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="46e91-1622">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1622">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="46e91-1623">Genel</span><span class="sxs-lookup"><span data-stu-id="46e91-1623">General</span></span>
* <span data-ttu-id="46e91-1624">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1624">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-1625">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-1625">Az.Accounts</span></span>
* <span data-ttu-id="46e91-1626">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="46e91-1626">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="46e91-1627">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46e91-1627">Az.Aks</span></span>
* <span data-ttu-id="46e91-1628">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1628">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="46e91-1629">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="46e91-1629">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46e91-1630">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-1630">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-1631">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1631">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="46e91-1632">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1632">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="46e91-1633">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1633">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="46e91-1634">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="46e91-1634">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="46e91-1635">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1635">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46e91-1636">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46e91-1636">Az.Batch</span></span>
* <span data-ttu-id="46e91-1637">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1637">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46e91-1638">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46e91-1638">Az.Cdn</span></span>
* <span data-ttu-id="46e91-1639">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1639">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1640">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1640">Az.Compute</span></span>
* <span data-ttu-id="46e91-1641">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1641">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="46e91-1642">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1642">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="46e91-1643">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1643">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="46e91-1644">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1644">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="46e91-1645">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="46e91-1645">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="46e91-1646">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1646">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="46e91-1647">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1647">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="46e91-1648">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1648">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1649">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1649">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1650">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1650">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="46e91-1651">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1651">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="46e91-1652">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1652">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="46e91-1653">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1653">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-1654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-1654">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-1655">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1655">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46e91-1656">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1656">Az.EventHub</span></span>
* <span data-ttu-id="46e91-1657">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="46e91-1657">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="46e91-1658">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="46e91-1658">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="46e91-1659">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1659">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="46e91-1660">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="46e91-1660">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="46e91-1661">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="46e91-1661">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="46e91-1662">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1662">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-1663">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-1663">Az.Monitor</span></span>
* <span data-ttu-id="46e91-1664">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1664">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1665">Az.Network</span></span>
* <span data-ttu-id="46e91-1666">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1666">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="46e91-1667">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1667">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="46e91-1668">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1668">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="46e91-1669">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="46e91-1669">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="46e91-1670">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1670">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="46e91-1671">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1671">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="46e91-1672">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1672">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-1673">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-1673">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-1674">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1674">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="46e91-1675">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1675">Added example</span></span>
    - <span data-ttu-id="46e91-1676">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1676">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="46e91-1677">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1677">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="46e91-1678">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1678">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-1680">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1680">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1681">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1681">Az.Resources</span></span>
* <span data-ttu-id="46e91-1682">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1682">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="46e91-1683">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1683">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="46e91-1684">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="46e91-1684">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="46e91-1685">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1685">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46e91-1686">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46e91-1686">Az.ServiceBus</span></span>
* <span data-ttu-id="46e91-1687">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="46e91-1687">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="46e91-1688">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="46e91-1688">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="46e91-1689">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1689">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46e91-1690">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-1690">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-1691">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1691">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="46e91-1692">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="46e91-1692">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="46e91-1693">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="46e91-1693">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="46e91-1694">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1694">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="46e91-1695">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="46e91-1695">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="46e91-1696">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1696">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1697">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1697">Az.Sql</span></span>
* <span data-ttu-id="46e91-1698">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1698">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1699">Az.Storage</span></span>
* <span data-ttu-id="46e91-1700">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1700">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="46e91-1701">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="46e91-1701">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="46e91-1702">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46e91-1702">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="46e91-1703">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46e91-1703">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="46e91-1704">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-1704">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="46e91-1705">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46e91-1705">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-1706">Az.Websites</span></span>
* <span data-ttu-id="46e91-1707">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1707">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="46e91-1708">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1708">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-1709">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-1709">Az.Accounts</span></span>
* <span data-ttu-id="46e91-1710">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1710">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="46e91-1711">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-1711">Az.ApplicationInsights</span></span>
* <span data-ttu-id="46e91-1712">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1712">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-1713">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-1713">Az.Automation</span></span>
* <span data-ttu-id="46e91-1714">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1714">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-1715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1715">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-1716">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1716">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1717">Az.Compute</span></span>
* <span data-ttu-id="46e91-1718">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1718">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="46e91-1719">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="46e91-1719">Az.ContainerRegistry</span></span>
* <span data-ttu-id="46e91-1720">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1720">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="46e91-1721">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="46e91-1721">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1722">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1722">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1723">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1723">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="46e91-1724">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1724">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46e91-1725">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1725">Az.EventHub</span></span>
* <span data-ttu-id="46e91-1726">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="46e91-1726">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="46e91-1727">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1727">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-1728">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-1728">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-1729">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1729">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46e91-1730">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46e91-1730">Az.LogicApp</span></span>
* <span data-ttu-id="46e91-1731">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="46e91-1731">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="46e91-1732">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1732">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="46e91-1733">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1733">Az.ManagedServices</span></span>
* <span data-ttu-id="46e91-1734">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="46e91-1734">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1735">Az.Network</span></span>
* <span data-ttu-id="46e91-1736">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1736">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="46e91-1737">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-1737">New cmdlets</span></span>
        - <span data-ttu-id="46e91-1738">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46e91-1738">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46e91-1739">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46e91-1739">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46e91-1740">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1740">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46e91-1741">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1741">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46e91-1742">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1742">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46e91-1743">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1743">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46e91-1744">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="46e91-1744">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="46e91-1745">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46e91-1745">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="46e91-1746">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="46e91-1746">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="46e91-1747">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1747">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="46e91-1748">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1748">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="46e91-1749">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1749">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="46e91-1750">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1750">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="46e91-1751">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1751">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="46e91-1752">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1752">Updated cmdlets</span></span>
        - <span data-ttu-id="46e91-1753">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1753">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46e91-1754">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1754">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46e91-1755">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1755">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="46e91-1756">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1756">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="46e91-1757">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1757">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="46e91-1758">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1758">Updated cmdlet:</span></span>
        - <span data-ttu-id="46e91-1759">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1759">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="46e91-1760">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1760">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="46e91-1761">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1761">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="46e91-1762">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1762">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="46e91-1763">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1763">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="46e91-1764">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="46e91-1764">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-1765">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-1765">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-1766">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1766">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="46e91-1767">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1767">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-1768">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1768">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-1769">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1769">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="46e91-1770">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1770">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="46e91-1771">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1771">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="46e91-1772">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1772">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="46e91-1773">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1773">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="46e91-1774">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1774">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="46e91-1775">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1775">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="46e91-1776">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1776">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="46e91-1777">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1777">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="46e91-1778">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1778">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1779">Az.Resources</span></span>
- <span data-ttu-id="46e91-1780">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1780">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="46e91-1781">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1781">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46e91-1782">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46e91-1782">Az.ServiceBus</span></span>
* <span data-ttu-id="46e91-1783">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="46e91-1783">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="46e91-1784">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1784">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1785">Az.Sql</span></span>
* <span data-ttu-id="46e91-1786">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1786">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="46e91-1787">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1787">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="46e91-1788">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1788">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1789">Az.Storage</span></span>
* <span data-ttu-id="46e91-1790">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1790">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46e91-1791">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46e91-1791">Az.StorageSync</span></span>
* <span data-ttu-id="46e91-1792">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1792">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="46e91-1793">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1793">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-1794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-1794">Az.Websites</span></span>
* <span data-ttu-id="46e91-1795">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1795">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="46e91-1796">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1796">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="46e91-1797">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1797">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="46e91-1798">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1798">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-1799">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-1799">Az.Accounts</span></span>
* <span data-ttu-id="46e91-1800">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1800">Add support for profile cmdlets</span></span>
* <span data-ttu-id="46e91-1801">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1801">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="46e91-1802">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1802">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="46e91-1803">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="46e91-1803">Az.Advisor</span></span>
* <span data-ttu-id="46e91-1804">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-1804">GA release of Az.Advisor</span></span>
* <span data-ttu-id="46e91-1805">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="46e91-1805">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46e91-1806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-1806">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-1807">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1807">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="46e91-1808">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="46e91-1808">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="46e91-1809">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1809">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="46e91-1810">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="46e91-1810">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="46e91-1811">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="46e91-1811">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="46e91-1812">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="46e91-1812">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="46e91-1813">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1813">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-1814">Az.Automation</span></span>
* <span data-ttu-id="46e91-1815">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1815">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1816">Az.Compute</span></span>
* <span data-ttu-id="46e91-1817">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1817">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-1818">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-1818">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-1819">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1819">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46e91-1820">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46e91-1820">Az.EventGrid</span></span>
* <span data-ttu-id="46e91-1821">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1821">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-1822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1822">Az.IotHub</span></span>
* <span data-ttu-id="46e91-1823">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1823">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1824">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1824">Az.Network</span></span>
* <span data-ttu-id="46e91-1825">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1825">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="46e91-1826">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1826">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46e91-1827">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-1827">Az.PolicyInsights</span></span>
* <span data-ttu-id="46e91-1828">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1828">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="46e91-1829">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="46e91-1829">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-1830">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-1830">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-1831">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1831">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-1832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1832">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-1833">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="46e91-1833">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1834">Az.Resources</span></span>
    - <span data-ttu-id="46e91-1835">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="46e91-1835">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="46e91-1836">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1836">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="46e91-1837">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1837">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="46e91-1838">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1838">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46e91-1839">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46e91-1839">Az.ServiceBus</span></span>
* <span data-ttu-id="46e91-1840">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1840">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1841">Az.Sql</span></span>
* <span data-ttu-id="46e91-1842">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1842">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="46e91-1843">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-1843">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="46e91-1844">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="46e91-1844">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="46e91-1845">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="46e91-1845">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="46e91-1846">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="46e91-1846">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="46e91-1847">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="46e91-1847">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="46e91-1848">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="46e91-1848">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="46e91-1849">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="46e91-1849">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="46e91-1850">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-1850">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1851">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1851">Az.Storage</span></span>
* <span data-ttu-id="46e91-1852">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1852">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="46e91-1853">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="46e91-1853">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="46e91-1854">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1854">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="46e91-1855">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="46e91-1855">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="46e91-1856">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1856">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="46e91-1857">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-1857">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="46e91-1858">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-1858">Set-AzStorageAccount</span></span>
* <span data-ttu-id="46e91-1859">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1859">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="46e91-1860">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46e91-1860">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="46e91-1861">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46e91-1861">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46e91-1862">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46e91-1862">Az.StorageSync</span></span>
* <span data-ttu-id="46e91-1863">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="46e91-1863">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="46e91-1864">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1864">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-1865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-1865">Az.Accounts</span></span>
* <span data-ttu-id="46e91-1866">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1866">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="46e91-1867">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="46e91-1867">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="46e91-1868">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1868">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="46e91-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="46e91-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="46e91-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="46e91-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1871">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1871">Az.Compute</span></span>
* <span data-ttu-id="46e91-1872">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-1872">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="46e91-1873">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1873">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="46e91-1874">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="46e91-1874">Az.Dns</span></span>
* <span data-ttu-id="46e91-1875">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1875">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46e91-1876">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46e91-1876">Az.EventGrid</span></span>
* <span data-ttu-id="46e91-1877">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1877">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="46e91-1878">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="46e91-1878">New cmdlets:</span></span>
    - <span data-ttu-id="46e91-1879">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="46e91-1879">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="46e91-1880">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46e91-1880">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="46e91-1881">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="46e91-1881">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="46e91-1882">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="46e91-1882">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="46e91-1883">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="46e91-1883">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="46e91-1884">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="46e91-1884">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="46e91-1885">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="46e91-1885">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="46e91-1886">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="46e91-1886">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="46e91-1887">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="46e91-1887">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="46e91-1888">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="46e91-1888">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="46e91-1889">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="46e91-1889">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="46e91-1890">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46e91-1890">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="46e91-1891">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="46e91-1891">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="46e91-1892">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="46e91-1892">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="46e91-1893">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="46e91-1893">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="46e91-1894">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="46e91-1894">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="46e91-1895">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1895">Updated cmdlets:</span></span>
    - <span data-ttu-id="46e91-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="46e91-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="46e91-1897">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-1897">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="46e91-1898">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-1898">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="46e91-1899">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-1899">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="46e91-1900">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1900">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="46e91-1901">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="46e91-1901">Event subscription expiration date,</span></span>
            - <span data-ttu-id="46e91-1902">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="46e91-1902">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="46e91-1903">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-1903">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="46e91-1904">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="46e91-1904">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="46e91-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="46e91-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="46e91-1906">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-1906">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="46e91-1907">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="46e91-1907">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="46e91-1908">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-1908">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="46e91-1909">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-1909">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46e91-1910">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-1910">Az.FrontDoor</span></span>
* <span data-ttu-id="46e91-1911">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="46e91-1911">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="46e91-1912">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="46e91-1912">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="46e91-1913">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="46e91-1913">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="46e91-1914">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="46e91-1914">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1915">Az.Network</span></span>
* <span data-ttu-id="46e91-1916">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="46e91-1916">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="46e91-1917">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-1917">New cmdlets</span></span>
        - <span data-ttu-id="46e91-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="46e91-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="46e91-1919">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="46e91-1919">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="46e91-1920">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-1920">New cmdlets</span></span>
        - <span data-ttu-id="46e91-1921">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="46e91-1921">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="46e91-1922">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="46e91-1922">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="46e91-1923">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-1923">New cmdlets</span></span>
        - <span data-ttu-id="46e91-1924">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46e91-1924">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46e91-1925">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46e91-1925">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46e91-1926">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46e91-1926">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46e91-1927">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-1927">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="46e91-1928">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1928">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="46e91-1929">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="46e91-1929">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="46e91-1930">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-1930">New cmdlets</span></span>
        - <span data-ttu-id="46e91-1931">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46e91-1931">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46e91-1932">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46e91-1932">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46e91-1933">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46e91-1933">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46e91-1934">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="46e91-1934">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="46e91-1935">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="46e91-1935">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="46e91-1936">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1936">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="46e91-1937">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1937">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="46e91-1938">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1938">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="46e91-1939">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1939">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="46e91-1940">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1940">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="46e91-1941">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1941">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="46e91-1942">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1942">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="46e91-1943">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1943">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="46e91-1944">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1944">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="46e91-1945">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1945">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="46e91-1946">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1946">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="46e91-1947">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1947">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="46e91-1948">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1948">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="46e91-1949">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-1949">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="46e91-1950">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1950">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="46e91-1951">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1951">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="46e91-1952">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="46e91-1952">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="46e91-1953">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="46e91-1953">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="46e91-1954">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="46e91-1954">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="46e91-1955">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1955">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="46e91-1956">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1956">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="46e91-1957">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1957">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-1958">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-1958">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-1959">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1959">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-1960">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-1960">Az.Resources</span></span>
* <span data-ttu-id="46e91-1961">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="46e91-1961">Support for additional Template Export options</span></span>
    - <span data-ttu-id="46e91-1962">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1962">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="46e91-1963">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1963">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="46e91-1964">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1964">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46e91-1965">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-1965">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-1966">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1966">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-1967">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-1967">Az.Sql</span></span>
* <span data-ttu-id="46e91-1968">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1968">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="46e91-1969">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1969">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="46e91-1970">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-1970">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="46e91-1971">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46e91-1971">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="46e91-1972">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46e91-1972">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="46e91-1973">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46e91-1973">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="46e91-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="46e91-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="46e91-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="46e91-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-1976">Az.Storage</span></span>
* <span data-ttu-id="46e91-1977">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="46e91-1977">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="46e91-1978">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-1978">New-AzStorageAccount</span></span>
* <span data-ttu-id="46e91-1979">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1979">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="46e91-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="46e91-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-1981">Az.Websites</span></span>
* <span data-ttu-id="46e91-1982">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="46e91-1982">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="46e91-1983">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="46e91-1983">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="46e91-1984">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-1984">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="46e91-1985">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46e91-1985">Az.Cdn</span></span>
* <span data-ttu-id="46e91-1986">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1986">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-1987">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-1987">Az.Compute</span></span>
* <span data-ttu-id="46e91-1988">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-1988">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="46e91-1989">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="46e91-1989">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46e91-1990">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46e91-1990">Az.EventHub</span></span>
* <span data-ttu-id="46e91-1991">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="46e91-1991">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="46e91-1992">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="46e91-1992">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-1993">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-1993">Az.Network</span></span>
* <span data-ttu-id="46e91-1994">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1994">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="46e91-1995">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-1995">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46e91-1996">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-1996">Az.PolicyInsights</span></span>
* <span data-ttu-id="46e91-1997">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1997">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-1998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-1998">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-1999">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-1999">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46e91-2000">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46e91-2000">Az.ServiceBus</span></span>
* <span data-ttu-id="46e91-2001">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="46e91-2001">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46e91-2002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-2002">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-2003">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2003">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="46e91-2004">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2004">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2005">Az.Sql</span></span>
* <span data-ttu-id="46e91-2006">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2006">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="46e91-2007">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-2007">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="46e91-2008">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-2008">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="46e91-2009">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2009">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-2010">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2010">Az.Websites</span></span>
* <span data-ttu-id="46e91-2011">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2011">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="46e91-2012">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2012">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="46e91-2013">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-2013">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-2014">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-2014">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="46e91-2015">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="46e91-2015">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="46e91-2016">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="46e91-2016">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="46e91-2017">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="46e91-2017">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="46e91-2018">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46e91-2018">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="46e91-2019">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="46e91-2019">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="46e91-2020">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="46e91-2020">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="46e91-2021">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="46e91-2021">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="46e91-2022">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-2022">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="46e91-2023">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="46e91-2023">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="46e91-2024">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="46e91-2024">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="46e91-2025">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="46e91-2025">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="46e91-2026">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="46e91-2026">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="46e91-2027">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-2027">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="46e91-2028">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="46e91-2028">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="46e91-2029">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="46e91-2029">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="46e91-2030">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="46e91-2030">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="46e91-2031">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="46e91-2031">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="46e91-2032">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="46e91-2032">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="46e91-2033">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="46e91-2033">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="46e91-2034">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-2034">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="46e91-2035">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="46e91-2035">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="46e91-2036">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="46e91-2036">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="46e91-2037">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2037">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="46e91-2038">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2038">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="46e91-2039">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2039">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="46e91-2040">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="46e91-2040">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="46e91-2041">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-2041">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="46e91-2042">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2042">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="46e91-2043">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2043">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="46e91-2044">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2044">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="46e91-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="46e91-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="46e91-2046">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2046">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="46e91-2047">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2047">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="46e91-2048">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="46e91-2048">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="46e91-2049">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="46e91-2049">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="46e91-2050">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="46e91-2050">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="46e91-2051">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2051">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="46e91-2052">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2052">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="46e91-2053">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2053">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="46e91-2054">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="46e91-2054">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="46e91-2055">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="46e91-2055">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="46e91-2056">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="46e91-2056">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="46e91-2057">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="46e91-2057">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="46e91-2058">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2058">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="46e91-2059">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="46e91-2059">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="46e91-2060">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="46e91-2060">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="46e91-2061">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="46e91-2061">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="46e91-2062">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2062">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="46e91-2063">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="46e91-2063">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="46e91-2064">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="46e91-2064">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="46e91-2065">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="46e91-2065">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="46e91-2066">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="46e91-2066">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="46e91-2067">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2067">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="46e91-2068">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="46e91-2068">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="46e91-2069">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="46e91-2069">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="46e91-2070">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2070">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="46e91-2071">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="46e91-2071">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="46e91-2072">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="46e91-2072">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="46e91-2073">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2073">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="46e91-2074">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2074">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="46e91-2075">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="46e91-2075">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="46e91-2076">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="46e91-2076">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="46e91-2077">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2077">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="46e91-2078">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2078">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="46e91-2079">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="46e91-2079">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="46e91-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="46e91-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="46e91-2081">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="46e91-2081">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="46e91-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="46e91-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="46e91-2083">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="46e91-2083">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="46e91-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="46e91-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="46e91-2085">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="46e91-2085">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="46e91-2086">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="46e91-2086">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="46e91-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="46e91-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="46e91-2088">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="46e91-2088">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="46e91-2089">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="46e91-2089">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="46e91-2090">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="46e91-2090">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-2091">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-2091">Az.Automation</span></span>
* <span data-ttu-id="46e91-2092">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2092">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="46e91-2093">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2093">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="46e91-2094">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2094">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="46e91-2095">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2095">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="46e91-2096">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="46e91-2097">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2097">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="46e91-2098">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-2098">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2099">Az.Compute</span></span>
* <span data-ttu-id="46e91-2100">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2100">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="46e91-2101">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="46e91-2101">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-2102">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-2102">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-2103">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2103">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-2104">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-2104">Az.Monitor</span></span>
* <span data-ttu-id="46e91-2105">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2105">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2106">Az.Network</span></span>
* <span data-ttu-id="46e91-2107">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2107">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="46e91-2108">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="46e91-2108">Updated cmdlet:</span></span>
        - <span data-ttu-id="46e91-2109">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="46e91-2109">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="46e91-2110">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2110">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2111">Az.Resources</span></span>
* <span data-ttu-id="46e91-2112">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2112">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2113">Az.Sql</span></span>
* <span data-ttu-id="46e91-2114">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="46e91-2114">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="46e91-2115">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2115">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-2116">Az.Accounts</span></span>
* <span data-ttu-id="46e91-2117">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="46e91-2117">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-2118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2118">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-2119">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="46e91-2119">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="46e91-2120">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="46e91-2120">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2121">Az.Compute</span></span>
* <span data-ttu-id="46e91-2122">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="46e91-2122">Proximity placement group feature.</span></span>
    - <span data-ttu-id="46e91-2123">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="46e91-2123">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="46e91-2124">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-2124">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="46e91-2125">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2125">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="46e91-2126">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-2126">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="46e91-2127">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2127">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="46e91-2128">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="46e91-2128">Breaking changes</span></span>
    - <span data-ttu-id="46e91-2129">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2129">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="46e91-2130">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2130">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="46e91-2131">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="46e91-2131">Az.DeploymentManager</span></span>
* <span data-ttu-id="46e91-2132">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="46e91-2132">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="46e91-2133">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="46e91-2133">Az.Dns</span></span>
* <span data-ttu-id="46e91-2134">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="46e91-2134">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="46e91-2135">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="46e91-2135">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="46e91-2136">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-2136">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46e91-2137">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-2137">Az.FrontDoor</span></span>
* <span data-ttu-id="46e91-2138">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="46e91-2138">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="46e91-2139">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="46e91-2139">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="46e91-2140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-2140">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-2141">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="46e91-2141">Removed two cmdlets:</span></span>
    - <span data-ttu-id="46e91-2142">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46e91-2142">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="46e91-2143">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46e91-2143">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="46e91-2144">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2144">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="46e91-2145">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="46e91-2145">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="46e91-2146">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="46e91-2146">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="46e91-2147">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="46e91-2147">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-2148">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-2148">Az.Monitor</span></span>
* <span data-ttu-id="46e91-2149">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="46e91-2149">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="46e91-2150">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="46e91-2150">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="46e91-2151">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="46e91-2151">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="46e91-2152">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="46e91-2152">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="46e91-2153">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="46e91-2153">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="46e91-2154">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="46e91-2154">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="46e91-2155">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="46e91-2155">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="46e91-2156">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46e91-2156">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46e91-2157">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46e91-2157">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46e91-2158">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46e91-2158">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46e91-2159">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46e91-2159">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46e91-2160">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46e91-2160">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46e91-2161">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="46e91-2161">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="46e91-2162">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2162">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2163">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2163">Az.Network</span></span>
* <span data-ttu-id="46e91-2164">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="46e91-2164">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="46e91-2165">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-2165">New cmdlets</span></span>
        - <span data-ttu-id="46e91-2166">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46e91-2166">New-AzNatGateway</span></span>
        - <span data-ttu-id="46e91-2167">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46e91-2167">Get-AzNatGateway</span></span>
        - <span data-ttu-id="46e91-2168">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46e91-2168">Set-AzNatGateway</span></span>
        - <span data-ttu-id="46e91-2169">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46e91-2169">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="46e91-2170">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2170">Updated cmdlets</span></span>
        - <span data-ttu-id="46e91-2171">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="46e91-2171">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="46e91-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="46e91-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="46e91-2173">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="46e91-2173">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="46e91-2174">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2174">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="46e91-2175">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2175">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46e91-2176">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-2176">Az.PolicyInsights</span></span>
* <span data-ttu-id="46e91-2177">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-2177">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="46e91-2178">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="46e91-2178">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="46e91-2179">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="46e91-2179">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-2180">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2180">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-2181">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-2181">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="46e91-2182">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="46e91-2182">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="46e91-2183">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="46e91-2183">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="46e91-2184">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="46e91-2184">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="46e91-2185">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="46e91-2185">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="46e91-2186">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="46e91-2186">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="46e91-2187">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="46e91-2187">Az.Relay</span></span>
* <span data-ttu-id="46e91-2188">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="46e91-2188">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46e91-2189">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46e91-2189">Az.ServiceBus</span></span>
* <span data-ttu-id="46e91-2190">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2190">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-2191">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-2191">Az.Storage</span></span>
* <span data-ttu-id="46e91-2192">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="46e91-2192">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="46e91-2193">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="46e91-2193">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="46e91-2194">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="46e91-2194">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="46e91-2195">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-2195">New-AzStorageAccount</span></span>
* <span data-ttu-id="46e91-2196">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="46e91-2196">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="46e91-2197">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-2197">New-AzStorageAccount</span></span>
    - <span data-ttu-id="46e91-2198">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-2198">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="46e91-2199">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-2199">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-2200">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2200">Az.Websites</span></span>
* <span data-ttu-id="46e91-2201">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="46e91-2201">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="46e91-2202">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2202">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="46e91-2203">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2203">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46e91-2204">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="46e91-2204">Highlights since the last major release</span></span>
* <span data-ttu-id="46e91-2205">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-2205">General availability of `Az` module</span></span>
* <span data-ttu-id="46e91-2206">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="46e91-2206">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="46e91-2207">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="46e91-2207">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="46e91-2208">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2208">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="46e91-2209">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2209">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46e91-2210">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2210">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="46e91-2211">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-2211">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-2212">Az.Accounts</span></span>
* <span data-ttu-id="46e91-2213">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2213">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46e91-2214">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46e91-2214">Az.Batch</span></span>
* <span data-ttu-id="46e91-2215">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2215">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46e91-2216">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46e91-2216">Az.Cdn</span></span>
* <span data-ttu-id="46e91-2217">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-2218">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2218">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-2219">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2220">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2220">Az.Compute</span></span>
* <span data-ttu-id="46e91-2221">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2221">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="46e91-2222">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46e91-2223">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2223">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-2224">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-2224">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-2225">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2225">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-2227">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2227">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46e91-2228">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46e91-2228">Az.EventGrid</span></span>
* <span data-ttu-id="46e91-2229">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2229">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46e91-2230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46e91-2230">Az.EventHub</span></span>
* <span data-ttu-id="46e91-2231">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2231">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46e91-2232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46e91-2232">Az.HDInsight</span></span>
* <span data-ttu-id="46e91-2233">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-2234">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-2234">Az.IotHub</span></span>
* <span data-ttu-id="46e91-2235">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2235">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-2236">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-2236">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-2237">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2237">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46e91-2238">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2238">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="46e91-2239">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46e91-2239">Az.MachineLearning</span></span>
* <span data-ttu-id="46e91-2240">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="46e91-2241">Az.Media</span><span class="sxs-lookup"><span data-stu-id="46e91-2241">Az.Media</span></span>
* <span data-ttu-id="46e91-2242">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-2243">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-2243">Az.Monitor</span></span>
  * <span data-ttu-id="46e91-2244">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="46e91-2244">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="46e91-2245">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="46e91-2245">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="46e91-2246">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="46e91-2246">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="46e91-2247">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="46e91-2247">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="46e91-2248">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="46e91-2248">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="46e91-2249">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="46e91-2249">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="46e91-2250">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2250">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2251">Az.Network</span></span>
* <span data-ttu-id="46e91-2252">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46e91-2253">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2253">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="46e91-2254">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="46e91-2254">Az.NotificationHubs</span></span>
* <span data-ttu-id="46e91-2255">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-2256">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-2256">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-2257">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="46e91-2258">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="46e91-2258">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="46e91-2259">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2259">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-2261">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2261">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46e91-2262">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="46e91-2262">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="46e91-2263">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2263">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="46e91-2264">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2264">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46e91-2265">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46e91-2265">Az.RedisCache</span></span>
* <span data-ttu-id="46e91-2266">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2266">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2267">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2267">Az.Resources</span></span>
* <span data-ttu-id="46e91-2268">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2268">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2269">Az.Sql</span></span>
* <span data-ttu-id="46e91-2270">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2270">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="46e91-2271">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2271">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46e91-2272">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2272">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="46e91-2273">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2273">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="46e91-2274">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2274">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="46e91-2275">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-2275">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="46e91-2276">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2276">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-2277">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2277">Az.Websites</span></span>
* <span data-ttu-id="46e91-2278">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2278">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="46e91-2279">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2279">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46e91-2280">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2280">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="46e91-2281">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2281">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="46e91-2282">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2282">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46e91-2283">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="46e91-2283">Highlights since the last major release</span></span>
* <span data-ttu-id="46e91-2284">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-2284">General availability of `Az` module</span></span>
* <span data-ttu-id="46e91-2285">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="46e91-2285">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="46e91-2286">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="46e91-2286">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="46e91-2287">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2287">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="46e91-2288">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2288">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46e91-2289">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2289">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="46e91-2290">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-2290">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46e91-2291">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-2291">Az.Accounts</span></span>
* <span data-ttu-id="46e91-2292">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2292">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46e91-2293">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2293">Az.AnalysisServices</span></span>
* <span data-ttu-id="46e91-2294">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="46e91-2294">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="46e91-2295">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="46e91-2295">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-2296">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-2296">Az.Automation</span></span>
* <span data-ttu-id="46e91-2297">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2297">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="46e91-2298">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-2298">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="46e91-2299">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="46e91-2299">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2300">Az.Compute</span></span>
* <span data-ttu-id="46e91-2301">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2301">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="46e91-2302">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2302">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="46e91-2303">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46e91-2303">Az.ContainerInstance</span></span>
* <span data-ttu-id="46e91-2304">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2304">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-2305">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-2305">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-2306">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2306">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="46e91-2307">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2307">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2308">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2308">Az.Resources</span></span>
* <span data-ttu-id="46e91-2309">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2309">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="46e91-2310">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2310">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="46e91-2311">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2311">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="46e91-2312">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="46e91-2312">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="46e91-2313">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2313">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="46e91-2314">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="46e91-2314">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2315">Az.Sql</span></span>
* <span data-ttu-id="46e91-2316">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-2316">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-2317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-2317">Az.Storage</span></span>
* <span data-ttu-id="46e91-2318">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="46e91-2318">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="46e91-2319">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="46e91-2319">New-AzStorageContext</span></span>
* <span data-ttu-id="46e91-2320">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-2320">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="46e91-2321">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="46e91-2321">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="46e91-2322">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="46e91-2322">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="46e91-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46e91-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="46e91-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46e91-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="46e91-2325">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-2325">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="46e91-2326">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46e91-2326">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="46e91-2327">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46e91-2327">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="46e91-2328">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46e91-2328">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="46e91-2329">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46e91-2329">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="46e91-2330">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2330">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46e91-2331">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="46e91-2331">Highlights since the last major release</span></span>
* <span data-ttu-id="46e91-2332">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-2332">General availability of `Az` module</span></span>
* <span data-ttu-id="46e91-2333">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="46e91-2333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="46e91-2334">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="46e91-2334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="46e91-2335">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="46e91-2336">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46e91-2337">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="46e91-2338">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-2338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-2339">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-2339">Az.Automation</span></span>
* <span data-ttu-id="46e91-2340">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="46e91-2340">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="46e91-2341">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="46e91-2341">Dynamic grouping</span></span>
    * <span data-ttu-id="46e91-2342">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="46e91-2342">Pre-Post script</span></span>
    * <span data-ttu-id="46e91-2343">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="46e91-2343">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2344">Az.Compute</span></span>
* <span data-ttu-id="46e91-2345">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="46e91-2345">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="46e91-2346">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2346">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-2347">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-2347">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-2348">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2348">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2349">Az.Network</span></span>
* <span data-ttu-id="46e91-2350">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2350">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="46e91-2351">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2351">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2352">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-2353">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2353">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="46e91-2354">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2354">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2355">Az.Resources</span></span>
* <span data-ttu-id="46e91-2356">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2356">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="46e91-2357">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2357">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2358">Az.Sql</span></span>
* <span data-ttu-id="46e91-2359">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2359">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-2360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-2360">Az.Storage</span></span>
* <span data-ttu-id="46e91-2361">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-2361">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="46e91-2362">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46e91-2362">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="46e91-2363">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46e91-2363">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="46e91-2364">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46e91-2364">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="46e91-2365">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="46e91-2365">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="46e91-2366">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="46e91-2366">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="46e91-2367">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="46e91-2367">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-2368">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2368">Az.Websites</span></span>
* <span data-ttu-id="46e91-2369">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2369">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="46e91-2370">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2370">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-2371">Az.Accounts</span></span>
* <span data-ttu-id="46e91-2372">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2372">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="46e91-2373">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2373">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-2374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-2374">Az.Automation</span></span>
* <span data-ttu-id="46e91-2375">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2375">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="46e91-2376">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2376">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="46e91-2377">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="46e91-2377">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46e91-2378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46e91-2378">Az.Cdn</span></span>
* <span data-ttu-id="46e91-2379">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-2379">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2380">Az.Compute</span></span>
* <span data-ttu-id="46e91-2381">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2381">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-2382">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-2382">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-2383">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2383">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46e91-2384">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46e91-2384">Az.LogicApp</span></span>
* <span data-ttu-id="46e91-2385">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="46e91-2385">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2386">Az.Network</span></span>
* <span data-ttu-id="46e91-2387">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2387">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-2388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2388">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-2389">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2389">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="46e91-2390">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="46e91-2390">SDK Update</span></span>
* <span data-ttu-id="46e91-2391">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-2391">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="46e91-2392">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2392">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2393">Az.Resources</span></span>
* <span data-ttu-id="46e91-2394">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2394">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="46e91-2395">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="46e91-2395">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="46e91-2396">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2396">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="46e91-2397">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="46e91-2397">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="46e91-2398">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2398">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="46e91-2399">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="46e91-2399">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2400">Az.Sql</span></span>
* <span data-ttu-id="46e91-2401">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-2401">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="46e91-2402">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-2402">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-2403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-2403">Az.Storage</span></span>
* <span data-ttu-id="46e91-2404">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46e91-2404">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="46e91-2405">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2405">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="46e91-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2406">Az.AnalysisServices</span></span>
* <span data-ttu-id="46e91-2407">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-2407">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-2408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-2408">Az.Automation</span></span>
* <span data-ttu-id="46e91-2409">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2409">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="46e91-2410">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2410">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="46e91-2411">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2411">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-2412">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2412">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-2413">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2413">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2414">Az.Compute</span></span>
* <span data-ttu-id="46e91-2415">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2415">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="46e91-2416">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2416">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="46e91-2417">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2417">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="46e91-2418">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="46e91-2418">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-2419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-2419">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-2420">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2420">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46e91-2421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46e91-2421">Az.EventHub</span></span>
* <span data-ttu-id="46e91-2422">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2422">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-2423">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-2423">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-2424">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2424">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46e91-2425">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46e91-2425">Az.LogicApp</span></span>
* <span data-ttu-id="46e91-2426">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2426">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="46e91-2427">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2427">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="46e91-2428">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-2428">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="46e91-2429">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46e91-2429">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="46e91-2430">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46e91-2430">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="46e91-2431">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46e91-2431">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="46e91-2432">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46e91-2432">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="46e91-2433">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="46e91-2433">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="46e91-2434">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46e91-2434">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="46e91-2435">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46e91-2435">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="46e91-2436">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46e91-2436">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="46e91-2437">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46e91-2437">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="46e91-2438">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2438">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46e91-2439">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-2439">Az.Monitor</span></span>
* <span data-ttu-id="46e91-2440">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2440">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2441">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2441">Az.Network</span></span>
* <span data-ttu-id="46e91-2442">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2442">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-2443">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-2443">Az.OperationalInsights</span></span>
* <span data-ttu-id="46e91-2444">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="46e91-2444">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="46e91-2445">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2445">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="46e91-2446">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2446">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2447">Az.Resources</span></span>
* <span data-ttu-id="46e91-2448">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2448">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="46e91-2449">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2449">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="46e91-2450">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2450">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="46e91-2451">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2451">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2452">Az.Sql</span></span>
* <span data-ttu-id="46e91-2453">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2453">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="46e91-2454">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2454">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-2455">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2455">Az.Websites</span></span>
* <span data-ttu-id="46e91-2456">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2456">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="46e91-2457">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2457">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-2458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-2458">Az.Accounts</span></span>
* <span data-ttu-id="46e91-2459">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="46e91-2459">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46e91-2460">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2460">Az.AnalysisServices</span></span>
<span data-ttu-id="46e91-2461">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="46e91-2461">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2462">Az.Compute</span></span>
* <span data-ttu-id="46e91-2463">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2463">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="46e91-2464">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2464">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="46e91-2465">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2465">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-2466">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2466">Az.RecoveryServices</span></span>
<span data-ttu-id="46e91-2467">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="46e91-2467">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2468">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2468">Az.Resources</span></span>
* <span data-ttu-id="46e91-2469">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2469">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="46e91-2470">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="46e91-2470">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="46e91-2471">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2471">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="46e91-2472">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="46e91-2472">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2473">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2473">Az.Sql</span></span>
* <span data-ttu-id="46e91-2474">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46e91-2474">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="46e91-2475">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2475">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="46e91-2476">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2476">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="46e91-2477">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2477">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-2478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-2478">Az.Accounts</span></span>
* <span data-ttu-id="46e91-2479">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="46e91-2479">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46e91-2480">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2480">Az.AnalysisServices</span></span>
* <span data-ttu-id="46e91-2481">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="46e91-2481">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-2482">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2482">Az.RecoveryServices</span></span>
* <span data-ttu-id="46e91-2483">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="46e91-2483">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="46e91-2484">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2484">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-2485">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-2485">Az.Accounts</span></span>
* <span data-ttu-id="46e91-2486">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2486">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46e91-2487">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2487">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46e91-2488">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2488">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="46e91-2489">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46e91-2489">Az.Aks</span></span>
* <span data-ttu-id="46e91-2490">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2490">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46e91-2491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-2491">Az.Automation</span></span>
* <span data-ttu-id="46e91-2492">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2492">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="46e91-2493">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2493">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46e91-2494">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46e91-2494">Az.Cdn</span></span>
* <span data-ttu-id="46e91-2495">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2495">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2496">Az.Compute</span></span>
* <span data-ttu-id="46e91-2497">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2497">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="46e91-2498">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2498">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="46e91-2499">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2499">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="46e91-2500">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="46e91-2500">Az.ContainerRegistry</span></span>
* <span data-ttu-id="46e91-2501">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2501">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46e91-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46e91-2502">Az.DataFactory</span></span>
* <span data-ttu-id="46e91-2503">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2503">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-2504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-2504">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-2505">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2505">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="46e91-2506">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="46e91-2506">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="46e91-2507">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2507">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-2508">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-2508">Az.IotHub</span></span>
* <span data-ttu-id="46e91-2509">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2509">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46e91-2510">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-2510">Az.KeyVault</span></span>
* <span data-ttu-id="46e91-2511">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2511">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2512">Az.Network</span></span>
* <span data-ttu-id="46e91-2513">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2513">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2514">Az.Resources</span></span>
* <span data-ttu-id="46e91-2515">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2515">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="46e91-2516">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2516">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="46e91-2517">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2517">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="46e91-2518">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2518">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="46e91-2519">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2519">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="46e91-2520">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2520">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="46e91-2521">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="46e91-2521">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46e91-2522">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-2522">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-2523">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="46e91-2523">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="46e91-2524">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2524">Fix some error messages.</span></span>
* <span data-ttu-id="46e91-2525">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2525">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="46e91-2526">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2526">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46e91-2527">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46e91-2527">Az.SignalR</span></span>
* <span data-ttu-id="46e91-2528">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2528">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2529">Az.Sql</span></span>
* <span data-ttu-id="46e91-2530">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2530">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46e91-2531">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2531">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="46e91-2532">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2532">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="46e91-2533">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-2533">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-2534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-2534">Az.Storage</span></span>
* <span data-ttu-id="46e91-2535">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46e91-2536">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-2536">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="46e91-2537">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="46e91-2537">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="46e91-2538">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="46e91-2538">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="46e91-2539">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46e91-2539">Az.TrafficManager</span></span>
* <span data-ttu-id="46e91-2540">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2540">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-2541">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2541">Az.Websites</span></span>
* <span data-ttu-id="46e91-2542">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2542">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46e91-2543">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2543">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="46e91-2544">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2544">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="46e91-2545">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="46e91-2545">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46e91-2546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-2546">Az.Accounts</span></span>
* <span data-ttu-id="46e91-2547">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2547">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2548">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2548">Az.Compute</span></span>
* <span data-ttu-id="46e91-2549">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="46e91-2549">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="46e91-2550">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2550">Updated the description of ID in help files</span></span>
* <span data-ttu-id="46e91-2551">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="46e91-2551">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-2552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-2552">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-2553">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2553">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="46e91-2554">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2554">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46e91-2555">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46e91-2555">Az.EventGrid</span></span>
* <span data-ttu-id="46e91-2556">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2556">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="46e91-2557">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2557">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="46e91-2558">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-2558">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="46e91-2559">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="46e91-2559">Event Time-To-Live,</span></span>
        - <span data-ttu-id="46e91-2560">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="46e91-2560">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="46e91-2561">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="46e91-2561">Dead letter endpoint.</span></span>
    - <span data-ttu-id="46e91-2562">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-2562">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="46e91-2563">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="46e91-2563">Event Time-To-Live,</span></span>
        - <span data-ttu-id="46e91-2564">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="46e91-2564">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="46e91-2565">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="46e91-2565">Dead letter endpoint.</span></span>
* <span data-ttu-id="46e91-2566">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2566">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="46e91-2567">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-2567">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46e91-2568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46e91-2568">Az.IotHub</span></span>
* <span data-ttu-id="46e91-2569">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2569">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46e91-2570">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46e91-2570">Az.LogicApp</span></span>
* <span data-ttu-id="46e91-2571">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="46e91-2571">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2572">Az.Resources</span></span>
* <span data-ttu-id="46e91-2573">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2573">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="46e91-2574">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="46e91-2574">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="46e91-2575">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2575">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="46e91-2576">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2576">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="46e91-2577">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2577">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="46e91-2578">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="46e91-2578">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46e91-2579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46e91-2579">Az.SignalR</span></span>
* <span data-ttu-id="46e91-2580">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="46e91-2580">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2581">Az.Sql</span></span>
* <span data-ttu-id="46e91-2582">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="46e91-2582">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46e91-2583">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-2583">Az.Storage</span></span>
* <span data-ttu-id="46e91-2584">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="46e91-2584">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="46e91-2585">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="46e91-2585">New-AzStorageContext</span></span>
* <span data-ttu-id="46e91-2586">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2586">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="46e91-2587">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="46e91-2587">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-2588">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2588">Az.Websites</span></span>
* <span data-ttu-id="46e91-2589">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2589">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="46e91-2590">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="46e91-2590">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="46e91-2591">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="46e91-2591">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="46e91-2592">Genel</span><span class="sxs-lookup"><span data-stu-id="46e91-2592">General</span></span>

- <span data-ttu-id="46e91-2593">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-2593">General Availability of Az Module</span></span>
- <span data-ttu-id="46e91-2594">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="46e91-2594">Online help for each module</span></span>
- <span data-ttu-id="46e91-2595">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="46e91-2595">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="46e91-2596">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2596">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="46e91-2597">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46e91-2597">Az.Accounts</span></span>
- <span data-ttu-id="46e91-2598">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46e91-2598">Changed from Az.Profile</span></span>
- <span data-ttu-id="46e91-2599">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2599">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="46e91-2600">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-2600">Az.ApiManagement</span></span>
- <span data-ttu-id="46e91-2601">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="46e91-2601">Fixes for #7002</span></span>
- <span data-ttu-id="46e91-2602">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2602">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="46e91-2603">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46e91-2603">Az.Batch</span></span>
- <span data-ttu-id="46e91-2604">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2604">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="46e91-2605">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="46e91-2605">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="46e91-2606">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2606">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="46e91-2607">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="46e91-2607">Az.Billing</span></span>
- <span data-ttu-id="46e91-2608">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2608">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="46e91-2609">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2609">Az.CognitivServices</span></span>
- <span data-ttu-id="46e91-2610">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2610">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="46e91-2611">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-2611">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="46e91-2612">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46e91-2612">Az.ContainerInstance</span></span>
- <span data-ttu-id="46e91-2613">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2613">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="46e91-2614">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="46e91-2614">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="46e91-2615">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2615">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="46e91-2616">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-2616">Az.DataLakeStore</span></span>
- <span data-ttu-id="46e91-2617">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2617">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="46e91-2618">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46e91-2618">Az.Monitor</span></span>
- <span data-ttu-id="46e91-2619">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2619">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="46e91-2620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46e91-2620">Az.KeyVault</span></span>
- <span data-ttu-id="46e91-2621">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-2621">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="46e91-2622">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46e91-2622">Az.MachineLearning</span></span>
- <span data-ttu-id="46e91-2623">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2623">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="46e91-2624">Az.Media</span><span class="sxs-lookup"><span data-stu-id="46e91-2624">Az.Media</span></span>
- <span data-ttu-id="46e91-2625">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="46e91-2625">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="46e91-2626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2626">Az.Network</span></span>
<span data-ttu-id="46e91-2627">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2627">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="46e91-2628">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="46e91-2628">New cmdlets added:</span></span>
        - <span data-ttu-id="46e91-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46e91-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46e91-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46e91-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46e91-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46e91-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46e91-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46e91-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46e91-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46e91-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46e91-2634">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="46e91-2634">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="46e91-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="46e91-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="46e91-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="46e91-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="46e91-2637">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2637">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="46e91-2638">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46e91-2638">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="46e91-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46e91-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="46e91-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46e91-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="46e91-2641">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-2641">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="46e91-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="46e91-2643">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2643">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="46e91-2644">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2644">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="46e91-2645">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="46e91-2645">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="46e91-2646">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="46e91-2646">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="46e91-2647">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="46e91-2647">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="46e91-2648">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2648">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="46e91-2649">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="46e91-2650">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-2650">Az.OperationalInsights</span></span>
- <span data-ttu-id="46e91-2651">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="46e91-2652">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46e91-2652">Az.Profile</span></span>
- <span data-ttu-id="46e91-2653">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2653">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-2654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2654">Az.RecoveryServices</span></span>
- <span data-ttu-id="46e91-2655">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2655">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="46e91-2656">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2656">Az.Resources</span></span>
- <span data-ttu-id="46e91-2657">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2657">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="46e91-2658">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-2658">Az.ServiceFabric</span></span>
- <span data-ttu-id="46e91-2659">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="46e91-2659">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="46e91-2660">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2660">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="46e91-2661">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="46e91-2661">Az.SIgnalR</span></span>
- <span data-ttu-id="46e91-2662">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="46e91-2662">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="46e91-2663">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2663">Az.Sql</span></span>
- <span data-ttu-id="46e91-2664">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2664">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="46e91-2665">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2665">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="46e91-2666">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2666">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="46e91-2667">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-2667">Az.Storage</span></span>
- <span data-ttu-id="46e91-2668">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2668">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="46e91-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2669">Az.Websites</span></span>
- <span data-ttu-id="46e91-2670">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46e91-2670">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="46e91-2671">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="46e91-2671">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="46e91-2672">Genel</span><span class="sxs-lookup"><span data-stu-id="46e91-2672">General</span></span>

* <span data-ttu-id="46e91-2673">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="46e91-2673">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="46e91-2674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2674">Az.Compute</span></span>

* <span data-ttu-id="46e91-2675">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2675">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="46e91-2676">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-2676">Az.DataLakeStore</span></span>

* <span data-ttu-id="46e91-2677">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2677">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="46e91-2678">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46e91-2678">Az.FrontDoor</span></span>

* <span data-ttu-id="46e91-2679">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2679">Fixed some broken links</span></span>
    - <span data-ttu-id="46e91-2680">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2680">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="46e91-2681">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2681">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="46e91-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2682">Az.RecoveryServices</span></span>

* <span data-ttu-id="46e91-2683">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2683">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="46e91-2684">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2684">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="46e91-2685">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2685">Az.Resources</span></span>

* <span data-ttu-id="46e91-2686">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="46e91-2686">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="46e91-2687">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2687">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="46e91-2688">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2688">Az.Sql</span></span>

* <span data-ttu-id="46e91-2689">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="46e91-2689">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="46e91-2690">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2690">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="46e91-2691">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2691">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="46e91-2692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46e91-2692">Az.Storage</span></span>

* <span data-ttu-id="46e91-2693">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2693">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="46e91-2694">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2694">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="46e91-2695">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="46e91-2695">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="46e91-2696">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2696">Support Static Website configuration</span></span>
    - <span data-ttu-id="46e91-2697">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="46e91-2697">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="46e91-2698">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="46e91-2698">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="46e91-2699">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2699">Az.Websites</span></span>

* <span data-ttu-id="46e91-2700">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="46e91-2700">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="46e91-2701">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2701">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="46e91-2702">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="46e91-2702">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="46e91-2703">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="46e91-2703">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="46e91-2704">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46e91-2704">Az.ApiManagement</span></span>
* <span data-ttu-id="46e91-2705">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="46e91-2705">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="46e91-2706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46e91-2706">Az.Automation</span></span>
* <span data-ttu-id="46e91-2707">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="46e91-2707">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="46e91-2708">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2708">Added Update Management cmdlets</span></span>
* <span data-ttu-id="46e91-2709">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2709">Added Source Control cmdlets</span></span>
* <span data-ttu-id="46e91-2710">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2710">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="46e91-2711">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2711">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="46e91-2712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2712">Az.Compute</span></span>
* <span data-ttu-id="46e91-2713">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2713">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="46e91-2714">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="46e91-2714">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="46e91-2715">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46e91-2715">Az.ContainerInstance</span></span>
* <span data-ttu-id="46e91-2716">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="46e91-2716">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="46e91-2717">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="46e91-2717">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="46e91-2718">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2718">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="46e91-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2719">Az.Network</span></span>
* <span data-ttu-id="46e91-2720">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2720">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="46e91-2721">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2721">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="46e91-2722">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2722">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="46e91-2723">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2723">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="46e91-2724">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46e91-2724">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46e91-2725">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2725">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="46e91-2726">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="46e91-2726">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="46e91-2727">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="46e91-2727">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="46e91-2728">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2728">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="46e91-2729">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="46e91-2729">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="46e91-2730">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="46e91-2730">Az.Relay</span></span>
* <span data-ttu-id="46e91-2731">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2731">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="46e91-2732">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2732">Az.Resources</span></span>
* <span data-ttu-id="46e91-2733">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2733">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="46e91-2734">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2734">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="46e91-2735">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="46e91-2735">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="46e91-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-2737">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2737">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="46e91-2738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2738">Az.Sql</span></span>
* <span data-ttu-id="46e91-2739">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2739">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="46e91-2740">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46e91-2740">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46e91-2741">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46e91-2741">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46e91-2742">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46e91-2742">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46e91-2743">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46e91-2743">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46e91-2744">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46e91-2744">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46e91-2745">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46e91-2745">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46e91-2746">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46e91-2746">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46e91-2747">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46e91-2747">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="46e91-2748">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2748">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="46e91-2749">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2749">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="46e91-2750">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2750">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="46e91-2751">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="46e91-2751">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="46e91-2752">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="46e91-2752">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="46e91-2753">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="46e91-2753">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="46e91-2754">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="46e91-2754">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="46e91-2755">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2755">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="46e91-2756">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="46e91-2756">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="46e91-2757">Genel</span><span class="sxs-lookup"><span data-stu-id="46e91-2757">General</span></span>
* <span data-ttu-id="46e91-2758">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="46e91-2758">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="46e91-2759">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46e91-2759">Az.Profile</span></span>
* <span data-ttu-id="46e91-2760">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2760">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="46e91-2761">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2761">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="46e91-2762">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2762">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="46e91-2763">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2763">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="46e91-2764">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2764">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="46e91-2765">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2765">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="46e91-2766">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2766">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-2767">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2767">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-2768">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2768">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2769">Az.Compute</span></span>
* <span data-ttu-id="46e91-2770">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2770">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="46e91-2771">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="46e91-2771">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="46e91-2772">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2772">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-2773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-2773">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-2774">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2774">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="46e91-2775">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2775">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="46e91-2776">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="46e91-2776">Az.Insights</span></span>
* <span data-ttu-id="46e91-2777">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2777">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="46e91-2778">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="46e91-2778">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="46e91-2779">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2779">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="46e91-2780">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="46e91-2780">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2781">Az.Network</span></span>
* <span data-ttu-id="46e91-2782">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="46e91-2782">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="46e91-2783">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="46e91-2783">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="46e91-2784">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="46e91-2784">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="46e91-2785">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46e91-2785">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="46e91-2786">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="46e91-2786">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="46e91-2787">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="46e91-2787">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="46e91-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46e91-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46e91-2789">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46e91-2789">Az.PolicyInsights</span></span>
* <span data-ttu-id="46e91-2790">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2790">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2791">Az.Resources</span></span>
* <span data-ttu-id="46e91-2792">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="46e91-2792">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="46e91-2793">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="46e91-2793">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46e91-2794">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46e91-2794">Az.ServiceBus</span></span>
* <span data-ttu-id="46e91-2795">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2795">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46e91-2796">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46e91-2796">Az.ServiceFabric</span></span>
* <span data-ttu-id="46e91-2797">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2797">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="46e91-2798">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2798">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="46e91-2799">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="46e91-2799">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="46e91-2800">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="46e91-2800">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="46e91-2801">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2801">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="46e91-2802">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="46e91-2802">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="46e91-2803">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46e91-2803">Az.Profile</span></span>
* <span data-ttu-id="46e91-2804">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="46e91-2804">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="46e91-2805">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2805">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2806">Az.Compute</span></span>
* <span data-ttu-id="46e91-2807">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2807">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="46e91-2808">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2808">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46e91-2809">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46e91-2809">Az.DataLakeStore</span></span>
* <span data-ttu-id="46e91-2810">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="46e91-2810">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="46e91-2811">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="46e91-2811">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="46e91-2812">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="46e91-2812">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="46e91-2813">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="46e91-2813">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="46e91-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="46e91-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2815">Az.Network</span></span>
* <span data-ttu-id="46e91-2816">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-2816">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="46e91-2817">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2817">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2818">Az.Resources</span></span>
* <span data-ttu-id="46e91-2819">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2819">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="46e91-2820">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2820">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="46e91-2821">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="46e91-2821">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="46e91-2822">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="46e91-2822">Azure.Storage</span></span>
* <span data-ttu-id="46e91-2823">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="46e91-2823">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="46e91-2824">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46e91-2824">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="46e91-2825">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="46e91-2825">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="46e91-2826">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="46e91-2826">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="46e91-2827">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="46e91-2827">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46e91-2828">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46e91-2828">Az.CognitiveServices</span></span>
* <span data-ttu-id="46e91-2829">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="46e91-2829">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46e91-2830">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46e91-2830">Az.Compute</span></span>
* <span data-ttu-id="46e91-2831">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2831">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="46e91-2832">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2832">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="46e91-2833">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2833">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="46e91-2834">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="46e91-2834">Az.DataFactoryV2</span></span>
* <span data-ttu-id="46e91-2835">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2835">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46e91-2836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46e91-2836">Az.Network</span></span>
* <span data-ttu-id="46e91-2837">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="46e91-2837">Added NetworkProfile functionality.</span></span> <span data-ttu-id="46e91-2838">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2838">new cmdlets added</span></span>
    - <span data-ttu-id="46e91-2839">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46e91-2839">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="46e91-2840">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46e91-2840">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="46e91-2841">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46e91-2841">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="46e91-2842">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46e91-2842">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="46e91-2843">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-2843">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="46e91-2844">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="46e91-2844">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="46e91-2845">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2845">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="46e91-2846">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2846">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="46e91-2847">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2847">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46e91-2848">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46e91-2848">Az.RedisCache</span></span>
* <span data-ttu-id="46e91-2849">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="46e91-2849">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="46e91-2850">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2850">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="46e91-2851">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46e91-2851">Az.Resources</span></span>
* <span data-ttu-id="46e91-2852">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="46e91-2852">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="46e91-2853">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2853">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="46e91-2854">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46e91-2854">Az.Sql</span></span>
* <span data-ttu-id="46e91-2855">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="46e91-2855">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46e91-2856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46e91-2856">Az.Websites</span></span>
* <span data-ttu-id="46e91-2857">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="46e91-2857">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="46e91-2858">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="46e91-2858">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="46e91-2859">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="46e91-2859">0.2.0 - September 2018</span></span>
 <span data-ttu-id="46e91-2860">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="46e91-2860">Initial Release</span></span>
