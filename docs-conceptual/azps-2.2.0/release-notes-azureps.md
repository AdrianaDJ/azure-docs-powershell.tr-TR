---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498684"
---
## <a name="220---june-2019"></a><span data-ttu-id="3fddc-101">2.2.0 - Haziran 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-101">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="3fddc-102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3fddc-102">Az.Cdn</span></span>
* <span data-ttu-id="3fddc-103">Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-103">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-104">Az.Compute</span></span>
* <span data-ttu-id="3fddc-105">İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-105">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="3fddc-106">Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3fddc-106">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3fddc-107">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3fddc-107">Az.EventHub</span></span>
* <span data-ttu-id="3fddc-108">#9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3fddc-108">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="3fddc-109">#9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3fddc-109">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-110">Az.Network</span></span>
* <span data-ttu-id="3fddc-111">Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-111">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="3fddc-112">ResourceId ve InputObject için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-112">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3fddc-113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3fddc-113">Az.PolicyInsights</span></span>
* <span data-ttu-id="3fddc-114">Get-AzPolicyEvent’de Boş referans sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-114">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3fddc-115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-115">Az.RecoveryServices</span></span>
* <span data-ttu-id="3fddc-116">IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-116">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3fddc-117">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3fddc-117">Az.ServiceBus</span></span>
* <span data-ttu-id="3fddc-118">#9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3fddc-118">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3fddc-119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3fddc-119">Az.ServiceFabric</span></span>
* <span data-ttu-id="3fddc-120">'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-120">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="3fddc-121">Service Fabric komut satırlarındaki eksik karakter düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-121">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-122">Az.Sql</span></span>
* <span data-ttu-id="3fddc-123">Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-123">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="3fddc-124">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="3fddc-124">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="3fddc-125">Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı</span><span class="sxs-lookup"><span data-stu-id="3fddc-125">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="3fddc-126">New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-126">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3fddc-127">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-127">Az.Websites</span></span>
* <span data-ttu-id="3fddc-128">Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-128">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="3fddc-129">2.1.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-129">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3fddc-130">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3fddc-130">Az.ApiManagement</span></span>
* <span data-ttu-id="3fddc-131">Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3fddc-131">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="3fddc-132">**Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır</span><span class="sxs-lookup"><span data-stu-id="3fddc-132">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="3fddc-133">**New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur</span><span class="sxs-lookup"><span data-stu-id="3fddc-133">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="3fddc-134">**New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="3fddc-134">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="3fddc-135">**New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3fddc-135">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="3fddc-136">**New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur</span><span class="sxs-lookup"><span data-stu-id="3fddc-136">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="3fddc-137">**Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır</span><span class="sxs-lookup"><span data-stu-id="3fddc-137">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="3fddc-138">**Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3fddc-138">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="3fddc-139">ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3fddc-139">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="3fddc-140">**Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="3fddc-140">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="3fddc-141">**New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur</span><span class="sxs-lookup"><span data-stu-id="3fddc-141">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="3fddc-142">**Remove-AzApiManagementCache** - Önbelleği kaldırır</span><span class="sxs-lookup"><span data-stu-id="3fddc-142">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="3fddc-143">**Update-AzApiManagementCache** - Önbelleği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3fddc-143">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="3fddc-144">API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3fddc-144">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="3fddc-145">**New-AzApiManagementSchema** - API için yeni Şema oluşturur</span><span class="sxs-lookup"><span data-stu-id="3fddc-145">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="3fddc-146">**Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır</span><span class="sxs-lookup"><span data-stu-id="3fddc-146">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="3fddc-147">**Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır</span><span class="sxs-lookup"><span data-stu-id="3fddc-147">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="3fddc-148">**Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3fddc-148">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="3fddc-149">Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="3fddc-149">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="3fddc-150">**New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./</span><span class="sxs-lookup"><span data-stu-id="3fddc-150">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="3fddc-151">Ağ Durumunu almak için yeni cmdlet oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="3fddc-151">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="3fddc-152">**Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="3fddc-152">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="3fddc-153">ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="3fddc-153">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="3fddc-154">**New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-154">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="3fddc-155">Yeni 'Consumption' SKU'su için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-155">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="3fddc-156">'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-156">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="3fddc-157">Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3fddc-157">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="3fddc-158">Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3fddc-158">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="3fddc-159">ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-159">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="3fddc-160">**Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-160">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="3fddc-161">Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-161">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="3fddc-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="3fddc-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="3fddc-163">**Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-163">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="3fddc-164">**Import-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-164">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3fddc-165">'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için</span><span class="sxs-lookup"><span data-stu-id="3fddc-165">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="3fddc-166">Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="3fddc-166">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="3fddc-167">Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="3fddc-167">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="3fddc-168">**Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-168">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="3fddc-169">**Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-169">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="3fddc-170">**New-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-170">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="3fddc-171">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="3fddc-171">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3fddc-172">'ApiVersionSet' içinde API oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="3fddc-172">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="3fddc-173">'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.</span><span class="sxs-lookup"><span data-stu-id="3fddc-173">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="3fddc-174">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="3fddc-174">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="3fddc-175">**Set-AzApiManagementApi** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-175">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3fddc-176">API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="3fddc-176">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3fddc-177">API'yi 'ApiVersionSet' olarak güncelleştirmek için</span><span class="sxs-lookup"><span data-stu-id="3fddc-177">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="3fddc-178">Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği.</span><span class="sxs-lookup"><span data-stu-id="3fddc-178">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="3fddc-179">**New-AzApiManagementRevision** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-179">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="3fddc-180">'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için.</span><span class="sxs-lookup"><span data-stu-id="3fddc-180">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="3fddc-181">Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.</span><span class="sxs-lookup"><span data-stu-id="3fddc-181">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="3fddc-182">'ApiRevisionDescription' sağlamak için</span><span class="sxs-lookup"><span data-stu-id="3fddc-182">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="3fddc-183">API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.</span><span class="sxs-lookup"><span data-stu-id="3fddc-183">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="3fddc-184">**New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-184">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="3fddc-185">'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için</span><span class="sxs-lookup"><span data-stu-id="3fddc-185">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="3fddc-186">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="3fddc-186">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="3fddc-187">**New-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-187">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3fddc-188">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="3fddc-188">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3fddc-189">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="3fddc-189">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3fddc-190">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-190">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3fddc-191">**Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-191">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3fddc-192">'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="3fddc-192">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3fddc-193">'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için</span><span class="sxs-lookup"><span data-stu-id="3fddc-193">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3fddc-194">Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-194">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3fddc-195">Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-195">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="3fddc-196">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="3fddc-196">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="3fddc-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="3fddc-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="3fddc-198">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="3fddc-198">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="3fddc-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="3fddc-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="3fddc-200">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3fddc-200">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="3fddc-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="3fddc-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="3fddc-202">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="3fddc-202">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="3fddc-203">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="3fddc-203">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="3fddc-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="3fddc-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="3fddc-205">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="3fddc-205">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="3fddc-206">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3fddc-206">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="3fddc-207">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="3fddc-207">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3fddc-208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3fddc-208">Az.Automation</span></span>
* <span data-ttu-id="3fddc-209">Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-209">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="3fddc-210">https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-210">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="3fddc-211">https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-211">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="3fddc-212">Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-212">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="3fddc-213">https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-213">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="3fddc-214">Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-214">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="3fddc-215">Artık yalnızca eşleşen düğüm döndürülüyor.</span><span class="sxs-lookup"><span data-stu-id="3fddc-215">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-216">Az.Compute</span></span>
* <span data-ttu-id="3fddc-217">Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-217">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="3fddc-218">New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor</span><span class="sxs-lookup"><span data-stu-id="3fddc-218">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3fddc-219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3fddc-219">Az.DataLakeStore</span></span>
* <span data-ttu-id="3fddc-220">ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-220">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3fddc-221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3fddc-221">Az.Monitor</span></span>
* <span data-ttu-id="3fddc-222">Yardım örneklerindeki yanlış parametre adları düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-222">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-223">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-223">Az.Network</span></span>
* <span data-ttu-id="3fddc-224">Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-224">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="3fddc-225">Şu cmdlet güncelleştirildi:</span><span class="sxs-lookup"><span data-stu-id="3fddc-225">Updated cmdlet:</span></span>
        - <span data-ttu-id="3fddc-226">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="3fddc-226">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="3fddc-227">New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-227">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-228">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-228">Az.Resources</span></span>
* <span data-ttu-id="3fddc-229">Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-229">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-230">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-230">Az.Sql</span></span>
* <span data-ttu-id="3fddc-231">Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor</span><span class="sxs-lookup"><span data-stu-id="3fddc-231">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="3fddc-232">2.0.0 - Mayıs 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-232">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3fddc-233">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3fddc-233">Az.Accounts</span></span>
* <span data-ttu-id="3fddc-234">Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="3fddc-234">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3fddc-235">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-235">Az.CognitiveServices</span></span>
* <span data-ttu-id="3fddc-236">Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="3fddc-236">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="3fddc-237">Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.</span><span class="sxs-lookup"><span data-stu-id="3fddc-237">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-238">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-238">Az.Compute</span></span>
* <span data-ttu-id="3fddc-239">Yakınlık yerleştirme grubu özelliği.</span><span class="sxs-lookup"><span data-stu-id="3fddc-239">Proximity placement group feature.</span></span>
    - <span data-ttu-id="3fddc-240">Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3fddc-240">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="3fddc-241">Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3fddc-241">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="3fddc-242">StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-242">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="3fddc-243">New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.</span><span class="sxs-lookup"><span data-stu-id="3fddc-243">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="3fddc-244">SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-244">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="3fddc-245">Yeni değişiklikler</span><span class="sxs-lookup"><span data-stu-id="3fddc-245">Breaking changes</span></span>
    - <span data-ttu-id="3fddc-246">Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-246">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="3fddc-247">Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-247">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="3fddc-248">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="3fddc-248">Az.DeploymentManager</span></span>
* <span data-ttu-id="3fddc-249">Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="3fddc-249">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="3fddc-250">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3fddc-250">Az.Dns</span></span>
* <span data-ttu-id="3fddc-251">Otomatik DNS NameServer Temsilcisi</span><span class="sxs-lookup"><span data-stu-id="3fddc-251">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="3fddc-252">Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.</span><span class="sxs-lookup"><span data-stu-id="3fddc-252">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="3fddc-253">Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.</span><span class="sxs-lookup"><span data-stu-id="3fddc-253">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3fddc-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3fddc-254">Az.FrontDoor</span></span>
* <span data-ttu-id="3fddc-255">Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü</span><span class="sxs-lookup"><span data-stu-id="3fddc-255">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="3fddc-256">WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın</span><span class="sxs-lookup"><span data-stu-id="3fddc-256">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="3fddc-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3fddc-257">Az.HDInsight</span></span>
* <span data-ttu-id="3fddc-258">İki cmdlet kaldırıldı:</span><span class="sxs-lookup"><span data-stu-id="3fddc-258">Removed two cmdlets:</span></span>
    - <span data-ttu-id="3fddc-259">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3fddc-259">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="3fddc-260">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3fddc-260">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3fddc-261">Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-261">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3fddc-262">Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:</span><span class="sxs-lookup"><span data-stu-id="3fddc-262">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="3fddc-263">Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="3fddc-263">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="3fddc-264">hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.</span><span class="sxs-lookup"><span data-stu-id="3fddc-264">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3fddc-265">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3fddc-265">Az.Monitor</span></span>
* <span data-ttu-id="3fddc-266">SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="3fddc-266">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="3fddc-267">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3fddc-267">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="3fddc-268">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="3fddc-268">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="3fddc-269">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="3fddc-269">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="3fddc-270">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="3fddc-270">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="3fddc-271">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="3fddc-271">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="3fddc-272">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="3fddc-272">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="3fddc-273">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3fddc-273">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3fddc-274">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3fddc-274">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3fddc-275">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3fddc-275">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3fddc-276">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3fddc-276">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3fddc-277">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3fddc-277">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3fddc-278">SQR API hakkında [daha fazla](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) bilgi</span><span class="sxs-lookup"><span data-stu-id="3fddc-278">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="3fddc-279">Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-279">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-280">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-280">Az.Network</span></span>
* <span data-ttu-id="3fddc-281">Nat Gateway Resource için destek ekleyin</span><span class="sxs-lookup"><span data-stu-id="3fddc-281">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="3fddc-282">Yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3fddc-282">New cmdlets</span></span>
        - <span data-ttu-id="3fddc-283">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3fddc-283">New-AzNatGateway</span></span>
        - <span data-ttu-id="3fddc-284">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3fddc-284">Get-AzNatGateway</span></span>
        - <span data-ttu-id="3fddc-285">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3fddc-285">Set-AzNatGateway</span></span>
        - <span data-ttu-id="3fddc-286">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3fddc-286">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="3fddc-287">Cmdlet'ler güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-287">Updated cmdlets</span></span>
        - <span data-ttu-id="3fddc-288">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3fddc-288">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="3fddc-289">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3fddc-289">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="3fddc-290">Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.</span><span class="sxs-lookup"><span data-stu-id="3fddc-290">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="3fddc-291">New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-291">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="3fddc-292">Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-292">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3fddc-293">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3fddc-293">Az.PolicyInsights</span></span>
* <span data-ttu-id="3fddc-294">İlke değerlendirme ayrıntılarını sorgulama desteği.</span><span class="sxs-lookup"><span data-stu-id="3fddc-294">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="3fddc-295">Get-AzPolicyState komutuna '-Expand' parametresini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3fddc-295">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="3fddc-296">'-Expand PolicyEvaluationDetails' öğesini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="3fddc-296">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3fddc-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="3fddc-298">Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.</span><span class="sxs-lookup"><span data-stu-id="3fddc-298">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="3fddc-299">Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.</span><span class="sxs-lookup"><span data-stu-id="3fddc-299">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="3fddc-300">Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="3fddc-300">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="3fddc-301">Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="3fddc-301">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="3fddc-302">Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.</span><span class="sxs-lookup"><span data-stu-id="3fddc-302">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="3fddc-303">Diğer küçük düzeltmeler.</span><span class="sxs-lookup"><span data-stu-id="3fddc-303">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="3fddc-304">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3fddc-304">Az.Relay</span></span>
* <span data-ttu-id="3fddc-305">Müşteriye dönük iletilerdeki yazım hatalarını düzeltin</span><span class="sxs-lookup"><span data-stu-id="3fddc-305">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3fddc-306">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3fddc-306">Az.ServiceBus</span></span>
* <span data-ttu-id="3fddc-307">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-307">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3fddc-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3fddc-308">Az.Storage</span></span>
* <span data-ttu-id="3fddc-309">Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)</span><span class="sxs-lookup"><span data-stu-id="3fddc-309">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="3fddc-310">Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="3fddc-310">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="3fddc-311">Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir</span><span class="sxs-lookup"><span data-stu-id="3fddc-311">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="3fddc-312">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fddc-312">New-AzStorageAccount</span></span>
* <span data-ttu-id="3fddc-313">'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin</span><span class="sxs-lookup"><span data-stu-id="3fddc-313">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="3fddc-314">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fddc-314">New-AzStorageAccount</span></span>
    - <span data-ttu-id="3fddc-315">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fddc-315">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="3fddc-316">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fddc-316">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3fddc-317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-317">Az.Websites</span></span>
* <span data-ttu-id="3fddc-318">'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır</span><span class="sxs-lookup"><span data-stu-id="3fddc-318">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="3fddc-319">Get-AzWebApp\*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-319">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="3fddc-320">1.8.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-320">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3fddc-321">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="3fddc-321">Highlights since the last major release</span></span>
* <span data-ttu-id="3fddc-322">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3fddc-322">General availability of `Az` module</span></span>
* <span data-ttu-id="3fddc-323">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3fddc-323">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3fddc-324">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3fddc-324">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3fddc-325">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-325">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3fddc-326">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-326">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3fddc-327">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-327">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3fddc-328">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3fddc-328">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3fddc-329">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3fddc-329">Az.Accounts</span></span>
* <span data-ttu-id="3fddc-330">Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-330">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3fddc-331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3fddc-331">Az.Batch</span></span>
* <span data-ttu-id="3fddc-332">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3fddc-333">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3fddc-333">Az.Cdn</span></span>
* <span data-ttu-id="3fddc-334">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-334">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3fddc-335">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-335">Az.CognitiveServices</span></span>
* <span data-ttu-id="3fddc-336">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-336">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-337">Az.Compute</span></span>
* <span data-ttu-id="3fddc-338">Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-338">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="3fddc-339">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-339">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3fddc-340">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-340">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3fddc-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3fddc-341">Az.DataFactory</span></span>
* <span data-ttu-id="3fddc-342">Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-342">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3fddc-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3fddc-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="3fddc-344">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-344">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3fddc-345">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3fddc-345">Az.EventGrid</span></span>
* <span data-ttu-id="3fddc-346">Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-346">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3fddc-347">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3fddc-347">Az.EventHub</span></span>
* <span data-ttu-id="3fddc-348">Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-348">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="3fddc-349">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3fddc-349">Az.HDInsight</span></span>
* <span data-ttu-id="3fddc-350">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3fddc-351">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3fddc-351">Az.IotHub</span></span>
* <span data-ttu-id="3fddc-352">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3fddc-353">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3fddc-353">Az.KeyVault</span></span>
* <span data-ttu-id="3fddc-354">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-354">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3fddc-355">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-355">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="3fddc-356">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3fddc-356">Az.MachineLearning</span></span>
* <span data-ttu-id="3fddc-357">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-357">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="3fddc-358">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3fddc-358">Az.Media</span></span>
* <span data-ttu-id="3fddc-359">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-359">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3fddc-360">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3fddc-360">Az.Monitor</span></span>
  * <span data-ttu-id="3fddc-361">GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler</span><span class="sxs-lookup"><span data-stu-id="3fddc-361">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="3fddc-362">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="3fddc-362">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="3fddc-363">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="3fddc-363">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="3fddc-364">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3fddc-364">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3fddc-365">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3fddc-365">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3fddc-366">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3fddc-366">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="3fddc-367">İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-367">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-368">Az.Network</span></span>
* <span data-ttu-id="3fddc-369">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3fddc-370">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-370">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="3fddc-371">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3fddc-371">Az.NotificationHubs</span></span>
* <span data-ttu-id="3fddc-372">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3fddc-373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3fddc-373">Az.OperationalInsights</span></span>
* <span data-ttu-id="3fddc-374">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-374">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="3fddc-375">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3fddc-375">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="3fddc-376">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3fddc-377">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-377">Az.RecoveryServices</span></span>
* <span data-ttu-id="3fddc-378">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-378">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3fddc-379">Azure VM'de SQL için güncelleştirilmiş tablo biçimi</span><span class="sxs-lookup"><span data-stu-id="3fddc-379">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="3fddc-380">AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-380">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="3fddc-381">SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-381">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3fddc-382">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3fddc-382">Az.RedisCache</span></span>
* <span data-ttu-id="3fddc-383">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-384">Az.Resources</span></span>
* <span data-ttu-id="3fddc-385">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-385">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-386">Az.Sql</span></span>
* <span data-ttu-id="3fddc-387">İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-387">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="3fddc-388">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-388">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3fddc-389">Birden fazla sütun sınıflandırma işlemi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-389">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="3fddc-390">Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-390">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="3fddc-391">Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-391">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="3fddc-392">Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.</span><span class="sxs-lookup"><span data-stu-id="3fddc-392">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="3fddc-393">Joker karakterlere ilişkin belgeler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-393">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3fddc-394">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-394">Az.Websites</span></span>
* <span data-ttu-id="3fddc-395">Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-395">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="3fddc-396">Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-396">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3fddc-397">Web siteleri SDK'sı güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-397">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="3fddc-398">PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-398">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="3fddc-399">1.7.0 - Nisan 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-399">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3fddc-400">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="3fddc-400">Highlights since the last major release</span></span>
* <span data-ttu-id="3fddc-401">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3fddc-401">General availability of `Az` module</span></span>
* <span data-ttu-id="3fddc-402">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3fddc-402">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3fddc-403">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3fddc-403">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3fddc-404">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-404">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3fddc-405">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-405">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3fddc-406">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-406">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3fddc-407">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3fddc-407">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3fddc-408">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3fddc-408">Az.Accounts</span></span>
* <span data-ttu-id="3fddc-409">Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-409">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3fddc-410">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-410">Az.AnalysisServices</span></span>
* <span data-ttu-id="3fddc-411">Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3fddc-411">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="3fddc-412">Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma</span><span class="sxs-lookup"><span data-stu-id="3fddc-412">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3fddc-413">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3fddc-413">Az.Automation</span></span>
* <span data-ttu-id="3fddc-414">Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-414">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="3fddc-415">IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="3fddc-415">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="3fddc-416">Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3fddc-416">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-417">Az.Compute</span></span>
* <span data-ttu-id="3fddc-418">New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-418">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3fddc-419">Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-419">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="3fddc-420">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3fddc-420">Az.ContainerInstance</span></span>
* <span data-ttu-id="3fddc-421">New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-421">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3fddc-422">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3fddc-422">Az.DataFactory</span></span>
* <span data-ttu-id="3fddc-423">ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-423">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="3fddc-424">Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-424">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-425">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-425">Az.Resources</span></span>
* <span data-ttu-id="3fddc-426">'-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-426">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="3fddc-427">‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-427">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="3fddc-428">İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-428">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="3fddc-429">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3fddc-429">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="3fddc-430">Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-430">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="3fddc-431">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3fddc-431">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-432">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-432">Az.Sql</span></span>
* <span data-ttu-id="3fddc-433">Veritabanı Verileri Sınıflandırması Desteği.</span><span class="sxs-lookup"><span data-stu-id="3fddc-433">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3fddc-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3fddc-434">Az.Storage</span></span>
* <span data-ttu-id="3fddc-435">-UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama</span><span class="sxs-lookup"><span data-stu-id="3fddc-435">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="3fddc-436">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3fddc-436">New-AzStorageContext</span></span>
* <span data-ttu-id="3fddc-437">Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği</span><span class="sxs-lookup"><span data-stu-id="3fddc-437">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="3fddc-438">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3fddc-438">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3fddc-439">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3fddc-439">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3fddc-440">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3fddc-440">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="3fddc-441">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3fddc-441">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="3fddc-442">Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği</span><span class="sxs-lookup"><span data-stu-id="3fddc-442">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="3fddc-443">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3fddc-443">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3fddc-444">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3fddc-444">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3fddc-445">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3fddc-445">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="3fddc-446">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3fddc-446">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="3fddc-447">1.6.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-447">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3fddc-448">Son ana sürümden bu yana öne çıkanlar</span><span class="sxs-lookup"><span data-stu-id="3fddc-448">Highlights since the last major release</span></span>
* <span data-ttu-id="3fddc-449">`Az` modülünü genel kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3fddc-449">General availability of `Az` module</span></span>
* <span data-ttu-id="3fddc-450">`Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3fddc-450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3fddc-451">Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3fddc-451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3fddc-452">Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3fddc-453">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3fddc-454">Az.Automation'da Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3fddc-455">Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3fddc-455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3fddc-456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3fddc-456">Az.Automation</span></span>
* <span data-ttu-id="3fddc-457">Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:</span><span class="sxs-lookup"><span data-stu-id="3fddc-457">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="3fddc-458">Dinamik gruplandırma</span><span class="sxs-lookup"><span data-stu-id="3fddc-458">Dynamic grouping</span></span>
    * <span data-ttu-id="3fddc-459">Ön-Son betik</span><span class="sxs-lookup"><span data-stu-id="3fddc-459">Pre-Post script</span></span>
    * <span data-ttu-id="3fddc-460">Yeniden Başlatma Ayarı</span><span class="sxs-lookup"><span data-stu-id="3fddc-460">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-461">Az.Compute</span></span>
* <span data-ttu-id="3fddc-462">Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3fddc-462">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="3fddc-463">İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-463">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3fddc-464">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3fddc-464">Az.KeyVault</span></span>
* <span data-ttu-id="3fddc-465">KeyVault cmdlet'lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-465">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-466">Az.Network</span></span>
* <span data-ttu-id="3fddc-467">Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-467">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="3fddc-468">Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-468">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3fddc-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="3fddc-470">Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-470">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="3fddc-471">Kapsayıcı kaydını kaldırmak için kanal desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-471">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-472">Az.Resources</span></span>
* <span data-ttu-id="3fddc-473">Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-473">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="3fddc-474">ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-474">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-475">Az.Sql</span></span>
* <span data-ttu-id="3fddc-476">Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-476">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3fddc-477">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3fddc-477">Az.Storage</span></span>
* <span data-ttu-id="3fddc-478">Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği</span><span class="sxs-lookup"><span data-stu-id="3fddc-478">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="3fddc-479">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3fddc-479">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3fddc-480">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3fddc-480">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3fddc-481">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3fddc-481">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3fddc-482">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3fddc-482">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="3fddc-483">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="3fddc-483">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="3fddc-484">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="3fddc-484">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3fddc-485">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-485">Az.Websites</span></span>
* <span data-ttu-id="3fddc-486">'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-486">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="3fddc-487">1.5.0 - Mart 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-487">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3fddc-488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3fddc-488">Az.Accounts</span></span>
* <span data-ttu-id="3fddc-489">AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-489">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="3fddc-490">Connect-AzAccount örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-490">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3fddc-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3fddc-491">Az.Automation</span></span>
* <span data-ttu-id="3fddc-492">Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-492">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="3fddc-493">Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-493">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="3fddc-494">Artık tüm düğümleri döndürür</span><span class="sxs-lookup"><span data-stu-id="3fddc-494">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3fddc-495">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3fddc-495">Az.Cdn</span></span>
* <span data-ttu-id="3fddc-496">Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="3fddc-496">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-497">Az.Compute</span></span>
* <span data-ttu-id="3fddc-498">Get cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-498">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3fddc-499">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3fddc-499">Az.DataFactory</span></span>
* <span data-ttu-id="3fddc-500">ADF .Net SDK sürümü 3.0.1'e güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-500">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3fddc-501">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3fddc-501">Az.LogicApp</span></span>
* <span data-ttu-id="3fddc-502">Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme</span><span class="sxs-lookup"><span data-stu-id="3fddc-502">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-503">Az.Network</span></span>
* <span data-ttu-id="3fddc-504">Network cmdlet’lerine joker karakter desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-504">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3fddc-505">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-505">Az.RecoveryServices</span></span>
* <span data-ttu-id="3fddc-506">Azure VM desteğine SQL Server eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-506">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="3fddc-507">SDK Güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="3fddc-507">SDK Update</span></span>
* <span data-ttu-id="3fddc-508">Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3fddc-508">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="3fddc-509">Get-ProtectableItem için Name ve ServerName parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-509">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-510">Az.Resources</span></span>
* <span data-ttu-id="3fddc-511">Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-511">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="3fddc-512">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="3fddc-512">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="3fddc-513">`Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-513">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="3fddc-514">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="3fddc-514">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="3fddc-515">`Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-515">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="3fddc-516">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="3fddc-516">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-517">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-517">Az.Sql</span></span>
* <span data-ttu-id="3fddc-518">AuditingEndpointsCommunicator güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="3fddc-518">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="3fddc-519">Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.</span><span class="sxs-lookup"><span data-stu-id="3fddc-519">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3fddc-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3fddc-520">Az.Storage</span></span>
* <span data-ttu-id="3fddc-521">Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fddc-521">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="3fddc-522">1.4.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-522">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="3fddc-523">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-523">Az.AnalysisServices</span></span>
* <span data-ttu-id="3fddc-524">AddAzureASAccount cmdlet'i kullanım dışı bırakıldı</span><span class="sxs-lookup"><span data-stu-id="3fddc-524">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3fddc-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3fddc-525">Az.Automation</span></span>
* <span data-ttu-id="3fddc-526">Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-526">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="3fddc-527">Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-527">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="3fddc-528">Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-528">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3fddc-529">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-529">Az.CognitiveServices</span></span>
* <span data-ttu-id="3fddc-530">Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-530">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-531">Az.Compute</span></span>
* <span data-ttu-id="3fddc-532">Kimlik parametresi kümeleriyle ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-532">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="3fddc-533">Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-533">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="3fddc-534">Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-534">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="3fddc-535">Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.</span><span class="sxs-lookup"><span data-stu-id="3fddc-535">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3fddc-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3fddc-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="3fddc-537">ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-537">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3fddc-538">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3fddc-538">Az.EventHub</span></span>
* <span data-ttu-id="3fddc-539">EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-539">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="3fddc-540">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3fddc-540">Az.KeyVault</span></span>
* <span data-ttu-id="3fddc-541">Set-AzKeyVaultSecret’daki etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-541">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3fddc-542">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3fddc-542">Az.LogicApp</span></span>
* <span data-ttu-id="3fddc-543">Tümleştirme Hesapları için Temel SKU eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-543">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="3fddc-544">XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-544">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="3fddc-545">Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3fddc-545">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="3fddc-546">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3fddc-546">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3fddc-547">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3fddc-547">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3fddc-548">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3fddc-548">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3fddc-549">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3fddc-549">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="3fddc-550">Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler</span><span class="sxs-lookup"><span data-stu-id="3fddc-550">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="3fddc-551">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fddc-551">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3fddc-552">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fddc-552">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3fddc-553">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fddc-553">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3fddc-554">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fddc-554">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="3fddc-555">Logic Apps SDK sürüm 4.1.0’a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-555">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3fddc-556">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3fddc-556">Az.Monitor</span></span>
* <span data-ttu-id="3fddc-557">Get-AzMetric için yardım güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-557">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-558">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-558">Az.Network</span></span>
* <span data-ttu-id="3fddc-559">Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-559">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3fddc-560">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3fddc-560">Az.OperationalInsights</span></span>
* <span data-ttu-id="3fddc-561">New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.</span><span class="sxs-lookup"><span data-stu-id="3fddc-561">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="3fddc-562">Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-562">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="3fddc-563">Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-563">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="3fddc-564">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-564">Az.Resources</span></span>
* <span data-ttu-id="3fddc-565">https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-565">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3fddc-566">https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-566">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="3fddc-567">https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-567">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="3fddc-568">KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-568">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-569">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-569">Az.Sql</span></span>
* <span data-ttu-id="3fddc-570">SQL DB Hiper Ölçek katmanı için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-570">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="3fddc-571">Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-571">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3fddc-572">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-572">Az.Websites</span></span>
* <span data-ttu-id="3fddc-573">Get-AzWebAppSlotMetrics örneği düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-573">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="3fddc-574">1.3.0 - Şubat 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-574">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3fddc-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3fddc-575">Az.Accounts</span></span>
* <span data-ttu-id="3fddc-576">En son ClientRuntime sürümüne güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3fddc-576">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3fddc-577">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-577">Az.AnalysisServices</span></span>
<span data-ttu-id="3fddc-578">Az.AnalysisServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="3fddc-578">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-579">Az.Compute</span></span>
* <span data-ttu-id="3fddc-580">AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-580">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="3fddc-581">Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-581">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="3fddc-582">Update-AzImage için yardım açıklaması ve örnek güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-582">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3fddc-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-583">Az.RecoveryServices</span></span>
<span data-ttu-id="3fddc-584">Az.RecoveryServices modülü için genel kullanılabilirlik.</span><span class="sxs-lookup"><span data-stu-id="3fddc-584">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-585">Az.Resources</span></span>
* <span data-ttu-id="3fddc-586">Kaynak grupları için etiketleme düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-586">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="3fddc-587">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3fddc-587">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3fddc-588">`Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-588">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="3fddc-589">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3fddc-589">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-590">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-590">Az.Sql</span></span>
* <span data-ttu-id="3fddc-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3fddc-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="3fddc-592">Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-592">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="3fddc-593">Get-AzSqlCapability'de null başvuru özel durumu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-593">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="3fddc-594">1.2.1 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-594">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3fddc-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3fddc-595">Az.Accounts</span></span>
* <span data-ttu-id="3fddc-596">Kimlik Doğrulaması'nın doğru yayınını içeren sürümü</span><span class="sxs-lookup"><span data-stu-id="3fddc-596">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3fddc-597">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-597">Az.AnalysisServices</span></span>
* <span data-ttu-id="3fddc-598">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="3fddc-598">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3fddc-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="3fddc-600">Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm</span><span class="sxs-lookup"><span data-stu-id="3fddc-600">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="3fddc-601">1.2.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-601">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3fddc-602">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3fddc-602">Az.Accounts</span></span>
* <span data-ttu-id="3fddc-603">Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-603">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3fddc-604">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-604">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3fddc-605">Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-605">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="3fddc-606">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3fddc-606">Az.Aks</span></span>
* <span data-ttu-id="3fddc-607">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-607">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3fddc-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3fddc-608">Az.Automation</span></span>
* <span data-ttu-id="3fddc-609">Python 2 runbook'ları için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-609">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="3fddc-610">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-610">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3fddc-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3fddc-611">Az.Cdn</span></span>
* <span data-ttu-id="3fddc-612">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-612">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-613">Az.Compute</span></span>
* <span data-ttu-id="3fddc-614">Invoke-AzVMReimage cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-614">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="3fddc-615">Set-AzVmss'ye TempDisk parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-615">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="3fddc-616">New-AzVM'nin uyarı iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-616">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3fddc-617">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3fddc-617">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3fddc-618">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-618">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3fddc-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3fddc-619">Az.DataFactory</span></span>
* <span data-ttu-id="3fddc-620">ADF .Net SDK sürümü 3.0.0'a güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-620">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3fddc-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3fddc-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="3fddc-622">MSI kullanırken ADLS uç noktasındaki sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-622">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="3fddc-623">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="3fddc-623">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="3fddc-624">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-624">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3fddc-625">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3fddc-625">Az.IotHub</span></span>
* <span data-ttu-id="3fddc-626">Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-626">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3fddc-627">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3fddc-627">Az.KeyVault</span></span>
* <span data-ttu-id="3fddc-628">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-628">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-629">Az.Network</span></span>
* <span data-ttu-id="3fddc-630">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-630">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-631">Az.Resources</span></span>
* <span data-ttu-id="3fddc-632">'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-632">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="3fddc-633">Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-633">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="3fddc-634">Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-634">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="3fddc-635">Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-635">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="3fddc-636">Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-636">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="3fddc-637">'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-637">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="3fddc-638">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="3fddc-638">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3fddc-639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3fddc-639">Az.ServiceFabric</span></span>
* <span data-ttu-id="3fddc-640">VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="3fddc-640">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="3fddc-641">Bazı hata iletileri düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-641">Fix some error messages.</span></span>
* <span data-ttu-id="3fddc-642">Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-642">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="3fddc-643">Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-643">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3fddc-644">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3fddc-644">Az.SignalR</span></span>
* <span data-ttu-id="3fddc-645">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-645">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-646">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-646">Az.Sql</span></span>
* <span data-ttu-id="3fddc-647">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-647">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3fddc-648">LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-648">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="3fddc-649">Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-649">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="3fddc-650">Yönetilen örnekte özel harmanlama desteği</span><span class="sxs-lookup"><span data-stu-id="3fddc-650">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3fddc-651">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3fddc-651">Az.Storage</span></span>
* <span data-ttu-id="3fddc-652">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3fddc-653">Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.</span><span class="sxs-lookup"><span data-stu-id="3fddc-653">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="3fddc-654">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3fddc-654">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="3fddc-655">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="3fddc-655">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="3fddc-656">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3fddc-656">Az.TrafficManager</span></span>
* <span data-ttu-id="3fddc-657">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-657">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3fddc-658">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-658">Az.Websites</span></span>
* <span data-ttu-id="3fddc-659">Hatalı çevrimiçi yardım URL'leri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-659">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3fddc-660">Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-660">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="3fddc-661">SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-661">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="3fddc-662">1.1.0 - Ocak 2019</span><span class="sxs-lookup"><span data-stu-id="3fddc-662">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3fddc-663">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3fddc-663">Az.Accounts</span></span>
* <span data-ttu-id="3fddc-664">Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-664">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-665">Az.Compute</span></span>
* <span data-ttu-id="3fddc-666">Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="3fddc-666">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="3fddc-667">Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-667">Updated the description of ID in help files</span></span>
* <span data-ttu-id="3fddc-668">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3fddc-668">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3fddc-669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3fddc-669">Az.DataLakeStore</span></span>
* <span data-ttu-id="3fddc-670">SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-670">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="3fddc-671">getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-671">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3fddc-672">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3fddc-672">Az.EventGrid</span></span>
* <span data-ttu-id="3fddc-673">2019-01-01 API sürümünü kullanmak için güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-673">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="3fddc-674">Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-674">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="3fddc-675">New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="3fddc-675">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3fddc-676">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="3fddc-676">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3fddc-677">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="3fddc-677">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3fddc-678">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="3fddc-678">Dead letter endpoint.</span></span>
    - <span data-ttu-id="3fddc-679">Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:</span><span class="sxs-lookup"><span data-stu-id="3fddc-679">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3fddc-680">Olay Yaşam Süresi,</span><span class="sxs-lookup"><span data-stu-id="3fddc-680">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3fddc-681">Olaylar için teslim girişimleri sayısı üst sınırı,</span><span class="sxs-lookup"><span data-stu-id="3fddc-681">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3fddc-682">Teslim edilemeyen ileti uç noktası.</span><span class="sxs-lookup"><span data-stu-id="3fddc-682">Dead letter endpoint.</span></span>
* <span data-ttu-id="3fddc-683">New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-683">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="3fddc-684">Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="3fddc-684">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3fddc-685">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3fddc-685">Az.IotHub</span></span>
* <span data-ttu-id="3fddc-686">IotHub SDK'sı en son sürümüne güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-686">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3fddc-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3fddc-687">Az.LogicApp</span></span>
* <span data-ttu-id="3fddc-688">Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor</span><span class="sxs-lookup"><span data-stu-id="3fddc-688">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-689">Az.Resources</span></span>
* <span data-ttu-id="3fddc-690">'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-690">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="3fddc-691">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="3fddc-691">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="3fddc-692">New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-692">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3fddc-693">New-AzDeployment belgelerindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-693">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="3fddc-694">'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-694">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="3fddc-695">Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="3fddc-695">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3fddc-696">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3fddc-696">Az.SignalR</span></span>
* <span data-ttu-id="3fddc-697">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3fddc-697">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-698">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-698">Az.Sql</span></span>
* <span data-ttu-id="3fddc-699">Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="3fddc-699">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3fddc-700">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3fddc-700">Az.Storage</span></span>
* <span data-ttu-id="3fddc-701">Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor</span><span class="sxs-lookup"><span data-stu-id="3fddc-701">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="3fddc-702">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3fddc-702">New-AzStorageContext</span></span>
* <span data-ttu-id="3fddc-703">Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-703">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="3fddc-704">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3fddc-704">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3fddc-705">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-705">Az.Websites</span></span>
* <span data-ttu-id="3fddc-706">'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-706">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3fddc-707">Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3fddc-707">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="3fddc-708">1.0.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="3fddc-708">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="3fddc-709">Genel</span><span class="sxs-lookup"><span data-stu-id="3fddc-709">General</span></span>

- <span data-ttu-id="3fddc-710">Az Modülü Genel Kullanıma Sunuldu</span><span class="sxs-lookup"><span data-stu-id="3fddc-710">General Availability of Az Module</span></span>
- <span data-ttu-id="3fddc-711">Her modül için çevrimiçi yardım</span><span class="sxs-lookup"><span data-stu-id="3fddc-711">Online help for each module</span></span>
- <span data-ttu-id="3fddc-712">Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="3fddc-712">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="3fddc-713">AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-713">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="3fddc-714">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3fddc-714">Az.Accounts</span></span>
- <span data-ttu-id="3fddc-715">Önceki adı: Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3fddc-715">Changed from Az.Profile</span></span>
- <span data-ttu-id="3fddc-716">Profil ve bağlam türleri için tablo biçimleri düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-716">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3fddc-717">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3fddc-717">Az.ApiManagement</span></span>
- <span data-ttu-id="3fddc-718">#7002 düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="3fddc-718">Fixes for #7002</span></span>
- <span data-ttu-id="3fddc-719">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-719">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="3fddc-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3fddc-720">Az.Batch</span></span>
- <span data-ttu-id="3fddc-721">`PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-721">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="3fddc-722">`PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="3fddc-722">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="3fddc-723">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-723">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="3fddc-724">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3fddc-724">Az.Billing</span></span>
- <span data-ttu-id="3fddc-725">Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-725">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="3fddc-726">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-726">Az.CognitivServices</span></span>
- <span data-ttu-id="3fddc-727">New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-727">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="3fddc-728">Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3fddc-728">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3fddc-729">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3fddc-729">Az.ContainerInstance</span></span>
- <span data-ttu-id="3fddc-730">ManagedIdentity desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-730">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="3fddc-731">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3fddc-731">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="3fddc-732">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-732">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3fddc-733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3fddc-733">Az.DataLakeStore</span></span>
- <span data-ttu-id="3fddc-734">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-734">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="3fddc-735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3fddc-735">Az.Monitor</span></span>
- <span data-ttu-id="3fddc-736">Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-736">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="3fddc-737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3fddc-737">Az.KeyVault</span></span>
- <span data-ttu-id="3fddc-738">Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3fddc-738">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="3fddc-739">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3fddc-739">Az.MachineLearning</span></span>
- <span data-ttu-id="3fddc-740">Az.MachineLearningCompute modülünden cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-740">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="3fddc-741">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3fddc-741">Az.Media</span></span>
- <span data-ttu-id="3fddc-742">New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="3fddc-742">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3fddc-743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-743">Az.Network</span></span>
<span data-ttu-id="3fddc-744">Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-744">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="3fddc-745">Yeni cmdlet'ler eklendi:</span><span class="sxs-lookup"><span data-stu-id="3fddc-745">New cmdlets added:</span></span>
        - <span data-ttu-id="3fddc-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3fddc-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3fddc-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3fddc-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3fddc-748">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3fddc-748">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3fddc-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3fddc-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3fddc-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3fddc-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3fddc-751">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3fddc-751">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="3fddc-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3fddc-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="3fddc-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fddc-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="3fddc-754">Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-754">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="3fddc-755">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3fddc-755">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="3fddc-756">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3fddc-756">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3fddc-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3fddc-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3fddc-758">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3fddc-758">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="3fddc-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3fddc-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="3fddc-760">New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-760">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="3fddc-761">Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-761">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="3fddc-762">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3fddc-762">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3fddc-763">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3fddc-763">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3fddc-764">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3fddc-764">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="3fddc-765">New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-765">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="3fddc-766">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-766">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="3fddc-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3fddc-767">Az.OperationalInsights</span></span>
- <span data-ttu-id="3fddc-768">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-768">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="3fddc-769">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3fddc-769">Az.Profile</span></span>
- <span data-ttu-id="3fddc-770">Modül adı Az.Accounts olarak değiştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-770">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3fddc-771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-771">Az.RecoveryServices</span></span>
- <span data-ttu-id="3fddc-772">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-772">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="3fddc-773">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-773">Az.Resources</span></span>
- <span data-ttu-id="3fddc-774">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-774">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3fddc-775">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3fddc-775">Az.ServiceFabric</span></span>
- <span data-ttu-id="3fddc-776">Sertifikayı ortak ad ve parmak iziyle belirtme desteği</span><span class="sxs-lookup"><span data-stu-id="3fddc-776">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="3fddc-777">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-777">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="3fddc-778">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3fddc-778">Az.SIgnalR</span></span>
- <span data-ttu-id="3fddc-779">SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu</span><span class="sxs-lookup"><span data-stu-id="3fddc-779">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="3fddc-780">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-780">Az.Sql</span></span>
- <span data-ttu-id="3fddc-781">Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-781">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="3fddc-782">Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-782">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="3fddc-783">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-783">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="3fddc-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3fddc-784">Az.Storage</span></span>
- <span data-ttu-id="3fddc-785">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-785">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3fddc-786">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-786">Az.Websites</span></span>
- <span data-ttu-id="3fddc-787">Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="3fddc-787">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="3fddc-788">0.7.0 - Aralık 2018</span><span class="sxs-lookup"><span data-stu-id="3fddc-788">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="3fddc-789">Genel</span><span class="sxs-lookup"><span data-stu-id="3fddc-789">General</span></span>

* <span data-ttu-id="3fddc-790">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="3fddc-790">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="3fddc-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-791">Az.Compute</span></span>

* <span data-ttu-id="3fddc-792">`New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-792">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3fddc-793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3fddc-793">Az.DataLakeStore</span></span>

* <span data-ttu-id="3fddc-794">Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-794">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="3fddc-795">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3fddc-795">Az.FrontDoor</span></span>

* <span data-ttu-id="3fddc-796">Bazı bozuk bağlantılar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-796">Fixed some broken links</span></span>
    - <span data-ttu-id="3fddc-797">New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-797">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="3fddc-798">New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-798">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3fddc-799">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-799">Az.RecoveryServices</span></span>

* <span data-ttu-id="3fddc-800">Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-800">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="3fddc-801">Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-801">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="3fddc-802">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-802">Az.Resources</span></span>

* <span data-ttu-id="3fddc-803">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3fddc-803">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="3fddc-804">Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-804">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="3fddc-805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-805">Az.Sql</span></span>

* <span data-ttu-id="3fddc-806">Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler</span><span class="sxs-lookup"><span data-stu-id="3fddc-806">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="3fddc-807">Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-807">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="3fddc-808">SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-808">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="3fddc-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3fddc-809">Az.Storage</span></span>

* <span data-ttu-id="3fddc-810">New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-810">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="3fddc-811">-DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-811">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="3fddc-812">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3fddc-812">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3fddc-813">Statik Web Sitesi yapılandırması için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-813">Support Static Website configuration</span></span>
    - <span data-ttu-id="3fddc-814">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3fddc-814">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="3fddc-815">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3fddc-815">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3fddc-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-816">Az.Websites</span></span>

* <span data-ttu-id="3fddc-817">Set-AzureRmWebApp ve Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3fddc-817">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="3fddc-818">Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-818">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="3fddc-819">Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="3fddc-819">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="3fddc-820">0.6.1 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="3fddc-820">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3fddc-821">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3fddc-821">Az.ApiManagement</span></span>
* <span data-ttu-id="3fddc-822">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="3fddc-822">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="3fddc-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3fddc-823">Az.Automation</span></span>
* <span data-ttu-id="3fddc-824">Swagger tabanlı Azure Otomasyon cmdlet'leri</span><span class="sxs-lookup"><span data-stu-id="3fddc-824">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="3fddc-825">Güncelleştirme Yönetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-825">Added Update Management cmdlets</span></span>
* <span data-ttu-id="3fddc-826">Kaynak Denetimi cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-826">Added Source Control cmdlets</span></span>
* <span data-ttu-id="3fddc-827">Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-827">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="3fddc-828">DSC Kayıt Düğümü komutu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-828">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="3fddc-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-829">Az.Compute</span></span>
* <span data-ttu-id="3fddc-830">SystemAssigned kimliği için kimlik sorunu düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-830">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="3fddc-831">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="3fddc-831">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3fddc-832">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3fddc-832">Az.ContainerInstance</span></span>
* <span data-ttu-id="3fddc-833">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="3fddc-833">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="3fddc-834">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3fddc-834">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3fddc-835">Market cmdlet'leri için örnekler açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-835">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3fddc-836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-836">Az.Network</span></span>
* <span data-ttu-id="3fddc-837">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-837">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="3fddc-838">Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-838">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="3fddc-839">Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-839">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="3fddc-840">VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-840">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="3fddc-841">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3fddc-841">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3fddc-842">Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-842">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="3fddc-843">İlke saat dilimi büyük harfe dönüştürüldü.</span><span class="sxs-lookup"><span data-stu-id="3fddc-843">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="3fddc-844">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3fddc-844">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3fddc-845">New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-845">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="3fddc-846">Tür eşlemesinde güncelleştirme bağımlılıkları sorunu</span><span class="sxs-lookup"><span data-stu-id="3fddc-846">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="3fddc-847">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3fddc-847">Az.Relay</span></span>
* <span data-ttu-id="3fddc-848">Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-848">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="3fddc-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-849">Az.Resources</span></span>
* <span data-ttu-id="3fddc-850">`New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-850">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="3fddc-851">New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-851">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="3fddc-852">NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="3fddc-852">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3fddc-853">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3fddc-853">Az.ServiceFabric</span></span>
* <span data-ttu-id="3fddc-854">Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-854">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="3fddc-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-855">Az.Sql</span></span>
* <span data-ttu-id="3fddc-856">Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-856">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="3fddc-857">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3fddc-857">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3fddc-858">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3fddc-858">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3fddc-859">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3fddc-859">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3fddc-860">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3fddc-860">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3fddc-861">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3fddc-861">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3fddc-862">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3fddc-862">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3fddc-863">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3fddc-863">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3fddc-864">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3fddc-864">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="3fddc-865">Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-865">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="3fddc-866">Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-866">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="3fddc-867">Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-867">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="3fddc-868">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3fddc-868">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3fddc-869">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3fddc-869">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3fddc-870">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3fddc-870">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="3fddc-871">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3fddc-871">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="3fddc-872">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-872">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="3fddc-873">0.5.0 - Kasım 2018</span><span class="sxs-lookup"><span data-stu-id="3fddc-873">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3fddc-874">Genel</span><span class="sxs-lookup"><span data-stu-id="3fddc-874">General</span></span>
* <span data-ttu-id="3fddc-875">Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır</span><span class="sxs-lookup"><span data-stu-id="3fddc-875">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="3fddc-876">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3fddc-876">Az.Profile</span></span>
* <span data-ttu-id="3fddc-877">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-877">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3fddc-878">Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-878">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3fddc-879">Connect-AzAccount için TenantId açıklaması güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-879">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="3fddc-880">Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-880">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3fddc-881">Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-881">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3fddc-882">MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-882">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3fddc-883">Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-883">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="3fddc-884">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-884">Az.CognitiveServices</span></span>
* <span data-ttu-id="3fddc-885">Get-AzCognitiveServicesAccountSkus işlemi eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-885">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-886">Az.Compute</span></span>
* <span data-ttu-id="3fddc-887">Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-887">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3fddc-888">Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor</span><span class="sxs-lookup"><span data-stu-id="3fddc-888">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3fddc-889">SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-889">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3fddc-890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3fddc-890">Az.DataLakeStore</span></span>
* <span data-ttu-id="3fddc-891">DataLake paketi 1.1.10'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-891">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3fddc-892">Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-892">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="3fddc-893">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="3fddc-893">Az.Insights</span></span>
* <span data-ttu-id="3fddc-894">7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-894">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3fddc-895">Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).</span><span class="sxs-lookup"><span data-stu-id="3fddc-895">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3fddc-896">Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-896">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3fddc-897">Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor</span><span class="sxs-lookup"><span data-stu-id="3fddc-897">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-898">Az.Network</span></span>
* <span data-ttu-id="3fddc-899">Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-</span><span class="sxs-lookup"><span data-stu-id="3fddc-899">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3fddc-900">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3fddc-900">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3fddc-901">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3fddc-901">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3fddc-902">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3fddc-902">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3fddc-903">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3fddc-903">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3fddc-904">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3fddc-904">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3fddc-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3fddc-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3fddc-906">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3fddc-906">Az.PolicyInsights</span></span>
* <span data-ttu-id="3fddc-907">İlke düzeltme cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-907">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-908">Az.Resources</span></span>
* <span data-ttu-id="3fddc-909">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402) düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="3fddc-909">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3fddc-910">'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı</span><span class="sxs-lookup"><span data-stu-id="3fddc-910">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3fddc-911">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3fddc-911">Az.ServiceBus</span></span>
* <span data-ttu-id="3fddc-912">PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-912">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3fddc-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3fddc-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="3fddc-914">Linux Vmss'ye sertifika ekleme sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-914">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3fddc-915">'Add-AzServiceFabricClusterCertificate' düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-915">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3fddc-916">Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="3fddc-916">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3fddc-917">Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="3fddc-917">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3fddc-918">'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-918">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="3fddc-919">0.4.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="3fddc-919">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="3fddc-920">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3fddc-920">Az.Profile</span></span>
* <span data-ttu-id="3fddc-921">CloudShell’de Get-AzSubscription sorunu çözüldü</span><span class="sxs-lookup"><span data-stu-id="3fddc-921">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="3fddc-922">ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-922">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-923">Az.Compute</span></span>
* <span data-ttu-id="3fddc-924">'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-924">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="3fddc-925">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-925">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3fddc-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3fddc-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="3fddc-927">Sanal Ağ Kuralları desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="3fddc-927">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3fddc-928">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="3fddc-928">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3fddc-929">Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="3fddc-929">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3fddc-930">Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="3fddc-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3fddc-931">Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.</span><span class="sxs-lookup"><span data-stu-id="3fddc-931">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-932">Az.Network</span></span>
* <span data-ttu-id="3fddc-933">Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.</span><span class="sxs-lookup"><span data-stu-id="3fddc-933">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3fddc-934">Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-934">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-935">Az.Resources</span></span>
* <span data-ttu-id="3fddc-936">Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-936">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3fddc-937">Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-937">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="3fddc-938">0.3.0 - Ekim 2018</span><span class="sxs-lookup"><span data-stu-id="3fddc-938">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3fddc-939">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="3fddc-939">Azure.Storage</span></span>
* <span data-ttu-id="3fddc-940">Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak</span><span class="sxs-lookup"><span data-stu-id="3fddc-940">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3fddc-941">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3fddc-941">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3fddc-942">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3fddc-942">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3fddc-943">Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.</span><span class="sxs-lookup"><span data-stu-id="3fddc-943">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3fddc-944">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3fddc-944">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="3fddc-945">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3fddc-945">Az.CognitiveServices</span></span>
* <span data-ttu-id="3fddc-946">Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.</span><span class="sxs-lookup"><span data-stu-id="3fddc-946">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3fddc-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3fddc-947">Az.Compute</span></span>
* <span data-ttu-id="3fddc-948">Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-948">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3fddc-949">New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-949">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="3fddc-950">Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-950">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="3fddc-951">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3fddc-951">Az.DataFactoryV2</span></span>
* <span data-ttu-id="3fddc-952">ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-952">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3fddc-953">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3fddc-953">Az.Network</span></span>
* <span data-ttu-id="3fddc-954">NetworkProfile işlevselliği eklendi.</span><span class="sxs-lookup"><span data-stu-id="3fddc-954">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3fddc-955">yeni cmdlet'ler eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-955">new cmdlets added</span></span>
    - <span data-ttu-id="3fddc-956">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3fddc-956">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="3fddc-957">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3fddc-957">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="3fddc-958">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3fddc-958">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="3fddc-959">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3fddc-959">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="3fddc-960">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3fddc-960">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="3fddc-961">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3fddc-961">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3fddc-962">Alt Ağ Modeline hizmet ilişki bağlantısı eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-962">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3fddc-963">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-963">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="3fddc-964">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-964">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3fddc-965">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3fddc-965">Az.RedisCache</span></span>
* <span data-ttu-id="3fddc-966">Bundan sonra Size parametresi olarak her dizeye izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="3fddc-966">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3fddc-967">PSArgumentCompleter açılan listesine P5 eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-967">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="3fddc-968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3fddc-968">Az.Resources</span></span>
* <span data-ttu-id="3fddc-969">Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="3fddc-969">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3fddc-970">Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-970">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="3fddc-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3fddc-971">Az.Sql</span></span>
* <span data-ttu-id="3fddc-972">Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi</span><span class="sxs-lookup"><span data-stu-id="3fddc-972">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3fddc-973">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3fddc-973">Az.Websites</span></span>
* <span data-ttu-id="3fddc-974">Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor</span><span class="sxs-lookup"><span data-stu-id="3fddc-974">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3fddc-975">Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor</span><span class="sxs-lookup"><span data-stu-id="3fddc-975">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="3fddc-976">0.2.0 - Eylül 2018</span><span class="sxs-lookup"><span data-stu-id="3fddc-976">0.2.0 - September 2018</span></span>
 <span data-ttu-id="3fddc-977">İlk Yayın</span><span class="sxs-lookup"><span data-stu-id="3fddc-977">Initial Release</span></span>