---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498684"
---
## <a name="220---june-2019"></a>2.2.0 - Haziran 2019
#### <a name="azcdn"></a>Az.Cdn
* Cmdlet'ler API sürümü 2019-04-15’i temel alan rulesEngine özelliğini destekleyecek şekilde güncelleştirildi.

#### <a name="azcompute"></a>Az.Compute
* İşlemi başlatan ve işlem tamamlanmadan önce hemen döndürülen `NoWait` parametresi eklendi.
    - Cmdlet'ler güncelleştirildi:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* #9231 - Get-AzEventHubNamespace etiketleri döndürmüyor hatasının düzeltmesi
* #9230 - Get-AzEventHubNamespace ResourceGroupName yerine ResourceGroup döndürüyor hatasının düzeltmesi

#### <a name="aznetwork"></a>Az.Network
* Nat Gateway için ResourceId ve InputObject değerleri güncelleştirildi
    - ResourceId ve InputObject için diğer ad eklendi

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Get-AzPolicyEvent’de Boş referans sorunu düzeltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* IaaSVM ilkesinin gün cinsinden en kısa saklama süresi 1'den 7'ye değiştirildi

#### <a name="azservicebus"></a>Az.ServiceBus
* #9182 - Get-AzServiceBusNamespace ResourceGroupName yerine ResourceGroup döndürüyor sorunu çözüldü

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 'Update-AzServiceFabricReliability' hata iletisindeki yazım hatası düzeltildi
* Service Fabric komut satırlarındaki eksik karakter düzeltildi

#### <a name="azsql"></a>Az.Sql
* Yönetilen Örnek için AutoDr’yi desteklemek amacıyla New-AzureSqlInstance cmdlet’ine DnsZonePartner parametresi eklendi.
* Get-AzSqlDatabaseSecureConnectionPolicy cmdlet’i kullanım dışı bırakıldı
* Gelişmiş Tehdit Koruması için Tehdit Algılama cmdlet’leri yeniden adlandırıldı
* New-AzSqlInstance - StorageSizeInGB ve -LicenseType parametreleri artık isteğe bağlı.

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp ve Set-AzWebAppSlot, WebApp özelliğiyle kullanıldığında etiketlerin kaldırılmasına neden olan sorun giderildi

## <a name="210---may-2019"></a>2.1.0 - Mayıs 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Genel Kapsamda ve API Kapsamında tanılamaları yönetmek için yeni Cmdlet'ler oluşturuldu
    - **Get-AzApiManagementDiagnostic** - Genel kapsam veya API Kapsamında yapılandırılan tanılamaları alır
    - **New-AzApiManagementDiagnostic** - Genel kapsamda veya API Kapsamında yeni tanılama oluşturur
    - **New-AzApiManagementHttpMessageDiagnostic** - Üst Bilgileri günlüğe kaydetme ve Gövde Baytları boyutu için tanılama ayarı oluşturur
    - **New-AzApiManagementPipelineDiagnosticSetting** - Ağ Geçidinde gelen/giden HTTP iletileri için Tanılama ayarları oluşturur.
    - **New-AzApiManagementSamplingSetting** - Tanılamaya yönelik istekler/yanıtlar için Örnekleme Ayarı oluşturur
    - **Remove-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama varlığını kaldırır
    - **Set-AzApiManagementDiagnostic** - Genel kapsamda veya API kapsamında tanılama Varlığını güncelleştirir
* ApiManagement hizmetinde Önbellek yönetimi için yeni Cmdlet'ler oluşturuldu
    - **Get-AzApiManagementCache** - Tanımlayıcı tarafından belirtilen Önbelleğin veya tüm önbelleklerin ayrıntılarını alır
    - **New-AzApiManagementCache** - Yeni bir 'varsayılan' Önbellek veya belirli bir azure 'bölgesinde' Önbellek oluşturur
    - **Remove-AzApiManagementCache** - Önbelleği kaldırır
    - **Update-AzApiManagementCache** - Önbelleği güncelleştirir
* API Şemasını yönetmek için yeni Cmdlet'ler oluşturuldu
    - **New-AzApiManagementSchema** - API için yeni Şema oluşturur
    - **Get-AzApiManagementSchema** - API'de yapılandırılan şemaları alır
    - **Remove-AzApiManagementSchema** - API'de yapılandırılan şemaları kaldırır
    - **Set-AzApiManagementSchema** - API'de yapılandırılan şemayı güncelleştirir
* Kullanıcı Belirteci oluşturmak için yeni Cmdlet oluşturuldu. 
    - **New-AzApiManagementUserToken** - Varsayılan olarak 8 saat geçerli kalan yeni bir Kullanıcı Belirteci oluşturur. 'GIT' kullanıcısı için bu cmdlet kullanılarak Belirteç oluşturulabilir./
* Ağ Durumunu almak için yeni cmdlet oluşturuldu
    - **Get-AzApiManagementNetworkStatus** - API Management hizmetinin bağımlı olduğu kaynakların bağlantısında ağ durumunu alır. ApiManagement hizmeti Sanal Ağa dağıtılırken ve bağımlılıklardan herhangi birinin bozulup bozulmadığı denetlenirken bu cmdlet yararlı olur.
* **New-AzApiManagement** cmdlet'i ApiManagement hizmetini yönetecek şekilde güncelleştirildi 
    - Yeni 'Consumption' SKU'su için destek eklendi
    - 'Consumption' SKU'sunda 'EnableClientCertificate' bayrağını etkinleştirmek için destek eklendi
    - Yeni **New-AzApiManagementSslSetting** cmdlet'i 'Backend' ve 'Frontend'de 'TLS/SSL' ayarını yapılandırmaya olanak tanır. Bu cmdlet ApiManagement hizmetinin 'Frontend'inde '3DES' gibi 'Ciphers' yapılandırması ve 'Http2' gibi 'ServerProtocols' yapılandırması için de kullanılabilir.
    - ApiManagement hizmetinde 'DeveloperPortal' ana bilgisayar adının yapılandırması için destek eklendi.
* **Get-AzApiManagementSsoToken** cmdlet'leri giriş olarak 'PsApiManagement' nesnesini alacak şekilde güncelleştirildi
* Cmdlet satır içinde Hata İletileri görüntüleyecek şekilde güncelleştirildi 
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hata Kodu: ValidationError Hata İletisi: Bir veya birden çok alan yanlış değerler içeriyor: Hata Ayrıntıları:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]
* **Export-AzApiManagementApi** cmdlet'i API'leri 'OpenApi 3.0' biçiminde dışarı aktaracak şekilde güncelleştirildi
* **Import-AzApiManagementApi** cmdlet'i güncelleştirildi
    - 'OpenApi 3.0' belge belirtiminden Api'yi içeri aktarmak için
    - Herhangi bir ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') belgesinde belirtilen 'PsApiManagementSchema' özelliğini geçersiz kılmak için.
    - Herhangi bir belgede belirtilen 'ServiceUrl' özelliğini geçersiz kılmak için.
* **Get-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak döndürecek şekilde güncelleştirildi
* **Set-AzApiManagementPolicy** cmdlet'i ilkeyi 'rawxml' kullanarak Non-Xml kaçışlı 'format' olarak ve 'xml' kullanarak Xml kaçışlı kabul edecek şekilde güncelleştirildi
* **New-AzApiManagementApi** cmdlet'i güncelleştirildi 
    - API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.
    - 'ApiVersionSet' içinde API oluşturmak için
    - 'SourceApiId' ve 'SourceApiRevision' kullanıp API'yi kopyalamak için.
    - Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği. 
* **Set-AzApiManagementApi** cmdlet'i güncelleştirildi
    - API'yi 'OpenId' yetkilendirme sunucusuyla yapılandırmak için.
    - API'yi 'ApiVersionSet' olarak güncelleştirmek için    
    - Api kapsamında 'SubscriptionRequired' yapılandırabilme özelliği. 
* **New-AzApiManagementRevision** cmdlet'i güncelleştirildi
    - 'SourceApiRevision' kullanarak mevcut düzeltmeyi kopyalamak (etiketleri, ürünleri, işlemleri ve ilkeleri kopyalamak) için. Yeni Düzeltme üst öğenin 'ApiId' değerini varsayılan olarak alır.
    - 'ApiRevisionDescription' sağlamak için
    - API kopyalanırken 'ServiceUrl' değerini geçersiz kılmak için.
* **New-AzApiManagementIdentityProvider** cmdlet'i güncelleştirildi
    - 'AAD' veya 'AADB2C'yi bir 'Authority' ile yapılandırmak için
    - 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' ve 'PasswordResetPolicy' ayarlamak için
* **New-AzApiManagementSubscription** cmdlet'i güncelleştirildi
    - 'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için
    - 'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için
    - Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.
* **Set-AzApiManagementSubscription** cmdlet'i güncelleştirildi
    - 'Scope' ve 'UserId' kullanarak yeni SubscriptonModel'i hesaba katmak için
    - 'ProductId' ve 'UserId' kullanarak eski abonelik modelini hesaba katmak için
    - Abonelik düzeyinde 'AllowTracing' özelliğini etkinleştirmek için destek eklendi.
* Aşağıdaki cmdlet'ler giriş olarak 'ResourceId' kabul edecek şekilde güncelleştirildi
    - 'New-AzApiManagementContext'
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - 'Get-AzApiManagementApiRelease'
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - 'Get-AzApiManagementApiVersionSet'
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - 'Get-AzApiManagementAuthorizationServer'
    - 'Get-AzApiManagementBackend'
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - 'Get-AzApiManagementCertificate' 
    - 'Remove-AzApiManagementApiVersionSet'
    - 'Remove-AzApiManagementSubscription'

#### <a name="azautomation"></a>Az.Automation
* Get-AzAutomationJobOutputRecord, JSON ve Text kayıt değerlerini işleyecek şekilde güncelleştirildi.
    - https://github.com/Azure/azure-powershell/issues/7977 sorunu düzeltildi
    - https://github.com/Azure/azure-powershell/issues/8600 sorunu düzeltildi
* Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.
    * https://github.com/Azure/azure-powershell/issues/8347 sorunu düzeltildi
* Get-AzAutomationDscNode için -Name kullanıldığında tüm düğümlerin döndürülmesi sorunu düzeltildi. Artık yalnızca eşleşen düğüm döndürülüyor.

#### <a name="azcompute"></a>Az.Compute
* Update-AzVmssVM cmdlet'ine ProtectFromScaleIn ve ProtectFromScaleSetAction parametreleri eklendi.
* New-AzVM basit parametre kümesi artık 'East US' desteklenmiyorsa varsayılan olarak kullanılabilir bir konumu kullanıyor

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* ADLS sdk'si azure çerçevesiyle httpclient, tümleşik veri düzlemi testi kullanacak şekilde güncelleştirildi

#### <a name="azmonitor"></a>Az.Monitor
* Yardım örneklerindeki yanlış parametre adları düzeltildi

#### <a name="aznetwork"></a>Az.Network
* Etkin Yol Tablosu çıkışına DisableBgpRoutePropagation bayrağı eklendi
    - Şu cmdlet güncelleştirildi:
        - Get-AzEffectiveRouteTable
* New-AzApplicationGatewayTrustedRootCertificate belgelerindeki çift tire düzeltildi

#### <a name="azresources"></a>Az.Resources
* Reddetme atamalarını almak için yeni Get-AzureRmDenyAssignment cmdlet'i eklendi

#### <a name="azsql"></a>Az.Sql
* Gelişmiş Tehdit Koruması (Advanced Threat Protection) cmdlet'leri Gelişmiş Veri Güvenliği (Advanced Data Security) olarak yeniden adlandırıldı ve varsayılan olarak Güvenlik Açığı Değerlendirmesi etkinleştiriliyor

## <a name="200---may-2019"></a>2.0.0 - Mayıs 2019
#### <a name="azaccounts"></a>Az.Accounts
* Kullanıcı adı/parola kimlik doğrulamasıyla ilişkili ADFS sorunlarını düzeltmek için Authentication Library’i güncelleştirin

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Yalnızca Bing Arama Hizmetleri için Bing bildirimini görüntüleyin.
* Hesap oluşturma başarısız olduğunda hata iletisini geliştirin.

#### <a name="azcompute"></a>Az.Compute
* Yakınlık yerleştirme grubu özelliği.
    - Aşağıdaki yeni cmdlet’ler eklendi:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Yeni ProximityPlacementGroupId parametresi aşağıdaki cmdlet'lere eklendi:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* StorageAccountType parametresi New-AzGalleryImageVersion öğesine eklendi.
* New-AzGalleryImageVersion komutunun TargetRegion parametresi StorageAccountType içerebilir.
* SkipShutdown anahtar parametresi Stop-AzVM ve Stop-AzVmss öğelerine eklendi       
* Yeni değişiklikler
    - Set-AzVMBootDiagnostics, Set-AzVMBootDiagnostic olarak değiştirildi.
    - Export-AzLogAnalyticThrottledRequests, Export-AzLogAnalyticThrottledRequests olarak değiştirildi.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Azure Deployment Manager cmdlet’lerinin Genel Kullanıma sunulan ilk sürümü

#### <a name="azdns"></a>Az.Dns
* Otomatik DNS NameServer Temsilcisi
    - Create DNS zone cmdlet’i üst bölge adını isteğe bağlı bir ek parametre olarak kabul eder.
    - Yeni oluşturulan alt bölge için NS kayıtlarını üst bölgeye ekler.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Azure FrontDoor cmdlet’lerinin Genel Kullanıma Sunulan ilk sürümü
* WAF cmdlet'lerini 'Waf' içerecek şekilde yeniden adlandırın
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* İki cmdlet kaldırıldı:
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Grant-AzHDInsightHttpServicesAccess, yeni Set-AzHDInsightGatewayCredential cmdlet’i ile değiştirildi
* Okuyucu rolü ile hdinsight işleç rolünü ayırt etmek için Get-AzHDInsightJobOutput cmdlet’ini güncelleştirin:
    - Okuyucu rolüne sahip kullanıcıların, 'DefaultStorageAccountKey' parametresini açıkça belirtmesi gerekir, aksi takdirde hata oluşur.
    - hdinsight işleç rolüne sahip kullanıcılar bu durumdan etkilenmez.

#### <a name="azmonitor"></a>Az.Monitor
* SQR API (Zamanlanmış Sorgu Kuralı) için yeni cmdlet'ler  
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - SQR API hakkında [daha fazla](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) bilgi
    - Az.Monitor.md, GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için cmdlet'leri içerecek şekilde güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* Nat Gateway Resource için destek ekleyin
    - Yeni cmdlet’ler
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Cmdlet'ler güncelleştirildi
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Özellik için aşağıdaki komutlar güncelleştirildi: Brooklyn Gateway üzerinde özel yollar ayarlama/kaldırma.
    - New-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.
    - Set-AzVirtualNetworkGateway güncelleştirildi: Adres ön eklerini Gateway’de ayarlanacak özel yol olarak belirlemek için isteğe bağlı -CustomRoute parametresi eklendi.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* İlke değerlendirme ayrıntılarını sorgulama desteği.
    - Get-AzPolicyState komutuna '-Expand' parametresini ekleyin. '-Expand PolicyEvaluationDetails' öğesini destekleyin.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Abonelikler arası Azure'dan Azure’a konum kurtarma desteği.
* Azure Site Recovery için yaklaşan hataya neden olan değişiklikleri işaretleme.
* Azure Site Recovery kurtarma planı ve eylem planı için düzeltme.
* Azure'dan Azure'a Azure Site Recovery Güncelleştirmesi ağ eşlemesi için düzeltme.
* Yönetilen diske yönelik Azure'dan Azure'a Azure Site Recovery güncelleştirmesi koruma yönü için düzeltme.
* Diğer küçük düzeltmeler.

#### <a name="azrelay"></a>Az.Relay
* Müşteriye dönük iletilerdeki yazım hatalarını düzeltin

#### <a name="azservicebus"></a>Az.ServiceBus
* Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi

#### <a name="azstorage"></a>Az.Storage
* Storage Client Library 10.0.1 sürümüne güncelleştirin (bu SDK’daki tüm nesnelerin 'Microsoft.WindowsAzure.Storage. *' ad alanı, 'Microsoft.Azure.Storage.* ' olarak değiştirilir)
* Yeni 2019-04-01 API sürümünü desteklemek için Microsoft.Azure.Management.Storage 11.0.0 sürümüne güncelleştirin.
* Depolama hesabı oluştur komutundaki varsayılan 'Storage' Depolama hesabı Türü 'StorageV2' olarak değişir
    - New-AzStorageAccount
* 'StandardLRS' öğesinin 'Standard_LRS' olarak değiştirilmesi gibi, '-' ekleyerek Sku.Name Depolama hesabı cmdlet çıkışını giriş SkuName ile hizalanacak şekilde değiştirin
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* 'Kind' özelliği artık Get-AzWebApp tarafından döndürülen PSSite nesneleri için ayarlanır
* Get-AzWebApp*Metrics ve Get-AzAppServicePlanMetrics, kullanım dışı olarak işaretlendi

## <a name="180---april-2019"></a>1.8.0 - Nisan 2019
### <a name="highlights-since-the-last-major-release"></a>Son ana sürümden bu yana öne çıkanlar
* `Az` modülünü genel kullanıma sunuldu
* `Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce
* Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
* Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi
* Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi
* Az.Automation'da Python 2 runbook'ları için destek eklendi
* Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler

#### <a name="azaccounts"></a>Az.Accounts
* Mac’te modülleri doğru bir biçimde silmek için Uninstall-AzureRm güncelleştirildi

#### <a name="azbatch"></a>Az.Batch
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azcdn"></a>Az.Cdn
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azcompute"></a>Az.Compute
* Disklerin kaynak kimlikleri kaynak kimliğinde küçük harfli kaynak grubu içerdiğinde oluşan AEM yüklemesiyle ilgili sorun düzeltildi
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="azdatafactory"></a>Az.DataFactory
* Yönetilen tümleştirme çalışma zamanı için Nodecount’ın null olmadığı durumlar için SsisProperties eklendi.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azeventgrid"></a>Az.EventGrid
* Oluşturma/güncelleştirme etkinliği için abonelik cmdlet’lerini kullanmadan önce kaynakların oluşturulmasının gerektiğini belirten yardım metni güncelleştirildi.

#### <a name="azeventhub"></a>Az.EventHub
* Ad alanının NetworkRuleSet’i için yeni cmdlet’ler eklendi 

#### <a name="azhdinsight"></a>Az.HDInsight
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="aziothub"></a>Az.IotHub
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azkeyvault"></a>Az.KeyVault
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azmedia"></a>Az.Media
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azmonitor"></a>Az.Monitor
  * GenV2 (klasik olmayan) ölçüm tabanlı uyarı kuralı için yeni cmdlet'ler
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * İzleyici SDK’sı 0.22.0-önizleme sürümüne güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Azure VM'de SQL için güncelleştirilmiş tablo biçimi
* AzureFileShare’de konumu getirmeye yönelik alternatif yöntem eklendi
* SchedulePolicy nesnesindeki ScheduleRunDays saat dilimine göre güncelleştirildi

#### <a name="azrediscache"></a>Az.RedisCache
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.

#### <a name="azresources"></a>Az.Resources
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="azsql"></a>Az.Sql
* İzleyici SDK’sının bağımlılığı ortak kod ile değiştirildi
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Birden fazla sütun sınıflandırma işlemi geliştirildi.
* Get-AzSqlServerServiceObjective’den alınan yanıta SKU özellikleri (SKU adı, ailesi, kapasitesi) dahil edildi ve bunlar varsayılan olarak tablo şeklinde biçimlendirildi.
* Bölgede önceden var olan bir sunucuya ihtiyaç duymadan, konuma göre Get-AzSqlServerServiceObjective yapabilme olanağı eklendi.
* Yönetilen Örnek oluşturmadaki saat dilimi parametresi desteği.
* Joker karakterlere ilişkin belgeler düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp ve Set-AzWebAppSlot çalıştırılırken etiketlerin kaldırılmaması sorunu düzeltildi
* Çoğul isimli cmdlet’ler tekil isimli olarak güncelleştirildi ve çoğul isimler kullanım dışı bırakıldı.
* Web siteleri SDK'sı güncelleştirildi.
* PSAppServicePlan’den AdminSiteName özelliği kaldırıldı.

## <a name="170---april-2019"></a>1.7.0 - Nisan 2019
### <a name="highlights-since-the-last-major-release"></a>Son ana sürümden bu yana öne çıkanlar
* `Az` modülünü genel kullanıma sunuldu
* `Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce
* Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
* Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi
* Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi
* Az.Automation'da Python 2 runbook'ları için destek eklendi
* Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler

#### <a name="azaccounts"></a>Az.Accounts
* Add-AzEnvironment ve Set-AzEnvironment, AzureAnalysisServicesEndpointResourceId parametresini kabul edecek biçimde güncelleştirildi

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Veri düzlemi cmdlet’lerinde ServiceClient kullanma ve orijinal kimlik doğrulaması mantığını kaldırma
* Hataya neden olan değişikliklerden kaçınmak için Add-AzureASAccount’ı Connect-AzAccount’ın sarmalayıcısı yapma

#### <a name="azautomation"></a>Az.Automation
* Eklemeler için New-AzAutomationSoftwareUpdateConfiguration cmdlet hatası düzeltildi. IncludedKbNumber ve IncludedPackageNameMask parametrelerinin artık çalışması bekleniyor.
* Azure otomasyonu güncelleştirmesi yönetim dinamik grubu için hata düzeltmesi

#### <a name="azcompute"></a>Az.Compute
* New-AzDiskConfig ve New-AzSnapshotConfig’e HyperVGeneration parametresi eklendi
* Diğer kiracıların karakter görüntüleriyle VM oluşturmaya izin verildi. 

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* New-AzContainerGroup’un -command parametresinde bağımsız boş değişken ekleyen sorun düzeltildi

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK’sı 3.0.2 sürümüne güncelleştirildi
* Set-AzDataFactoryV2 cmdlet’i RepoConfiguration ile ilgili ayarların ek parametreleriyle güncelleştirildi.

#### <a name="azresources"></a>Az.Resources
* '-ResourceId' veya '-ResourceGroupName', '-Name' ve '-ResourceType' parametreleri sağlanırken ‘Get-AzResource’ için sağlayıcıların işlenmesi geliştirildi
* ‘Test-AzDeployment’ ve ‘Test-AzResourceGroupDeployment’ için hata işleme geliştirildi
    - İşleme hataları dağıtım doğrulamasının dışında tutuldu ve komut çıkışına dahil edildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856
* Betik ve iş senaryolarında istemi atlamak için bir dizi dağıtım cmdlet’lerine ‘-IgnoreDynamicParameters’ anahtar parametresi eklendi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* Veritabanı Verileri Sınıflandırması Desteği.

#### <a name="azstorage"></a>Az.Storage
* -UseConnectedAccount parametresi ile depolama bağlamı oluştururken ayrıntı hatası raporlama
    - New-AzStorageContext
* Belirtilen depolama hesabının Yönetim düzlemi API’si ile Blob Hizmeti Özellikleri için Yönetim Desteği
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Blob ve dosya karşıya yükleme ve indirme cmdlet’leri için -Asjob desteği
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 - Mart 2019
### <a name="highlights-since-the-last-major-release"></a>Son ana sürümden bu yana öne çıkanlar
* `Az` modülünü genel kullanıma sunuldu
* `Az` modülü hakkında daha fazla bilgi için şu bağlantıyı ziyaret edin: https://aka.ms/azps-announce
* Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
* Az.Compute ve Az.Network için Get cmdlet'lerine joker karakter desteği eklendi
* Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi
* Az.Automation'da Python 2 runbook'ları için destek eklendi
* Az.LogicApp: Tümleştirme Hesabı Derlemeleri ve Toplu Yapılandırması için yeni cmdlet’ler

#### <a name="azautomation"></a>Az.Automation
* Aşağıdaki yeni özellikleri desteklemek için Azure otomasyonu güncelleştirme yönetimi değişikliği:
    * Dinamik gruplandırma
    * Ön-Son betik
    * Yeniden Başlatma Ayarı

#### <a name="azcompute"></a>Az.Compute
* Get-AzVmBootDiagnosticsData içinde yol çözümleme sorunu çözüldü
* İşlem istemci kitaplığı 25.0.0'a güncelleştirildi.

#### <a name="azkeyvault"></a>Az.KeyVault
* KeyVault cmdlet'lerine joker karakter desteği eklendi

#### <a name="aznetwork"></a>Az.Network
* Azure Güvenlik Duvarı için Tehdit Bilgileri desteği eklendi
* Application Gateway Güvenlik Duvarı İlkesi üst düzey kaynağı ve Özel Kurallar eklendi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Anında RP desteği için Azure VM ilkesine SnapshotRetentionInDays eklendi
* Kapsayıcı kaydını kaldırmak için kanal desteği eklendi

#### <a name="azresources"></a>Az.Resources
* Get-AzResource ve Get-AzResourceGroup için joker karakter desteği güncelleştirildi
* ARM'ye genel çağrı yapılırken kullanılan kimlik bilgileri güncelleştirildi

#### <a name="azsql"></a>Az.Sql
* Yeni DetectionType'lar eklendiğinde gelecekte kullanılabilmesini sağlamak ve otomatik tamamlamayı da desteklemek için Tehdit Algılama cmdlet'lerinin DetectionType olan parametresi (ExcludeDetectionType) string[] olarak değiştirildi.

#### <a name="azstorage"></a>Az.Storage
* Depolama hesabında Yönetim İlkesini Alma/Ayarlama/Kaldırma desteği
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* 'New-AzWebApp -IncludeSourceWebAppSlots' kullanarak tüm yuvaların kopyalanmasını kesintiye uğratan ARM şablon hatası düzeltildi 

## <a name="150---march-2019"></a>1.5.0 - Mart 2019
#### <a name="azaccounts"></a>Az.Accounts
* AutoRest tarafından oluşturulan cmdlet’leri desteklemek için 'Register-AzModule' komutu eklendi
* Connect-AzAccount örnekleri güncelleştirildi

#### <a name="azautomation"></a>Az.Automation
* Birden fazla Azure Otomasyonu cmdlet’inde belirli aylık zamanlamalar alınırken yaşanan sorun düzeltildi
* Yalnızca ilk 20 düğümü döndüren Get-AzAutomationDscNode düzeltildi. Artık tüm düğümleri döndürür

#### <a name="azcdn"></a>Az.Cdn
* Özel Etki Alanı Https Etkinleştirmesi/Devre Dışı Bırakması için yeni PowerShell cmdlet’leri eklendi ve eskiler kullanım dışı bırakıldı

#### <a name="azcompute"></a>Az.Compute
* Get cmdlet’lerine joker karakter desteği eklendi

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK sürümü 3.0.1'e güncelleştirildi

#### <a name="azlogicapp"></a>Az.LogicApp
* Yalnızca ilk sonuç sayfasını getiren ListWorkflows için düzeltme

#### <a name="aznetwork"></a>Az.Network
* Network cmdlet’lerine joker karakter desteği eklendi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Azure VM desteğine SQL Server eklendi
* SDK Güncelleştirmesi
* Get-ProtectableItem içindeki Removed VMappContainer denetimi kaldırıldı
* Get-ProtectableItem için Name ve ServerName parametreleri eklendi

#### <a name="azresources"></a>Az.Resources
* Dağıtım cmdlet’lerine `-TemplateObject` parametresi eklendi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2933
* `Get-AzResource` sonucu `Set-AzResource` üzerine aktarılırken oluşan sorun düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8240
* `Set-AzResource` çalıştırılırken JSON veri türü değişikliğine neden olan sorun düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* AuditingEndpointsCommunicator güncelleştiriliyor.
    - Yeni tanılama ayarları oluşturulurken kenar durumunun davranışı düzeltiliyor.

#### <a name="azstorage"></a>Az.Storage
* Depolama hesabı oluşturulurken Support Kind BlockBlobStorage desteği sağlandı      - New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 - Şubat 2019
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* AddAzureASAccount cmdlet'i kullanım dışı bırakıldı

#### <a name="azautomation"></a>Az.Automation
* Import-AzAutomationDscNodeConfiguration için yardım güncelleştirildi
* Import-AzAutomationDscConfiguration cmdlet'ine yapılandırma adı doğrulaması eklendi
* Import-AzAutomationDscConfiguration cmdlet'i için hata işleme iyileştirildi

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Kaynağın alt etki alanını belirtmek amacıyla kullanılan New-AzCognitiveServicesAccount için CustomSubdomainName adlı, isteğe bağlı, yeni bir parametre eklendi.

#### <a name="azcompute"></a>Az.Compute
* Kimlik parametresi kümeleriyle ilgili sorun düzeltildi
* Get-AzVMExtension, Name parametresi sağlanmadığında yüklü tüm uzantıları listeleyecek şekilde güncelleştirildi
* Update-AzImage cmdlet’ine Tag ve ResourceId parametreleri eklendi
* Get-AzVmssVM, örnek kimliği olmadan ve InstanceView ile, örnek görünümüne sahip VMSS VM’lerini listeleyebilir.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* ADL silinmiş öğe listeleme ve geri yükleme cmdlet’leri eklendi

#### <a name="azeventhub"></a>Az.EventHub
* EventHub’ın CaptureDescription sınıfında Boş Arşivleri Atlamak için SkipEmptyArchives adlı yeni Boole özelliği eklendi 

#### <a name="azkeyvault"></a>Az.KeyVault
* Set-AzKeyVaultSecret’daki etiketleme düzeltildi

#### <a name="azlogicapp"></a>Az.LogicApp
* Tümleştirme Hesapları için Temel SKU eklendi
* XSLT 2.0, XSLT 3.0 ve Liquid Eşleşme Türleri eklendi
* Tümleştirme Hesabı Bütünleştirilmiş Kodları için yeni cmdlet’ler
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* Tümleştirme Hesabı Toplu Yapılandırması için yeni cmdlet’ler
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* Logic Apps SDK sürüm 4.1.0’a güncelleştirildi

#### <a name="azmonitor"></a>Az.Monitor
* Get-AzMetric için yardım güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* Add-AzApplicationGatewayCustomError için yardım örneği güncelleştirildi

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* New ve Get ApplicationInsights veri kaynağı için ek destek sunuldu.
    - Belirli bir çalışma alanı için belirli ve tüm Get ApplicationInsights veri kaynaklarını desteklemek için yeni ‘ApplicationInsights’ türü eklendi. 
    - Belirli Application-Insights kaynak parametrelerine (abonelik kimliği, resourceGroupName ve ad) göre veri kaynağı oluşturmak için New-AzOperationalInsightsApplicationInsightsDataSource cmdlet’i eklendi. 

#### <a name="azresources"></a>Az.Resources
* https://github.com/Azure/azure-powershell/issues/8166 sorunu düzeltildi
* https://github.com/Azure/azure-powershell/issues/8235 sorunu düzeltildi
* https://github.com/Azure/azure-powershell/issues/6219 sorunu düzeltildi
* KeyCredentials’ın tekrar oluşturmasını engelleyen hata düzeltildi

#### <a name="azsql"></a>Az.Sql
* SQL DB Hiper Ölçek katmanı için destek eklendi
* Geri yükleme isteğinde gereksiz özellikler ayarlandığı için geri yüklemenin başarısız olmasına yol açan hata düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* Get-AzWebAppSlotMetrics örneği düzeltildi

## <a name="130---february-2019"></a>1.3.0 - Şubat 2019
#### <a name="azaccounts"></a>Az.Accounts
* En son ClientRuntime sürümüne güncelleştirme

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Az.AnalysisServices modülü için genel kullanılabilirlik.

#### <a name="azcompute"></a>Az.Compute
* AEM uzantısı: UltraSSD ile P60,P70 ve P80 diskleri için destek eklendi
* Set-AzVMBootDiagnostics yardım açıklaması güncelleştirildi
* Update-AzImage için yardım açıklaması ve örnek güncelleştirildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Az.RecoveryServices modülü için genel kullanılabilirlik.

#### <a name="azresources"></a>Az.Resources
* Kaynak grupları için etiketleme düzeltildi 
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8166
* `Get-AzureRmRoleAssignment` komutunun -ErrorAction'a uymama sorunu düzeltildi 
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy
* Azure hesabında oturum açılmamasının SQL cmdlet'leri yürütülürken nullref özel durumuna yol açması sorunu düzeltildi
* Get-AzSqlCapability'de null başvuru özel durumu düzeltildi

## <a name="121---january-2019"></a>1.2.1 - Ocak 2019
#### <a name="azaccounts"></a>Az.Accounts
* Kimlik Doğrulaması'nın doğru yayınını içeren sürümü

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Güncelleştirilmiş Kimlik Doğrulaması bağımlılığını içeren sürüm

## <a name="120---january-2019"></a>1.2.0 - Ocak 2019
#### <a name="azaccounts"></a>Az.Accounts
* Yalnızca Windows PowerShell 5.1 için etkileşim ve kullanıcı adı/parola kimlik doğrulaması eklendi
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi
* Uninstall-AzureRm için PC Çekirdeğine uyarı iletisi eklendi

#### <a name="azaks"></a>Az.Aks
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azautomation"></a>Az.Automation
* Python 2 runbook'ları için destek eklendi
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azcdn"></a>Az.Cdn
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azcompute"></a>Az.Compute
* Invoke-AzVMReimage cmdlet'i eklendi
* Set-AzVmss'ye TempDisk parametresi eklendi
* New-AzVM'nin uyarı iletisi düzeltildi

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK sürümü 3.0.0'a güncelleştirildi

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* MSI kullanırken ADLS uç noktasındaki sorun düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7462
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="aziothub"></a>Az.IotHub
* Add-IotHubRoutingEndpoint cmdlet'ine Kodlama biçimi eklendi.

#### <a name="azkeyvault"></a>Az.KeyVault
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="aznetwork"></a>Az.Network
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azresources"></a>Az.Resources
* 'New-AzADAppCredential' ve 'New-AzADSpCredential' başvuru belgelerindeki hatalı örnekler düzeltildi
* Kaynak grubu dağıtım cmdlet'lerini yürütmeden önce '-TemplateFile' parametresi yolunun çözülmemesi sorunu düzeltildi
* Az.Resources: Belgede New-AzureRmPolicyDefinition -Mode varsayılan değeri düzeltildi
* Az.Resources: https://github.com/Azure/azure-powershell/issues/7522 sorunu düzeltildi
* Az.Resources: https://github.com/Azure/azure-powershell/issues/5747 sorunu düzeltildi
* 'PSResourceGroupDeployment' nesnesinin biçimlendirme sorunu düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* VMSS modeline sertifika eklendiğinde ama özel durum oluştuğunda geri alma için hata düzeltmesi: https://github.com/Azure/service-fabric-issues/issues/932
* Bazı hata iletileri düzeltildi.
* Az geçişinde çalışmayan New-AzServiceFabriCluster için varsayılan ARM şablonuyla küme oluşturma sorunu düzeltildi.
* Uzantıda küme kimliği denetlenerek küme/uygulama sertifikasının yalnızca kümeye karşılık gelen VM Ölçek Kümelerine eklenmesi düzeltildi.

#### <a name="azsignalr"></a>Az.SignalR
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azsql"></a>Az.Sql
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi
* LicenseType parametresinin parametre açıklaması olası değerlerle güncelleştirildi
* Yönetilen örnek kimliği güncelleştirmesinin, güncelleştirilen tek özellik bu olduğunda çalışmaması sorunu düzeltildi
* Yönetilen örnekte özel harmanlama desteği

#### <a name="azstorage"></a>Az.Storage
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi
* Premium Depolama Hesabı klasik Günlük/Ölçüm desteği sağlamadığından, Premium Depolama Hesabında klasik Günlük/Ölçüm için get/set komutları kullanıldığında ayrıntılı hata iletisi veriliyor.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi

#### <a name="azwebsites"></a>Az.Websites
* Hatalı çevrimiçi yardım URL'leri güncelleştirildi
* Uygulama ASE'de barındırılıyorsa, sertifikayı doğru kaynak grubuna ve konuma yüklemek için 'New-AzWebAppSSLBinding' düzeltildi.
* SSL sertifikası bir uygulamaya bağlanırken etiketlerin üzerine yazılmaması için 'New-AzWebAppSSLBinding' düzeltildi

## <a name="110---january-2019"></a>1.1.0 - Ocak 2019
#### <a name="azaccounts"></a>Az.Accounts
* Enable-AzureRmAlias cmdlet'ine 'Local' Kapsamı eklendi

#### <a name="azcompute"></a>Az.Compute
* Restart/Start/Stop/Remove/Set-AzVM ve Save-AzVMImage için ayarlanan ID parametresinde ad artık isteğe bağlı
* Yardım dosyalarında ID parametresinin açıklaması güncelleştirildi
* Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* SDK düzeltmeleri için veri düzleminin SDK sürümü 1.1.14 olarak güncelleştirildi.
    - getfilestatus ve liststatus için negatif acesstime ve modificationtime değerlerini işleme yöntemi düzeltildi, async iptal belirteci düzeltildi

#### <a name="azeventgrid"></a>Az.EventGrid
* 2019-01-01 API sürümünü kullanmak için güncelleştirildi.
* Aşağıdaki cmdlet'ler 2019-01-01 API sürümünde yeni senaryoyu destekleyecek şekilde güncelleştirildi
    - New-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:
        - Olay Yaşam Süresi,
        - Olaylar için teslim girişimleri sayısı üst sınırı,
        - Teslim edilemeyen ileti uç noktası.
    - Update-AzureRmEventGridSubscription: Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:
        - Olay Yaşam Süresi,
        - Olaylar için teslim girişimleri sayısı üst sınırı,
        - Teslim edilemeyen ileti uç noktası.
* New-AzureRmEventGridSubscription ve Update-AzureRmEventGridSubscription cmdlet'lerinde EndpointType seçeneği için yeni enum değerleri (storageQueue ve hybridConnection) eklendi.
* Olay aboneliğini oluşturma veya güncelleştirme işleminde kullanıcının el ile bir eylem yapması beklendiğinde uyarı iletisi gösteriliyor.

#### <a name="aziothub"></a>Az.IotHub
* IotHub SDK'sı en son sürümüne güncelleştirildi

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzLogicApp, Name değeri belirtilmemiş olanların tümünü listeliyor

#### <a name="azresources"></a>Az.Resources
* 'Get-AzResource' için '-ODataQuery' ve '-ResourceId' parametreleri sağlanırken ortaya çıkan parametre ayarlama sorunu düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/7875
* New/Set-AzPolicyDefinition cmdlet'lerinde -Custom parametresinin işlenmesi düzeltildi
* New-AzDeployment belgelerindeki yazım hatası düzeltildi
* 'New-AzADUser' için '-MailNickname' parametresi zorunlu hale getirildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü

#### <a name="azsql"></a>Az.Sql
* Depolama yönetimi istemci bağımlılığı ortak SDK uygulamasına dönüştürüldü.

#### <a name="azstorage"></a>Az.Storage
* Sas Token, OAuth veya Anonymous ile oluşturulduğunda Storage bağlamının StorageAccountName değeri gerçek Depolama Hesabı Adına ayarlanıyor
    - New-AzStorageContext
* Blob Anlık Görüntü Nesnesinin Sas Belirteci '-FullUri' parametresiyle oluşturulduğunda, döndürülen Uri anlık görüntü Uri'si olacak şekilde düzeltildi
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* 'Get-AzDeletedWebApp' cmdlet'indeki tarih ayrıştırma hatası düzeltildi
* Az.Accounts modülündeki geriye dönük uyumluluk sorunu çözüldü

## <a name="100---december-2018"></a>1.0.0 - Aralık 2018
### <a name="general"></a>Genel

- Az Modülü Genel Kullanıma Sunuldu
- Her modül için çevrimiçi yardım
- Diğer ayrıntılar ve yol haritası için bkz. [Az Duyuru Sayfası](https://aka.ms/azps-announce)
- AzureRM’den geçiş hakkında bilgi edinmek için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azaccounts"></a>Az.Accounts
- Önceki adı: Az.Profile
- Profil ve bağlam türleri için tablo biçimleri düzeltildi

### <a name="azapimanagement"></a>Az.ApiManagement
- #7002 düzeltmeleri
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azbatch"></a>Az.Batch
- `PSComputeNode` üzerinde yeni `NodeAgentInformation` aracılığıyla bir havuzdaki her bir VM’de Azure Batch Düğüm Aracısı’nın hangi sürümünün çalıştığını görme olanağı eklendi.
- `PSDataDisk` için `Caching` varsayılan ayarı artık `None` yerine `ReadWrite`.
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azbilling"></a>Az.Billing
- Billing, Consumption ve UsageAggregates cmdlet’lerini birleştirir, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azcognitivservices"></a>Az.CognitivServices
- New-AzureRmCognitiveServicesAccount işleminde kullanılabilen SkuName ve Typem için tamamlayıcılar eklendi
- Get-AzCognitiveServicesAccountSkus cmdlet’inden GetSkusWithAccountParamSetName parametresi kaldırıldı

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- ManagedIdentity desteği eklendi

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azmonitor"></a>Az.Monitor
- Az.Insights cmdlet’inin adı Az.Monitor olarak değiştirildi ve başka yeni değişiklikler yapıldı, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azkeyvault"></a>Az.KeyVault
- Çıkış türlerinden kullanım dışı 'PurgeDisabled' özelliği kaldırıldı

### <a name="azmachinelearning"></a>Az.MachineLearning
- Az.MachineLearningCompute modülünden cmdlet’ler eklendi

### <a name="azmedia"></a>Az.Media
- New-AzMediaService cmdlet’inden kullanım dışı -Tags diğer adı kaldırıldı

### <a name="aznetwork"></a>Az.Network
Application Gateway’de RewriteRuleSets parametresini yapılandırma desteği eklendi
    - Yeni cmdlet'ler eklendi:
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - Cmdlet’ler isteğe bağlı -RewriteRuleSet parametresiyle güncelleştirildi
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig, Kimlik kullanarak Application Gateway’e KeyVault Desteği ekledi.
    - Cmdlet’ler isteğe bağlı -KeyVaultSecretId, -KeyVaultSecret parametresiyle güncelleştirildi
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - New-AzApplicationGateway cmdlet’i isteğe bağlı -UserAssignedIdentity parametresiyle güncelleştirildi
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azprofile"></a>Az.Profile
- Modül adı Az.Accounts olarak değiştirildi

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azresources"></a>Az.Resources
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azservicefabric"></a>Az.ServiceFabric
- Sertifikayı ortak ad ve parmak iziyle belirtme desteği
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azsignalr"></a>Az.SIgnalR
- SIgnalR için PowerShell cmdlet'leri Genel Kullanıma sunuldu

### <a name="azsql"></a>Az.Sql
- Tehdit Algılama cmdlet’lerine yeni Data_Exfiltration ve Unsafe_Action algılama türleri eklendi
- Sql Denetimi cmdlet'leri için belge örnekleri güncelleştirildi
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azstorage"></a>Az.Storage
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

### <a name="azwebsites"></a>Az.Websites
- Küçük yeni değişiklikler, ayrıntılar için bkz. [Geçiş Kılavuzu](https://aka.ms/azps-migration-guide)

## <a name="070---december-2018"></a>0.7.0 - Aralık 2018

### <a name="general"></a>Genel

* Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler

### <a name="azcompute"></a>Az.Compute

* `New-AzVm(ss)` cmdlet’leri için basit parametre kümelerinde UltraSSD ve Galeri Görüntüleri desteği eklendi.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Adls hesabı etki alanının sonundaki eğik çizgi düzeltildi

### <a name="azfrontdoor"></a>Az.FrontDoor

* Bazı bozuk bağlantılar düzeltildi
    - New-AzureRmFrontDoor ve Set-AzureRmFrontDoor makalelerinde, New-AzureRmFrontDoorHealthProbeSettingObject cmdlet’i makalesinin bağlantısı düzeltildi.
    - New-AzureRmFrontDoorManagedRuleObject makalesinde, New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet’i makalesinin bağlantısı düzeltildi.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Azure Dosya Paylaşımı geri yükleme işlemleri için istemci tarafı doğrulamalar eklendi.
* Afs geri yükleme işlemi için storageAccountName ve storageAccountResourceGroupName isteğe bağlı hale getirildi.

### <a name="azresources"></a>Az.Resources

* [https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7679) düzeltmesi
    - Get-AzureRmRoleAssignment, klasik yöneticiler istenirken sağlanmışsa abonelik kapsamını kullanacak şekilde güncelleştirildi.

### <a name="azsql"></a>Az.Sql

* Yakında gerçekleşecek AzureRM’den Az’ye geçiş süreci için küçük değişiklikler
* Get-AzureRmSqlDatabaseVulnerabilityAssessment cmdlet’inin DotNet core ile kullanılması konusundaki bir sorun düzeltildi
* SQL Denetimi cmdlet’leriyle ilgili yardım iletilerinin belgeleri değiştirildi.

### <a name="azstorage"></a>Az.Storage

* New-AzureRmStorageAccount cmdlet’ine -EnableHierarchicalNamespace eklendi
* -DestContext girilmediğinde Dosya Kopyalama cmdlet’inin hedefte kaynak bağlamını yeniden kullanamamasına yol açan sorun düzeltildi
    - Start-AzureStorageFileCopy
* Statik Web Sitesi yapılandırması için destek eklendi
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp ve Set-AzureRmWebAppSlot 
    - Windows ve Linux kapsayıcı uygulamalarında bağlanacak Azure Depolama yollarının belirtilmesi için yeni parametre (-AzureStoragePath) eklendi. Azure Depolama yollarını ayarlamak için yeni New-AzureRmWebAppAzureStoragePath cmdlet’inin çıktısını bir parametre olarak kullanın.

## <a name="061---november-2018"></a>0.6.1 - Kasım 2018

### <a name="azapimanagement"></a>Az.ApiManagement
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

### <a name="azautomation"></a>Az.Automation
* Swagger tabanlı Azure Otomasyon cmdlet'leri
* Güncelleştirme Yönetimi cmdlet'leri eklendi
* Kaynak Denetimi cmdlet'leri eklendi
* Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi
* DSC Kayıt Düğümü komutu düzeltildi

### <a name="azcompute"></a>Az.Compute
* SystemAssigned kimliği için kimlik sorunu düzeltildi
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Market cmdlet'leri için örnekler açıklaması güncelleştirildi

### <a name="aznetwork"></a>Az.Network
* New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi
* Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi
* Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi. 
* VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.
* İlke saat dilimi büyük harfe dönüştürüldü.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

### <a name="azrelay"></a>Az.Relay
* Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.

### <a name="azresources"></a>Az.Resources
* `New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi
* New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi
* NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703

### <a name="azservicefabric"></a>Az.ServiceFabric
* Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi

### <a name="azsql"></a>Az.Sql
* Azure Sql Veritabanı Yönetilen Örneği ve Azure Sql Yönetilen Veritabanı'nındaki CRUD işlemleri için yeni cmdlet'ler eklendi
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* Sunucuda veya veritabanında Genişletilmiş Denetim İlkesi yönetimi etkinleştirildi.
    - Denetim günlüklerinde filtrelemeyi etkinleştirmek için yeni parametre (PredicateExpression) eklendi.
    - Cmdlet'ler, SQL istemcileri yerine Eski istemcileri kullanacak şekilde değiştirildi.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings cmdlet'inin depolama hesabı ad parametre kümesiyle kullanılmasıyla ilgili sorun düzeltildi

## <a name="050---november-2018"></a>0.5.0 - Kasım 2018
#### <a name="general"></a>Genel
* Birçok temel cmdlet’e Kaynak Tamamlayıcıları eklendi - bunlar cmdlet’leri etkileşimli olarak çağırırken mevcut kaynak adları arasında gezinmenize olanak tanır

#### <a name="azprofile"></a>Az.Profile
* ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi
* Connect-AzAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi
* Connect-AzAccount için TenantId açıklaması güncelleştirildi
* Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi
    - https://github.com/Azure/azure-powershell/issues/6936
* Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/7453
* MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/7462
* Bağlantı olmadığında 'Disconnect-AzAccount' oluşturulmasına neden olan sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Get-AzCognitiveServicesAccountSkus işlemi eklendi.

#### <a name="azcompute"></a>Az.Compute
* Add-AzVmssVMDataDisk ve Remove-AzVmssVMDataDisk cmdlet'leri eklendi
* Get-AzVMImage, AutomaticOSUpgradeProperties gösteriyor
* SetAzVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin Json biçiminde ayarlanmamasıyla ilgili hata düzeltildi.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* DataLake paketi 1.1.10'a güncelleştirildi.
* Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.

#### <a name="azinsights"></a>Az.Insights
* 7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi
    - Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).
* Set-AzDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi
    - Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor

#### <a name="aznetwork"></a>Az.Network
* Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* İlke düzeltme cmdlet'leri eklendi

#### <a name="azresources"></a>Az.Resources
* [https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402) düzeltmesi
    - 'Get-AzResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı

#### <a name="azservicebus"></a>Az.ServiceBus
* PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Linux Vmss'ye sertifika ekleme sorunu düzeltildi.
* 'Add-AzServiceFabricClusterCertificate' düzeltildi
    - Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).
    - Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).
* 'Update-AzServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.

## <a name="040---october-2018"></a>0.4.0 - Ekim 2018
#### <a name="azprofile"></a>Az.Profile
* CloudShell’de Get-AzSubscription sorunu çözüldü
* ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi

#### <a name="azcompute"></a>Az.Compute
* 'New-AzVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi
* Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Sanal Ağ Kuralları desteği ekleme
    - Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.
    - Add-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.
    - Set-AzDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.
    - Remove-AzDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.

#### <a name="aznetwork"></a>Az.Network
* Test-AzNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.
* Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.

#### <a name="azresources"></a>Az.Resources
* Get-AzRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi. Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.

## <a name="030---october-2018"></a>0.3.0 - Ekim 2018
#### <a name="azurestorage"></a>Azure Depolama
* Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.
    - Get-AzStorageUsage
    
#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Mevcut hesap olmadan Get-AzCognitiveServicesAccountSkus desteği.

#### <a name="azcompute"></a>Az.Compute
* Get-AzVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi
* New-AzVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.
* Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.

#### <a name="aznetwork"></a>Az.Network
* NetworkProfile işlevselliği eklendi. yeni cmdlet'ler eklendi
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Alt Ağ Modeline hizmet ilişki bağlantısı eklendi
* New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet'leri eklendi
* Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet'leri eklendi

#### <a name="azrediscache"></a>Az.RedisCache
* Bundan sonra Size parametresi olarak her dizeye izin veriliyor. PSArgumentCompleter açılan listesine P5 eklendi

#### <a name="azresources"></a>Az.Resources
* Set-AzPolicyDefinition'a eksik -Mode parametresi eklendi
* Origin öğesi User içeren işlemler için Get-AzProviderOperation commandlet hatası düzeltildi

#### <a name="azsql"></a>Az.Sql
* Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* Yeni Get-AzWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor
* Yeni New-AzWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor

## <a name="020---september-2018"></a>0.2.0 - Eylül 2018
 İlk Yayın