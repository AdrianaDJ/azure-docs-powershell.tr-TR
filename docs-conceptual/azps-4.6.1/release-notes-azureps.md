---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 04e85c32b1af0bbdfb622973e0900724b8e3c8e3
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244237"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="7672c-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="7672c-103">Azure PowerShell release notes</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="7672c-104">4.6.1 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-104">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="7672c-105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-105">Az.Compute</span></span>
* <span data-ttu-id="7672c-106">False değerinin varsayılan değerini kaldırmak için 'New-AzVm' içindeki '-EncryptionAtHost' parametresine yama uygulandı [#12776]</span><span class="sxs-lookup"><span data-stu-id="7672c-106">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="7672c-107">4.6.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-107">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-108">Az.Accounts</span></span>
* <span data-ttu-id="7672c-109">Bulma uç noktası varsayılan AzureCloud ortamını veya diğer genel ortamları döndürmediğinden tüm genel bulut ortamları yüklendi (#12633)</span><span class="sxs-lookup"><span data-stu-id="7672c-109">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="7672c-110">SubscriptionPolicies, 'Get-AzSubscription' cmdlet’inde kullanıma sunuldu [#12551]</span><span class="sxs-lookup"><span data-stu-id="7672c-110">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-111">Az.Automation</span></span>
* <span data-ttu-id="7672c-112">Karma Çalışanı Grubu belirtmek için 'Set-AzAutomationWebhook' cmdlet’ine '-RunOn' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-112">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-113">Az.Compute</span></span>
* <span data-ttu-id="7672c-114">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' ve 'Update-AzVmss' cmdlet’lerine '-EncryptionAtHost' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-114">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="7672c-115">'Get-AzVM' ve 'Get-AzVmss' cmdlet’lerinin dönüş nesnesine 'SecurityProfile' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-115">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="7672c-116">'-InstanceView' anahtarı 'Get-AzHostGroup' cmdlet’ine isteğe bağlı parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-116">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="7672c-117">Yeni 'Invoke-AzVmPatchAssessment' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-117">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-118">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-118">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-119">PSPipelineRun sınıfındaki eksik özellikler eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-119">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-120">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-121">Konakta şifreleme özelliğiyle küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-121">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-122">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-123">Geçici silmeyi devre dışı bırakma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-123">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="7672c-124">SecretValueText özniteliğini kaldırma planlaması için uyarı iletileri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-124">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="7672c-125">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="7672c-125">Az.Maintenance</span></span>
* <span data-ttu-id="7672c-126">'New-AzMaintenanceConfiguration' cmdlet’ine isteğe bağlı zamanlamayla ilgili alanlar eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-126">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="7672c-127">'Get-AzMaintenancePublicConfiguration' için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-127">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7672c-128">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7672c-128">Az.ManagedServices</span></span>
* <span data-ttu-id="7672c-129">Yönetilen hizmet atama ve tanım cmdlet’lerine hataya neden olan değişiklik uyarıları eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-129">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-130">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-130">Az.Monitor</span></span>
* <span data-ttu-id="7672c-131">Günlüklerin ve Ölçümlerin ayrılmasını etkinleştirmek için 'Set-AzDiagnosticSetting' cmdlet’indeki parametre kümesi genişletildi [#12482]</span><span class="sxs-lookup"><span data-stu-id="7672c-131">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="7672c-132">'Add-AzMetricAlertRuleV2' cmdlet’inde işlem hattından ölçüm uyarısı alınırken oluşan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-132">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-133">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-133">Az.Resources</span></span>
* <span data-ttu-id="7672c-134">'Get-AzPolicyAlias' cmdlet’i, diğer adın Azure İlkesi tarafından değiştirilebilir olup olmadığını belirten bilgiler içerek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-134">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="7672c-135">Yeni 'Set-AzRoleAssignment' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-135">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="7672c-136">Yönetim grubu kapsamındaki ARM şablonu Durum sonuçlarını almak için 'Get-AzDeploymentManagementGroupWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-136">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="7672c-137">Kiracı kapsamındaki ARM şablonu Durum sonuçlarını almaya yönelik yeni 'Get-AzTenantWhatIfResult' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-137">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="7672c-138">'New-AzManagementGroupDeployment' ve 'New-AzTenantDeployment' için '-WhatIf' ve '-Confirm' parametreleri, ARM şablonu Durum sonuçlarını kullanacak şekilde geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="7672c-138">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="7672c-139">Yeni dağıtım cmdlet’lerindeki '-WhatIf' ve '-Confirm' parametrelerinin davranışları False ile uyumlu olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-139">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="7672c-140">'-TemplateObject' ve 'TemplateParameterObject' için serileştirme hatası düzeltildi [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="7672c-140">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="7672c-141">'Get-AzResourceGroupDeploymentOperation' cmdlet’ine, yaklaşan çıkış türü değişikliğine yönelik hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-141">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7672c-142">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7672c-142">Az.SignalR</span></span>
* <span data-ttu-id="7672c-143">'Restart-AzSignalR' ve 'Update-AzSignalR' yardım dosyalarındaki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-143">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="7672c-144">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-144">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-145">Az.Storage</span></span>
* <span data-ttu-id="7672c-146">Blob sorgu hızlandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-146">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="7672c-147">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="7672c-147">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="7672c-148">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="7672c-148">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="7672c-149">Yardım dosyası güncelleştirildi, daha fazla açıklama eklendi ve yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-149">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="7672c-150">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="7672c-150">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="7672c-151">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="7672c-151">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="7672c-152">İlgili alt dizin mevcut olmadığında blobu indirme işleminin başarısız olmasıyla ilgili sorun düzeltildi [#12592]</span><span class="sxs-lookup"><span data-stu-id="7672c-152">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="7672c-153">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="7672c-153">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="7672c-154">Depolama hesaplarında Set/Get/Remove Nesne Çoğaltma İlkesi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-154">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="7672c-155">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="7672c-155">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="7672c-156">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="7672c-156">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="7672c-157">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="7672c-157">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="7672c-158">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="7672c-158">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="7672c-159">Bir Depolama hesabının Blob Hizmeti üzerinde ChangeFeed’i etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-159">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="7672c-160">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="7672c-160">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="7672c-161">4.5.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-161">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-162">Az.Accounts</span></span>
* <span data-ttu-id="7672c-163">'Connect-AzAccount' cmdlet’i 'MaxContextPopulation' parametresini kabul edecek şekilde güncelleştirildi [#9865]</span><span class="sxs-lookup"><span data-stu-id="7672c-163">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="7672c-164">SubscriptionClient sürümü 2019-06-01 olarak ve kiracı etki alanlarını görüntüleyecek şekilde güncelleştirildi [#9838]</span><span class="sxs-lookup"><span data-stu-id="7672c-164">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="7672c-165">Aboneliğin giriş kiracısı ve yöneten kiracısı bilgilerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-165">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="7672c-166">Telemetri verilerindeki modül adı ve sürüm bilgileri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-166">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="7672c-167">SqlDatabaseDnsSuffix ve ServiceManagementUrl, ortam meta verileri uç noktasının uyumsuz değer döndürdüğü durumlar için ayarlandı</span><span class="sxs-lookup"><span data-stu-id="7672c-167">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="7672c-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7672c-168">Az.Aks</span></span>
* <span data-ttu-id="7672c-169">'ClientIdAndSecret' kaldırılarak 'ServicePrincipalIdAndSecret' eklendi ve 'ClientIdAndSecret' bir diğer ad olarak ayarlandı [#12381].</span><span class="sxs-lookup"><span data-stu-id="7672c-169">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="7672c-170">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' cmdlet’leri kaldırılarak 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' eklendi ve özgün olanlar diğer ad olarak ayarlandı [#12373].</span><span class="sxs-lookup"><span data-stu-id="7672c-170">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7672c-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-171">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-172">Yeni 'Add-AzApiManagementApiToGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-172">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="7672c-173">Yeni 'Get-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-173">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="7672c-174">Yeni 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-174">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="7672c-175">Yeni 'Get-AzApiManagementGatewayKey' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-175">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="7672c-176">Yeni 'New-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-176">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="7672c-177">Yeni 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-177">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="7672c-178">Yeni 'New-AzApiManagementResourceLocationObject' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-178">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="7672c-179">Yeni 'Remove-AzApiManagementApiFromGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-179">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="7672c-180">Yeni 'Remove-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-180">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="7672c-181">Yeni 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-181">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="7672c-182">Yeni 'Update-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-182">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="7672c-183">'Get-AzApiManagementApi' cmdlet’ine yeni ve isteğe bağlı [-GatewayId] parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-183">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-184">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-184">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-185">'Deny', özellikle NetworkRules varsayılan eylemi olarak kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-185">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7672c-186">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-186">Az.FrontDoor</span></span>
* <span data-ttu-id="7672c-187">Enum.Parse metodu, bir null değeri Enabled veya Disabled sabit listesi değerlerine zorladığında özel durum oluşturulmasıyla ilgili bir sorun düzeltildi [#12344]</span><span class="sxs-lookup"><span data-stu-id="7672c-187">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-188">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-189">Aktarma özelliğinde şifrelemeye sahip küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-189">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="7672c-190">'New-AzHDInsightCluster' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-190">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="7672c-191">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-191">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="7672c-192">Özel bağlantı özelliğine sahip küme oluşturma desteği eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-192">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="7672c-193">'New-AzHDInsightCluster' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-193">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="7672c-194">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-194">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="7672c-195">'New-AzHDInsightCluster' veya 'Get-AzHDInsightCluster' çağrıldığında sanal ağ bilgileri döndürüldü</span><span class="sxs-lookup"><span data-stu-id="7672c-195">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-196">Az.Network</span></span>
* <span data-ttu-id="7672c-197">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-197">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="7672c-198">Hataya neden olmayan değişiklikler eklendi: 'Remove-AzExpressRouteCircutPeeringConfig' cmdlet’inde Özel Eşleme’ye yönelik PeerAddressType işlevi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-198">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="7672c-199">AddressPrefixType ve PeerAddressType parametresindeki kodlar büyük/küçük harfi yoksayacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-199">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="7672c-200">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-200">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-201">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-202">'Remove-AzOperationalInsightsworkspace' için '-ForceDelete' seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-202">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="7672c-203">Yeni 'Get-AzOperationalInsightsDeletedWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-203">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="7672c-204">Yeni 'Restore-AzOperationalInsightsWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-204">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-206">Azure Backup kapsayıcı/öğe keşif deneyimi iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-206">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-207">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-207">Az.Resources</span></span>
* <span data-ttu-id="7672c-208">'New-AzRoleAssignment' cmdlet’ine 'Condition', 'ConditionVersion' ve 'Description' özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-208">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="7672c-209">Bu, veri modellerinde yapılan tüm ilgili değişiklikleri içerir</span><span class="sxs-lookup"><span data-stu-id="7672c-209">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-210">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-210">Az.Sql</span></span>
* <span data-ttu-id="7672c-211">'New-AzSqlServer' ve 'Set-AzSqlServer' cmdlet’lerindeki sunucu adının olası büyük/küçük harfe duyarsızlık hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-211">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="7672c-212">'New-AzSqlDatabaseSecondary' cmdlet’indeki mevcut veritabanına yanlış veritabanı adının döndürülmesi hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-212">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-213">Az.Storage</span></span>
* <span data-ttu-id="7672c-214">Yeni x,t izniyle kapsayıcı/blob Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-214">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="7672c-215">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="7672c-215">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="7672c-216">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="7672c-216">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="7672c-217">Yeni x,t,f izniyle hesap Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-217">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="7672c-218">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="7672c-218">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="7672c-219">Tek dosya paylaşımı kullanımını alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-219">Supported get single file share usage</span></span>
    - <span data-ttu-id="7672c-220">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="7672c-220">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="7672c-221">4.4.0 - Temmuz 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-221">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-222">Az.Accounts</span></span>
* <span data-ttu-id="7672c-223">“Invoke-AzRestMethod” adlı yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-223">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="7672c-224">“Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]</span><span class="sxs-lookup"><span data-stu-id="7672c-224">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="7672c-225">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7672c-225">Az.Aks</span></span>
* <span data-ttu-id="7672c-226">“Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]</span><span class="sxs-lookup"><span data-stu-id="7672c-226">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7672c-227">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7672c-227">Az.AnalysisServices</span></span>
* <span data-ttu-id="7672c-228">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-228">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-229">Az.Automation</span></span>
* <span data-ttu-id="7672c-230">Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-230">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-231">Az.Compute</span></span>
* <span data-ttu-id="7672c-232">“En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-232">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-233">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-234">Data Factory’ye genel parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-234">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7672c-235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7672c-235">Az.EventGrid</span></span>
* <span data-ttu-id="7672c-236">2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-236">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="7672c-237">Yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-237">Added new features:</span></span>
    - <span data-ttu-id="7672c-238">Giriş eşleme</span><span class="sxs-lookup"><span data-stu-id="7672c-238">Input mapping</span></span>
    - <span data-ttu-id="7672c-239">Olay Teslim Şeması</span><span class="sxs-lookup"><span data-stu-id="7672c-239">Event Delivery Schema</span></span>
    - <span data-ttu-id="7672c-240">Özel Bağlantı</span><span class="sxs-lookup"><span data-stu-id="7672c-240">Private Link</span></span>
    - <span data-ttu-id="7672c-241">Bulut Olayı V10 Şeması</span><span class="sxs-lookup"><span data-stu-id="7672c-241">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="7672c-242">Hedef Olarak Service Bus Konu Başlığı</span><span class="sxs-lookup"><span data-stu-id="7672c-242">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="7672c-243">Hedef Olarak Azure İşlevi</span><span class="sxs-lookup"><span data-stu-id="7672c-243">Azure Function As Destination</span></span>
    - <span data-ttu-id="7672c-244">Web Kancası Toplu İş</span><span class="sxs-lookup"><span data-stu-id="7672c-244">WebHook Batching</span></span>
    - <span data-ttu-id="7672c-245">Güvenli web kancası (AAD desteği)</span><span class="sxs-lookup"><span data-stu-id="7672c-245">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="7672c-246">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="7672c-246">IpFiltering</span></span>
* <span data-ttu-id="7672c-247">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-247">Updated cmdlets:</span></span>
    - <span data-ttu-id="7672c-248">“New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="7672c-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="7672c-249">Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-249">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="7672c-250">AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-250">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="7672c-251">Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-251">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="7672c-252">Teslim şeması için yeni, isteğe bağlı parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-252">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="7672c-253">“New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="7672c-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="7672c-254">IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-254">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="7672c-255">“New-AzEventGridTopic'/'New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="7672c-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="7672c-256">Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-256">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7672c-257">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-257">Az.FrontDoor</span></span>
* <span data-ttu-id="7672c-258">Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-258">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="7672c-259">Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-259">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-260">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-260">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-261">Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-261">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-262">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-262">Az.Monitor</span></span>
* <span data-ttu-id="7672c-263">Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]</span><span class="sxs-lookup"><span data-stu-id="7672c-263">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-264">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-264">Az.Network</span></span>
* <span data-ttu-id="7672c-265">VWan HubVnet bağlantısında değişen parametreler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-265">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="7672c-266">Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-266">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="7672c-267">“Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="7672c-267">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="7672c-268">“New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="7672c-268">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="7672c-269">“Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="7672c-269">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="7672c-270">“Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="7672c-270">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="7672c-271">“New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="7672c-271">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="7672c-272">Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-272">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="7672c-273">“Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="7672c-273">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="7672c-274">“New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="7672c-274">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="7672c-275">“Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="7672c-275">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="7672c-276">“Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="7672c-276">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="7672c-277">“Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="7672c-277">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="7672c-278">“New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="7672c-278">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="7672c-279">Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-279">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="7672c-280">Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-280">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="7672c-281">Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-281">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-283">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-283">Removed project reference to Authentication</span></span>
* <span data-ttu-id="7672c-284">Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı</span><span class="sxs-lookup"><span data-stu-id="7672c-284">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="7672c-285">Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="7672c-285">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-286">Az.Resources</span></span>
* <span data-ttu-id="7672c-287">“Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-287">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="7672c-288">“Unregister-AzResourceProvider” cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-288">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-289">Az.Sql</span></span>
* <span data-ttu-id="7672c-290">“Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-290">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="7672c-291">Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-291">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="7672c-292">Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="7672c-292">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-293">Az.Storage</span></span>
* <span data-ttu-id="7672c-294">Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-294">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="7672c-295">MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-295">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="7672c-296">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="7672c-296">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="7672c-297">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="7672c-297">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="7672c-298">Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-298">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="7672c-299">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="7672c-299">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="7672c-300">Blob sürümlerini içeren destek listesi blobları</span><span class="sxs-lookup"><span data-stu-id="7672c-300">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="7672c-301">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="7672c-301">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="7672c-302">Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-302">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="7672c-303">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="7672c-303">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="7672c-304">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="7672c-304">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="7672c-305">Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-305">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="7672c-306">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="7672c-306">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="7672c-307">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="7672c-307">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="7672c-308">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="7672c-308">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="7672c-309">“Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="7672c-309">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="7672c-310">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="7672c-310">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7672c-311">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7672c-311">Az.StorageSync</span></span>
* <span data-ttu-id="7672c-312">ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-312">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="7672c-313">“UpdateStorageSyncService” cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-313">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="7672c-314">“Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="7672c-314">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="7672c-315">StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-315">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-316">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-316">Az.Websites</span></span>
* <span data-ttu-id="7672c-317">App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-317">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="7672c-318">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-318">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-319">Az.Accounts</span></span>
* <span data-ttu-id="7672c-320">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-320">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="7672c-321">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="7672c-321">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="7672c-322">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-322">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="7672c-323">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="7672c-323">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="7672c-324">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7672c-324">Az.Aks</span></span>
* <span data-ttu-id="7672c-325">Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-325">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7672c-326">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7672c-326">Az.Batch</span></span>
* <span data-ttu-id="7672c-327">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-327">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="7672c-328">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-328">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-329">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-329">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-330">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-330">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="7672c-331">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-331">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-332">Az.Compute</span></span>
* <span data-ttu-id="7672c-333">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-333">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="7672c-334">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-334">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="7672c-335">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="7672c-335">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="7672c-336">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-336">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="7672c-337">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-337">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-338">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-339">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-339">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7672c-340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7672c-340">Az.EventHub</span></span>
* <span data-ttu-id="7672c-341">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-341">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="7672c-342">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="7672c-342">Az.Functions</span></span>
* <span data-ttu-id="7672c-343">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-343">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-344">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-344">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-345">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-345">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7672c-346">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7672c-346">Az.HealthcareApis</span></span>
* <span data-ttu-id="7672c-347">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-347">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="7672c-348">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-348">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-349">Az.Monitor</span></span>
* <span data-ttu-id="7672c-350">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-350">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="7672c-351">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="7672c-351">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-352">Az.Network</span></span>
* <span data-ttu-id="7672c-353">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-353">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="7672c-354">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-354">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="7672c-355">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="7672c-355">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="7672c-356">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-356">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="7672c-357">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-357">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="7672c-358">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="7672c-358">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="7672c-359">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="7672c-359">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="7672c-360">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="7672c-360">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="7672c-361">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="7672c-361">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="7672c-362">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="7672c-362">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="7672c-363">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-363">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="7672c-364">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-364">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="7672c-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="7672c-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="7672c-366">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="7672c-366">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="7672c-367">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-367">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="7672c-368">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-368">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="7672c-369">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-369">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="7672c-370">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-370">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="7672c-371">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-371">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="7672c-372">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="7672c-372">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="7672c-373">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-373">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="7672c-374">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-374">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="7672c-375">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-375">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="7672c-376">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-376">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="7672c-377">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-377">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="7672c-378">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-378">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="7672c-379">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="7672c-379">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="7672c-380">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-380">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="7672c-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7672c-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7672c-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7672c-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7672c-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="7672c-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="7672c-387">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-387">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="7672c-388">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="7672c-388">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="7672c-389">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="7672c-389">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="7672c-390">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="7672c-390">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="7672c-391">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="7672c-391">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="7672c-392">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="7672c-392">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="7672c-393">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-393">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="7672c-394">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="7672c-394">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="7672c-395">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="7672c-395">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="7672c-396">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="7672c-396">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7672c-397">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="7672c-397">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7672c-398">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="7672c-398">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="7672c-399">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="7672c-399">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="7672c-400">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="7672c-400">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="7672c-401">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="7672c-401">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-402">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-402">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-403">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="7672c-403">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="7672c-404">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-404">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="7672c-405">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-405">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="7672c-406">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="7672c-406">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="7672c-407">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="7672c-407">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-408">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-408">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-409">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-409">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="7672c-410">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="7672c-410">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-411">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-411">Az.Resources</span></span>
* <span data-ttu-id="7672c-412">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="7672c-412">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="7672c-413">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="7672c-413">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="7672c-414">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-414">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="7672c-415">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-415">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="7672c-416">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-416">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="7672c-417">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-417">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-418">Az.Sql</span></span>
* <span data-ttu-id="7672c-419">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-419">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="7672c-420">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-420">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="7672c-421">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="7672c-421">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-422">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-422">Az.Storage</span></span>
* <span data-ttu-id="7672c-423">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-423">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="7672c-424">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="7672c-424">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="7672c-425">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="7672c-425">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-426">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-426">Az.Websites</span></span>
* <span data-ttu-id="7672c-427">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-427">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7672c-428">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-428">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="7672c-429">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-429">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="7672c-430">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-430">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="7672c-431">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-431">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="7672c-432">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-432">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="7672c-433">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-433">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-434">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-434">Az.Accounts</span></span>
* <span data-ttu-id="7672c-435">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="7672c-435">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7672c-436">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7672c-436">Az.AnalysisServices</span></span>
* <span data-ttu-id="7672c-437">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-437">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7672c-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-438">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-439">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-439">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="7672c-440">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7672c-440">Az.Billing</span></span>
* <span data-ttu-id="7672c-441">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-441">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-442">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-442">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-443">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-443">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-444">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-445">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-445">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="7672c-446">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="7672c-446">Az.DataShare</span></span>
* <span data-ttu-id="7672c-447">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-447">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="7672c-448">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="7672c-448">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="7672c-449">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-449">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-450">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-450">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-451">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-451">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="7672c-452">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-452">Added optional parameters to</span></span> 
    - <span data-ttu-id="7672c-453">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="7672c-453">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="7672c-454">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="7672c-454">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7672c-455">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-455">Az.PolicyInsights</span></span>
* <span data-ttu-id="7672c-456">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-456">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7672c-457">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7672c-457">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7672c-458">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-458">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="7672c-459">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="7672c-459">Az.PrivateDns</span></span>
* <span data-ttu-id="7672c-460">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-460">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-461">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-461">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-462">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-462">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="7672c-463">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-463">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-464">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-464">Az.Resources</span></span>
* <span data-ttu-id="7672c-465">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-465">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="7672c-466">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="7672c-466">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="7672c-467">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-467">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="7672c-468">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-468">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="7672c-469">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-469">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-470">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-470">Az.Sql</span></span>
* <span data-ttu-id="7672c-471">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-471">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="7672c-472">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-472">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="7672c-473">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-473">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-474">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-474">Az.Storage</span></span>
* <span data-ttu-id="7672c-475">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-475">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="7672c-476">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-476">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="7672c-477">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7672c-477">Highlights since the last release</span></span>
* <span data-ttu-id="7672c-478">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="7672c-478">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="7672c-479">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-479">General availability of Az.Functions</span></span> 
* <span data-ttu-id="7672c-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="7672c-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-481">Az.Accounts</span></span>
* <span data-ttu-id="7672c-482">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-482">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="7672c-483">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="7672c-483">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="7672c-484">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7672c-484">Az.Aks</span></span>
* <span data-ttu-id="7672c-485">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-485">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="7672c-486">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-486">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="7672c-487">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="7672c-487">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7672c-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-488">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-489">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-489">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="7672c-490">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="7672c-490">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="7672c-491">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-491">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="7672c-492">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-492">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="7672c-493">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-493">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="7672c-494">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-494">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="7672c-495">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-495">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="7672c-496">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-496">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="7672c-497">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-497">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="7672c-498">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-498">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="7672c-499">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="7672c-499">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="7672c-500">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="7672c-500">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="7672c-501">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="7672c-501">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="7672c-502">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="7672c-502">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="7672c-503">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="7672c-503">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="7672c-504">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="7672c-504">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7672c-505">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-505">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7672c-506">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="7672c-506">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="7672c-507">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-507">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="7672c-508">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-508">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7672c-509">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7672c-509">Az.Batch</span></span>
* <span data-ttu-id="7672c-510">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-510">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="7672c-511">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-511">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="7672c-512">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-512">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="7672c-513">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-513">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="7672c-514">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="7672c-514">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="7672c-515">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-515">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="7672c-516">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-516">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="7672c-517">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="7672c-517">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="7672c-518">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-518">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-519">Az.Compute</span></span>
* <span data-ttu-id="7672c-520">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-520">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="7672c-521">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-521">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="7672c-522">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7672c-522">Breaking changes</span></span>
    - <span data-ttu-id="7672c-523">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-523">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="7672c-524">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-524">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="7672c-525">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-525">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="7672c-526">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-526">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="7672c-527">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-527">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="7672c-528">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-528">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="7672c-529">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-529">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-530">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-530">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-531">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-531">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7672c-532">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-532">Az.FrontDoor</span></span>
* <span data-ttu-id="7672c-533">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-533">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="7672c-534">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-534">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="7672c-535">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-535">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="7672c-536">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-536">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="7672c-537">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="7672c-537">Az.Functions</span></span>
* <span data-ttu-id="7672c-538">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-538">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-539">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-539">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-540">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="7672c-540">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7672c-541">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7672c-541">Az.HealthcareApis</span></span>
* <span data-ttu-id="7672c-542">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="7672c-542">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-543">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-543">Az.IotHub</span></span>
* <span data-ttu-id="7672c-544">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-544">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="7672c-545">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="7672c-545">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="7672c-546">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-546">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="7672c-547">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-547">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="7672c-548">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="7672c-548">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="7672c-549">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-549">New cmdlets are:</span></span>
    - <span data-ttu-id="7672c-550">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="7672c-550">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="7672c-551">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="7672c-551">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="7672c-552">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="7672c-552">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="7672c-553">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="7672c-553">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="7672c-554">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-554">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="7672c-555">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-555">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-556">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-556">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-557">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="7672c-557">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="7672c-558">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-558">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="7672c-559">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="7672c-559">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="7672c-560">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-560">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="7672c-561">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="7672c-561">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="7672c-562">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="7672c-562">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="7672c-563">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-563">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-564">Az.Monitor</span></span>
* <span data-ttu-id="7672c-565">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="7672c-565">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="7672c-566">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-566">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="7672c-567">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-567">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="7672c-568">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="7672c-568">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="7672c-569">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="7672c-569">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="7672c-570">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="7672c-570">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="7672c-571">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-571">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-572">Az.Network</span></span>
* <span data-ttu-id="7672c-573">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-573">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="7672c-574">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="7672c-574">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="7672c-575">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="7672c-575">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="7672c-576">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="7672c-576">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="7672c-577">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-577">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="7672c-578">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-578">New cmdlets added:</span></span>
        - <span data-ttu-id="7672c-579">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7672c-579">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="7672c-580">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7672c-580">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="7672c-581">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7672c-581">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="7672c-582">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="7672c-582">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="7672c-583">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-583">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="7672c-584">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-584">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="7672c-585">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-585">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="7672c-586">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="7672c-586">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="7672c-587">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="7672c-587">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="7672c-588">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-588">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="7672c-589">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="7672c-589">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="7672c-590">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="7672c-590">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="7672c-591">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="7672c-591">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="7672c-592">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="7672c-592">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="7672c-593">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="7672c-593">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="7672c-594">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-594">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="7672c-595">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-595">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="7672c-596">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="7672c-597">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7672c-597">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-598">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-598">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-599">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-599">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="7672c-600">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-600">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="7672c-601">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="7672c-601">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="7672c-602">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="7672c-602">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="7672c-603">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="7672c-603">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="7672c-604">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-604">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="7672c-605">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-605">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="7672c-606">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-606">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-608">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-608">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="7672c-609">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-609">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="7672c-610">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-610">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="7672c-611">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-611">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="7672c-612">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-612">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-613">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-613">Az.Resources</span></span>
* <span data-ttu-id="7672c-614">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-614">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="7672c-615">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-615">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="7672c-616">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="7672c-616">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="7672c-617">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="7672c-617">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="7672c-618">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="7672c-618">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="7672c-619">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="7672c-619">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="7672c-620">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="7672c-620">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="7672c-621">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="7672c-621">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="7672c-622">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-622">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="7672c-623">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-623">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="7672c-624">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-624">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="7672c-625">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-625">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="7672c-626">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-626">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="7672c-627">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-627">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="7672c-628">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-628">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="7672c-629">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-629">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="7672c-630">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="7672c-630">'New-AzDeployment'</span></span>
    - <span data-ttu-id="7672c-631">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="7672c-631">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="7672c-632">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="7672c-632">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7672c-633">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="7672c-633">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7672c-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-635">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-635">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-636">Az.Sql</span></span>
* <span data-ttu-id="7672c-637">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-637">Enhance performance of:</span></span>
    - <span data-ttu-id="7672c-638">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="7672c-638">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="7672c-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="7672c-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="7672c-640">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="7672c-640">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="7672c-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="7672c-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="7672c-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="7672c-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="7672c-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="7672c-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="7672c-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="7672c-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="7672c-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="7672c-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="7672c-646">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-646">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="7672c-647">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-647">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-648">Az.Storage</span></span>
* <span data-ttu-id="7672c-649">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-649">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="7672c-650">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-650">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="7672c-651">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="7672c-651">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="7672c-652">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-652">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="7672c-653">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="7672c-653">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="7672c-654">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-654">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="7672c-655">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="7672c-655">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="7672c-656">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="7672c-656">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="7672c-657">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="7672c-657">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="7672c-658">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="7672c-658">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="7672c-659">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-659">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="7672c-660">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="7672c-660">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="7672c-661">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="7672c-661">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="7672c-662">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-662">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="7672c-663">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="7672c-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="7672c-664">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="7672c-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="7672c-665">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-665">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="7672c-666">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="7672c-666">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="7672c-667">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="7672c-667">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7672c-668">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-668">Supported failover Storage account</span></span>
    - <span data-ttu-id="7672c-669">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="7672c-669">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="7672c-670">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-670">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="7672c-671">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-671">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="7672c-672">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-672">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="7672c-673">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="7672c-673">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="7672c-674">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="7672c-674">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="7672c-675">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="7672c-675">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="7672c-676">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="7672c-676">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="7672c-677">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="7672c-677">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="7672c-678">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="7672c-678">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="7672c-679">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="7672c-679">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="7672c-680">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="7672c-680">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="7672c-681">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="7672c-681">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="7672c-682">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="7672c-682">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="7672c-683">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="7672c-683">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="7672c-684">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="7672c-684">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="7672c-685">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="7672c-685">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="7672c-686">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="7672c-686">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="7672c-687">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="7672c-687">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7672c-688">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7672c-688">Az.TrafficManager</span></span>
* <span data-ttu-id="7672c-689">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-689">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-690">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-690">Az.Websites</span></span>
* <span data-ttu-id="7672c-691">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-691">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="7672c-692">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-692">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="7672c-693">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7672c-693">Highlights since the last release</span></span>
* <span data-ttu-id="7672c-694">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="7672c-694">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-695">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-695">Az.Accounts</span></span>
* <span data-ttu-id="7672c-696">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="7672c-696">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7672c-697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-697">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-698">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-698">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="7672c-699">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-699">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7672c-700">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7672c-700">Az.Cdn</span></span>
* <span data-ttu-id="7672c-701">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-701">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-702">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-702">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-703">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="7672c-703">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-704">Az.Compute</span></span>
* <span data-ttu-id="7672c-705">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-705">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="7672c-706">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-706">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-707">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-707">Az.IotHub</span></span>
* <span data-ttu-id="7672c-708">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-708">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="7672c-709">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="7672c-709">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="7672c-710">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="7672c-710">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="7672c-711">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-711">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="7672c-712">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-712">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="7672c-713">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="7672c-713">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="7672c-714">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="7672c-714">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="7672c-715">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="7672c-715">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="7672c-716">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-716">New cmdlets are:</span></span>
    - <span data-ttu-id="7672c-717">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-717">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="7672c-718">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-718">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="7672c-719">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-719">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="7672c-720">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="7672c-720">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="7672c-721">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-721">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-722">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-722">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-723">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-723">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="7672c-724">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="7672c-724">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="7672c-725">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="7672c-725">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="7672c-726">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-726">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="7672c-727">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="7672c-727">Az.Maintenance</span></span>
* <span data-ttu-id="7672c-728">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="7672c-728">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-729">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-729">Az.Monitor</span></span>
* <span data-ttu-id="7672c-730">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-730">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="7672c-731">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="7672c-731">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="7672c-732">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="7672c-732">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="7672c-733">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="7672c-733">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="7672c-734">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="7672c-734">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="7672c-735">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="7672c-735">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="7672c-736">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="7672c-736">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="7672c-737">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="7672c-737">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-738">Az.Network</span></span>
* <span data-ttu-id="7672c-739">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-739">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="7672c-740">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="7672c-740">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="7672c-741">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="7672c-741">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="7672c-742">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="7672c-742">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="7672c-743">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="7672c-743">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="7672c-744">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-744">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="7672c-745">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="7672c-745">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="7672c-746">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="7672c-746">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="7672c-747">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-747">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="7672c-748">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-748">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="7672c-749">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="7672c-749">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="7672c-750">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-750">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="7672c-751">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-751">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="7672c-752">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-752">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="7672c-753">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-753">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="7672c-754">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-754">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7672c-755">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-755">Az.PolicyInsights</span></span>
* <span data-ttu-id="7672c-756">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-756">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="7672c-757">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-757">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7672c-758">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-758">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-759">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-759">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-760">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-760">Az.Sql</span></span>
* <span data-ttu-id="7672c-761">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-761">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="7672c-762">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-762">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-763">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-763">Az.Storage</span></span>
* <span data-ttu-id="7672c-764">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-764">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="7672c-765">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-765">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="7672c-766">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="7672c-766">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="7672c-767">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="7672c-767">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="7672c-768">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-768">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="7672c-769">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="7672c-769">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="7672c-770">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="7672c-770">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="7672c-771">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="7672c-771">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="7672c-772">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="7672c-772">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="7672c-773">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="7672c-773">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="7672c-774">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="7672c-774">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="7672c-775">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="7672c-775">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="7672c-776">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="7672c-776">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="7672c-777">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-777">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="7672c-778">Genel</span><span class="sxs-lookup"><span data-stu-id="7672c-778">General</span></span>
* <span data-ttu-id="7672c-779">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-779">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="7672c-780">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="7672c-780">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="7672c-781">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7672c-781">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="7672c-782">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="7672c-782">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="7672c-783">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7672c-783">Az.Billing</span></span>
  - <span data-ttu-id="7672c-784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-784">Az.Compute</span></span>
  - <span data-ttu-id="7672c-785">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7672c-785">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="7672c-786">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7672c-786">Az.EventHub</span></span>
  - <span data-ttu-id="7672c-787">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-787">Az.IotHub</span></span>
  - <span data-ttu-id="7672c-788">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-788">Az.KeyVault</span></span>
  - <span data-ttu-id="7672c-789">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-789">Az.Monitor</span></span>
  - <span data-ttu-id="7672c-790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-790">Az.Network</span></span>
  - <span data-ttu-id="7672c-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-791">Az.Resources</span></span>
  - <span data-ttu-id="7672c-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-792">Az.Storage</span></span>
  - <span data-ttu-id="7672c-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-793">Az.Websites</span></span>
* <span data-ttu-id="7672c-794">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-794">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="7672c-795">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="7672c-795">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="7672c-796">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="7672c-796">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="7672c-797">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-797">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-798">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-798">Az.Accounts</span></span>
* <span data-ttu-id="7672c-799">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="7672c-799">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-800">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-800">Az.Compute</span></span>
* <span data-ttu-id="7672c-801">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-801">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="7672c-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="7672c-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="7672c-803">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-803">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="7672c-804">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-804">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="7672c-805">[#11354]</span><span class="sxs-lookup"><span data-stu-id="7672c-805">[#11354]</span></span>
* <span data-ttu-id="7672c-806">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-806">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="7672c-807">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="7672c-807">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="7672c-808">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="7672c-808">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="7672c-809">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="7672c-809">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="7672c-810">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="7672c-810">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="7672c-811">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-811">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="7672c-812">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-812">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="7672c-813">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-813">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="7672c-814">[#11257]</span><span class="sxs-lookup"><span data-stu-id="7672c-814">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-815">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-816">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-816">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="7672c-817">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-817">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-818">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-818">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-819">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-819">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="7672c-820">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-820">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-821">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-821">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-822">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-822">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-823">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-823">Az.IotHub</span></span>
* <span data-ttu-id="7672c-824">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-824">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="7672c-825">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-825">New Cmdlets are:</span></span>
    - <span data-ttu-id="7672c-826">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="7672c-826">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="7672c-827">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="7672c-827">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-828">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-828">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-829">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-829">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-830">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-830">Az.Monitor</span></span>
* <span data-ttu-id="7672c-831">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-831">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-832">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-832">Az.Network</span></span>
* <span data-ttu-id="7672c-833">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-833">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="7672c-834">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="7672c-834">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7672c-835">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="7672c-835">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="7672c-836">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="7672c-836">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="7672c-837">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="7672c-837">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="7672c-838">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-838">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7672c-839">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-839">Az.PolicyInsights</span></span>
* <span data-ttu-id="7672c-840">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-840">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-841">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-841">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-842">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-842">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="7672c-843">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-843">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="7672c-844">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-844">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="7672c-845">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-845">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="7672c-846">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-846">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="7672c-847">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-847">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-848">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-848">Az.Resources</span></span>
* <span data-ttu-id="7672c-849">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="7672c-849">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="7672c-850">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-850">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="7672c-851">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-851">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="7672c-852">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-852">Added example.</span></span>
* <span data-ttu-id="7672c-853">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="7672c-853">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="7672c-854">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="7672c-854">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-855">Az.Sql</span></span>
* <span data-ttu-id="7672c-856">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-856">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="7672c-857">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-857">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="7672c-858">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-858">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="7672c-859">Az.Support</span><span class="sxs-lookup"><span data-stu-id="7672c-859">Az.Support</span></span>
* <span data-ttu-id="7672c-860">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-860">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-861">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-861">Az.Websites</span></span>
* <span data-ttu-id="7672c-862">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-862">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="7672c-863">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="7672c-863">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="7672c-864">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="7672c-864">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="7672c-865">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="7672c-865">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="7672c-866">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="7672c-866">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="7672c-867">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-867">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-868">Az.Accounts</span></span>
* <span data-ttu-id="7672c-869">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="7672c-869">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="7672c-870">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="7672c-870">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="7672c-871">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-871">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7672c-872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-872">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-873">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="7672c-873">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="7672c-874">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="7672c-874">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="7672c-875">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-875">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="7672c-876">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="7672c-876">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-877">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-877">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-878">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-878">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-879">Az.IotHub</span></span>
* <span data-ttu-id="7672c-880">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-880">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="7672c-881">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-881">New Cmdlets are:</span></span>
    - <span data-ttu-id="7672c-882">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="7672c-882">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7672c-883">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="7672c-883">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7672c-884">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="7672c-884">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7672c-885">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="7672c-885">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="7672c-886">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-886">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="7672c-887">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-887">New Cmdlets are:</span></span>
    - <span data-ttu-id="7672c-888">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="7672c-888">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="7672c-889">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="7672c-889">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="7672c-890">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="7672c-890">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="7672c-891">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="7672c-891">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="7672c-892">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-892">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="7672c-893">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-893">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="7672c-894">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-894">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="7672c-895">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-895">New Cmdlets are:</span></span>
    - <span data-ttu-id="7672c-896">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="7672c-896">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="7672c-897">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="7672c-897">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="7672c-898">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-898">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-899">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-899">Az.Monitor</span></span>
* <span data-ttu-id="7672c-900">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="7672c-900">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-901">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-901">Az.Network</span></span>
* <span data-ttu-id="7672c-902">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-902">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="7672c-903">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-903">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="7672c-904">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-904">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="7672c-905">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-905">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-906">Az.Resources</span></span>
* <span data-ttu-id="7672c-907">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-907">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="7672c-908">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="7672c-908">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="7672c-909">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="7672c-909">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="7672c-910">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="7672c-910">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="7672c-911">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-911">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="7672c-912">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-912">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="7672c-913">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-913">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="7672c-914">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="7672c-914">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="7672c-915">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7672c-915">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="7672c-916">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7672c-916">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="7672c-917">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7672c-917">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="7672c-918">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-918">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="7672c-919">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="7672c-919">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="7672c-920">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-920">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-921">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-921">Az.Sql</span></span>
* <span data-ttu-id="7672c-922">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-922">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="7672c-923">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-923">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="7672c-924">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="7672c-924">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="7672c-925">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="7672c-925">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="7672c-926">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="7672c-926">Remove an LTR backup</span></span>
    - <span data-ttu-id="7672c-927">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="7672c-927">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="7672c-928">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-928">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="7672c-929">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-929">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="7672c-930">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-930">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-931">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-931">Az.Storage</span></span>
* <span data-ttu-id="7672c-932">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-932">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="7672c-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="7672c-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="7672c-934">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-934">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="7672c-935">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="7672c-935">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="7672c-936">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="7672c-936">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-937">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-937">Az.Websites</span></span>
* <span data-ttu-id="7672c-938">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-938">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="7672c-939">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="7672c-939">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="7672c-940">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-940">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="7672c-941">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="7672c-941">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="7672c-942">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-942">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="7672c-943">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-943">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7672c-944">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7672c-944">Highlights since the last major release</span></span>
* <span data-ttu-id="7672c-945">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-945">Updated client side telemetry.</span></span>
* <span data-ttu-id="7672c-946">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-946">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="7672c-947">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-947">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-948">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-948">Az.Accounts</span></span>
* <span data-ttu-id="7672c-949">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-949">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-950">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-950">Az.Automation</span></span>
* <span data-ttu-id="7672c-951">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-951">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-952">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-952">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-953">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-953">Updated SDK to 7.0</span></span>
* <span data-ttu-id="7672c-954">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-954">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-955">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-955">Az.Compute</span></span>
* <span data-ttu-id="7672c-956">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="7672c-956">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7672c-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-957">Az.FrontDoor</span></span>
* <span data-ttu-id="7672c-958">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-958">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-959">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-959">Az.IotHub</span></span>
* <span data-ttu-id="7672c-960">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-960">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="7672c-961">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-961">New Cmdlets are:</span></span>
    - <span data-ttu-id="7672c-962">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="7672c-962">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7672c-963">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="7672c-963">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7672c-964">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="7672c-964">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="7672c-965">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="7672c-965">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-966">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-967">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-967">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-968">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-968">Az.Monitor</span></span>
* <span data-ttu-id="7672c-969">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-969">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="7672c-970">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-970">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="7672c-971">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-971">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-972">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-972">Az.Network</span></span>
* <span data-ttu-id="7672c-973">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-973">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="7672c-974">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-974">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7672c-975">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-975">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="7672c-976">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="7672c-976">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="7672c-977">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="7672c-977">No new cmdlets are added.</span></span> <span data-ttu-id="7672c-978">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="7672c-978">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-980">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-980">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-981">Az.Resources</span></span>
* <span data-ttu-id="7672c-982">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="7672c-982">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="7672c-983">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7672c-983">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="7672c-984">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7672c-984">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="7672c-985">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="7672c-985">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="7672c-986">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-986">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="7672c-987">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-987">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="7672c-988">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-988">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="7672c-989">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-989">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-990">Az.Sql</span></span>
* <span data-ttu-id="7672c-991">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-991">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="7672c-992">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-992">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="7672c-993">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="7672c-993">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7672c-994">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7672c-994">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7672c-995">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-995">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7672c-996">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7672c-996">Az.StorageSync</span></span>
* <span data-ttu-id="7672c-997">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-997">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="7672c-998">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-998">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7672c-999">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7672c-999">Highlights since the last major release</span></span>
* <span data-ttu-id="7672c-1000">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="7672c-1000">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="7672c-1001">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1001">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-1002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-1002">Az.Accounts</span></span>
* <span data-ttu-id="7672c-1003">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7672c-1003">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="7672c-1004">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1004">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7672c-1005">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-1005">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-1006">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="7672c-1006">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="7672c-1007">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="7672c-1007">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="7672c-1008">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1008">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="7672c-1009">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1009">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1010">Az.Compute</span></span>
* <span data-ttu-id="7672c-1011">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="7672c-1011">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="7672c-1012">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1012">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="7672c-1013">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1013">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="7672c-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="7672c-1015">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1015">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1016">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1016">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1017">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1017">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7672c-1018">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7672c-1018">Az.DeploymentManager</span></span>
* <span data-ttu-id="7672c-1019">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="7672c-1019">Adds LIST operations for resources</span></span>
* <span data-ttu-id="7672c-1020">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="7672c-1020">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-1021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-1021">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-1022">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1022">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-1023">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-1023">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-1024">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1024">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1025">Az.Network</span></span>
* <span data-ttu-id="7672c-1026">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1026">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="7672c-1027">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="7672c-1027">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="7672c-1028">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1028">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7672c-1029">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1029">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="7672c-1030">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="7672c-1030">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="7672c-1031">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1031">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="7672c-1032">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1032">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="7672c-1033">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1033">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="7672c-1034">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1034">New cmdlets added:</span></span>
        - <span data-ttu-id="7672c-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="7672c-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="7672c-1036">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1036">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="7672c-1037">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7672c-1037">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="7672c-1038">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1038">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7672c-1039">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-1039">Az.PolicyInsights</span></span>
* <span data-ttu-id="7672c-1040">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="7672c-1040">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="7672c-1041">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1041">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="7672c-1042">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1042">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="7672c-1043">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1043">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-1044">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1044">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-1045">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1045">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="7672c-1046">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1046">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1047">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1047">Az.Resources</span></span>
* <span data-ttu-id="7672c-1048">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1048">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="7672c-1049">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1049">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1050">Az.Sql</span></span>
<span data-ttu-id="7672c-1051">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1051">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1052">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1052">Az.Storage</span></span>
* <span data-ttu-id="7672c-1053">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="7672c-1053">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="7672c-1054">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-1054">New-AzStorageAccount</span></span>
* <span data-ttu-id="7672c-1055">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="7672c-1055">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="7672c-1056">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1056">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-1057">Az.Websites</span></span>
* <span data-ttu-id="7672c-1058">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="7672c-1058">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="7672c-1059">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1059">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="7672c-1060">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="7672c-1060">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-1061">Az.Accounts</span></span>
* <span data-ttu-id="7672c-1062">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1062">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7672c-1063">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7672c-1063">Az.Cdn</span></span>
* <span data-ttu-id="7672c-1064">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="7672c-1064">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1065">Az.Compute</span></span>
* <span data-ttu-id="7672c-1066">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1066">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7672c-1067">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7672c-1067">Az.ContainerInstance</span></span>
* <span data-ttu-id="7672c-1068">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1068">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7672c-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7672c-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7672c-1070">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1070">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7672c-1071">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="7672c-1071">Get the Edge Storage Container</span></span>
* <span data-ttu-id="7672c-1072">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1072">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7672c-1073">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7672c-1073">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="7672c-1074">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1074">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7672c-1075">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7672c-1075">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="7672c-1076">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1076">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7672c-1077">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="7672c-1077">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="7672c-1078">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1078">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7672c-1079">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="7672c-1079">Get the Edge Storage Account</span></span>
* <span data-ttu-id="7672c-1080">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1080">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7672c-1081">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="7672c-1081">Create new Edge Storage Account</span></span>
* <span data-ttu-id="7672c-1082">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1082">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7672c-1083">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7672c-1083">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="7672c-1084">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="7672c-1084">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="7672c-1085">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="7672c-1085">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="7672c-1086">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1086">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="7672c-1087">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7672c-1087">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1088">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1089">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1089">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="7672c-1090">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1090">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="7672c-1091">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1091">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="7672c-1092">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="7672c-1092">Az.DevTestLabs</span></span>
* <span data-ttu-id="7672c-1093">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1093">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7672c-1094">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1094">Az.EventHub</span></span>
* <span data-ttu-id="7672c-1095">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1095">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-1096">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-1096">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-1097">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1097">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7672c-1098">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7672c-1098">Az.MachineLearning</span></span>
* <span data-ttu-id="7672c-1099">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1099">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="7672c-1100">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7672c-1100">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="7672c-1101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="7672c-1101">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="7672c-1102">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7672c-1102">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="7672c-1103">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7672c-1103">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="7672c-1104">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7672c-1104">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="7672c-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="7672c-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="7672c-1106">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="7672c-1106">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1107">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1107">Az.Network</span></span>
* <span data-ttu-id="7672c-1108">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1108">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-1109">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1109">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-1110">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1110">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="7672c-1111">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1111">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7672c-1112">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1112">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7672c-1113">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1113">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1114">Az.Resources</span></span>
* <span data-ttu-id="7672c-1115">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1115">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1116">Az.Sql</span></span>
* <span data-ttu-id="7672c-1117">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1117">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="7672c-1118">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1118">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7672c-1119">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7672c-1119">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7672c-1120">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1120">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1121">Az.Storage</span></span>
* <span data-ttu-id="7672c-1122">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1122">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="7672c-1123">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7672c-1123">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="7672c-1124">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="7672c-1124">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="7672c-1125">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-1125">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="7672c-1126">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1126">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="7672c-1127">Genel</span><span class="sxs-lookup"><span data-stu-id="7672c-1127">General</span></span>
* <span data-ttu-id="7672c-1128">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1128">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-1129">Az.Accounts</span></span>
* <span data-ttu-id="7672c-1130">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="7672c-1130">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="7672c-1131">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="7672c-1131">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7672c-1132">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7672c-1132">Az.Batch</span></span>
* <span data-ttu-id="7672c-1133">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1133">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1134">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1134">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1135">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1135">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7672c-1136">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-1136">Az.FrontDoor</span></span>
* <span data-ttu-id="7672c-1137">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1137">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="7672c-1138">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1138">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7672c-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7672c-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="7672c-1140">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="7672c-1140">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-1141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-1141">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-1142">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1142">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="7672c-1143">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="7672c-1143">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="7672c-1144">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1144">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-1145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-1145">Az.Monitor</span></span>
* <span data-ttu-id="7672c-1146">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1146">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="7672c-1147">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="7672c-1147">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="7672c-1148">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="7672c-1148">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1149">Az.Network</span></span>
* <span data-ttu-id="7672c-1150">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1150">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1151">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1151">Az.Resources</span></span>
* <span data-ttu-id="7672c-1152">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1152">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="7672c-1153">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1153">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1154">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1154">Az.Sql</span></span>
* <span data-ttu-id="7672c-1155">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1155">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1156">Az.Storage</span></span>
* <span data-ttu-id="7672c-1157">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-1157">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="7672c-1158">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="7672c-1158">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="7672c-1159">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7672c-1159">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="7672c-1160">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-1160">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="7672c-1161">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="7672c-1161">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="7672c-1162">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1162">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="7672c-1163">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1163">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="7672c-1164">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7672c-1164">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="7672c-1165">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7672c-1165">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="7672c-1166">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1166">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="7672c-1167">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="7672c-1167">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="7672c-1168">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1168">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="7672c-1169">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="7672c-1169">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="7672c-1170">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1170">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7672c-1171">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7672c-1171">Highlights since the last major release</span></span>
* <span data-ttu-id="7672c-1172">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="7672c-1172">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="7672c-1173">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="7672c-1173">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1174">Az.Compute</span></span>
* <span data-ttu-id="7672c-1175">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="7672c-1175">VM Reapply feature</span></span>
    - <span data-ttu-id="7672c-1176">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="7672c-1176">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="7672c-1177">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="7672c-1177">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="7672c-1178">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7672c-1178">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="7672c-1179">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-1179">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="7672c-1180">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1180">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7672c-1181">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1181">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="7672c-1182">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1182">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="7672c-1183">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1183">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="7672c-1184">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1184">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="7672c-1185">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1185">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7672c-1186">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7672c-1186">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7672c-1187">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1187">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7672c-1188">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="7672c-1188">Get the Order</span></span>
* <span data-ttu-id="7672c-1189">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1189">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7672c-1190">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="7672c-1190">Create new Order</span></span>
* <span data-ttu-id="7672c-1191">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1191">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7672c-1192">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="7672c-1192">Remove the Order</span></span>
* <span data-ttu-id="7672c-1193">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="7672c-1193">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="7672c-1194">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="7672c-1194">Now creates Local Share</span></span>
* <span data-ttu-id="7672c-1195">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1195">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="7672c-1196">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="7672c-1196">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="7672c-1197">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1197">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="7672c-1198">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="7672c-1198">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="7672c-1199">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1199">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7672c-1200">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="7672c-1200">Gets the information about Triggers</span></span>
* <span data-ttu-id="7672c-1201">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1201">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7672c-1202">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="7672c-1202">Create new Triggers</span></span>
* <span data-ttu-id="7672c-1203">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1203">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7672c-1204">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="7672c-1204">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1205">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1206">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1206">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="7672c-1207">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1207">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-1208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-1208">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-1209">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1209">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7672c-1210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1210">Az.EventHub</span></span>
* <span data-ttu-id="7672c-1211">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1211">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7672c-1212">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-1212">Az.FrontDoor</span></span>
* <span data-ttu-id="7672c-1213">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1213">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="7672c-1214">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1214">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="7672c-1215">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1215">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="7672c-1216">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="7672c-1216">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1217">Az.Network</span></span>
* <span data-ttu-id="7672c-1218">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1218">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="7672c-1219">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="7672c-1219">Az.PrivateDns</span></span>
* <span data-ttu-id="7672c-1220">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1220">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-1222">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1222">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="7672c-1223">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1223">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="7672c-1224">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1224">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7672c-1225">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7672c-1225">Az.RedisCache</span></span>
* <span data-ttu-id="7672c-1226">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1226">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="7672c-1227">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1227">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="7672c-1228">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1228">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1229">Az.Resources</span></span>
- <span data-ttu-id="7672c-1230">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1230">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="7672c-1231">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1231">Updated create policy definition help example</span></span>
- <span data-ttu-id="7672c-1232">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1232">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="7672c-1233">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1233">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="7672c-1234">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1234">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1235">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1235">Az.Sql</span></span>
* <span data-ttu-id="7672c-1236">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1236">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="7672c-1237">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1237">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="7672c-1238">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1238">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="7672c-1239">Genel</span><span class="sxs-lookup"><span data-stu-id="7672c-1239">General</span></span>
* <span data-ttu-id="7672c-1240">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="7672c-1240">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-1241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-1241">Az.Accounts</span></span>
* <span data-ttu-id="7672c-1242">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7672c-1242">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7672c-1243">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7672c-1243">Az.Advisor</span></span>
* <span data-ttu-id="7672c-1244">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1244">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7672c-1245">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7672c-1245">Az.Batch</span></span>
* <span data-ttu-id="7672c-1246">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1246">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="7672c-1247">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="7672c-1247">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="7672c-1248">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1248">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="7672c-1249">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1249">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="7672c-1250">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="7672c-1250">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="7672c-1251">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-1251">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="7672c-1252">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="7672c-1252">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="7672c-1253">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1253">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="7672c-1254">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1254">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="7672c-1255">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1255">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7672c-1256">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-1256">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="7672c-1257">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="7672c-1257">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="7672c-1258">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1258">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7672c-1259">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="7672c-1259">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="7672c-1260">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1260">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="7672c-1261">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1261">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="7672c-1262">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1262">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="7672c-1263">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1263">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="7672c-1264">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1264">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="7672c-1265">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1265">This operation is no longer supported.</span></span>
* <span data-ttu-id="7672c-1266">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1266">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7672c-1267">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1267">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7672c-1268">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1268">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="7672c-1269">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1269">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="7672c-1270">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1270">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="7672c-1271">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1271">New non-verified images are also now returned.</span></span> <span data-ttu-id="7672c-1272">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1272">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="7672c-1273">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1273">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="7672c-1274">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1274">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="7672c-1275">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1275">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="7672c-1276">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1276">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="7672c-1277">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1277">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="7672c-1278">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1278">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="7672c-1279">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1279">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="7672c-1280">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="7672c-1280">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="7672c-1281">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="7672c-1281">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7672c-1282">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7672c-1282">Az.Cdn</span></span>
* <span data-ttu-id="7672c-1283">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1283">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="7672c-1284">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1284">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1285">Az.Compute</span></span>
* <span data-ttu-id="7672c-1286">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="7672c-1286">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="7672c-1287">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7672c-1287">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="7672c-1288">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7672c-1288">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="7672c-1289">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1289">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7672c-1290">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1290">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="7672c-1291">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="7672c-1291">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="7672c-1292">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1292">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="7672c-1293">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7672c-1293">Breaking changes</span></span>
    - <span data-ttu-id="7672c-1294">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="7672c-1294">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="7672c-1295">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="7672c-1295">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1296">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1296">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1297">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1297">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-1298">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-1298">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-1299">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="7672c-1299">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="7672c-1300">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="7672c-1300">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="7672c-1301">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="7672c-1301">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="7672c-1302">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="7672c-1302">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="7672c-1303">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="7672c-1303">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="7672c-1304">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="7672c-1304">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7672c-1305">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-1305">Az.FrontDoor</span></span>
* <span data-ttu-id="7672c-1306">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1306">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-1307">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-1308">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1308">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="7672c-1309">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1309">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="7672c-1310">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1310">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="7672c-1311">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="7672c-1311">Removed five cmdlets:</span></span>
    - <span data-ttu-id="7672c-1312">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7672c-1312">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7672c-1313">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7672c-1313">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7672c-1314">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7672c-1314">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7672c-1315">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7672c-1315">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="7672c-1316">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7672c-1316">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="7672c-1317">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1317">Added three cmdlets:</span></span>
    - <span data-ttu-id="7672c-1318">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="7672c-1318">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7672c-1319">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="7672c-1319">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7672c-1320">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="7672c-1320">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="7672c-1321">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1321">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="7672c-1322">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1322">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="7672c-1323">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1323">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="7672c-1324">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1324">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="7672c-1325">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1325">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="7672c-1326">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1326">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="7672c-1327">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1327">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="7672c-1328">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1328">Added some scenario test cases.</span></span>
* <span data-ttu-id="7672c-1329">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="7672c-1329">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-1330">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1330">Az.IotHub</span></span>
* <span data-ttu-id="7672c-1331">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="7672c-1331">Breaking changes:</span></span>
    - <span data-ttu-id="7672c-1332">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1332">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7672c-1333">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1333">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7672c-1334">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1334">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7672c-1335">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1335">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7672c-1336">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1336">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="7672c-1337">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1337">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="7672c-1338">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1338">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="7672c-1339">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1339">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="7672c-1340">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1340">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7672c-1341">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1341">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7672c-1342">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1342">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7672c-1343">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1343">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-1344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1344">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-1345">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1345">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="7672c-1346">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1346">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="7672c-1347">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1347">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="7672c-1348">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1348">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="7672c-1349">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1349">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="7672c-1350">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1350">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="7672c-1351">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1351">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="7672c-1352">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1352">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="7672c-1353">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1353">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1354">Az.Resources</span></span>
* <span data-ttu-id="7672c-1355">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1355">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1356">Az.Network</span></span>
* <span data-ttu-id="7672c-1357">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1357">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="7672c-1358">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1358">Updated cmdlet:</span></span>
        - <span data-ttu-id="7672c-1359">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1359">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7672c-1360">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1360">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7672c-1361">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1361">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7672c-1362">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1362">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7672c-1363">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1363">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7672c-1364">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1364">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="7672c-1365">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7672c-1365">New cmdlet:</span></span>
        - <span data-ttu-id="7672c-1366">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7672c-1366">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="7672c-1367">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1367">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="7672c-1368">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1368">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="7672c-1369">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1369">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="7672c-1370">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1370">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="7672c-1371">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1371">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="7672c-1372">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1372">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="7672c-1373">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1373">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="7672c-1374">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1374">New cmdlets added:</span></span>
        - <span data-ttu-id="7672c-1375">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7672c-1375">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="7672c-1376">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7672c-1376">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7672c-1377">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7672c-1377">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7672c-1378">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7672c-1378">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7672c-1379">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1379">Set-AzVirtualHub</span></span>
* <span data-ttu-id="7672c-1380">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1380">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="7672c-1381">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7672c-1382">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1382">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7672c-1383">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1383">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7672c-1384">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1384">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="7672c-1385">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1385">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="7672c-1386">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1386">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="7672c-1387">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1387">New cmdlets added:</span></span>
        - <span data-ttu-id="7672c-1388">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1388">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="7672c-1389">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1389">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7672c-1390">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1390">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7672c-1391">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1391">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7672c-1392">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1392">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7672c-1393">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1393">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7672c-1394">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1394">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="7672c-1395">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1395">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="7672c-1396">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1396">New cmdlets added:</span></span>
        - <span data-ttu-id="7672c-1397">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="7672c-1397">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="7672c-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="7672c-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="7672c-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7672c-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="7672c-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7672c-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="7672c-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="7672c-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="7672c-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7672c-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="7672c-1403">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1403">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7672c-1404">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1404">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="7672c-1405">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1405">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="7672c-1406">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1406">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="7672c-1407">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1407">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="7672c-1408">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1408">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7672c-1409">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1409">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="7672c-1410">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1410">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="7672c-1411">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1411">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="7672c-1412">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="7672c-1412">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="7672c-1413">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1413">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="7672c-1414">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1414">New cmdlets added:</span></span>
        - <span data-ttu-id="7672c-1415">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7672c-1415">New-AzIpGroup</span></span>
        - <span data-ttu-id="7672c-1416">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7672c-1416">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="7672c-1417">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7672c-1417">Get-AzIpGroup</span></span>
        - <span data-ttu-id="7672c-1418">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7672c-1418">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7672c-1419">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-1419">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-1420">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1420">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1421">Az.Sql</span></span>
* <span data-ttu-id="7672c-1422">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1422">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="7672c-1423">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1423">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="7672c-1424">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="7672c-1424">Removed deprecated aliases:</span></span>
* <span data-ttu-id="7672c-1425">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="7672c-1425">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="7672c-1426">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="7672c-1426">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="7672c-1427">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1427">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7672c-1428">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1428">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="7672c-1429">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1429">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="7672c-1430">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1430">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1431">Az.Storage</span></span>
* <span data-ttu-id="7672c-1432">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-1432">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="7672c-1433">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-1433">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7672c-1434">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-1434">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7672c-1435">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="7672c-1435">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="7672c-1436">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7672c-1436">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="7672c-1437">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7672c-1437">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="7672c-1438">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1438">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="7672c-1439">Genel</span><span class="sxs-lookup"><span data-stu-id="7672c-1439">General</span></span>
* <span data-ttu-id="7672c-1440">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="7672c-1440">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-1441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-1441">Az.Accounts</span></span>
* <span data-ttu-id="7672c-1442">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1442">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7672c-1443">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-1443">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-1444">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1444">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="7672c-1445">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1445">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-1446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-1446">Az.Automation</span></span>
* <span data-ttu-id="7672c-1447">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1447">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7672c-1448">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7672c-1448">Az.Batch</span></span>
* <span data-ttu-id="7672c-1449">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="7672c-1449">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1450">Az.Compute</span></span>
* <span data-ttu-id="7672c-1451">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1451">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7672c-1452">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1452">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="7672c-1453">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1453">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="7672c-1454">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1454">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1455">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1456">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="7672c-1456">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="7672c-1457">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="7672c-1457">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="7672c-1458">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1458">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-1459">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-1459">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-1460">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1460">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7672c-1461">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7672c-1461">Az.HealthcareApis</span></span>
* <span data-ttu-id="7672c-1462">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1462">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="7672c-1463">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1463">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="7672c-1464">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1464">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="7672c-1465">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1465">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-1466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1466">Az.IotHub</span></span>
* <span data-ttu-id="7672c-1467">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="7672c-1467">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="7672c-1468">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="7672c-1468">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-1469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-1469">Az.Monitor</span></span>
* <span data-ttu-id="7672c-1470">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1470">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="7672c-1471">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="7672c-1471">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="7672c-1472">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="7672c-1472">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="7672c-1473">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1473">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1474">Az.Network</span></span>
* <span data-ttu-id="7672c-1475">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1475">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="7672c-1476">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1476">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="7672c-1477">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1477">New cmdlets added:</span></span>
        - <span data-ttu-id="7672c-1478">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="7672c-1478">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="7672c-1479">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1479">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7672c-1480">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1480">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="7672c-1481">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1481">Updated cmdlets:</span></span>
        - <span data-ttu-id="7672c-1482">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1482">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7672c-1483">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1483">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7672c-1484">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1484">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7672c-1485">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1485">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="7672c-1486">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="7672c-1486">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="7672c-1487">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="7672c-1487">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="7672c-1488">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="7672c-1488">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7672c-1489">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7672c-1489">Az.RedisCache</span></span>
* <span data-ttu-id="7672c-1490">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1490">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1491">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1491">Az.Sql</span></span>
* <span data-ttu-id="7672c-1492">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1492">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1493">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1493">Az.Storage</span></span>
* <span data-ttu-id="7672c-1494">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1494">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="7672c-1495">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="7672c-1495">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7672c-1496">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7672c-1496">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="7672c-1497">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="7672c-1497">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7672c-1498">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-1498">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7672c-1499">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7672c-1499">Az.StorageSync</span></span>
* <span data-ttu-id="7672c-1500">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1500">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-1501">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-1501">Az.Websites</span></span>
* <span data-ttu-id="7672c-1502">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="7672c-1502">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="7672c-1503">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1503">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7672c-1504">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-1504">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-1505">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1505">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="7672c-1506">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1506">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="7672c-1507">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="7672c-1507">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-1508">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-1508">Az.Automation</span></span>
* <span data-ttu-id="7672c-1509">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1509">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="7672c-1510">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1510">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="7672c-1511">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1511">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1512">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1512">Az.Compute</span></span>
* <span data-ttu-id="7672c-1513">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1513">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="7672c-1514">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1514">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7672c-1515">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1515">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="7672c-1516">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1516">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="7672c-1517">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1517">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="7672c-1518">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1518">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="7672c-1519">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1519">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="7672c-1520">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1520">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="7672c-1521">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1521">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1522">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1522">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1523">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="7672c-1523">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="7672c-1524">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1524">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-1525">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-1525">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-1526">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="7672c-1526">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-1527">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1527">Az.IotHub</span></span>
* <span data-ttu-id="7672c-1528">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1528">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="7672c-1529">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1529">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="7672c-1530">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7672c-1530">New cmdlets are:</span></span>
    - <span data-ttu-id="7672c-1531">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7672c-1531">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7672c-1532">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7672c-1532">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7672c-1533">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7672c-1533">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7672c-1534">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7672c-1534">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-1535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-1535">Az.Monitor</span></span>
* <span data-ttu-id="7672c-1536">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="7672c-1536">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="7672c-1537">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-1537">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="7672c-1538">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="7672c-1538">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="7672c-1539">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="7672c-1539">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="7672c-1540">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1540">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="7672c-1541">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1541">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="7672c-1542">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1542">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="7672c-1543">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="7672c-1543">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="7672c-1544">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1544">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7672c-1545">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="7672c-1545">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="7672c-1546">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1546">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7672c-1547">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="7672c-1547">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="7672c-1548">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1548">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="7672c-1549">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="7672c-1549">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="7672c-1550">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="7672c-1550">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="7672c-1551">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="7672c-1551">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="7672c-1552">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="7672c-1552">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="7672c-1553">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="7672c-1553">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="7672c-1554">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1554">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="7672c-1555">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1555">Overall improved help files</span></span>
* <span data-ttu-id="7672c-1556">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1556">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1557">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1557">Az.Network</span></span>
* <span data-ttu-id="7672c-1558">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1558">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="7672c-1559">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1559">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="7672c-1560">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1560">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="7672c-1561">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1561">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="7672c-1562">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1562">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="7672c-1563">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1563">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="7672c-1564">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1564">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="7672c-1565">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1565">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="7672c-1566">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1566">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="7672c-1567">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1567">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="7672c-1568">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1568">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="7672c-1569">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-1569">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="7672c-1570">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-1570">New cmdlets</span></span>
        - <span data-ttu-id="7672c-1571">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7672c-1571">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="7672c-1572">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1572">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="7672c-1573">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1573">Updated cmdlet:</span></span>
        - <span data-ttu-id="7672c-1574">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7672c-1574">New-VpnSite</span></span>
        - <span data-ttu-id="7672c-1575">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7672c-1575">Update-VpnSite</span></span>
        - <span data-ttu-id="7672c-1576">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1576">New-VpnConnection</span></span>
        - <span data-ttu-id="7672c-1577">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1577">Update-VpnConnection</span></span>
* <span data-ttu-id="7672c-1578">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1578">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-1579">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1579">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-1580">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1580">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="7672c-1581">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1581">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1582">Az.Resources</span></span>
* <span data-ttu-id="7672c-1583">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1583">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7672c-1584">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-1584">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-1585">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1585">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="7672c-1586">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="7672c-1586">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="7672c-1587">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7672c-1587">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7672c-1588">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7672c-1588">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7672c-1589">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7672c-1589">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7672c-1590">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7672c-1590">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="7672c-1591">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7672c-1591">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7672c-1592">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7672c-1592">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7672c-1593">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7672c-1593">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7672c-1594">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7672c-1594">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7672c-1595">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7672c-1595">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="7672c-1596">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7672c-1596">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7672c-1597">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7672c-1597">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7672c-1598">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7672c-1598">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7672c-1599">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="7672c-1599">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="7672c-1600">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1600">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7672c-1601">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7672c-1601">Az.SignalR</span></span>
* <span data-ttu-id="7672c-1602">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1602">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1603">Az.Sql</span></span>
* <span data-ttu-id="7672c-1604">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1604">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="7672c-1605">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1605">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="7672c-1606">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1606">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="7672c-1607">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1607">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="7672c-1608">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1608">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1609">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1609">Az.Storage</span></span>
* <span data-ttu-id="7672c-1610">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1610">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7672c-1611">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1611">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="7672c-1612">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7672c-1612">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="7672c-1613">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7672c-1613">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="7672c-1614">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1614">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="7672c-1615">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7672c-1615">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="7672c-1616">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1616">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="7672c-1617">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7672c-1617">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7672c-1618">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7672c-1618">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7672c-1619">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7672c-1619">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7672c-1620">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7672c-1620">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-1621">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-1621">Az.Websites</span></span>
* <span data-ttu-id="7672c-1622">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="7672c-1622">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="7672c-1623">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="7672c-1623">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="7672c-1624">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1624">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="7672c-1625">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1625">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="7672c-1626">Genel</span><span class="sxs-lookup"><span data-stu-id="7672c-1626">General</span></span>
* <span data-ttu-id="7672c-1627">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1627">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-1628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-1628">Az.Accounts</span></span>
* <span data-ttu-id="7672c-1629">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="7672c-1629">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="7672c-1630">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7672c-1630">Az.Aks</span></span>
* <span data-ttu-id="7672c-1631">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1631">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="7672c-1632">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="7672c-1632">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7672c-1633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-1633">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-1634">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1634">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="7672c-1635">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1635">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="7672c-1636">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1636">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="7672c-1637">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="7672c-1637">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="7672c-1638">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1638">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7672c-1639">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7672c-1639">Az.Batch</span></span>
* <span data-ttu-id="7672c-1640">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1640">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7672c-1641">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7672c-1641">Az.Cdn</span></span>
* <span data-ttu-id="7672c-1642">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1642">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1643">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1643">Az.Compute</span></span>
* <span data-ttu-id="7672c-1644">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1644">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="7672c-1645">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1645">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="7672c-1646">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1646">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="7672c-1647">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1647">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="7672c-1648">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="7672c-1648">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="7672c-1649">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1649">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="7672c-1650">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1650">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="7672c-1651">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1651">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1652">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1653">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1653">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="7672c-1654">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1654">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="7672c-1655">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1655">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="7672c-1656">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1656">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-1657">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-1658">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1658">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7672c-1659">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1659">Az.EventHub</span></span>
* <span data-ttu-id="7672c-1660">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="7672c-1660">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="7672c-1661">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="7672c-1661">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="7672c-1662">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1662">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="7672c-1663">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="7672c-1663">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="7672c-1664">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7672c-1664">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7672c-1665">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1665">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-1666">Az.Monitor</span></span>
* <span data-ttu-id="7672c-1667">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1667">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1668">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1668">Az.Network</span></span>
* <span data-ttu-id="7672c-1669">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1669">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="7672c-1670">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1670">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="7672c-1671">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1671">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="7672c-1672">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="7672c-1672">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="7672c-1673">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1673">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="7672c-1674">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1674">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="7672c-1675">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1675">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-1676">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-1676">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-1677">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1677">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="7672c-1678">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1678">Added example</span></span>
    - <span data-ttu-id="7672c-1679">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1679">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="7672c-1680">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1680">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="7672c-1681">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1681">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-1682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1682">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-1683">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1683">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1684">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1684">Az.Resources</span></span>
* <span data-ttu-id="7672c-1685">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1685">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="7672c-1686">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1686">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="7672c-1687">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="7672c-1687">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="7672c-1688">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1688">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7672c-1689">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7672c-1689">Az.ServiceBus</span></span>
* <span data-ttu-id="7672c-1690">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="7672c-1690">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="7672c-1691">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="7672c-1691">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="7672c-1692">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1692">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7672c-1693">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-1693">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-1694">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1694">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="7672c-1695">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="7672c-1695">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="7672c-1696">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="7672c-1696">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="7672c-1697">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1697">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="7672c-1698">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="7672c-1698">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="7672c-1699">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1699">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1700">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1700">Az.Sql</span></span>
* <span data-ttu-id="7672c-1701">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1701">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1702">Az.Storage</span></span>
* <span data-ttu-id="7672c-1703">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1703">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="7672c-1704">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="7672c-1704">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="7672c-1705">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7672c-1705">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="7672c-1706">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7672c-1706">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="7672c-1707">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-1707">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="7672c-1708">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7672c-1708">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-1709">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-1709">Az.Websites</span></span>
* <span data-ttu-id="7672c-1710">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1710">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="7672c-1711">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1711">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-1712">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-1712">Az.Accounts</span></span>
* <span data-ttu-id="7672c-1713">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1713">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7672c-1714">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-1714">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7672c-1715">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1715">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-1716">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-1716">Az.Automation</span></span>
* <span data-ttu-id="7672c-1717">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1717">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-1718">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1718">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-1719">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1719">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1720">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1720">Az.Compute</span></span>
* <span data-ttu-id="7672c-1721">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1721">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7672c-1722">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7672c-1722">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7672c-1723">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1723">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="7672c-1724">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="7672c-1724">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1725">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1725">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1726">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1726">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="7672c-1727">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1727">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7672c-1728">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1728">Az.EventHub</span></span>
* <span data-ttu-id="7672c-1729">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7672c-1729">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7672c-1730">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-1731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-1731">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-1732">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1732">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7672c-1733">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7672c-1733">Az.LogicApp</span></span>
* <span data-ttu-id="7672c-1734">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="7672c-1734">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="7672c-1735">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1735">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7672c-1736">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1736">Az.ManagedServices</span></span>
* <span data-ttu-id="7672c-1737">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="7672c-1737">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1738">Az.Network</span></span>
* <span data-ttu-id="7672c-1739">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1739">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="7672c-1740">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-1740">New cmdlets</span></span>
        - <span data-ttu-id="7672c-1741">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7672c-1741">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7672c-1742">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7672c-1742">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7672c-1743">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1743">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7672c-1744">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1744">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7672c-1745">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1745">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7672c-1746">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1746">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7672c-1747">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="7672c-1747">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="7672c-1748">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7672c-1748">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="7672c-1749">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="7672c-1749">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="7672c-1750">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1750">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="7672c-1751">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1751">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="7672c-1752">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1752">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="7672c-1753">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1753">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="7672c-1754">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1754">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="7672c-1755">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1755">Updated cmdlets</span></span>
        - <span data-ttu-id="7672c-1756">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1756">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7672c-1757">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1757">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7672c-1758">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1758">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7672c-1759">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1759">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7672c-1760">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1760">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="7672c-1761">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1761">Updated cmdlet:</span></span>
        - <span data-ttu-id="7672c-1762">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1762">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7672c-1763">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1763">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7672c-1764">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1764">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="7672c-1765">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1765">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="7672c-1766">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1766">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="7672c-1767">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="7672c-1767">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-1768">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-1768">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-1769">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1769">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="7672c-1770">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1770">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-1771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1771">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-1772">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1772">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7672c-1773">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1773">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="7672c-1774">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1774">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="7672c-1775">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1775">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7672c-1776">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1776">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="7672c-1777">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1777">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7672c-1778">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1778">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="7672c-1779">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1779">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7672c-1780">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1780">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="7672c-1781">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1781">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1782">Az.Resources</span></span>
- <span data-ttu-id="7672c-1783">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1783">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="7672c-1784">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1784">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7672c-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7672c-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="7672c-1786">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7672c-1786">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7672c-1787">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1787">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1788">Az.Sql</span></span>
* <span data-ttu-id="7672c-1789">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1789">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="7672c-1790">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1790">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="7672c-1791">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1791">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1792">Az.Storage</span></span>
* <span data-ttu-id="7672c-1793">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1793">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7672c-1794">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7672c-1794">Az.StorageSync</span></span>
* <span data-ttu-id="7672c-1795">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1795">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="7672c-1796">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1796">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-1797">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-1797">Az.Websites</span></span>
* <span data-ttu-id="7672c-1798">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1798">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="7672c-1799">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1799">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="7672c-1800">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1800">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="7672c-1801">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1801">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-1802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-1802">Az.Accounts</span></span>
* <span data-ttu-id="7672c-1803">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1803">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7672c-1804">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1804">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7672c-1805">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1805">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7672c-1806">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7672c-1806">Az.Advisor</span></span>
* <span data-ttu-id="7672c-1807">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-1807">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7672c-1808">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="7672c-1808">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7672c-1809">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-1809">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-1810">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1810">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7672c-1811">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7672c-1811">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7672c-1812">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1812">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7672c-1813">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="7672c-1813">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7672c-1814">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="7672c-1814">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7672c-1815">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7672c-1815">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7672c-1816">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1816">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-1817">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-1817">Az.Automation</span></span>
* <span data-ttu-id="7672c-1818">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1818">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1819">Az.Compute</span></span>
* <span data-ttu-id="7672c-1820">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1820">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-1821">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-1821">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-1822">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1822">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7672c-1823">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7672c-1823">Az.EventGrid</span></span>
* <span data-ttu-id="7672c-1824">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1824">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-1825">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1825">Az.IotHub</span></span>
* <span data-ttu-id="7672c-1826">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1826">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1827">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1827">Az.Network</span></span>
* <span data-ttu-id="7672c-1828">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1828">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7672c-1829">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1829">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7672c-1830">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-1830">Az.PolicyInsights</span></span>
* <span data-ttu-id="7672c-1831">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1831">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7672c-1832">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="7672c-1832">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-1833">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-1833">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-1834">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1834">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-1835">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-1835">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-1836">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7672c-1836">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1837">Az.Resources</span></span>
    - <span data-ttu-id="7672c-1838">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7672c-1838">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7672c-1839">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1839">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7672c-1840">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1840">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7672c-1841">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1841">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7672c-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7672c-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="7672c-1843">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1843">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1844">Az.Sql</span></span>
* <span data-ttu-id="7672c-1845">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1845">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7672c-1846">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-1846">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7672c-1847">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7672c-1847">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7672c-1848">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7672c-1848">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7672c-1849">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7672c-1849">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7672c-1850">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7672c-1850">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7672c-1851">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7672c-1851">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7672c-1852">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7672c-1852">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7672c-1853">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-1853">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1854">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1854">Az.Storage</span></span>
* <span data-ttu-id="7672c-1855">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1855">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7672c-1856">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7672c-1856">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7672c-1857">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1857">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7672c-1858">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="7672c-1858">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7672c-1859">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1859">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7672c-1860">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-1860">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7672c-1861">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-1861">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7672c-1862">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1862">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7672c-1863">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7672c-1863">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7672c-1864">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7672c-1864">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7672c-1865">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7672c-1865">Az.StorageSync</span></span>
* <span data-ttu-id="7672c-1866">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="7672c-1866">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7672c-1867">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1867">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-1868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-1868">Az.Accounts</span></span>
* <span data-ttu-id="7672c-1869">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1869">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7672c-1870">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="7672c-1870">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7672c-1871">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1871">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7672c-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7672c-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7672c-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="7672c-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1874">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1874">Az.Compute</span></span>
* <span data-ttu-id="7672c-1875">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-1875">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7672c-1876">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1876">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7672c-1877">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7672c-1877">Az.Dns</span></span>
* <span data-ttu-id="7672c-1878">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1878">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7672c-1879">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7672c-1879">Az.EventGrid</span></span>
* <span data-ttu-id="7672c-1880">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1880">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7672c-1881">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="7672c-1881">New cmdlets:</span></span>
    - <span data-ttu-id="7672c-1882">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7672c-1882">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7672c-1883">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7672c-1883">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7672c-1884">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7672c-1884">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7672c-1885">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="7672c-1885">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7672c-1886">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7672c-1886">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7672c-1887">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7672c-1887">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7672c-1888">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7672c-1888">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7672c-1889">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="7672c-1889">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7672c-1890">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7672c-1890">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7672c-1891">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="7672c-1891">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7672c-1892">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7672c-1892">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7672c-1893">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7672c-1893">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7672c-1894">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7672c-1894">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7672c-1895">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="7672c-1895">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="7672c-1896">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7672c-1896">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7672c-1897">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7672c-1897">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7672c-1898">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1898">Updated cmdlets:</span></span>
    - <span data-ttu-id="7672c-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7672c-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7672c-1900">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-1900">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7672c-1901">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-1901">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7672c-1902">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-1902">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7672c-1903">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1903">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7672c-1904">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="7672c-1904">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7672c-1905">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="7672c-1905">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7672c-1906">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-1906">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7672c-1907">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="7672c-1907">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="7672c-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7672c-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7672c-1909">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-1909">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7672c-1910">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7672c-1910">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7672c-1911">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-1911">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7672c-1912">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-1912">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7672c-1913">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-1913">Az.FrontDoor</span></span>
* <span data-ttu-id="7672c-1914">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7672c-1914">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7672c-1915">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="7672c-1915">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7672c-1916">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7672c-1916">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7672c-1917">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="7672c-1917">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1918">Az.Network</span></span>
* <span data-ttu-id="7672c-1919">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="7672c-1919">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7672c-1920">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-1920">New cmdlets</span></span>
        - <span data-ttu-id="7672c-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7672c-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7672c-1922">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="7672c-1922">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7672c-1923">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-1923">New cmdlets</span></span>
        - <span data-ttu-id="7672c-1924">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7672c-1924">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7672c-1925">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="7672c-1925">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7672c-1926">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-1926">New cmdlets</span></span>
        - <span data-ttu-id="7672c-1927">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7672c-1927">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7672c-1928">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7672c-1928">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7672c-1929">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7672c-1929">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7672c-1930">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-1930">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7672c-1931">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1931">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7672c-1932">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="7672c-1932">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7672c-1933">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-1933">New cmdlets</span></span>
        - <span data-ttu-id="7672c-1934">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7672c-1934">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7672c-1935">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7672c-1935">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7672c-1936">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7672c-1936">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7672c-1937">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7672c-1937">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7672c-1938">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="7672c-1938">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7672c-1939">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1939">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7672c-1940">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1940">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7672c-1941">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1941">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7672c-1942">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1942">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7672c-1943">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1943">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7672c-1944">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1944">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7672c-1945">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1945">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7672c-1946">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1946">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7672c-1947">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1947">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7672c-1948">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1948">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7672c-1949">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1949">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7672c-1950">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1950">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7672c-1951">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1951">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7672c-1952">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-1952">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7672c-1953">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1953">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7672c-1954">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1954">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7672c-1955">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7672c-1955">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7672c-1956">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7672c-1956">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="7672c-1957">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="7672c-1957">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="7672c-1958">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1958">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7672c-1959">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1959">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7672c-1960">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1960">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-1961">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-1961">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-1962">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1962">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-1963">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-1963">Az.Resources</span></span>
* <span data-ttu-id="7672c-1964">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="7672c-1964">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7672c-1965">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1965">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7672c-1966">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1966">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7672c-1967">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1967">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7672c-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-1968">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-1969">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1969">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-1970">Az.Sql</span></span>
* <span data-ttu-id="7672c-1971">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1971">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7672c-1972">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1972">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7672c-1973">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-1973">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7672c-1974">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7672c-1974">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7672c-1975">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7672c-1975">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7672c-1976">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7672c-1976">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7672c-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7672c-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7672c-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7672c-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-1979">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-1979">Az.Storage</span></span>
* <span data-ttu-id="7672c-1980">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="7672c-1980">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7672c-1981">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-1981">New-AzStorageAccount</span></span>
* <span data-ttu-id="7672c-1982">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1982">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7672c-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7672c-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-1984">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-1984">Az.Websites</span></span>
* <span data-ttu-id="7672c-1985">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="7672c-1985">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7672c-1986">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="7672c-1986">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7672c-1987">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-1987">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7672c-1988">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7672c-1988">Az.Cdn</span></span>
* <span data-ttu-id="7672c-1989">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1989">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-1990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-1990">Az.Compute</span></span>
* <span data-ttu-id="7672c-1991">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-1991">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7672c-1992">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7672c-1992">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7672c-1993">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7672c-1993">Az.EventHub</span></span>
* <span data-ttu-id="7672c-1994">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7672c-1994">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7672c-1995">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7672c-1995">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-1996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-1996">Az.Network</span></span>
* <span data-ttu-id="7672c-1997">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-1997">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7672c-1998">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-1998">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7672c-1999">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-1999">Az.PolicyInsights</span></span>
* <span data-ttu-id="7672c-2000">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2000">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-2001">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2001">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-2002">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2002">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7672c-2003">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7672c-2003">Az.ServiceBus</span></span>
* <span data-ttu-id="7672c-2004">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7672c-2004">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7672c-2005">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-2005">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-2006">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2006">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7672c-2007">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2007">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2008">Az.Sql</span></span>
* <span data-ttu-id="7672c-2009">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2009">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7672c-2010">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-2010">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7672c-2011">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-2011">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7672c-2012">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2012">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-2013">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2013">Az.Websites</span></span>
* <span data-ttu-id="7672c-2014">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2014">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7672c-2015">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2015">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7672c-2016">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-2016">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-2017">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-2017">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7672c-2018">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="7672c-2018">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7672c-2019">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="7672c-2019">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7672c-2020">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="7672c-2020">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7672c-2021">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7672c-2021">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7672c-2022">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="7672c-2022">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7672c-2023">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="7672c-2023">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7672c-2024">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7672c-2024">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7672c-2025">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-2025">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7672c-2026">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="7672c-2026">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7672c-2027">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="7672c-2027">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7672c-2028">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="7672c-2028">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7672c-2029">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7672c-2029">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7672c-2030">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-2030">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7672c-2031">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="7672c-2031">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7672c-2032">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="7672c-2032">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7672c-2033">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="7672c-2033">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7672c-2034">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7672c-2034">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7672c-2035">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="7672c-2035">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="7672c-2036">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="7672c-2036">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7672c-2037">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-2037">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7672c-2038">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7672c-2038">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7672c-2039">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="7672c-2039">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7672c-2040">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2040">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="7672c-2041">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2041">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7672c-2042">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2042">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7672c-2043">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7672c-2043">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7672c-2044">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-2044">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7672c-2045">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2045">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7672c-2046">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2046">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7672c-2047">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2047">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="7672c-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7672c-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7672c-2049">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2049">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7672c-2050">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2050">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7672c-2051">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="7672c-2051">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7672c-2052">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="7672c-2052">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7672c-2053">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="7672c-2053">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7672c-2054">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2054">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7672c-2055">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2055">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7672c-2056">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2056">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7672c-2057">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="7672c-2057">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7672c-2058">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="7672c-2058">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7672c-2059">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="7672c-2059">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7672c-2060">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="7672c-2060">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="7672c-2061">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2061">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7672c-2062">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="7672c-2062">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7672c-2063">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="7672c-2063">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7672c-2064">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="7672c-2064">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="7672c-2065">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2065">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7672c-2066">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="7672c-2066">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7672c-2067">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="7672c-2067">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7672c-2068">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="7672c-2068">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7672c-2069">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="7672c-2069">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7672c-2070">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2070">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7672c-2071">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="7672c-2071">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7672c-2072">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="7672c-2072">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7672c-2073">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2073">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7672c-2074">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="7672c-2074">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7672c-2075">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="7672c-2075">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7672c-2076">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2076">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7672c-2077">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2077">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7672c-2078">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="7672c-2078">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7672c-2079">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="7672c-2079">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7672c-2080">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2080">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7672c-2081">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2081">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7672c-2082">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="7672c-2082">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7672c-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7672c-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7672c-2084">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="7672c-2084">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7672c-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7672c-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7672c-2086">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7672c-2086">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7672c-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7672c-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7672c-2088">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="7672c-2088">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7672c-2089">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="7672c-2089">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7672c-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7672c-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7672c-2091">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="7672c-2091">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="7672c-2092">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7672c-2092">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7672c-2093">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="7672c-2093">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-2094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-2094">Az.Automation</span></span>
* <span data-ttu-id="7672c-2095">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2095">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7672c-2096">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7672c-2097">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2097">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7672c-2098">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2098">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7672c-2099">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2099">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7672c-2100">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2100">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7672c-2101">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-2101">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2102">Az.Compute</span></span>
* <span data-ttu-id="7672c-2103">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2103">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7672c-2104">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="7672c-2104">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-2106">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2106">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-2107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-2107">Az.Monitor</span></span>
* <span data-ttu-id="7672c-2108">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2108">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2109">Az.Network</span></span>
* <span data-ttu-id="7672c-2110">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2110">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7672c-2111">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="7672c-2111">Updated cmdlet:</span></span>
        - <span data-ttu-id="7672c-2112">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7672c-2112">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7672c-2113">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2113">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2114">Az.Resources</span></span>
* <span data-ttu-id="7672c-2115">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2115">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2116">Az.Sql</span></span>
* <span data-ttu-id="7672c-2117">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="7672c-2117">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7672c-2118">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2118">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-2119">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-2119">Az.Accounts</span></span>
* <span data-ttu-id="7672c-2120">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="7672c-2120">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-2121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2121">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-2122">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="7672c-2122">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7672c-2123">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="7672c-2123">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2124">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2124">Az.Compute</span></span>
* <span data-ttu-id="7672c-2125">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="7672c-2125">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7672c-2126">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7672c-2126">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7672c-2127">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-2127">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7672c-2128">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2128">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7672c-2129">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-2129">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7672c-2130">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2130">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="7672c-2131">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7672c-2131">Breaking changes</span></span>
    - <span data-ttu-id="7672c-2132">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2132">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7672c-2133">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2133">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7672c-2134">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7672c-2134">Az.DeploymentManager</span></span>
* <span data-ttu-id="7672c-2135">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="7672c-2135">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7672c-2136">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7672c-2136">Az.Dns</span></span>
* <span data-ttu-id="7672c-2137">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="7672c-2137">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7672c-2138">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="7672c-2138">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7672c-2139">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-2139">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7672c-2140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-2140">Az.FrontDoor</span></span>
* <span data-ttu-id="7672c-2141">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="7672c-2141">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7672c-2142">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="7672c-2142">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7672c-2143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-2143">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-2144">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="7672c-2144">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7672c-2145">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7672c-2145">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7672c-2146">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7672c-2146">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7672c-2147">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2147">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7672c-2148">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="7672c-2148">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7672c-2149">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="7672c-2149">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7672c-2150">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="7672c-2150">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-2151">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-2151">Az.Monitor</span></span>
* <span data-ttu-id="7672c-2152">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="7672c-2152">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="7672c-2153">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7672c-2153">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7672c-2154">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7672c-2154">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7672c-2155">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7672c-2155">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7672c-2156">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7672c-2156">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7672c-2157">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7672c-2157">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7672c-2158">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7672c-2158">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7672c-2159">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7672c-2159">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7672c-2160">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7672c-2160">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7672c-2161">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7672c-2161">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7672c-2162">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7672c-2162">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7672c-2163">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7672c-2163">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7672c-2164">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="7672c-2164">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7672c-2165">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2165">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2166">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2166">Az.Network</span></span>
* <span data-ttu-id="7672c-2167">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="7672c-2167">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7672c-2168">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-2168">New cmdlets</span></span>
        - <span data-ttu-id="7672c-2169">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7672c-2169">New-AzNatGateway</span></span>
        - <span data-ttu-id="7672c-2170">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7672c-2170">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7672c-2171">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7672c-2171">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7672c-2172">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7672c-2172">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7672c-2173">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2173">Updated cmdlets</span></span>
        - <span data-ttu-id="7672c-2174">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7672c-2174">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7672c-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7672c-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7672c-2176">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="7672c-2176">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7672c-2177">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2177">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7672c-2178">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2178">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7672c-2179">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-2179">Az.PolicyInsights</span></span>
* <span data-ttu-id="7672c-2180">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-2180">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7672c-2181">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7672c-2181">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7672c-2182">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="7672c-2182">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-2183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2183">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-2184">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-2184">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7672c-2185">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="7672c-2185">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7672c-2186">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="7672c-2186">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7672c-2187">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="7672c-2187">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7672c-2188">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="7672c-2188">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7672c-2189">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="7672c-2189">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7672c-2190">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7672c-2190">Az.Relay</span></span>
* <span data-ttu-id="7672c-2191">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="7672c-2191">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7672c-2192">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7672c-2192">Az.ServiceBus</span></span>
* <span data-ttu-id="7672c-2193">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2193">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-2194">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-2194">Az.Storage</span></span>
* <span data-ttu-id="7672c-2195">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="7672c-2195">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="7672c-2196">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="7672c-2196">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7672c-2197">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="7672c-2197">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7672c-2198">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-2198">New-AzStorageAccount</span></span>
* <span data-ttu-id="7672c-2199">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="7672c-2199">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7672c-2200">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-2200">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7672c-2201">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-2201">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7672c-2202">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-2202">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-2203">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2203">Az.Websites</span></span>
* <span data-ttu-id="7672c-2204">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="7672c-2204">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7672c-2205">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2205">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7672c-2206">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2206">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7672c-2207">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7672c-2207">Highlights since the last major release</span></span>
* <span data-ttu-id="7672c-2208">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-2208">General availability of `Az` module</span></span>
* <span data-ttu-id="7672c-2209">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7672c-2209">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7672c-2210">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7672c-2210">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7672c-2211">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2211">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7672c-2212">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2212">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7672c-2213">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2213">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7672c-2214">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-2214">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-2215">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-2215">Az.Accounts</span></span>
* <span data-ttu-id="7672c-2216">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2216">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7672c-2217">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7672c-2217">Az.Batch</span></span>
* <span data-ttu-id="7672c-2218">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7672c-2219">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7672c-2219">Az.Cdn</span></span>
* <span data-ttu-id="7672c-2220">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2220">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-2222">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2223">Az.Compute</span></span>
* <span data-ttu-id="7672c-2224">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2224">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7672c-2225">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7672c-2226">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2226">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-2227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-2227">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-2228">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2228">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-2229">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-2229">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-2230">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2230">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7672c-2231">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7672c-2231">Az.EventGrid</span></span>
* <span data-ttu-id="7672c-2232">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2232">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7672c-2233">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7672c-2233">Az.EventHub</span></span>
* <span data-ttu-id="7672c-2234">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2234">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7672c-2235">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7672c-2235">Az.HDInsight</span></span>
* <span data-ttu-id="7672c-2236">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-2237">Az.IotHub</span></span>
* <span data-ttu-id="7672c-2238">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-2239">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-2239">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-2240">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7672c-2241">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2241">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7672c-2242">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7672c-2242">Az.MachineLearning</span></span>
* <span data-ttu-id="7672c-2243">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7672c-2244">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7672c-2244">Az.Media</span></span>
* <span data-ttu-id="7672c-2245">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-2246">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-2246">Az.Monitor</span></span>
  * <span data-ttu-id="7672c-2247">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="7672c-2247">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7672c-2248">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7672c-2248">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7672c-2249">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7672c-2249">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7672c-2250">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7672c-2250">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7672c-2251">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7672c-2251">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7672c-2252">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7672c-2252">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7672c-2253">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2253">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2254">Az.Network</span></span>
* <span data-ttu-id="7672c-2255">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7672c-2256">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2256">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7672c-2257">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7672c-2257">Az.NotificationHubs</span></span>
* <span data-ttu-id="7672c-2258">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2258">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-2259">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-2259">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-2260">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7672c-2261">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7672c-2261">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7672c-2262">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2262">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-2263">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2263">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-2264">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2264">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7672c-2265">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="7672c-2265">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7672c-2266">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2266">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7672c-2267">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2267">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7672c-2268">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7672c-2268">Az.RedisCache</span></span>
* <span data-ttu-id="7672c-2269">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2269">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2270">Az.Resources</span></span>
* <span data-ttu-id="7672c-2271">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2271">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2272">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2272">Az.Sql</span></span>
* <span data-ttu-id="7672c-2273">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2273">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7672c-2274">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2274">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7672c-2275">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2275">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7672c-2276">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2276">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7672c-2277">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2277">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7672c-2278">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-2278">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7672c-2279">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2279">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-2280">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2280">Az.Websites</span></span>
* <span data-ttu-id="7672c-2281">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2281">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7672c-2282">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2282">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7672c-2283">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2283">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7672c-2284">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2284">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7672c-2285">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2285">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7672c-2286">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7672c-2286">Highlights since the last major release</span></span>
* <span data-ttu-id="7672c-2287">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-2287">General availability of `Az` module</span></span>
* <span data-ttu-id="7672c-2288">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7672c-2288">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7672c-2289">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7672c-2289">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7672c-2290">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2290">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7672c-2291">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2291">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7672c-2292">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2292">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7672c-2293">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-2293">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7672c-2294">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-2294">Az.Accounts</span></span>
* <span data-ttu-id="7672c-2295">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2295">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7672c-2296">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2296">Az.AnalysisServices</span></span>
* <span data-ttu-id="7672c-2297">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7672c-2297">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7672c-2298">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="7672c-2298">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-2299">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-2299">Az.Automation</span></span>
* <span data-ttu-id="7672c-2300">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2300">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7672c-2301">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-2301">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7672c-2302">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7672c-2302">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2303">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2303">Az.Compute</span></span>
* <span data-ttu-id="7672c-2304">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2304">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7672c-2305">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2305">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7672c-2306">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7672c-2306">Az.ContainerInstance</span></span>
* <span data-ttu-id="7672c-2307">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2307">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-2308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-2308">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-2309">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2309">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7672c-2310">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2310">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2311">Az.Resources</span></span>
* <span data-ttu-id="7672c-2312">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2312">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7672c-2313">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2313">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7672c-2314">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2314">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7672c-2315">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7672c-2315">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7672c-2316">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2316">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7672c-2317">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7672c-2317">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2318">Az.Sql</span></span>
* <span data-ttu-id="7672c-2319">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-2319">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-2320">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-2320">Az.Storage</span></span>
* <span data-ttu-id="7672c-2321">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="7672c-2321">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7672c-2322">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7672c-2322">New-AzStorageContext</span></span>
* <span data-ttu-id="7672c-2323">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-2323">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7672c-2324">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7672c-2324">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7672c-2325">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7672c-2325">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7672c-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7672c-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7672c-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7672c-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7672c-2328">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-2328">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7672c-2329">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7672c-2329">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7672c-2330">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7672c-2330">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7672c-2331">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7672c-2331">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7672c-2332">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7672c-2332">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7672c-2333">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2333">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7672c-2334">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="7672c-2334">Highlights since the last major release</span></span>
* <span data-ttu-id="7672c-2335">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-2335">General availability of `Az` module</span></span>
* <span data-ttu-id="7672c-2336">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7672c-2336">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7672c-2337">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7672c-2337">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7672c-2338">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2338">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7672c-2339">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2339">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7672c-2340">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2340">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7672c-2341">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-2341">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-2342">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-2342">Az.Automation</span></span>
* <span data-ttu-id="7672c-2343">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="7672c-2343">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7672c-2344">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="7672c-2344">Dynamic grouping</span></span>
    * <span data-ttu-id="7672c-2345">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="7672c-2345">Pre-Post script</span></span>
    * <span data-ttu-id="7672c-2346">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="7672c-2346">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2347">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2347">Az.Compute</span></span>
* <span data-ttu-id="7672c-2348">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7672c-2348">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7672c-2349">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2349">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-2350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-2350">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-2351">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2351">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2352">Az.Network</span></span>
* <span data-ttu-id="7672c-2353">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2353">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7672c-2354">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2354">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-2355">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2355">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-2356">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2356">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7672c-2357">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2357">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2358">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2358">Az.Resources</span></span>
* <span data-ttu-id="7672c-2359">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2359">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7672c-2360">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2360">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2361">Az.Sql</span></span>
* <span data-ttu-id="7672c-2362">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2362">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-2363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-2363">Az.Storage</span></span>
* <span data-ttu-id="7672c-2364">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-2364">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7672c-2365">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7672c-2365">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7672c-2366">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7672c-2366">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7672c-2367">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7672c-2367">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7672c-2368">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7672c-2368">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7672c-2369">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7672c-2369">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7672c-2370">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7672c-2370">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-2371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2371">Az.Websites</span></span>
* <span data-ttu-id="7672c-2372">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2372">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="7672c-2373">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2373">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-2374">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-2374">Az.Accounts</span></span>
* <span data-ttu-id="7672c-2375">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2375">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7672c-2376">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2376">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-2377">Az.Automation</span></span>
* <span data-ttu-id="7672c-2378">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2378">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7672c-2379">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2379">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7672c-2380">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="7672c-2380">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7672c-2381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7672c-2381">Az.Cdn</span></span>
* <span data-ttu-id="7672c-2382">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-2382">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2383">Az.Compute</span></span>
* <span data-ttu-id="7672c-2384">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2384">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-2385">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-2385">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-2386">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2386">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7672c-2387">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7672c-2387">Az.LogicApp</span></span>
* <span data-ttu-id="7672c-2388">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="7672c-2388">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2389">Az.Network</span></span>
* <span data-ttu-id="7672c-2390">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2390">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-2391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2391">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-2392">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2392">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7672c-2393">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="7672c-2393">SDK Update</span></span>
* <span data-ttu-id="7672c-2394">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-2394">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7672c-2395">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2395">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2396">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2396">Az.Resources</span></span>
* <span data-ttu-id="7672c-2397">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2397">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7672c-2398">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="7672c-2398">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7672c-2399">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2399">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7672c-2400">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="7672c-2400">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7672c-2401">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2401">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7672c-2402">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="7672c-2402">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2403">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2403">Az.Sql</span></span>
* <span data-ttu-id="7672c-2404">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-2404">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7672c-2405">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-2405">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-2406">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-2406">Az.Storage</span></span>
* <span data-ttu-id="7672c-2407">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7672c-2407">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7672c-2408">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2408">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7672c-2409">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2409">Az.AnalysisServices</span></span>
* <span data-ttu-id="7672c-2410">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-2410">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-2411">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-2411">Az.Automation</span></span>
* <span data-ttu-id="7672c-2412">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2412">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7672c-2413">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2413">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7672c-2414">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2414">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-2415">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2415">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-2416">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2416">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2417">Az.Compute</span></span>
* <span data-ttu-id="7672c-2418">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2418">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7672c-2419">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2419">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7672c-2420">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2420">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7672c-2421">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="7672c-2421">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-2422">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-2422">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-2423">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2423">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7672c-2424">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7672c-2424">Az.EventHub</span></span>
* <span data-ttu-id="7672c-2425">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2425">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-2426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-2426">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-2427">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2427">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7672c-2428">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7672c-2428">Az.LogicApp</span></span>
* <span data-ttu-id="7672c-2429">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2429">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7672c-2430">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2430">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7672c-2431">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-2431">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7672c-2432">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7672c-2432">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7672c-2433">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7672c-2433">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7672c-2434">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7672c-2434">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7672c-2435">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7672c-2435">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7672c-2436">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="7672c-2436">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7672c-2437">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7672c-2437">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7672c-2438">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7672c-2438">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7672c-2439">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7672c-2439">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7672c-2440">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7672c-2440">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7672c-2441">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2441">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7672c-2442">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-2442">Az.Monitor</span></span>
* <span data-ttu-id="7672c-2443">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2443">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2444">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2444">Az.Network</span></span>
* <span data-ttu-id="7672c-2445">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2445">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-2446">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-2446">Az.OperationalInsights</span></span>
* <span data-ttu-id="7672c-2447">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="7672c-2447">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7672c-2448">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2448">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="7672c-2449">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2449">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2450">Az.Resources</span></span>
* <span data-ttu-id="7672c-2451">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2451">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7672c-2452">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2452">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7672c-2453">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2453">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7672c-2454">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2454">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2455">Az.Sql</span></span>
* <span data-ttu-id="7672c-2456">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2456">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7672c-2457">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2457">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2458">Az.Websites</span></span>
* <span data-ttu-id="7672c-2459">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2459">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7672c-2460">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2460">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-2461">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-2461">Az.Accounts</span></span>
* <span data-ttu-id="7672c-2462">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7672c-2462">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7672c-2463">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2463">Az.AnalysisServices</span></span>
<span data-ttu-id="7672c-2464">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="7672c-2464">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2465">Az.Compute</span></span>
* <span data-ttu-id="7672c-2466">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2466">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7672c-2467">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2467">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7672c-2468">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2468">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-2469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2469">Az.RecoveryServices</span></span>
<span data-ttu-id="7672c-2470">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="7672c-2470">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2471">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2471">Az.Resources</span></span>
* <span data-ttu-id="7672c-2472">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2472">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="7672c-2473">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7672c-2473">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7672c-2474">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2474">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="7672c-2475">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7672c-2475">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2476">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2476">Az.Sql</span></span>
* <span data-ttu-id="7672c-2477">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7672c-2477">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7672c-2478">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2478">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7672c-2479">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2479">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7672c-2480">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2480">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-2481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-2481">Az.Accounts</span></span>
* <span data-ttu-id="7672c-2482">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="7672c-2482">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7672c-2483">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2483">Az.AnalysisServices</span></span>
* <span data-ttu-id="7672c-2484">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="7672c-2484">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-2485">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2485">Az.RecoveryServices</span></span>
* <span data-ttu-id="7672c-2486">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="7672c-2486">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7672c-2487">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2487">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-2488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-2488">Az.Accounts</span></span>
* <span data-ttu-id="7672c-2489">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2489">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7672c-2490">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2490">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7672c-2491">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2491">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7672c-2492">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7672c-2492">Az.Aks</span></span>
* <span data-ttu-id="7672c-2493">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2493">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7672c-2494">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-2494">Az.Automation</span></span>
* <span data-ttu-id="7672c-2495">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2495">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7672c-2496">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2496">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7672c-2497">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7672c-2497">Az.Cdn</span></span>
* <span data-ttu-id="7672c-2498">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2498">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2499">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2499">Az.Compute</span></span>
* <span data-ttu-id="7672c-2500">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2500">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7672c-2501">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2501">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7672c-2502">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2502">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7672c-2503">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7672c-2503">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7672c-2504">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2504">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7672c-2505">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7672c-2505">Az.DataFactory</span></span>
* <span data-ttu-id="7672c-2506">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2506">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-2507">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-2507">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-2508">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2508">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7672c-2509">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="7672c-2509">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7672c-2510">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2510">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-2511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-2511">Az.IotHub</span></span>
* <span data-ttu-id="7672c-2512">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2512">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7672c-2513">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-2513">Az.KeyVault</span></span>
* <span data-ttu-id="7672c-2514">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2514">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2515">Az.Network</span></span>
* <span data-ttu-id="7672c-2516">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2516">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2517">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2517">Az.Resources</span></span>
* <span data-ttu-id="7672c-2518">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2518">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7672c-2519">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2519">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7672c-2520">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2520">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7672c-2521">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2521">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7672c-2522">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2522">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7672c-2523">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2523">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7672c-2524">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="7672c-2524">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7672c-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-2526">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="7672c-2526">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7672c-2527">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2527">Fix some error messages.</span></span>
* <span data-ttu-id="7672c-2528">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2528">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7672c-2529">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2529">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7672c-2530">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7672c-2530">Az.SignalR</span></span>
* <span data-ttu-id="7672c-2531">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2531">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2532">Az.Sql</span></span>
* <span data-ttu-id="7672c-2533">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2533">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7672c-2534">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2534">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7672c-2535">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2535">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7672c-2536">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-2536">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-2537">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-2537">Az.Storage</span></span>
* <span data-ttu-id="7672c-2538">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2538">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7672c-2539">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-2539">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7672c-2540">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7672c-2540">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7672c-2541">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7672c-2541">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7672c-2542">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7672c-2542">Az.TrafficManager</span></span>
* <span data-ttu-id="7672c-2543">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2543">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-2544">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2544">Az.Websites</span></span>
* <span data-ttu-id="7672c-2545">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2545">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7672c-2546">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2546">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7672c-2547">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2547">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7672c-2548">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="7672c-2548">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7672c-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-2549">Az.Accounts</span></span>
* <span data-ttu-id="7672c-2550">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2550">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2551">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2551">Az.Compute</span></span>
* <span data-ttu-id="7672c-2552">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="7672c-2552">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7672c-2553">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2553">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7672c-2554">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7672c-2554">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-2555">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-2555">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-2556">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2556">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7672c-2557">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2557">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7672c-2558">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7672c-2558">Az.EventGrid</span></span>
* <span data-ttu-id="7672c-2559">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2559">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7672c-2560">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2560">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7672c-2561">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-2561">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7672c-2562">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="7672c-2562">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7672c-2563">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="7672c-2563">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7672c-2564">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="7672c-2564">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7672c-2565">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-2565">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7672c-2566">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="7672c-2566">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7672c-2567">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="7672c-2567">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7672c-2568">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="7672c-2568">Dead letter endpoint.</span></span>
* <span data-ttu-id="7672c-2569">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2569">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7672c-2570">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-2570">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7672c-2571">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7672c-2571">Az.IotHub</span></span>
* <span data-ttu-id="7672c-2572">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2572">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7672c-2573">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7672c-2573">Az.LogicApp</span></span>
* <span data-ttu-id="7672c-2574">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="7672c-2574">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2575">Az.Resources</span></span>
* <span data-ttu-id="7672c-2576">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2576">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7672c-2577">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="7672c-2577">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7672c-2578">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2578">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7672c-2579">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2579">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7672c-2580">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2580">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7672c-2581">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="7672c-2581">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7672c-2582">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7672c-2582">Az.SignalR</span></span>
* <span data-ttu-id="7672c-2583">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7672c-2583">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2584">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2584">Az.Sql</span></span>
* <span data-ttu-id="7672c-2585">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="7672c-2585">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7672c-2586">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-2586">Az.Storage</span></span>
* <span data-ttu-id="7672c-2587">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="7672c-2587">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7672c-2588">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7672c-2588">New-AzStorageContext</span></span>
* <span data-ttu-id="7672c-2589">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2589">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7672c-2590">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7672c-2590">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-2591">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2591">Az.Websites</span></span>
* <span data-ttu-id="7672c-2592">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2592">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7672c-2593">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7672c-2593">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7672c-2594">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="7672c-2594">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7672c-2595">Genel</span><span class="sxs-lookup"><span data-stu-id="7672c-2595">General</span></span>

- <span data-ttu-id="7672c-2596">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-2596">General Availability of Az Module</span></span>
- <span data-ttu-id="7672c-2597">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="7672c-2597">Online help for each module</span></span>
- <span data-ttu-id="7672c-2598">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="7672c-2598">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7672c-2599">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2599">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7672c-2600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7672c-2600">Az.Accounts</span></span>
- <span data-ttu-id="7672c-2601">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7672c-2601">Changed from Az.Profile</span></span>
- <span data-ttu-id="7672c-2602">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2602">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7672c-2603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-2603">Az.ApiManagement</span></span>
- <span data-ttu-id="7672c-2604">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="7672c-2604">Fixes for #7002</span></span>
- <span data-ttu-id="7672c-2605">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7672c-2606">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7672c-2606">Az.Batch</span></span>
- <span data-ttu-id="7672c-2607">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2607">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7672c-2608">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="7672c-2608">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7672c-2609">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2609">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7672c-2610">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7672c-2610">Az.Billing</span></span>
- <span data-ttu-id="7672c-2611">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2611">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7672c-2612">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2612">Az.CognitivServices</span></span>
- <span data-ttu-id="7672c-2613">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2613">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7672c-2614">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-2614">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7672c-2615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7672c-2615">Az.ContainerInstance</span></span>
- <span data-ttu-id="7672c-2616">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2616">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7672c-2617">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7672c-2617">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7672c-2618">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2618">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7672c-2619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-2619">Az.DataLakeStore</span></span>
- <span data-ttu-id="7672c-2620">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2620">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7672c-2621">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7672c-2621">Az.Monitor</span></span>
- <span data-ttu-id="7672c-2622">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2622">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7672c-2623">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7672c-2623">Az.KeyVault</span></span>
- <span data-ttu-id="7672c-2624">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-2624">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7672c-2625">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7672c-2625">Az.MachineLearning</span></span>
- <span data-ttu-id="7672c-2626">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2626">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7672c-2627">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7672c-2627">Az.Media</span></span>
- <span data-ttu-id="7672c-2628">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="7672c-2628">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7672c-2629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2629">Az.Network</span></span>
<span data-ttu-id="7672c-2630">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2630">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7672c-2631">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="7672c-2631">New cmdlets added:</span></span>
        - <span data-ttu-id="7672c-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7672c-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7672c-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7672c-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7672c-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7672c-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7672c-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7672c-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7672c-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7672c-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7672c-2637">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7672c-2637">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7672c-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7672c-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7672c-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7672c-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7672c-2640">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2640">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7672c-2641">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7672c-2641">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7672c-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7672c-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7672c-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7672c-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7672c-2644">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-2644">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7672c-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7672c-2646">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2646">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7672c-2647">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2647">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7672c-2648">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7672c-2648">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7672c-2649">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7672c-2649">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7672c-2650">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7672c-2650">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7672c-2651">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2651">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7672c-2652">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7672c-2653">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-2653">Az.OperationalInsights</span></span>
- <span data-ttu-id="7672c-2654">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7672c-2655">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7672c-2655">Az.Profile</span></span>
- <span data-ttu-id="7672c-2656">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2656">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-2657">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2657">Az.RecoveryServices</span></span>
- <span data-ttu-id="7672c-2658">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2658">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7672c-2659">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2659">Az.Resources</span></span>
- <span data-ttu-id="7672c-2660">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2660">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7672c-2661">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-2661">Az.ServiceFabric</span></span>
- <span data-ttu-id="7672c-2662">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="7672c-2662">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7672c-2663">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2663">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7672c-2664">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7672c-2664">Az.SIgnalR</span></span>
- <span data-ttu-id="7672c-2665">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="7672c-2665">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7672c-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2666">Az.Sql</span></span>
- <span data-ttu-id="7672c-2667">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2667">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7672c-2668">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2668">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7672c-2669">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2669">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7672c-2670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-2670">Az.Storage</span></span>
- <span data-ttu-id="7672c-2671">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2671">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7672c-2672">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2672">Az.Websites</span></span>
- <span data-ttu-id="7672c-2673">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="7672c-2673">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7672c-2674">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="7672c-2674">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7672c-2675">Genel</span><span class="sxs-lookup"><span data-stu-id="7672c-2675">General</span></span>

* <span data-ttu-id="7672c-2676">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7672c-2676">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7672c-2677">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2677">Az.Compute</span></span>

* <span data-ttu-id="7672c-2678">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2678">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7672c-2679">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-2679">Az.DataLakeStore</span></span>

* <span data-ttu-id="7672c-2680">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2680">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7672c-2681">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7672c-2681">Az.FrontDoor</span></span>

* <span data-ttu-id="7672c-2682">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2682">Fixed some broken links</span></span>
    - <span data-ttu-id="7672c-2683">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2683">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7672c-2684">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2684">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7672c-2685">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2685">Az.RecoveryServices</span></span>

* <span data-ttu-id="7672c-2686">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2686">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7672c-2687">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2687">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7672c-2688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2688">Az.Resources</span></span>

* <span data-ttu-id="7672c-2689">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7672c-2689">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7672c-2690">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2690">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7672c-2691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2691">Az.Sql</span></span>

* <span data-ttu-id="7672c-2692">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="7672c-2692">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7672c-2693">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2693">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7672c-2694">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2694">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7672c-2695">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7672c-2695">Az.Storage</span></span>

* <span data-ttu-id="7672c-2696">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2696">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7672c-2697">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2697">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7672c-2698">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7672c-2698">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7672c-2699">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2699">Support Static Website configuration</span></span>
    - <span data-ttu-id="7672c-2700">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7672c-2700">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7672c-2701">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7672c-2701">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7672c-2702">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2702">Az.Websites</span></span>

* <span data-ttu-id="7672c-2703">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7672c-2703">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="7672c-2704">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2704">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7672c-2705">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="7672c-2705">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7672c-2706">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="7672c-2706">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7672c-2707">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7672c-2707">Az.ApiManagement</span></span>
* <span data-ttu-id="7672c-2708">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7672c-2708">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7672c-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7672c-2709">Az.Automation</span></span>
* <span data-ttu-id="7672c-2710">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="7672c-2710">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7672c-2711">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2711">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7672c-2712">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2712">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7672c-2713">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2713">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7672c-2714">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2714">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7672c-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2715">Az.Compute</span></span>
* <span data-ttu-id="7672c-2716">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2716">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7672c-2717">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7672c-2717">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7672c-2718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7672c-2718">Az.ContainerInstance</span></span>
* <span data-ttu-id="7672c-2719">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7672c-2719">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7672c-2720">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7672c-2720">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7672c-2721">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2721">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7672c-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2722">Az.Network</span></span>
* <span data-ttu-id="7672c-2723">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2723">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7672c-2724">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2724">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7672c-2725">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2725">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="7672c-2726">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2726">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7672c-2727">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7672c-2727">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7672c-2728">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2728">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7672c-2729">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="7672c-2729">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7672c-2730">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7672c-2730">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7672c-2731">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2731">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7672c-2732">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="7672c-2732">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7672c-2733">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7672c-2733">Az.Relay</span></span>
* <span data-ttu-id="7672c-2734">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2734">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7672c-2735">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2735">Az.Resources</span></span>
* <span data-ttu-id="7672c-2736">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2736">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7672c-2737">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2737">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7672c-2738">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7672c-2738">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7672c-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-2740">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2740">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7672c-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2741">Az.Sql</span></span>
* <span data-ttu-id="7672c-2742">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2742">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7672c-2743">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7672c-2743">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7672c-2744">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7672c-2744">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7672c-2745">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7672c-2745">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7672c-2746">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7672c-2746">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7672c-2747">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7672c-2747">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7672c-2748">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7672c-2748">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7672c-2749">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7672c-2749">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7672c-2750">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7672c-2750">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7672c-2751">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2751">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7672c-2752">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2752">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7672c-2753">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2753">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7672c-2754">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7672c-2754">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7672c-2755">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7672c-2755">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7672c-2756">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7672c-2756">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7672c-2757">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7672c-2757">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7672c-2758">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2758">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7672c-2759">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="7672c-2759">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7672c-2760">Genel</span><span class="sxs-lookup"><span data-stu-id="7672c-2760">General</span></span>
* <span data-ttu-id="7672c-2761">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="7672c-2761">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7672c-2762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7672c-2762">Az.Profile</span></span>
* <span data-ttu-id="7672c-2763">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2763">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7672c-2764">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2764">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7672c-2765">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2765">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7672c-2766">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2766">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7672c-2767">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2767">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7672c-2768">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2768">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7672c-2769">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2769">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-2770">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2770">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-2771">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2771">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2772">Az.Compute</span></span>
* <span data-ttu-id="7672c-2773">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2773">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7672c-2774">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="7672c-2774">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7672c-2775">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2775">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-2776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-2776">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-2777">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2777">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7672c-2778">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2778">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7672c-2779">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7672c-2779">Az.Insights</span></span>
* <span data-ttu-id="7672c-2780">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2780">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7672c-2781">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="7672c-2781">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7672c-2782">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2782">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7672c-2783">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="7672c-2783">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2784">Az.Network</span></span>
* <span data-ttu-id="7672c-2785">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="7672c-2785">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7672c-2786">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7672c-2786">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7672c-2787">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7672c-2787">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7672c-2788">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7672c-2788">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7672c-2789">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7672c-2789">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7672c-2790">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7672c-2790">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7672c-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7672c-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7672c-2792">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7672c-2792">Az.PolicyInsights</span></span>
* <span data-ttu-id="7672c-2793">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2793">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2794">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2794">Az.Resources</span></span>
* <span data-ttu-id="7672c-2795">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="7672c-2795">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7672c-2796">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="7672c-2796">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7672c-2797">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7672c-2797">Az.ServiceBus</span></span>
* <span data-ttu-id="7672c-2798">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2798">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7672c-2799">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7672c-2799">Az.ServiceFabric</span></span>
* <span data-ttu-id="7672c-2800">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2800">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7672c-2801">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2801">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7672c-2802">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7672c-2802">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7672c-2803">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7672c-2803">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7672c-2804">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2804">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7672c-2805">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="7672c-2805">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7672c-2806">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7672c-2806">Az.Profile</span></span>
* <span data-ttu-id="7672c-2807">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="7672c-2807">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7672c-2808">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2808">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2809">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2809">Az.Compute</span></span>
* <span data-ttu-id="7672c-2810">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2810">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7672c-2811">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2811">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7672c-2812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7672c-2812">Az.DataLakeStore</span></span>
* <span data-ttu-id="7672c-2813">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="7672c-2813">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7672c-2814">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="7672c-2814">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7672c-2815">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="7672c-2815">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7672c-2816">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7672c-2816">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7672c-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="7672c-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2818">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2818">Az.Network</span></span>
* <span data-ttu-id="7672c-2819">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-2819">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7672c-2820">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2820">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2821">Az.Resources</span></span>
* <span data-ttu-id="7672c-2822">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2822">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7672c-2823">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2823">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7672c-2824">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="7672c-2824">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7672c-2825">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="7672c-2825">Azure.Storage</span></span>
* <span data-ttu-id="7672c-2826">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="7672c-2826">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7672c-2827">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7672c-2827">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7672c-2828">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7672c-2828">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7672c-2829">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="7672c-2829">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7672c-2830">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7672c-2830">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7672c-2831">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7672c-2831">Az.CognitiveServices</span></span>
* <span data-ttu-id="7672c-2832">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="7672c-2832">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7672c-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7672c-2833">Az.Compute</span></span>
* <span data-ttu-id="7672c-2834">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2834">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7672c-2835">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2835">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7672c-2836">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2836">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7672c-2837">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7672c-2837">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7672c-2838">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2838">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7672c-2839">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7672c-2839">Az.Network</span></span>
* <span data-ttu-id="7672c-2840">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="7672c-2840">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7672c-2841">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2841">new cmdlets added</span></span>
    - <span data-ttu-id="7672c-2842">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7672c-2842">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7672c-2843">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7672c-2843">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7672c-2844">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7672c-2844">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7672c-2845">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7672c-2845">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7672c-2846">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-2846">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7672c-2847">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7672c-2847">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7672c-2848">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2848">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7672c-2849">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2849">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7672c-2850">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2850">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7672c-2851">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7672c-2851">Az.RedisCache</span></span>
* <span data-ttu-id="7672c-2852">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="7672c-2852">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7672c-2853">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2853">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7672c-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7672c-2854">Az.Resources</span></span>
* <span data-ttu-id="7672c-2855">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="7672c-2855">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7672c-2856">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2856">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7672c-2857">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7672c-2857">Az.Sql</span></span>
* <span data-ttu-id="7672c-2858">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="7672c-2858">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7672c-2859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7672c-2859">Az.Websites</span></span>
* <span data-ttu-id="7672c-2860">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="7672c-2860">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7672c-2861">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="7672c-2861">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7672c-2862">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="7672c-2862">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7672c-2863">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="7672c-2863">Initial Release</span></span>
