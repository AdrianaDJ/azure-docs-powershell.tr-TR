---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882650"
---
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
* SQL DB Hiper Ölçeklendirme katmanı için destek eklendi
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