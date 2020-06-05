---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 8d53923f76506469cdc2c111faf7c4568b54f7de
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/02/2020
ms.locfileid: "84294802"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="45021-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="45021-103">Azure PowerShell release notes</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="45021-104">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="45021-104">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-105">Az.Accounts</span></span>
* <span data-ttu-id="45021-106">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="45021-106">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="45021-107">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="45021-107">Az.AnalysisServices</span></span>
* <span data-ttu-id="45021-108">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-108">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="45021-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-109">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-110">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-110">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="45021-111">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="45021-111">Az.Billing</span></span>
* <span data-ttu-id="45021-112">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-112">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="45021-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="45021-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="45021-114">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="45021-114">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="45021-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-115">Az.DataFactory</span></span>
* <span data-ttu-id="45021-116">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-116">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="45021-117">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="45021-117">Az.DataShare</span></span>
* <span data-ttu-id="45021-118">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-118">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="45021-119">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="45021-119">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="45021-120">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-120">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="45021-121">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="45021-121">Az.OperationalInsights</span></span>
* <span data-ttu-id="45021-122">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-122">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="45021-123">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-123">Added optional parameters to</span></span> 
    - <span data-ttu-id="45021-124">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="45021-124">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="45021-125">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="45021-125">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="45021-126">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="45021-126">Az.PolicyInsights</span></span>
* <span data-ttu-id="45021-127">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-127">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="45021-128">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="45021-128">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="45021-129">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-129">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="45021-130">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="45021-130">Az.PrivateDns</span></span>
* <span data-ttu-id="45021-131">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-131">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-132">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-132">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-133">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-133">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="45021-134">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-134">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-135">Az.Resources</span></span>
* <span data-ttu-id="45021-136">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-136">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="45021-137">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="45021-137">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="45021-138">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-138">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="45021-139">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-139">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="45021-140">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-140">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-141">Az.Sql</span></span>
* <span data-ttu-id="45021-142">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-142">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="45021-143">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-143">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="45021-144">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-144">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-145">Az.Storage</span></span>
* <span data-ttu-id="45021-146">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-146">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="45021-147">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="45021-147">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="45021-148">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="45021-148">Highlights since the last release</span></span>
* <span data-ttu-id="45021-149">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="45021-149">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="45021-150">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-150">General availability of Az.Functions</span></span> 
* <span data-ttu-id="45021-151">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="45021-151">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-152">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-152">Az.Accounts</span></span>
* <span data-ttu-id="45021-153">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-153">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="45021-154">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="45021-154">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="45021-155">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="45021-155">Az.Aks</span></span>
* <span data-ttu-id="45021-156">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="45021-156">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="45021-157">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-157">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="45021-158">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="45021-158">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="45021-159">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-159">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-160">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-160">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="45021-161">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="45021-161">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="45021-162">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-162">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="45021-163">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-163">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="45021-164">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-164">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="45021-165">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-165">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="45021-166">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-166">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="45021-167">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-167">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="45021-168">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-168">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="45021-169">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-169">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="45021-170">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="45021-170">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="45021-171">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="45021-171">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="45021-172">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="45021-172">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="45021-173">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="45021-173">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="45021-174">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="45021-174">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="45021-175">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="45021-175">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="45021-176">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="45021-176">Az.ApplicationInsights</span></span>
* <span data-ttu-id="45021-177">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="45021-177">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="45021-178">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-178">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="45021-179">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-179">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="45021-180">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="45021-180">Az.Batch</span></span>
* <span data-ttu-id="45021-181">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-181">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="45021-182">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-182">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="45021-183">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-183">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="45021-184">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="45021-184">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="45021-185">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="45021-185">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="45021-186">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="45021-186">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="45021-187">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="45021-187">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="45021-188">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="45021-188">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="45021-189">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="45021-189">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-190">Az.Compute</span></span>
* <span data-ttu-id="45021-191">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-191">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="45021-192">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-192">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="45021-193">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="45021-193">Breaking changes</span></span>
    - <span data-ttu-id="45021-194">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-194">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="45021-195">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-195">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="45021-196">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-196">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="45021-197">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-197">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="45021-198">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-198">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="45021-199">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-199">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="45021-200">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-200">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="45021-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-201">Az.DataFactory</span></span>
* <span data-ttu-id="45021-202">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-202">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="45021-203">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="45021-203">Az.FrontDoor</span></span>
* <span data-ttu-id="45021-204">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-204">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="45021-205">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-205">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="45021-206">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-206">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="45021-207">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-207">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="45021-208">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="45021-208">Az.Functions</span></span>
* <span data-ttu-id="45021-209">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-209">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="45021-210">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="45021-210">Az.HDInsight</span></span>
* <span data-ttu-id="45021-211">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="45021-211">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="45021-212">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="45021-212">Az.HealthcareApis</span></span>
* <span data-ttu-id="45021-213">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="45021-213">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-214">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-214">Az.IotHub</span></span>
* <span data-ttu-id="45021-215">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-215">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="45021-216">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="45021-216">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="45021-217">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-217">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="45021-218">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-218">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="45021-219">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="45021-219">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="45021-220">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-220">New cmdlets are:</span></span>
    - <span data-ttu-id="45021-221">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="45021-221">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="45021-222">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="45021-222">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="45021-223">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="45021-223">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="45021-224">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="45021-224">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="45021-225">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-225">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="45021-226">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-226">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-227">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-227">Az.KeyVault</span></span>
* <span data-ttu-id="45021-228">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="45021-228">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="45021-229">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-229">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="45021-230">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="45021-230">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="45021-231">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-231">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="45021-232">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="45021-232">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="45021-233">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="45021-233">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="45021-234">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-234">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-235">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-235">Az.Monitor</span></span>
* <span data-ttu-id="45021-236">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="45021-236">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="45021-237">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-237">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="45021-238">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-238">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="45021-239">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="45021-239">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="45021-240">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="45021-240">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="45021-241">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="45021-241">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="45021-242">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-242">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-243">Az.Network</span></span>
* <span data-ttu-id="45021-244">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-244">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="45021-245">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="45021-245">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="45021-246">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="45021-246">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="45021-247">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="45021-247">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="45021-248">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-248">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="45021-249">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-249">New cmdlets added:</span></span>
        - <span data-ttu-id="45021-250">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="45021-250">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="45021-251">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="45021-251">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="45021-252">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="45021-252">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="45021-253">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="45021-253">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="45021-254">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-254">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="45021-255">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-255">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="45021-256">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-256">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="45021-257">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="45021-257">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="45021-258">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="45021-258">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="45021-259">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-259">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="45021-260">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="45021-260">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="45021-261">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="45021-261">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="45021-262">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="45021-262">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="45021-263">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="45021-263">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="45021-264">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="45021-264">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="45021-265">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-265">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="45021-266">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-266">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="45021-267">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-267">Updated cmdlet:</span></span>
        - <span data-ttu-id="45021-268">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="45021-268">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="45021-269">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="45021-269">Az.OperationalInsights</span></span>
* <span data-ttu-id="45021-270">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-270">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="45021-271">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-271">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="45021-272">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="45021-272">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="45021-273">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="45021-273">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="45021-274">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="45021-274">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="45021-275">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-275">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="45021-276">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-276">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="45021-277">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-277">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-279">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-279">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="45021-280">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-280">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="45021-281">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-281">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="45021-282">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-282">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="45021-283">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-283">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-284">Az.Resources</span></span>
* <span data-ttu-id="45021-285">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-285">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="45021-286">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-286">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="45021-287">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="45021-287">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="45021-288">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="45021-288">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="45021-289">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="45021-289">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="45021-290">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="45021-290">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="45021-291">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="45021-291">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="45021-292">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="45021-292">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="45021-293">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-293">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="45021-294">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-294">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="45021-295">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-295">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="45021-296">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-296">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="45021-297">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-297">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="45021-298">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-298">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="45021-299">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="45021-299">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="45021-300">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-300">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="45021-301">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="45021-301">'New-AzDeployment'</span></span>
    - <span data-ttu-id="45021-302">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="45021-302">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="45021-303">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="45021-303">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="45021-304">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="45021-304">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="45021-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-306">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-306">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-307">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-307">Az.Sql</span></span>
* <span data-ttu-id="45021-308">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-308">Enhance performance of:</span></span>
    - <span data-ttu-id="45021-309">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="45021-309">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="45021-310">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="45021-310">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="45021-311">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="45021-311">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="45021-312">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="45021-312">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="45021-313">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="45021-313">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="45021-314">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="45021-314">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="45021-315">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="45021-315">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="45021-316">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="45021-316">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="45021-317">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-317">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="45021-318">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-318">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-319">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-319">Az.Storage</span></span>
* <span data-ttu-id="45021-320">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-320">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="45021-321">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="45021-321">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="45021-322">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="45021-322">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="45021-323">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-323">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="45021-324">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="45021-324">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="45021-325">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-325">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="45021-326">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="45021-326">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="45021-327">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="45021-327">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="45021-328">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="45021-328">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="45021-329">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="45021-329">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="45021-330">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="45021-330">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="45021-331">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="45021-331">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="45021-332">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="45021-332">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="45021-333">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-333">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="45021-334">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="45021-334">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="45021-335">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="45021-335">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="45021-336">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-336">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="45021-337">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="45021-337">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="45021-338">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="45021-338">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="45021-339">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-339">Supported failover Storage account</span></span>
    - <span data-ttu-id="45021-340">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="45021-340">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="45021-341">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-341">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="45021-342">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-342">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="45021-343">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-343">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="45021-344">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="45021-344">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="45021-345">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="45021-345">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="45021-346">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="45021-346">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="45021-347">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="45021-347">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="45021-348">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="45021-348">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="45021-349">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="45021-349">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="45021-350">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="45021-350">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="45021-351">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="45021-351">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="45021-352">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="45021-352">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="45021-353">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="45021-353">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="45021-354">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="45021-354">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="45021-355">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="45021-355">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="45021-356">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="45021-356">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="45021-357">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="45021-357">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="45021-358">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="45021-358">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="45021-359">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="45021-359">Az.TrafficManager</span></span>
* <span data-ttu-id="45021-360">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-360">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-361">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-361">Az.Websites</span></span>
* <span data-ttu-id="45021-362">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-362">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="45021-363">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="45021-363">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="45021-364">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="45021-364">Highlights since the last release</span></span>
* <span data-ttu-id="45021-365">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="45021-365">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-366">Az.Accounts</span></span>
* <span data-ttu-id="45021-367">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="45021-367">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="45021-368">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-368">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-369">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-369">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="45021-370">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-370">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="45021-371">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="45021-371">Az.Cdn</span></span>
* <span data-ttu-id="45021-372">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-372">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="45021-373">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="45021-373">Az.CognitiveServices</span></span>
* <span data-ttu-id="45021-374">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="45021-374">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-375">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-375">Az.Compute</span></span>
* <span data-ttu-id="45021-376">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-376">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="45021-377">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="45021-377">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-378">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-378">Az.IotHub</span></span>
* <span data-ttu-id="45021-379">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-379">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="45021-380">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="45021-380">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="45021-381">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="45021-381">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="45021-382">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-382">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="45021-383">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-383">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="45021-384">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="45021-384">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="45021-385">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="45021-385">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="45021-386">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="45021-386">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="45021-387">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-387">New cmdlets are:</span></span>
    - <span data-ttu-id="45021-388">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="45021-388">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="45021-389">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="45021-389">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="45021-390">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="45021-390">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="45021-391">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="45021-391">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="45021-392">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-392">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-393">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-393">Az.KeyVault</span></span>
* <span data-ttu-id="45021-394">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-394">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="45021-395">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="45021-395">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="45021-396">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="45021-396">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="45021-397">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-397">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="45021-398">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="45021-398">Az.Maintenance</span></span>
* <span data-ttu-id="45021-399">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="45021-399">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-400">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-400">Az.Monitor</span></span>
* <span data-ttu-id="45021-401">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-401">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="45021-402">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="45021-402">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="45021-403">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="45021-403">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="45021-404">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="45021-404">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="45021-405">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="45021-405">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="45021-406">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="45021-406">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="45021-407">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="45021-407">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="45021-408">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="45021-408">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-409">Az.Network</span></span>
* <span data-ttu-id="45021-410">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-410">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="45021-411">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="45021-411">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="45021-412">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="45021-412">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="45021-413">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="45021-413">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="45021-414">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="45021-414">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="45021-415">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-415">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="45021-416">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="45021-416">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="45021-417">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="45021-417">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="45021-418">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-418">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="45021-419">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-419">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="45021-420">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="45021-420">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="45021-421">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-421">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="45021-422">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-422">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="45021-423">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-423">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="45021-424">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="45021-424">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="45021-425">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="45021-425">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="45021-426">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="45021-426">Az.PolicyInsights</span></span>
* <span data-ttu-id="45021-427">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-427">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="45021-428">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-428">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="45021-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-429">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-430">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-430">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-431">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-431">Az.Sql</span></span>
* <span data-ttu-id="45021-432">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-432">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="45021-433">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-433">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-434">Az.Storage</span></span>
* <span data-ttu-id="45021-435">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-435">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="45021-436">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-436">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="45021-437">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="45021-437">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="45021-438">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="45021-438">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="45021-439">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="45021-439">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="45021-440">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="45021-440">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="45021-441">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="45021-441">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="45021-442">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="45021-442">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="45021-443">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="45021-443">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="45021-444">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="45021-444">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="45021-445">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="45021-445">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="45021-446">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="45021-446">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="45021-447">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="45021-447">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="45021-448">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="45021-448">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="45021-449">Genel</span><span class="sxs-lookup"><span data-stu-id="45021-449">General</span></span>
* <span data-ttu-id="45021-450">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="45021-450">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="45021-451">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="45021-451">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="45021-452">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="45021-452">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="45021-453">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="45021-453">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="45021-454">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="45021-454">Az.Billing</span></span>
  - <span data-ttu-id="45021-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-455">Az.Compute</span></span>
  - <span data-ttu-id="45021-456">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="45021-456">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="45021-457">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="45021-457">Az.EventHub</span></span>
  - <span data-ttu-id="45021-458">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-458">Az.IotHub</span></span>
  - <span data-ttu-id="45021-459">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-459">Az.KeyVault</span></span>
  - <span data-ttu-id="45021-460">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-460">Az.Monitor</span></span>
  - <span data-ttu-id="45021-461">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-461">Az.Network</span></span>
  - <span data-ttu-id="45021-462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-462">Az.Resources</span></span>
  - <span data-ttu-id="45021-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-463">Az.Storage</span></span>
  - <span data-ttu-id="45021-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-464">Az.Websites</span></span>
* <span data-ttu-id="45021-465">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-465">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="45021-466">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="45021-466">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="45021-467">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="45021-467">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="45021-468">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="45021-468">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-469">Az.Accounts</span></span>
* <span data-ttu-id="45021-470">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="45021-470">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-471">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-471">Az.Compute</span></span>
* <span data-ttu-id="45021-472">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-472">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="45021-473">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="45021-473">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="45021-474">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="45021-474">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="45021-475">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-475">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="45021-476">[#11354]</span><span class="sxs-lookup"><span data-stu-id="45021-476">[#11354]</span></span>
* <span data-ttu-id="45021-477">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-477">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="45021-478">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="45021-478">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="45021-479">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="45021-479">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="45021-480">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="45021-480">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="45021-481">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="45021-481">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="45021-482">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-482">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="45021-483">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="45021-483">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="45021-484">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-484">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="45021-485">[#11257]</span><span class="sxs-lookup"><span data-stu-id="45021-485">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-486">Az.DataFactory</span></span>
* <span data-ttu-id="45021-487">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-487">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="45021-488">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-488">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-489">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-490">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-490">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="45021-491">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-491">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="45021-492">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="45021-492">Az.HDInsight</span></span>
* <span data-ttu-id="45021-493">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-493">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-494">Az.IotHub</span></span>
* <span data-ttu-id="45021-495">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-495">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="45021-496">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-496">New Cmdlets are:</span></span>
    - <span data-ttu-id="45021-497">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="45021-497">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="45021-498">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="45021-498">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-499">Az.KeyVault</span></span>
* <span data-ttu-id="45021-500">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-500">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-501">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-501">Az.Monitor</span></span>
* <span data-ttu-id="45021-502">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-502">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-503">Az.Network</span></span>
* <span data-ttu-id="45021-504">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-504">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="45021-505">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="45021-505">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="45021-506">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="45021-506">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="45021-507">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="45021-507">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="45021-508">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="45021-508">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="45021-509">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-509">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="45021-510">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="45021-510">Az.PolicyInsights</span></span>
* <span data-ttu-id="45021-511">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-511">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-512">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-513">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-513">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="45021-514">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-514">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="45021-515">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-515">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="45021-516">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-516">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="45021-517">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-517">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="45021-518">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-518">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-519">Az.Resources</span></span>
* <span data-ttu-id="45021-520">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="45021-520">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="45021-521">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-521">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="45021-522">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-522">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="45021-523">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-523">Added example.</span></span>
* <span data-ttu-id="45021-524">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="45021-524">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="45021-525">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="45021-525">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-526">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-526">Az.Sql</span></span>
* <span data-ttu-id="45021-527">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-527">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="45021-528">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-528">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="45021-529">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="45021-529">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="45021-530">Az.Support</span><span class="sxs-lookup"><span data-stu-id="45021-530">Az.Support</span></span>
* <span data-ttu-id="45021-531">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-531">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-532">Az.Websites</span></span>
* <span data-ttu-id="45021-533">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-533">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="45021-534">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="45021-534">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="45021-535">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="45021-535">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="45021-536">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="45021-536">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="45021-537">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="45021-537">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="45021-538">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="45021-538">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-539">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-539">Az.Accounts</span></span>
* <span data-ttu-id="45021-540">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="45021-540">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="45021-541">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="45021-541">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="45021-542">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-542">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="45021-543">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-543">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-544">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="45021-544">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="45021-545">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="45021-545">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="45021-546">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-546">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="45021-547">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="45021-547">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-548">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-548">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-549">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-549">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-550">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-550">Az.IotHub</span></span>
* <span data-ttu-id="45021-551">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-551">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="45021-552">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-552">New Cmdlets are:</span></span>
    - <span data-ttu-id="45021-553">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="45021-553">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="45021-554">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="45021-554">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="45021-555">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="45021-555">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="45021-556">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="45021-556">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="45021-557">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-557">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="45021-558">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-558">New Cmdlets are:</span></span>
    - <span data-ttu-id="45021-559">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="45021-559">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="45021-560">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="45021-560">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="45021-561">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="45021-561">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="45021-562">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="45021-562">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="45021-563">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-563">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="45021-564">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-564">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="45021-565">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-565">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="45021-566">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-566">New Cmdlets are:</span></span>
    - <span data-ttu-id="45021-567">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="45021-567">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="45021-568">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="45021-568">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="45021-569">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-569">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-570">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-570">Az.Monitor</span></span>
* <span data-ttu-id="45021-571">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="45021-571">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-572">Az.Network</span></span>
* <span data-ttu-id="45021-573">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-573">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="45021-574">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-574">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="45021-575">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="45021-575">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="45021-576">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-576">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-577">Az.Resources</span></span>
* <span data-ttu-id="45021-578">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-578">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="45021-579">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="45021-579">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="45021-580">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="45021-580">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="45021-581">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="45021-581">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="45021-582">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-582">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="45021-583">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-583">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="45021-584">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-584">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="45021-585">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="45021-585">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="45021-586">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="45021-586">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="45021-587">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="45021-587">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="45021-588">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="45021-588">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="45021-589">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-589">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="45021-590">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="45021-590">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="45021-591">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="45021-591">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-592">Az.Sql</span></span>
* <span data-ttu-id="45021-593">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-593">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="45021-594">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-594">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="45021-595">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="45021-595">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="45021-596">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="45021-596">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="45021-597">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="45021-597">Remove an LTR backup</span></span>
    - <span data-ttu-id="45021-598">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="45021-598">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="45021-599">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-599">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="45021-600">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-600">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="45021-601">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-601">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-602">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-602">Az.Storage</span></span>
* <span data-ttu-id="45021-603">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-603">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="45021-604">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="45021-604">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="45021-605">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-605">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="45021-606">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="45021-606">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="45021-607">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="45021-607">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-608">Az.Websites</span></span>
* <span data-ttu-id="45021-609">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-609">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="45021-610">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="45021-610">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="45021-611">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-611">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="45021-612">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="45021-612">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="45021-613">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-613">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="45021-614">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="45021-614">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="45021-615">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="45021-615">Highlights since the last major release</span></span>
* <span data-ttu-id="45021-616">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-616">Updated client side telemetry.</span></span>
* <span data-ttu-id="45021-617">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-617">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="45021-618">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-618">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-619">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-619">Az.Accounts</span></span>
* <span data-ttu-id="45021-620">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-620">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-621">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-621">Az.Automation</span></span>
* <span data-ttu-id="45021-622">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-622">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="45021-623">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="45021-623">Az.CognitiveServices</span></span>
* <span data-ttu-id="45021-624">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-624">Updated SDK to 7.0</span></span>
* <span data-ttu-id="45021-625">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-625">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-626">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-626">Az.Compute</span></span>
* <span data-ttu-id="45021-627">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="45021-627">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="45021-628">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="45021-628">Az.FrontDoor</span></span>
* <span data-ttu-id="45021-629">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-629">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-630">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-630">Az.IotHub</span></span>
* <span data-ttu-id="45021-631">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-631">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="45021-632">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-632">New Cmdlets are:</span></span>
    - <span data-ttu-id="45021-633">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="45021-633">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="45021-634">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="45021-634">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="45021-635">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="45021-635">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="45021-636">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="45021-636">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-637">Az.KeyVault</span></span>
* <span data-ttu-id="45021-638">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-638">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-639">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-639">Az.Monitor</span></span>
* <span data-ttu-id="45021-640">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-640">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="45021-641">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-641">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="45021-642">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="45021-642">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-643">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-643">Az.Network</span></span>
* <span data-ttu-id="45021-644">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-644">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="45021-645">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-645">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="45021-646">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-646">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="45021-647">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="45021-647">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="45021-648">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="45021-648">No new cmdlets are added.</span></span> <span data-ttu-id="45021-649">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="45021-649">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-650">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-650">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-651">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-651">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-652">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-652">Az.Resources</span></span>
* <span data-ttu-id="45021-653">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="45021-653">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="45021-654">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45021-654">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="45021-655">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="45021-655">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="45021-656">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="45021-656">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="45021-657">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-657">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="45021-658">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-658">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="45021-659">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-659">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="45021-660">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-660">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-661">Az.Sql</span></span>
* <span data-ttu-id="45021-662">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-662">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="45021-663">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-663">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="45021-664">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="45021-664">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="45021-665">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="45021-665">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="45021-666">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-666">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="45021-667">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="45021-667">Az.StorageSync</span></span>
* <span data-ttu-id="45021-668">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-668">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="45021-669">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="45021-669">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="45021-670">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="45021-670">Highlights since the last major release</span></span>
* <span data-ttu-id="45021-671">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="45021-671">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="45021-672">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-672">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-673">Az.Accounts</span></span>
* <span data-ttu-id="45021-674">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="45021-674">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="45021-675">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-675">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="45021-676">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-676">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-677">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="45021-677">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="45021-678">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="45021-678">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="45021-679">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-679">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="45021-680">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-680">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-681">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-681">Az.Compute</span></span>
* <span data-ttu-id="45021-682">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="45021-682">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="45021-683">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-683">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="45021-684">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-684">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="45021-685">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="45021-685">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="45021-686">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-686">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-687">Az.DataFactory</span></span>
* <span data-ttu-id="45021-688">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-688">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="45021-689">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="45021-689">Az.DeploymentManager</span></span>
* <span data-ttu-id="45021-690">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="45021-690">Adds LIST operations for resources</span></span>
* <span data-ttu-id="45021-691">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="45021-691">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="45021-692">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="45021-692">Az.HDInsight</span></span>
* <span data-ttu-id="45021-693">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-693">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-694">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-694">Az.KeyVault</span></span>
* <span data-ttu-id="45021-695">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-695">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-696">Az.Network</span></span>
* <span data-ttu-id="45021-697">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-697">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="45021-698">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="45021-698">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="45021-699">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-699">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="45021-700">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-700">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="45021-701">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="45021-701">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="45021-702">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-702">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="45021-703">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-703">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="45021-704">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-704">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="45021-705">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-705">New cmdlets added:</span></span>
        - <span data-ttu-id="45021-706">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="45021-706">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="45021-707">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-707">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="45021-708">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="45021-708">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="45021-709">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-709">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="45021-710">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="45021-710">Az.PolicyInsights</span></span>
* <span data-ttu-id="45021-711">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="45021-711">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="45021-712">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-712">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="45021-713">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-713">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="45021-714">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-714">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-715">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-715">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-716">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-716">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="45021-717">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="45021-717">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-718">Az.Resources</span></span>
* <span data-ttu-id="45021-719">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="45021-719">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="45021-720">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-720">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-721">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-721">Az.Sql</span></span>
<span data-ttu-id="45021-722">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-722">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-723">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-723">Az.Storage</span></span>
* <span data-ttu-id="45021-724">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="45021-724">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="45021-725">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-725">New-AzStorageAccount</span></span>
* <span data-ttu-id="45021-726">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="45021-726">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="45021-727">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-727">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-728">Az.Websites</span></span>
* <span data-ttu-id="45021-729">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="45021-729">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="45021-730">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-730">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="45021-731">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="45021-731">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-732">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-732">Az.Accounts</span></span>
* <span data-ttu-id="45021-733">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-733">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="45021-734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="45021-734">Az.Cdn</span></span>
* <span data-ttu-id="45021-735">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="45021-735">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-736">Az.Compute</span></span>
* <span data-ttu-id="45021-737">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-737">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="45021-738">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="45021-738">Az.ContainerInstance</span></span>
* <span data-ttu-id="45021-739">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-739">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="45021-740">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="45021-740">Az.DataBoxEdge</span></span>
* <span data-ttu-id="45021-741">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-741">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="45021-742">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="45021-742">Get the Edge Storage Container</span></span>
* <span data-ttu-id="45021-743">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-743">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="45021-744">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="45021-744">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="45021-745">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-745">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="45021-746">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="45021-746">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="45021-747">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-747">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="45021-748">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="45021-748">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="45021-749">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-749">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="45021-750">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="45021-750">Get the Edge Storage Account</span></span>
* <span data-ttu-id="45021-751">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-751">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="45021-752">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="45021-752">Create new Edge Storage Account</span></span>
* <span data-ttu-id="45021-753">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-753">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="45021-754">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="45021-754">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="45021-755">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="45021-755">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="45021-756">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="45021-756">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="45021-757">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-757">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="45021-758">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="45021-758">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-759">Az.DataFactory</span></span>
* <span data-ttu-id="45021-760">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-760">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="45021-761">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-761">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="45021-762">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-762">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="45021-763">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="45021-763">Az.DevTestLabs</span></span>
* <span data-ttu-id="45021-764">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-764">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="45021-765">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="45021-765">Az.EventHub</span></span>
* <span data-ttu-id="45021-766">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-766">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="45021-767">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="45021-767">Az.HDInsight</span></span>
* <span data-ttu-id="45021-768">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-768">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="45021-769">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="45021-769">Az.MachineLearning</span></span>
* <span data-ttu-id="45021-770">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-770">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="45021-771">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="45021-771">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="45021-772">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="45021-772">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="45021-773">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="45021-773">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="45021-774">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="45021-774">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="45021-775">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="45021-775">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="45021-776">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="45021-776">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="45021-777">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="45021-777">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-778">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-778">Az.Network</span></span>
* <span data-ttu-id="45021-779">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="45021-779">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-780">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-780">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-781">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-781">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="45021-782">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-782">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="45021-783">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-783">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="45021-784">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-784">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-785">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-785">Az.Resources</span></span>
* <span data-ttu-id="45021-786">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-786">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-787">Az.Sql</span></span>
* <span data-ttu-id="45021-788">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-788">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="45021-789">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-789">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="45021-790">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="45021-790">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="45021-791">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-791">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-792">Az.Storage</span></span>
* <span data-ttu-id="45021-793">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-793">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="45021-794">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="45021-794">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="45021-795">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="45021-795">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="45021-796">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-796">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="45021-797">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="45021-797">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="45021-798">Genel</span><span class="sxs-lookup"><span data-stu-id="45021-798">General</span></span>
* <span data-ttu-id="45021-799">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-799">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-800">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-800">Az.Accounts</span></span>
* <span data-ttu-id="45021-801">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="45021-801">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="45021-802">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="45021-802">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="45021-803">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="45021-803">Az.Batch</span></span>
* <span data-ttu-id="45021-804">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-804">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-805">Az.DataFactory</span></span>
* <span data-ttu-id="45021-806">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-806">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="45021-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="45021-807">Az.FrontDoor</span></span>
* <span data-ttu-id="45021-808">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-808">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="45021-809">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-809">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="45021-810">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="45021-810">Az.HealthcareApis</span></span>
* <span data-ttu-id="45021-811">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="45021-811">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-812">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-812">Az.KeyVault</span></span>
* <span data-ttu-id="45021-813">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-813">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="45021-814">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="45021-814">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="45021-815">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-815">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-816">Az.Monitor</span></span>
* <span data-ttu-id="45021-817">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-817">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="45021-818">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="45021-818">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="45021-819">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="45021-819">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-820">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-820">Az.Network</span></span>
* <span data-ttu-id="45021-821">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-821">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-822">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-822">Az.Resources</span></span>
* <span data-ttu-id="45021-823">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-823">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="45021-824">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-824">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-825">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-825">Az.Sql</span></span>
* <span data-ttu-id="45021-826">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="45021-826">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-827">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-827">Az.Storage</span></span>
* <span data-ttu-id="45021-828">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="45021-828">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="45021-829">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="45021-829">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="45021-830">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="45021-830">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="45021-831">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="45021-831">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="45021-832">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="45021-832">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="45021-833">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-833">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="45021-834">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-834">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="45021-835">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="45021-835">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="45021-836">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="45021-836">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="45021-837">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-837">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="45021-838">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="45021-838">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="45021-839">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-839">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="45021-840">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="45021-840">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="45021-841">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="45021-841">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="45021-842">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="45021-842">Highlights since the last major release</span></span>
* <span data-ttu-id="45021-843">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="45021-843">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="45021-844">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="45021-844">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-845">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-845">Az.Compute</span></span>
* <span data-ttu-id="45021-846">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="45021-846">VM Reapply feature</span></span>
    - <span data-ttu-id="45021-847">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="45021-847">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="45021-848">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="45021-848">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="45021-849">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="45021-849">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="45021-850">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="45021-850">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="45021-851">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-851">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="45021-852">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-852">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="45021-853">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-853">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="45021-854">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-854">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="45021-855">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-855">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="45021-856">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-856">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="45021-857">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="45021-857">Az.DataBoxEdge</span></span>
* <span data-ttu-id="45021-858">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-858">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="45021-859">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="45021-859">Get the Order</span></span>
* <span data-ttu-id="45021-860">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-860">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="45021-861">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="45021-861">Create new Order</span></span>
* <span data-ttu-id="45021-862">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-862">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="45021-863">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="45021-863">Remove the Order</span></span>
* <span data-ttu-id="45021-864">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="45021-864">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="45021-865">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="45021-865">Now creates Local Share</span></span>
* <span data-ttu-id="45021-866">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-866">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="45021-867">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="45021-867">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="45021-868">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-868">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="45021-869">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="45021-869">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="45021-870">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-870">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="45021-871">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="45021-871">Gets the information about Triggers</span></span>
* <span data-ttu-id="45021-872">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-872">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="45021-873">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="45021-873">Create new Triggers</span></span>
* <span data-ttu-id="45021-874">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-874">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="45021-875">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="45021-875">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-876">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-876">Az.DataFactory</span></span>
* <span data-ttu-id="45021-877">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-877">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="45021-878">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-878">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-879">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-879">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-880">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-880">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="45021-881">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="45021-881">Az.EventHub</span></span>
* <span data-ttu-id="45021-882">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-882">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="45021-883">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="45021-883">Az.FrontDoor</span></span>
* <span data-ttu-id="45021-884">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-884">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="45021-885">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-885">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="45021-886">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-886">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="45021-887">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="45021-887">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-888">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-888">Az.Network</span></span>
* <span data-ttu-id="45021-889">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-889">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="45021-890">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="45021-890">Az.PrivateDns</span></span>
* <span data-ttu-id="45021-891">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-891">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-892">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-892">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-893">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-893">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="45021-894">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="45021-894">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="45021-895">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-895">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="45021-896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="45021-896">Az.RedisCache</span></span>
* <span data-ttu-id="45021-897">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-897">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="45021-898">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-898">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="45021-899">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-899">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-900">Az.Resources</span></span>
- <span data-ttu-id="45021-901">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-901">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="45021-902">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-902">Updated create policy definition help example</span></span>
- <span data-ttu-id="45021-903">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-903">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="45021-904">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-904">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="45021-905">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-905">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-906">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-906">Az.Sql</span></span>
* <span data-ttu-id="45021-907">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-907">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="45021-908">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-908">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="45021-909">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="45021-909">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="45021-910">Genel</span><span class="sxs-lookup"><span data-stu-id="45021-910">General</span></span>
* <span data-ttu-id="45021-911">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="45021-911">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-912">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-912">Az.Accounts</span></span>
* <span data-ttu-id="45021-913">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="45021-913">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="45021-914">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="45021-914">Az.Advisor</span></span>
* <span data-ttu-id="45021-915">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-915">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="45021-916">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="45021-916">Az.Batch</span></span>
* <span data-ttu-id="45021-917">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-917">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="45021-918">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="45021-918">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="45021-919">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-919">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="45021-920">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="45021-920">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="45021-921">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="45021-921">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="45021-922">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="45021-922">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="45021-923">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="45021-923">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="45021-924">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="45021-924">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="45021-925">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="45021-925">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="45021-926">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-926">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="45021-927">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="45021-927">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="45021-928">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="45021-928">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="45021-929">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-929">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="45021-930">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="45021-930">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="45021-931">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-931">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="45021-932">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-932">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="45021-933">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-933">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="45021-934">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-934">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="45021-935">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-935">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="45021-936">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="45021-936">This operation is no longer supported.</span></span>
* <span data-ttu-id="45021-937">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-937">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="45021-938">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-938">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="45021-939">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-939">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="45021-940">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="45021-940">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="45021-941">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="45021-941">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="45021-942">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="45021-942">New non-verified images are also now returned.</span></span> <span data-ttu-id="45021-943">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="45021-943">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="45021-944">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-944">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="45021-945">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="45021-945">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="45021-946">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="45021-946">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="45021-947">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-947">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="45021-948">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="45021-948">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="45021-949">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-949">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="45021-950">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-950">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="45021-951">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="45021-951">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="45021-952">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="45021-952">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="45021-953">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="45021-953">Az.Cdn</span></span>
* <span data-ttu-id="45021-954">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-954">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="45021-955">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-955">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-956">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-956">Az.Compute</span></span>
* <span data-ttu-id="45021-957">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="45021-957">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="45021-958">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="45021-958">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="45021-959">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="45021-959">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="45021-960">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="45021-960">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="45021-961">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-961">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="45021-962">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="45021-962">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="45021-963">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-963">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="45021-964">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="45021-964">Breaking changes</span></span>
    - <span data-ttu-id="45021-965">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="45021-965">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="45021-966">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="45021-966">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-967">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-967">Az.DataFactory</span></span>
* <span data-ttu-id="45021-968">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-968">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-969">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-969">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-970">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="45021-970">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="45021-971">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="45021-971">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="45021-972">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="45021-972">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="45021-973">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="45021-973">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="45021-974">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="45021-974">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="45021-975">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="45021-975">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="45021-976">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="45021-976">Az.FrontDoor</span></span>
* <span data-ttu-id="45021-977">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-977">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="45021-978">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="45021-978">Az.HDInsight</span></span>
* <span data-ttu-id="45021-979">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-979">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="45021-980">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-980">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="45021-981">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="45021-981">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="45021-982">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="45021-982">Removed five cmdlets:</span></span>
    - <span data-ttu-id="45021-983">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="45021-983">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="45021-984">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="45021-984">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="45021-985">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="45021-985">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="45021-986">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="45021-986">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="45021-987">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="45021-987">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="45021-988">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-988">Added three cmdlets:</span></span>
    - <span data-ttu-id="45021-989">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="45021-989">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="45021-990">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="45021-990">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="45021-991">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="45021-991">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="45021-992">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-992">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="45021-993">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-993">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="45021-994">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-994">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="45021-995">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-995">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="45021-996">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-996">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="45021-997">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-997">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="45021-998">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-998">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="45021-999">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-999">Added some scenario test cases.</span></span>
* <span data-ttu-id="45021-1000">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="45021-1000">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-1001">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-1001">Az.IotHub</span></span>
* <span data-ttu-id="45021-1002">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="45021-1002">Breaking changes:</span></span>
    - <span data-ttu-id="45021-1003">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="45021-1003">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="45021-1004">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1004">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="45021-1005">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="45021-1005">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="45021-1006">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1006">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="45021-1007">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1007">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="45021-1008">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1008">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="45021-1009">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="45021-1009">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="45021-1010">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="45021-1010">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="45021-1011">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="45021-1011">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="45021-1012">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1012">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="45021-1013">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="45021-1013">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="45021-1014">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1014">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-1015">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-1015">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-1016">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1016">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="45021-1017">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1017">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="45021-1018">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1018">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="45021-1019">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1019">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="45021-1020">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1020">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="45021-1021">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1021">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="45021-1022">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1022">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="45021-1023">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1023">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="45021-1024">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1024">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-1025">Az.Resources</span></span>
* <span data-ttu-id="45021-1026">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1026">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1027">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1027">Az.Network</span></span>
* <span data-ttu-id="45021-1028">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1028">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="45021-1029">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1029">Updated cmdlet:</span></span>
        - <span data-ttu-id="45021-1030">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1030">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="45021-1031">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1031">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="45021-1032">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1032">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="45021-1033">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1033">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="45021-1034">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1034">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="45021-1035">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-1035">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="45021-1036">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="45021-1036">New cmdlet:</span></span>
        - <span data-ttu-id="45021-1037">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="45021-1037">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="45021-1038">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1038">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="45021-1039">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1039">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="45021-1040">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1040">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="45021-1041">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1041">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="45021-1042">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1042">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="45021-1043">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1043">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="45021-1044">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1044">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="45021-1045">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-1045">New cmdlets added:</span></span>
        - <span data-ttu-id="45021-1046">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="45021-1046">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="45021-1047">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45021-1047">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="45021-1048">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45021-1048">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="45021-1049">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45021-1049">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="45021-1050">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="45021-1050">Set-AzVirtualHub</span></span>
* <span data-ttu-id="45021-1051">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1051">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="45021-1052">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1052">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="45021-1053">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1053">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="45021-1054">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1054">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="45021-1055">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1055">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="45021-1056">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1056">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="45021-1057">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1057">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="45021-1058">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-1058">New cmdlets added:</span></span>
        - <span data-ttu-id="45021-1059">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1059">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="45021-1060">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1060">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="45021-1061">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1061">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="45021-1062">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1062">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="45021-1063">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1063">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="45021-1064">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1064">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="45021-1065">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1065">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="45021-1066">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1066">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="45021-1067">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-1067">New cmdlets added:</span></span>
        - <span data-ttu-id="45021-1068">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="45021-1068">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="45021-1069">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="45021-1069">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="45021-1070">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="45021-1070">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="45021-1071">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="45021-1071">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="45021-1072">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="45021-1072">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="45021-1073">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="45021-1073">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="45021-1074">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1074">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="45021-1075">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1075">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="45021-1076">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1076">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="45021-1077">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1077">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="45021-1078">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1078">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="45021-1079">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1079">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="45021-1080">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1080">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="45021-1081">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1081">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="45021-1082">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1082">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="45021-1083">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="45021-1083">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="45021-1084">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1084">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="45021-1085">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-1085">New cmdlets added:</span></span>
        - <span data-ttu-id="45021-1086">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="45021-1086">New-AzIpGroup</span></span>
        - <span data-ttu-id="45021-1087">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="45021-1087">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="45021-1088">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="45021-1088">Get-AzIpGroup</span></span>
        - <span data-ttu-id="45021-1089">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="45021-1089">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="45021-1090">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-1090">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-1091">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1091">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1092">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1092">Az.Sql</span></span>
* <span data-ttu-id="45021-1093">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1093">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="45021-1094">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1094">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="45021-1095">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="45021-1095">Removed deprecated aliases:</span></span>
* <span data-ttu-id="45021-1096">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="45021-1096">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="45021-1097">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="45021-1097">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="45021-1098">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1098">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="45021-1099">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1099">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="45021-1100">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1100">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="45021-1101">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1101">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-1102">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-1102">Az.Storage</span></span>
* <span data-ttu-id="45021-1103">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="45021-1103">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="45021-1104">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1104">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="45021-1105">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1105">Set-AzStorageAccount</span></span>
* <span data-ttu-id="45021-1106">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="45021-1106">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="45021-1107">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="45021-1107">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="45021-1108">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="45021-1108">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="45021-1109">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1109">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="45021-1110">Genel</span><span class="sxs-lookup"><span data-stu-id="45021-1110">General</span></span>
* <span data-ttu-id="45021-1111">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="45021-1111">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-1112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-1112">Az.Accounts</span></span>
* <span data-ttu-id="45021-1113">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1113">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="45021-1114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-1114">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-1115">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1115">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="45021-1116">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-1117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-1117">Az.Automation</span></span>
* <span data-ttu-id="45021-1118">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1118">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="45021-1119">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="45021-1119">Az.Batch</span></span>
* <span data-ttu-id="45021-1120">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="45021-1120">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1121">Az.Compute</span></span>
* <span data-ttu-id="45021-1122">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1122">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="45021-1123">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1123">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="45021-1124">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1124">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="45021-1125">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1125">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-1126">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-1126">Az.DataFactory</span></span>
* <span data-ttu-id="45021-1127">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="45021-1127">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="45021-1128">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="45021-1128">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="45021-1129">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1129">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-1130">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-1130">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-1131">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1131">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="45021-1132">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="45021-1132">Az.HealthcareApis</span></span>
* <span data-ttu-id="45021-1133">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1133">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="45021-1134">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1134">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="45021-1135">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1135">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="45021-1136">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1136">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-1137">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-1137">Az.IotHub</span></span>
* <span data-ttu-id="45021-1138">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="45021-1138">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="45021-1139">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="45021-1139">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-1140">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-1140">Az.Monitor</span></span>
* <span data-ttu-id="45021-1141">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1141">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="45021-1142">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="45021-1142">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="45021-1143">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="45021-1143">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="45021-1144">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-1144">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1145">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1145">Az.Network</span></span>
* <span data-ttu-id="45021-1146">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1146">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="45021-1147">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1147">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="45021-1148">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-1148">New cmdlets added:</span></span>
        - <span data-ttu-id="45021-1149">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="45021-1149">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="45021-1150">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1150">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="45021-1151">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1151">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="45021-1152">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1152">Updated cmdlets:</span></span>
        - <span data-ttu-id="45021-1153">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1153">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="45021-1154">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1154">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="45021-1155">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1155">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="45021-1156">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1156">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="45021-1157">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="45021-1157">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="45021-1158">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="45021-1158">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="45021-1159">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="45021-1159">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="45021-1160">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="45021-1160">Az.RedisCache</span></span>
* <span data-ttu-id="45021-1161">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1161">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1162">Az.Sql</span></span>
* <span data-ttu-id="45021-1163">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1163">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-1164">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-1164">Az.Storage</span></span>
* <span data-ttu-id="45021-1165">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1165">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="45021-1166">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="45021-1166">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="45021-1167">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="45021-1167">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="45021-1168">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="45021-1168">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="45021-1169">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1169">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="45021-1170">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="45021-1170">Az.StorageSync</span></span>
* <span data-ttu-id="45021-1171">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1171">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-1172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-1172">Az.Websites</span></span>
* <span data-ttu-id="45021-1173">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="45021-1173">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="45021-1174">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1174">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="45021-1175">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-1175">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-1176">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1176">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="45021-1177">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1177">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="45021-1178">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="45021-1178">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-1179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-1179">Az.Automation</span></span>
* <span data-ttu-id="45021-1180">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1180">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="45021-1181">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1181">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="45021-1182">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1182">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1183">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1183">Az.Compute</span></span>
* <span data-ttu-id="45021-1184">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1184">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="45021-1185">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1185">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="45021-1186">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-1186">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="45021-1187">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1187">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="45021-1188">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1188">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="45021-1189">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1189">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="45021-1190">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1190">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="45021-1191">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1191">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="45021-1192">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1192">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-1193">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-1193">Az.DataFactory</span></span>
* <span data-ttu-id="45021-1194">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="45021-1194">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="45021-1195">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1195">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="45021-1196">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="45021-1196">Az.HDInsight</span></span>
* <span data-ttu-id="45021-1197">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="45021-1197">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-1198">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-1198">Az.IotHub</span></span>
* <span data-ttu-id="45021-1199">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1199">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="45021-1200">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1200">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="45021-1201">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45021-1201">New cmdlets are:</span></span>
    - <span data-ttu-id="45021-1202">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="45021-1202">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="45021-1203">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="45021-1203">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="45021-1204">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="45021-1204">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="45021-1205">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="45021-1205">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-1206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-1206">Az.Monitor</span></span>
* <span data-ttu-id="45021-1207">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="45021-1207">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="45021-1208">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="45021-1208">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="45021-1209">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="45021-1209">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="45021-1210">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="45021-1210">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="45021-1211">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1211">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="45021-1212">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1212">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="45021-1213">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="45021-1213">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="45021-1214">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="45021-1214">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="45021-1215">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1215">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="45021-1216">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="45021-1216">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="45021-1217">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1217">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="45021-1218">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="45021-1218">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="45021-1219">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1219">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="45021-1220">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="45021-1220">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="45021-1221">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="45021-1221">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="45021-1222">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="45021-1222">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="45021-1223">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="45021-1223">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="45021-1224">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="45021-1224">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="45021-1225">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1225">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="45021-1226">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1226">Overall improved help files</span></span>
* <span data-ttu-id="45021-1227">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1227">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1228">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1228">Az.Network</span></span>
* <span data-ttu-id="45021-1229">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1229">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="45021-1230">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1230">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="45021-1231">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1231">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="45021-1232">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1232">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="45021-1233">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1233">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="45021-1234">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1234">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="45021-1235">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1235">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="45021-1236">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1236">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="45021-1237">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1237">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="45021-1238">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1238">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="45021-1239">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1239">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="45021-1240">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="45021-1240">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="45021-1241">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1241">New cmdlets</span></span>
        - <span data-ttu-id="45021-1242">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="45021-1242">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="45021-1243">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1243">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="45021-1244">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1244">Updated cmdlet:</span></span>
        - <span data-ttu-id="45021-1245">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="45021-1245">New-VpnSite</span></span>
        - <span data-ttu-id="45021-1246">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="45021-1246">Update-VpnSite</span></span>
        - <span data-ttu-id="45021-1247">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1247">New-VpnConnection</span></span>
        - <span data-ttu-id="45021-1248">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1248">Update-VpnConnection</span></span>
* <span data-ttu-id="45021-1249">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1249">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-1250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-1250">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-1251">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1251">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="45021-1252">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1252">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-1253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-1253">Az.Resources</span></span>
* <span data-ttu-id="45021-1254">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1254">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="45021-1255">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-1255">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-1256">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1256">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="45021-1257">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="45021-1257">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="45021-1258">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="45021-1258">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="45021-1259">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="45021-1259">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="45021-1260">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="45021-1260">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="45021-1261">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="45021-1261">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="45021-1262">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="45021-1262">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="45021-1263">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="45021-1263">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="45021-1264">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="45021-1264">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="45021-1265">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="45021-1265">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="45021-1266">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="45021-1266">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="45021-1267">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="45021-1267">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="45021-1268">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="45021-1268">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="45021-1269">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="45021-1269">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="45021-1270">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="45021-1270">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="45021-1271">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1271">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="45021-1272">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="45021-1272">Az.SignalR</span></span>
* <span data-ttu-id="45021-1273">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1273">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1274">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1274">Az.Sql</span></span>
* <span data-ttu-id="45021-1275">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1275">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="45021-1276">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1276">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="45021-1277">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1277">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="45021-1278">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1278">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="45021-1279">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1279">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-1280">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-1280">Az.Storage</span></span>
* <span data-ttu-id="45021-1281">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1281">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="45021-1282">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1282">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="45021-1283">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="45021-1283">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="45021-1284">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="45021-1284">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="45021-1285">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1285">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="45021-1286">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="45021-1286">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="45021-1287">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1287">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="45021-1288">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="45021-1288">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="45021-1289">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="45021-1289">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="45021-1290">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="45021-1290">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="45021-1291">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="45021-1291">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-1292">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-1292">Az.Websites</span></span>
* <span data-ttu-id="45021-1293">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="45021-1293">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="45021-1294">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="45021-1294">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="45021-1295">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1295">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="45021-1296">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1296">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="45021-1297">Genel</span><span class="sxs-lookup"><span data-stu-id="45021-1297">General</span></span>
* <span data-ttu-id="45021-1298">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1298">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-1299">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-1299">Az.Accounts</span></span>
* <span data-ttu-id="45021-1300">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="45021-1300">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="45021-1301">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="45021-1301">Az.Aks</span></span>
* <span data-ttu-id="45021-1302">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1302">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="45021-1303">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="45021-1303">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="45021-1304">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-1304">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-1305">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1305">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="45021-1306">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1306">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="45021-1307">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1307">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="45021-1308">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="45021-1308">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="45021-1309">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1309">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="45021-1310">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="45021-1310">Az.Batch</span></span>
* <span data-ttu-id="45021-1311">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1311">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="45021-1312">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="45021-1312">Az.Cdn</span></span>
* <span data-ttu-id="45021-1313">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1313">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1314">Az.Compute</span></span>
* <span data-ttu-id="45021-1315">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1315">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="45021-1316">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1316">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="45021-1317">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1317">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="45021-1318">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1318">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="45021-1319">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="45021-1319">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="45021-1320">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1320">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="45021-1321">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1321">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="45021-1322">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1322">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-1323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-1323">Az.DataFactory</span></span>
* <span data-ttu-id="45021-1324">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1324">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="45021-1325">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1325">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="45021-1326">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1326">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="45021-1327">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1327">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-1328">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-1328">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-1329">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1329">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="45021-1330">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="45021-1330">Az.EventHub</span></span>
* <span data-ttu-id="45021-1331">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="45021-1331">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="45021-1332">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="45021-1332">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="45021-1333">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1333">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="45021-1334">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="45021-1334">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="45021-1335">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="45021-1335">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="45021-1336">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1336">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-1337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-1337">Az.Monitor</span></span>
* <span data-ttu-id="45021-1338">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1338">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1339">Az.Network</span></span>
* <span data-ttu-id="45021-1340">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1340">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="45021-1341">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1341">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="45021-1342">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1342">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="45021-1343">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="45021-1343">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="45021-1344">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="45021-1344">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="45021-1345">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1345">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="45021-1346">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1346">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="45021-1347">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="45021-1347">Az.OperationalInsights</span></span>
* <span data-ttu-id="45021-1348">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1348">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="45021-1349">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1349">Added example</span></span>
    - <span data-ttu-id="45021-1350">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1350">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="45021-1351">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1351">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="45021-1352">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1352">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-1353">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-1354">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1354">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-1355">Az.Resources</span></span>
* <span data-ttu-id="45021-1356">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1356">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="45021-1357">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1357">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="45021-1358">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="45021-1358">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="45021-1359">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1359">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="45021-1360">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="45021-1360">Az.ServiceBus</span></span>
* <span data-ttu-id="45021-1361">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="45021-1361">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="45021-1362">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="45021-1362">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="45021-1363">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1363">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="45021-1364">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-1364">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-1365">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1365">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="45021-1366">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="45021-1366">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="45021-1367">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="45021-1367">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="45021-1368">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1368">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="45021-1369">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="45021-1369">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="45021-1370">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1370">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1371">Az.Sql</span></span>
* <span data-ttu-id="45021-1372">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1372">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-1373">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-1373">Az.Storage</span></span>
* <span data-ttu-id="45021-1374">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1374">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="45021-1375">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="45021-1375">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="45021-1376">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="45021-1376">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="45021-1377">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="45021-1377">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="45021-1378">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="45021-1378">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="45021-1379">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="45021-1379">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-1380">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-1380">Az.Websites</span></span>
* <span data-ttu-id="45021-1381">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1381">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="45021-1382">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1382">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-1383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-1383">Az.Accounts</span></span>
* <span data-ttu-id="45021-1384">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1384">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="45021-1385">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="45021-1385">Az.ApplicationInsights</span></span>
* <span data-ttu-id="45021-1386">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1386">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-1387">Az.Automation</span></span>
* <span data-ttu-id="45021-1388">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1388">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="45021-1389">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="45021-1389">Az.CognitiveServices</span></span>
* <span data-ttu-id="45021-1390">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1390">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1391">Az.Compute</span></span>
* <span data-ttu-id="45021-1392">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1392">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="45021-1393">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="45021-1393">Az.ContainerRegistry</span></span>
* <span data-ttu-id="45021-1394">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1394">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="45021-1395">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="45021-1395">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-1396">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-1396">Az.DataFactory</span></span>
* <span data-ttu-id="45021-1397">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1397">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="45021-1398">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1398">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="45021-1399">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="45021-1399">Az.EventHub</span></span>
* <span data-ttu-id="45021-1400">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="45021-1400">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="45021-1401">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1401">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-1402">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-1402">Az.KeyVault</span></span>
* <span data-ttu-id="45021-1403">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1403">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="45021-1404">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="45021-1404">Az.LogicApp</span></span>
* <span data-ttu-id="45021-1405">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="45021-1405">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="45021-1406">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1406">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="45021-1407">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="45021-1407">Az.ManagedServices</span></span>
* <span data-ttu-id="45021-1408">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="45021-1408">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1409">Az.Network</span></span>
* <span data-ttu-id="45021-1410">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1410">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="45021-1411">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1411">New cmdlets</span></span>
        - <span data-ttu-id="45021-1412">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="45021-1412">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="45021-1413">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="45021-1413">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="45021-1414">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1414">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="45021-1415">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1415">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="45021-1416">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1416">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="45021-1417">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1417">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="45021-1418">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="45021-1418">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="45021-1419">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="45021-1419">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="45021-1420">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="45021-1420">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="45021-1421">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1421">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="45021-1422">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1422">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="45021-1423">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1423">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="45021-1424">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1424">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="45021-1425">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1425">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="45021-1426">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1426">Updated cmdlets</span></span>
        - <span data-ttu-id="45021-1427">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1427">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="45021-1428">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1428">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="45021-1429">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1429">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="45021-1430">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1430">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="45021-1431">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1431">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="45021-1432">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1432">Updated cmdlet:</span></span>
        - <span data-ttu-id="45021-1433">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1433">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="45021-1434">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1434">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="45021-1435">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1435">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="45021-1436">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1436">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="45021-1437">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1437">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="45021-1438">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="45021-1438">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="45021-1439">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="45021-1439">Az.OperationalInsights</span></span>
* <span data-ttu-id="45021-1440">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1440">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="45021-1441">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1441">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-1442">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-1442">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-1443">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1443">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="45021-1444">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1444">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="45021-1445">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1445">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="45021-1446">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1446">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="45021-1447">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1447">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="45021-1448">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1448">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="45021-1449">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1449">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="45021-1450">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1450">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="45021-1451">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1451">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="45021-1452">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1452">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-1453">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-1453">Az.Resources</span></span>
- <span data-ttu-id="45021-1454">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1454">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="45021-1455">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1455">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="45021-1456">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="45021-1456">Az.ServiceBus</span></span>
* <span data-ttu-id="45021-1457">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="45021-1457">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="45021-1458">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1458">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1459">Az.Sql</span></span>
* <span data-ttu-id="45021-1460">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1460">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="45021-1461">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1461">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="45021-1462">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1462">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-1463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-1463">Az.Storage</span></span>
* <span data-ttu-id="45021-1464">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1464">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="45021-1465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="45021-1465">Az.StorageSync</span></span>
* <span data-ttu-id="45021-1466">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="45021-1466">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="45021-1467">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1467">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-1468">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-1468">Az.Websites</span></span>
* <span data-ttu-id="45021-1469">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1469">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="45021-1470">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1470">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="45021-1471">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1471">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="45021-1472">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1472">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-1473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-1473">Az.Accounts</span></span>
* <span data-ttu-id="45021-1474">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1474">Add support for profile cmdlets</span></span>
* <span data-ttu-id="45021-1475">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1475">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="45021-1476">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1476">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="45021-1477">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="45021-1477">Az.Advisor</span></span>
* <span data-ttu-id="45021-1478">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-1478">GA release of Az.Advisor</span></span>
* <span data-ttu-id="45021-1479">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="45021-1479">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="45021-1480">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-1480">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-1481">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1481">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="45021-1482">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="45021-1482">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="45021-1483">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1483">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="45021-1484">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="45021-1484">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="45021-1485">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="45021-1485">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="45021-1486">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="45021-1486">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="45021-1487">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1487">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-1488">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-1488">Az.Automation</span></span>
* <span data-ttu-id="45021-1489">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1489">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1490">Az.Compute</span></span>
* <span data-ttu-id="45021-1491">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1491">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-1492">Az.DataFactory</span></span>
* <span data-ttu-id="45021-1493">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-1493">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="45021-1494">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="45021-1494">Az.EventGrid</span></span>
* <span data-ttu-id="45021-1495">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1495">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-1496">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-1496">Az.IotHub</span></span>
* <span data-ttu-id="45021-1497">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1497">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1498">Az.Network</span></span>
* <span data-ttu-id="45021-1499">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1499">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="45021-1500">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1500">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="45021-1501">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="45021-1501">Az.PolicyInsights</span></span>
* <span data-ttu-id="45021-1502">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1502">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="45021-1503">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="45021-1503">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="45021-1504">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="45021-1504">Az.OperationalInsights</span></span>
* <span data-ttu-id="45021-1505">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1505">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-1506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-1506">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-1507">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="45021-1507">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-1508">Az.Resources</span></span>
    - <span data-ttu-id="45021-1509">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="45021-1509">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="45021-1510">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1510">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="45021-1511">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1511">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="45021-1512">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1512">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="45021-1513">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="45021-1513">Az.ServiceBus</span></span>
* <span data-ttu-id="45021-1514">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1514">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1515">Az.Sql</span></span>
* <span data-ttu-id="45021-1516">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1516">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="45021-1517">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1517">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="45021-1518">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="45021-1518">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="45021-1519">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="45021-1519">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="45021-1520">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="45021-1520">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="45021-1521">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="45021-1521">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="45021-1522">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="45021-1522">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="45021-1523">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="45021-1523">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="45021-1524">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1524">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-1525">Az.Storage</span></span>
* <span data-ttu-id="45021-1526">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1526">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="45021-1527">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="45021-1527">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="45021-1528">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1528">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="45021-1529">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="45021-1529">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="45021-1530">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1530">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="45021-1531">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1531">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="45021-1532">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1532">Set-AzStorageAccount</span></span>
* <span data-ttu-id="45021-1533">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1533">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="45021-1534">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="45021-1534">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="45021-1535">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="45021-1535">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="45021-1536">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="45021-1536">Az.StorageSync</span></span>
* <span data-ttu-id="45021-1537">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="45021-1537">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="45021-1538">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1538">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-1539">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-1539">Az.Accounts</span></span>
* <span data-ttu-id="45021-1540">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1540">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="45021-1541">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="45021-1541">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="45021-1542">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1542">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="45021-1543">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="45021-1543">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="45021-1544">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="45021-1544">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1545">Az.Compute</span></span>
* <span data-ttu-id="45021-1546">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="45021-1546">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="45021-1547">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1547">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="45021-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="45021-1548">Az.Dns</span></span>
* <span data-ttu-id="45021-1549">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1549">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="45021-1550">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="45021-1550">Az.EventGrid</span></span>
* <span data-ttu-id="45021-1551">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1551">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="45021-1552">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="45021-1552">New cmdlets:</span></span>
    - <span data-ttu-id="45021-1553">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="45021-1553">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="45021-1554">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45021-1554">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="45021-1555">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="45021-1555">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="45021-1556">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="45021-1556">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="45021-1557">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="45021-1557">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="45021-1558">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="45021-1558">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="45021-1559">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="45021-1559">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="45021-1560">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="45021-1560">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="45021-1561">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="45021-1561">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="45021-1562">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="45021-1562">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="45021-1563">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="45021-1563">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="45021-1564">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45021-1564">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="45021-1565">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="45021-1565">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="45021-1566">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="45021-1566">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="45021-1567">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="45021-1567">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="45021-1568">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="45021-1568">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="45021-1569">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1569">Updated cmdlets:</span></span>
    - <span data-ttu-id="45021-1570">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="45021-1570">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="45021-1571">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="45021-1571">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="45021-1572">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="45021-1572">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="45021-1573">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="45021-1573">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="45021-1574">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-1574">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="45021-1575">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="45021-1575">Event subscription expiration date,</span></span>
            - <span data-ttu-id="45021-1576">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="45021-1576">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="45021-1577">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="45021-1577">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="45021-1578">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="45021-1578">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="45021-1579">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="45021-1579">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="45021-1580">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="45021-1580">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="45021-1581">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="45021-1581">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="45021-1582">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="45021-1582">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="45021-1583">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="45021-1583">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="45021-1584">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="45021-1584">Az.FrontDoor</span></span>
* <span data-ttu-id="45021-1585">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="45021-1585">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="45021-1586">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="45021-1586">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="45021-1587">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="45021-1587">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="45021-1588">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="45021-1588">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1589">Az.Network</span></span>
* <span data-ttu-id="45021-1590">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="45021-1590">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="45021-1591">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1591">New cmdlets</span></span>
        - <span data-ttu-id="45021-1592">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="45021-1592">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="45021-1593">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="45021-1593">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="45021-1594">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1594">New cmdlets</span></span>
        - <span data-ttu-id="45021-1595">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="45021-1595">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="45021-1596">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="45021-1596">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="45021-1597">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1597">New cmdlets</span></span>
        - <span data-ttu-id="45021-1598">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="45021-1598">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="45021-1599">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="45021-1599">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="45021-1600">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="45021-1600">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="45021-1601">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1601">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="45021-1602">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1602">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="45021-1603">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="45021-1603">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="45021-1604">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1604">New cmdlets</span></span>
        - <span data-ttu-id="45021-1605">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="45021-1605">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="45021-1606">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="45021-1606">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="45021-1607">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="45021-1607">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="45021-1608">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="45021-1608">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="45021-1609">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="45021-1609">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="45021-1610">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1610">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="45021-1611">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1611">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="45021-1612">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1612">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="45021-1613">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1613">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="45021-1614">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1614">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="45021-1615">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1615">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="45021-1616">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1616">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="45021-1617">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1617">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="45021-1618">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1618">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="45021-1619">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1619">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="45021-1620">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1620">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="45021-1621">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1621">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="45021-1622">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1622">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="45021-1623">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1623">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="45021-1624">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1624">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="45021-1625">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1625">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="45021-1626">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="45021-1626">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="45021-1627">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="45021-1627">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="45021-1628">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="45021-1628">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="45021-1629">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1629">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="45021-1630">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1630">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="45021-1631">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1631">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="45021-1632">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="45021-1632">Az.OperationalInsights</span></span>
* <span data-ttu-id="45021-1633">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1633">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-1634">Az.Resources</span></span>
* <span data-ttu-id="45021-1635">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="45021-1635">Support for additional Template Export options</span></span>
    - <span data-ttu-id="45021-1636">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1636">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="45021-1637">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1637">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="45021-1638">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1638">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="45021-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-1639">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-1640">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1640">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1641">Az.Sql</span></span>
* <span data-ttu-id="45021-1642">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1642">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="45021-1643">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1643">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="45021-1644">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1644">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="45021-1645">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="45021-1645">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="45021-1646">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="45021-1646">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="45021-1647">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="45021-1647">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="45021-1648">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="45021-1648">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="45021-1649">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="45021-1649">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-1650">Az.Storage</span></span>
* <span data-ttu-id="45021-1651">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="45021-1651">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="45021-1652">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1652">New-AzStorageAccount</span></span>
* <span data-ttu-id="45021-1653">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1653">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="45021-1654">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="45021-1654">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-1655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-1655">Az.Websites</span></span>
* <span data-ttu-id="45021-1656">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="45021-1656">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="45021-1657">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="45021-1657">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="45021-1658">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1658">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="45021-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="45021-1659">Az.Cdn</span></span>
* <span data-ttu-id="45021-1660">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1660">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1661">Az.Compute</span></span>
* <span data-ttu-id="45021-1662">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1662">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="45021-1663">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="45021-1663">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="45021-1664">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="45021-1664">Az.EventHub</span></span>
* <span data-ttu-id="45021-1665">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="45021-1665">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="45021-1666">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="45021-1666">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1667">Az.Network</span></span>
* <span data-ttu-id="45021-1668">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1668">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="45021-1669">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1669">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="45021-1670">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="45021-1670">Az.PolicyInsights</span></span>
* <span data-ttu-id="45021-1671">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1671">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-1672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-1672">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-1673">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1673">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="45021-1674">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="45021-1674">Az.ServiceBus</span></span>
* <span data-ttu-id="45021-1675">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="45021-1675">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="45021-1676">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-1676">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-1677">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1677">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="45021-1678">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1678">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1679">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1679">Az.Sql</span></span>
* <span data-ttu-id="45021-1680">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1680">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="45021-1681">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1681">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="45021-1682">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-1682">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="45021-1683">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="45021-1683">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-1684">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-1684">Az.Websites</span></span>
* <span data-ttu-id="45021-1685">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="45021-1685">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="45021-1686">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1686">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="45021-1687">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-1687">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-1688">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-1688">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="45021-1689">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="45021-1689">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="45021-1690">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="45021-1690">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="45021-1691">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="45021-1691">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="45021-1692">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="45021-1692">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="45021-1693">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="45021-1693">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="45021-1694">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="45021-1694">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="45021-1695">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="45021-1695">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="45021-1696">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-1696">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="45021-1697">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="45021-1697">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="45021-1698">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="45021-1698">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="45021-1699">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="45021-1699">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="45021-1700">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="45021-1700">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="45021-1701">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-1701">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="45021-1702">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="45021-1702">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="45021-1703">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="45021-1703">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="45021-1704">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="45021-1704">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="45021-1705">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="45021-1705">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="45021-1706">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="45021-1706">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="45021-1707">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="45021-1707">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="45021-1708">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="45021-1708">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="45021-1709">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="45021-1709">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="45021-1710">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="45021-1710">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="45021-1711">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1711">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="45021-1712">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1712">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="45021-1713">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1713">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="45021-1714">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="45021-1714">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="45021-1715">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="45021-1715">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="45021-1716">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1716">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="45021-1717">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1717">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="45021-1718">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1718">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="45021-1719">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="45021-1719">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="45021-1720">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1720">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="45021-1721">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1721">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="45021-1722">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="45021-1722">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="45021-1723">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="45021-1723">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="45021-1724">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="45021-1724">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="45021-1725">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1725">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="45021-1726">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1726">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="45021-1727">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1727">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="45021-1728">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="45021-1728">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="45021-1729">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="45021-1729">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="45021-1730">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="45021-1730">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="45021-1731">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="45021-1731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="45021-1732">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1732">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="45021-1733">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="45021-1733">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="45021-1734">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="45021-1734">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="45021-1735">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="45021-1735">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="45021-1736">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1736">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="45021-1737">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="45021-1737">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="45021-1738">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="45021-1738">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="45021-1739">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="45021-1739">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="45021-1740">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="45021-1740">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="45021-1741">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1741">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="45021-1742">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="45021-1742">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="45021-1743">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="45021-1743">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="45021-1744">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1744">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="45021-1745">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="45021-1745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="45021-1746">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="45021-1746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="45021-1747">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="45021-1748">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1748">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="45021-1749">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="45021-1749">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="45021-1750">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="45021-1750">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="45021-1751">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1751">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="45021-1752">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1752">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="45021-1753">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="45021-1753">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="45021-1754">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="45021-1754">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="45021-1755">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="45021-1755">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="45021-1756">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="45021-1756">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="45021-1757">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="45021-1757">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="45021-1758">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="45021-1758">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="45021-1759">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="45021-1759">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="45021-1760">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="45021-1760">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="45021-1761">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="45021-1761">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="45021-1762">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="45021-1762">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="45021-1763">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="45021-1763">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="45021-1764">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="45021-1764">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-1765">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-1765">Az.Automation</span></span>
* <span data-ttu-id="45021-1766">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1766">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="45021-1767">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1767">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="45021-1768">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1768">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="45021-1769">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1769">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="45021-1770">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1770">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="45021-1771">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1771">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="45021-1772">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="45021-1772">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1773">Az.Compute</span></span>
* <span data-ttu-id="45021-1774">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1774">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="45021-1775">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="45021-1775">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-1776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-1776">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-1777">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1777">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-1778">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-1778">Az.Monitor</span></span>
* <span data-ttu-id="45021-1779">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1779">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1780">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1780">Az.Network</span></span>
* <span data-ttu-id="45021-1781">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1781">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="45021-1782">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="45021-1782">Updated cmdlet:</span></span>
        - <span data-ttu-id="45021-1783">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="45021-1783">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="45021-1784">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1784">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-1785">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-1785">Az.Resources</span></span>
* <span data-ttu-id="45021-1786">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1786">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1787">Az.Sql</span></span>
* <span data-ttu-id="45021-1788">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="45021-1788">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="45021-1789">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1789">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-1790">Az.Accounts</span></span>
* <span data-ttu-id="45021-1791">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="45021-1791">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="45021-1792">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="45021-1792">Az.CognitiveServices</span></span>
* <span data-ttu-id="45021-1793">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="45021-1793">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="45021-1794">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="45021-1794">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1795">Az.Compute</span></span>
* <span data-ttu-id="45021-1796">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="45021-1796">Proximity placement group feature.</span></span>
    - <span data-ttu-id="45021-1797">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="45021-1797">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="45021-1798">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="45021-1798">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="45021-1799">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1799">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="45021-1800">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="45021-1800">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="45021-1801">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1801">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="45021-1802">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="45021-1802">Breaking changes</span></span>
    - <span data-ttu-id="45021-1803">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1803">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="45021-1804">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1804">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="45021-1805">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="45021-1805">Az.DeploymentManager</span></span>
* <span data-ttu-id="45021-1806">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="45021-1806">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="45021-1807">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="45021-1807">Az.Dns</span></span>
* <span data-ttu-id="45021-1808">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="45021-1808">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="45021-1809">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="45021-1809">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="45021-1810">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="45021-1810">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="45021-1811">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="45021-1811">Az.FrontDoor</span></span>
* <span data-ttu-id="45021-1812">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="45021-1812">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="45021-1813">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="45021-1813">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="45021-1814">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="45021-1814">Az.HDInsight</span></span>
* <span data-ttu-id="45021-1815">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="45021-1815">Removed two cmdlets:</span></span>
    - <span data-ttu-id="45021-1816">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="45021-1816">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="45021-1817">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="45021-1817">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="45021-1818">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1818">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="45021-1819">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="45021-1819">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="45021-1820">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="45021-1820">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="45021-1821">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="45021-1821">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-1822">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-1822">Az.Monitor</span></span>
* <span data-ttu-id="45021-1823">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="45021-1823">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="45021-1824">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="45021-1824">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="45021-1825">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="45021-1825">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="45021-1826">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="45021-1826">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="45021-1827">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="45021-1827">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="45021-1828">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="45021-1828">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="45021-1829">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="45021-1829">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="45021-1830">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="45021-1830">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="45021-1831">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="45021-1831">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="45021-1832">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="45021-1832">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="45021-1833">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="45021-1833">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="45021-1834">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="45021-1834">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="45021-1835">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="45021-1835">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="45021-1836">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1836">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1837">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1837">Az.Network</span></span>
* <span data-ttu-id="45021-1838">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="45021-1838">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="45021-1839">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1839">New cmdlets</span></span>
        - <span data-ttu-id="45021-1840">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="45021-1840">New-AzNatGateway</span></span>
        - <span data-ttu-id="45021-1841">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="45021-1841">Get-AzNatGateway</span></span>
        - <span data-ttu-id="45021-1842">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="45021-1842">Set-AzNatGateway</span></span>
        - <span data-ttu-id="45021-1843">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="45021-1843">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="45021-1844">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1844">Updated cmdlets</span></span>
        - <span data-ttu-id="45021-1845">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="45021-1845">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="45021-1846">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="45021-1846">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="45021-1847">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="45021-1847">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="45021-1848">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1848">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="45021-1849">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1849">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="45021-1850">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="45021-1850">Az.PolicyInsights</span></span>
* <span data-ttu-id="45021-1851">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1851">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="45021-1852">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="45021-1852">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="45021-1853">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="45021-1853">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-1854">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-1854">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-1855">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1855">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="45021-1856">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="45021-1856">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="45021-1857">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="45021-1857">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="45021-1858">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="45021-1858">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="45021-1859">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="45021-1859">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="45021-1860">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="45021-1860">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="45021-1861">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="45021-1861">Az.Relay</span></span>
* <span data-ttu-id="45021-1862">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="45021-1862">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="45021-1863">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="45021-1863">Az.ServiceBus</span></span>
* <span data-ttu-id="45021-1864">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1864">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-1865">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-1865">Az.Storage</span></span>
* <span data-ttu-id="45021-1866">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="45021-1866">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="45021-1867">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="45021-1867">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="45021-1868">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="45021-1868">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="45021-1869">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1869">New-AzStorageAccount</span></span>
* <span data-ttu-id="45021-1870">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="45021-1870">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="45021-1871">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1871">New-AzStorageAccount</span></span>
    - <span data-ttu-id="45021-1872">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1872">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="45021-1873">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-1873">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-1874">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-1874">Az.Websites</span></span>
* <span data-ttu-id="45021-1875">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="45021-1875">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="45021-1876">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="45021-1876">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="45021-1877">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1877">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="45021-1878">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="45021-1878">Highlights since the last major release</span></span>
* <span data-ttu-id="45021-1879">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-1879">General availability of `Az` module</span></span>
* <span data-ttu-id="45021-1880">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="45021-1880">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="45021-1881">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="45021-1881">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="45021-1882">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1882">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="45021-1883">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1883">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="45021-1884">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1884">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="45021-1885">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1885">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-1886">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-1886">Az.Accounts</span></span>
* <span data-ttu-id="45021-1887">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1887">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="45021-1888">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="45021-1888">Az.Batch</span></span>
* <span data-ttu-id="45021-1889">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="45021-1890">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="45021-1890">Az.Cdn</span></span>
* <span data-ttu-id="45021-1891">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1891">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="45021-1892">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="45021-1892">Az.CognitiveServices</span></span>
* <span data-ttu-id="45021-1893">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1894">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1894">Az.Compute</span></span>
* <span data-ttu-id="45021-1895">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1895">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="45021-1896">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1896">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="45021-1897">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1897">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-1898">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-1898">Az.DataFactory</span></span>
* <span data-ttu-id="45021-1899">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1899">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-1900">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-1900">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-1901">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="45021-1902">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="45021-1902">Az.EventGrid</span></span>
* <span data-ttu-id="45021-1903">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1903">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="45021-1904">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="45021-1904">Az.EventHub</span></span>
* <span data-ttu-id="45021-1905">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1905">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="45021-1906">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="45021-1906">Az.HDInsight</span></span>
* <span data-ttu-id="45021-1907">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-1908">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-1908">Az.IotHub</span></span>
* <span data-ttu-id="45021-1909">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1909">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-1910">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-1910">Az.KeyVault</span></span>
* <span data-ttu-id="45021-1911">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="45021-1912">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1912">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="45021-1913">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="45021-1913">Az.MachineLearning</span></span>
* <span data-ttu-id="45021-1914">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1914">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="45021-1915">Az.Media</span><span class="sxs-lookup"><span data-stu-id="45021-1915">Az.Media</span></span>
* <span data-ttu-id="45021-1916">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1916">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-1917">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-1917">Az.Monitor</span></span>
  * <span data-ttu-id="45021-1918">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="45021-1918">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="45021-1919">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="45021-1919">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="45021-1920">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="45021-1920">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="45021-1921">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="45021-1921">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="45021-1922">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="45021-1922">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="45021-1923">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="45021-1923">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="45021-1924">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1924">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-1925">Az.Network</span></span>
* <span data-ttu-id="45021-1926">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="45021-1927">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1927">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="45021-1928">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="45021-1928">Az.NotificationHubs</span></span>
* <span data-ttu-id="45021-1929">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="45021-1930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="45021-1930">Az.OperationalInsights</span></span>
* <span data-ttu-id="45021-1931">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="45021-1932">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="45021-1932">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="45021-1933">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1933">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-1934">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-1934">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-1935">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1935">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="45021-1936">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="45021-1936">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="45021-1937">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1937">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="45021-1938">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1938">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="45021-1939">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="45021-1939">Az.RedisCache</span></span>
* <span data-ttu-id="45021-1940">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1940">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-1941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-1941">Az.Resources</span></span>
* <span data-ttu-id="45021-1942">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1942">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1943">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1943">Az.Sql</span></span>
* <span data-ttu-id="45021-1944">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1944">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="45021-1945">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1945">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="45021-1946">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1946">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="45021-1947">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1947">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="45021-1948">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-1948">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="45021-1949">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1949">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="45021-1950">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1950">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-1951">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-1951">Az.Websites</span></span>
* <span data-ttu-id="45021-1952">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1952">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="45021-1953">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1953">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="45021-1954">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1954">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="45021-1955">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="45021-1955">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="45021-1956">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="45021-1956">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="45021-1957">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="45021-1957">Highlights since the last major release</span></span>
* <span data-ttu-id="45021-1958">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-1958">General availability of `Az` module</span></span>
* <span data-ttu-id="45021-1959">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="45021-1959">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="45021-1960">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="45021-1960">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="45021-1961">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1961">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="45021-1962">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1962">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="45021-1963">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1963">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="45021-1964">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-1964">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="45021-1965">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-1965">Az.Accounts</span></span>
* <span data-ttu-id="45021-1966">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1966">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="45021-1967">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="45021-1967">Az.AnalysisServices</span></span>
* <span data-ttu-id="45021-1968">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="45021-1968">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="45021-1969">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="45021-1969">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-1970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-1970">Az.Automation</span></span>
* <span data-ttu-id="45021-1971">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1971">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="45021-1972">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="45021-1972">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="45021-1973">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="45021-1973">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-1974">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-1974">Az.Compute</span></span>
* <span data-ttu-id="45021-1975">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1975">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="45021-1976">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1976">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="45021-1977">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="45021-1977">Az.ContainerInstance</span></span>
* <span data-ttu-id="45021-1978">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-1978">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-1979">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-1979">Az.DataFactory</span></span>
* <span data-ttu-id="45021-1980">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1980">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="45021-1981">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-1981">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-1982">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-1982">Az.Resources</span></span>
* <span data-ttu-id="45021-1983">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1983">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="45021-1984">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-1984">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="45021-1985">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="45021-1985">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="45021-1986">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="45021-1986">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="45021-1987">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-1987">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="45021-1988">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="45021-1988">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-1989">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-1989">Az.Sql</span></span>
* <span data-ttu-id="45021-1990">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-1990">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-1991">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-1991">Az.Storage</span></span>
* <span data-ttu-id="45021-1992">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="45021-1992">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="45021-1993">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="45021-1993">New-AzStorageContext</span></span>
* <span data-ttu-id="45021-1994">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="45021-1994">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="45021-1995">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="45021-1995">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="45021-1996">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="45021-1996">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="45021-1997">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="45021-1997">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="45021-1998">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="45021-1998">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="45021-1999">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="45021-1999">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="45021-2000">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="45021-2000">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="45021-2001">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="45021-2001">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="45021-2002">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="45021-2002">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="45021-2003">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="45021-2003">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="45021-2004">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="45021-2004">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="45021-2005">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="45021-2005">Highlights since the last major release</span></span>
* <span data-ttu-id="45021-2006">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-2006">General availability of `Az` module</span></span>
* <span data-ttu-id="45021-2007">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="45021-2007">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="45021-2008">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="45021-2008">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="45021-2009">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2009">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="45021-2010">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2010">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="45021-2011">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2011">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="45021-2012">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-2012">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-2013">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-2013">Az.Automation</span></span>
* <span data-ttu-id="45021-2014">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="45021-2014">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="45021-2015">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="45021-2015">Dynamic grouping</span></span>
    * <span data-ttu-id="45021-2016">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="45021-2016">Pre-Post script</span></span>
    * <span data-ttu-id="45021-2017">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="45021-2017">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-2018">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2018">Az.Compute</span></span>
* <span data-ttu-id="45021-2019">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="45021-2019">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="45021-2020">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2020">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-2021">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-2021">Az.KeyVault</span></span>
* <span data-ttu-id="45021-2022">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2022">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-2023">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-2023">Az.Network</span></span>
* <span data-ttu-id="45021-2024">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2024">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="45021-2025">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2025">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-2026">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-2026">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-2027">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2027">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="45021-2028">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2028">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-2029">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2029">Az.Resources</span></span>
* <span data-ttu-id="45021-2030">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2030">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="45021-2031">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2031">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-2032">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2032">Az.Sql</span></span>
* <span data-ttu-id="45021-2033">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2033">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-2034">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-2034">Az.Storage</span></span>
* <span data-ttu-id="45021-2035">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="45021-2035">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="45021-2036">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="45021-2036">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="45021-2037">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="45021-2037">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="45021-2038">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="45021-2038">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="45021-2039">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="45021-2039">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="45021-2040">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="45021-2040">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="45021-2041">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="45021-2041">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-2042">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-2042">Az.Websites</span></span>
* <span data-ttu-id="45021-2043">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2043">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="45021-2044">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="45021-2044">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-2045">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-2045">Az.Accounts</span></span>
* <span data-ttu-id="45021-2046">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2046">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="45021-2047">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2047">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-2048">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-2048">Az.Automation</span></span>
* <span data-ttu-id="45021-2049">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2049">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="45021-2050">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2050">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="45021-2051">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="45021-2051">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="45021-2052">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="45021-2052">Az.Cdn</span></span>
* <span data-ttu-id="45021-2053">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="45021-2053">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-2054">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2054">Az.Compute</span></span>
* <span data-ttu-id="45021-2055">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2055">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-2056">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-2056">Az.DataFactory</span></span>
* <span data-ttu-id="45021-2057">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2057">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="45021-2058">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="45021-2058">Az.LogicApp</span></span>
* <span data-ttu-id="45021-2059">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="45021-2059">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-2060">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-2060">Az.Network</span></span>
* <span data-ttu-id="45021-2061">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2061">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-2062">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-2062">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-2063">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2063">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="45021-2064">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="45021-2064">SDK Update</span></span>
* <span data-ttu-id="45021-2065">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-2065">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="45021-2066">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2066">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-2067">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2067">Az.Resources</span></span>
* <span data-ttu-id="45021-2068">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2068">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="45021-2069">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="45021-2069">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="45021-2070">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2070">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="45021-2071">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="45021-2071">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="45021-2072">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2072">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="45021-2073">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="45021-2073">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-2074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2074">Az.Sql</span></span>
* <span data-ttu-id="45021-2075">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-2075">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="45021-2076">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-2076">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-2077">Az.Storage</span></span>
* <span data-ttu-id="45021-2078">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45021-2078">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="45021-2079">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="45021-2079">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="45021-2080">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="45021-2080">Az.AnalysisServices</span></span>
* <span data-ttu-id="45021-2081">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="45021-2081">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-2082">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-2082">Az.Automation</span></span>
* <span data-ttu-id="45021-2083">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2083">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="45021-2084">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2084">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="45021-2085">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2085">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="45021-2086">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="45021-2086">Az.CognitiveServices</span></span>
* <span data-ttu-id="45021-2087">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2087">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-2088">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2088">Az.Compute</span></span>
* <span data-ttu-id="45021-2089">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2089">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="45021-2090">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2090">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="45021-2091">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2091">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="45021-2092">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="45021-2092">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-2093">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-2093">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-2094">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2094">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="45021-2095">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="45021-2095">Az.EventHub</span></span>
* <span data-ttu-id="45021-2096">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2096">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-2097">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-2097">Az.KeyVault</span></span>
* <span data-ttu-id="45021-2098">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2098">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="45021-2099">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="45021-2099">Az.LogicApp</span></span>
* <span data-ttu-id="45021-2100">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2100">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="45021-2101">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2101">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="45021-2102">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-2102">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="45021-2103">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="45021-2103">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="45021-2104">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="45021-2104">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="45021-2105">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="45021-2105">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="45021-2106">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="45021-2106">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="45021-2107">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="45021-2107">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="45021-2108">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="45021-2108">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="45021-2109">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="45021-2109">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="45021-2110">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="45021-2110">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="45021-2111">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="45021-2111">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="45021-2112">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2112">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="45021-2113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-2113">Az.Monitor</span></span>
* <span data-ttu-id="45021-2114">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2114">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-2115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-2115">Az.Network</span></span>
* <span data-ttu-id="45021-2116">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2116">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="45021-2117">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="45021-2117">Az.OperationalInsights</span></span>
* <span data-ttu-id="45021-2118">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="45021-2118">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="45021-2119">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2119">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="45021-2120">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2120">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-2121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2121">Az.Resources</span></span>
* <span data-ttu-id="45021-2122">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2122">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="45021-2123">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2123">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="45021-2124">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2124">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="45021-2125">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2125">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-2126">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2126">Az.Sql</span></span>
* <span data-ttu-id="45021-2127">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2127">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="45021-2128">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2128">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-2129">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-2129">Az.Websites</span></span>
* <span data-ttu-id="45021-2130">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2130">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="45021-2131">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="45021-2131">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-2132">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-2132">Az.Accounts</span></span>
* <span data-ttu-id="45021-2133">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="45021-2133">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="45021-2134">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="45021-2134">Az.AnalysisServices</span></span>
<span data-ttu-id="45021-2135">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="45021-2135">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-2136">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2136">Az.Compute</span></span>
* <span data-ttu-id="45021-2137">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2137">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="45021-2138">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2138">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="45021-2139">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2139">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-2140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-2140">Az.RecoveryServices</span></span>
<span data-ttu-id="45021-2141">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="45021-2141">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-2142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2142">Az.Resources</span></span>
* <span data-ttu-id="45021-2143">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2143">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="45021-2144">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="45021-2144">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="45021-2145">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2145">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="45021-2146">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="45021-2146">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-2147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2147">Az.Sql</span></span>
* <span data-ttu-id="45021-2148">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="45021-2148">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="45021-2149">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2149">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="45021-2150">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2150">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="45021-2151">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="45021-2151">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-2152">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-2152">Az.Accounts</span></span>
* <span data-ttu-id="45021-2153">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="45021-2153">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="45021-2154">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="45021-2154">Az.AnalysisServices</span></span>
* <span data-ttu-id="45021-2155">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="45021-2155">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="45021-2156">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-2156">Az.RecoveryServices</span></span>
* <span data-ttu-id="45021-2157">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="45021-2157">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="45021-2158">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="45021-2158">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-2159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-2159">Az.Accounts</span></span>
* <span data-ttu-id="45021-2160">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2160">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="45021-2161">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2161">Update incorrect online help URLs</span></span>
* <span data-ttu-id="45021-2162">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2162">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="45021-2163">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="45021-2163">Az.Aks</span></span>
* <span data-ttu-id="45021-2164">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2164">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="45021-2165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-2165">Az.Automation</span></span>
* <span data-ttu-id="45021-2166">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2166">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="45021-2167">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2167">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="45021-2168">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="45021-2168">Az.Cdn</span></span>
* <span data-ttu-id="45021-2169">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2169">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-2170">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2170">Az.Compute</span></span>
* <span data-ttu-id="45021-2171">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2171">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="45021-2172">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2172">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="45021-2173">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2173">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="45021-2174">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="45021-2174">Az.ContainerRegistry</span></span>
* <span data-ttu-id="45021-2175">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2175">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="45021-2176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="45021-2176">Az.DataFactory</span></span>
* <span data-ttu-id="45021-2177">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2177">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-2178">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-2178">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-2179">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2179">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="45021-2180">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="45021-2180">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="45021-2181">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2181">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-2182">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-2182">Az.IotHub</span></span>
* <span data-ttu-id="45021-2183">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2183">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="45021-2184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-2184">Az.KeyVault</span></span>
* <span data-ttu-id="45021-2185">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2185">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-2186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-2186">Az.Network</span></span>
* <span data-ttu-id="45021-2187">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2187">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-2188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2188">Az.Resources</span></span>
* <span data-ttu-id="45021-2189">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2189">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="45021-2190">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2190">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="45021-2191">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2191">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="45021-2192">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2192">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="45021-2193">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2193">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="45021-2194">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2194">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="45021-2195">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="45021-2195">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="45021-2196">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-2196">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-2197">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="45021-2197">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="45021-2198">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2198">Fix some error messages.</span></span>
* <span data-ttu-id="45021-2199">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2199">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="45021-2200">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2200">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="45021-2201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="45021-2201">Az.SignalR</span></span>
* <span data-ttu-id="45021-2202">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2202">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-2203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2203">Az.Sql</span></span>
* <span data-ttu-id="45021-2204">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2204">Update incorrect online help URLs</span></span>
* <span data-ttu-id="45021-2205">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2205">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="45021-2206">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2206">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="45021-2207">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="45021-2207">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-2208">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-2208">Az.Storage</span></span>
* <span data-ttu-id="45021-2209">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2209">Update incorrect online help URLs</span></span>
* <span data-ttu-id="45021-2210">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-2210">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="45021-2211">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="45021-2211">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="45021-2212">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="45021-2212">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="45021-2213">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="45021-2213">Az.TrafficManager</span></span>
* <span data-ttu-id="45021-2214">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2214">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-2215">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-2215">Az.Websites</span></span>
* <span data-ttu-id="45021-2216">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2216">Update incorrect online help URLs</span></span>
* <span data-ttu-id="45021-2217">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2217">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="45021-2218">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2218">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="45021-2219">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="45021-2219">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="45021-2220">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-2220">Az.Accounts</span></span>
* <span data-ttu-id="45021-2221">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2221">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-2222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2222">Az.Compute</span></span>
* <span data-ttu-id="45021-2223">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="45021-2223">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="45021-2224">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2224">Updated the description of ID in help files</span></span>
* <span data-ttu-id="45021-2225">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="45021-2225">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-2227">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2227">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="45021-2228">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2228">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="45021-2229">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="45021-2229">Az.EventGrid</span></span>
* <span data-ttu-id="45021-2230">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2230">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="45021-2231">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2231">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="45021-2232">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-2232">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="45021-2233">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="45021-2233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="45021-2234">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="45021-2234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="45021-2235">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="45021-2235">Dead letter endpoint.</span></span>
    - <span data-ttu-id="45021-2236">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-2236">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="45021-2237">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="45021-2237">Event Time-To-Live,</span></span>
        - <span data-ttu-id="45021-2238">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="45021-2238">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="45021-2239">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="45021-2239">Dead letter endpoint.</span></span>
* <span data-ttu-id="45021-2240">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2240">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="45021-2241">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-2241">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="45021-2242">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="45021-2242">Az.IotHub</span></span>
* <span data-ttu-id="45021-2243">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2243">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="45021-2244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="45021-2244">Az.LogicApp</span></span>
* <span data-ttu-id="45021-2245">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="45021-2245">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-2246">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2246">Az.Resources</span></span>
* <span data-ttu-id="45021-2247">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2247">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="45021-2248">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="45021-2248">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="45021-2249">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2249">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="45021-2250">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2250">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="45021-2251">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2251">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="45021-2252">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="45021-2252">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="45021-2253">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="45021-2253">Az.SignalR</span></span>
* <span data-ttu-id="45021-2254">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="45021-2254">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-2255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2255">Az.Sql</span></span>
* <span data-ttu-id="45021-2256">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="45021-2256">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="45021-2257">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-2257">Az.Storage</span></span>
* <span data-ttu-id="45021-2258">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="45021-2258">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="45021-2259">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="45021-2259">New-AzStorageContext</span></span>
* <span data-ttu-id="45021-2260">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2260">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="45021-2261">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="45021-2261">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-2262">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-2262">Az.Websites</span></span>
* <span data-ttu-id="45021-2263">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2263">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="45021-2264">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="45021-2264">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="45021-2265">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="45021-2265">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="45021-2266">Genel</span><span class="sxs-lookup"><span data-stu-id="45021-2266">General</span></span>

- <span data-ttu-id="45021-2267">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-2267">General Availability of Az Module</span></span>
- <span data-ttu-id="45021-2268">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="45021-2268">Online help for each module</span></span>
- <span data-ttu-id="45021-2269">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="45021-2269">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="45021-2270">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2270">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="45021-2271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="45021-2271">Az.Accounts</span></span>
- <span data-ttu-id="45021-2272">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="45021-2272">Changed from Az.Profile</span></span>
- <span data-ttu-id="45021-2273">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2273">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="45021-2274">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-2274">Az.ApiManagement</span></span>
- <span data-ttu-id="45021-2275">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="45021-2275">Fixes for #7002</span></span>
- <span data-ttu-id="45021-2276">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="45021-2277">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="45021-2277">Az.Batch</span></span>
- <span data-ttu-id="45021-2278">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2278">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="45021-2279">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="45021-2279">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="45021-2280">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2280">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="45021-2281">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="45021-2281">Az.Billing</span></span>
- <span data-ttu-id="45021-2282">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2282">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="45021-2283">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="45021-2283">Az.CognitivServices</span></span>
- <span data-ttu-id="45021-2284">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2284">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="45021-2285">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-2285">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="45021-2286">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="45021-2286">Az.ContainerInstance</span></span>
- <span data-ttu-id="45021-2287">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2287">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="45021-2288">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="45021-2288">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="45021-2289">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2289">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="45021-2290">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-2290">Az.DataLakeStore</span></span>
- <span data-ttu-id="45021-2291">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2291">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="45021-2292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="45021-2292">Az.Monitor</span></span>
- <span data-ttu-id="45021-2293">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2293">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="45021-2294">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="45021-2294">Az.KeyVault</span></span>
- <span data-ttu-id="45021-2295">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-2295">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="45021-2296">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="45021-2296">Az.MachineLearning</span></span>
- <span data-ttu-id="45021-2297">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2297">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="45021-2298">Az.Media</span><span class="sxs-lookup"><span data-stu-id="45021-2298">Az.Media</span></span>
- <span data-ttu-id="45021-2299">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="45021-2299">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="45021-2300">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-2300">Az.Network</span></span>
<span data-ttu-id="45021-2301">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2301">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="45021-2302">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="45021-2302">New cmdlets added:</span></span>
        - <span data-ttu-id="45021-2303">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45021-2303">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="45021-2304">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45021-2304">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="45021-2305">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45021-2305">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="45021-2306">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45021-2306">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="45021-2307">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="45021-2307">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="45021-2308">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="45021-2308">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="45021-2309">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="45021-2309">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="45021-2310">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="45021-2310">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="45021-2311">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2311">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="45021-2312">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="45021-2312">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="45021-2313">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="45021-2313">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="45021-2314">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="45021-2314">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="45021-2315">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45021-2315">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="45021-2316">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="45021-2316">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="45021-2317">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="45021-2317">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="45021-2318">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2318">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="45021-2319">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="45021-2319">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="45021-2320">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="45021-2320">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="45021-2321">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="45021-2321">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="45021-2322">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2322">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="45021-2323">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="45021-2324">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="45021-2324">Az.OperationalInsights</span></span>
- <span data-ttu-id="45021-2325">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="45021-2326">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="45021-2326">Az.Profile</span></span>
- <span data-ttu-id="45021-2327">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2327">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="45021-2328">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-2328">Az.RecoveryServices</span></span>
- <span data-ttu-id="45021-2329">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2329">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="45021-2330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2330">Az.Resources</span></span>
- <span data-ttu-id="45021-2331">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2331">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="45021-2332">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-2332">Az.ServiceFabric</span></span>
- <span data-ttu-id="45021-2333">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="45021-2333">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="45021-2334">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2334">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="45021-2335">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="45021-2335">Az.SIgnalR</span></span>
- <span data-ttu-id="45021-2336">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="45021-2336">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="45021-2337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2337">Az.Sql</span></span>
- <span data-ttu-id="45021-2338">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2338">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="45021-2339">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2339">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="45021-2340">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="45021-2341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-2341">Az.Storage</span></span>
- <span data-ttu-id="45021-2342">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2342">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="45021-2343">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-2343">Az.Websites</span></span>
- <span data-ttu-id="45021-2344">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="45021-2344">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="45021-2345">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="45021-2345">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="45021-2346">Genel</span><span class="sxs-lookup"><span data-stu-id="45021-2346">General</span></span>

* <span data-ttu-id="45021-2347">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="45021-2347">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="45021-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2348">Az.Compute</span></span>

* <span data-ttu-id="45021-2349">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2349">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="45021-2350">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-2350">Az.DataLakeStore</span></span>

* <span data-ttu-id="45021-2351">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2351">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="45021-2352">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="45021-2352">Az.FrontDoor</span></span>

* <span data-ttu-id="45021-2353">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2353">Fixed some broken links</span></span>
    - <span data-ttu-id="45021-2354">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2354">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="45021-2355">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2355">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="45021-2356">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="45021-2356">Az.RecoveryServices</span></span>

* <span data-ttu-id="45021-2357">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2357">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="45021-2358">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2358">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="45021-2359">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2359">Az.Resources</span></span>

* <span data-ttu-id="45021-2360">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="45021-2360">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="45021-2361">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2361">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="45021-2362">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2362">Az.Sql</span></span>

* <span data-ttu-id="45021-2363">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="45021-2363">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="45021-2364">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2364">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="45021-2365">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2365">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="45021-2366">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="45021-2366">Az.Storage</span></span>

* <span data-ttu-id="45021-2367">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2367">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="45021-2368">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2368">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="45021-2369">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="45021-2369">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="45021-2370">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2370">Support Static Website configuration</span></span>
    - <span data-ttu-id="45021-2371">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="45021-2371">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="45021-2372">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="45021-2372">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="45021-2373">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-2373">Az.Websites</span></span>

* <span data-ttu-id="45021-2374">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="45021-2374">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="45021-2375">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2375">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="45021-2376">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="45021-2376">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="45021-2377">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="45021-2377">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="45021-2378">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="45021-2378">Az.ApiManagement</span></span>
* <span data-ttu-id="45021-2379">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="45021-2379">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="45021-2380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="45021-2380">Az.Automation</span></span>
* <span data-ttu-id="45021-2381">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="45021-2381">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="45021-2382">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2382">Added Update Management cmdlets</span></span>
* <span data-ttu-id="45021-2383">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2383">Added Source Control cmdlets</span></span>
* <span data-ttu-id="45021-2384">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2384">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="45021-2385">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2385">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="45021-2386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2386">Az.Compute</span></span>
* <span data-ttu-id="45021-2387">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2387">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="45021-2388">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="45021-2388">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="45021-2389">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="45021-2389">Az.ContainerInstance</span></span>
* <span data-ttu-id="45021-2390">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="45021-2390">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="45021-2391">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="45021-2391">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="45021-2392">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2392">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="45021-2393">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-2393">Az.Network</span></span>
* <span data-ttu-id="45021-2394">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2394">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="45021-2395">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2395">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="45021-2396">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2396">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="45021-2397">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2397">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="45021-2398">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="45021-2398">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="45021-2399">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2399">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="45021-2400">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="45021-2400">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="45021-2401">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="45021-2401">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="45021-2402">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2402">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="45021-2403">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="45021-2403">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="45021-2404">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="45021-2404">Az.Relay</span></span>
* <span data-ttu-id="45021-2405">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2405">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="45021-2406">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2406">Az.Resources</span></span>
* <span data-ttu-id="45021-2407">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2407">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="45021-2408">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2408">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="45021-2409">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="45021-2409">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="45021-2410">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-2410">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-2411">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2411">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="45021-2412">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2412">Az.Sql</span></span>
* <span data-ttu-id="45021-2413">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2413">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="45021-2414">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="45021-2414">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="45021-2415">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="45021-2415">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="45021-2416">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="45021-2416">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="45021-2417">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="45021-2417">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="45021-2418">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="45021-2418">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="45021-2419">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="45021-2419">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="45021-2420">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="45021-2420">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="45021-2421">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="45021-2421">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="45021-2422">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2422">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="45021-2423">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2423">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="45021-2424">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2424">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="45021-2425">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="45021-2425">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="45021-2426">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="45021-2426">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="45021-2427">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="45021-2427">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="45021-2428">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="45021-2428">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="45021-2429">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2429">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="45021-2430">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="45021-2430">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="45021-2431">Genel</span><span class="sxs-lookup"><span data-stu-id="45021-2431">General</span></span>
* <span data-ttu-id="45021-2432">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="45021-2432">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="45021-2433">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="45021-2433">Az.Profile</span></span>
* <span data-ttu-id="45021-2434">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2434">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="45021-2435">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2435">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="45021-2436">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2436">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="45021-2437">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2437">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="45021-2438">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2438">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="45021-2439">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2439">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="45021-2440">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2440">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="45021-2441">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="45021-2441">Az.CognitiveServices</span></span>
* <span data-ttu-id="45021-2442">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2442">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-2443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2443">Az.Compute</span></span>
* <span data-ttu-id="45021-2444">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2444">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="45021-2445">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="45021-2445">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="45021-2446">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2446">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-2447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-2447">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-2448">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2448">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="45021-2449">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2449">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="45021-2450">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="45021-2450">Az.Insights</span></span>
* <span data-ttu-id="45021-2451">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2451">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="45021-2452">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="45021-2452">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="45021-2453">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2453">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="45021-2454">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="45021-2454">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-2455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-2455">Az.Network</span></span>
* <span data-ttu-id="45021-2456">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="45021-2456">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="45021-2457">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="45021-2457">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="45021-2458">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="45021-2458">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="45021-2459">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="45021-2459">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="45021-2460">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="45021-2460">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="45021-2461">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="45021-2461">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="45021-2462">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="45021-2462">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="45021-2463">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="45021-2463">Az.PolicyInsights</span></span>
* <span data-ttu-id="45021-2464">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2464">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-2465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2465">Az.Resources</span></span>
* <span data-ttu-id="45021-2466">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="45021-2466">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="45021-2467">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="45021-2467">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="45021-2468">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="45021-2468">Az.ServiceBus</span></span>
* <span data-ttu-id="45021-2469">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2469">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="45021-2470">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="45021-2470">Az.ServiceFabric</span></span>
* <span data-ttu-id="45021-2471">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2471">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="45021-2472">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2472">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="45021-2473">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="45021-2473">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="45021-2474">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="45021-2474">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="45021-2475">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2475">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="45021-2476">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="45021-2476">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="45021-2477">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="45021-2477">Az.Profile</span></span>
* <span data-ttu-id="45021-2478">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="45021-2478">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="45021-2479">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="45021-2479">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-2480">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2480">Az.Compute</span></span>
* <span data-ttu-id="45021-2481">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2481">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="45021-2482">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2482">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="45021-2483">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="45021-2483">Az.DataLakeStore</span></span>
* <span data-ttu-id="45021-2484">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="45021-2484">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="45021-2485">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="45021-2485">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="45021-2486">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="45021-2486">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="45021-2487">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="45021-2487">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="45021-2488">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="45021-2488">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-2489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-2489">Az.Network</span></span>
* <span data-ttu-id="45021-2490">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="45021-2490">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="45021-2491">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2491">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-2492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2492">Az.Resources</span></span>
* <span data-ttu-id="45021-2493">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2493">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="45021-2494">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="45021-2494">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="45021-2495">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="45021-2495">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="45021-2496">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="45021-2496">Azure.Storage</span></span>
* <span data-ttu-id="45021-2497">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="45021-2497">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="45021-2498">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="45021-2498">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="45021-2499">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="45021-2499">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="45021-2500">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="45021-2500">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="45021-2501">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="45021-2501">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="45021-2502">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="45021-2502">Az.CognitiveServices</span></span>
* <span data-ttu-id="45021-2503">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="45021-2503">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="45021-2504">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="45021-2504">Az.Compute</span></span>
* <span data-ttu-id="45021-2505">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2505">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="45021-2506">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2506">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="45021-2507">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2507">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="45021-2508">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="45021-2508">Az.DataFactoryV2</span></span>
* <span data-ttu-id="45021-2509">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="45021-2509">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="45021-2510">Az.Network</span><span class="sxs-lookup"><span data-stu-id="45021-2510">Az.Network</span></span>
* <span data-ttu-id="45021-2511">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="45021-2511">Added NetworkProfile functionality.</span></span> <span data-ttu-id="45021-2512">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2512">new cmdlets added</span></span>
    - <span data-ttu-id="45021-2513">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="45021-2513">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="45021-2514">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="45021-2514">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="45021-2515">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="45021-2515">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="45021-2516">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="45021-2516">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="45021-2517">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="45021-2517">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="45021-2518">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="45021-2518">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="45021-2519">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2519">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="45021-2520">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2520">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="45021-2521">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2521">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="45021-2522">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="45021-2522">Az.RedisCache</span></span>
* <span data-ttu-id="45021-2523">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="45021-2523">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="45021-2524">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2524">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="45021-2525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="45021-2525">Az.Resources</span></span>
* <span data-ttu-id="45021-2526">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="45021-2526">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="45021-2527">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2527">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="45021-2528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="45021-2528">Az.Sql</span></span>
* <span data-ttu-id="45021-2529">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="45021-2529">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="45021-2530">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="45021-2530">Az.Websites</span></span>
* <span data-ttu-id="45021-2531">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="45021-2531">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="45021-2532">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="45021-2532">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="45021-2533">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="45021-2533">0.2.0 - September 2018</span></span>
 <span data-ttu-id="45021-2534">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="45021-2534">Initial Release</span></span>
