---
title: Azure PowerShell sürüm notları
description: Azure PowerShell modüllerine yönelik en son güncelleştirmeler hakkında bilgi edinin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 656e61e7f208367fc7fae28f73d1b6f289831d77
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427743"
---
# <a name="azure-powershell-release-notes"></a>Azure PowerShell sürüm notları
## <a name="280---october-2019"></a>2.8.0 - Ekim 2019
### <a name="general"></a>Genel
* Az.HealthcareApis 1.0.0 sürümü

#### <a name="azaccounts"></a>Az.Accounts
* Oluşturulan modüller için telemetri ve URL’yi yeniden yazma özelliği güncelleştirildi, Windows birim testleri düzeltildi.

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi** - ApiVersionSet’e Güncelleştirme API’si desteği eklendi
    - [https://github.com/Azure/azure-powershell/issues/10068](https://github.com/Azure/azure-powershell/issues/10068 ) sorunu düzeltildi

#### <a name="azautomation"></a>Az.Automation
* Linux yeniden başlatma ayarı parametresi için New-AzureAutomationSoftwareUpdateConfiguration cmdlet’i düzeltildi.

#### <a name="azbatch"></a>Az.Batch
* Kullanımdan kaldırılan **Get-AzBatchNodeAgentSku** yerine 2.0.0 sürümünde **Get-AzBatchSupportImage** kullanıma sunulacak.

#### <a name="azcompute"></a>Az.Compute
* New-AzVM ve New-AzVmss cmdlet’lerine Priority, EvictionPolicy ve MaxPrice parametreleri eklendi
* Add-AzVMAdditionalUnattendContent ve Add-AzVMSshPublicKey cmdlet’leri için uyarı iletisi ve yardım belgesi düzeltildi
* Set-AzVMDiskEncryptionExtension için yönetilen diskleri olan Linux VM’lere yönelik -skipVmBackup özel durumu düzeltildi.
* Set-AzVMDiskEncryptionExtension’daki iki geçişli senaryoda güncelleştirme şifreleme ayarlarındaki hata düzeltildi.

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF V2 veri akışı için CRUD komutları eklendi: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, ve Get-AzDataFactoryV2DataFlow.
* ADF V2 veri akışı hata ayıklama oturumu için eylem komutları eklendi: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand ve Stop-AzDataFactoryV2DataFlowDebugSession.
* ADF .Net SDK sürümü 4.2.0’a güncelleştirildi

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* ‘-’ içeren hesapların etki alanı olmadan geçirilebilmesi için hesap doğrulama düzeltildi

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* PowerShell sürümü 1.0.0 olarak güncelleştirildi
* SDK sürümü 1.0.2 olarak güncelleştirildi
* Yeni SDK sürümüne başvurmaları için testler güncelleştirildi
* İç içe geçmiş çıkış yapısı, düzleştirilmiş olarak güncelleştirildi.

#### <a name="aziothub"></a>Az.IotHub
* Yeni yönlendirme kaynağı eklendi: DigitalTwinChangeEvents
* Küçük hata düzeltmesi: Get-AzIothub SubscriptionId öğesini döndürmüyor

#### <a name="azmonitor"></a>Az.Monitor
* New-AzActionGroupReceiver için yeni eylem grubu alıcıları eklendi:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver
* Alıcılar için etkinleştirilen ortak uyarı şemasını kullanın. Bunlar SMS, Azure Uygulaması iletimi, ITSM ve ses alıcıları için geçerli değildir
* Web kancaları artık Azure Active Directory kimlik doğrulamasını destekliyor.

#### <a name="aznetwork"></a>Az.Network
* Hizmet Uç Noktası İlkeleri için kullanılabilen diğer adları almak için çağrılabilen Get-AzAvailableServiceAlias cmdlet’i eklendi.
* Sanal Ağ Geçidi Bağlantılarına trafik seçicileri eklemeye yönelik destek eklendi
    - Yeni cmdlet'ler eklendi:
        - New-AzIpsecTrafficSelectorPolicy
    - Cmdlet’ler isteğe bağlı -TrafficSelectorPolicies parametresi ile güncelleştirildi
        - New-AzVirtualNetworkGatewayConnection
        - Set-AzVirtualNetworkGatewayConnection
* Ağ güvenlik kuralı yapılandırmalarında ESP ve AH protokollerine yönelik destek eklendi
    - Cmdlet'ler güncelleştirildi:
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Cortex cmdlet’lerinde özel durumların işlenmesi geliştirildi
* VirtualNetworkGateways için yeni Nesiller ve SKU’lar
  - VirtualNetworkGateways için yeni Nesiller sunuldu.
  - VirtualNetworkGateways için yüksek verimliliğe sahip yeni SKU’lar sunuldu.

#### <a name="azrediscache"></a>Az.RedisCache
* ‘-Size’ parametresine yönelik eksik değerleri eklemek için ‘Set-AzRedisCache’ başvuru belgesi güncelleştirildi

#### <a name="azsql"></a>Az.Sql
* Yönetilen örnekte Active Directory yöneticisini ayarlama desteği eklendi

#### <a name="azstorage"></a>Az.Storage
* Depolama İstemcisi Kitaplığı 11.1.0 sürümüne yükseltildi
* Yönetim düzlemi API’si olan liste kapsayıcıları NextPageLink ile listelenecek
    -  Get-AzRmStorageContainer
* Abonelikteki Liste Depolama hesapları NextPageLink ile listelenecek
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* Reset-AzStorageSyncServerCertificate öğesinde Sorun 9810 düzeltildi.

#### <a name="azwebsites"></a>Az.Websites
* Bir uygulamanın ASP’sini güncelleştiren Set-AzWebApp başarısız oluyor

## <a name="270---september-2019"></a>2.7.0 - Eylül 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* 'Set-AzApiManagementPolicy' başvuru belgesindeki '-Format' parametresinin açıklaması güncelleştirildi
* Kullanım dışı bırakılan 'Update-AzApiManagementDeployment' cmdlet’ine başvurular, başvuru belgesinden kaldırıldı. Bunun yerine 'Set-AzApiManagement' kullanın.

#### <a name="azautomation"></a>Az.Automation
* 'Register-AzAutomationDscNode' için başvuru belgesindeki örnek yazım yanlışı düzeltildi
* Register-AzAutomationDSCNode için işletim sistemi kısıtlamasına açıklama eklendi
* -Wait seçeneği için Start-AzAutomationRunbook cmdlet’i Null başvuru özel durumu düzeltildi.

#### <a name="azcompute"></a>Az.Compute
* New-AzDiskConfig cmdlet’ine UploadSizeInBytes parametresi eklendi
* New-AzSnapshotConfig cmdlet’ine Incremental parametresi eklendi
* Düşük öncelikli sanal makine özelliği eklendi:
    - New-AzVMConfig cmdlet’ine MaxPrice, EvictionPolicy ve Priority parametreleri eklendi.
    - New-AzVmssConfig, Update-AzVM ve Update-AzVmss cmdlet’lerine MaxPrice parametresi eklendi.
* Get-AzAvailabilitySet cmdlet’i abonelikteki tüm kullanılabilirlik kümelerini listelediğinde oluşan VM başvuru sorunu düzeltildi.
* Get-AzRemoteDesktopFile için null özel durumu düzeltildi.
* Sona göre konum için VHD Seek yöntemi düzeltildi.
* New-AzVM ve Update-AzVM için UltraSSD sorunu düzeltildi.

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF V2’ye 3 yeni komut eklendi - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription ve Get-AzDataFactoryV2TriggerSubscriptionStatus
* ADF .Net SDK sürümü 4.1.3’e güncelleştirildi

#### <a name="azhdinsight"></a>Az.HDInsight
* Son değişiklikler duyurusu

#### <a name="aziothub"></a>Az.IotHub
* Coğrafi olarak eşleştirilmiş olağanüstü durum kurtarma bölgesine bir IotHub için yük devretme çağırmaya yönelik destek eklendi.
* IotHub için ileti zenginleştirmelerini yönetmeye yönelik destek eklendi. Yeni cmdlet’ler şunlardır:
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* En son İzleme SDK’sını, yani 0.24.1-preview sürümünü işaret eder
   - Ölçüm cmdlet’lerine hataya neden olmayan değişiklikler ekler, yani Birim sabit listesi birçok yeni değeri destekler. Bunlar salt okunur cmdlet’ler olduğundan girişlerinde değişiklik olmaz.
   - **ActionGroups** istekleri için api-version şimdi **2019-06-01** değerine sahiptir. Önceden **2018-03-01** sürümü kullanılıyordu. Senaryo testleri bu değişikliğe uyum sağlayacak şekilde güncelleştirildi.
   - **EmailReceiver** ve **WebhookReceiver** sınıfları için oluşturuculara yeni bir zorunlu bağımsız değişken (**useCommonAlertSchema** adlı bir Boole değeri) eklendi. Şu anda, hataya neden olan bu değişikliği cmdlet’lerden gizlemek için değer **false** olarak ayarlandı. **NOT**: Bu, Uyarılar ekibi tarafından doğrulanması gereken geçici bir değişikliktir.
   - **Kaynak** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi. Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.
   - **AlertingAction** (**ScheduledQueryRuleSource** sınıfı ile ilişkili) sınıfının oluşturucusu için bağımsız değişkenlerin sırası önceki SDK’dan değiştirildi. Bu değişiklik iki birim testinin düzeltilmesini gerektirdi: Bunlar derlenebiliyor ancak testleri geçemiyordu.
* Ölçüm uyarısı V2 için Dinamik Eşik ölçütlerine yönelik destek eklendi
    - New-AzMetricAlertRuleV2Criteria: Şimdi dinamik eşik ölçütleri de oluşturur
    - Add-AzMetricAlertRuleV2: Şimdi dinamik eşik ölçütlerini de kabul eder
* Zamanlanmış Sorgu Kuralı cmdlet’lerinde (SQR) geliştirmeler
 - Cmdlet’ler 'Location' parametresini hem konum (ör. eastus) hem de konumun görünen adı (ör. Doğu ABD) biçiminde kabul eder
 - 'Enabled' parametresi yardım dosyalarında düzgün şekilde açıklandı
 - İsteğe bağlı 'ActionGroup' parametresi için örnekler eklendi
 - Yardım dosyaları genel olarak geliştirildi
* 'Set-AzActionRule' için kapsam türünü belirlemeyle ilgili bir hata düzeltildi

#### <a name="aznetwork"></a>Az.Network
* 'New-AzApplicationGateway' başvuru belgesindeki yanlış örnek düzeltildi
* 'Get-AzNetworkWatcherPacketCapture' başvuru belgesine paket yakalama için tüm özellikleri almayla ilgili not eklendi
* 'Test-AzNetworkWatcherIPFlow' başvuru belgesindeki örnek, NIC’lerin doğru olarak numaralandırılacağı şekilde düzeltildi
* Bulut özel durum ayrıştırması, mevcut olması durumunda daha fazla ayrıntı gösterecek şekilde iyileştirildi
* Bulut özel durum ayrıştırması, ek SDK özel durum türünü işleyecek şekilde geliştirildi
* Güvenlik Kuralı modellerinin yanlış eşlenmesi düzeltildi
* Özel IP özelliği için ağ arabirimine özellikler eklendi
    - 'PrivateEndpoint' özelliği PSResourceId türü olarak PSNetworkInterface öğesine eklendi
    - 'PrivateLinkConnectionProperties' özelliği PSIpConfigurationConnectivityInformation türü olarak PSNetworkInterfaceIPConfiguration öğesine eklendi
    - Yeni PSIpConfigurationConnectivityInformation model sınıfı eklendi
* Azure Güvenlik Duvarı kaynağı için 'mssql' adlı yeni ApplicationRuleProtocolType eklendi
* Sanal WAN’da çoklu bağlantı desteği
    - Yeni cmdlet’ler
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - Şu cmdlet güncelleştirildi:
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* Belgeler, bazı PowerShell örneklerinde AzureRM cmdlet’leri yerine Az cmdlet’leri kullanılacak şekilde düzeltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* AzureVMpolicy Nesnesi, ProtectedItemsCount Özniteliği ile güncelleştirildi
* VM ilkesi ve Özgün Depolama Hesabı Geri Yükleme için Testler eklendi

#### <a name="azresources"></a>Az.Resources
* New-AzRoleAssignment cmdlet’inin Scope parametresi olmadan çağrılamamasına neden olan bir hata düzeltildi.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* 'Update-AzServiceFabricReliability' başvuru belgesindeki örnekteki yazım yanlışı düzeltildi
* Uygulamaları ve hizmetleri yönetmek için yeni cmdlet’ler ekleniyor:
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* Service Fabric SDK’sı, Service Fabric kaynak sağlayıcısı api-version 2019-03-01 kullanan 1.2.0 sürümüne yükseltildi.

#### <a name="azsignalr"></a>Az.SignalR
* Update, Restart, CheckNameAvailability, GetUsage Cmdlet’leri eklendi

#### <a name="azsql"></a>Az.Sql
* 'Get-AzSqlElasticPool' için başvuru belgesindeki örnek güncelleştirildi
* Elastik havuz oluşturmak (New-AzSqlElasticPool) için sanal çekirdek örneği eklendi.
* Set-AzSqlServerAdvancedThreatProtectionPolicy ve Set-AzSqlDatabaseAdvancedThreatProtectionPolicy içinde EmailAddresses’in doğrulanması ve EmailAddresses’in boş olması durumunda EmailAdmins’in false olmamasına yönelik denetim kaldırıldı
* Denetim kategorisini etkinleştiren birden çok tanılama ayarı olduğunda sunucu/veritabanı denetim ayarlarının kaldırılması etkinleştirildi.
* Birden çok Sql Güvenlik Açığı Değerlendirmesi cmdlet’inde (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting ve Update-AzSqlInstanceVulnerabilityAssessmentSetting) e-posta adresleri doğrulaması düzeltildi.

#### <a name="azstorage"></a>Az.Storage
* 'Get-AzStorageAccountKey' için başvuru belgesindeki örnek güncelleştirildi
* Azure Dosyasını karşıya yüklerken/indirirken, hedef dosyada, dosya SMB özelliklerinin (Dosya Öznitelikleri, Dosya Oluşturma Zamanı, Dosya Son Yazma Zamanı) korunmasına yönelik destek eklendi
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Kapsayıcı tarafından etkinleştirilmiş ImmutabilityPolicy üzerinde özellikler/meta tarih hatası içeren Karşıya yükleme blok blobu düzeltildi.
    -  Set-AzStorageBlobContent
* Yönetim düzlemi API’si ile Azure Dosya paylaşımlarını yönetmeye yönelik destek eklendi
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* Uygulama yeni ASP’ye geçirilirken webapp etiketlerinin silinmesine neden olan sorun düzeltiliyor
* Publish-AzureWebapp cmdlet’i Linux ve Windows üzerinde çalışacak şekilde düzeltiliyor
* 'Get-AzWebAppPublishingProfile' başvuru belgesindeki örnek güncelleştirildi

## <a name="260---august-2019"></a>2.6.0 - Ağustos 2019
#### <a name="general"></a>Genel
* Çok sayıda modülde çeşitli yazım hataları düzeltildi

#### <a name="azaccounts"></a>Az.Accounts
* Azure İşlevleri Kimlik Doğrulaması’nda kullanıcı tarafından atanan MSI desteği (#9479)

#### <a name="azaks"></a>Az.Aks
* ‘Get-AzAks’ için çıkışla ilgili bir sorun düzeltildi
    * Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/9351 ) sorunu düzeltildi
    - ProductID, APIID, GroupID ve UserID için kısıtlamaları zorunlu kılmayan .NET NuGet sürümü güncelleştirildi
* **Get-AzApiManagementProduct** - Ürünleri API kullanarak sorgulama desteği eklendi.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision** - Yeni API düzeltmesi oluşturulurken ApiRevisionDescription parametresinin ayarlanmamasına neden olan sorun düzeltildi https://github.com/Azure/azure-powershell/issues/9752
* 'PsApiManagementOAuth2AuthrozationServer' modeli 'PsApiManagementOAuth2AuthorizationServer' olarak değiştirilerek yazım hatası düzeltildi

#### <a name="azbatch"></a>Az.Batch
* Windows’un ilk harfi büyütülerek yardım iletisindeki ve belgelerdeki yazım hatası düzeltildi

#### <a name="azcdn"></a>Az.Cdn
* CDN modülü dönüştürme yardımcısındaki yazım hatası düzeltildi

#### <a name="azcompute"></a>Az.Compute
* New-AzVMConfig cmdlet’ine VmssID eklendi
* New-AzVmssConfig ve Update-AzVmss öğelerine TerminateScheduledEvents ve TerminateScheduledEventNotBeforeTimeoutInMinutes parametreleri eklendi
* VM görüntüsü nesnesine HyperVGeneration özelliği eklendi
* Host ve HostGroup özellikleri eklendi
    - Yeni cmdlet’ler:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - New-AzVMConfig ve New-AzVM öğelerine HostId parametresi eklendi
* Doğru parametre adını kullanmak için ‘Invoke-AzVMRunCommand’ belgesindeki örnek güncelleştirildi
* 'Set-AzVMDiskEncryptionExtension' ve 'Set-AzVmssDiskEncryptionExtension' referans belgelerindeki '-VolumeType' açıklaması güncelleştirildi

#### <a name="azdatafactory"></a>Az.DataFactory
* ‘Windows’ sözcüğünün baş harfi büyütülerek 'New-AzDataFactoryEncryptValue' belgesindeki yazım hatası düzeltildi
* ADF .Net SDK sürümü 4.1.2’ye güncelleştirildi
* Şirket İçinde Barındırılan Integration Runtime’ı SSIS Integration Runtime için ara sunucu olarak ayarlamak üzere 'Set-AzureRmDataFactoryV2IntegrationRuntime' komutuna 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' ve 'DataProxyStagingPath' parametreleri eklendi
* Tetiklenen işlem hatlarını, iletiyi ve özellikleri göstermesi için PSTriggerRun öğesi, etkinlik türünü göstermesi için de PSActivityRun öğesi güncelleştirildi

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Hata veya uzak özel durumları için Get-DataLakeStoreDeletedItem öğesinin yanıt vermemeye başlaması düzeltildi.

#### <a name="azeventhub"></a>Az.EventHub
* #9658 numaralı şu sorun düzeltildi: Set-AzEventHubNetworkRuleSet öğesinde bulunan VirtualNteworkRule parametresindeki yazım hatası
* #9558 numaralı şu sorun düzeltildi: Set-AzEventHubNamespace öğesinin PUT yerine PATCH kullanması
* Set-AzEventHubNamespace cmdlet’ine EnableKafka parametresi eklendi
* #9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* ‘Azure’ın’ tamamen küçük harflerle yazılmasıyla belgede oluşan yazım hatası düzeltildi

#### <a name="azmonitor"></a>Az.Monitor
* Yardım belgelerindeki yanlış parametre adı düzeltildi

#### <a name="aznetwork"></a>Az.Network
* New-AzPrivateLinkServiceIpConfig güncelleştirildi
    - Sunucu tarafında hiç kullanılmadığı için ‘PublicIpAddress’ parametresi kullanım dışı bırakıldı.
    - Mevcut IP yapılandırmasının birincil yapılandırma olup olmadığını belirten bir isteğe bağlı bir parametre (‘Primary’) eklendi.
* SDK’daki istek hatası özel durumunun işlenmesi geliştirildi. Bu, daha önceden SDK özel durumlarının düzgün şekilde işlenenmemesiyle oluşan ve önemli hata ayrıntılarının görüntülenmemesine neden olan sorunu düzeltir
* Doğru IPv6 ön ek uzunluğunu denetlemek amacıyla Ipv6 IP Ön eki için doğrulama mantığı ayarlandı.
* Get-AzVirtualNetworkSubnetConfig güncelleştirildi: Alt ağ kaynak kimliği ile almak için parametre kümesi eklendi.
* AzNetworkServiceTag için Konum parametresinin açıklaması güncelleştirildi

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* 'New-AzOperationalInsightsLinuxSyslogDataSource' öğesine yönelik belgeler güncelleştirildi
    - Örnek eklendi
    - ‘-Name’ parametresi için açıklama güncelleştirildi
* New-AzOperationalInsightsWindowsEventDataSource için bir örnek eklendi
* New-AzOperationalInsightsWindowsEventDataSource için -Name parametresinin açıklaması değiştirildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 'Get-AzRecoveryServicesBackupJobDetail.md' dosyası güncelleştirildi

#### <a name="azresources"></a>Az.Resources
* Microsoft.Resource için yeni API sürümüne (2019-05-10) yönelik destek eklendi
    - Değişkenler, kaynaklar ve özellikler için copy.count = 0 parametresine yönelik destek eklendi
    - 'condition = false' veya 'copy.count = 0' içeren kaynaklar tam modda silinir
* Belgelere yardımcı olması için abonelik düzeyinde ilke atama örneği eklendi

#### <a name="azservicebus"></a>Az.ServiceBus
* #9658 numaralı şu sorun düzeltildi: Set-AzServiceBusNetworkRuleSet öğesinde bulunan VirtualNetworkRule parametresindeki yazım hatası
* #9786 numaralı şu sorun düzeltildi: Yalnızca dinleme haklarıyla bir kural oluşturulamaması
* Sıra ve konu için ad kullanılabilirliğini denetlemeye yönelik yeni komut ('Test-AzServiceBusNameAvailability') eklendi

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Düğüm ekleme türü cmdlet hataları düzeltildi:
    - Kaynak grubunun Service Fabric kümesiyle ilgili diğer vmss öğesi olduğunda oluşan NullReferenceException hatası. Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8681
    - virtualNetwork kümeyle farklı bir kaynak grubunda yer aldığında cmdlet’in başarısız olmasına neden olan sorun düzeltildi. Şu sorunu düzeltir: https://github.com/Azure/azure-powershell/issues/8407
    - Add-AzServiceFabricApplicationCertificate cmdlet’i kullanımdan kaldırıldı

#### <a name="azsql"></a>Az.Sql
* Eski denetim cmdlet’lerinin belgeleri güncelleştirildi.

#### <a name="azstorage"></a>Az.Storage
* Cmdlet örneklerine ve güncelleştirme parametresi açıklamalarına daha fazla senaryo eklenerek Get/Close-AzStorageFileHandle öğesi için yardım güncelleştirildi
* Karşıya yükleme blobu ve kopyalama blobunda StandardBlobTier için destek
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Blobu kopyala işleminde Yeniden Doldurma Önceliği Desteği
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebApp ve Set-AzWebAppSlot öğelerindeki -AppSettings parametresine yönelik açıklama eklendi

## <a name="250---july-2019"></a>2.5.0 - Temmuz 2019
#### <a name="azaccounts"></a>Az.Accounts
* ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* 'Remove-AzApplicationInsightsApiKey' belgesindeki örnek yazım hatası düzeltildi

#### <a name="azautomation"></a>Az.Automation
* Kaynak dizesindeki yazım hatası düzeltildi

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* NetworkRuleSet desteği eklendi.

#### <a name="azcompute"></a>Az.Compute
* VM örneği görünüm nesnesinin eksik özellikleri (ComputerName, OsName, OsVersion ve HyperVGeneration) eklendi.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Çoğaltma parametresi için Remove-AzContainerRegistryReplication içindeki yazım hatası düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9633

#### <a name="azdatafactory"></a>Az.DataFactory
* ADF .Net SDK’sı 4.1.0 sürümüne güncelleştirildi
* 'Get-AzDataFactoryV2PipelineRun' belgelerindeki yazım hatası düzeltildi

#### <a name="azeventhub"></a>Az.EventHub
* SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzEventHubAuthorizationRuleSASToken
* yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi

#### <a name="azkeyvault"></a>Az.KeyVault
* Sertifika İlkeleri için KeySize’ı belirtmeye yönelik destek eklendi

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzIntegrationAccountMap’in tüm eşleme türlerini listelemesi için düzeltme
    - Filtreleme için yeni MapType parametresi eklendi

#### <a name="azmanagedservices"></a>Az.ManagedServices
* API 2019-06-01 sürümü için destek eklendi (GA)

#### <a name="aznetwork"></a>Az.Network
* Özel uç nokta ve özel bağlantı hizmeti için destek eklendi
    - Yeni cmdlet’ler
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* Özellik için aşağıdaki komutlar güncelleştirildi: Virtualnetwork’te Alt Ağ üzerinde PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies bayrağı
    - New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig güncelleştirildi
        - Bu alt ağda özel uç nokta üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateEndpointNetworkPoliciesFlag parametresi eklendi.
        - Bu alt ağda özel bağlantı hizmeti üzerinde ağ ilkelerinin uygulanıp uygulanmayacağını yapılandıran isteğe bağlı -PrivateLinkServiceNetworkPoliciesFlag parametresi eklendi.
* AzPrivateLinkService’in cmdlet 'ServiceName' parametresi, geriye yönelik uyumluluk için 'ServiceName' diğer adıyla 'Name' olarak yeniden adlandırıldı
* Ağ güvenlik kuralı yapılandırmalarına yönelik ICMP protokolü etkinleştirildi
    - Cmdlet'ler güncelleştirildi
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* ConnectionProtocolType (Ikev1/Ikev2), New-AzVirtualNetworkGatewayConnection için yapılandırılabilir bir parametre olarak eklendi
* LoadBalancerFrontendIpConfiguration içinde PrivateIpAddressVersion eklendi
    - Şu cmdlet güncelleştirildi:
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* Yoklama içinde özek bağlantı noktasını desteklemek için Application Gateway New-AzApplicationGatewayProbeConfig komutu güncelleştirildi
    - New-AzApplicationGatewayProbeConfig güncelleştirildi: Arka uç sunucusunu yoklamak için kullanılan isteğe bağlı parametre Bağlantı Noktası eklendi. Bu parametre Standard_V2 ve WAF_V2 SKU için geçerlidir.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Kayıtlı aramaların varsayılan sürümü 1 olacak şekilde güncelleştirildi.
* Özel günlük null normal ifade işleme düzeltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* 'Get-AzRecoveryServicesBackupJob.md' güncelleştirildi
* 'Get-AzRecoveryServicesBackupContainer.md' güncelleştirildi
* 'Get-AzRecoveryServicesVault.md' güncelleştirildi
* 'Wait-AzRecoveryServicesBackupJob.md' güncelleştirildi
* 'Set-AzRecoveryServicesVaultContext.md' güncelleştirildi
* 'Get-AzRecoveryServicesBackupItem.md' güncelleştirildi
* 'Get-AzRecoveryServicesBackupRecoveryPoint.md' güncelleştirildi
* 'Restore-AzRecoveryServicesBackupItem.md' güncelleştirildi
* Azure Dosya Paylaşımı kapsayıcısının Kaydını Silmeye yönelik hizmet çağrısı güncelleştirildi
* 'Set-AzRecoveryServicesAsrAlertSetting.md' güncelleştirildi

#### <a name="azresources"></a>Az.Resources
- 'New-AzResourceGroupDeployment' belgelerinde başvurulan eksik cmdlet kaldırıldı
- İlke cmdlet’leri yeni 2019-01-01 api sürümünü kullanacak şekilde güncelleştirildi

#### <a name="azservicebus"></a>Az.ServiceBus
* SAS belirteci oluşturmak için yeni cmdlet eklendi: New-AzServiceBusAuthorizationRuleSASToken
* yalnızca 'Manage' atanırsa authorizationrules hakları için doğrulama ve hata iletisi eklendi

#### <a name="azsql"></a>Az.Sql
* Set-AzSqlDatabaseSecondary cmdlet’i için eksik örnekler düzeltildi
* E-posta adresi sağlamadan yinelenen Güvenlik Açığı Değerlendirme taramalarının ayarlanması düzeltildi
* Bir uyarı iletisindeki küçük bir yazım hatası düzeltildi.

#### <a name="azstorage"></a>Az.Storage
* 'Get-AzStorageAccount' başvuru belgelerindeki örnek, doğru parametre adını kullanacak şekilde güncelleştirildi

#### <a name="azstoragesync"></a>Az.StorageSync
* Invoke-AzStorageSyncChangeDetection cmdlet’i ekleniyor.
* TierFilesOlderThanDays’in uygulanmasına yönelik Sorun 9551 düzeltildi

#### <a name="azwebsites"></a>Az.Websites
* Bazı SiteConfig özelliklerinin Get-AzWebApp ve Set-AzWebApp tarafından döndürülmemesi sorunu düzeltildi
* Get-AzDeletedWebApp ve Restore-AzDeletedWebApp için yeni bir Konum parametresi eklendi
* New-AzWebApp -IncludeSourceWebAppSlots kullanılarak web uygulaması yuvalarının kopyalanmasıyla ilgili bir hata düzeltildi

## <a name="240---july-2019"></a>2.4.0 - Temmuz 2019
#### <a name="azaccounts"></a>Az.Accounts
* Profil cmdlet’leri için destek eklendi
* Oluşturulan cmdlet’lerde ortamlar ve veri düzlemleri için destek eklendi
* Windows PowerShell’deki veri düzlemi cmdlet’leri için bazı durumlarda yanlış uç noktası kullanılması hatası düzeltildi

#### <a name="azadvisor"></a>Az.Advisor
* Az.Advisor genel kullanıma sunuldu
* Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur

#### <a name="azapimanagement"></a>Az.ApiManagement
* [https://github.com/Azure/azure-powershell/issues/8671](https://github.com/Azure/azure-powershell/issues/8671 ) sorunu düzeltildi
    - **Get-AzApiManagementSubscription**
        - Abonelikleri Kullanıcı ve Ürüne göre sorgulama desteği eklendi
        - Kapsam kullanarak sorgulama desteği eklendi ('/', '/apis', '/apis/echo-api')
* [https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) ve https://github.com/Azure/azure-powershell/issues/8432 sorunları için düzeltme
    - **Import-AzApiManagementApi**
        - API’leri içeri aktarırken ‘ApiVersion’ ve ‘ApiVersionSetId’ belirtmek için destek eklendi

#### <a name="azautomation"></a>Az.Automation
* Dize değerini işlemek için Set-AzAutomationConnectionFieldValue cmdlet hatası düzeltildi.

#### <a name="azcompute"></a>Az.Compute
* New-AzImageConfig’e HyperVGeneration parametresi eklendi

#### <a name="azdatafactory"></a>Az.DataFactory
* Etkinlik çalıştırmalarını alma, işlem hattı çalıştırmalarını alma ve tetikleme çalıştırmalarını alma ADF cmdlet’lerinin çıkışları, Select-Object kanalını destekleyecek şekilde güncelleştiriliyor.

#### <a name="azeventgrid"></a>Az.EventGrid
* ‘New-AzEventGridSubscription’ belgesindeki yazım hatası düzeltildi

#### <a name="aziothub"></a>Az.IotHub
* Yetkilendirme ilkesi anahtarlarını yeniden oluşturma desteği eklendi.

#### <a name="aznetwork"></a>Az.Network
* Genel IP etiketlerine ‘RoutingPreference’ eklendi
* ‘Get-AzNetworkServiceTag’ başvuru belgesi için örnekler geliştirildi

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Get-AzPolicyState’de boş başvuru sorunu düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Get-AzOperationalInsightsDataSource’da döndürülen CustomLog veri kaynağı modeli düzeltildi

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* IaaSVM’ler için get-policy komutu düzeltmesi

#### <a name="azresources"></a>Az.Resources
    - Get-AzPolicyState -Top parametresi için yardım metni düzeltmesi
    - Get-AzPolicyAlias için istemci tarafı sayfalama desteği eklendi
    - Set-AzPolicyAssignment, -PolicyParameters ve -PolicyParametersObject için yeni parametreler eklendi
    - İlke cmdlet’leri için bazı belge ve örnekler güncelleştirildi

#### <a name="azservicebus"></a>Az.ServiceBus
* 4938 numaralı, MaxSizeInMegabytes ayarlanırken New-AzureRmServiceBusQueue’nun BadRequest döndürmesi sorunu düzeltildi

#### <a name="azsql"></a>Az.Sql
* Önizleme sürümündeki Örnek Yük Devretme Grubu cmdlet’leri genel kullanım sürümüne eklendi
* Yeni cmdlet’ler ile Azure SQL Server\Veritabanı Denetimi desteği.
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* Güvenlik Açığı Değerlendirmesi ayarlarından e-posta kısıtlamaları kaldırıldı

#### <a name="azstorage"></a>Az.Storage
* Aşağıdaki cmdlet’te 2 parametre (‘-IndexDocument’ ve ‘-ErrorDocument404Path’) gerekliden isteğe bağlı olarak değiştirildi:
    -  Enable-AzStorageStaticWebsite
* Get-AzStorageBlobContent’in yardımı, örnek eklenerek güncelleştirildi
* Cmdlet StorageException ile başarısız olduğunda artık daha ayrıntılı hata bilgisi gösteriliyor
* Azure Dosyalar AAD DS Kimlik Doğrulaması ile Depolama hesabı oluşturma veya güncelleştirme desteği eklendi
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Bir dosya paylaşımının, dosya dizininin veya dosyanın dosya tanıtıcılarını listeleme veya kapatma desteği eklendi
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Bu modül, artık toplama `Az` modülünün bir parçası olarak sunulur

## <a name="232---june-2019"></a>2.3.2 - Haziran 2019
#### <a name="azaccounts"></a>Az.Accounts
* İşlevler çağrıları için bazı durumlarda yanlış URL’nin kullanılmasına neden olan hata düzeltildi
    - Burada daha fazla bilgi bulunabilir: https://github.com/Azure/azure-powershell/issues/8983
* AzureRM’den Az cmdlet’lerine yönelik diğer adlarla ilgili sorun düzeltildi
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* New-AzVm ve New-AzVmss basit parametre kümeleri artık 'ProximityPlacementGroup' parametresini kabul ediyor.
* 'New-AzVM' başvuru belgelerindeki yazım hatası düzeltildi

#### <a name="azdns"></a>Az.Dns
* 'Set-AzDnsZone' yardım örneklerindeki bir yazım hatası düzeltildi.

#### <a name="azeventgrid"></a>Az.EventGrid
* 2019-06-01 API sürümünü kullanacak biçimde güncelleştirildi.
* Yeni cmdlet’ler:
    - New-AzureRmEventGridDomain
        - Yeni bir Azure Event Grid etki alanı oluşturur.
    - Get-AzureRmEventGridDomain
        - Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki tüm Event Grid Etki Alanlarının listesini alır.
    - Remove-AzureRmEventGridDomain
        - Bir Azure Event Grid Etki Alanını kaldırır.
    - New-AzureRmEventGridDomainKey
        - Bir Azure Event Grid Etki Alanı için paylaşılan erişim anahtarını yeniden üretir.
    - Get-AzureRmEventGridDomainKey
        - Etkinlikleri bir Event Grid Etki Alanıyla paylaşmak için kullanılan paylaşılan erişim anahtarlarını alır.
    - New-AzureRmEventGridDomainTopic:
        - Yeni bir Azure Event Grid Etki Alanı Konu Başlığı oluşturur.
    - Get-AzureRmEventGridDomainTopic
        - Bir Event Grid Etki Alanının ayrıntılarını veya mevcut Azure aboneliğindeki belirli Event Grid Etki Alanlarının altında bulunan tüm Event Grid Etki Alanı Konu Başlıklarının listesini alır
    - Remove-AzureRmEventGridDomainTopic:
        - Mevcut bir Azure Event Grid Etki Alanı Konu Başlığını kaldırır.
* Cmdlet'ler güncelleştirildi:
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:
        - Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmanın desteklemesi için yeni zorunlu parametreler ekler.
        - Bu kaynakların altında yeni olay aboneliklerinin oluşturulmasına olanak tanımak amacıyla yeni Event Grid Etki Alanı adını ve/veya Event Grid Etki Alanı Konu Başlığının adını belirtmek için yeni zorunlu parametreler ekler.
        - Mevcut parametrelerin yeniden kullanılmasına olanak tanımak için etki alanları ve etki alanı konu başlıkları için yeni Parametre kümeleri (örneğin, EndPointType, SubjectBeginsWith vb.) ekler.
        - Şunları belirtmek için yeni isteğe bağlı parametreler eklendi:
            - Olay aboneliği bitiş tarihi,
            - Gelişmiş filtreleme parametreleri.
        - Hedef olarak servicebusqueue için yeni sabit listesi ekler.
        - -IncludedEventType seçeneğinde ‘All’ kullanılmasını engeller ve bunu şununla değiştirir
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:
        - Sayfalandırma ve filtreleme sonuçlarını desteklemek için yeni isteğe bağlı parametreler (Top, ODataQuery and NextLink) ekler.
    - Remove-AzureRmEventGridSubscription
        - Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı ve Event Grid Etki Alanı Konu Başlığına yönelik kanal oluşturmayı desteklemek için yeni zorunlu parametreler ekler.
        - Bu kaynakların altında bulunan mevcut olay aboneliklerinin taşınmasına olanak tanımak amacıyla Event Grid Etki Alanı adının ve/veya Event Grid Etki Alanı Konu Başlığı adını belirtmek için yeni zorunlu parametreler ekler.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Dönüştürmeler desteği ve yeni işleç otomatik tamamlama değeri (RegEx) ekler
* New-AzFrontDoorWafManagedRuleObject
    - Yeni otomatik tamamlama değerleri ekler

#### <a name="aznetwork"></a>Az.Network
* Sanal Ağ Geçidi Kaynağı için destek ekler
    - Yeni cmdlet’ler
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* AvailablePrivateEndpointType ekler
    - Yeni cmdlet’ler
        - Get-AzAvailablePrivateEndpointType
* PrivatePrivateLinkService ekler
    - Yeni cmdlet’ler
        - Get-AzPrivateLinkService
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* PrivateEndpoint ekler
    - Yeni cmdlet’ler
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Özellik için aşağıdaki komutlar güncelleştirildi: VpnConnection’da UseLocalAzureIpAddress bayrağı
    - New-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.
    - Set-AzVpnConnection güncelleştirildi: Bağlantı başlatılırken yerel Azure IP adresinin kullanılması gerektiğini belirtmek için isteğe bağlı -UseLocalAzureIpAddress parametresi eklendi.
* ExpressRoute eşlemede PeeredConnections salt okunur alanı eklendi.
* ExpressRoute’ta GlobalReachEnabled salt okunur alanı eklendi.
* ExpressRouteCircuit modelindeki AllowGlobalReach alanının kullanımdan kaldırıldığını duyurmak için hataya neden olan değişiklik özniteliği eklendi
* AzApplicationGatewayRedirectConfiguration cmdlet’leri ile TargetListenerID’yi kullanırken oluşan 8756 Hatası Sorunu düzeltildi
* New-AzApplicationGatewayPathRuleConfig’de yeniden yazma kuralının ayarlanmasını engelleyen hata düzeltildi.
* NetworkInterfaceIpConfiguration’da VirtualNetworkTaps’in görüntülenmesi düzeltildi
* Tümünü listele bölümü için Cortex Get cmdlet’leri düzeltildi
* ExpressRouteGateways ve VpnGateway için VirtualHub başvurusu oluşturma düzeltildi
* AzureFirewall ve NatGateway için Kullanılabilirlik Alanları desteği eklendi
* Get-AzNetworkServiceTag cmdlet’i eklendi
* Azure Güvenlik Duvarı için birden fazla genel IP adresi desteği eklendi
    - New-AzFirewall cmdlet'i güncelleştirildi:
        - Bir veya daha fazla Genel IP Adresi nesnesi kabul eden -PublicIpAddress parametresi eklendi
        - Bir Sanal Ağ nesnesini kabul eden -VirtualNetwork parametresi eklendi
        - Güvenlik duvarı nesnesine AddPublicIpAddress ve RemovePublicIpAddress yöntemleri eklendi - bunlar giriş olarak Genel IP Adresi nesnesini kabul eder
        - Kullanım dışı parametreler - PublicIpName ve -VirtualNetworkName
* Özellik için aşağıdaki komutlar güncelleştirildi: Sanal ağ geçidi kaynağına VpnClient AAD kimlik doğrulaması seçenekleri ayarlandı.
    - New-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametreleri eklendi.
    - Set-AzVirtualNetworkGateway güncelleştirildi: Ağ Geçidinde VpnClient AAD kimlik doğrulamasını ayarlamak için isteğe bağlı AadTenantUri, AadAudienceId, AadIssuerUri parametresi eklendi.
    - Set-AzVirtualNetworkGateway güncelleştirildi: VpnClient AAD kimlik doğrulaması seçeneklerini Ağ Geçidinden kaldırmak için isteğe bağlı RemoveAadAuthentication anahtar parametresi eklendi.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* ‘New-Azurermoperationalınsightsworkspace’ komutunda **pergb2018** fiyatlandırma katmanı etkinleştirildi

#### <a name="azresources"></a>Az.Resources
* Ek Şablon Dışarı Aktarma seçenekleri için destek
    - Export-AzResourceGroup’a ‘-SkipResourceNameParameterization’ parametresi eklendi
    - Export-AzResourceGroup’a ‘-SkipAllParameterization’ parametresi eklendi
    - Dışarı aktarılan kaynak filtrelemesi için Export-AzResourceGroup’a ‘Resource’ parametresi eklendi

#### <a name="azservicefabric"></a>Az.ServiceFabric
* ByExistingKeyVault sertifika eklemenin bazı durumlarda yanlış parmak izi alması düzeltildi

#### <a name="azsql"></a>Az.Sql
* Gelişmiş Tehdit Koruması depolama uç noktası son eki düzeltildi
* Gelişmiş Veri Güvenliği’ni etkinleştirmenin Gelişmiş Tehdit Koruması ilkesini geçersiz kılması düzeltildi
* Müşterilerin yönetilen örnekler için TDE anahtarları ekleyip TDE koruyucusu ayarlamasına olanak tanımak için Management.Sql’e yönelik yeni cmdlet’ler
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Depolama hesabı oluştururken FileStorage ve SkuName Premium_ZRS tiplerine yönelik destek
    - New-AzStorageAccount
* Blob değiştirilemezlik cmdlet’inin açıklaması netleştirildi
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Kaynak grubu ile filtrelemeyi istemci yerine sunucuda yapmasını sağlayarak Get-AzWebAppCertificate’ı iyileştirir
* Get-AzWebAppSnapshot’a -UseDisasterRecovery anahtar parametresi ekler

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
    - [https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/7977 ) sorunu düzeltildi
    - [https://github.com/Azure/azure-powershell/issues/8600](https://github.com/Azure/azure-powershell/issues/8600 ) sorunu düzeltildi
* Start-AzAutomationDscCompilationJob cmdlet'inin davranışı tamamlanmasını beklemek yerine yalnızca işi başlatacak şekilde değiştirildi.
    * [https://github.com/Azure/azure-powershell/issues/8347](https://github.com/Azure/azure-powershell/issues/8347 ) sorunu düzeltildi
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
    - SQR API hakkında [daha fazla](/rest/api/monitor/scheduledqueryrules) bilgi
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
* Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/
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
* Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/
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
* Location, ResourceGroup ve ResourceName tamamlayıcıları eklendi: https://azure.microsoft.com/blog/completers-in-azure-powershell/
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
* [https://github.com/Azure/azure-powershell/issues/8166](https://github.com/Azure/azure-powershell/issues/8166 ) sorunu düzeltildi
* [https://github.com/Azure/azure-powershell/issues/8235](https://github.com/Azure/azure-powershell/issues/8235 ) sorunu düzeltildi
* [https://github.com/Azure/azure-powershell/issues/6219](https://github.com/Azure/azure-powershell/issues/6219 ) sorunu düzeltildi
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
* Az.Resources: [https://github.com/Azure/azure-powershell/issues/9351](https://github.com/Azure/azure-powershell/issues/7522 ) sorunu düzeltildi
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

* https://github.com/Azure/azure-powershell/issues/7679 düzeltmesi
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
* https://github.com/Azure/azure-powershell/issues/7402 düzeltmesi
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