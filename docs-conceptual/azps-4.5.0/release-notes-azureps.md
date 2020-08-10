---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 77cbbeb01f5c6fcbf0f61bfab3d3f63b74a53bc4
ms.sourcegitcommit: edfe63c6949cd59127028ac8a13bb4a8827d555c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/04/2020
ms.locfileid: "87566623"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="27234-103">Azure PowerShell sürüm notları</span><span class="sxs-lookup"><span data-stu-id="27234-103">Azure PowerShell release notes</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="27234-104">4.5.0 - Ağustos 2020</span><span class="sxs-lookup"><span data-stu-id="27234-104">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-105">Az.Accounts</span></span>
* <span data-ttu-id="27234-106">'Connect-AzAccount' cmdlet’i 'MaxContextPopulation' parametresini kabul edecek şekilde güncelleştirildi [#9865]</span><span class="sxs-lookup"><span data-stu-id="27234-106">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="27234-107">SubscriptionClient sürümü 2019-06-01 olarak ve kiracı etki alanlarını görüntüleyecek şekilde güncelleştirildi [#9838]</span><span class="sxs-lookup"><span data-stu-id="27234-107">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="27234-108">Aboneliğin giriş kiracısı ve yöneten kiracısı bilgilerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-108">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="27234-109">Telemetri verilerindeki modül adı ve sürüm bilgileri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-109">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="27234-110">SqlDatabaseDnsSuffix ve ServiceManagementUrl, ortam meta verileri uç noktasının uyumsuz değer döndürdüğü durumlar için ayarlandı</span><span class="sxs-lookup"><span data-stu-id="27234-110">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="27234-111">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27234-111">Az.Aks</span></span>
* <span data-ttu-id="27234-112">'ClientIdAndSecret' kaldırılarak 'ServicePrincipalIdAndSecret' eklendi ve 'ClientIdAndSecret' bir diğer ad olarak ayarlandı [#12381].</span><span class="sxs-lookup"><span data-stu-id="27234-112">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="27234-113">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' cmdlet’leri kaldırılarak 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' eklendi ve özgün olanlar diğer ad olarak ayarlandı [#12373].</span><span class="sxs-lookup"><span data-stu-id="27234-113">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27234-114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-114">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-115">Yeni 'Add-AzApiManagementApiToGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-115">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="27234-116">Yeni 'Get-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-116">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="27234-117">Yeni 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-117">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="27234-118">Yeni 'Get-AzApiManagementGatewayKey' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-118">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="27234-119">Yeni 'New-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-119">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="27234-120">Yeni 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-120">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="27234-121">Yeni 'New-AzApiManagementResourceLocationObject' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-121">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="27234-122">Yeni 'Remove-AzApiManagementApiFromGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-122">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="27234-123">Yeni 'Remove-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-123">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="27234-124">Yeni 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-124">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="27234-125">Yeni 'Update-AzApiManagementGateway' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-125">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="27234-126">'Get-AzApiManagementApi' cmdlet’ine yeni ve isteğe bağlı [-GatewayId] parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-126">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-127">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-127">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-128">'Deny', özellikle NetworkRules varsayılan eylemi olarak kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-128">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27234-129">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-129">Az.FrontDoor</span></span>
* <span data-ttu-id="27234-130">Enum.Parse metodu, bir null değeri Enabled veya Disabled sabit listesi değerlerine zorladığında özel durum oluşturulmasıyla ilgili bir sorun düzeltildi [#12344]</span><span class="sxs-lookup"><span data-stu-id="27234-130">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-131">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-131">Az.HDInsight</span></span>
* <span data-ttu-id="27234-132">Aktarma özelliğinde şifrelemeye sahip küme oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-132">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="27234-133">'New-AzHDInsightCluster' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-133">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="27234-134">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'EncryptionInTransit' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-134">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="27234-135">Özel bağlantı özelliğine sahip küme oluşturma desteği eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-135">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="27234-136">'New-AzHDInsightCluster' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-136">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="27234-137">'New-AzHDInsightClusterConfig' cmdlet’ine yeni 'PublicNetworkAccessType' ve 'OutboundPublicNetworkAccessType' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-137">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="27234-138">'New-AzHDInsightCluster' veya 'Get-AzHDInsightCluster' çağrıldığında sanal ağ bilgileri döndürüldü</span><span class="sxs-lookup"><span data-stu-id="27234-138">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-139">Az.Network</span></span>
* <span data-ttu-id="27234-140">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-140">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="27234-141">Hataya neden olmayan değişiklikler eklendi: 'Remove-AzExpressRouteCircutPeeringConfig' cmdlet’inde Özel Eşleme’ye yönelik PeerAddressType işlevi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-141">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="27234-142">AddressPrefixType ve PeerAddressType parametresindeki kodlar büyük/küçük harfi yoksayacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-142">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="27234-143">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' ve 'New-AzPublicIpPrefix' uyarı iletisi değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-143">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-144">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-144">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-145">'Remove-AzOperationalInsightsworkspace' için '-ForceDelete' seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-145">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="27234-146">Yeni 'Get-AzOperationalInsightsDeletedWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-146">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="27234-147">Yeni 'Restore-AzOperationalInsightsWorkspace' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-147">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-149">Azure Backup kapsayıcı/öğe keşif deneyimi iyileştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-149">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-150">Az.Resources</span></span>
* <span data-ttu-id="27234-151">'New-AzRoleAssignment' cmdlet’ine 'Condition', 'ConditionVersion' ve 'Description' özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-151">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="27234-152">Bu, veri modellerinde yapılan tüm ilgili değişiklikleri içerir</span><span class="sxs-lookup"><span data-stu-id="27234-152">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-153">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-153">Az.Sql</span></span>
* <span data-ttu-id="27234-154">'New-AzSqlServer' ve 'Set-AzSqlServer' cmdlet’lerindeki sunucu adının olası büyük/küçük harfe duyarsızlık hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-154">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="27234-155">'New-AzSqlDatabaseSecondary' cmdlet’indeki mevcut veritabanına yanlış veritabanı adının döndürülmesi hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-155">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-156">Az.Storage</span></span>
* <span data-ttu-id="27234-157">Yeni x,t izniyle kapsayıcı/blob Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-157">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="27234-158">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="27234-158">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="27234-159">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="27234-159">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="27234-160">Yeni x,t,f izniyle hesap Sas belirteci oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-160">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="27234-161">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="27234-161">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="27234-162">Tek dosya paylaşımı kullanımını alma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-162">Supported get single file share usage</span></span>
    - <span data-ttu-id="27234-163">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="27234-163">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="27234-164">4.4.0 - Temmuz 2020</span><span class="sxs-lookup"><span data-stu-id="27234-164">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-165">Az.Accounts</span></span>
* <span data-ttu-id="27234-166">“Invoke-AzRestMethod” adlı yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-166">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="27234-167">“Start-Job” kullanan birden çok Azure PowerShell cmdlet’inin çalıştığı durumlar gibi çok işlemli senaryolarda kimlik doğrulama hatalarına sebep olabilen bir sorun düzeltildi [#9448]</span><span class="sxs-lookup"><span data-stu-id="27234-167">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="27234-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27234-168">Az.Aks</span></span>
* <span data-ttu-id="27234-169">“Get-AzAks” cmdlet’inin tüm kümeleri almamasına neden olan hata düzeltildi [#12296]</span><span class="sxs-lookup"><span data-stu-id="27234-169">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27234-170">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27234-170">Az.AnalysisServices</span></span>
* <span data-ttu-id="27234-171">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-171">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-172">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-172">Az.Automation</span></span>
* <span data-ttu-id="27234-173">Kaçış karakterleri içeren dizenin bir JSON nesnesine dönüştürülememesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-173">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-174">Az.Compute</span></span>
* <span data-ttu-id="27234-175">“En son” resim sürümü olmadan “New-AzVmss” cmdlet’ini kullanırken görüntülenecek bir uyarı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-175">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-176">Az.DataFactory</span></span>
* <span data-ttu-id="27234-177">Data Factory’ye genel parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-177">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27234-178">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27234-178">Az.EventGrid</span></span>
* <span data-ttu-id="27234-179">2020-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-179">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="27234-180">Yeni özellikler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-180">Added new features:</span></span>
    - <span data-ttu-id="27234-181">Giriş eşleme</span><span class="sxs-lookup"><span data-stu-id="27234-181">Input mapping</span></span>
    - <span data-ttu-id="27234-182">Olay Teslim Şeması</span><span class="sxs-lookup"><span data-stu-id="27234-182">Event Delivery Schema</span></span>
    - <span data-ttu-id="27234-183">Özel Bağlantı</span><span class="sxs-lookup"><span data-stu-id="27234-183">Private Link</span></span>
    - <span data-ttu-id="27234-184">Bulut Olayı V10 Şeması</span><span class="sxs-lookup"><span data-stu-id="27234-184">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="27234-185">Hedef Olarak Service Bus Konu Başlığı</span><span class="sxs-lookup"><span data-stu-id="27234-185">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="27234-186">Hedef Olarak Azure İşlevi</span><span class="sxs-lookup"><span data-stu-id="27234-186">Azure Function As Destination</span></span>
    - <span data-ttu-id="27234-187">Web Kancası Toplu İş</span><span class="sxs-lookup"><span data-stu-id="27234-187">WebHook Batching</span></span>
    - <span data-ttu-id="27234-188">Güvenli web kancası (AAD desteği)</span><span class="sxs-lookup"><span data-stu-id="27234-188">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="27234-189">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="27234-189">IpFiltering</span></span>
* <span data-ttu-id="27234-190">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-190">Updated cmdlets:</span></span>
    - <span data-ttu-id="27234-191">“New-AzEventGridSubscription'/'Update-AzEventGridSubscription”:</span><span class="sxs-lookup"><span data-stu-id="27234-191">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="27234-192">Web kancası toplu işlemin destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-192">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="27234-193">AAD kullanarak güvenli web kancasını desteklemek için yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-193">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="27234-194">Yeni hedef olarak Azure İşlevi’ni ve Service Bus konu başlığını desteklemek üzere EndpointType parametresi için yeni bir sabit listesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-194">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="27234-195">Teslim şeması için yeni, isteğe bağlı parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-195">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="27234-196">“New-AzEventGridTopic'/'Update-AzEventGridTopic” ve “New-AzEventGridDomain'/'Update-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="27234-196">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="27234-197">IpFiltering’i destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-197">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="27234-198">“New-AzEventGridTopic'/'New-AzEventGridDomain”:</span><span class="sxs-lookup"><span data-stu-id="27234-198">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="27234-199">Giriş eşlemeyi destekleyecek yeni, isteğe bağlı parametreler eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-199">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27234-200">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-200">Az.FrontDoor</span></span>
* <span data-ttu-id="27234-201">Modül, API 2020-05-01 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-201">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="27234-202">Depolama, Key Vault ve Web App Service kaynakları için Özel bağlantı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-202">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-203">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-203">Az.HDInsight</span></span>
* <span data-ttu-id="27234-204">Ulusal bulutlarda ADLS 1. veya 2. Nesil depolama ile küme oluşturmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-204">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-205">Az.Monitor</span></span>
* <span data-ttu-id="27234-206">Ölçümler ve günlükler null olduğunda “Get-AzDiagnosticSetting” cmdlet’inde oluşan hata düzeltildi [#12272]</span><span class="sxs-lookup"><span data-stu-id="27234-206">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-207">Az.Network</span></span>
* <span data-ttu-id="27234-208">VWan HubVnet bağlantısında değişen parametreler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-208">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="27234-209">Azure Ağ Sanal Alet Siteleri’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-209">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="27234-210">“Get-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="27234-210">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="27234-211">“New-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="27234-211">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="27234-212">“Remove-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="27234-212">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="27234-213">“Update-AzVirtualApplianceSite”</span><span class="sxs-lookup"><span data-stu-id="27234-213">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="27234-214">“New-AzOffice365PolicyProperty”</span><span class="sxs-lookup"><span data-stu-id="27234-214">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="27234-215">Azure Ağ Sanal Gereçi’ne yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-215">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="27234-216">“Get-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="27234-216">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="27234-217">“New-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="27234-217">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="27234-218">“Remove-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="27234-218">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="27234-219">“Update-AzNetworkVirtualAppliance”</span><span class="sxs-lookup"><span data-stu-id="27234-219">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="27234-220">“Get-AzNetworkVirtualApplianceSku”</span><span class="sxs-lookup"><span data-stu-id="27234-220">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="27234-221">“New-AzVirtualApplianceSkuProperty”</span><span class="sxs-lookup"><span data-stu-id="27234-221">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="27234-222">Özel Bağlantı Ortak Cmdlet’lerine Application Gateway eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-222">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="27234-223">Özel Bağlantı Ortak Cmdlet’lerine StorageSync Eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-223">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="27234-224">Özel Bağlantı Ortak Cmdlet’lerine SignalR Eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-224">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-226">Kimlik Doğrulamasına yönelik proje başvurusu kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-226">Removed project reference to Authentication</span></span>
* <span data-ttu-id="27234-227">Azure Backup, cmdlet’leri metinlerin daha doğru görüneceği şekilde ayarladı</span><span class="sxs-lookup"><span data-stu-id="27234-227">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="27234-228">Azure Backup, “Get-AzRecoveryServicesBackupJob” cmdlet’i kullanılarak MAB aracı işlerinin getirilmesine yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="27234-228">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-229">Az.Resources</span></span>
* <span data-ttu-id="27234-230">“Save-AzResourceGroupDeploymentTemplate” cmdlet’i SDK’yı kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-230">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="27234-231">“Unregister-AzResourceProvider” cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-231">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-232">Az.Sql</span></span>
* <span data-ttu-id="27234-233">“Set-AzSqlInstanceActiveDirectoryAdministrator” cmdlet’indeki Hizmet sorumlusu ve konuk kullanıcılara yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-233">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="27234-234">Veri Sınıflandırma cmdlet’lerindeki bir sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-234">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="27234-235">Azure SQL Yönetilen Örneği yük devretmesine yönelik destek eklendi: “Invoke-AzSqlInstanceFailover”</span><span class="sxs-lookup"><span data-stu-id="27234-235">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-236">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-236">Az.Storage</span></span>
* <span data-ttu-id="27234-237">Bazı veri düzlemi cmdlet’leri için UserAgent’ın eklenmemesiyle ilgili sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-237">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="27234-238">MinimumTlsVersion ve AllowBlobPublicAccess içeren bir Depolama hesabını oluşturmaya/güncelleştirmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-238">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="27234-239">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27234-239">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="27234-240">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27234-240">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27234-241">Bir Depolama hesabının Blob Hizmeti üzerinde sürüm oluşturmayı etkinleştirmeye/devre dışı bırakmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-241">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="27234-242">“Update-AzStorageBlobServiceProperty”</span><span class="sxs-lookup"><span data-stu-id="27234-242">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="27234-243">Blob sürümlerini içeren destek listesi blobları</span><span class="sxs-lookup"><span data-stu-id="27234-243">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="27234-244">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="27234-244">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="27234-245">Tek bir blob anlık görüntüsünü veya blob sürümünü almaya/kaldırmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-245">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="27234-246">“Get-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="27234-246">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="27234-247">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="27234-247">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="27234-248">Azure.Storage.Blobs V12’den oluşturulan blob nesnesindeki işlem hattına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-248">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="27234-249">“Get-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="27234-249">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="27234-250">“New-AzStorageBlobSASToken”</span><span class="sxs-lookup"><span data-stu-id="27234-250">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="27234-251">“Remove-AzStorageBlob”</span><span class="sxs-lookup"><span data-stu-id="27234-251">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="27234-252">“Set-AzStorageBlobContent”</span><span class="sxs-lookup"><span data-stu-id="27234-252">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="27234-253">“Start-AzStorageBlobCopy”</span><span class="sxs-lookup"><span data-stu-id="27234-253">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27234-254">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27234-254">Az.StorageSync</span></span>
* <span data-ttu-id="27234-255">ApiVersion 2020-03-01 sürümünü hedefleyen yeni bir StorageSync SDK sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-255">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="27234-256">“UpdateStorageSyncService” cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-256">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="27234-257">“Set-AzStorageSyncService”</span><span class="sxs-lookup"><span data-stu-id="27234-257">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="27234-258">StorageSyncService cmdlet’ine IncomingTrafficPolicy ve PrivateEndpointConnections eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-258">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-259">Az.Websites</span></span>
* <span data-ttu-id="27234-260">App Service Planıyla aynı kaynak grubunda bulunmayan Yuvalar için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-260">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="27234-261">4.3.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="27234-261">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-262">Az.Accounts</span></span>
* <span data-ttu-id="27234-263">Ortam ayarını varsayılan olarak bulma ve 'Add-AzEnvironment' aracılığıyla ortam ekleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-263">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="27234-264">Önceden yüklenmiş bütünleştirilmiş kodlar güncelleştirildi [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="27234-264">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="27234-265">Azure.Core bütünleştirilmiş kodu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-265">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="27234-266">'Connect-AzAccount' cmdlet’inin çok iş parçacıklı yürütmede başarısız olmasına neden olabilen bir sorun düzeltildi [#11201]</span><span class="sxs-lookup"><span data-stu-id="27234-266">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="27234-267">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27234-267">Az.Aks</span></span>
* <span data-ttu-id="27234-268">Eski [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)’sinin kullanımı [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) ve [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API’lerine yönelik çağrılarla değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-268">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27234-269">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27234-269">Az.Batch</span></span>
* <span data-ttu-id="27234-270">Az.Batch, 'Microsoft.Azure.Management.Batch' SDK sürüm 11.0.0 kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-270">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="27234-271">BatchAccount.Identity özelliğini 'New-AzBatchAccount' cmdlet’ine ayarlama özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-271">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-272">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-272">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-273">Hesap özelliklerini görüntüleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-273">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="27234-274">PublicNetworkAccess özelliğinin değiştirilmesi desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-274">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-275">Az.Compute</span></span>
* <span data-ttu-id="27234-276">Set-AzVM ve Set-AzVmssVM cmdlet’lerine SimulateEviction parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-276">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="27234-277">New-AzGalleryImageVersion cmdlet’i için StorageAccountType parametresinin bağımsız değişken tamamlayıcısına 'Premium_LRS' eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-277">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="27234-278">VMCustomScriptExtension için Alt Durumlar eklendi [#11297]</span><span class="sxs-lookup"><span data-stu-id="27234-278">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="27234-279">New-AzVM ve New-AzVMConfig cmdlet’leri için EvictionPolicy parametresinin bağımsız değişken tamamlayıcısına 'Delete' eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-279">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="27234-280">SAP için yeni VM Uzantısı’nın adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-280">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-281">Az.DataFactory</span></span>
* <span data-ttu-id="27234-282">ADF .NET SDK’sı 4.9.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-282">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27234-283">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27234-283">Az.EventHub</span></span>
* <span data-ttu-id="27234-284">'New-AzEventHubNamespace' ve 'Set-AzEventHubNamespace' cmdlet’lerine Yönetilen Kimlik parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-284">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="27234-285">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="27234-285">Az.Functions</span></span>
* <span data-ttu-id="27234-286">PowerShell 7.0 ve Java 11 işlev uygulamaları oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-286">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-287">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-287">Az.HDInsight</span></span>
* <span data-ttu-id="27234-288">HDInsight kümesinin konaklarını listeleme ve belirli konaklarını yeniden başlatma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-288">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27234-289">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27234-289">Az.HealthcareApis</span></span>
* <span data-ttu-id="27234-290">SDK sürümü 1.1.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-290">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="27234-291">Dışarı aktarma ayarları ve Yönetilen Kimlik desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-291">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-292">Az.Monitor</span></span>
* <span data-ttu-id="27234-293">'Set-AzActivityLogAlert' için giriş nesnesi parametresi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-293">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="27234-294">'Set-AzActionGroup' için 'InputObject' parametresi düzeltildi [#10868]</span><span class="sxs-lookup"><span data-stu-id="27234-294">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-295">Az.Network</span></span>
* <span data-ttu-id="27234-296">'Remove-AzExpressRouteCircuitConnectionConfig' cmdlet’ine yönelik AddressPrefixType parametresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-296">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="27234-297">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-297">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="27234-298">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="27234-298">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="27234-299">Güvenlik Duvarı İlkesi için Ağ Kuralları’nda Hedef FQDN Desteği</span><span class="sxs-lookup"><span data-stu-id="27234-299">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="27234-300">Arka uç adres havuzu işlemlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-300">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="27234-301">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="27234-301">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="27234-302">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="27234-302">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="27234-303">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="27234-303">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="27234-304">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="27234-304">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="27234-305">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="27234-305">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="27234-306">'New-AzIpGroup' için ad doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-306">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="27234-307">Azure FirewallPolicy için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-307">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="27234-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="27234-308">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="27234-309">Özellik için aşağıdaki komutlar güncelleştirildi: VirtualWan P2SVpnGateway üzerinde özel DNS sunucuları ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="27234-309">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="27234-310">New-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-310">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="27234-311">Update-AzP2sVpnGateway güncelleştirildi: Müşterilerin DNS sunucularını, Noktadan siteye işlemciler tarafından kullanılabilen P2SVpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-CustomDnsServer' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-311">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="27234-312">'Update-AzVpnGateway' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-312">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="27234-313">Müşterilerin özel BGP’lerini VpnGateway üzerinde ayarlanacak şekilde belirtmeleri için '-BgpPeeringAddress' isteğe bağlı parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-313">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="27234-314">Bir VirtualHub kaynağının yönlendirme durumunu sıfırlamayı desteklemek amacıyla yeni cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-314">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="27234-315">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="27234-315">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="27234-316">Güvenlik Duvarı İlkesi’nde yapılan son Swagger değişikliğine göre aşağıdakiler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-316">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="27234-317">RuleGroup, RuleCollectionGroup ve RuleType adları değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-317">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="27234-318">Birden çok NAT Kural Koleksiyonu’nu desteklemek amacıyla Güvenlik Duvarı İlkesi NAT Kural Koleksiyonları’na yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-318">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="27234-319">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule' ve 'New-AzFirewallPolicyNetworkRule' için 'SourceIpGroup' zorunlu parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-319">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="27234-320">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-320">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="27234-321">[Yeni Değişiklik] 'New-AzFirewallPolicyApplicationRule', 'SourceAddress' parametresi zorunlu olacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-321">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="27234-322">[Yeni Değişiklik] Şu zorunu parametreler kaldırıldı: 'New-AzFirewallPolicyNatRuleCollection' için 'TranslatedAddress', 'TranslatedPort'.</span><span class="sxs-lookup"><span data-stu-id="27234-322">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="27234-323">Application Gateway üzerinde PrivateLink’i destekleyecek yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-323">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="27234-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-324">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27234-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-325">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27234-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-326">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27234-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-327">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27234-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-328">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="27234-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-329">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="27234-330">VirtualHub’ın HubRouteTables alt kaynağı için yeni cmdlet’ler eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-330">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="27234-331">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="27234-331">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="27234-332">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="27234-332">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="27234-333">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="27234-333">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="27234-334">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="27234-334">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="27234-335">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="27234-335">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="27234-336">Mevcut cmdlet’ler VirtualWan’deki özel yönlendirmede isteğe bağlı RoutingConfiguration giriş parametresini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-336">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="27234-337">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="27234-337">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="27234-338">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="27234-338">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="27234-339">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="27234-339">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27234-340">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="27234-340">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27234-341">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="27234-341">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="27234-342">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="27234-342">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="27234-343">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="27234-343">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="27234-344">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="27234-344">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-345">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-345">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-346">PSWorkspace’in OperationalInsightsWorkspace’i uygulamamasıyla ilgili hata düzeltildi [#12135]</span><span class="sxs-lookup"><span data-stu-id="27234-346">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="27234-347">'Set-AzOperationalInsightsWorkspace' cmdlet’indeki 'Sku' parametresinin geçerli değer kümesine 'pergb2018' eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-347">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="27234-348">'FunctionParameter' parametresi için 'FunctionParameters' diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-348">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="27234-349">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="27234-349">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="27234-350">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="27234-350">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-352">Azure Backup’a MAB öğelerini getirme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-352">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="27234-353">Azure Site Recovery, 'StandardSSD_LRS' disk türünü destekler</span><span class="sxs-lookup"><span data-stu-id="27234-353">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-354">Az.Resources</span></span>
* <span data-ttu-id="27234-355">'PSADUser' değerine 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname' eklendi [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="27234-355">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="27234-356">'Get-AzADUser' üzerinde '-Mail' değerinin çalışmamasıyla ilgili sorun düzeltildi [#11981]</span><span class="sxs-lookup"><span data-stu-id="27234-356">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="27234-357">'Get-AzDeploymentWhatIfResult' ve 'Get-AzResourceGroupDeploymentWhatIfResult' cmdlet’lerine -ExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-357">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="27234-358">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' cmdlet’lerine '-WhatIfExcludeChangeType' parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-358">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="27234-359">'Test-Az\*Deployment' cmdlet’leri daha iyi hata iletileri gösterecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-359">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="27234-360">deployment create ve What-If cmdlet’lerinin '-Name' parametresine yönelik yardım iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-360">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-361">Az.Sql</span></span>
* <span data-ttu-id="27234-362">SQL Server Azure Active Directory Yönetici cmdlet’ine hizmet sorumlusu desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-362">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="27234-363">Veri Sınıflandırma cmdlet’lerindeki eşitleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-363">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="27234-364">'Set-AzSqlServerActiveDirectoryAdministrator' üzerinde postaya göre kullanıcı arama desteği eklendi [#12192]</span><span class="sxs-lookup"><span data-stu-id="27234-364">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-365">Az.Storage</span></span>
* <span data-ttu-id="27234-366">RequireInfrastructureEncryption ile Depolama hesabı oluşturma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-366">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="27234-367">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27234-367">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="27234-368">Azure.Core yükleme mantığı Az.Accounts’a taşındı</span><span class="sxs-lookup"><span data-stu-id="27234-368">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-369">Az.Websites</span></span>
* <span data-ttu-id="27234-370">'Restore-AzDeletedWebApp' cmdlet’inde geri yüklemenin başarısız olması durumunda, oluşturulan web uygulamasının silinmesine yönelik koruma eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-370">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="27234-371">'New-AzWebApp' ve 'New-AzWebAppSlot' için SourceWebApp.Location' eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-371">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="27234-372">'Set-AzWebApp' ve 'Set-AzWebAppSlot' cmdlet’lerinde Kapsayıcı ayarlarının değiştirilmesini engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-372">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="27234-373">Get-AzWebApp için -Name verilmediğinde SiteConfig alınmasıyla ilgili hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-373">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="27234-374">Linux Uygulamaları için ASP oluşturmaya yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-374">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="27234-375">Kaynak grupları arasında kopyalama için özel durumlar eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-375">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="27234-376">4.2.0 - Haziran 2020</span><span class="sxs-lookup"><span data-stu-id="27234-376">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-377">Az.Accounts</span></span>
* <span data-ttu-id="27234-378">Azure Otomasyonu veya PowerShell işlerinde Az’nin günlükleri atlamasına neden olabilecek bir sorun düzeltildi [#11492]</span><span class="sxs-lookup"><span data-stu-id="27234-378">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27234-379">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27234-379">Az.AnalysisServices</span></span>
* <span data-ttu-id="27234-380">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-380">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27234-381">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-381">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-382">Hizmet yönetimi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-382">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="27234-383">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="27234-383">Az.Billing</span></span>
* <span data-ttu-id="27234-384">Tüketim cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-384">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-386">PrivateEndpoint ve PublicNetworkAccess denetimini destekler.</span><span class="sxs-lookup"><span data-stu-id="27234-386">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="27234-387">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-387">Az.DataFactory</span></span>
* <span data-ttu-id="27234-388">Veri fabrikası V2 cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-388">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="27234-389">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="27234-389">Az.DataShare</span></span>
* <span data-ttu-id="27234-390">''Az.DataShare'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-390">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="27234-391">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="27234-391">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="27234-392">''Az.DesktopVirtualization'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-392">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-393">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-393">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-394">SDK 0.21.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-394">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="27234-395">İsteğe bağlı aşağıdaki parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-395">Added optional parameters to</span></span> 
    - <span data-ttu-id="27234-396">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="27234-396">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="27234-397">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="27234-397">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27234-398">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27234-398">Az.PolicyInsights</span></span>
* <span data-ttu-id="27234-399">'Start-AzPolicyComplianceScan' için 3. örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-399">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="27234-400">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="27234-400">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="27234-401">PowerBI cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-401">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="27234-402">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="27234-402">Az.PrivateDns</span></span>
* <span data-ttu-id="27234-403">Remove-AzPrivateDnsRecordSet için ayrıntılı çıkış dizesi biçimlendirmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-403">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-404">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-404">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-405">XML girişinden bölgeler arasında çoğaltma için kurtarma planı oluşturmaya yönelik Azure Site Recovery desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-405">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="27234-406">SiteRecovery ve Backup cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-406">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-407">Az.Resources</span></span>
* <span data-ttu-id="27234-408">Get-AzDeploymentScriptLog ve Save-AzDeploymentScriptLog cmdlet’lerine Tail parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-408">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="27234-409">Çıkış özelliği biçimlendirildi ve Get-AzDeploymentScript cmdlet çıkışında gösterildi</span><span class="sxs-lookup"><span data-stu-id="27234-409">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="27234-410">-DeploymentScriptInputObject parametresinin adı -DeploymentScriptObject olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-410">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="27234-411">Cmdlet iletilerinde geçersiz dosya/hedef adı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-411">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="27234-412">Kaynak yöneticisi ve etiketler cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-412">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-413">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-413">Az.Sql</span></span>
* <span data-ttu-id="27234-414">'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine UsePrivateLinkConnection eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-414">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="27234-415">'New-AzSqlSyncMember' ve 'Update-AzSqlSyncMember' öğelerine SyncMemberAzureDatabaseResourceId eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-415">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="27234-416">SQL Server Azure Active Directory Yönetici cmdlet’ine Konuk kullanıcı arama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-416">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-417">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-417">Az.Storage</span></span>
* <span data-ttu-id="27234-418">Veri düzlemi cmdlet’lerinin derleme sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-418">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="27234-419">4.1.0 - Mayıs 2020</span><span class="sxs-lookup"><span data-stu-id="27234-419">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="27234-420">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="27234-420">Highlights since the last release</span></span>
* <span data-ttu-id="27234-421">Desteklenen PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="27234-421">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="27234-422">Az.Functions genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-422">General availability of Az.Functions</span></span> 
* <span data-ttu-id="27234-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources ve Az.Storage için ana sürüm yayımlandı</span><span class="sxs-lookup"><span data-stu-id="27234-423">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-424">Az.Accounts</span></span>
* <span data-ttu-id="27234-425">'Add-AzEnvironment' ve 'Set-AzEnvironment', 'AzureSynapseAnalyticsEndpointResourceId' ve 'AzureSynapseAnalyticsEndpointSuffix' parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-425">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="27234-426">Azure.Core ile ilgili bütünleştirilmiş kodlar Az.Accounts’a eklendi, desteklenen PowerShell platformları Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+ sürümlerini içerir</span><span class="sxs-lookup"><span data-stu-id="27234-426">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="27234-427">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27234-427">Az.Aks</span></span>
* <span data-ttu-id="27234-428">API Sürümü 2019-10-01’e yükseltildi</span><span class="sxs-lookup"><span data-stu-id="27234-428">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="27234-429">Windows kapsayıcısı kullanılarak AKS oluşturma desteği sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-429">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="27234-430">Yeni cmdlet’ler sağlandı: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="27234-430">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27234-431">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-431">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-432">'New-AzApiManagement' ve 'Set-AzApiManagement': [-AssignIdentity] parametresi [-SystemAssignedIdentity] olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-432">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="27234-433">'New-AzApiManagement' ve 'Set-AzApiManagement': Yeni parametre eklendi: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="27234-433">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="27234-434">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-434">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27234-435">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-435">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="27234-436">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-436">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27234-437">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-437">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="27234-438">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-438">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27234-439">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-439">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="27234-440">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue' olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-440">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="27234-441">PropertyId parametresi NamedValueId olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-441">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="27234-442">Yeni 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementAuthorizationServer' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="27234-442">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="27234-443">Yeni 'Get-AzApiManagementNamedValueSecretValue' cmdlet’i eklendi. 'Get-AzApiManagementNamedValue' artık gizli dizi değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="27234-443">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="27234-444">Yeni 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet’i eklendi. 'Get-AzApiManagementOpenIdConnectProvider' artık istemci gizli dizisini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="27234-444">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="27234-445">Yeni 'Get-AzApiManagementSubscriptionKey' cmdlet’i eklendi. 'Get-AzApiManagementSubscription' artık abonelik anahtarlarını döndürmez.</span><span class="sxs-lookup"><span data-stu-id="27234-445">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="27234-446">Yeni 'Get-AzApiManagementTenantAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="27234-446">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="27234-447">Yeni 'Get-AzApiManagementTenantGitAccessSecret' cmdlet’i eklendi. 'Get-AzApiManagementTenantGitAccess' artık anahtarları döndürmez.</span><span class="sxs-lookup"><span data-stu-id="27234-447">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="27234-448">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="27234-448">Az.ApplicationInsights</span></span>
* <span data-ttu-id="27234-449">Parametreler eklendi: 'New-AzApplicationInsights' için 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="27234-449">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="27234-450">'Update-AzApplicationInsights' cmdlet’i oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-450">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="27234-451">Bağlı Depolama Hesapları için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-451">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27234-452">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27234-452">Az.Batch</span></span>
* <span data-ttu-id="27234-453">Az.Batch, 'Microsoft.Azure.Batch' SDK sürüm 13.0.0 ve 'Microsoft.Azure.Management.Batch' SDK sürüm 9.0.0 kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-453">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="27234-454">'New-AzBatchCertificate' için yeni '-CertificateKind' parametresi kullanılarak eklenen sertifika türünü seçme yeteneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-454">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="27234-455">Önceden hep '' olan 'ApplicationPackages' özelliği 'PSApplication' öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-455">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="27234-456">Uygulamanın içindeki belirli paketler artık 'Get-AzBatchApplicationPackage' kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="27234-456">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="27234-457">Örneğin: 'Get-AzBatchApplication -AccountName hesabım -ResourceGroupName kaynakgrubum -ApplicationId uygulamam'.</span><span class="sxs-lookup"><span data-stu-id="27234-457">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="27234-458">'New-AzBatchPool' kullanılarak havuz oluşturulurken, 'PSImageReference' öğesinin 'VirtualMachineImageId' özelliği artık yalnızca bir Paylaşılan Görüntü Galerisi görüntüsüne başvurabilir.</span><span class="sxs-lookup"><span data-stu-id="27234-458">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="27234-459">'New-AzBatchPool' kullanılarak havuz oluşturulurken, havuz 'PSNetworkConfiguration' öğesinin yeni 'PublicIPAddressConfiguration' özelliği kullanılarak genel IP olmadan sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="27234-459">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="27234-460">'PSNetworkConfiguration' öğesinin 'PublicIPs' özelliği de 'PSPublicIPAddressConfiguration' içine taşındı.</span><span class="sxs-lookup"><span data-stu-id="27234-460">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="27234-461">Bu özellik yalnızca 'IPAddressProvisioningType' değeri 'UserManaged' olduğunda belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="27234-461">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-462">Az.Compute</span></span>
* <span data-ttu-id="27234-463">'Update-AzVM' cmdlet’ine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-463">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="27234-464">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' ve 'Set-AzVmssOsProfile' cmdlet’leri için Yardım belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-464">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="27234-465">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="27234-465">Breaking changes</span></span>
    - <span data-ttu-id="27234-466">FilterExpression parametresi 'Get-AzVMImage' cmdlet’inden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-466">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="27234-467">AssignIdentity parametresi 'New-AzVmssConfig', 'New-AzVMConfig' ve 'Update-AzVM' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-467">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="27234-468">AutomaticRepairMaxInstanceRepairsPercent, 'New-AzVmssConfig' ve 'Update-AzVmss' cmdlet’lerinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-468">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="27234-469">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus ve VirtualMachineScaleSetsColocationStatus özellikleri ProximityPlacementGroup öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-469">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="27234-470">MaxInstanceRepairsPercent özelliği AutomaticRepairsPolicy öğesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-470">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="27234-471">AvailabilitySets, VirtualMachines ve VirtualMachineScaleSets türleri IList<SubResource> türünden IList<SubResourceWithColocationStatus> türüne değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-471">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="27234-472">'Get-AzVM' cmdlet’inin açıklaması, cmdlet’i daha iyi açıklayacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-472">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="27234-473">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-473">Az.DataFactory</span></span>
* <span data-ttu-id="27234-474">Yönetilen IR içinde veri akışı çalışma zamanı özelliklerinin CRUD’si desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-474">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27234-475">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-475">Az.FrontDoor</span></span>
* <span data-ttu-id="27234-476">Front Door Kural Altyapısı nesnesini oluşturmak, güncelleştirmek, almak ve silmek için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-476">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="27234-477">Front Door Kural Altyapısı nesnesini oluşturmak için yardımcı cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-477">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="27234-478">Front Door Yönlendirme Kuralı nesnesine Kural Altyapısı başvurusu eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-478">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="27234-479">Front Door Arka Uç nesnesine Özel Bağlantı parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-479">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="27234-480">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="27234-480">Az.Functions</span></span>
* <span data-ttu-id="27234-481">''Az.Functions'' modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-481">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-482">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-482">Az.HDInsight</span></span>
* <span data-ttu-id="27234-483">Müşteri tarafından yönetilen anahtar disk şifrelemesi desteği sunuldu.</span><span class="sxs-lookup"><span data-stu-id="27234-483">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27234-484">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27234-484">Az.HealthcareApis</span></span>
* <span data-ttu-id="27234-485">Erişim ilkeleri artık varsayılan olarak geçerli sorumluyu kullanmıyor</span><span class="sxs-lookup"><span data-stu-id="27234-485">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-486">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-486">Az.IotHub</span></span>
* <span data-ttu-id="27234-487">SQL benzeri bir dil kullanarak bilgi almak üzere bir IoT hub’ında sorgu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-487">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="27234-488">'Add-AzIotHubDevice' cmdlet’inin alt cihaz olmadan Uç Özellikli Cihaz oluşturamaması sorunu düzeltildi [#11597]</span><span class="sxs-lookup"><span data-stu-id="27234-488">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="27234-489">IoT hub’ı, cihaz veya modül için SAS belirteci oluşturmak üzere cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-489">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="27234-490">Yapılandırma ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-490">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="27234-491">IoT Edge otomatik dağıtımını büyük ölçekte yönetin.</span><span class="sxs-lookup"><span data-stu-id="27234-491">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="27234-492">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-492">New cmdlets are:</span></span>
    - <span data-ttu-id="27234-493">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="27234-493">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="27234-494">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="27234-494">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="27234-495">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="27234-495">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="27234-496">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="27234-496">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="27234-497">IoT Edge dağıtım ölçümleri sorgusunu çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-497">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="27234-498">Yapılandırma içeriğini belirtilen uç cihaza uygulamak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-498">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-499">Az.KeyVault</span></span>
* <span data-ttu-id="27234-500">İki diğer ad kaldırıldı: 'New-AzKeyVaultCertificateAdministratorDetails' ve 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="27234-500">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="27234-501">Anahtar kasası oluştururken varsayılan olarak geçici silme etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-501">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="27234-502">Ağ kuralları, bir anahtar kasası oluştururken belirli ağ konumlarından erişilebilirliği yönetecek şekilde ayarlanabilir</span><span class="sxs-lookup"><span data-stu-id="27234-502">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="27234-503">Kendi anahtarını getir (BYOK) desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-503">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="27234-504">'Add-AzKeyVaultKey' anahtar değişim anahtarı oluşturmayı destekler</span><span class="sxs-lookup"><span data-stu-id="27234-504">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="27234-505">'Get-AzKeyVaultKey' genel bir anahtarı PEM biçiminde indirmeyi destekler</span><span class="sxs-lookup"><span data-stu-id="27234-505">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="27234-506">'Add-AzKeyVaultKey' yardım belgesinin 'KeyOps' bölümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-506">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-507">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-507">Az.Monitor</span></span>
* <span data-ttu-id="27234-508">'Set-AzDiagnosticSettings' için saklama ilkesinin tüm kategorilere uygulanmadığı hata düzeltildi [#11589]</span><span class="sxs-lookup"><span data-stu-id="27234-508">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="27234-509">Ölçüm uyarısı V2 için WebTest kullanılabilirlik ölçütleri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-509">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="27234-510">'New-AzMetricAlertRuleV2Criteria': Web testi kullanılabilirlik ölçütü oluşturma seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-510">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="27234-511">'Add-AzMetricAlertRuleV2': Yeni web testi kullanılabilirlik ölçütünü destekler</span><span class="sxs-lookup"><span data-stu-id="27234-511">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="27234-512">PSLogProfile içinde RetentionPolicy için gereksiz tanım kaldırıldı [#7608]</span><span class="sxs-lookup"><span data-stu-id="27234-512">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="27234-513">PSEventData içinde tanımlanan gereksiz özellikler kaldırıldı [#11353]</span><span class="sxs-lookup"><span data-stu-id="27234-513">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="27234-514">'Get-AzLog', 'Get-AzActivityLog' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-514">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-515">Az.Network</span></span>
* <span data-ttu-id="27234-516">Bölge varsayılan davranışının değiştirileceğini bildirmek için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-516">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="27234-517">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="27234-517">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="27234-518">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="27234-518">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="27234-519">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="27234-519">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="27234-520">Yeni üst düzey SecurityPartnerProvider kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-520">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="27234-521">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-521">New cmdlets added:</span></span>
        - <span data-ttu-id="27234-522">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="27234-522">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="27234-523">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="27234-523">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="27234-524">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="27234-524">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="27234-525">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="27234-525">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="27234-526">'PSPrivateLinkResource' üzerinde 'RequiredZoneNames' ve 'PSPrivateEndpointConnection' üzerinde 'GroupId' eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-526">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="27234-527">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject için SuccessThresholdRoundTripTimeMs parametresinin hatalı türü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-527">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="27234-528">VirtualWan cmdlet’leri AllowVnetToVnetTraffic bağımsız değişkeninin varsayılan değerini True olarak ayarlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-528">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="27234-529">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="27234-529">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="27234-530">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="27234-530">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="27234-531">Özel uç nokta için DNS bölgesi grubunu desteklemek amacıyla yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-531">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="27234-532">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="27234-532">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="27234-533">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="27234-533">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="27234-534">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="27234-534">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="27234-535">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="27234-535">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="27234-536">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="27234-536">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="27234-537">'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' ve 'DNSServers' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-537">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="27234-538">'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' ve 'DnsServer' parametreleri 'AzureFirewall' öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-538">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="27234-539">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-539">Updated cmdlet:</span></span>
        - <span data-ttu-id="27234-540">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="27234-540">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-541">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-541">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-542">Yeni oluşturulan SDK’yı uygulamak için eski kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-542">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="27234-543">Kullanımdan kaldırılan API’ler nedeniyle silinen cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-543">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="27234-544">'Get-AzOperationalInsightsSavedSearchResult' (diğer adı 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="27234-544">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="27234-545">'Get-AzOperationalInsightsSearchResult' (diğer adı 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="27234-545">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="27234-546">'Get-AzOperationalInsightsLinkTarget' (diğer adı 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="27234-546">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="27234-547">'Set-AzOperationalInsightsWorkspace' ve 'New-AzOperationalInsightsWorkspace' için parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-547">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="27234-548">Bağlı Depolama Hesabı için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-548">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="27234-549">Kümeler ve Bağlı Hizmet için cmdlet’ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-549">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-550">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-551">Azure Site Recovery’de Azure’dan Azure’a sağlayıcı için yakın yerleştirilen grup sanal makinelerini korumak üzere destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-551">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="27234-552">Azure Site Recovery’de bölgeden bölgeye çoğaltma için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-552">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="27234-553">Azure Backup’ta Azure Dosya Paylaşımı Kurtarma Noktaları için uzun süreli saklama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-553">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="27234-554">Azure Backup’ta 'Get-AzRecoveryServicesBackupItem' cmdlet’inin çıkışına disk hariç tutma özellikleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-554">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="27234-555">Site Recovery hizmeti için Kasa kimlik bilgilerine yönelik özel uç noktalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-555">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-556">Az.Resources</span></span>
* <span data-ttu-id="27234-557">Yeni bir Rol Tanımı oluşturulurken görüntüleme gecikmesi hakkında ileti uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-557">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="27234-558">Kesin tür belirtilmiş nesne çıkışı için ilke cmdlet’leri değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-558">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="27234-559">'Get-AzResourceLock' cmdlet’i üzerinde kullanılan '-TenantLevel' parametresi kaldırıldı [#11335]</span><span class="sxs-lookup"><span data-stu-id="27234-559">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="27234-560">'Remove-AzResourceGroup -Id ResourceId' düzeltildi [#9882]</span><span class="sxs-lookup"><span data-stu-id="27234-560">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="27234-561">Kaynak grubu kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="27234-561">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="27234-562">Abonelik kapsamında ARM şablonu Durum çözümlemesi sonuçlarını almak için yeni cmdlet eklendi: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="27234-562">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="27234-563">Diğer ad: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="27234-563">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="27234-564">'New-AzDeployment' ve 'New-AzResourceGroupDeployment' için '-WhatIf' ve '-Confirm' parametreleri ARM şablonu Durum sonuçlarını kullanmak için geçersiz kılındı</span><span class="sxs-lookup"><span data-stu-id="27234-564">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="27234-565">Dağıtım cmdlet’lerinde 'ApiVersion' parametresi için kullanımdan kaldırma iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-565">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="27234-566">Dağıtım hataları için iyileştirilmiş hata iletilerini gösterme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-566">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="27234-567">Dağıtım hataları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-567">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="27234-568">Dağıtım betiği çıkışına 'error' özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-568">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="27234-569">NuGet Microsoft.Azure.Management.ResourceManager '3.7.1-preview' sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-569">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="27234-570">DeploymentValidateResult içindeki Error özelliği nuget 3.7.1-preview sürümünden itibaren salt okunur olarak değiştirildiğinden belirli test çalışmaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-570">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="27234-571">SDK ResourceManager 3.7.1-preview sürümünden GenericResourceExpanded öğesi getirildi</span><span class="sxs-lookup"><span data-stu-id="27234-571">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="27234-572">Dağıtım için tüm Get cmdlet’lerine yönelik etiket desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-572">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="27234-573">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="27234-573">'New-AzDeployment'</span></span>
    - <span data-ttu-id="27234-574">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="27234-574">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="27234-575">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="27234-575">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="27234-576">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="27234-576">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27234-577">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-577">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-578">Yanlış sertifika parmak izini alan --SecretIdentifier parametresini kullanarak sertifika ekleme özelliğindeki hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-578">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-579">Az.Sql</span></span>
* <span data-ttu-id="27234-580">Şunların performansı iyileştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-580">Enhance performance of:</span></span>
    - <span data-ttu-id="27234-581">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="27234-581">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27234-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="27234-582">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27234-583">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="27234-583">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27234-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="27234-584">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="27234-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="27234-585">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="27234-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="27234-586">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="27234-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="27234-587">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="27234-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="27234-588">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="27234-589">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet’inden 'RetentionDays' parametresinin istemci tarafı doğrulaması kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-589">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="27234-590">Sanal ağ içindeki bir depolama hesabına denetim yapılarak Depolama Blob Verileri Katkıda Bulunan rolünün oluşturulması sırasında karşılaşılan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-590">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-591">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-591">Az.Storage</span></span>
* <span data-ttu-id="27234-592">'Get-AzStorageAccount' hesap alma/listeleme cmdlet’ine '-AsJob' eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-592">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="27234-593">Anahtar otomatik döndürmesini desteklemek için Depolama hesabı KeyvaultEncryption ile güncelleştirilirken KeyVersion isteğe bağlı hale getirildi</span><span class="sxs-lookup"><span data-stu-id="27234-593">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="27234-594">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27234-594">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27234-595">İşlem hattıyla Azure Dosya Dizinini kaldırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-595">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="27234-596">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="27234-596">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="27234-597">Düzeltildi [#9880]: NetWorkRule DefaultAction değer tanımı swagger ile uyumlu olacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-597">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="27234-598">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="27234-598">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="27234-599">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="27234-599">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="27234-600">Düzeltildi [#11624]: Sunucu hatasından kaçınmak için NetworkRules eklenirken yinelenen kuralları atla</span><span class="sxs-lookup"><span data-stu-id="27234-600">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="27234-601">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="27234-601">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="27234-602">Microsoft.Azure.Cosmos.Table SDK 1.0.7 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="27234-602">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="27234-603">DataLake 2. Nesil Öğeleri listesinde yalnızca bazı öğeler döndürüldüğünde kullanıcıya ContinuationToken ile yeniden listelemesini anımsatmak için uyarı iletisi eklendi,</span><span class="sxs-lookup"><span data-stu-id="27234-603">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="27234-604">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="27234-604">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="27234-605">Azure Dosyalar Active Directory Domain Services Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-605">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="27234-606">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27234-606">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="27234-607">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27234-607">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27234-608">Depolama hesabının Kerberos anahtarlarını yeni oluşturma veya listeleme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-608">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="27234-609">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="27234-609">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="27234-610">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="27234-610">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="27234-611">Yük devretme Depolama hesabı desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-611">Supported failover Storage account</span></span>
    - <span data-ttu-id="27234-612">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="27234-612">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="27234-613">'Get-AzStorageBlobCopyState' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-613">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="27234-614">'Get-AzStorageFileCopyState' ve 'Start-AzStorageBlobCopy' yardımı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-614">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="27234-615">Depolama istemci kitaplığı v12, Kuyruk ve Dosya cmdlet’leriyle tümleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-615">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="27234-616">CloudFile olan çıkış türü AzureStorageFile olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="27234-616">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="27234-617">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="27234-617">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="27234-618">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="27234-618">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="27234-619">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="27234-619">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="27234-620">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="27234-620">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="27234-621">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="27234-621">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="27234-622">CloudFileDirectory olan çıkış türü AzureStorageFileDirectory olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="27234-622">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="27234-623">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="27234-623">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="27234-624">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="27234-624">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="27234-625">CloudFileShare olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="27234-625">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="27234-626">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="27234-626">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="27234-627">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="27234-627">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="27234-628">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="27234-628">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="27234-629">FileShareProperties olan çıkış türü AzureStorageFileShare olarak değiştirildi, özgün çıkış yeni çıkışın bir alt alt özelliği olacak</span><span class="sxs-lookup"><span data-stu-id="27234-629">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="27234-630">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="27234-630">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="27234-631">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="27234-631">Az.TrafficManager</span></span>
* <span data-ttu-id="27234-632">'DisableAzureTrafficManagerEndpoint' ayrıntılı çıkışındaki hatalı profil adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-632">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-633">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-633">Az.Websites</span></span>
* <span data-ttu-id="27234-634">'Update-AzWebAppAccessRestrictionConfig' yardımındaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-634">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="27234-635">3.8.0 - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="27234-635">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="27234-636">Son sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="27234-636">Highlights since the last release</span></span>
* <span data-ttu-id="27234-637">Az.Storage’ın desteklediği PowerShell sürümleri: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="27234-637">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-638">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-638">Az.Accounts</span></span>
* <span data-ttu-id="27234-639">'Resolve-AzError' içinde Azure PowerShell anket URL’si güncelleştirildi [#11507]</span><span class="sxs-lookup"><span data-stu-id="27234-639">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27234-640">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-640">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-641">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-641">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="27234-642">'Set-AzApiManagementGroup' belgeleri GroupId parametresini belirtmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-642">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27234-643">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27234-643">Az.Cdn</span></span>
* <span data-ttu-id="27234-644">ChinaCDN ile ilgili fiyatlandırma SKU’nun görüntüsü düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-644">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-645">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-645">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-646">Kimlik, Şifreleme, UserOwnedStorage desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="27234-646">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-647">Az.Compute</span></span>
* <span data-ttu-id="27234-648">'Set-AzVmssOrchestrationServiceState' cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-648">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="27234-649">-InstanceView ile 'Get-AzVmss', OrchestrationService durumlarını gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="27234-649">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-650">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-650">Az.IotHub</span></span>
* <span data-ttu-id="27234-651">IoT cihaz ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-651">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="27234-652">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="27234-652">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="27234-653">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="27234-653">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="27234-654">IoT Hub’ındaki bir cihazda doğrudan yöntem çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-654">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="27234-655">IoT cihaz modülü ikizi yapılandırmasını yönetme, Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-655">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="27234-656">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="27234-656">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="27234-657">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="27234-657">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="27234-658">Büyük ölçekte IoT otomatik cihaz yönetimi yapılandırmasını yönetin.</span><span class="sxs-lookup"><span data-stu-id="27234-658">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="27234-659">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-659">New cmdlets are:</span></span>
    - <span data-ttu-id="27234-660">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-660">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="27234-661">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-661">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="27234-662">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-662">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="27234-663">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="27234-663">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="27234-664">Bir IoT Hub’ında kenar modülü yöntemini çağırmak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-664">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-665">Az.KeyVault</span></span>
* <span data-ttu-id="27234-666">Bir kasada geçici silme ve temizleme korumasını etkinleştirebilen yeni bir 'Update-AzKeyVault' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-666">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="27234-667">Microsoft.PowerShell.SecretManagement desteği eklendi [#11178]</span><span class="sxs-lookup"><span data-stu-id="27234-667">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="27234-668">'Remove-AzKeyVaultManagedStorageSasDefinition' örneklerindeki hata düzeltildi [#11479]</span><span class="sxs-lookup"><span data-stu-id="27234-668">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="27234-669">Özel uç noktaya destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-669">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="27234-670">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="27234-670">Az.Maintenance</span></span>
* <span data-ttu-id="27234-671">GA için Bakım cmdlet’lerinin yayın sürümü yayımlanıyor</span><span class="sxs-lookup"><span data-stu-id="27234-671">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-672">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-672">Az.Monitor</span></span>
* <span data-ttu-id="27234-673">Özel bağlantı kapsamı için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-673">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="27234-674">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="27234-674">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27234-675">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="27234-675">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27234-676">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="27234-676">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27234-677">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="27234-677">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="27234-678">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="27234-678">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="27234-679">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="27234-679">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="27234-680">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="27234-680">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-681">Az.Network</span></span>
* <span data-ttu-id="27234-682">Sanal Ağ Geçidi için özel IP’de bağlantıyı etkinleştirmek üzere cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-682">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="27234-683">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="27234-683">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="27234-684">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="27234-684">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="27234-685">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="27234-685">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="27234-686">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="27234-686">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="27234-687">FQDN tabanlı LocalNetworkGateways ve VpnSites’ı etkinleştirmek için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-687">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="27234-688">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="27234-688">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="27234-689">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="27234-689">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="27234-690">ExpressRouteCircuitConnectionConfig (Global Reach) içinde IPv6 adres ailesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-690">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="27234-691">'Set-AzExpressRouteCircuitConnectionConfig' eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-691">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="27234-692">IPv6CircuitConnectionProperties dahil tüm mevcut özelliklerin ayarlanmasına olanak sağlar</span><span class="sxs-lookup"><span data-stu-id="27234-692">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="27234-693">'Add-AzExpressRouteCircuitConnectionConfig' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-693">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="27234-694">Adres ön ekinin adres ailesini belirtmek için başka bir isteğe bağlı AddressPrefixType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-694">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="27234-695">Sanal Ağ Geçidi Bağlantılarında DPD Zaman Aşımı ayarlanmasını sağlamak için cmdlet’ler güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-695">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="27234-696">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="27234-696">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="27234-697">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="27234-697">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27234-698">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27234-698">Az.PolicyInsights</span></span>
* <span data-ttu-id="27234-699">İlke uyumluluğu taramalarını tetiklemek için 'Start-AzPolicyComplianceScan' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-699">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="27234-700">'Get-AzPolicyState' çıkışına ilke tanımı, küme tanımı ve atama sürümleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-700">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27234-701">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-701">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-702">'New-AzServiceFabricCluster' örneklerinin kod biçimlendirmesi ve kullanılabilirliği iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-702">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-703">Az.Sql</span></span>
* <span data-ttu-id="27234-704">'Get-AzSqlInstanceOperation' ve 'Stop-AzSqlInstanceOperation' cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-704">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="27234-705">Sanal ağdaki bir depolama hesabının denetlenmesine yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-705">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-706">Az.Storage</span></span>
* <span data-ttu-id="27234-707">Sonraki sürümlerde Azure Dosya cmdlet’leri için hataya neden olan değişiklik bildirimi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-707">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="27234-708">Depolama hesabı oluşturma/güncelleştirme sırasında yeni SkuName StandardGZRS, StandardRAGZRS desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-708">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="27234-709">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27234-709">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="27234-710">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="27234-710">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="27234-711">DataLake Gen2 desteklendi</span><span class="sxs-lookup"><span data-stu-id="27234-711">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="27234-712">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27234-712">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27234-713">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27234-713">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27234-714">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="27234-714">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="27234-715">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27234-715">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27234-716">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="27234-716">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="27234-717">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27234-717">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="27234-718">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="27234-718">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="27234-719">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="27234-719">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="27234-720">0.10.0-preview - Nisan 2020</span><span class="sxs-lookup"><span data-stu-id="27234-720">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="27234-721">Genel</span><span class="sxs-lookup"><span data-stu-id="27234-721">General</span></span>
* <span data-ttu-id="27234-722">Az modülleri artık Azure Stack Hub’da önizlemede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="27234-722">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="27234-723">Bu, Linux ve macOs ile platformlar arası uyumluluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="27234-723">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="27234-724">Azure Stack Hub artık Az modülleriyle PowerShell Core’u destekliyor, daha fazla bilgiyi [burada](https://aka.ms/az4AzureStack) bulabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="27234-724">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="27234-725">Az modülleri profil 2019-03-01-hybrid’i destekliyor:</span><span class="sxs-lookup"><span data-stu-id="27234-725">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="27234-726">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="27234-726">Az.Billing</span></span>
  - <span data-ttu-id="27234-727">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-727">Az.Compute</span></span>
  - <span data-ttu-id="27234-728">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="27234-728">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="27234-729">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27234-729">Az.EventHub</span></span>
  - <span data-ttu-id="27234-730">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-730">Az.IotHub</span></span>
  - <span data-ttu-id="27234-731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-731">Az.KeyVault</span></span>
  - <span data-ttu-id="27234-732">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-732">Az.Monitor</span></span>
  - <span data-ttu-id="27234-733">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-733">Az.Network</span></span>
  - <span data-ttu-id="27234-734">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-734">Az.Resources</span></span>
  - <span data-ttu-id="27234-735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-735">Az.Storage</span></span>
  - <span data-ttu-id="27234-736">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-736">Az.Websites</span></span>
* <span data-ttu-id="27234-737">Az için Azure Stack Hub ile çalışan üç yeni PowerShell modülü (Az.Databox, Az.IotHub ve Az.EventHub) kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-737">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="27234-738">Komutlar, AzureRM’nin Az olarak değiştirilmesi gibi küçük değişiklikler ile görece aynı kalır</span><span class="sxs-lookup"><span data-stu-id="27234-738">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="27234-739">Azure Stack Hub için PowerShell belgelerine güncelleştirilmiş bağlantı [burada](https://aka.ms/InstallASHPowerShell) bulunabilir</span><span class="sxs-lookup"><span data-stu-id="27234-739">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="27234-740">3.7.0 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="27234-740">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-741">Az.Accounts</span></span>
* <span data-ttu-id="27234-742">Oturum açılmadığında ‘Get-AzTenant’/’Get-AzDefault’/’Set-AzDefault’ cmdlet’lerinin NullReferenceException hatası oluşturması düzeltildi [#10292]</span><span class="sxs-lookup"><span data-stu-id="27234-742">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-743">Az.Compute</span></span>
* <span data-ttu-id="27234-744">‘New-AzDiskConfig’ cmdlet’ine şu parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-744">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="27234-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="27234-745">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="27234-746">Şifreleme özelliğinin ‘New-AzGalleryImageVersion’ cmdlet’inin parametrelerini hedeflemesine izin verildi.</span><span class="sxs-lookup"><span data-stu-id="27234-746">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="27234-747">‘Set-AzVmss’ -Reimage ve ‘Invoke-AzVMReimage’ cmdlet’lerine yönelik tempDisk sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-747">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="27234-748">[#11354]</span><span class="sxs-lookup"><span data-stu-id="27234-748">[#11354]</span></span>
* <span data-ttu-id="27234-749">Aşağıdaki cmdlet’lere yeni SAP uzantısına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-749">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="27234-750">‘Set-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="27234-750">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="27234-751">‘Get-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="27234-751">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="27234-752">‘Remove-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="27234-752">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="27234-753">‘Update-AzVMAEMExtension’</span><span class="sxs-lookup"><span data-stu-id="27234-753">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="27234-754">Yardım belgelerinde bulunan örneklerdeki hatalar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-754">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="27234-755">VM PowerState için tam dize değeri tablo biçiminde gösterildi.</span><span class="sxs-lookup"><span data-stu-id="27234-755">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="27234-756">‘New-AzVmssConfig’: SinglePlacementGroup devre dışı bırakıldığında AutomaticRepairs özelliğinin serileştirilmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-756">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="27234-757">[#11257]</span><span class="sxs-lookup"><span data-stu-id="27234-757">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-758">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-758">Az.DataFactory</span></span>
* <span data-ttu-id="27234-759">ADF .NET SDK’sı 4.8.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-759">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="27234-760">Yeniden çalıştırmayı desteklemek için ‘Invoke-AzDataFactoryV2Pipeline’ komutuna isteğe bağlı parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-760">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-761">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-761">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-762">‘Export-AzDataLakeStoreItem’ ve ‘Import-AzDataLakeStoreItem’ için hataya neden olan değişiklik açıklaması eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-762">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="27234-763">‘New-AzDataLakeStoreItem’, ‘Add-AzDAtaLakeStoreItemContent’ ve ‘Get-AzDAtaLakeStoreItemContent’ için Bayt kodlaması seçeneği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-763">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-764">Az.HDInsight</span></span>
* <span data-ttu-id="27234-765">Küme oluştururken TLS sürümünün desteklenen en düşük sürümünün belirtilmesine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-765">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-766">Az.IotHub</span></span>
* <span data-ttu-id="27234-767">Cihaz başına dağıtılmış ayarları yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-767">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="27234-768">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-768">New Cmdlets are:</span></span>
    - <span data-ttu-id="27234-769">‘Get-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="27234-769">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="27234-770">‘Set-AzIotHubDistributedTracing’</span><span class="sxs-lookup"><span data-stu-id="27234-770">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-771">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-771">Az.KeyVault</span></span>
* <span data-ttu-id="27234-772">‘New-AzKeyVault’ cmdlet’ine hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-772">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-773">Az.Monitor</span></span>
* <span data-ttu-id="27234-774">‘New-AzScheduledQueryRuleLogMetricTrigger’ cmdlet’ine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-774">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-775">Az.Network</span></span>
* <span data-ttu-id="27234-776">Kiracılar arası VirtualHubVnetConnections kurulmasına olanak tanımak için cmdlet’ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-776">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="27234-777">‘New-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="27234-777">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27234-778">‘Update-AzVirtualHubVnetConnection’</span><span class="sxs-lookup"><span data-stu-id="27234-778">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="27234-779">‘New-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="27234-779">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="27234-780">‘Update-AzVirtualHub’</span><span class="sxs-lookup"><span data-stu-id="27234-780">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="27234-781">SQL Yönetim SDK’sı bağımlılığı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-781">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27234-782">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27234-782">Az.PolicyInsights</span></span>
* <span data-ttu-id="27234-783">Hata iletileri iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-783">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-784">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-784">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-785">Azure Site Recovery’de, Azure disk tarafından şifrelenmiş Sanal Makinelere yönelik VM özellikleri güncelleştirildi ve yeniden koruma gerçekleştirmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-785">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="27234-786">Azure Site Recovery VmwareToAzure DR izleme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-786">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="27234-787">Başarısız öğeler için ilke güncelleştirmesini yeniden deneme özelliğine yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-787">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="27234-788">Yedekleme ve geri yükleme işlemleri sırasında disk dışlaması ayarını kullanmaya yönelik destek Azure Backup’a eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-788">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="27234-789">AzureFileShare’den birden fazla dosyayı/klasörü geri yüklemeye yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-789">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="27234-790">IaasVM İlkesini güncelleştirilirken kullanıcı tarafından belirtilen Resourcegroup desteğine yönelik destek Azure Backup’a eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-790">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-791">Az.Resources</span></span>
* <span data-ttu-id="27234-792">‘Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType’ komutlarındaki bir hata düzeltildi ve bunların varsayılan apiVersion yerine kaynakların asıl apiVersion’unu kullanması sağlandı [#11267]</span><span class="sxs-lookup"><span data-stu-id="27234-792">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="27234-793">Hata senaryoları için correlationId’yi günlüğe kaydetme özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-793">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="27234-794">‘Get-AzResourceLock’ cmdlet’inde küçük bir belge değişikliği yapıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-794">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="27234-795">Örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-795">Added example.</span></span>
* <span data-ttu-id="27234-796">‘Get-AzADUser’ cmdlet’inin parametre değerinde tek tırnak işaretinin atlanması [#11317]</span><span class="sxs-lookup"><span data-stu-id="27234-796">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="27234-797">Dağıtım Betikleri için yeni cmdlet’ler eklendi (‘Get-AzDeploymentScript’, ‘Get-AzDeploymentScriptLog’, ‘Save-AzDeploymentScriptLog’ ve ‘Remove-AzDeploymentScript’)</span><span class="sxs-lookup"><span data-stu-id="27234-797">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-798">Az.Sql</span></span>
* <span data-ttu-id="27234-799">‘Invoke-AzSqlDatabaseFailover’ cmdlet’ine okunabilir ikincil parametre eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-799">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="27234-800">‘Disable-AzSqlServerActiveDirectoryOnlyAuthentication’ cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-800">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="27234-801">Veritabanındaki sütunlar sınıflandırılırken duyarlılık derecesi kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="27234-801">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="27234-802">Az.Support</span><span class="sxs-lookup"><span data-stu-id="27234-802">Az.Support</span></span>
* <span data-ttu-id="27234-803">‘Az.Support’ modülü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-803">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-804">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-804">Az.Websites</span></span>
* <span data-ttu-id="27234-805">Aşağıdaki yeni cmdlet’leri kullanarak Trafik Yönlendirme Kurallarıyla çalışmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-805">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="27234-806">‘Get-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="27234-806">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="27234-807">‘Update-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="27234-807">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="27234-808">‘Add-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="27234-808">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="27234-809">‘Remove-AzWebAppTrafficRouting’</span><span class="sxs-lookup"><span data-stu-id="27234-809">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="27234-810">3.6.1 - Mart 2020</span><span class="sxs-lookup"><span data-stu-id="27234-810">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-811">Az.Accounts</span></span>
* <span data-ttu-id="27234-812">'Send-Feedback' içinde Azure PowerShell anket sayfasını açma [#11020]</span><span class="sxs-lookup"><span data-stu-id="27234-812">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="27234-813">'Resolve-Error' içinde Azure PowerShell anket URL’sini görüntüleme [#11021]</span><span class="sxs-lookup"><span data-stu-id="27234-813">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="27234-814">UserAgent’ta Az sürümü eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-814">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27234-815">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-815">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-816">DeveloperPortal Uç Noktasında Özel Etki Alanını alma ve yapılandırma desteği eklendi [#11007]</span><span class="sxs-lookup"><span data-stu-id="27234-816">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="27234-817">'Export-AzApiManagementApi' içinde Api Tanımını Json biçiminde indirme desteği eklendi [#9987]</span><span class="sxs-lookup"><span data-stu-id="27234-817">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="27234-818">'Import-AzApiManagementApi' içinde OpenApi 3.0 tanımını Json belgesinden içeri aktarma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-818">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="27234-819">'New-AzApiManagementIdentityProvider' ve 'Set-AzApiManagementIdentityProvider' içinde AAD B2C Sağlayıcısı için 'Oturum Açan Kiracı' yapılandırma desteği eklendi [#9784]</span><span class="sxs-lookup"><span data-stu-id="27234-819">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-820">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-820">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-821">csproj ve psd1 içinde System.Buffers öğesine açık başvuru eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-821">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-822">Az.IotHub</span></span>
* <span data-ttu-id="27234-823">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-823">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="27234-824">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-824">New Cmdlets are:</span></span>
    - <span data-ttu-id="27234-825">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="27234-825">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27234-826">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="27234-826">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27234-827">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="27234-827">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27234-828">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="27234-828">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="27234-829">IoT hub’ındaki hedef IoT cihazında modülleri yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-829">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="27234-830">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-830">New Cmdlets are:</span></span>
    - <span data-ttu-id="27234-831">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="27234-831">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="27234-832">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="27234-832">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="27234-833">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="27234-833">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="27234-834">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="27234-834">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="27234-835">Bir IoT hub’ında hedef IoT cihazının bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-835">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="27234-836">Bir IoT hub’ında hedef IoT cihazındaki modülün bağlantı dizesini almak için cmdlet eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-836">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="27234-837">IoT cihazının üst cihazını almak/ayarlamak için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-837">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="27234-838">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-838">New Cmdlets are:</span></span>
    - <span data-ttu-id="27234-839">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="27234-839">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="27234-840">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="27234-840">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="27234-841">Cihaz üst-alt ilişkisinin yönetilmesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-841">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-842">Az.Monitor</span></span>
* <span data-ttu-id="27234-843">'Get-AzMetricDefinition' için çıkış değeri düzeltildi [#9714]</span><span class="sxs-lookup"><span data-stu-id="27234-843">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-844">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-844">Az.Network</span></span>
* <span data-ttu-id="27234-845">SQL Yönetim SDK’sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-845">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="27234-846">PrivateLinkServiceConnectionState sınıfındaki bir adlandırma farkı sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-846">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="27234-847">ActionsRequired alanı ActionRequired alanına eşleniyor.</span><span class="sxs-lookup"><span data-stu-id="27234-847">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="27234-848">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-848">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-849">Az.Resources</span></span>
* <span data-ttu-id="27234-850">'Get-AzRoleAssignment' içindeki null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-850">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="27234-851">'-Force' ve '-PassThru' anahtarı 'Remove-AzADGroup' içinde isteğe bağlı olarak işaretlendi [#10849]</span><span class="sxs-lookup"><span data-stu-id="27234-851">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="27234-852">'MailNickname' öğesinin 'Remove-AzADGroup' içinde döndürülmemesi sorunu düzeltildi [#11167]</span><span class="sxs-lookup"><span data-stu-id="27234-852">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="27234-853">'Remove-AzADGroup' kanal oluşturma işleminin çalışmaması sorunu düzeltildi [#11171]</span><span class="sxs-lookup"><span data-stu-id="27234-853">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="27234-854">GetAzureRoleAssignmentCommand içinde null başvuru hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-854">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="27234-855">İlke cmdlet’lerinde yaklaşan değişiklikler için hataya neden olan değişiklik öznitelikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-855">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="27234-856">'Get-AzResourceGroup' sunucu tarafında kaynak grubu etiket filtreleme gerçekleştirmek için güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-856">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="27234-857">Tag cmdlet’leri -ResourceId öğesini kabul edecek şekilde genişletildi</span><span class="sxs-lookup"><span data-stu-id="27234-857">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="27234-858">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27234-858">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="27234-859">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27234-859">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="27234-860">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27234-860">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="27234-861">Yeni Tag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-861">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="27234-862">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="27234-862">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="27234-863">SDK 3.3.0 sürümünden ScopedDeployment getirildi</span><span class="sxs-lookup"><span data-stu-id="27234-863">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-864">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-864">Az.Sql</span></span>
* <span data-ttu-id="27234-865">'New-AzSqlServer' ve 'Set-AzSqlServer' için PublicNetworkAccess eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-865">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="27234-866">Yönetilen Veritabanları için Uzun Süreli Saklamalı yedekleme yapılandırması desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-866">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="27234-867">Yönetilen bir veritabanında LTR ilkesini alma/ayarlama</span><span class="sxs-lookup"><span data-stu-id="27234-867">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="27234-868">Yönetilen veritabanı, yönetilen örnek veya konuma göre LTR yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="27234-868">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="27234-869">Bir LTR yedeklemesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="27234-869">Remove an LTR backup</span></span>
    - <span data-ttu-id="27234-870">Yeni yönetilen veritabanı oluşturmak için LTR yedeklemesini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="27234-870">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="27234-871">New-AzSqlServer ve Set-AzSqlServer için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-871">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="27234-872">New-AzSqlInstance ve Set-AzSqlInstance için MinimalTlsVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-872">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="27234-873">Az.Network için SQL SDK sürümü artırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-873">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-874">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-874">Az.Storage</span></span>
* <span data-ttu-id="27234-875">ImmutabilityPolicy içinde AllowProtectedAppendWrite desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-875">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="27234-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="27234-876">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="27234-877">Gelecekteki bir yayın için AzureStorageTable tür değişikliğine yönelik hataya neden olan değişiklik uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-877">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="27234-878">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="27234-878">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="27234-879">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="27234-879">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-880">Az.Websites</span></span>
* <span data-ttu-id="27234-881">'New-AzAppServicePlan' ve 'Set-AzAppServicePlan' için Etiket parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-881">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="27234-882">Özel etki alanı bir web sitesine eklenirken özel durum oluşturulursa cmdlet’i yürütmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="27234-882">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="27234-883">App Service Planıyla aynı kaynak grubunda bulunmayan Uygulama Hizmetleri için işlem gerçekleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-883">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="27234-884">Farklı kaynak gruplarındaki WebApp/İşlev öğesine erişim kısıtlaması uygulandı</span><span class="sxs-lookup"><span data-stu-id="27234-884">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="27234-885">WebAppSlots için özel ana bilgisayar adları ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-885">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="27234-886">3.5.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="27234-886">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27234-887">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="27234-887">Highlights since the last major release</span></span>
* <span data-ttu-id="27234-888">İstemci tarafı telemetri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-888">Updated client side telemetry.</span></span>
* <span data-ttu-id="27234-889">Cihaz yönetimini desteklemek için Az.IotHub cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-889">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="27234-890">Kullanılabilirlik Grubu Dinleyicisi için Az.SqlVirtualMachine cmdlet’leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-890">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-891">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-891">Az.Accounts</span></span>
* <span data-ttu-id="27234-892">İstemci tarafı telemetri verilerine SubscriptionId, TenantId ve yürütme zamanı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-892">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-893">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-893">Az.Automation</span></span>
* <span data-ttu-id="27234-894">'New-AzAutomationSoftwareUpdateConfiguration' için başvuru belgelerinde Örnek 1’deki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-894">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-895">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-895">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-896">SDK 7.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-896">Updated SDK to 7.0</span></span>
* <span data-ttu-id="27234-897">Sunucu yanıtları boş gövde olduğunda alınan hata iletisi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-897">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-898">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-898">Az.Compute</span></span>
* <span data-ttu-id="27234-899">Güncelleştirme sırasında ProximityPlacementGroupId için boş değere izin verildi</span><span class="sxs-lookup"><span data-stu-id="27234-899">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27234-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-900">Az.FrontDoor</span></span>
* <span data-ttu-id="27234-901">WAF’de kullanılabilen yönetilen kural tanımlarını almak için cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-901">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-902">Az.IotHub</span></span>
* <span data-ttu-id="27234-903">Iot Hub’daki cihazları yönetmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-903">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="27234-904">Yeni Cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-904">New Cmdlets are:</span></span>
    - <span data-ttu-id="27234-905">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="27234-905">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27234-906">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="27234-906">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27234-907">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="27234-907">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="27234-908">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="27234-908">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-909">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-909">Az.KeyVault</span></span>
* <span data-ttu-id="27234-910">Add-AzKeyVaultKey.md için yinelenen metin düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-910">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-911">Az.Monitor</span></span>
* <span data-ttu-id="27234-912">Get-AzLog cmdlet’inin açıklaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-912">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="27234-913">'New-AzMetricAlertRuleV2' komutuna ActionGroupId adlı yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-913">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="27234-914">Kullanıcı ActionGroupId(string) veya ActionGroup(ActivityLogAlertActionGroup) sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="27234-914">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-915">Az.Network</span></span>
* <span data-ttu-id="27234-916">'New-AzPrivateLinkService' cmdlet’inin '-EnableProxyProtocol' parametresi için ek bir parametre notu eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-916">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="27234-917">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içindeki FilterData örneği düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-917">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="27234-918">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md ve Start-AzVirtualnetworkGatewayPacketCapture.md içinde tüm iç ve dış paketleri yakalamak için Paket Yakalama örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-918">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="27234-919">Sanal Ağ Güvenlik Duvarları üzerinde Azure Güvenlik Duvarı desteği sağlandı</span><span class="sxs-lookup"><span data-stu-id="27234-919">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="27234-920">Yeni cmdlet eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="27234-920">No new cmdlets are added.</span></span> <span data-ttu-id="27234-921">Sanal ağ güvenlik duvarları üzerinde güvenlik duvarı ilkesi için kısıtlama gevşetiliyor</span><span class="sxs-lookup"><span data-stu-id="27234-921">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-922">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-923">SQL Veritabanları için Dosya olarak geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-923">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-924">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-924">Az.Resources</span></span>
* <span data-ttu-id="27234-925">Şablon dağıtım cmdlet’leri yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="27234-925">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="27234-926">Yönetim grubunda dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="27234-926">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="27234-927">Kiracı kapsamında dağıtımları yönetmek için yeni cmdlet’ler eklendi: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="27234-927">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="27234-928">\*-AzDeployment cmdlet’leri özel olarak abonelik kapsamında çalışmak için yeniden düzenlendi</span><span class="sxs-lookup"><span data-stu-id="27234-928">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="27234-929">\*-AzDeployment cmdlet’leri için \*-AzSubscriptionDeployment diğer adları oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-929">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="27234-930">'AvailableToOtherTenants' parametresi ayarlanmadığında 'Update-AzADApplication' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-930">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="27234-931">AmbiguousParameterSetException özel durumundan kaçınmak için ApplicationObjectWithoutCredentialParameterSet kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-931">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="27234-932">Yardım dosyaları yeniden oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-932">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-933">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-933">Az.Sql</span></span>
* <span data-ttu-id="27234-934">Yönetilen Örneklerde abonelikler arasında zaman noktası geri yüklemesi için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-934">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="27234-935">Mevcut SQL Yönetilen Örnek donanım neslini değiştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-935">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="27234-936">'Update-AzSqlServerVulnerabilityAssessmentSetting' yardım örnekleri düzeltildi: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="27234-936">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="27234-937">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="27234-937">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="27234-938">Kullanılabilirlik Grubu Dinleyicisi için cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-938">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27234-939">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27234-939">Az.StorageSync</span></span>
* <span data-ttu-id="27234-940">'Invoke-AzStorageSyncCompatibilityCheck' içinde desteklenen karakter kümeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-940">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="27234-941">3.4.0 - Şubat 2020</span><span class="sxs-lookup"><span data-stu-id="27234-941">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27234-942">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="27234-942">Highlights since the last major release</span></span>
* <span data-ttu-id="27234-943">Az.CosmosDB ilk sürüm 0.1.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="27234-943">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="27234-944">Az.Network ConnectionMonitor V2 desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-944">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-945">Az.Accounts</span></span>
* <span data-ttu-id="27234-946">AzureRmContext.json kullanılamadığında bağlamı otomatik olarak kaydetmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="27234-946">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="27234-947">Azure PowerShell Common’ın başvurusu 1.3.5-önizleme olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-947">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27234-948">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-948">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-949">**Get-AzApiManagementApiSchema** Bir API ile ilişkili Open-Api Şemasını alma düzeltildi https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="27234-949">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="27234-950">**New-AzApiManagementProduct**\* ve **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="27234-950">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="27234-951">https://github.com/Azure/azure-powershell/issues/10472 öğesine ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-951">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="27234-952">**Set-AzApiManagementApi** ServiceUrl’nin cmdlet kullanılarak nasıl güncelleştirildiğini göstermek için örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-952">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-953">Az.Compute</span></span>
* <span data-ttu-id="27234-954">Get-AzVM -Status VM adı olmadan gerçekleştirildiğinde ağ kapasitesinin azaltılmasını engellemek için VM durumu sayısını 100 ile sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="27234-954">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="27234-955">Update-AzDiskEncryptionSet cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-955">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="27234-956">Aşağıdaki cmdlet’lere EncryptionType ve DiskEncryptionSetId parametreleri eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-956">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="27234-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="27234-957">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="27234-958">Get-AzProximityPlacementGroup cmdlet’ine ColocationStatus parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-958">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-959">Az.DataFactory</span></span>
* <span data-ttu-id="27234-960">ADF .Net SDK sürümü 4.7.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-960">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="27234-961">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="27234-961">Az.DeploymentManager</span></span>
* <span data-ttu-id="27234-962">Kaynaklara yönelik LIST işlemlerini ekler</span><span class="sxs-lookup"><span data-stu-id="27234-962">Adds LIST operations for resources</span></span>
* <span data-ttu-id="27234-963">Durum Denetimi adımlarında işlem gerçekleştirmeye yönelik özellik ekler</span><span class="sxs-lookup"><span data-stu-id="27234-963">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-964">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-964">Az.HDInsight</span></span>
* <span data-ttu-id="27234-965">New-AzHDInsightCluster’ın belge hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-965">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-966">Az.KeyVault</span></span>
* <span data-ttu-id="27234-967">Remove-AzureKeyVault’un New-AzureKeyVault ile tutarlı olmasını sağlamak için VaultName özniteliğine Name diğer adı eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-967">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-968">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-968">Az.Network</span></span>
* <span data-ttu-id="27234-969">Trafik Analizi’nin devre dışı bırakıldığı bir senaryoyu göstermek için Set-AzNetworkWatcherConfigFlowLog.md dosyasına yeni örnek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-969">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="27234-970">Azure Güvenlik Duvarı’na yönetim IP yapılandırması atamaya yönelik destek eklendi. Güvenlik duvarı, yönetim trafiği için ayrılmış alt ağı ve Genel IP’yi kullanacak</span><span class="sxs-lookup"><span data-stu-id="27234-970">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="27234-971">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-971">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="27234-972">Genel IP Adresi nesnesi kabul eden -ManagementPublicIpAdress (zorunlu değil) parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-972">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="27234-973">Güvenlik duvarı nesnesine SetManagementIpConfiguration yöntemi eklendi. Giriş olarak bir alt ağ ve Genel IP adresi gerektirir. Alt ağ adının ‘AzureFirewallManagementSubnet’ olması gerekir</span><span class="sxs-lookup"><span data-stu-id="27234-973">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="27234-974">Get-AzNetworkSecurityGroup örnekleri, ağ arabirimlerinin yerine NSG’lere yönelik örnekleri gösterecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-974">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="27234-975">Kaynak kimliği tamamlayıcısının bir parametreyi tamamlamasını engelleyen New-AzVpnSite komutundaki yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-975">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="27234-976">Application Gateway’de Yeniden Yazma Kuralları Eylem Kümesinde Url Yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-976">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="27234-977">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-977">New cmdlets added:</span></span>
        - <span data-ttu-id="27234-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="27234-978">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="27234-979">Cmdlet’ler isteğe bağlı -UrlConfiguration parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-979">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="27234-980">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="27234-980">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="27234-981">NetworkWatcher ConnectionMonitor sürüm 2 kaynakları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-981">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27234-982">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27234-982">Az.PolicyInsights</span></span>
* <span data-ttu-id="27234-983">Hangi kaynağın düzeltileceği belirlenmeden önce destek değerlendirmesi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="27234-983">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="27234-984">Start-AzPolicyRemediation cmdlet’ine ‘-ResourceDiscoverMode’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-984">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="27234-985">İlke meta verilerine ilişkin kaynakları almak için Get-AzPolicyMetadata cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-985">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="27234-986">API sürümü 2019-10-01 için Get-AzPolicyState ve Get-AzPolicyStateSummary güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-986">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-987">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-987">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-988">Çoğaltılan bir diski kaldırılmasına yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-988">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="27234-989">Azure Backup, Kurtarma Hizmetleri Kasası oluştururken etiket eklemeye yönelik destek ekledi.</span><span class="sxs-lookup"><span data-stu-id="27234-989">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-990">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-990">Az.Resources</span></span>
* <span data-ttu-id="27234-991">Varsayılanı bağlam aboneliği olan \*-AzPolicyAssignment cmdlet’lerinde -Scope isteğe bağlı yapıldı</span><span class="sxs-lookup"><span data-stu-id="27234-991">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="27234-992">Parola ve anahtar kimlik bilgileriyle ADServicePrincipal oluşturma örnekleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-992">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-993">Az.Sql</span></span>
<span data-ttu-id="27234-994">DatabaseName’in yerine PartnerDatabaseName’in olup olmadığını denetlemeye yarayan New-AzSqlDatabaseSecondary cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-994">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-995">Az.Storage</span></span>
* <span data-ttu-id="27234-996">Depolama Hesabı Oluştur’da Tablo/Sıra Şifreleme Anahtarı’nın ayarlanmasına yönelik destek</span><span class="sxs-lookup"><span data-stu-id="27234-996">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="27234-997">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-997">New-AzStorageAccount</span></span>
* <span data-ttu-id="27234-998">StorageException’da ExtendedErrorInformation olmadığında RequestId’nin gösterilmesi</span><span class="sxs-lookup"><span data-stu-id="27234-998">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="27234-999">Start-AzStorageBlobCopy cmdlet’ine ait olan Örnek 6 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-999">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-1000">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-1000">Az.Websites</span></span>
* <span data-ttu-id="27234-1001">Set-AzWebapp ve Set-AzWebappSlot, şu özellikleri destekler: AlwaysOn, MinTls ve FtpsState</span><span class="sxs-lookup"><span data-stu-id="27234-1001">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="27234-1002">Tek Set-AzWebApp Komutunu kullanarak HttpsOnly ayarlanırken aynı anda AppservicePlan değiştirildiğinde HttpsOnly’nin varsayılan değere sıfırlanması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1002">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="27234-1003">3.3.0 - Ocak 2020</span><span class="sxs-lookup"><span data-stu-id="27234-1003">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-1004">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-1004">Az.Accounts</span></span>
* <span data-ttu-id="27234-1005">Add-AzEnvironment ve Set-AzEnvironment, AzureAttestationServiceEndpointResourceId ve AzureAttestationServiceEndpointSuffix parametrelerini kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1005">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27234-1006">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27234-1006">Az.Cdn</span></span>
* <span data-ttu-id="27234-1007">New-AzCdnEndpoint cmdlet’inde hata yanıtı ayrıntılarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="27234-1007">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1008">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1008">Az.Compute</span></span>
* <span data-ttu-id="27234-1009">İşletim sistemi profili bulunmayan, yönetilen OD diskine sahip bir VM için Set-AzVMCustomScriptExtension cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1009">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="27234-1010">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27234-1010">Az.ContainerInstance</span></span>
* <span data-ttu-id="27234-1011">New-AzContainerGroup örneği tarafından kullanılan parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1011">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="27234-1012">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="27234-1012">Az.DataBoxEdge</span></span>
* <span data-ttu-id="27234-1013">'Get-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1013">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27234-1014">Edge Depolama Kapsayıcısını edinme</span><span class="sxs-lookup"><span data-stu-id="27234-1014">Get the Edge Storage Container</span></span>
* <span data-ttu-id="27234-1015">'New-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1015">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27234-1016">Yeni Edge Depolama Kapsayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="27234-1016">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="27234-1017">'Remove-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1017">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27234-1018">Edge Depolama Kapsayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="27234-1018">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="27234-1019">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1019">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="27234-1020">Edge Depolama Kapsayıcısındaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="27234-1020">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="27234-1021">'Get-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1021">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="27234-1022">Edge Depolama Hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="27234-1022">Get the Edge Storage Account</span></span>
* <span data-ttu-id="27234-1023">'New-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1023">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="27234-1024">Yeni Edge Depolama Hesabını oluşturma</span><span class="sxs-lookup"><span data-stu-id="27234-1024">Create new Edge Storage Account</span></span>
* <span data-ttu-id="27234-1025">'Remove-AzDataBoxEdgeStorageAccount' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1025">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="27234-1026">Edge Depolama Hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="27234-1026">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="27234-1027">'Invoke-AzDataBoxEdgeShare' cmdlet’ini çağırma</span><span class="sxs-lookup"><span data-stu-id="27234-1027">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="27234-1028">Paylaşımdaki verileri yenilemek için eylem çağırma</span><span class="sxs-lookup"><span data-stu-id="27234-1028">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="27234-1029">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1029">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="27234-1030">Az databoxedge depolama hesabı kimlik bilgilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="27234-1030">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-1031">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-1031">Az.DataFactory</span></span>
* <span data-ttu-id="27234-1032">Get-AzDataFactoryV2IntegrationRuntime cmdlet’i için AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId ve VersionStatus özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1032">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="27234-1033">ADF .Net SDK sürümü 4.6.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1033">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="27234-1034">Statik genel IP adreslerine sahip Azure-SSIS IR’nin oluşturulmasına olanak tanımak için ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ cmdlet’ine yönelik ‘PublicIPs’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1034">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="27234-1035">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="27234-1035">Az.DevTestLabs</span></span>
* <span data-ttu-id="27234-1036">Get-AzDtlAllowedVMSizesPolicy.md’deki bozuk bağlantı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1036">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27234-1037">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27234-1037">Az.EventHub</span></span>
* <span data-ttu-id="27234-1038">Sorun 10634’e yönelik düzeltme: Eventhubnamespace’i kaldırmaya yönelik null Nesne başvurusu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1038">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-1039">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-1039">Az.HDInsight</span></span>
* <span data-ttu-id="27234-1040">Invoke-AzHDInsightHiveJob.md hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1040">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="27234-1041">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="27234-1041">Az.MachineLearning</span></span>
* <span data-ttu-id="27234-1042">MachineLearningCompute artık kullanılamadığından, aşağıdaki cmdlet’ler kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1042">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="27234-1043">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="27234-1043">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="27234-1044">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="27234-1044">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="27234-1045">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="27234-1045">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="27234-1046">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="27234-1046">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="27234-1047">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="27234-1047">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="27234-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="27234-1048">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="27234-1049">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="27234-1049">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1050">Az.Network</span></span>
* <span data-ttu-id="27234-1051">1\.36-preview olan Microsoft.Azure.Management.Sql bağımlılığı 1.37-preview’a yükseltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1051">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-1053">Azure’dan Azure’a sağlayıcı için müşteri tarafından yönetilen anahtarlar ile bekleyen durumda şifrelenen yönetilen disk VM’lerine yönelik Azure Site Recovery değişim desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1053">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="27234-1054">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1054">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="27234-1055">Disk şifreleme Kümesi Kimliklerini VMware’den Azure’a aktarımlara yönelik koruma sağlayan disk düzeyinde isteğe bağlı giriş olarak girmek için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1055">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="27234-1056">HyperV’den Azure’a disk şifrelemesi ayarlama eşlemesi ile çoğaltma korumalı öğeyi güncelleştirmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1056">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-1057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-1057">Az.Resources</span></span>
* <span data-ttu-id="27234-1058">'Remove-AzTag' yardım belgesindeki bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1058">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1059">Az.Sql</span></span>
* <span data-ttu-id="27234-1060">Güvenlik açığı değerlendirmesi tarafından ayarlanan temel cmdlet işlevi, Azure veritabanına yönelik ana veritabanında çalışacak ve yönetilen örnek sistem veritabanlarında sınırlandırılacak şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1060">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="27234-1061">SQL örneği yük devretme grubu oluşturulurken karşılaşılan bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1061">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="27234-1062">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="27234-1062">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="27234-1063">Yeni geçerli Lisans türü olarak DR eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1063">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-1064">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-1064">Az.Storage</span></span>
* <span data-ttu-id="27234-1065">Sonraki bir sürümde gerçekleşecek DefaultAction değerinin değişikliğine yönelik hataya neden olan değişiklik uyarısı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1065">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="27234-1066">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="27234-1066">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="27234-1067">Get-AzureRMStorageAccount cmdlet’i -IncludeGeoReplicationStats parametresiyle çalıştırarak Depolama hesabının en son eşitleme zamanını almaya yönelik destek</span><span class="sxs-lookup"><span data-stu-id="27234-1067">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="27234-1068">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-1068">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="27234-1069">3.2.0 - Aralık 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1069">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="27234-1070">Genel</span><span class="sxs-lookup"><span data-stu-id="27234-1070">General</span></span>
* <span data-ttu-id="27234-1071">.psd1 içindeki başvurular, tüm modüller için göreli yol kullanılacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1071">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-1072">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-1072">Az.Accounts</span></span>
* <span data-ttu-id="27234-1073">Az 4.0 önizlemesine yönelik istemci tarafı telemetri için doğru UserAgent ayarlandı</span><span class="sxs-lookup"><span data-stu-id="27234-1073">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="27234-1074">Az 4.0 önizlemesinde bağlam null olduğunda kolay hata iletisi görüntüleniyor</span><span class="sxs-lookup"><span data-stu-id="27234-1074">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27234-1075">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27234-1075">Az.Batch</span></span>
* <span data-ttu-id="27234-1076">**New-AzBatchPool** cmdlet’inin 'VirtualMachineConfiguration. ContainerConfiguration' veya 'VirtualMachineConfiguration.DataDisks' öğelerini sunucuya doğru bir şekilde göndermediği [10602](https://github.com/Azure/azure-powershell/issues/10602) numaralı sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1076">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-1077">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-1077">Az.DataFactory</span></span>
* <span data-ttu-id="27234-1078">ADF .Net SDK sürümü 4.5.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1078">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27234-1079">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-1079">Az.FrontDoor</span></span>
* <span data-ttu-id="27234-1080">WAF tarafından yönetilen kuralları dışlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1080">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="27234-1081">Otomatik tamamlamaya SocketAddr eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1081">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27234-1082">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27234-1082">Az.HealthcareApis</span></span>
* <span data-ttu-id="27234-1083">Özel Durum İşleme</span><span class="sxs-lookup"><span data-stu-id="27234-1083">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-1084">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-1084">Az.KeyVault</span></span>
* <span data-ttu-id="27234-1085">Ayarlanmamış olabilecek değere erişirken gerçekleşen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1085">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="27234-1086">Eliptik Eğri Şifrelemesi Sertifika Yönetimi</span><span class="sxs-lookup"><span data-stu-id="27234-1086">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="27234-1087">Sertifika İlkeleri için Eğri belirtme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1087">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-1088">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-1088">Az.Monitor</span></span>
* <span data-ttu-id="27234-1089">Tanılama Ayarları Ekle komutuna isteğe bağlı bağımsız değişken eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1089">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="27234-1090">Mevcut olduğunda, Log Analytics’e aktarmanın sabit bir şemaya (ayrılmış</span><span class="sxs-lookup"><span data-stu-id="27234-1090">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="27234-1091">veri türü olarak da bilinir) yönelik olması gerektiğini belirten bir anahtar bağımsız değişkeni</span><span class="sxs-lookup"><span data-stu-id="27234-1091">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1092">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1092">Az.Network</span></span>
* <span data-ttu-id="27234-1093">AzureFirewall Uygulama, NAT ve Ağ Kuralları içinde IpGroups desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1093">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-1094">Az.Resources</span></span>
* <span data-ttu-id="27234-1095">Şablon parametresi adının yerleşik bir parametre adıyla çakışması durumunda şablon dağıtımının, şablon parametresini okuyamamasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1095">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="27234-1096">İlke cmdlet’leri, ilke kümesi tanımları içinde gruplandırma desteği sunan yeni API sürümü 2019-09-01’i kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1096">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1097">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1097">Az.Sql</span></span>
* <span data-ttu-id="27234-1098">Güvenlik Açığı Değerlendirmesi otomatik etkinleştirmesi, depolamayı StorageV2'de oluşturacak şekilde yükseltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1098">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-1099">Az.Storage</span></span>
* <span data-ttu-id="27234-1100">OAuth kimlik doğrulaması tabanlı Depolama Bağlamı ile Blob/Kapsayıcı Kimliği tabanlı SAS belirteci oluşturma desteği</span><span class="sxs-lookup"><span data-stu-id="27234-1100">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="27234-1101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="27234-1101">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="27234-1102">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="27234-1102">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="27234-1103">Tüm Kimlik SAS belirteçleri iptal edilecek şekilde Depolama Hesabı Kullanıcı Temsilcisi Anahtarlarını iptal etme desteği</span><span class="sxs-lookup"><span data-stu-id="27234-1103">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="27234-1104">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="27234-1104">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="27234-1105">Microsoft.Azure.Management.Storage, yeni API sürümü 2019-06-01 desteklenecek şekilde 14.2.0 sürümüne güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1105">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="27234-1106">Dosya Paylaşımı cmdlet’lerinin Yönetim düzlemindeki 5120’den daha büyük değerler için QuotaGiB (Gibibayt temelinde Paylaşım Kotası) desteği sunuldu ve 'QuotaGiB' parametresine yönelik diğer ad olarak 'Quota' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1106">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="27234-1107">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27234-1107">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="27234-1108">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27234-1108">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="27234-1109">'Quota' parametresine 'QuotaGiB' parametre diğer adı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1109">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="27234-1110">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="27234-1110">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="27234-1111">Set-AzStorageContainerAcl’nin depolanan Erişim İlkesini temizlemesine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1111">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="27234-1112">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="27234-1112">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="27234-1113">3.1.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1113">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27234-1114">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="27234-1114">Highlights since the last major release</span></span>
* <span data-ttu-id="27234-1115">Az.DataBoxEdge 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="27234-1115">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="27234-1116">Az.SqlVirtualMachine 1.0.0 yayımlandı</span><span class="sxs-lookup"><span data-stu-id="27234-1116">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1117">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1117">Az.Compute</span></span>
* <span data-ttu-id="27234-1118">VM Reapply özelliği</span><span class="sxs-lookup"><span data-stu-id="27234-1118">VM Reapply feature</span></span>
    - <span data-ttu-id="27234-1119">Set-AzVM cmdlet’ine Reapply parametresi ekleme</span><span class="sxs-lookup"><span data-stu-id="27234-1119">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="27234-1120">VM Ölçek Kümesi AutomaticRepairs özelliği:</span><span class="sxs-lookup"><span data-stu-id="27234-1120">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="27234-1121">EnableAutomaticRepair, AutomaticRepairGracePeriod ve AutomaticRepairMaxInstanceRepairsPercent parametreleri şu cmdlet’lere eklendi:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="27234-1121">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="27234-1122">New-AzVM için kiracılar arası galeri görüntüsü desteği</span><span class="sxs-lookup"><span data-stu-id="27234-1122">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="27234-1123">New-AzVM, New-AzVMConfig ve New-AzVmss cmdlet’lerindeki Priority parametresinin bağımsız değişken tamamlayıcısına ‘Spot’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1123">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="27234-1124">Add-AzVmssDataDisk cmdlet’ine DiskIOPSReadWrite ve DiskMBpsReadWrite parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1124">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="27234-1125">New-AzGalleryImageVersion cmdlet’inin SourceImageId parametresi isteğe bağlı olacak şekilde değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1125">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="27234-1126">New-AzGalleryImageVersion cmdlet’ine OSDiskImage ve DataDiskImage parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1126">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="27234-1127">New-AzGalleryImageDefinition cmdlet’ine HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1127">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="27234-1128">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet’lerine SkipExtensionsOnOverprovisionedVMs parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1128">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="27234-1129">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="27234-1129">Az.DataBoxEdge</span></span>
* <span data-ttu-id="27234-1130">`Get-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1130">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="27234-1131">Sırayı Al</span><span class="sxs-lookup"><span data-stu-id="27234-1131">Get the Order</span></span>
* <span data-ttu-id="27234-1132">`New-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1132">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="27234-1133">Yeni Sıra oluştur</span><span class="sxs-lookup"><span data-stu-id="27234-1133">Create new Order</span></span>
* <span data-ttu-id="27234-1134">`Remove-AzDataBoxEdgeOrder` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1134">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="27234-1135">Sırayı kaldır</span><span class="sxs-lookup"><span data-stu-id="27234-1135">Remove the Order</span></span>
* <span data-ttu-id="27234-1136">`New-AzDataBoxEdgeShare` cmdlet’inde değiştir</span><span class="sxs-lookup"><span data-stu-id="27234-1136">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="27234-1137">Yerel Paylaşım’ı oluşturur</span><span class="sxs-lookup"><span data-stu-id="27234-1137">Now creates Local Share</span></span>
* <span data-ttu-id="27234-1138">`Set-AzDataBoxEdgeRole` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1138">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="27234-1139">IotRole artık Paylaş ile eşlenebilir</span><span class="sxs-lookup"><span data-stu-id="27234-1139">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="27234-1140">`Invoke-AzDataBoxEdgeDevice` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1140">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="27234-1141">Tarama güncelleştirmesi çağırın, güncelleştirmeyi indirin ve bunları cihaza yükleyin</span><span class="sxs-lookup"><span data-stu-id="27234-1141">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="27234-1142">`Get-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1142">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="27234-1143">Tetikleyicilere ilişkin bilgileri alır</span><span class="sxs-lookup"><span data-stu-id="27234-1143">Gets the information about Triggers</span></span>
* <span data-ttu-id="27234-1144">`New-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1144">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="27234-1145">Yeni Tetikleyiciler oluştur</span><span class="sxs-lookup"><span data-stu-id="27234-1145">Create new Triggers</span></span>
* <span data-ttu-id="27234-1146">`Remove-AzDataBoxEdgeTrigger` cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1146">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="27234-1147">Tetikleyicileri kaldır</span><span class="sxs-lookup"><span data-stu-id="27234-1147">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-1148">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-1148">Az.DataFactory</span></span>
* <span data-ttu-id="27234-1149">ADF .Net SDK sürümü 4.4.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1149">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="27234-1150">Özel kurulum betiği olmadan kurulum yapılandırmalarını ve 3. taraf bileşenleri etkinleştirmek üzere ‘Set-AzureRmDataFactoryV2IntegrationRuntime’ komutu için ‘ExpressCustomSetup’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1150">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-1151">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-1151">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-1152">Get-AzDataLakeStoreDeletedItem ve Restore-AzDataLakeStoreDeletedItem parametrelerinin belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1152">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27234-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27234-1153">Az.EventHub</span></span>
* <span data-ttu-id="27234-1154">#10301 numaralı şu sorun düzeltildi: SAS Belirtecinin tarih biçimi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1154">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27234-1155">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-1155">Az.FrontDoor</span></span>
* <span data-ttu-id="27234-1156">Enable-AzFrontDoorCustomDomainHttps ve New-AzFrontDoorFrontendEndpointObject öğelerine MinimumTlsVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1156">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="27234-1157">New-AzFrontDoorHealthProbeSettingObject öğesine HealthProbeMethod ve EnabledState parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1157">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="27234-1158">BackendPoolsSettings öğesinin Front Door oluşturmasına/güncelleştirmesine geçmesi için BackendPoolsSettings nesnesi oluşturmaya yönelik yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1158">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="27234-1159">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="27234-1159">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1160">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1160">Az.Network</span></span>
* <span data-ttu-id="27234-1161">‘Start-AzVirtualNetworkGatewayConnectionPacketCapture.md’ ve 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData seçeneği örnekleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1161">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="27234-1162">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="27234-1162">Az.PrivateDns</span></span>
* <span data-ttu-id="27234-1163">PrivateDns .Net SDK’sı sürüm 1.0.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1163">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-1164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-1164">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-1165">Koruma etkinleştirilirken disk türünü seçmeye yönelik Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1165">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="27234-1166">Kurtarma planı eylemi düzenlemesine yönelik Azure Site Recovery hata düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="27234-1166">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="27234-1167">Dosya akışı Veritabanlarını kabul etmek için Azure Backup SQL Geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1167">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27234-1168">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27234-1168">Az.RedisCache</span></span>
* <span data-ttu-id="27234-1169">‘New-AzRedisCache’ ve ‘Set-AzRedisCache’ cmdletlerine ‘MinimumTlsVersion’ parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1169">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="27234-1170">‘Get-AzRedisCache’ cmdlet’inin çıkışına ‘MinimumTlsVersion’ eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1170">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="27234-1171">‘Set-AzRedisCache’ ve ‘New-AzRedisCache’ cmdletlerine yönelik ‘-Size’ parametresine doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1171">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-1172">Az.Resources</span></span>
- <span data-ttu-id="27234-1173">İlke cmdletleri, ilke atamasında EnforcementMode özelliğine sahip yeni 2019-06-01 api sürümünü kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1173">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="27234-1174">İlke tanımı oluştur yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1174">Updated create policy definition help example</span></span>
- <span data-ttu-id="27234-1175">Remove-AZADServicePrincipal -ServicePrincipalName’in boş referans adı bulunamadığında boş referans sunması hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1175">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="27234-1176">Kiracının aboneliği olmadığında New-AZADServicePrincipal’ın boş referans sunmasına ilişkin hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1176">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="27234-1177">Kimlik bilgilerini yalnızca ilişkili uygulamaya eklemek için New-AzAdServicePrincipal değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1177">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1178">Az.Sql</span></span>
* <span data-ttu-id="27234-1179">ReadReplicaCount veritabanı için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1179">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="27234-1180">Alan yedekliliği ayarlı olmadığında Set-AzSqlDatabase düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1180">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="27234-1181">3.0.0 - Kasım 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1181">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="27234-1182">Genel</span><span class="sxs-lookup"><span data-stu-id="27234-1182">General</span></span>
* <span data-ttu-id="27234-1183">Az.PrivateDns 1.0.0 yayınlandı</span><span class="sxs-lookup"><span data-stu-id="27234-1183">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-1184">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-1184">Az.Accounts</span></span>
* <span data-ttu-id="27234-1185">'Resolve-Error' diğer adı için bir kullanımdan kaldırma iletisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="27234-1185">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="27234-1186">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="27234-1186">Az.Advisor</span></span>
* <span data-ttu-id="27234-1187">Get-AzAdvisorRecommendation cmdlet'ine yeni 'Operational Excellence' (Operasyonel Mükemmellik) kategorisi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1187">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27234-1188">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27234-1188">Az.Batch</span></span>
* <span data-ttu-id="27234-1189">`BatchAccountContext` içinde `CoreQuota`, `DedicatedCoreQuota` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1189">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="27234-1190">Ayrıca yeni bir `LowPriorityCoreQuota` var.</span><span class="sxs-lookup"><span data-stu-id="27234-1190">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="27234-1191">Bu **Get-AzBatchAccount** cmdlet'ini etkiliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1191">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="27234-1192">**New-AzBatchTask**`-ResourceFile` parametresi şimdi yeni **New-AzBatchResourceFile** cmdlet’i kullanılarak oluşturulabilen bir `PSResourceFile` koleksiyonu alıyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1192">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="27234-1193">`PSResourceFile` nesnelerini oluşturmaya yardımcı olmak için yeni **New-AzBatchResourceFile** cmdlet'i.</span><span class="sxs-lookup"><span data-stu-id="27234-1193">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="27234-1194">Bunlar `-ResourceFile` parametresinde **New-AzBatchTask** cmdlet'ine sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="27234-1194">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="27234-1195">Mevcut `HttpUrl` yolunun yanı sıra iki tür yeni kaynak dosyasını destekliyor:</span><span class="sxs-lookup"><span data-stu-id="27234-1195">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="27234-1196">`AutoStorageContainerName` tabanlı kaynak dosyaları bir otomatik depolama kapsayıcısının tamamını Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1196">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="27234-1197">`StorageContainerUrl` tabanlı kaynak dosyaları URL'de belirtilen kapsayıcıyı Batch düğümüne indiriyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1197">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="27234-1198">**Get-AzBatchApplication** tarafından döndürülen `PSApplication` öğesinin `ApplicationPackages` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1198">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="27234-1199">Uygulamanın içindeki belirli paketler artık **Get-AzBatchApplicationPackage** kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="27234-1199">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="27234-1200">Örneğin: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="27234-1200">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="27234-1201">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, ve **Set-AzBatchApplication** cmdlet'lerinde `ApplicationId` parametresi `ApplicationName` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1201">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="27234-1202">`ApplicationId` artık `ApplicationName` parametresinin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="27234-1202">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="27234-1203">`PSUserAccount` öğesine yeni `PSWindowsUserConfiguration` özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1203">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="27234-1204">`PSApplicationPackage` içinde `Version` öğesi `Name` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1204">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="27234-1205">`PSResourceFile` içinde `BlobSource` öğesi `HttpUrl` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1205">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="27234-1206">`PSVirtualMachineConfiguration` içinden `OSDisk` özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1206">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="27234-1207">**Set-AzBatchPoolOSVersion** kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1207">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="27234-1208">Bu işlem artık desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1208">This operation is no longer supported.</span></span>
* <span data-ttu-id="27234-1209">`PSCloudServiceConfiguration` içinden `TargetOSVersion` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1209">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="27234-1210">`PSCloudServiceConfiguration` içinde `CurrentOSVersion` öğesi `OSVersion` olarak yeniden adlandırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1210">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="27234-1211">`PSPoolUsageMetrics` içinden `DataEgressGiB` ve `DataIngressGiB` kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1211">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="27234-1212">**Get-AzBatchNodeAgentSku** kaldırıldı ve bunun yerini **Get-AzBatchSupportedImage** aldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1212">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="27234-1213">**Get-AzBatchSupportedImage**, **Get-AzBatchNodeAgentSku** ile aynı verileri ama daha kullanımı kolay bir biçimde döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1213">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="27234-1214">Artık yeni doğrulanmamış resimler de döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1214">New non-verified images are also now returned.</span></span> <span data-ttu-id="27234-1215">Her resim için `Capabilities` ve `BatchSupportEndOfLife` hakkında ek bilgiler de ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1215">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="27234-1216">**New-AzBatchPool** cmdlet'inin `MountConfiguration` parametresiyle havuzun her düğümünde uzak dosya sistemlerini bağlama özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1216">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="27234-1217">Artık trafiğin kaynak bağlantı noktası temelinde havuza ağ erişimini engelleyen ağ güvenlik kuralları destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1217">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="27234-1218">Bu destek `PSNetworkSecurityGroupRule` öğesinin `SourcePortRanges` özelliğiyle sağlanıyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1218">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="27234-1219">Kapsayıcıyı çalıştırırken, şimdi Batch görevin kapsayıcı çalışma dizininde veya Batch görevi çalışma dizininde yürütülmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1219">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="27234-1220">Bu, `PSTaskContainerSettings` öğesinin `WorkingDirectory` özelliğiyle denetleniyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1220">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="27234-1221">Yeni `PublicIPs` özelliği aracılığıyla `PSNetworkConfiguration` parametresinde bir genel IP koleksiyonu belirtme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1221">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="27234-1222">Bu sayede Havuzdaki düğümlerin kullanıcı tarafından sağlanan IP listesinden bir IP alması garanti ediliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1222">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="27234-1223">Belirtilmediğinde, `PSSTartTask` üzerindeki `WaitForSuccess` öğesinin varsayılan değeri artık `$True` (daha önce `$False` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="27234-1223">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="27234-1224">Belirtilmediğinde, `PSAutoUserSpecification` üzerindeki `Scope` öğesinin varsayılan değeri artık `Pool` (daha önce Windows'da `Task` ve Linux'ta `Pool` değeriydi).</span><span class="sxs-lookup"><span data-stu-id="27234-1224">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27234-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27234-1225">Az.Cdn</span></span>
* <span data-ttu-id="27234-1226">RulesEngine'e UrlRewriteAction ve CacheKeyQueryStringAction eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1226">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="27234-1227">New-AzDeliveryRuleCondition cmdlet'inde eksik 'Selector' Girişi gibi çeşitli hatalar düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1227">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1228">Az.Compute</span></span>
* <span data-ttu-id="27234-1229">Disk Şifreleme Kümesi özelliği</span><span class="sxs-lookup"><span data-stu-id="27234-1229">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="27234-1230">Yeni cmdlet’ler:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="27234-1230">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="27234-1231">Aşağıdaki cmdlet'lere DiskEncryptionSetId parametresi eklendi:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="27234-1231">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="27234-1232">Aşağıdaki cmdlet'lere DiskEncryptionSetId ve EncryptionType parametreleri eklendi:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1232">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="27234-1233">New-AzVmssIPConfig cmdlet'ine PublicIPAddressVersion parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1233">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="27234-1234">Özel betik uzantısının FileUris öğesi genel ayardan korumalı ayara taşındı</span><span class="sxs-lookup"><span data-stu-id="27234-1234">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="27234-1235">New-AzVmss, New-AzVmssConfig ve Update-AzVmss cmdlet'lerine ScaleInPolicy eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1235">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="27234-1236">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="27234-1236">Breaking changes</span></span>
    - <span data-ttu-id="27234-1237">CreateOption değeri Upload olduğunda New-AzDiskConfig cmdlet'i için DiskSizeGB yerine UploadSizeInBytes parametresi kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="27234-1237">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="27234-1238">GalleryImageVersion nesnesinde PublishingProfile.Source.ManagedImage.Id yerini StorageProfile.Source.Id'ye bıraktı</span><span class="sxs-lookup"><span data-stu-id="27234-1238">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-1239">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-1239">Az.DataFactory</span></span>
* <span data-ttu-id="27234-1240">ADF .Net SDK sürümü 4.3.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1240">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-1241">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-1241">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-1242">ADLS SDK sürümünün güncelleştirilmesi (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) aşağıdaki düzeltmeleri sağlıyor</span><span class="sxs-lookup"><span data-stu-id="27234-1242">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="27234-1243">Geri dönüşüm kutusu veya dizin girdisinin creationtime öğesi seri durumdan çıkarılamadığında özel durum oluşturulmasını önleme.</span><span class="sxs-lookup"><span data-stu-id="27234-1243">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="27234-1244">adlsclient içinde istek başına zaman aşımı ayarını kullanıma sunma</span><span class="sxs-lookup"><span data-stu-id="27234-1244">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="27234-1245">badoffset kurtarması için özgün syncflag değerinin geçirilmesini düzeltme</span><span class="sxs-lookup"><span data-stu-id="27234-1245">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="27234-1246">Yanıt denetlendikten sonra devamlılık belirtecini almak için EnumerateDirectory'yi düzeltme</span><span class="sxs-lookup"><span data-stu-id="27234-1246">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="27234-1247">Birleştirme Hatasını Düzeltme</span><span class="sxs-lookup"><span data-stu-id="27234-1247">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27234-1248">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-1248">Az.FrontDoor</span></span>
* <span data-ttu-id="27234-1249">Modüllerde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1249">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-1250">Az.HDInsight</span></span>
* <span data-ttu-id="27234-1251">ADLSGen1 depolamasıyla kümeyi almak için Get-AzHDInsightCluster cmdlet'ini kullandığında müşterinin 'Geçerli bir Base-64 dizesi değil' hatası almasına yol açan hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1251">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="27234-1252">Müşterinin Azure Data Lake'e erişirken hizmet sorumlusu uygulama kimliğini sağlayabilmesi için üç cmdlet'e (Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig ve New-AzHDInsightCluster) 'ApplicationId' parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1252">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="27234-1253">Microsoft.Azure.Management.HDInsight 2.1.0'dan 5.1.0'a geçirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1253">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="27234-1254">Beş cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="27234-1254">Removed five cmdlets:</span></span>
    - <span data-ttu-id="27234-1255">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="27234-1255">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="27234-1256">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="27234-1256">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="27234-1257">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="27234-1257">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="27234-1258">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27234-1258">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="27234-1259">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27234-1259">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="27234-1260">Üç cmdlet eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-1260">Added three cmdlets:</span></span>
    - <span data-ttu-id="27234-1261">Get-AzHDInsightMonitoring (Get-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="27234-1261">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="27234-1262">Enable-AzHDInsightMonitoring (Enable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="27234-1262">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="27234-1263">Disable-AzHDInsightMonitoring (Disable-AzHDInsightOMS yerine).</span><span class="sxs-lookup"><span data-stu-id="27234-1263">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="27234-1264">Belirli bir konumdan özellik bilgilerinin alınmasını desteklemek için Get-AzHDInsightProperties cmdlet'i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1264">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="27234-1265">Add-AzHDInsightConfigValue cmdlet'inden parametre kümeleri ('Spark1', 'Spark2') kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1265">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="27234-1266">Add-AzHDInsightSecurityProfile cmdlet'inin yardım belgelerine örnekler eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1266">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="27234-1267">Aşağıdaki cmdlet'lerin çıkış türü değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1267">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="27234-1268">Get-AzHDInsightProperties cmdlet'inin CapabilitiesResponse olan çıkış türü AzureHDInsightCapabilities olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1268">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="27234-1269">Remove-AzHDInsightCluster cmdlet'inin ClusterGetResponse olan çıkış türü bool olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1269">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="27234-1270">Set-AzHDInsightGatewaySettings cmdlet'inin HttpConnectivitySettings olan çıkış türü GatewaySettings olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1270">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="27234-1271">Bazı senaryo test çalışmaları eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1271">Added some scenario test cases.</span></span>
* <span data-ttu-id="27234-1272">Bazı diğer adlar kaldırıldı: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="27234-1272">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-1273">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-1273">Az.IotHub</span></span>
* <span data-ttu-id="27234-1274">Hataya neden olan değişiklikler:</span><span class="sxs-lookup"><span data-stu-id="27234-1274">Breaking changes:</span></span>
    - <span data-ttu-id="27234-1275">'Add-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="27234-1275">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27234-1276">'Add-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1276">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="27234-1277">'Get-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="27234-1277">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27234-1278">'Get-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1278">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="27234-1279">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1279">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="27234-1280">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' türündeki 'OperationsMonitoringProperties' özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1280">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="27234-1281">'New-AzIotHubExportDevice' cmdlet'i artık 'New-AzIotHubExportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1281">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="27234-1282">'New-AzIotHubImportDevice' cmdlet'i artık 'New-AzIotHubImportDevices' diğer adını desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1282">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="27234-1283">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'i artık 'EventHubEndpointName' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="27234-1283">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27234-1284">'Remove-AzIotHubEventHubConsumerGroup' cmdlet'inden '__AllParameterSets' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1284">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="27234-1285">'Set-AzIotHub' cmdet'i artık 'OperationsMonitoringProperties' parametresini desteklemiyor ve özgün parametre adı için hiçbir diğer ad bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="27234-1285">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="27234-1286">'Set-AzIotHub' cmdlet'inden 'UpdateOperationsMonitoringProperties' parametre kümesi kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1286">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-1287">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-1287">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-1288">NSG, genel IP ve Azure'dan Azure'a iç yük dengeleyiciler gibi ağ kaynaklarını yapılandırmak için Azure Site Recovery desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1288">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="27234-1289">Azure'a vMWare için yönetilen diske yazmaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1289">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="27234-1290">Azure'a vMWare için NIC azaltmasına yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1290">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="27234-1291">Azure'a Azure için hızlandırılmış ağa yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1291">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="27234-1292">Azure'a Azure için aracı otomatik güncelleştirmesine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1292">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="27234-1293">Azure'a Azure için Standart SSD'ye yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1293">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="27234-1294">Azure'a Azure için Azure Disk Şifrelemesi iki geçişine yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1294">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="27234-1295">Azure'a Azure için yeni eklenen diski korumaya yönelik Azure Site Recovery Desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1295">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="27234-1296">VM için SoftDelete özelliği eklendi ve softdelete için de testler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1296">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-1297">Az.Resources</span></span>
* <span data-ttu-id="27234-1298">Bağımlılık derlemesi Microsoft.Extensions.Caching.Memory 1.1.1'den 2.2'ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1298">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1299">Az.Network</span></span>
* <span data-ttu-id="27234-1300">PrivateEndpointConnection için tüm cmdlet'ler genel hizmet sağlayıcısını destekleyecek şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1300">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="27234-1301">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1301">Updated cmdlet:</span></span>
        - <span data-ttu-id="27234-1302">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1302">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27234-1303">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1303">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27234-1304">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1304">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27234-1305">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1305">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27234-1306">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1306">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="27234-1307">PrivateLinkResource için yeni cmdlet eklendi ve bu da genel hizmet sağlayıcısını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1307">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="27234-1308">Yeni cmdlet:</span><span class="sxs-lookup"><span data-stu-id="27234-1308">New cmdlet:</span></span>
        - <span data-ttu-id="27234-1309">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="27234-1309">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="27234-1310">Proxy Protocol V2 özelliği için yeni alanlar ve parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1310">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="27234-1311">PrivateLinkService'e EnableProxyProtocol özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1311">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="27234-1312">PrivateEndpointConnection'a LinkIdentifier özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1312">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="27234-1313">New-AzPrivateLinkService cmdlet'i yeni isteğe bağlı EnableProxyProtocol parametresi eklenerek güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1313">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="27234-1314">'New-AzApplicationGatewaySku' başvuru belgelerindeki yanlış parametre açıklaması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1314">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="27234-1315">Azure güvenlik duvarı ilkesini desteklemek için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1315">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="27234-1316">VirtualHub'ın RouteTables alt kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1316">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="27234-1317">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-1317">New cmdlets added:</span></span>
        - <span data-ttu-id="27234-1318">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="27234-1318">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="27234-1319">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="27234-1319">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="27234-1320">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="27234-1320">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="27234-1321">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="27234-1321">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="27234-1322">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="27234-1322">Set-AzVirtualHub</span></span>
* <span data-ttu-id="27234-1323">VirtualWan'ın yeni VirtualHub ve VirtualWANType özellikleri Sku'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1323">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="27234-1324">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1324">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27234-1325">New-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1325">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="27234-1326">Update-AzVirtualHub : Sku parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1326">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="27234-1327">New-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1327">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="27234-1328">Update-AzVirtualWan : VirtualWANType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1328">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="27234-1329">HubVnetConnection, VpnConnection ve ExpressRouteConnection için EnableInternetSecurity özelliği desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1329">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="27234-1330">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-1330">New cmdlets added:</span></span>
        - <span data-ttu-id="27234-1331">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1331">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="27234-1332">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1332">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27234-1333">New-AzureRmVirtualHubVnetConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1333">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27234-1334">New-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1334">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27234-1335">Update-AzureRmVpnConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1335">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27234-1336">New-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1336">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="27234-1337">Set-AzureRmExpressRouteConnection : EnableInternetSecurity parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1337">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="27234-1338">TopLevel WebApplicationFirewall İlkesini Yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1338">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="27234-1339">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-1339">New cmdlets added:</span></span>
        - <span data-ttu-id="27234-1340">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="27234-1340">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="27234-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="27234-1341">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="27234-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="27234-1342">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="27234-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="27234-1343">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="27234-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="27234-1344">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="27234-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="27234-1345">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="27234-1346">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1346">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27234-1347">New-AzApplicationGatewayFirewallPolicy : PolicySetting, ManagedRule parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1347">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="27234-1348">CustomRule'da Geo-Match işleci için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1348">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="27234-1349">FirewallCondition'da işlece GeoMatch eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1349">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="27234-1350">perListener ve perSite Güvenlik duvarı ilkesi için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1350">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="27234-1351">Cmdlet'ler isteğe bağlı parametrelerle güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1351">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="27234-1352">New-AzApplicationGatewayHttpListener : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1352">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="27234-1353">New-AzApplicationGatewayPathRuleConfig : FirewallPolicy, FirewallPolicyId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1353">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="27234-1354">'PSBastion' içinde AzureBastionSubnet adlı gerekli alt ağın büyük/küçük harfe duyarlı olması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1354">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="27234-1355">Azure Güvenlik Duvarı için Ağ Kurallarında Hedef FQDN'lere ve NAT Kurallarında Çevrilmiş FQDN'ye yönelik destek</span><span class="sxs-lookup"><span data-stu-id="27234-1355">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="27234-1356">IpGroup'un RouteTables üst düzey kaynağı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1356">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="27234-1357">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-1357">New cmdlets added:</span></span>
        - <span data-ttu-id="27234-1358">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27234-1358">New-AzIpGroup</span></span>
        - <span data-ttu-id="27234-1359">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27234-1359">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="27234-1360">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27234-1360">Get-AzIpGroup</span></span>
        - <span data-ttu-id="27234-1361">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="27234-1361">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27234-1362">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-1362">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-1363">Bu senaryo artık Add-AzVmssSecret cmdlet'inin kapsamına girdiğinden Add-AzServiceFabricApplicationCertificate cmdlet'i kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1363">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1364">Az.Sql</span></span>
* <span data-ttu-id="27234-1365">Yönetilen Örneklerde bırakılan veritabanlarını geri yükleme desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1365">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="27234-1366">Eski denetim cmdlet'leri kodda kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1366">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="27234-1367">Kullanım dışı bırakılan diğer adlar kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="27234-1367">Removed deprecated aliases:</span></span>
* <span data-ttu-id="27234-1368">Get-AzSqlDatabaseIndexRecommendations (bunun yerine Get-AzSqlDatabaseIndexRecommendation kullanın)</span><span class="sxs-lookup"><span data-stu-id="27234-1368">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="27234-1369">Get-AzSqlDatabaseRestorePoints (bunun yerine Get-AzSqlDatabaseRestorePoint kullanıldı)</span><span class="sxs-lookup"><span data-stu-id="27234-1369">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="27234-1370">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet'i kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1370">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="27234-1371">Kullanım dışı bırakılan Güvenlik Açığı Değerlendirmesi Ayarları cmdlet'lerinin diğer adları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1371">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="27234-1372">Gelişmiş Tehdit Algılama Ayarları cmdlet'leri kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1372">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="27234-1373">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakma ve etkinleştirme cmdlet'leri eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1373">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-1374">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-1374">Az.Storage</span></span>
* <span data-ttu-id="27234-1375">Depolama hesabı oluşturulur veya güncelleştirilirken Büyük dosya paylaşımını etkinleştirme desteği</span><span class="sxs-lookup"><span data-stu-id="27234-1375">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="27234-1376">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-1376">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="27234-1377">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-1377">Set-AzStorageAccount</span></span>
* <span data-ttu-id="27234-1378">Dosya işleyicisi kapatılırken/alınırken, DeletePending durumundaki nesnesinde hata olmasını önlemek için giriş yolunun Dosya dizini mi yoksa Dosya mı olduğunu denetlemeyi atlayın</span><span class="sxs-lookup"><span data-stu-id="27234-1378">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="27234-1379">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27234-1379">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="27234-1380">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27234-1380">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="27234-1381">2.8.0 - Ekim 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1381">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="27234-1382">Genel</span><span class="sxs-lookup"><span data-stu-id="27234-1382">General</span></span>
* <span data-ttu-id="27234-1383">Az.HealthcareApis 1.0.0 sürümü</span><span class="sxs-lookup"><span data-stu-id="27234-1383">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-1384">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-1384">Az.Accounts</span></span>
* <span data-ttu-id="27234-1385">Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1385">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27234-1386">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-1386">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-1387">**Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1387">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="27234-1388">[https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1388">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-1389">Az.Automation</span></span>
* <span data-ttu-id="27234-1390">Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1390">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27234-1391">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27234-1391">Az.Batch</span></span>
* <span data-ttu-id="27234-1392">Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.</span><span class="sxs-lookup"><span data-stu-id="27234-1392">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1393">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1393">Az.Compute</span></span>
* <span data-ttu-id="27234-1394">New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1394">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="27234-1395">Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1395">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="27234-1396">Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1396">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="27234-1397">Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1397">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-1398">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-1398">Az.DataFactory</span></span>
* <span data-ttu-id="27234-1399">ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="27234-1399">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="27234-1400">ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="27234-1400">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="27234-1401">ADF .Net SDK sürümü 4.2.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1401">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-1402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-1402">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-1403">‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1403">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="27234-1404">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="27234-1404">Az.HealthcareApis</span></span>
* <span data-ttu-id="27234-1405">PowerShell sürümü 1.0.0 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1405">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="27234-1406">SDK sürümü 1.0.2 olarak güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1406">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="27234-1407">Yeni SDK sürümüne başvurmaları için testler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1407">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="27234-1408">İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1408">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-1409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-1409">Az.IotHub</span></span>
* <span data-ttu-id="27234-1410">Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="27234-1410">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="27234-1411">Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor</span><span class="sxs-lookup"><span data-stu-id="27234-1411">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-1412">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-1412">Az.Monitor</span></span>
* <span data-ttu-id="27234-1413">Eylem grupları -ItsmReceiver -VoiceReceiver -ArmRoleReceiver -AzureFunctionReceiver -LogicAppReceiver -AutomationRunbookReceiver -AzureAppPushReceiver için yeni eylem grubu alıcıları eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1413">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="27234-1414">Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="27234-1414">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="27234-1415">Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir</span><span class="sxs-lookup"><span data-stu-id="27234-1415">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="27234-1416">Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1416">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1417">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1417">Az.Network</span></span>
* <span data-ttu-id="27234-1418">Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1418">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="27234-1419">Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1419">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="27234-1420">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-1420">New cmdlets added:</span></span>
        - <span data-ttu-id="27234-1421">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="27234-1421">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="27234-1422">Cmdlet’ler, şu isteğe bağlı parametreler ile güncelleştirildi: -TrafficSelectorPolicies -New-AzureRmVirtualNetworkGatewayConnection -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1422">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="27234-1423">Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1423">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="27234-1424">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1424">Updated cmdlets:</span></span>
        - <span data-ttu-id="27234-1425">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1425">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27234-1426">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1426">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27234-1427">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1427">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="27234-1428">Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1428">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="27234-1429">VirtualNetworkGateways için yeni Nesiller ve SKU’lar</span><span class="sxs-lookup"><span data-stu-id="27234-1429">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="27234-1430">VirtualNetworkGateways için yeni Nesiller sunuldu.</span><span class="sxs-lookup"><span data-stu-id="27234-1430">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="27234-1431">VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.</span><span class="sxs-lookup"><span data-stu-id="27234-1431">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27234-1432">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27234-1432">Az.RedisCache</span></span>
* <span data-ttu-id="27234-1433">‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1433">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1434">Az.Sql</span></span>
* <span data-ttu-id="27234-1435">Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1435">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-1436">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-1436">Az.Storage</span></span>
* <span data-ttu-id="27234-1437">Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1437">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="27234-1438">Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="27234-1438">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="27234-1439">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="27234-1439">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="27234-1440">Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek</span><span class="sxs-lookup"><span data-stu-id="27234-1440">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="27234-1441">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-1441">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27234-1442">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27234-1442">Az.StorageSync</span></span>
* <span data-ttu-id="27234-1443">Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1443">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-1444">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-1444">Az.Websites</span></span>
* <span data-ttu-id="27234-1445">Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor</span><span class="sxs-lookup"><span data-stu-id="27234-1445">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="27234-1446">2.7.0 - Eylül 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1446">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="27234-1447">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-1447">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-1448">'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1448">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="27234-1449">Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1449">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="27234-1450">Bunun yerine 'Set-AzApiManagement' kullanın.</span><span class="sxs-lookup"><span data-stu-id="27234-1450">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-1451">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-1451">Az.Automation</span></span>
* <span data-ttu-id="27234-1452">'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1452">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="27234-1453">Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1453">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="27234-1454">-Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1454">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1455">Az.Compute</span></span>
* <span data-ttu-id="27234-1456">New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1456">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="27234-1457">New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1457">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="27234-1458">Düşük öncelikli sanal makine özelliği eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-1458">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="27234-1459">New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1459">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="27234-1460">New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1460">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="27234-1461">Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1461">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="27234-1462">Get-AzRemoteDesktopFile için null özel durumu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1462">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="27234-1463">Sona göre konum için VHD Seek yöntemi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1463">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="27234-1464">New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1464">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-1465">Az.DataFactory</span></span>
* <span data-ttu-id="27234-1466">ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="27234-1466">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="27234-1467">ADF .Net SDK sürümü 4.1.3’e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1467">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-1468">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-1468">Az.HDInsight</span></span>
* <span data-ttu-id="27234-1469">Son değişiklikler duyurusu</span><span class="sxs-lookup"><span data-stu-id="27234-1469">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-1470">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-1470">Az.IotHub</span></span>
* <span data-ttu-id="27234-1471">Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1471">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="27234-1472">IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1472">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="27234-1473">Yeni cmdlet’ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="27234-1473">New cmdlets are:</span></span>
    - <span data-ttu-id="27234-1474">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="27234-1474">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="27234-1475">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="27234-1475">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="27234-1476">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="27234-1476">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="27234-1477">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="27234-1477">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-1478">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-1478">Az.Monitor</span></span>
* <span data-ttu-id="27234-1479">En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder</span><span class="sxs-lookup"><span data-stu-id="27234-1479">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="27234-1480">Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="27234-1480">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="27234-1481">Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="27234-1481">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="27234-1482">**ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu.</span><span class="sxs-lookup"><span data-stu-id="27234-1482">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="27234-1483">Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1483">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="27234-1484">**EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1484">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="27234-1485">Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="27234-1485">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="27234-1486">**NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="27234-1486">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="27234-1487">**Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1487">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="27234-1488">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="27234-1488">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="27234-1489">**AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1489">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="27234-1490">Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.</span><span class="sxs-lookup"><span data-stu-id="27234-1490">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="27234-1491">Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1491">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="27234-1492">New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur</span><span class="sxs-lookup"><span data-stu-id="27234-1492">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="27234-1493">Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder</span><span class="sxs-lookup"><span data-stu-id="27234-1493">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="27234-1494">Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="27234-1494">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="27234-1495">Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder</span><span class="sxs-lookup"><span data-stu-id="27234-1495">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="27234-1496">'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı</span><span class="sxs-lookup"><span data-stu-id="27234-1496">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="27234-1497">İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1497">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="27234-1498">Yardım dosyaları genel olarak geliştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1498">Overall improved help files</span></span>
* <span data-ttu-id="27234-1499">'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1499">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1500">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1500">Az.Network</span></span>
* <span data-ttu-id="27234-1501">'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1501">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="27234-1502">'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1502">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="27234-1503">'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1503">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="27234-1504">Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1504">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="27234-1505">Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1505">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="27234-1506">Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1506">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="27234-1507">Özel IP özelliği için ağ arabirimine özellikler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1507">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="27234-1508">'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1508">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="27234-1509">'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1509">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="27234-1510">Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1510">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="27234-1511">Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1511">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="27234-1512">Sanal WAN’da çoklu bağlantı desteği</span><span class="sxs-lookup"><span data-stu-id="27234-1512">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="27234-1513">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-1513">New cmdlets</span></span>
        - <span data-ttu-id="27234-1514">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="27234-1514">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="27234-1515">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1515">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="27234-1516">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1516">Updated cmdlet:</span></span>
        - <span data-ttu-id="27234-1517">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="27234-1517">New-VpnSite</span></span>
        - <span data-ttu-id="27234-1518">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="27234-1518">Update-VpnSite</span></span>
        - <span data-ttu-id="27234-1519">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1519">New-VpnConnection</span></span>
        - <span data-ttu-id="27234-1520">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1520">Update-VpnConnection</span></span>
* <span data-ttu-id="27234-1521">Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1521">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-1523">AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1523">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="27234-1524">VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1524">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-1525">Az.Resources</span></span>
* <span data-ttu-id="27234-1526">New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1526">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27234-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-1527">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-1528">'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1528">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="27234-1529">Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:</span><span class="sxs-lookup"><span data-stu-id="27234-1529">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="27234-1530">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="27234-1530">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27234-1531">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="27234-1531">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="27234-1532">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="27234-1532">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="27234-1533">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="27234-1533">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="27234-1534">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="27234-1534">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27234-1535">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="27234-1535">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27234-1536">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="27234-1536">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="27234-1537">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="27234-1537">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="27234-1538">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="27234-1538">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="27234-1539">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="27234-1539">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="27234-1540">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="27234-1540">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="27234-1541">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="27234-1541">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="27234-1542">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="27234-1542">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="27234-1543">Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1543">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="27234-1544">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="27234-1544">Az.SignalR</span></span>
* <span data-ttu-id="27234-1545">Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1545">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1546">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1546">Az.Sql</span></span>
* <span data-ttu-id="27234-1547">'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1547">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="27234-1548">Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1548">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="27234-1549">Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1549">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="27234-1550">Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1550">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="27234-1551">Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1551">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-1552">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-1552">Az.Storage</span></span>
* <span data-ttu-id="27234-1553">'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1553">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="27234-1554">Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1554">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="27234-1555">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27234-1555">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="27234-1556">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27234-1556">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="27234-1557">Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1557">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="27234-1558">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27234-1558">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="27234-1559">Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1559">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="27234-1560">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27234-1560">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="27234-1561">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27234-1561">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="27234-1562">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27234-1562">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="27234-1563">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="27234-1563">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-1564">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-1564">Az.Websites</span></span>
* <span data-ttu-id="27234-1565">Uygulamanın yeni ASP’ye geçirilmesi sırasında webapp Etiketlerinin silinmesine neden olan bir sorun düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="27234-1565">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="27234-1566">Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor</span><span class="sxs-lookup"><span data-stu-id="27234-1566">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="27234-1567">'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1567">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="27234-1568">2.6.0 - Ağustos 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1568">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="27234-1569">Genel</span><span class="sxs-lookup"><span data-stu-id="27234-1569">General</span></span>
* <span data-ttu-id="27234-1570">Çok sayıda modülde çeşitli yazım hataları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1570">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-1571">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-1571">Az.Accounts</span></span>
* <span data-ttu-id="27234-1572">Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)</span><span class="sxs-lookup"><span data-stu-id="27234-1572">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="27234-1573">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27234-1573">Az.Aks</span></span>
* <span data-ttu-id="27234-1574">‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1574">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="27234-1575">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="27234-1575">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27234-1576">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-1576">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-1577">[https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1577">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="27234-1578">ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1578">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="27234-1579">**Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1579">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="27234-1580">**New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="27234-1580">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="27234-1581">'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1581">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27234-1582">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27234-1582">Az.Batch</span></span>
* <span data-ttu-id="27234-1583">Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1583">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27234-1584">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27234-1584">Az.Cdn</span></span>
* <span data-ttu-id="27234-1585">CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1585">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1586">Az.Compute</span></span>
* <span data-ttu-id="27234-1587">New-AzVMConfig cmdlet’ine VmssID eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1587">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="27234-1588">New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1588">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="27234-1589">VM görüntüsü nesnesine HyperVGeneration özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1589">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="27234-1590">Host ve HostGroup özellikleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1590">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="27234-1591">Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="27234-1591">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="27234-1592">New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1592">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="27234-1593">Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1593">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="27234-1594">'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1594">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-1595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-1595">Az.DataFactory</span></span>
* <span data-ttu-id="27234-1596">‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1596">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="27234-1597">ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1597">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="27234-1598">Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1598">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="27234-1599">Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1599">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-1601">Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1601">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27234-1602">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27234-1602">Az.EventHub</span></span>
* <span data-ttu-id="27234-1603">#9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="27234-1603">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="27234-1604">#9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması</span><span class="sxs-lookup"><span data-stu-id="27234-1604">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="27234-1605">Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1605">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="27234-1606">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="27234-1606">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="27234-1607">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="27234-1607">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="27234-1608">‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1608">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-1609">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-1609">Az.Monitor</span></span>
* <span data-ttu-id="27234-1610">Yardım belgelerindeki yanlış parametre adı düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1610">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1611">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1611">Az.Network</span></span>
* <span data-ttu-id="27234-1612">New-AzPrivateLinkServiceIpConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1612">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="27234-1613">Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-1613">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="27234-1614">Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1614">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="27234-1615">SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir</span><span class="sxs-lookup"><span data-stu-id="27234-1615">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="27234-1616">Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="27234-1616">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="27234-1617">Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1617">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="27234-1618">AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1618">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-1619">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-1619">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-1620">'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1620">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="27234-1621">Örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1621">Added example</span></span>
    - <span data-ttu-id="27234-1622">‘-Name’ parametresi için açıklama güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1622">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="27234-1623">New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1623">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="27234-1624">New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1624">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-1625">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-1625">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-1626">'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1626">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-1627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-1627">Az.Resources</span></span>
* <span data-ttu-id="27234-1628">Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1628">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="27234-1629">Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1629">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="27234-1630">'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir</span><span class="sxs-lookup"><span data-stu-id="27234-1630">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="27234-1631">Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1631">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27234-1632">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27234-1632">Az.ServiceBus</span></span>
* <span data-ttu-id="27234-1633">#9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası</span><span class="sxs-lookup"><span data-stu-id="27234-1633">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="27234-1634">#9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması</span><span class="sxs-lookup"><span data-stu-id="27234-1634">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="27234-1635">Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1635">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27234-1636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-1636">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-1637">Düğüm ekleme türü cmdlet hataları düzeltildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1637">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="27234-1638">Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası.</span><span class="sxs-lookup"><span data-stu-id="27234-1638">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="27234-1639">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="27234-1639">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="27234-1640">virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1640">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="27234-1641">Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="27234-1641">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="27234-1642">Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1642">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1643">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1643">Az.Sql</span></span>
* <span data-ttu-id="27234-1644">Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1644">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-1645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-1645">Az.Storage</span></span>
* <span data-ttu-id="27234-1646">Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1646">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="27234-1647">Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek</span><span class="sxs-lookup"><span data-stu-id="27234-1647">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="27234-1648">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27234-1648">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="27234-1649">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27234-1649">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="27234-1650">Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği</span><span class="sxs-lookup"><span data-stu-id="27234-1650">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="27234-1651">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27234-1651">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-1652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-1652">Az.Websites</span></span>
* <span data-ttu-id="27234-1653">Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1653">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="27234-1654">2.5.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1654">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-1655">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-1655">Az.Accounts</span></span>
* <span data-ttu-id="27234-1656">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1656">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="27234-1657">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="27234-1657">Az.ApplicationInsights</span></span>
* <span data-ttu-id="27234-1658">'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1658">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-1659">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-1659">Az.Automation</span></span>
* <span data-ttu-id="27234-1660">Kaynak dizesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1660">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-1661">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-1661">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-1662">NetworkRuleSet desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1662">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1663">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1663">Az.Compute</span></span>
* <span data-ttu-id="27234-1664">VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1664">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="27234-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27234-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="27234-1666">Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1666">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="27234-1667">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="27234-1667">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-1668">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-1668">Az.DataFactory</span></span>
* <span data-ttu-id="27234-1669">ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1669">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="27234-1670">'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1670">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27234-1671">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27234-1671">Az.EventHub</span></span>
* <span data-ttu-id="27234-1672">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="27234-1672">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="27234-1673">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1673">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-1674">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-1674">Az.KeyVault</span></span>
* <span data-ttu-id="27234-1675">Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1675">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27234-1676">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27234-1676">Az.LogicApp</span></span>
* <span data-ttu-id="27234-1677">Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme</span><span class="sxs-lookup"><span data-stu-id="27234-1677">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="27234-1678">Filtreleme için yeni MapType parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1678">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="27234-1679">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="27234-1679">Az.ManagedServices</span></span>
* <span data-ttu-id="27234-1680">API 2019-06-01 sürümü için destek eklendi (GA)</span><span class="sxs-lookup"><span data-stu-id="27234-1680">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1681">Az.Network</span></span>
* <span data-ttu-id="27234-1682">Özel uç nokta ve özel bağlantı hizmeti için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1682">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="27234-1683">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-1683">New cmdlets</span></span>
        - <span data-ttu-id="27234-1684">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27234-1684">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27234-1685">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27234-1685">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27234-1686">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1686">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27234-1687">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1687">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27234-1688">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1688">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27234-1689">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1689">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="27234-1690">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="27234-1690">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="27234-1691">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27234-1691">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="27234-1692">Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı</span><span class="sxs-lookup"><span data-stu-id="27234-1692">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="27234-1693">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1693">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="27234-1694">Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1694">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="27234-1695">Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1695">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="27234-1696">AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1696">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="27234-1697">Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1697">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="27234-1698">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1698">Updated cmdlets</span></span>
        - <span data-ttu-id="27234-1699">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1699">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27234-1700">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1700">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="27234-1701">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1701">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="27234-1702">ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1702">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="27234-1703">LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1703">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="27234-1704">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1704">Updated cmdlet:</span></span>
        - <span data-ttu-id="27234-1705">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1705">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="27234-1706">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1706">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="27234-1707">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1707">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="27234-1708">Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1708">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="27234-1709">New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1709">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="27234-1710">Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="27234-1710">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-1711">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-1711">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-1712">Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1712">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="27234-1713">Özel günlük null normal ifade işleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1713">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-1714">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-1714">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-1715">'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1715">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="27234-1716">'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1716">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="27234-1717">'Get-AzRecoveryServicesVault.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1717">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="27234-1718">'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1718">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="27234-1719">'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1719">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="27234-1720">'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1720">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="27234-1721">'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1721">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="27234-1722">'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1722">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="27234-1723">Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1723">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="27234-1724">'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1724">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-1725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-1725">Az.Resources</span></span>
- <span data-ttu-id="27234-1726">'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1726">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="27234-1727">İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1727">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27234-1728">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27234-1728">Az.ServiceBus</span></span>
* <span data-ttu-id="27234-1729">SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="27234-1729">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="27234-1730">yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1731">Az.Sql</span></span>
* <span data-ttu-id="27234-1732">Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1732">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="27234-1733">E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1733">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="27234-1734">Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1734">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-1735">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-1735">Az.Storage</span></span>
* <span data-ttu-id="27234-1736">'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1736">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27234-1737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27234-1737">Az.StorageSync</span></span>
* <span data-ttu-id="27234-1738">Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1738">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="27234-1739">TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1739">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-1740">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-1740">Az.Websites</span></span>
* <span data-ttu-id="27234-1741">Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1741">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="27234-1742">Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1742">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="27234-1743">New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1743">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="27234-1744">2.4.0 - Temmuz 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1744">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-1745">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-1745">Az.Accounts</span></span>
* <span data-ttu-id="27234-1746">Profil cmdlet’leri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1746">Add support for profile cmdlets</span></span>
* <span data-ttu-id="27234-1747">Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1747">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="27234-1748">Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1748">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="27234-1749">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="27234-1749">Az.Advisor</span></span>
* <span data-ttu-id="27234-1750">Az.Advisor genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-1750">GA release of Az.Advisor</span></span>
* <span data-ttu-id="27234-1751">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="27234-1751">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="27234-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-1753">[https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1753">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="27234-1754">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="27234-1754">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="27234-1755">Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1755">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="27234-1756">Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')</span><span class="sxs-lookup"><span data-stu-id="27234-1756">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="27234-1757">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme</span><span class="sxs-lookup"><span data-stu-id="27234-1757">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="27234-1758">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="27234-1758">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="27234-1759">API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1759">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-1760">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-1760">Az.Automation</span></span>
* <span data-ttu-id="27234-1761">Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1761">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1762">Az.Compute</span></span>
* <span data-ttu-id="27234-1763">New-AzImageConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1763">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-1764">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-1764">Az.DataFactory</span></span>
* <span data-ttu-id="27234-1765">Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1765">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27234-1766">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27234-1766">Az.EventGrid</span></span>
* <span data-ttu-id="27234-1767">‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1767">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-1768">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-1768">Az.IotHub</span></span>
* <span data-ttu-id="27234-1769">Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1769">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1770">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1770">Az.Network</span></span>
* <span data-ttu-id="27234-1771">Genel IP etiketlerine ‘RoutingPreference’ eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1771">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="27234-1772">‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1772">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27234-1773">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27234-1773">Az.PolicyInsights</span></span>
* <span data-ttu-id="27234-1774">Get-AzPolicyState’de boş başvuru sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1774">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="27234-1775">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="27234-1775">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-1776">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-1776">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-1777">Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1777">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-1778">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-1778">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-1779">IaaSVM’ler için get-policy komutu düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="27234-1779">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-1780">Az.Resources</span></span>
    - <span data-ttu-id="27234-1781">Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="27234-1781">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="27234-1782">Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1782">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="27234-1783">Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1783">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="27234-1784">İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1784">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27234-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27234-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="27234-1786">4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1786">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1787">Az.Sql</span></span>
* <span data-ttu-id="27234-1788">Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1788">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="27234-1789">Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-1789">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="27234-1790">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="27234-1790">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="27234-1791">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="27234-1791">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="27234-1792">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="27234-1792">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="27234-1793">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="27234-1793">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="27234-1794">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="27234-1794">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="27234-1795">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="27234-1795">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="27234-1796">Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1796">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-1797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-1797">Az.Storage</span></span>
* <span data-ttu-id="27234-1798">Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1798">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="27234-1799">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="27234-1799">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="27234-1800">Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1800">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="27234-1801">Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="27234-1801">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="27234-1802">Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1802">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="27234-1803">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-1803">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="27234-1804">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-1804">Set-AzStorageAccount</span></span>
* <span data-ttu-id="27234-1805">Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1805">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="27234-1806">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27234-1806">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="27234-1807">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="27234-1807">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="27234-1808">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="27234-1808">Az.StorageSync</span></span>
* <span data-ttu-id="27234-1809">Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur</span><span class="sxs-lookup"><span data-stu-id="27234-1809">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="27234-1810">2.3.2 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1810">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-1811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-1811">Az.Accounts</span></span>
* <span data-ttu-id="27234-1812">İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1812">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="27234-1813">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="27234-1813">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="27234-1814">AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1814">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="27234-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="27234-1815">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="27234-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="27234-1816">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1817">Az.Compute</span></span>
* <span data-ttu-id="27234-1818">New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.</span><span class="sxs-lookup"><span data-stu-id="27234-1818">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="27234-1819">'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1819">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="27234-1820">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="27234-1820">Az.Dns</span></span>
* <span data-ttu-id="27234-1821">'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1821">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27234-1822">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27234-1822">Az.EventGrid</span></span>
* <span data-ttu-id="27234-1823">2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1823">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="27234-1824">Yeni cmdlet’ler:</span><span class="sxs-lookup"><span data-stu-id="27234-1824">New cmdlets:</span></span>
    - <span data-ttu-id="27234-1825">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="27234-1825">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="27234-1826">Yeni bir Azure Event Grid etki alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27234-1826">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="27234-1827">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="27234-1827">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="27234-1828">Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="27234-1828">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="27234-1829">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="27234-1829">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="27234-1830">Bir Azure Event Grid Etki Alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="27234-1830">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="27234-1831">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="27234-1831">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="27234-1832">Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.</span><span class="sxs-lookup"><span data-stu-id="27234-1832">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="27234-1833">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="27234-1833">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="27234-1834">Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="27234-1834">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="27234-1835">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="27234-1835">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="27234-1836">Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27234-1836">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="27234-1837">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="27234-1837">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="27234-1838">Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır</span><span class="sxs-lookup"><span data-stu-id="27234-1838">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="27234-1839">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="27234-1839">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="27234-1840">Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="27234-1840">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="27234-1841">Cmdlet'ler güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1841">Updated cmdlets:</span></span>
    - <span data-ttu-id="27234-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="27234-1842">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="27234-1843">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="27234-1843">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="27234-1844">Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="27234-1844">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="27234-1845">Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.</span><span class="sxs-lookup"><span data-stu-id="27234-1845">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="27234-1846">Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-1846">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="27234-1847">Olay aboneliği bitiş tarihi,</span><span class="sxs-lookup"><span data-stu-id="27234-1847">Event subscription expiration date,</span></span>
            - <span data-ttu-id="27234-1848">Gelişmiş filtreleme parametreleri.</span><span class="sxs-lookup"><span data-stu-id="27234-1848">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="27234-1849">Hedef olarak servicebusqueue için yeni sabit listesi ekler.</span><span class="sxs-lookup"><span data-stu-id="27234-1849">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="27234-1850">-IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir</span><span class="sxs-lookup"><span data-stu-id="27234-1850">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="27234-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="27234-1851">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="27234-1852">Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.</span><span class="sxs-lookup"><span data-stu-id="27234-1852">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="27234-1853">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="27234-1853">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="27234-1854">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="27234-1854">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="27234-1855">Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.</span><span class="sxs-lookup"><span data-stu-id="27234-1855">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27234-1856">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-1856">Az.FrontDoor</span></span>
* <span data-ttu-id="27234-1857">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="27234-1857">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="27234-1858">Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler</span><span class="sxs-lookup"><span data-stu-id="27234-1858">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="27234-1859">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="27234-1859">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="27234-1860">Yeni otomatik tamamlama değerleri ekler</span><span class="sxs-lookup"><span data-stu-id="27234-1860">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1861">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1861">Az.Network</span></span>
* <span data-ttu-id="27234-1862">Sanal Ağ Geçidi Kaynağı için destek ekler</span><span class="sxs-lookup"><span data-stu-id="27234-1862">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="27234-1863">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-1863">New cmdlets</span></span>
        - <span data-ttu-id="27234-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="27234-1864">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="27234-1865">AvailablePrivateEndpointType ekler</span><span class="sxs-lookup"><span data-stu-id="27234-1865">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="27234-1866">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-1866">New cmdlets</span></span>
        - <span data-ttu-id="27234-1867">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="27234-1867">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="27234-1868">PrivatePrivateLinkService ekler</span><span class="sxs-lookup"><span data-stu-id="27234-1868">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="27234-1869">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-1869">New cmdlets</span></span>
        - <span data-ttu-id="27234-1870">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27234-1870">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27234-1871">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27234-1871">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27234-1872">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="27234-1872">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="27234-1873">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="27234-1873">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="27234-1874">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1874">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="27234-1875">PrivateEndpoint ekler</span><span class="sxs-lookup"><span data-stu-id="27234-1875">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="27234-1876">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-1876">New cmdlets</span></span>
        - <span data-ttu-id="27234-1877">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27234-1877">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27234-1878">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27234-1878">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27234-1879">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="27234-1879">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="27234-1880">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="27234-1880">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="27234-1881">Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı</span><span class="sxs-lookup"><span data-stu-id="27234-1881">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="27234-1882">New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1882">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="27234-1883">Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1883">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="27234-1884">ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1884">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="27234-1885">ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1885">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="27234-1886">ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1886">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="27234-1887">AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1887">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="27234-1888">New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1888">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="27234-1889">NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1889">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="27234-1890">Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1890">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="27234-1891">ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1891">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="27234-1892">AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1892">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="27234-1893">Get-AzNetworkServiceTag cmdlet’i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1893">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="27234-1894">Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1894">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="27234-1895">New-AzFirewall cmdlet'i güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-1895">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="27234-1896">Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1896">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="27234-1897">Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1897">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="27234-1898">Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder</span><span class="sxs-lookup"><span data-stu-id="27234-1898">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="27234-1899">Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="27234-1899">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="27234-1900">Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="27234-1900">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="27234-1901">New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1901">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="27234-1902">Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1902">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="27234-1903">Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1903">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-1904">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-1904">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-1905">‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1905">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-1906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-1906">Az.Resources</span></span>
* <span data-ttu-id="27234-1907">Ek Şablon Dışarı Aktarma seçenekleri için destek</span><span class="sxs-lookup"><span data-stu-id="27234-1907">Support for additional Template Export options</span></span>
    - <span data-ttu-id="27234-1908">Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1908">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="27234-1909">Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1909">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="27234-1910">Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1910">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27234-1911">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-1911">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-1912">ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1912">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1913">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1913">Az.Sql</span></span>
* <span data-ttu-id="27234-1914">Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1914">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="27234-1915">Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1915">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="27234-1916">Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-1916">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="27234-1917">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27234-1917">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="27234-1918">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27234-1918">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="27234-1919">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="27234-1919">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="27234-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="27234-1920">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="27234-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="27234-1921">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-1922">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-1922">Az.Storage</span></span>
* <span data-ttu-id="27234-1923">Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek</span><span class="sxs-lookup"><span data-stu-id="27234-1923">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="27234-1924">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-1924">New-AzStorageAccount</span></span>
* <span data-ttu-id="27234-1925">Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1925">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="27234-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="27234-1926">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-1927">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-1927">Az.Websites</span></span>
* <span data-ttu-id="27234-1928">Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir</span><span class="sxs-lookup"><span data-stu-id="27234-1928">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="27234-1929">Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler</span><span class="sxs-lookup"><span data-stu-id="27234-1929">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="27234-1930">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1930">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="27234-1931">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27234-1931">Az.Cdn</span></span>
* <span data-ttu-id="27234-1932">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-1932">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-1933">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-1933">Az.Compute</span></span>
* <span data-ttu-id="27234-1934">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1934">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="27234-1935">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="27234-1935">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27234-1936">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27234-1936">Az.EventHub</span></span>
* <span data-ttu-id="27234-1937">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="27234-1937">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="27234-1938">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="27234-1938">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-1939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-1939">Az.Network</span></span>
* <span data-ttu-id="27234-1940">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1940">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="27234-1941">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1941">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27234-1942">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27234-1942">Az.PolicyInsights</span></span>
* <span data-ttu-id="27234-1943">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1943">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-1944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-1944">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-1945">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1945">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27234-1946">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27234-1946">Az.ServiceBus</span></span>
* <span data-ttu-id="27234-1947">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="27234-1947">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27234-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-1949">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1949">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="27234-1950">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-1950">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-1951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-1951">Az.Sql</span></span>
* <span data-ttu-id="27234-1952">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1952">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="27234-1953">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1953">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="27234-1954">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-1954">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="27234-1955">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="27234-1955">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-1956">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-1956">Az.Websites</span></span>
* <span data-ttu-id="27234-1957">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="27234-1957">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="27234-1958">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="27234-1958">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="27234-1959">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-1959">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-1960">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-1960">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="27234-1961">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="27234-1961">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="27234-1962">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="27234-1962">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="27234-1963">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="27234-1963">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="27234-1964">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27234-1964">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="27234-1965">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="27234-1965">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="27234-1966">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="27234-1966">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="27234-1967">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="27234-1967">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="27234-1968">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-1968">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="27234-1969">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="27234-1969">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="27234-1970">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="27234-1970">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="27234-1971">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="27234-1971">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="27234-1972">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="27234-1972">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="27234-1973">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-1973">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="27234-1974">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="27234-1974">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="27234-1975">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="27234-1975">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="27234-1976">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="27234-1976">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="27234-1977">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="27234-1977">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="27234-1978">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="27234-1978">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="27234-1979">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="27234-1979">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="27234-1980">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="27234-1980">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="27234-1981">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="27234-1981">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="27234-1982">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="27234-1982">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="27234-1983">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1983">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="27234-1984">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1984">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="27234-1985">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-1985">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="27234-1986">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="27234-1986">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="27234-1987">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="27234-1987">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="27234-1988">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-1988">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="27234-1989">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1989">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="27234-1990">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1990">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="27234-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="27234-1991">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="27234-1992">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1992">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="27234-1993">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1993">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="27234-1994">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="27234-1994">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="27234-1995">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="27234-1995">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="27234-1996">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="27234-1996">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="27234-1997">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1997">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="27234-1998">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1998">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="27234-1999">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-1999">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="27234-2000">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="27234-2000">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="27234-2001">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="27234-2001">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="27234-2002">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="27234-2002">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="27234-2003">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="27234-2003">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="27234-2004">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2004">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="27234-2005">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="27234-2005">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="27234-2006">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="27234-2006">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="27234-2007">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="27234-2007">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="27234-2008">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2008">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="27234-2009">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="27234-2009">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="27234-2010">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="27234-2010">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="27234-2011">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="27234-2011">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="27234-2012">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="27234-2012">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="27234-2013">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2013">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="27234-2014">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="27234-2014">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="27234-2015">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="27234-2015">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="27234-2016">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2016">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="27234-2017">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="27234-2017">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="27234-2018">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="27234-2018">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="27234-2019">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2019">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="27234-2020">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2020">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="27234-2021">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="27234-2021">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="27234-2022">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="27234-2022">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="27234-2023">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2023">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="27234-2024">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2024">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="27234-2025">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="27234-2025">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="27234-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="27234-2026">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="27234-2027">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="27234-2027">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="27234-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="27234-2028">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="27234-2029">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="27234-2029">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="27234-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="27234-2030">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="27234-2031">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="27234-2031">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="27234-2032">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="27234-2032">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="27234-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="27234-2033">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="27234-2034">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="27234-2034">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="27234-2035">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="27234-2035">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="27234-2036">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="27234-2036">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-2037">Az.Automation</span></span>
* <span data-ttu-id="27234-2038">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2038">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="27234-2039">[https://github.com/Azure/azure-powershell/issues/7977](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2039">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="27234-2040">[https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2040">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="27234-2041">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2041">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="27234-2042">[https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2042">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="27234-2043">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2043">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="27234-2044">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="27234-2044">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2045">Az.Compute</span></span>
* <span data-ttu-id="27234-2046">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2046">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="27234-2047">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="27234-2047">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-2048">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-2048">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-2049">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2049">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-2050">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-2050">Az.Monitor</span></span>
* <span data-ttu-id="27234-2051">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2051">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2052">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2052">Az.Network</span></span>
* <span data-ttu-id="27234-2053">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2053">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="27234-2054">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="27234-2054">Updated cmdlet:</span></span>
        - <span data-ttu-id="27234-2055">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="27234-2055">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="27234-2056">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2056">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2057">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2057">Az.Resources</span></span>
* <span data-ttu-id="27234-2058">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2058">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2059">Az.Sql</span></span>
* <span data-ttu-id="27234-2060">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="27234-2060">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="27234-2061">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2061">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-2062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-2062">Az.Accounts</span></span>
* <span data-ttu-id="27234-2063">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="27234-2063">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-2064">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-2064">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-2065">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="27234-2065">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="27234-2066">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="27234-2066">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2067">Az.Compute</span></span>
* <span data-ttu-id="27234-2068">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="27234-2068">Proximity placement group feature.</span></span>
    - <span data-ttu-id="27234-2069">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="27234-2069">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="27234-2070">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="27234-2070">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="27234-2071">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2071">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="27234-2072">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="27234-2072">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="27234-2073">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2073">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="27234-2074">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="27234-2074">Breaking changes</span></span>
    - <span data-ttu-id="27234-2075">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2075">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="27234-2076">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2076">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="27234-2077">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="27234-2077">Az.DeploymentManager</span></span>
* <span data-ttu-id="27234-2078">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="27234-2078">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="27234-2079">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="27234-2079">Az.Dns</span></span>
* <span data-ttu-id="27234-2080">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="27234-2080">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="27234-2081">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="27234-2081">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="27234-2082">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="27234-2082">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="27234-2083">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-2083">Az.FrontDoor</span></span>
* <span data-ttu-id="27234-2084">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="27234-2084">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="27234-2085">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="27234-2085">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="27234-2086">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-2086">Az.HDInsight</span></span>
* <span data-ttu-id="27234-2087">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="27234-2087">Removed two cmdlets:</span></span>
    - <span data-ttu-id="27234-2088">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27234-2088">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="27234-2089">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="27234-2089">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="27234-2090">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2090">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="27234-2091">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="27234-2091">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="27234-2092">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="27234-2092">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="27234-2093">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="27234-2093">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-2094">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-2094">Az.Monitor</span></span>
* <span data-ttu-id="27234-2095">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="27234-2095">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="27234-2096">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="27234-2096">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="27234-2097">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="27234-2097">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="27234-2098">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="27234-2098">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="27234-2099">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="27234-2099">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="27234-2100">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="27234-2100">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="27234-2101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="27234-2101">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="27234-2102">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27234-2102">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27234-2103">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27234-2103">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27234-2104">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27234-2104">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27234-2105">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27234-2105">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27234-2106">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="27234-2106">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="27234-2107">SQR API hakkında [daha fazla](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="27234-2107">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="27234-2108">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2108">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2109">Az.Network</span></span>
* <span data-ttu-id="27234-2110">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="27234-2110">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="27234-2111">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-2111">New cmdlets</span></span>
        - <span data-ttu-id="27234-2112">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27234-2112">New-AzNatGateway</span></span>
        - <span data-ttu-id="27234-2113">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27234-2113">Get-AzNatGateway</span></span>
        - <span data-ttu-id="27234-2114">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27234-2114">Set-AzNatGateway</span></span>
        - <span data-ttu-id="27234-2115">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="27234-2115">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="27234-2116">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2116">Updated cmdlets</span></span>
        - <span data-ttu-id="27234-2117">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="27234-2117">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="27234-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="27234-2118">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="27234-2119">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="27234-2119">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="27234-2120">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2120">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="27234-2121">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2121">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27234-2122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27234-2122">Az.PolicyInsights</span></span>
* <span data-ttu-id="27234-2123">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-2123">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="27234-2124">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="27234-2124">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="27234-2125">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="27234-2125">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-2126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-2126">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-2127">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-2127">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="27234-2128">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="27234-2128">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="27234-2129">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="27234-2129">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="27234-2130">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="27234-2130">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="27234-2131">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="27234-2131">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="27234-2132">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="27234-2132">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="27234-2133">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="27234-2133">Az.Relay</span></span>
* <span data-ttu-id="27234-2134">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="27234-2134">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27234-2135">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27234-2135">Az.ServiceBus</span></span>
* <span data-ttu-id="27234-2136">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2136">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-2137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-2137">Az.Storage</span></span>
* <span data-ttu-id="27234-2138">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="27234-2138">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="27234-2139">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="27234-2139">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="27234-2140">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="27234-2140">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="27234-2141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-2141">New-AzStorageAccount</span></span>
* <span data-ttu-id="27234-2142">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="27234-2142">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="27234-2143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-2143">New-AzStorageAccount</span></span>
    - <span data-ttu-id="27234-2144">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-2144">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="27234-2145">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-2145">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-2146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-2146">Az.Websites</span></span>
* <span data-ttu-id="27234-2147">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="27234-2147">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="27234-2148">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="27234-2148">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="27234-2149">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2149">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27234-2150">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="27234-2150">Highlights since the last major release</span></span>
* <span data-ttu-id="27234-2151">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-2151">General availability of `Az` module</span></span>
* <span data-ttu-id="27234-2152">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="27234-2152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="27234-2153">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="27234-2153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="27234-2154">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="27234-2155">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27234-2156">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="27234-2157">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-2157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-2158">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-2158">Az.Accounts</span></span>
* <span data-ttu-id="27234-2159">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2159">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="27234-2160">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27234-2160">Az.Batch</span></span>
* <span data-ttu-id="27234-2161">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27234-2162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27234-2162">Az.Cdn</span></span>
* <span data-ttu-id="27234-2163">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2163">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-2164">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-2164">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-2165">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2165">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2166">Az.Compute</span></span>
* <span data-ttu-id="27234-2167">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2167">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="27234-2168">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2168">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27234-2169">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2169">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-2170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-2170">Az.DataFactory</span></span>
* <span data-ttu-id="27234-2171">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2171">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-2172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-2172">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-2173">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2173">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27234-2174">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27234-2174">Az.EventGrid</span></span>
* <span data-ttu-id="27234-2175">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2175">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27234-2176">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27234-2176">Az.EventHub</span></span>
* <span data-ttu-id="27234-2177">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2177">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="27234-2178">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="27234-2178">Az.HDInsight</span></span>
* <span data-ttu-id="27234-2179">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-2180">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-2180">Az.IotHub</span></span>
* <span data-ttu-id="27234-2181">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2181">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-2182">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-2182">Az.KeyVault</span></span>
* <span data-ttu-id="27234-2183">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2183">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27234-2184">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2184">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="27234-2185">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="27234-2185">Az.MachineLearning</span></span>
* <span data-ttu-id="27234-2186">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2186">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="27234-2187">Az.Media</span><span class="sxs-lookup"><span data-stu-id="27234-2187">Az.Media</span></span>
* <span data-ttu-id="27234-2188">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2188">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-2189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-2189">Az.Monitor</span></span>
  * <span data-ttu-id="27234-2190">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="27234-2190">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="27234-2191">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="27234-2191">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="27234-2192">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="27234-2192">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="27234-2193">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="27234-2193">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="27234-2194">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="27234-2194">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="27234-2195">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="27234-2195">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="27234-2196">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2196">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2197">Az.Network</span></span>
* <span data-ttu-id="27234-2198">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27234-2199">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2199">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="27234-2200">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="27234-2200">Az.NotificationHubs</span></span>
* <span data-ttu-id="27234-2201">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-2202">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-2202">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-2203">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="27234-2204">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="27234-2204">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="27234-2205">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-2206">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-2206">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-2207">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2207">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27234-2208">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="27234-2208">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="27234-2209">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2209">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="27234-2210">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2210">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27234-2211">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27234-2211">Az.RedisCache</span></span>
* <span data-ttu-id="27234-2212">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2212">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2213">Az.Resources</span></span>
* <span data-ttu-id="27234-2214">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2214">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2215">Az.Sql</span></span>
* <span data-ttu-id="27234-2216">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2216">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="27234-2217">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27234-2218">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2218">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="27234-2219">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2219">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="27234-2220">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2220">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="27234-2221">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-2221">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="27234-2222">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2222">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-2223">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-2223">Az.Websites</span></span>
* <span data-ttu-id="27234-2224">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2224">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="27234-2225">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="27234-2226">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2226">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="27234-2227">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27234-2227">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="27234-2228">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2228">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27234-2229">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="27234-2229">Highlights since the last major release</span></span>
* <span data-ttu-id="27234-2230">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-2230">General availability of `Az` module</span></span>
* <span data-ttu-id="27234-2231">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="27234-2231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="27234-2232">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="27234-2232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="27234-2233">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="27234-2234">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27234-2235">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="27234-2236">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-2236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="27234-2237">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-2237">Az.Accounts</span></span>
* <span data-ttu-id="27234-2238">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2238">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27234-2239">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27234-2239">Az.AnalysisServices</span></span>
* <span data-ttu-id="27234-2240">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="27234-2240">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="27234-2241">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="27234-2241">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-2242">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-2242">Az.Automation</span></span>
* <span data-ttu-id="27234-2243">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2243">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="27234-2244">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="27234-2244">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="27234-2245">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="27234-2245">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2246">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2246">Az.Compute</span></span>
* <span data-ttu-id="27234-2247">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2247">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="27234-2248">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2248">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="27234-2249">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27234-2249">Az.ContainerInstance</span></span>
* <span data-ttu-id="27234-2250">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2250">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-2251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-2251">Az.DataFactory</span></span>
* <span data-ttu-id="27234-2252">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2252">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="27234-2253">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2253">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2254">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2254">Az.Resources</span></span>
* <span data-ttu-id="27234-2255">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2255">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="27234-2256">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2256">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="27234-2257">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="27234-2257">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="27234-2258">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="27234-2258">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="27234-2259">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2259">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="27234-2260">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="27234-2260">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2261">Az.Sql</span></span>
* <span data-ttu-id="27234-2262">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-2262">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-2263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-2263">Az.Storage</span></span>
* <span data-ttu-id="27234-2264">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="27234-2264">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="27234-2265">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="27234-2265">New-AzStorageContext</span></span>
* <span data-ttu-id="27234-2266">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="27234-2266">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="27234-2267">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="27234-2267">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="27234-2268">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="27234-2268">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="27234-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27234-2269">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="27234-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27234-2270">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="27234-2271">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="27234-2271">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="27234-2272">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27234-2272">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="27234-2273">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="27234-2273">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="27234-2274">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27234-2274">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="27234-2275">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27234-2275">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="27234-2276">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2276">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="27234-2277">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="27234-2277">Highlights since the last major release</span></span>
* <span data-ttu-id="27234-2278">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-2278">General availability of `Az` module</span></span>
* <span data-ttu-id="27234-2279">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="27234-2279">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="27234-2280">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="27234-2280">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="27234-2281">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2281">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="27234-2282">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2282">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27234-2283">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2283">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="27234-2284">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-2284">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-2285">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-2285">Az.Automation</span></span>
* <span data-ttu-id="27234-2286">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="27234-2286">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="27234-2287">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="27234-2287">Dynamic grouping</span></span>
    * <span data-ttu-id="27234-2288">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="27234-2288">Pre-Post script</span></span>
    * <span data-ttu-id="27234-2289">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="27234-2289">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2290">Az.Compute</span></span>
* <span data-ttu-id="27234-2291">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="27234-2291">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="27234-2292">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2292">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-2293">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-2293">Az.KeyVault</span></span>
* <span data-ttu-id="27234-2294">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2294">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2295">Az.Network</span></span>
* <span data-ttu-id="27234-2296">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2296">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="27234-2297">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2297">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-2298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-2298">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-2299">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2299">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="27234-2300">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2300">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2301">Az.Resources</span></span>
* <span data-ttu-id="27234-2302">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2302">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="27234-2303">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2303">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2304">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2304">Az.Sql</span></span>
* <span data-ttu-id="27234-2305">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2305">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-2306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-2306">Az.Storage</span></span>
* <span data-ttu-id="27234-2307">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="27234-2307">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="27234-2308">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27234-2308">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="27234-2309">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27234-2309">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="27234-2310">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="27234-2310">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="27234-2311">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="27234-2311">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="27234-2312">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="27234-2312">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="27234-2313">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="27234-2313">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-2314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-2314">Az.Websites</span></span>
* <span data-ttu-id="27234-2315">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2315">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="27234-2316">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2316">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-2317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-2317">Az.Accounts</span></span>
* <span data-ttu-id="27234-2318">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2318">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="27234-2319">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2319">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-2320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-2320">Az.Automation</span></span>
* <span data-ttu-id="27234-2321">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2321">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="27234-2322">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2322">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="27234-2323">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="27234-2323">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27234-2324">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27234-2324">Az.Cdn</span></span>
* <span data-ttu-id="27234-2325">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="27234-2325">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2326">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2326">Az.Compute</span></span>
* <span data-ttu-id="27234-2327">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2327">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-2328">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-2328">Az.DataFactory</span></span>
* <span data-ttu-id="27234-2329">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2329">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27234-2330">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27234-2330">Az.LogicApp</span></span>
* <span data-ttu-id="27234-2331">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="27234-2331">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2332">Az.Network</span></span>
* <span data-ttu-id="27234-2333">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2333">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-2334">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-2334">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-2335">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2335">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="27234-2336">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="27234-2336">SDK Update</span></span>
* <span data-ttu-id="27234-2337">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-2337">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="27234-2338">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2338">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2339">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2339">Az.Resources</span></span>
* <span data-ttu-id="27234-2340">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2340">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="27234-2341">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="27234-2341">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="27234-2342">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2342">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="27234-2343">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="27234-2343">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="27234-2344">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2344">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="27234-2345">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="27234-2345">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2346">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2346">Az.Sql</span></span>
* <span data-ttu-id="27234-2347">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-2347">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="27234-2348">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-2348">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-2349">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-2349">Az.Storage</span></span>
* <span data-ttu-id="27234-2350">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="27234-2350">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="27234-2351">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2351">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="27234-2352">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27234-2352">Az.AnalysisServices</span></span>
* <span data-ttu-id="27234-2353">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="27234-2353">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-2354">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-2354">Az.Automation</span></span>
* <span data-ttu-id="27234-2355">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2355">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="27234-2356">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2356">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="27234-2357">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2357">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-2358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-2358">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-2359">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2359">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2360">Az.Compute</span></span>
* <span data-ttu-id="27234-2361">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2361">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="27234-2362">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2362">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="27234-2363">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2363">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="27234-2364">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="27234-2364">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-2365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-2365">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-2366">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2366">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="27234-2367">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="27234-2367">Az.EventHub</span></span>
* <span data-ttu-id="27234-2368">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2368">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-2369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-2369">Az.KeyVault</span></span>
* <span data-ttu-id="27234-2370">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2370">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27234-2371">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27234-2371">Az.LogicApp</span></span>
* <span data-ttu-id="27234-2372">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2372">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="27234-2373">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2373">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="27234-2374">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-2374">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="27234-2375">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="27234-2375">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="27234-2376">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="27234-2376">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="27234-2377">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="27234-2377">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="27234-2378">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="27234-2378">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="27234-2379">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="27234-2379">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="27234-2380">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="27234-2380">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="27234-2381">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="27234-2381">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="27234-2382">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="27234-2382">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="27234-2383">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="27234-2383">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="27234-2384">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2384">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="27234-2385">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-2385">Az.Monitor</span></span>
* <span data-ttu-id="27234-2386">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2386">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2387">Az.Network</span></span>
* <span data-ttu-id="27234-2388">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2388">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="27234-2389">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-2389">Az.OperationalInsights</span></span>
* <span data-ttu-id="27234-2390">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="27234-2390">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="27234-2391">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2391">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="27234-2392">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2392">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2393">Az.Resources</span></span>
* <span data-ttu-id="27234-2394">[https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2394">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="27234-2395">[https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2395">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="27234-2396">[https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2396">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="27234-2397">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2397">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2398">Az.Sql</span></span>
* <span data-ttu-id="27234-2399">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2399">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="27234-2400">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2400">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-2401">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-2401">Az.Websites</span></span>
* <span data-ttu-id="27234-2402">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2402">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="27234-2403">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2403">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-2404">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-2404">Az.Accounts</span></span>
* <span data-ttu-id="27234-2405">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="27234-2405">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27234-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27234-2406">Az.AnalysisServices</span></span>
<span data-ttu-id="27234-2407">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="27234-2407">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2408">Az.Compute</span></span>
* <span data-ttu-id="27234-2409">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2409">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="27234-2410">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2410">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="27234-2411">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2411">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-2412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-2412">Az.RecoveryServices</span></span>
<span data-ttu-id="27234-2413">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="27234-2413">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2414">Az.Resources</span></span>
* <span data-ttu-id="27234-2415">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2415">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="27234-2416">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="27234-2416">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="27234-2417">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2417">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="27234-2418">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="27234-2418">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2419">Az.Sql</span></span>
* <span data-ttu-id="27234-2420">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="27234-2420">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="27234-2421">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2421">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="27234-2422">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2422">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="27234-2423">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2423">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-2424">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-2424">Az.Accounts</span></span>
* <span data-ttu-id="27234-2425">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="27234-2425">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="27234-2426">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="27234-2426">Az.AnalysisServices</span></span>
* <span data-ttu-id="27234-2427">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="27234-2427">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="27234-2428">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-2428">Az.RecoveryServices</span></span>
* <span data-ttu-id="27234-2429">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="27234-2429">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="27234-2430">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2430">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-2431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-2431">Az.Accounts</span></span>
* <span data-ttu-id="27234-2432">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2432">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="27234-2433">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27234-2434">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2434">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="27234-2435">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="27234-2435">Az.Aks</span></span>
* <span data-ttu-id="27234-2436">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2436">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="27234-2437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-2437">Az.Automation</span></span>
* <span data-ttu-id="27234-2438">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2438">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="27234-2439">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2439">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="27234-2440">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="27234-2440">Az.Cdn</span></span>
* <span data-ttu-id="27234-2441">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2441">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2442">Az.Compute</span></span>
* <span data-ttu-id="27234-2443">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2443">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="27234-2444">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2444">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="27234-2445">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2445">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="27234-2446">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27234-2446">Az.ContainerRegistry</span></span>
* <span data-ttu-id="27234-2447">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2447">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="27234-2448">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="27234-2448">Az.DataFactory</span></span>
* <span data-ttu-id="27234-2449">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2449">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-2450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-2450">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-2451">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2451">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="27234-2452">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="27234-2452">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="27234-2453">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2453">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-2454">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-2454">Az.IotHub</span></span>
* <span data-ttu-id="27234-2455">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2455">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="27234-2456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-2456">Az.KeyVault</span></span>
* <span data-ttu-id="27234-2457">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2457">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2458">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2458">Az.Network</span></span>
* <span data-ttu-id="27234-2459">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2459">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2460">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2460">Az.Resources</span></span>
* <span data-ttu-id="27234-2461">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2461">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="27234-2462">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2462">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="27234-2463">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2463">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="27234-2464">Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2464">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="27234-2465">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2465">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="27234-2466">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2466">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="27234-2467">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="27234-2467">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27234-2468">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-2468">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-2469">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="27234-2469">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="27234-2470">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2470">Fix some error messages.</span></span>
* <span data-ttu-id="27234-2471">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2471">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="27234-2472">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2472">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="27234-2473">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="27234-2473">Az.SignalR</span></span>
* <span data-ttu-id="27234-2474">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2474">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2475">Az.Sql</span></span>
* <span data-ttu-id="27234-2476">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2476">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27234-2477">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2477">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="27234-2478">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2478">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="27234-2479">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="27234-2479">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-2480">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-2480">Az.Storage</span></span>
* <span data-ttu-id="27234-2481">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2481">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27234-2482">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-2482">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="27234-2483">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="27234-2483">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="27234-2484">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="27234-2484">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="27234-2485">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="27234-2485">Az.TrafficManager</span></span>
* <span data-ttu-id="27234-2486">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2486">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-2487">Az.Websites</span></span>
* <span data-ttu-id="27234-2488">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2488">Update incorrect online help URLs</span></span>
* <span data-ttu-id="27234-2489">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2489">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="27234-2490">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2490">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="27234-2491">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="27234-2491">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="27234-2492">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-2492">Az.Accounts</span></span>
* <span data-ttu-id="27234-2493">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2493">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2494">Az.Compute</span></span>
* <span data-ttu-id="27234-2495">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="27234-2495">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="27234-2496">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2496">Updated the description of ID in help files</span></span>
* <span data-ttu-id="27234-2497">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="27234-2497">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-2498">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-2498">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-2499">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2499">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="27234-2500">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2500">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="27234-2501">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="27234-2501">Az.EventGrid</span></span>
* <span data-ttu-id="27234-2502">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2502">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="27234-2503">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2503">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="27234-2504">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-2504">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="27234-2505">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="27234-2505">Event Time-To-Live,</span></span>
        - <span data-ttu-id="27234-2506">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="27234-2506">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="27234-2507">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="27234-2507">Dead letter endpoint.</span></span>
    - <span data-ttu-id="27234-2508">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-2508">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="27234-2509">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="27234-2509">Event Time-To-Live,</span></span>
        - <span data-ttu-id="27234-2510">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="27234-2510">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="27234-2511">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="27234-2511">Dead letter endpoint.</span></span>
* <span data-ttu-id="27234-2512">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2512">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="27234-2513">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-2513">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="27234-2514">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="27234-2514">Az.IotHub</span></span>
* <span data-ttu-id="27234-2515">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2515">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="27234-2516">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="27234-2516">Az.LogicApp</span></span>
* <span data-ttu-id="27234-2517">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="27234-2517">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2518">Az.Resources</span></span>
* <span data-ttu-id="27234-2519">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2519">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="27234-2520">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="27234-2520">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="27234-2521">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2521">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="27234-2522">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2522">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="27234-2523">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2523">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="27234-2524">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="27234-2524">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="27234-2525">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="27234-2525">Az.SignalR</span></span>
* <span data-ttu-id="27234-2526">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="27234-2526">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2527">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2527">Az.Sql</span></span>
* <span data-ttu-id="27234-2528">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="27234-2528">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="27234-2529">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-2529">Az.Storage</span></span>
* <span data-ttu-id="27234-2530">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="27234-2530">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="27234-2531">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="27234-2531">New-AzStorageContext</span></span>
* <span data-ttu-id="27234-2532">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2532">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="27234-2533">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="27234-2533">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-2534">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-2534">Az.Websites</span></span>
* <span data-ttu-id="27234-2535">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2535">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="27234-2536">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="27234-2536">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="27234-2537">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="27234-2537">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="27234-2538">Genel</span><span class="sxs-lookup"><span data-stu-id="27234-2538">General</span></span>

- <span data-ttu-id="27234-2539">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-2539">General Availability of Az Module</span></span>
- <span data-ttu-id="27234-2540">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="27234-2540">Online help for each module</span></span>
- <span data-ttu-id="27234-2541">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="27234-2541">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="27234-2542">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2542">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="27234-2543">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="27234-2543">Az.Accounts</span></span>
- <span data-ttu-id="27234-2544">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27234-2544">Changed from Az.Profile</span></span>
- <span data-ttu-id="27234-2545">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2545">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="27234-2546">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-2546">Az.ApiManagement</span></span>
- <span data-ttu-id="27234-2547">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="27234-2547">Fixes for #7002</span></span>
- <span data-ttu-id="27234-2548">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2548">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="27234-2549">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="27234-2549">Az.Batch</span></span>
- <span data-ttu-id="27234-2550">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2550">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="27234-2551">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="27234-2551">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="27234-2552">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="27234-2553">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="27234-2553">Az.Billing</span></span>
- <span data-ttu-id="27234-2554">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2554">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="27234-2555">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="27234-2555">Az.CognitivServices</span></span>
- <span data-ttu-id="27234-2556">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2556">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="27234-2557">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-2557">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="27234-2558">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27234-2558">Az.ContainerInstance</span></span>
- <span data-ttu-id="27234-2559">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2559">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="27234-2560">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="27234-2560">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="27234-2561">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2561">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="27234-2562">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-2562">Az.DataLakeStore</span></span>
- <span data-ttu-id="27234-2563">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2563">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="27234-2564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="27234-2564">Az.Monitor</span></span>
- <span data-ttu-id="27234-2565">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2565">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="27234-2566">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="27234-2566">Az.KeyVault</span></span>
- <span data-ttu-id="27234-2567">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-2567">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="27234-2568">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="27234-2568">Az.MachineLearning</span></span>
- <span data-ttu-id="27234-2569">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2569">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="27234-2570">Az.Media</span><span class="sxs-lookup"><span data-stu-id="27234-2570">Az.Media</span></span>
- <span data-ttu-id="27234-2571">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="27234-2571">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="27234-2572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2572">Az.Network</span></span>
<span data-ttu-id="27234-2573">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2573">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="27234-2574">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="27234-2574">New cmdlets added:</span></span>
        - <span data-ttu-id="27234-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27234-2575">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27234-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27234-2576">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27234-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27234-2577">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27234-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27234-2578">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27234-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="27234-2579">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="27234-2580">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="27234-2580">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="27234-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="27234-2581">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="27234-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="27234-2582">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="27234-2583">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2583">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="27234-2584">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="27234-2584">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="27234-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="27234-2585">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="27234-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="27234-2586">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="27234-2587">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27234-2587">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="27234-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="27234-2588">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="27234-2589">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="27234-2589">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="27234-2590">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2590">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="27234-2591">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="27234-2591">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="27234-2592">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="27234-2592">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="27234-2593">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="27234-2593">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="27234-2594">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2594">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="27234-2595">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2595">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="27234-2596">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="27234-2596">Az.OperationalInsights</span></span>
- <span data-ttu-id="27234-2597">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2597">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="27234-2598">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27234-2598">Az.Profile</span></span>
- <span data-ttu-id="27234-2599">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2599">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="27234-2600">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-2600">Az.RecoveryServices</span></span>
- <span data-ttu-id="27234-2601">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="27234-2602">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2602">Az.Resources</span></span>
- <span data-ttu-id="27234-2603">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="27234-2604">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-2604">Az.ServiceFabric</span></span>
- <span data-ttu-id="27234-2605">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="27234-2605">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="27234-2606">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2606">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="27234-2607">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="27234-2607">Az.SIgnalR</span></span>
- <span data-ttu-id="27234-2608">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="27234-2608">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="27234-2609">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2609">Az.Sql</span></span>
- <span data-ttu-id="27234-2610">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2610">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="27234-2611">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2611">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="27234-2612">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2612">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="27234-2613">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-2613">Az.Storage</span></span>
- <span data-ttu-id="27234-2614">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2614">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="27234-2615">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-2615">Az.Websites</span></span>
- <span data-ttu-id="27234-2616">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="27234-2616">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="27234-2617">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="27234-2617">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="27234-2618">Genel</span><span class="sxs-lookup"><span data-stu-id="27234-2618">General</span></span>

* <span data-ttu-id="27234-2619">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="27234-2619">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="27234-2620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2620">Az.Compute</span></span>

* <span data-ttu-id="27234-2621">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2621">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="27234-2622">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-2622">Az.DataLakeStore</span></span>

* <span data-ttu-id="27234-2623">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2623">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="27234-2624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="27234-2624">Az.FrontDoor</span></span>

* <span data-ttu-id="27234-2625">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2625">Fixed some broken links</span></span>
    - <span data-ttu-id="27234-2626">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2626">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="27234-2627">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2627">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="27234-2628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="27234-2628">Az.RecoveryServices</span></span>

* <span data-ttu-id="27234-2629">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2629">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="27234-2630">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2630">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="27234-2631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2631">Az.Resources</span></span>

* <span data-ttu-id="27234-2632">https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="27234-2632">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="27234-2633">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2633">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="27234-2634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2634">Az.Sql</span></span>

* <span data-ttu-id="27234-2635">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="27234-2635">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="27234-2636">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2636">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="27234-2637">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2637">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="27234-2638">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="27234-2638">Az.Storage</span></span>

* <span data-ttu-id="27234-2639">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2639">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="27234-2640">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2640">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="27234-2641">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="27234-2641">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="27234-2642">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2642">Support Static Website configuration</span></span>
    - <span data-ttu-id="27234-2643">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="27234-2643">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="27234-2644">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="27234-2644">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="27234-2645">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-2645">Az.Websites</span></span>

* <span data-ttu-id="27234-2646">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="27234-2646">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="27234-2647">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2647">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="27234-2648">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="27234-2648">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="27234-2649">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="27234-2649">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="27234-2650">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="27234-2650">Az.ApiManagement</span></span>
* <span data-ttu-id="27234-2651">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="27234-2651">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="27234-2652">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="27234-2652">Az.Automation</span></span>
* <span data-ttu-id="27234-2653">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="27234-2653">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="27234-2654">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2654">Added Update Management cmdlets</span></span>
* <span data-ttu-id="27234-2655">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2655">Added Source Control cmdlets</span></span>
* <span data-ttu-id="27234-2656">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2656">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="27234-2657">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2657">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="27234-2658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2658">Az.Compute</span></span>
* <span data-ttu-id="27234-2659">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2659">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="27234-2660">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="27234-2660">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="27234-2661">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="27234-2661">Az.ContainerInstance</span></span>
* <span data-ttu-id="27234-2662">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="27234-2662">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="27234-2663">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="27234-2663">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="27234-2664">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2664">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="27234-2665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2665">Az.Network</span></span>
* <span data-ttu-id="27234-2666">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2666">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="27234-2667">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2667">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="27234-2668">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2668">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="27234-2669">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2669">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="27234-2670">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="27234-2670">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="27234-2671">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2671">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="27234-2672">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="27234-2672">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="27234-2673">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="27234-2673">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="27234-2674">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2674">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="27234-2675">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="27234-2675">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="27234-2676">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="27234-2676">Az.Relay</span></span>
* <span data-ttu-id="27234-2677">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2677">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="27234-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2678">Az.Resources</span></span>
* <span data-ttu-id="27234-2679">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2679">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="27234-2680">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2680">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="27234-2681">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="27234-2681">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="27234-2682">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-2682">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-2683">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2683">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="27234-2684">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2684">Az.Sql</span></span>
* <span data-ttu-id="27234-2685">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2685">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="27234-2686">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27234-2686">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27234-2687">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27234-2687">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27234-2688">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27234-2688">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27234-2689">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="27234-2689">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="27234-2690">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="27234-2690">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="27234-2691">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="27234-2691">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="27234-2692">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="27234-2692">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="27234-2693">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="27234-2693">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="27234-2694">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2694">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="27234-2695">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2695">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="27234-2696">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2696">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="27234-2697">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="27234-2697">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="27234-2698">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="27234-2698">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="27234-2699">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="27234-2699">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="27234-2700">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="27234-2700">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="27234-2701">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2701">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="27234-2702">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="27234-2702">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="27234-2703">Genel</span><span class="sxs-lookup"><span data-stu-id="27234-2703">General</span></span>
* <span data-ttu-id="27234-2704">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="27234-2704">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="27234-2705">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27234-2705">Az.Profile</span></span>
* <span data-ttu-id="27234-2706">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2706">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="27234-2707">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2707">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="27234-2708">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2708">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="27234-2709">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2709">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="27234-2710">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2710">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="27234-2711">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2711">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="27234-2712">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2712">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-2713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-2713">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-2714">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2714">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2715">Az.Compute</span></span>
* <span data-ttu-id="27234-2716">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2716">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="27234-2717">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="27234-2717">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="27234-2718">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2718">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-2719">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-2719">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-2720">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2720">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="27234-2721">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2721">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="27234-2722">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="27234-2722">Az.Insights</span></span>
* <span data-ttu-id="27234-2723">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2723">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="27234-2724">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="27234-2724">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="27234-2725">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2725">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="27234-2726">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="27234-2726">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2727">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2727">Az.Network</span></span>
* <span data-ttu-id="27234-2728">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="27234-2728">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="27234-2729">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="27234-2729">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="27234-2730">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="27234-2730">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="27234-2731">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="27234-2731">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="27234-2732">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="27234-2732">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="27234-2733">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="27234-2733">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="27234-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="27234-2734">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="27234-2735">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="27234-2735">Az.PolicyInsights</span></span>
* <span data-ttu-id="27234-2736">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2736">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2737">Az.Resources</span></span>
* <span data-ttu-id="27234-2738">https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="27234-2738">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="27234-2739">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="27234-2739">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="27234-2740">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="27234-2740">Az.ServiceBus</span></span>
* <span data-ttu-id="27234-2741">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2741">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="27234-2742">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="27234-2742">Az.ServiceFabric</span></span>
* <span data-ttu-id="27234-2743">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2743">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="27234-2744">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2744">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="27234-2745">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="27234-2745">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="27234-2746">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="27234-2746">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="27234-2747">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2747">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="27234-2748">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="27234-2748">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="27234-2749">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="27234-2749">Az.Profile</span></span>
* <span data-ttu-id="27234-2750">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="27234-2750">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="27234-2751">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="27234-2751">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2752">Az.Compute</span></span>
* <span data-ttu-id="27234-2753">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2753">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="27234-2754">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="27234-2755">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="27234-2755">Az.DataLakeStore</span></span>
* <span data-ttu-id="27234-2756">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="27234-2756">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="27234-2757">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="27234-2757">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="27234-2758">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="27234-2758">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="27234-2759">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="27234-2759">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="27234-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="27234-2760">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2761">Az.Network</span></span>
* <span data-ttu-id="27234-2762">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="27234-2762">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="27234-2763">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2763">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2764">Az.Resources</span></span>
* <span data-ttu-id="27234-2765">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2765">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="27234-2766">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="27234-2766">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="27234-2767">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="27234-2767">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="27234-2768">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="27234-2768">Azure.Storage</span></span>
* <span data-ttu-id="27234-2769">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="27234-2769">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="27234-2770">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="27234-2770">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="27234-2771">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="27234-2771">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="27234-2772">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="27234-2772">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="27234-2773">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="27234-2773">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="27234-2774">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="27234-2774">Az.CognitiveServices</span></span>
* <span data-ttu-id="27234-2775">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="27234-2775">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="27234-2776">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="27234-2776">Az.Compute</span></span>
* <span data-ttu-id="27234-2777">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2777">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="27234-2778">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2778">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="27234-2779">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2779">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="27234-2780">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="27234-2780">Az.DataFactoryV2</span></span>
* <span data-ttu-id="27234-2781">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="27234-2781">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="27234-2782">Az.Network</span><span class="sxs-lookup"><span data-stu-id="27234-2782">Az.Network</span></span>
* <span data-ttu-id="27234-2783">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="27234-2783">Added NetworkProfile functionality.</span></span> <span data-ttu-id="27234-2784">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2784">new cmdlets added</span></span>
    - <span data-ttu-id="27234-2785">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27234-2785">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="27234-2786">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27234-2786">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="27234-2787">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27234-2787">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="27234-2788">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="27234-2788">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="27234-2789">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="27234-2789">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="27234-2790">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="27234-2790">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="27234-2791">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2791">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="27234-2792">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2792">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="27234-2793">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2793">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="27234-2794">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="27234-2794">Az.RedisCache</span></span>
* <span data-ttu-id="27234-2795">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="27234-2795">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="27234-2796">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2796">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="27234-2797">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="27234-2797">Az.Resources</span></span>
* <span data-ttu-id="27234-2798">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="27234-2798">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="27234-2799">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2799">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="27234-2800">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="27234-2800">Az.Sql</span></span>
* <span data-ttu-id="27234-2801">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="27234-2801">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="27234-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="27234-2802">Az.Websites</span></span>
* <span data-ttu-id="27234-2803">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="27234-2803">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="27234-2804">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="27234-2804">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="27234-2805">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="27234-2805">0.2.0 - September 2018</span></span>
 <span data-ttu-id="27234-2806">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="27234-2806">Initial Release</span></span>
