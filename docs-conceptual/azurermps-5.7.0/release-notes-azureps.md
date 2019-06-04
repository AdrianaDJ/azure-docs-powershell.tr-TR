---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: ee9fb7e777d06f50514c6b4ba39805936b867045
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65535061"
---
# <a name="release-notes"></a>Sürüm notları

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.

---

# <a name="azure-powershell-570"></a>Azure PowerShell 5.7.0

Azure PowerShell 5.7.0 Yükleyicisi: [bağlantı](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)

ARM Cmdlet’leri için Galeri Modülü: [bağlantı](https://www.powershellgallery.com/packages/AzureRM/5.7.0)

`AzureRM` uygulamasını PowerShell Galerisi’nden yüklemek için şu komutu çalıştırın:

```powershell-interactive
Install-Module -Name AzureRM -Repository PSGallery -Force
```

`AzureRM` uygulamasının eski bir sürümünü güncelleştirmek için şu komutu çalıştırın:

```powershell-interactive
Update-Module -Name AzureRM
```

## <a name="changes-since-last-release"></a>Son Sürümden Sonraki Değişiklikler

#### <a name="general"></a>Genel
* Azure ClientRuntime’ın en son sürüme güncelleştirildi

#### <a name="azurestorage"></a>Azure Depolama
* FIPS ilkesinin etkinleştirildiği makinelerde Blob karşıya yükleme ve Dosya karşıya yükleme cmdlet’lerinde hataya neden olan sorun düzeltildi
    - Set-AzureStorageBlobContent
    - Set-AzureStorageFileContent

#### <a name="azurermbilling"></a>AzureRM.Billing
* Yeni Cmdlet Get-AzureRmEnrollmentAccount
  - Kayıt hesaplarını almayı sağlayan cmdlet

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Bilişsel Hizmetler Yönetim SDK’sı sürüm 4.0.0 ile tümleştirme.
* Get-AzureRmCognitiveServicesAccountUsage işlemi eklendi.

#### <a name="azurermcompute"></a>AzureRM.Compute
* `Get-AzureRmVmssDiskEncryptionStatus`, veri diski düzeyinde şifreleme durumunu destekler
* `Get-AzureRmVmssVmDiskEncryptionStatus`, veri diski düzeyinde şifreleme durumunu destekler
* Alan Dayanıklılığı Güncelleştirmesi
* “New-AzureRmVm” ve “New-AzureRmVmss” (basit parametre kümesi) kullanılabilirlik alanlarını destekler.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Commands.Resources.Rest ve ARM/Storage SDK’larının kullanılması gerekliliği kaldırıldı.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Hata ayıklama işlevselliği eklendi
* ADLS veri düzlemi SDK’sı 1.1.2 sürümüne güncelleştirildi
* Export-AzureRmDataLakeStoreItem - PerFileThreadCount, ConcurrentFileCount parametreleri kullanım dışı bırakıldı ve Concurrency parametresi eklendi
* Import-AzureRMDataLakeStoreItem - PerFileThreadCount, ConcurrentFileCount parametreleri kullanım dışı bırakıldı ve Concurrency parametresi eklendi
* Get-AzureRMDataLakeStoreItemContent - 4 MB’tan büyük olan içerikler için kuyruk davranışı düzeltildi
* Set-AzureRMDataLakeStoreItemExpiry - Göreli süre sonu zamanını ayarlamayı sağlayan yeni SetRelativeExpiry parametre kümesi eklendi
* Remove-AzureRmDataLakeStoreItem - Clean parametresi kullanımdan kaldırıldı.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* New-AzureRmEventHubGeoDRConfiguration içindeki AlternameName düzeltildi

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Cmdlet’ler kanal oluşturma senaryolarını içerecek biçimde güncelleştirildi
* Hataya neden olan değişiklik sürümü yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi

#### <a name="azurermnetwork"></a>AzureRM.Network
* Ağ cmdlet’lerindeki hata iletisi düzeltildi

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* customproperties özelliğini desteklemek için Rules cmdlet’inin CorrelationFilter bölümüne “properties” parametresi eklendi
* New-AzureRmServiceBusGeoDRConfiguration yardımı güncelleştirildi ve Rules cmdlet’inin çıktısı düzeltildi
* New-AzureRmServiceBusQueue ve New-AzureRmServiceBusSubscription cmdlet’inde otomatik iletme özellikleri düzeltildi

#### <a name="azurermsql"></a>AzureRM.Sql
* Elastik havuzda zaman uyumsuz işlemlerin iptal edilmesini desteklemek için yeni “Stop-AzureRmSqlElasticPoolActivity” cmdlet’i eklendi
* Yanıtta daha fazla bilgi sağlamak için Get-AzureRmSqlDatabaseActivity ve Get-AzureRmSqlElasticPoolActivity cmdlet’lerinin yanıtı güncelleştirildi

Son sürümden sonraki değişiklikler: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018

## <a name="560---march-2018"></a>5.6.0 - Mart 2018

#### <a name="general"></a>Genel
* CloudShell’de Varsayılan Kaynak Grubu ile ilgili sorun düzeltildi
* Modül içeri aktarma sırasında yanlış başlangıç betiklerinin yürütülmesi sorunu düzeltildi

#### <a name="azurermprofile"></a>AzureRM.Profile
* Desteklenmeyen senaryolarda MSI kimlik doğrulaması etkinleştirildi
* Kullanıcı tanımlı Yönetilen Hizmet Kimliği desteği eklendi

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Derlemedeki betiklerin temizlenmesiyle ilgili sorun düzeltildi

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Derlemedeki betiklerin temizlenmesiyle ilgili sorun düzeltildi

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVM' ve 'New-AzureRmVMSS', veri disklerini destekler.
* 'New-AzureRmVM' ve 'New-AzureRmVMSS', ada veya kimliğe göre özel görüntüyü destekler.
* Günlük analizi özelliği
    - 'Export-AzureRmLogAnalyticRequestRateByInterval' cmdlet’i eklendi
    - 'Export-AzureRmLogAnalyticThrottledRequests' cmdlet’i eklendi

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Kapsayıcı kayıt defteri ve azure dosya birimi bağlamaya ilişkin parametre kümeleri sorunu düzeltildi

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK’sı, aşağıdaki değişiklikleri içeren 0.6.0 sürümü önizlemesine güncelleştirildi:
    - Yeni AzureDatabricks LinkedService ve DatabricksNotebook Etkinliği eklendi
    - HDInsightOnDemand LinkedService içine headNodeSize ve dataNodeSize özellikleri eklendi
    - SalesforceMarketingCloud için LinkedService, Dataset, CopySource eklendi
    - Tüm etkinliklerde SecureOutput desteği eklendi
    - Kaç tane eşzamanlı etkinliğin çalıştırılacağını denetleyen ForEach etkinliğine yeni BatchCount özelliği eklendi
    - Yeni Filtre Etkinliği eklendi
    - Bağlantılı Hizmet Parametreleri desteği eklendi

#### <a name="azurermdns"></a>AzureRM.Dns
* Özel DNS Bölgeleri (Genel Önizleme) desteği
    - Yalnızca ilişkili sanal ağlar için görünür olan DNS bölgeleri oluşturma yeteneği eklendi

#### <a name="azurermnetwork"></a>AzureRM.Network
* DNS cmdlet’leriyle uyumluluk için model türleri güncelleştiriliyor.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* ASR Azure için Azure Site Recovery’de yapılan değişiklikler (cmdlet’ler şu anda Enterprise-Enterprise, Enterprise-Azure, HyperV-Azure, VMware-Azure arasındaki işlemleri desteklemektedir)
    - New-AzureRmRecoveryServicesAsrProtectionContainer
    - New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig
    - Remove-AzureRmRecoveryServicesAsrProtectionContainer
    - Update-AzureRmRecoveryServicesAsrProtectionDirection

#### <a name="azurermstorage"></a>AzureRM.Storage
* Yeni ve ayarlanan Depolama Hesabı cmdlet’lerindeki EnableEncryptionService ve DisableEncryptionService parametreleri, Bekleyen Şifreleme varsayılan olarak etkinleştirildiğinden ve devre dışı bırakılamadığından artık kullanılmıyor.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Remove-AzureRmWebAppSlot yardımı düzeltildi

## <a name="550---march-2018"></a>5.5.0 - Mart 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi
* Newtonsoft.Json 10.0.3 sürümünün 6.0.8 sürümüyle yan yana yüklenmesi

#### <a name="azurestorage"></a>Azure Depolama
* Geçici Silme özelliği desteği
    - Enable-AzureStorageDeleteRetentionPolicy
    - Disable-AzureStorageDeleteRetentionPolicy
    - Get-AzureStorageBlob

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi
* 2017-08-01 API sürümü desteğinin yanı sıra güvenlik duvarı ve sorgu ölçeğini genişletme özelliği desteği eklendi.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* notice.txt dosyası ve bildirim iletisi güncelleştirildi.

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVMSS', bağlantı dizelerini ayrıntılı modda yazdırır.
* 'New-AzureRmVmss', genel IP adresini, yük dengeleme kurallarını, gelen NAT kurallarını destekler.
* WriteAccelerator özelliği
    - Aşağıdaki cmdlet’lere WriteAccelerator anahtar parametresi eklendi: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk
    - Aşağıdaki cmdlet’lere OsDiskWriteAccelerator anahtar parametresi eklendi:     Set-AzureRmVmssStorageProfile.
    - Aşağıdaki cmdlet’lere OsDiskWriteAccelerator Boole parametresi eklendi:     Update-AzureRmVM     Update-AzureRmVmss

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Bazı şifreleme işlemleri için anlamlı bir hataya yol açmayan kimlik bilgileri şifreleme sorunu düzeltildi
* Veri fabrikasında paylaşılacak tümleştirme çalışma zamanı etkinleştirildi

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Özel kurulum ve sürüm seçimi işlevselliğini etkinleştirmek amacıyla "Set-AzureRmDataFactoryV2IntegrationRuntime" cmdlet’i için "SetupScriptContainerSasUri" ve "Edition" parametresi eklendi
* Bazı şifreleme işlemleri için anlamlı bir hataya yol açmayan kimlik bilgileri şifreleme sorunu düzeltildi.
* Veri fabrikasında paylaşılacak tümleştirme çalışma zamanı etkinleştirildi

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Set-AzureRmKeyVaultAccessPolicy için örnek düzeltildi

#### <a name="azurermnetwork"></a>AzureRM.Network
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi

#### <a name="azurermresources"></a>AzureRM.Resources
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Queue için EnableBatchedOperations özelliği eklendi
* Subscriptions için DeadLetteringOnFilterEvaluationExceptions özelliği eklendi

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Service Fabric cmdlet’i yenilendi
  - ARM şablonları güncelleştirildi
  - Artık başarısız işlemler geri alınmaz
  - Add-AzureRmServiceFabricNodeType
    - Sanal makineler varsayılan olarak yönetilen diskler kullanır
    - Mevcut VMSS alt ağı kullanılır
    - Tüm işlemler eşgüçlüdür
  - Remove-AzureRmServiceFabricNodeType, kısmen oluşturulan VMSS ve/veya küme düğümü türlerini temizler
  - Karmaşık özellik türleri için PSCluster nesnesinin çıkışı düzeltildi

#### <a name="azurermsql"></a>AzureRM.Sql
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi
* Get-AzureRmSqlServer, New-AzureRmSqlServer ve Remove-AzureRmSqlServer yanıtı artık FullyQualifiedDomainName özelliğini içerir.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Diğer adları içeri aktarma ile ilgili sorun düzeltildi
* New-AzureRMWebApp için yerel git deposu desteği ile, basitleştirilmiş WebApp oluşturma amacıyla parametre kümesi eklendi.

## <a name="540---february-2018"></a>5.4.0 - Şubat 2018
#### <a name="azurermautomation"></a>AzureRM.Automation
* New-AzureRmAutomationModule’dan Import-AzureRmAutomationModule’a diğer ad eklendi

#### <a name="azurermcompute"></a>AzureRM.Compute
* Bazı Get cmdlet’leri için ErrorAction sorunu düzeltildi.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Azure Container Instance SDK’sı 2018-02-01 uygulandı
    - DNS ad etiketi desteği

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Daha önce çalışmayan tüm GET cmdlet’leri düzeltildi.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Get-AzureRmEventHubGeoDRConfiguration yardımındaki hata düzeltildi

#### <a name="azurermnetwork"></a>AzureRM.Network
* Yeni bir bağlantı izleyicisi oluşturmak için cmdlet eklendi
    - New-AzureRmNetworkWatcherConnectionMonitor
* Bir bağlantı izleyicisini güncelleştirmek için cmdlet eklendi
    - Set-AzureRmNetworkWatcherConnectionMonitor
* Bağlantı izleyicisini veya bağlantı izleyicisi listesini almak için cmdlet eklendi
    - Get-AzureRmNetworkWatcherConnectionMonitor
* Bağlantı izleyicisini sorgulamak için cmdlet eklendi
    - Get-AzureRmNetworkWatcherConnectionMonitorReport
* Bağlantı izleyicisini başlatmak için cmdlet eklendi
    - Start-AzureRmNetworkWatcherConnectionMonitor
* Bağlantı izleyicisini durdurmak için cmdlet eklendi
    - Stop-AzureRmNetworkWatcherConnectionMonitor
* Bağlantı izleyicisini kaldırmak için cmdlet eklendi
    - Remove-AzureRmNetworkWatcherConnectionMonitor
* Kullanım dışı olan örneği kaldırmak için AzureRmApplicationGatewayBackendAddressPool belgeleri güncelleştirildi
* Application Gateway’e EnableHttp2 bayrağı eklendi
    - New-AzureRmApplicationGateway güncelleştirildi: İsteğe bağlı -EnableHttp2 parametresi eklendi
* IpTags, PublicIpAddress’e eklendi
    - New-AzureRmPublicIpAddress güncelleştirildi: IpTags eklendi
    - New-AzureRmPublicIpTag’e Iptag eklendi
* RouteTable ve effectiveRoute’a DisableBgpRoutePropagation özelliği eklendi.

#### <a name="azurermresources"></a>AzureRM.Resources
* Register-AzureRmProviderFeature: Eksik örnek belgelere eklendi
* Register-AzureRmResourceProvider: Eksik örnek belgelere eklendi

#### <a name="azurermstorage"></a>AzureRM.Storage
* Yeni ve ayarlanan Depolama Hesabı cmdlet’lerindeki EnableEncryptionService ve DisableEncryptionService parametreleri, Bekleyen Şifreleme varsayılan olarak etkinleştirildiğinden ve devre dışı bırakılamadığından artık kullanılmıyor.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount


## <a name="530---february-2018"></a>5.3.0 - Şubat 2018
### <a name="azurermprofile"></a>AzureRM.Profile
* PowerShell 3 ve 4 için kullanımdan kaldırılma uyarısı eklendi
* `Add-AzureRmAccount` `Connect-AzureRmAccount` olarak yeniden adlandırıldı; eski cmdlet adına bir diğer ad eklendi ve başka diğer adlar (`Login-AzAccount` ve `Login-AzureRmAccount`) yeni cmdlet adına yeniden yönlendirildi.
* `Remove-AzureRmAccount` `Disconnect-AzureRmAccount` olarak yeniden adlandırıldı; eski cmdlet adına bir diğer ad eklendi ve başka diğer adlar (`Logout-AzAccount` ve `Logout-AzureRmAccount`) yeni cmdlet adına yeniden yönlendirildi.
* Kaynak Dizeler `Login-AzureRmAccount` yerine `Connect-AzureRmAccount` kullanmak için düzeltildi
* `Add-AzureRmEnvironment` ve `Set-AzureRmEnvironment`
  - OperationalInsights veri düzlemi RP ile parametre olarak kullanılmak üzere `-AzureOperationalInsightsEndpoint` ve `-AzureOperationalInsightsEndpointResourceId` eklendi.

### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* `Login-AzureRmAccount` kullanımı `Connect-AzureRmAccount` olarak düzeltildi

### <a name="azurermcompute"></a>AzureRM.Compute
* `-AvailabilitySetName` parametresi `New-AzureRmVM` basitleştirilmiş parametre kümesine eklendi.
* `Login-AzureRmAccount` kullanımı `Connect-AzureRmAccount` olarak düzeltildi
* VM ve VM ölçek kümesi için kullanıcıya atanan kimlik desteği
    - `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` ve `Update-AzureRmVmss` için `-IdentityType` ve `-IdentityId` parametreleri eklendi
* `Add-AzureRmVmssNetworkInterfaceConfig` özelliğine `-EnableIPForwarding` parametresi eklendi
* `New-AzureRmVmssConfig` özelliğine `-Priority` parametresi eklendi

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* `Login-AzureRmAccount` kullanımı `Connect-AzureRmAccount` olarak düzeltildi

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* `Login-AzureRmAccount` kullanımı `Connect-AzureRmAccount` olarak düzeltildi
* `Login-AzureRmAccount` ile oturum açmadan bu cmdlet çalıştırıldığında oluşan `Test-AzureRmDataLakeStoreAccount` hata iletisi düzeltildi

### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* 2018-01-01 API sürümünü kullanmak için güncelleştirildi.

### <a name="azurermeventhub"></a>AzureRM.EventHub

* Coğrafi Bölge Olağanüstü Durum Kurtarma işlemleri için aşağıdaki yeni komutlar eklendi.
  - Yeni bir Diğer Ad (Olağanüstü Durum Kurtarma yapılandırması) oluşturur:
    - `New-AzureRmEventHubGeoDRConfiguration`
  - Diğer Ad (Olağanüstü Durum Kurtarma yapılandırması) alır:
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - Olağanüstü Durum Kurtarma'yı devre dışı bırakır ve birincil ad alanındaki değişiklikleri ikincil ad alanına çoğaltmayı durdurur
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - Olağanüstü Durum Kurtarma yük devretmesini çağırır ve diğer adı, ikincil ad alanına işaret edecek şekilde yeniden yapılandırır
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - Diğer Adı (Olağanüstü Durum Kurtarma yapılandırması) siler
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* Ad Alanı Adı ve GeoDr Yapılandırması Adı - Diğer Ad kullanılabilirliğini denetlemek için aşağıdaki yeni komutlar eklendi.
  - Ad Alanı adı veya Diğer Ad (Olağanüstü Durum Kurtarma yapılandırması) kullanılabilirliğini denetler:
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a>AzureRM.Insights
* `Login-AzureRmAccount` kullanımı `Connect-AzureRmAccount` olarak düzeltildi

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* `Login-AzureRmAccount` kullanımı `Connect-AzureRmAccount` olarak düzeltildi

### <a name="azurermnetwork"></a>AzureRM.Network
* 'Kaynağın üzerine yazmak istediğinizden emin misiniz' üzerine yazma iletisi düzeltildi

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* `Invoke-AzureRmOperationalInsightsQuery` aracılığıyla V2 API sorgulama desteği eklendi. Yeni API hakkında daha fazla bilgi için bkz. [https://dev.loganalytics.io/](https://dev.loganalytics.io/).

### <a name="azurermresources"></a>AzureRM.Resources
* `Get-AzureRmADServicePrincipal`: `-ServicePrincipalName` SPN parametre kümesi ile gereksiz olduğundan varsayılan Boş parametre kümesinden kaldırıldı

### <a name="azurermservicebus"></a>AzureRM.ServiceBus

* `Remove-AzureRmServiceBusRule` ve `Get-AzureRmServiceBusKey` için işlevsellik düzeltmesi eklendi
* Coğrafi Bölge Olağanüstü Durum Kurtarma işlemleri için aşağıdaki yeni commandlet’ler eklendi.
  - Yeni bir Diğer Ad (Olağanüstü Durum Kurtarma yapılandırması) oluşturur:
    - `New-AzureRmServiceBusDRConfigurations`
  - Diğer Ad (Olağanüstü Durum Kurtarma yapılandırması) alır:
    - `Get-AzureRmServiceBusDRConfigurations`
  - Olağanüstü Durum Kurtarma'yı devre dışı bırakır ve birincil ad alanındaki değişiklikleri ikincil ad alanına çoğaltmayı durdurur
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - Olağanüstü Durum Kurtarma yük devretmesini çağırır ve diğer adı, ikincil ad alanına işaret edecek şekilde yeniden yapılandırır
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - Diğer Adı (Olağanüstü Durum Kurtarma yapılandırması) siler
    - `Remove-AzureRmServiceBusDRConfigurations`
* `Test-AzureRmServiceBusName` commandlet’leri Coğrafi Bölge Olağanüstü Durum Kurtarma - Diğer ad kullanılabilirliğini denetleme işlemleri için güncelleştirildi.
  - Ad Alanı adı veya Diğer Ad (Olağanüstü Durum Kurtarma yapılandırması) kullanılabilirliğini denetler:
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* `Login-AzureRmAccount` kullanımı `Connect-AzureRmAccount` olarak düzeltildi

## <a name="520---january-2018"></a>5.2.0 - Ocak 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Add-AzureRmAccount
  * Geçerli VM / Hizmetin Yönetilen Hizmet Kimliğine ait kimlik bilgileri kullanılarak kimlik doğrulaması yapılması için -MSI oturum açma bilgileri eklendi
  * Kullanıcı tarafından sağlanan erişim belirteçleriyle oturum açılırken KeyVault Kimlik Doğrulaması düzeltildi

#### <a name="azurestorage"></a>Azure Depolama
* Depolama hizmeti özelliklerini almak ve ayarlamak için cmdlet’ler eklendi
    - Get-AzureStorageServiceProperty
    - Update-AzureStorageServiceProperty

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty ve New-AzureRmApiManagement için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermautomation"></a>AzureRM.Automation
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Set-AzureRmAutomationRunbook için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermbackup"></a>AzureRM.Backup
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermbatch"></a>AzureRM.Batch
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* New-AzureRmCdnEndpoint ve New-AzureRmCdnProfile için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Bilişsel Hizmetler Yönetim SDK’sı sürüm 3.0.0 ile tümleştirme.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Akıllı varsayılanlar kullanılarak bir Sanal Makine Ölçek Kümesi ve tüm gerekli kaynakları oluşturan New-AzureRmVmss cmdlet’ine basitleştirilmiş parametre kümesi eklendi
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* New-AzureRmVm ve Update-AzureRmVm için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı
* Kısıtlamaya Bölge dahil edildiğinde Get-AzureRmComputeResourceSku cmdlet’i düzeltildi.
* Azure İzleyici havuz desteği için Tanılama Aracısı yapılandırma şeması güncelleştirildi.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Tüm veri deposu bağlantılı hizmetler için Azure Key Vault desteği etkinleştirildi
* Azure SSIS Integration Runtime için lisans türü özelliği eklendi
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* New-AzureRmDataFactory için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Tüm veri deposu bağlantılı hizmetler için Azure Key Vault desteği etkinleştirildi
* Azure SSIS Integration Runtime için lisans türü özelliği eklendi
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* AHUB işlevselliğini etkinleştirmek amacıyla "Set-AzureRmDataFactoryV2IntegrationRuntime" komutuna "LicenseType" parametresi eklendi

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* New-AzureRmDataLakeAnalyticsAccount ve Set-AzureRmDataLakeAnalyticsAccount için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* New-AzureRmDataLakeStoreAccount ve Set-AzureRmDataLakeStoreAccount için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermdns"></a>AzureRM.Dns
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Aşağıdaki yeni cmdlet eklendi:
  - Update-AzureRmEventGridSubscription
    - Event Grid olay aboneliğinin özellikleri güncelleştirildi.
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurerminsights"></a>AzureRM.Insights
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermiothub"></a>AzureRM.IotHub
* IoTHub cmdlet’leri için Sertifika desteği eklendi
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Uzun süre çalışan KeyVault cmdlet’leri için -AsJob desteği eklendi. Seçilen cmdlet’lerin arka planda çalışmasını ve ilerlemeyi izleyip denetlemek için bir iş döndürmesini sağlar.
  * Etkilenen cmdlet: Remove-AzureRmKeyVault
* Set-AzureRmKeyVaultAccessPolicy içinde, AAD filtresinin UPN’yi ayarlamak yerine, SPN’yi sağlanan UPN’ye ayarladığı hata düzeltildi
  - Daha fazla bilgi için şu soruna bakın: https://github.com/Azure/azure-powershell/issues/5201

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Update-AzureRmMlCommitmentPlan için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Remove-AzureRmMlOpCluster cmdlet’ine IncludeAllResources parametresini eklendi
  - Bu anahtar parametresi kullanıldığında, başlangıçta kümeyle birlikte oluşturulan tüm kaynaklar kaldırılır
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermmedia"></a>AzureRM.Media
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Set-AzureRmMediaService ve New-AzureRmMediaService için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermnetwork"></a>AzureRM.Network
* Uzun süre çalışan Network cmdlet’leri için -AsJob desteği eklendi. Seçilen cmdlet’lerin arka planda çalışmasını ve ilerlemeyi izleyip denetlemek için bir iş döndürmesini sağlar.
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* New-AzureRmNotificationHubsNamespace ve Set-AzureRmNotificationHubsNamespace için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace ve Set-AzureRmOperationalInsightsWorkspace için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Restore-AzureRmRecoveryServicesBackupItem cmdlet’ine -UseOriginalStorageAccount seçeneği eklendi.
  - Bu bayrağın etkinleştirilmesi disklerin özgün depolama hesaplarına geri yüklenmesini sağlar ve böylece kullanıcılar geri yüklenen sanal makinenin yapılandırmasını özgün sanal makinelere olabildiğince yakın tutabilir.
  - Geri yükleme işleminin performansının geliştirilmesine de yardımcı olur.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Güvenlik duvarı kuralları için 3 yeni cmdlet eklendi
* Coğrafi çoğaltma için 3 yeni cmdlet eklendi
* Bölgeler ve etiketler için destek eklendi
* ResourceGroup öğesini mümkün olduğunca isteğe bağlı hale getirin.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermresources"></a>AzureRM.Resources
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Uzun süre çalışan Resources cmdlet’leri için -AsJob desteği eklendi. Seçilen cmdlet’lerin arka planda çalışmasını ve ilerlemeyi izleyip denetlemek için bir iş döndürmesini sağlar.
* Adlandırma kurallarına uymak için Get-AzureRmProviderOperation içinden Get-AzureRmResourceProviderAction içine diğer ad eklendi

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermservermanagement"></a>AzureRM.ServerManagement
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* New-AzureRmServerManagementNode ve New-AzureRmServerManagementGateway için -Tags kullanımdan kaldırıldı ve -Tag kullanılmaya başlandı

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermsiterecovery"></a>AzureRM.SiteRecovery
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermsql"></a>AzureRM.Sql
* Denetim komutları parametrelerinin açıklamaları güncelleştirildi
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Uzun süre çalışan cmdlet’lere -AsJob parametresi eklendi
* Get-AzureRmSqlServiceObjective içindeki -DatabaseName parametresi kullanımdan kaldırıldı

#### <a name="azurermstorage"></a>AzureRM.Storage
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* -EnableEncryptionService parametresi None olacak şekilde New-AzureRMStorageAccount cmdlet’ini çalıştırmaya ilişkin null başvuru sorunu düzeltildi
* Uzun süre çalışan Storage cmdlet’leri için -AsJob desteği eklendi. Seçilen cmdlet’lerin arka planda çalışmasını ve ilerlemeyi izleyip denetlemek için bir iş döndürmesini sağlar.
    - Etkilenen cmdlet’ler, Depolama Hesabı ve Depolama Hesabı Ağ Kuralı için New-, Remove-, Add- ve Update- cmdlet’leridir.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Geçerli Konumlar aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -Location parametrelerine Location Tamamlayıcısı eklendi
* Geçerli abonelikteki kaynak grupları aracılığıyla sekme ile tamamlamaya olanak sağlayacak şekilde -ResourceGroup parametrelerine ResourceGroup Tamamlayıcısı eklendi
* Uzun süre çalışan Websites cmdlet’leri için -AsJob desteği eklendi. Seçilen cmdlet’lerin arka planda çalışmasını ve ilerlemeyi izleyip denetlemek için bir iş döndürmesini sağlar.
     - Etkilenen cmdlet’ler WebApps, AppServicePlan ve Slots için New-, Remove-, Add- ve Set- cmdlet’leridir

## <a name="2017128-version-511"></a>2017.12.8 Sürüm 5.1.1
* AnalysisServices
  - Tüm bulutların desteklenmesi için konum kümesini doğrulama, dinamik arama olarak değiştirildi.
* Otomasyon
  - Import-AzureRMAutomationRunbook güncelleştirmesi
    - Artık Python2 runbook’ları için destek sağlanmaktadır
* Batch
  - Bir kaynak grubu olmayan hesap işlemlerinin kaynak grubunu otomatik olarak algılayamadığı bir hata düzeltildi
* İşlem
  - Get-AzureRmComputeResourceSku, bölge bilgilerini gösterir.
  - [https://github.com/Azure/azure-powershell/issues/5038](https://github.com/Azure/azure-powershell/issues/5038) sorununu düzeltmek için Disable-AzureRmVmssDiskEncryption öğesini güncelleştirin
  - Uzun süre çalışan İşlem cmdlet’leri için -AsJob desteği eklendi. Seçilen cmdlet’lerin arka planda çalışmasını ve ilerlemeyi izleyip denetlemek için bir iş döndürmesini sağlar.
    - Etkilenen cmdlet’ler şunlardır: Sanal Makineler ve Sanal Makine Ölçek Kümeleri için New-, Update-, Set-, Remove-, Start-, Restart-, Stop- cmdlet’leri
    - New-AzureRmVM cmdlet’ine akıllı varsayılanları kullanarak bir Sanal Makine ve tüm gerekli kaynakları oluşturan basitleştirilmiş parametre kümesi eklendi
* ContainerInstance
  - Azure Container Instance SDK’sı uygulama 2017-10-01
    - Kapsayıcıyı tamamlanana kadar çalıştırma desteği
    - Azure Dosya birimi bağlama desteği
    - Ortak IP için birden çok bağlantı noktası açma desteği
* ContainerRegistry
  - Coğrafi çoğaltma ve web kancaları için yeni cmdlet’ler
    - Get/New/Remove-AzureRmContainerRegistryReplication
    - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* DataFactories
    - Kimlik bilgisi şifreleme işlevi artık "Uzaktan Erişim" etkinken (Ağ Üzerinden) ve "Uzaktan Erişim" devre dışıyken (Yerel Makine) çalışır.
* DataFactoryV2
  - İki yeni cmdlet eklendi: Update-AzureRmDataFactoryV2 ve Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
  - Submit-AzureRmDataLakeAnalyticsJob’a ScriptParameter adlı bir parametre eklendi
    - ScriptParameter hakkında daha ayrıntılı bilgiye Submit-AzureRmDataLakeAnalyticsJob üzerinde Get-Help kullanarak ulaşabilirsiniz
  - New-AzureRmDataLakeAnalyticsAccount için, MaxDegreeOfParallelism parametresi MaxAnalyticsUnits olarak değiştirildi
    - MaxAnalyticsUnits parametresi için bir diğer ad eklendi: MaxDegreeOfParallelism
  - New-AzureRmDataLakeAnalyticsComputePolicy için, MaxDegreeOfParallelismPerJob parametresi MaxAnalyticsUnitsPerJob olarak değiştirildi
    - MaxAnalyticsUnitsPerJob parametresi için bir diğer ad eklendi: MaxDegreeOfParallelismPerJob
  - Set-AzureRmDataLakeAnalyticsAccount için, MaxDegreeOfParallelism parametresi MaxAnalyticsUnits olarak değiştirildi
    - MaxAnalyticsUnits parametresi için bir diğer ad eklendi: MaxDegreeOfParallelism
  - Submit-AzureRmDataLakeAnalyticsJob için, DegreeOfParallelism parametresi AnalyticsUnits olarak değiştirildi
    - AnalyticsUnits parametresi için bir diğer ad eklendi: DegreeOfParallelism
  - Update-AzureRmDataLakeAnalyticsComputePolicy için, MaxDegreeOfParallelismPerJob parametresi MaxAnalyticsUnitsPerJob olarak değiştirildi
    - MaxAnalyticsUnitsPerJob parametresi için bir diğer ad eklendi: MaxDegreeOfParallelismPerJob
* MachineLearningCompute
  - Set-AzureRmMlOpCluster ekleme
    - Kümenin aracı sayısını veya SSL yapılandırmasını güncelleştirme
  - Orchestrator özellikleri isteğe bağlıdır
    - Bir hizmet sorumlusu sağlanmadıysa servis tarafından oluşturulur ve bu nedenle düzenleyici özellikleri artık isteğe bağlıdır
* PowerBIEmbedded
  - Power BI Embedded Kapasite cmdlet’leri için destek eklendi
  - Yeni Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesinin ayrıntılarını alır.
  - Yeni Cmdlet New-AzureRmPowerBIEmbeddedCapacity - Yeni bir PowerBI Embedded Kapasitesi oluşturur
  - Yeni Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğini siler
  - Yeni Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğini sürdürür
  - Yeni Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğini askıya alır
  - Yeni Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğinin varlığını test eder
  - Yeni Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - Bir PowerBI Embedded Kapasitesi örneğini değiştirir
* Profil
  - [https://login.microsoftonline.us](https://login.microsoftonline.us/) için USGovernmentActiveDirectoryEndpoint güncelleştirildi
    - Azure Kamu uç nokta eşlemeleri hakkında daha fazla bilgi için bkz. https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - Cmdlet’ler için -AsJob desteği eklenerek seçilen cmdlet’lerin arka planda yürütülmesi ve ilerlemeyi izleyip denetlemek için bir iş döndürmesine olanak sağlandı
    - Get-AzureRmSubscription cmdlet’ine -AsJob parametresi eklendi
* RecoveryServices.Backup
  - Hata düzeltildi - Get-AzureRmRecoveryServicesBackupItem, kapsayıcı adı filtresi için büyük küçük harf duyarsız karşılaştırma yapar.
  - Hata düzeltildi - AzureVmItem, artık bir yedekleme işleminin en son gerçekleştirildiği zamanı gösteren bir özelliğe sahip: LastBackupTime.
* Kaynaklar
  - Get-AzureRMRoleAssignment’ın özel roller için roledefiniton adı olmayan atamalarla sonuçlandığı bir hata düzeltildi
    - Kullanıcılar artık rol türünden bağımsız olarak roledefinition adları olan atamalar ile Get-AzureRMRoleAssignment kullanabilir
  - Set-AzureRMRoleRoleDefinition’ın assignablescopes içinde yeni bir kapsam olduğunda RD bulunamadı hatası vermesine neden olan sorun düzeltildi
    - Kullanıcılar artık kapsamın konumundan bağımsız olarak yeni kapsamlar dahil atanabilir kapsamlar ile Set-AzureRMRoleRoleDefinition kullanabilir
  - Kapsamların "/" ile bitmesine olanak sağlandı
    - Kullanıcılar artık API ve CLI ile tutarlı olarak "/" ile biten kapsamlarda RoleDefinition ve RoleAssignment commandlet’lerini kullanabilir
  - Kullanıcıların temsilci bayrağı kullanarak RoleAssignment oluşturmasına olanak sağlandı
    - Kullanıcılar artık temsilci bayrağı ekleme seçeneğiyle New-AzureRMRoleAssignment kullanabilir
  - RoleAssignment kapsam parametresine uyacak şekilde düzeltildi
  - New-AzureRmRoleAssignment Commandlet’inde ServicePrincipalName için bir diğer ad eklendi
    - Kullanıcılar artık New-AzureRmRoleAssignment commandlet’ini kullanırken ServicePrincipalName yerine ApplicationId kullanabilir
* SiteRecovery
  - Büyük değişiklikler içeren bir sonraki sürüme hazırlık olarak bu modüldeki tüm cmdlet’ler için kullanımdan kaldırılma uyarıları eklendi.
    - Cmdlet’lerinizi AzureRM’den geçirme hakkında daha fazla bilgi için yakında sunulacak olan büyük değişikliklere ilişkin kılavuza bakın.
* Sql
  - Set-AzureRmSqlDatabase kullanarak veritabanını yeniden adlandırma özelliği eklendi
  - [https://github.com/Azure/azure-powershell/issues/4974](https://github.com/Azure/azure-powershell/issues/4974) sorunu düzeltildi
    - Denetim cmdlet’leri için geçersiz AUDIT_CHANGED_GROUP değeri sağlamak artık hata oluşturmuyor ve gelecek bir sürümde kaldırılacak.
  - [https://github.com/Azure/azure-powershell/issues/5046](https://github.com/Azure/azure-powershell/issues/5046) sorunu düzeltildi
    - Denetim cmdlet’lerinde AuditAction parametresi artık yok sayılmıyor
  - Denetim cmdlet’lerinde 'Secondary' StorageKeyType sağlandığında oluşan bir hata düzeltildi
    - Blob denetimi ayarlanırken, StorageKeyType parametresi için 'Secondary' değeri sağlandığında ikincil anahtar yerine birincil depolama hesabı anahtarı kullanılıyordu.
  - Set-AzureRmSqlServerTransparentDataEncryptionProtector onay iletisi ifadesi değiştirildi
* Azure (RDFE)
    - Tüm RemoteApp Cmdlet’leri kaldırıldı
* Azure Depolama
    - Azure Depolama İstemci Kitaplığı 8.6.0 ve Azure Depolama DataMovement Kitaplığı 0.6.5 sürümüne yükseltildi

## <a name="20171110-version-501"></a>2017.11.10 Sürüm 5.0.1
* Aşağıdaki modüller çalıştırılırken bazı cmdlet'lerin başarısız olmasına neden olan bütünleştirilmiş kod yükleme sorunu düzeltildi:
  - AzureRM.ApiManagement
  - AzureRM.Backup
  - AzureRM.Batch
  - AzureRM.Compute
  - AzureRM.DataFactories
  - AzureRM.HDInsight
  - AzureRM.KeyVault
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices.Backup
  - AzureRM.RecoveryServices.SiteRecovery
  - AzureRM.RedisCache
  - AzureRM.SiteRecovery
  - AzureRM.Sql
  - AzureRM.Storage
  - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>2017.11.8 - Sürüm 5.0.0
* NOT: Bu bir hataya neden olan değişiklik yayınıdır. Sunulan önemli değişikliklerin tam listesi için lütfen geçiş kılavuzuna (https://aka.ms/azps-migration-guide)) bakın.
* AzureRM’deki tüm cmdlet'ler artık çevrimiçi yardımı destekler
  - Çevrimiçi yardımı varsayılan İnternet tarayıcınızda açmak için Get-Help komutunu -Online parametresiyle birlikte çalıştırın
* AnalysisServices
  * Synchronize-AzureAsInstance komutu düzeltildi ve eşitleme için yeni AsAzure REST API’si ile çalışması sağlandı
* ApiManagement
  * Bu yayında ApiManagement’ta yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
  * [https://github.com/Azure/azure-powershell/issues/4510](https://github.com/Azure/azure-powershell/issues/4510) sorununu düzeltmek için Get-AzureRmApiManagementUser Cmdlet’i güncelleştirildi
  * Boş https://github.com/Azure/azure-powershell/issues/4069 Yolu ile API oluşturmak için New-AzureRmApiManagementApi Cmdlet’i güncelleştirildi
* ApplicationInsights
  * Application Insights kaynağını alma/oluşturma/kaldırma komutları eklendi
    - Get-AzureRmApplicationInsights
    - New-AzureRmApplicationInsights
    - Remove-AzureRmApplicationInsights
  * Application Insights kaynağının fiyatlandırmasını/günlük sınırını alma/güncelleştirme komutları eklendi
    - Get-AzureRmApplicationInsights -IncludeDailyCap
    - Set-AzureRmApplicationInsightsPricingPlan
    - Set-AzureRmApplicationInsightsDailyCap
  * Application Insights kaynağının sürekli dışarı aktarma işlemini alma/oluşturma/güncelleştirme/kaldırma komutları eklendi
    - Get-AzureRmApplicationInsightsContinuousExport
    - Set-AzureRmApplicationInsightsContinuousExport
    - New-AzureRmApplicationInsightsContinuousExport
    - Remove-AzureRmApplicationInsightsContinuousExport
  * Application Insights kaynağı api anahtarlarını alma/oluşturma/kaldırma komutları eklendi
    - Get-AzureRmApplicationInsightsApiKey
    - New-AzureRmApplicationInsightsApiKey
    - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
  * `New-AzureRmBatchAccount` içine yeni parametreler eklendi.
    - `PoolAllocationMode`: Batch hesabında havuz oluşturmak için kullanılacak ayırma modu. Kullanıcının aboneliğindeki havuz düğümlerini ayıran bir Batch hesabı oluşturmak için bu ayarı `UserSubscription` olarak belirleyin.
    - `KeyVaultId`: Batch hesabıyla ilişkili Azure anahtar kasasının kaynak kimliği.
    - `KeyVaultUrl`: Batch hesabıyla ilişkili Azure anahtar kasasının URL’si.
  * Parametreler `New-AzureBatchTask` olarak güncelleştirildi.
    - `RunElevated` anahtarı kaldırıldı. `RunElevated` parametresi kaldırılıp bunun yerine `UserIdentity` parametresi eklendi. Eşdeğer bir davranış aşağıda gösterildiği gibi bir `PSUserIdentity` oluşturularak elde edilebilir:
      - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Görev", "Yönetici")
      - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
    - `AuthenticationTokenSettings` parametresi eklendi. Bu parametre Batch hizmetinden çalıştığında, göreve bir kimlik doğrulama belirteci sağlamasını istemenize olanak tanır ve Batch hizmetine istek göndermek için göreve Batch hesap anahtarlarını geçirme gereksinimini ortadan kaldırır.
    - `ContainerSettings` parametresi eklendi.
      - Bu parametre, Batch hizmetinin görevi bir kapsayıcı içinde çalıştırmasını istemenize olanak tanır.
    - `OutputFiles` parametresi eklendi.
      - Bu parametre, görevi tamamlandıktan sonra dosyaları Azure Depolama’ya yükleyecek şekilde yapılandırmanıza olanak tanır.
  * Parametreler `New-AzureBatchPool` olarak güncelleştirildi.
    - `UserAccounts` parametresi eklendi.
      - Bu parametre, havuzdaki her düğümde oluşturulan kullanıcı hesaplarını tanımlar.
    - `TargetLowPriorityComputeNodes` eklendi ve `TargetDedicated` olan ad, `TargetDedicatedComputeNodes` olarak değiştirildi.
      - `TargetDedicatedComputeNodes` parametresi için bir `TargetDedicated` diğer adı oluşturuldu.
    - `NetworkConfiguration` parametresi eklendi.
      - Bu parametre, havuz ağ ayarlarını yapılandırmanıza olanak sağlar.
  * Parametreler `New-AzureBatchCertificate` olarak güncelleştirildi.
    - `Password` parametresi, `SecureString` olacak şekilde değiştirildi.
  * Parametreler `New-AzureBatchComputeNodeUser` olarak güncelleştirildi.
    - `Password` parametresi, `SecureString` olacak şekilde değiştirildi.
  * Parametreler `Set-AzureBatchComputeNodeUser` olarak güncelleştirildi.
    - `Password` parametresi, `SecureString` olacak şekilde değiştirildi.
  * `Name` parametresi `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent` ve `Remove-AzureBatchNodeFile` üzerinde `Path` olarak yeniden adlandırıldı.
    - `Path` parametresi için bir `Name` diğer adı oluşturuldu.
  * Nesnelerde yapılan değişiklikler
    - Lütfen tam liste için Batch değişiklik günlüğüne bakın
  * Azure Active Directory tabanlı kimlik doğrulaması için destek eklendi.
    - Azure Active Directory kimlik doğrulamasını kullanmak için `Get-AzureRmBatchAccount` cmdlet'ini kullanarak bir `BatchAccountContext` nesnesi alın ve bu `BatchAccountContext` değerini bir Batch hizmeti cmdlet’inin `-BatchContext` parametresine ekleyin. Azure Active Directory kimlik doğrulaması, `PoolAllocationMode = UserSubscription` özelliğine sahip hesaplar için zorunludur.
    - Mevcut hesaplar veya `PoolAllocationMode = BatchService` ile oluşturulan yeni hesaplar için, `Get-AzureRmBatchAccoutKeys` cmdlet'i ile bir `BatchAccountContext` nesnesi alarak paylaşılan anahtar kimlik doğrulamasını kullanmaya devam edebilirsiniz.
* İşlem
  * Azure Disk Şifrelemesi Uzantı Komutları
    - Yeni 'Set-AzureRmVmDiskEncryptionExtension' Parametresi olan '-EncryptFormatAll' biçim veri disklerini şifreler
    - Yeni 'Set-AzureRmVmDiskEncryptionExtension' Parametreleri olan '-ExtensionPublisherName' ve '-ExtensionType', uzantının diğer sürümlerine geçişe olanak tanır
    - Yeni 'Disable-AzureRmVmDiskEncryption' Parametreleri olan '-ExtensionPublisherName' ve '-ExtensionType', uzantının diğer sürümlerine geçişe olanak tanır
    - Yeni 'Get-AzureRmVmDiskEncryptionStatus' Parametreleri olan '-ExtensionPublisherName' ve '-ExtensionType', uzantının diğer sürümlerine geçişe olanak tanır
* DataLakeAnalytics
  * Bu yayında DataLakeAnalytics’te yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
  * İki Get-AzureRmDataLakeAnalyticsAccount OutputTypes seçeneğinden biri değiştirildi
    - List\<DataLakeAnalyticsAccount> - List\<PSDataLakeAnalyticsAccountBasic>
    - PSDataLakeAnalyticsAccountBasic özellikleri, DataLakeAnalyticsAccount özelliklerinin katı bir alt kümesidir
    - DataLakeAnalyticsAccount içindeki ek özellikler hizmet tarafından döndürülmez.  Bu nedenle, bu değişiklik bu durumu doğru şekilde yansıtmalıdır. Bu ek özellikler hala PSDataLakeAnalyticsAccountBasic içindedir, ancak Eski olarak etiketlenir.
  * İki Get-AzureRmDataLakeAnalyticsJob OutputTypes seçeneğinden biri değiştirildi
    - List\<JobInformation> - List\<PSJobInformationBasic>
    - PSJobInformationBasic özellikleri, JobInformation özelliklerinin katı bir alt kümesidir
    - JobInformation içindeki ek özellikler hizmet tarafından döndürülmez.  Bu nedenle, bu değişiklik bu durumu doğru şekilde yansıtmalıdır. Bu ek özellikler hala PSJobInformationBasic içindedir, ancak Eski olarak etiketlenir.
* DataLakeStore
  * Bu yayında DataLakeStore’da yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
  * İki Get-AzureRmDataLakeStoreAccount OutputTypes seçeneğinden biri değiştirildi
    - List\<PSDataLakeStoreAccount> - List\<PSDataLakeStoreAccountBasic>
    - PSDataLakeStoreAccountBasic özellikleri, PSDataLakeStoreAccount özelliklerinin katı bir alt kümesidir
    - PSDataLakeStoreAccount içindeki ek özellikler hizmet tarafından döndürülmez.  Bu nedenle, bu değişiklik bu durumu doğru şekilde yansıtmalıdır. Bu ek özellikler hala PSDataLakeStoreAccountBasic içindedir, ancak Eski olarak etiketlenir.
* Dns
  * Azure DNS'de CAA kayıt türleri desteği
    - CAA kayıt türündeki tüm işlemleri destekler
* EventHub
  * Bu yayında EventHub’da yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
* Insights
  * Bu yayında Insights’ta yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
* Ağ
  * Bu yayında Network’te yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
  * Belirtilen bir Azure bölgesi için kullanılabilir internet hizmet sağlayıcılarını listelemeyi sağlayan cmdlet eklendi
    - Get-AzureRmNetworkWatcherReachabilityProvidersList
  * Belirtilen bir konumdan Azure bölgelerine internet hizmet sağlayıcılarının göreli gecikme puanını almayı sağlayan cmdlet eklendi
    - Get-AzureRmNetworkWatcherReachabilityReport
* Profil
  - Set-AzureRmDefault
    - Varsayılan kaynak grubunu ayarlamak için bu cmdlet'i kullanın.  Bunun yapılması, bazı cmdlet’ler için -ResourceGroup parametresini isteğe bağlı hale getirir ve varsayılan bir grup belirtilmediğinde varsayılan seçeneği kullanır
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - Belirtilen kaynak grubu abonelikte mevcutsa, bu kaynak grubu varsayılan olarak ayarlanır.  Aksi halde, kaynak grubu oluşturulur ve sonra varsayılan olarak ayarlanır.
  - Get-AzureRmDefault
    - Geçerli varsayılan kaynak grubunu (ve gelecekteki diğer varsayılanları) almak için bu cmdlet'i kullanın.
    - ```Get-AzureRmDefault -ResourceGroup```
  - Clear-AzureRmDefault
    - Geçerli varsayılan kaynak grubunu kaldırmak için bu cmdlet'i kullanın
    - ```Clear-AzureRmDefault -ResourceGroup```
  - Add-AzureRmEnvironment ve Set-AzureRmEnvironment
    - Batch hizmeti için kimlik doğrulama belirteçleri alırken kullanılacak Azure Batch Active Directory hedef kitlesini belirtmenize olanak tanıyan BatchAudience parametresini ekleyin.
* RecoveryServices.Backup
  * Anlık dosya kurtarmayı gerçekleştirmeyi sağlayan cmdlet'ler eklendi.
    - Get-AzureRmRecoveryServicesBackupRPMountScript
    - Disable-AzureRmRecoveryServicesBackupRPMountScript
  * RecoveryServices.Backup SDK’sı en son sürüme güncelleştirildi
  * Azure VM iş yüküne yönelik testler, test çalıştırmaları için gereken tüm ayarlar testler tarafından yapılacak şekilde güncelleştirildi.
  * [https://github.com/Azure/azure-powershell/issues/3164](https://github.com/Azure/azure-powershell/issues/3164) sorununu düzeltir
* RecoveryServices.SiteRecovery
  * ASR VMware için Azure Site Recovery’de yapılan değişiklikler (cmdlet’ler şu anda Enterprise-Enterprise, Enterprise-Azure, HyperV-Azure arasındaki işlemleri desteklemektedir)
    - New-AzureRmRecoveryServicesAsrPolicy
    - New-AzureRmRecoveryServicesAsrProtectedItem
    - Update-AzureRmRecoveryServicesAsrPolicy
    - Update-AzureRmRecoveryServicesAsrProtectionDirection
  * AAD tabanlı kasa desteği eklendi
  * VCenter kaynaklarını yönetmeyi sağlayan cmdlet’ler eklendi
    - Get-AzureRmRecoveryServicesAsrVCenter
    - New-AzureRmRecoveryServicesAsrVCenter
    - Remove-AzureRmRecoveryServicesAsrVCenter
    - Update-AzureRmRecoveryServicesAsrVCenter
  * Diğer cmdlet'ler eklendi
    - Get-AzureRmRecoveryServicesAsrAlertSetting
    - Get-AzureRmRecoveryServicesAsrEvent
    - New-AzureRmRecoveryServicesAsrProtectableItem
    - Set-AzureRmRecoveryServicesAsrAlertSetting
    - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
    - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
    - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
    - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
  - Bu yayında ServiceBus’ta yapılan önemli değişiklikler için lütfen geçiş kılavuzuna bakın
* Sql
  * Veritabanındaki zaman uyumsuz updateslo işlemini listeleme ve iptal etme desteği eklendi
    - Mevcut Get-AzureRmSqlDatabaseActivity cmdlet’i DB updateslo işlem durumunu döndürecek şekilde güncelleştirildi.
    - Veritabanında zaman uyumsuz updateslo işlemini iptal etmeyi sağlayan yeni Stop-AzureRmSqlDatabaseActivity cmdlet’i eklendi.
  * Veritabanları ve elastik havuzlar için Bölge Artıklığı desteği eklendi
    - New-AzureRmSqlDatabase cmdlet’ine ZoneRedundant anahtar parametresi eklendi
    - Set-AzureRmSqlDatabase cmdlet’ine ZoneRedundant anahtar parametresi eklendi
    - New-AzureRmSqlElasticPool cmdlet’ine ZoneRedundant anahtar parametresi eklendi
    - Set-AzureRmSqlElasticPool cmdlet’ine ZoneRedundant anahtar parametresi eklendi
  * Sunucu DNS Diğer Adları için destek eklendi
    - Sunucu ve diğer ada göre sunucu dns diğer adlarını ya da bir Azure Sql Server’a ait sunucu dns diğer adlarının listesini alan Get-AzureRmSqlServerDnsAlias cmdlet’i eklendi.
    - Belirli bir Azure Sql Server için yeni sunucu dns diğer adları oluşturan New-AzureRmSqlServerDnsAlias cmdlet’i eklendi
    - Sunucu dns diğer adlarının işaret ettiği bir Azure Sql Server’ı güncelleştirmeye olanak tanıyan Set-AzurermSqlServerDnsAlias cmdlet’i eklendi
    - Azure Sql Server için sunucu dns diğer adını kaldıran Remove-AzureRmSqlServerDnsAlias cmdlet’i eklendi
* Azure Depolama
  * Azure Depolama İstemci Kitaplığı 8.5.0 ve Azure Depolama DataMovement Kitaplığı 0.6.3 sürümüne yükseltildi
  * Dosya Paylaşımı Anlık Görüntüsü Destek Özelliği eklendi
    - Get-AzureStorageShare cmdlet’ine 'SnapshotTime' parametresi eklendi
    - Remove-AzureStorageShare cmdlet’ine 'IncludeAllSnapshot' parametresi eklendi
