---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 189b360f8825b7de93b67b0b2cbe670d00187327
ms.sourcegitcommit: 6071038ed955107220a01156550a541bf68d0266
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2020
ms.locfileid: "89241364"
---
# <a name="release-notes"></a>Sürüm notları

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.

---
## <a name="6130---november-2018"></a>6.13.0 - Kasım 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

#### <a name="azurermautomation"></a>AzureRM.Automation
* Swagger tabanlı Azure Otomasyon cmdlet'leri
* Güncelleştirme Yönetimi cmdlet'leri eklendi
* Kaynak Denetimi cmdlet'leri eklendi
* Remove-AzureRmAutomationHybridWorkerGroup cmdlet'i eklendi
* DSC Kayıt Düğümü komutu düzeltildi

#### <a name="azurermcompute"></a>AzureRM.Compute
* SystemAssigned kimliği için kimlik sorunu düzeltildi
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Market cmdlet'leri için örnekler açıklaması güncelleştirildi

#### <a name="azurermnetwork"></a>AzureRM.Network
* New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet'leri eklendi
* Desteklenen AzureFirewall Ağ Protokollerine yeniden ICMP eklendi
* Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi; hedef kimlik, adres ve bağlantı noktasında doğrulama eklendi.
* VirtualNetwork eşlemesinde bellek kullanımıyla ilgili sorunlar düzeltildi

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Korumalı dosya paylaşımı için ilke değiştirme sorunu düzeltildi.
* İlke saat dilimi büyük harfe dönüştürüldü.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* New-AzureRmRecoveryServicesAsrProtectableItem cmdlet'indeki örnek düzeltildi
* Tür eşlemesinde güncelleştirme bağımlılıkları sorunu

#### <a name="azurermrelay"></a>AzureRM.Relay
* Kullanıcının New-AzureRmRelayKey cmdlet'ine KeyValue sağlamasına olanak tanıyan isteğe bağlı -KeyValue parametresi eklendi.

#### <a name="azurermresources"></a>AzureRM.Resources
* `New-AzureRmPolicyAssignment` ve `Set-AzureRmPolicyAssignment` cmdlet'lerindeki kaynak kimliğiyle ilgili parametrelerin yardım belgeleri güncelleştirildi
* New-AzureRmPolicyDefinition cmdlet'ine -Metadata kullanan bir örnek eklendi
* NetStandard'da Tag anahtarında büyük/küçük harf kullanımının korunmasına yönelik düzeltme yapıldı: #7678 #7703

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Hataya neden olan değişiklikler yayınlanacağından kullanımdan kaldırılacak özellikleri belirten iletiler eklendi

#### <a name="azurermsql"></a>AzureRM.Sql
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

## <a name="6120---november-2018"></a>6.12.0 - Kasım 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi
* Connect-AzureRmAccount cmdlet'indeki TenantId parametresi Tenant olarak yeniden adlandırıldı ve TenantId için diğer ad eklendi
* Connect-AzureRmAccount için TenantId açıklaması güncelleştirildi
* Kiracı etki alanı sağlanırken başarısız oturum açma durumunda gösterilen hata iletisi düzeltildi
    - https://github.com/Azure/azure-powershell/issues/6936
* Kiracıda abonelikleri olmayan hesaplar için bağlam adı çakışmasıyla ilgili sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/7453
* MSI kullanırken DataLake uç noktalarıyla ilgili sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/7462
* Bağlantı olmadığında 'Disconnect-AzureRmAccount' oluşturulmasına neden olan sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a>AzureRM.Automation
* Cmdlet DLL dosya adı Microsoft.Azure.Commands.Automation.dll olarak değiştirildi

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Get-AzureRmCognitiveServicesAccountSkus işlemi eklendi.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Add-AzureRmVmssVMDataDisk ve Remove-AzureRmVmssVMDataDisk cmdlet'leri eklendi
* Get-AzureRmVMImage, AutomaticOSUpgradeProperties gösteriyor
* Json biçiminde SetAzureRmVMChefExtension -BootstrapOptions ve -JsonAttribute seçeneği değerlerinin ayarlanmamasıyla ilgili hata düzeltildi.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* DataLake paketi 1.1.10'a güncelleştirildi.
* Çok iş parçacıklı işlemlere varsayılan Concurrency değeri eklendi.

#### <a name="azurerminsights"></a>AzureRM.Insights
* 7267 numaralı (Otomatik ölçeklendirme alanı) sorun düzeltildi
    - Yeni otomatik ölçeklendirme kuralı oluşturma sırasında numaralandırılmış parametrelerin düzgün ayarlanmamasıyla ilgili sorunlar (bunlar her zaman varsayılan değere ayarlanıyordu).
* Set-AzureRMDiagnosticSetting'in ayar oluşturma sırasında kategorilerin açıkça belirtilmesini gerektirmesiyle ilgili 7513 numaralı [Insights] sorun düzeltildi
    - Artık cmdlet oluşturma sırasında açık kategori gösteriminin etkinleştirilmesini gerektirmiyor; başka bir deyişle belgelerinde belirtildiği gibi çalışıyor

#### <a name="azurermnetwork"></a>AzureRM.Network
* Aşağıdaki parametrelerde PeeringType parametresi zorunlu parametre olarak değiştirildi:-
    - Get-AzureRmExpressRouteCircuitRouteTable
    - Get-AzureRmExpressRouteCircuitARPTable
    - Get-AzureRmExpressRouteCircuitRouteTableSummary
    - Get-AzureRMExpressRouteCrossConnectionArpTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* İlke düzeltme cmdlet'leri eklendi

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Kurtarma hizmetlerinde Azure dosya paylaşımları için destek eklendi.

#### <a name="azurermresources"></a>AzureRM.Resources
* [https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) düzeltmesi
    - 'Get-AzureRmResource' için '-ResourceId' parametresi kullanılarak kaynakların listelenmesine olanak tanındı

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* PSServiceBusMigrationConfigurationAttributes'e Geçiş durumunun bilinmesine yardımcı olacak salt okunur MigrationState özelliği eklendi.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Linux Vmss'ye sertifika ekleme sorunu düzeltildi.
* 'Add-AzureRmServiceFabricClusterCertificate' düzeltildi
    - Yeni sertifikadan doğru parmak izi kullanıyor (Azure/service-fabric-issues#932).
    - Özel durum doğru görüntüleniyor (Azure/service-fabric-issues#1054).
* 'Update-AzureRmServiceFabricDurability', Vmss CreateOrUpdate işlemini başlatmadan önce küme yapılandırmasını güncelleştirecek şekilde düzeltildi.

## <a name="6110---october-2018"></a>6.11.0 - Ekim 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* CloudShell’de Get-AzureRmSubscription sorunu çözüldü
* ClientRuntime’ın en son sürümünü kullanacak şekilde ortak kod güncelleştirildi

#### <a name="azurermbackup"></a>AzureRM.Backup
* Azure Backup cmdlet’leri kullanım dışı bırakıldı.

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVm' için basit parametre kümesi kullanıldığında hızlandırılmış ağların açılacağı VM boyutları beyaz listesine yeni boyutlar eklendi
* Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Sanal Ağ Kuralları desteği ekleme
    - Get-AzureRmDataLakeStoreVirtualNetworkRule: Azure Data Lake Store sanal ağ kuralını alır veya listeler.
    - Add-AzureRmDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabına sanal ağ kuralı ekler.
    - Set-AzureRmDataLakeStoreVirtualNetworkRule: Belirtilen Data Lake Store hesabındaki belirtilen sanal ağ kuralını değiştirir.
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule: Bir Azure Data Lake Store sanal ağ kuralını siler.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Test-AzureRmNetworkWatcherConnectivity cmdlet'i güncelleştirildi, arka uca protokol değerini geçiriyor.
* Tüm cmdlet'lere ResourceName bağımsız değişken tamamlayıcısı eklendi.

#### <a name="azurermresources"></a>AzureRM.Resources
* Get-AzureRMRoleDefinition cmdlet'inin anlaşılmaz bir özel durum oluşturmasına neden olan hata (varsayılan profilin içinde abonelik olmadığında ve hiçbir kapsam belirtilmediğinde), senaryoya anlamlı bir özel durum eklenerek düzeltildi. Ayrıca varsayılan parametre kümesi 'RoleDefinitionNameParameterSet' olarak ayarlandı.

## <a name="6100---october-2018"></a>6.10.0 - Ekim 2018
#### <a name="azurestorage"></a>Azure Depolama
* Hedefte meta veri sorunu olduğunda Fix Copy Blob/File meta verileri kopyalamayacak
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Mevcut hesap olmadan Get-AzureRmCognitiveServicesAccountSkus desteği.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Get-AzureRmVM -ResourceGroupName <rg> gerektiğinde 50'den fazla sonuç döndürecek şekilde düzeltildi
* New-AzureRmVmss cmdlet'inin yardımına 'SimpleParameterSet' örneği eklendi.
* Azure Disk Şifrelemesi ilerleme durumu iletisindeki yazım hatası düzeltildi

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK sürümü 2.3.0'a güncelleştirildi.

#### <a name="azurermnetwork"></a>AzureRM.Network
* NetworkProfile işlevselliği eklendi. yeni cmdlet'ler eklendi
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* Alt Ağ Modeline hizmet ilişki bağlantısı eklendi
* New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap cmdlet'leri eklendi
* Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig cmdlet'leri eklendi

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Bundan sonra Size parametresi olarak her dizeye izin veriliyor. PSArgumentCompleter açılan listesine P5 eklendi

#### <a name="azurermresources"></a>AzureRM.Resources
* Set-AzureRmPolicyDefinition'a eksik -Mode parametresi eklendi
* Origin öğesi User içeren işlemler için Get-AzureRmProviderOperation commandlet hatası düzeltildi

#### <a name="azurermsql"></a>AzureRM.Sql
* Bazı yedekleme cmdlet'lerinin geçerli Azure aboneliğini tanıyamamasına neden olan sorun düzeltildi

#### <a name="azurermstorage"></a>AzureRM.Storage
* Belirli bir konumunun Depolama kaynağı kullanımını alma desteği ve genel Depolama kayrağı kullanımını almak için uyarı iletisi ekleme kullanımdan kalktı.
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Yeni Get-AzureRMWebAppContainerContinuousDeploymentUrl Cmdlet'i - Kapsayıcı Sürekli Dağıtım Web Kancası URL'sini alıyor
* Yeni New-AzureRMWebAppContainerPSSession ve Enter-WebAppContainerPSSession Cmdlet'leri - Windows kapsayıcı uygulamasında PowerShell uzak oturumunu başlatıyor

## <a name="690---september-2018"></a>6.9.0 - Eylül 2018
#### <a name="general"></a>Genel
* AzureRM.SignalR, AzureRM toplu modülüne eklendi

#### <a name="azurermprofile"></a>AzureRM.Profile
* Depolama ortak kodunda küçük değişiklikler yapıldı
* Yardım dosyaları tüm parametre türlerini içerecek şekilde güncelleştirildi.
* ServicePrincipalCertificateWithSubscriptionId parametre kümesindeki -ServicePrincipal parametresi zorunlu olmaktan çıkarıldı

#### <a name="azurestorage"></a>Azure Depolama
* OAuth ile Depolama Bağlamı oluşturma desteği eklendi.
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* CDN fiyatlandırma SKU'suna Standard_Microsoft eklendi.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Keyvault ve Storage bağımlılıkları ortak bağımlılıklara taşındı
* AEM cmdlet'lerine daha fazla sanal makine boyutu için destek eklendi
* New-AzureRmVmssIpConfig cmdlet'ine Add PublicIPPrefix parametresi eklendi
* Invoke-AzureRmVMRunCommand cmdlet'ine ResourceId parametresi eklendi
* Invoke-AzureRmVmssVMRunCommand cmdlet'i eklendi

#### <a name="azurermdns"></a>AzureRM.Dns
* DNS kaydı oluşturma işlemi sırasında diğer ad kaydı desteği eklendi

#### <a name="azurerminsights"></a>AzureRM.Insights
* 6833 ve 7102 numaralı sorunlar giderildi (Tanılama Ayarları bölümü)
    - Tanılama ayarlarını oluşturma ve listeleme/alma sırasında karşılaşılan varsayılan ad 'service' sorunları
    - Kategoriye sahip tanılama ayarı oluşturma sorunları
* Ölçümler zaman dilimi parametreleri için kullanımdan kaldırma iletisi eklendi
    - Zaman dilimi parametreleri yine kabul ediliyor (bu bir hataya neden olan değişiklik değil) ancak yalnızca PT1M geçerli olduğu için bu parametreler arka uçta yoksayılıyor

#### <a name="azurermnetwork"></a>AzureRM.Network
* LoadBalancer cmdlet'lerinde değişiklikler yapıldı
  - LoadBalancerInboundNatPoolConfig: IdleTimeoutInMinutes, EnableFloatingIp ve EnableTcpReset parametreleri eklendi
  - LoadBalancerInboundNatRuleConfig: EnableTcpReset parametresi eklendi
  - LoadBalancerRuleConfig: EnableTcpReset parametresi eklendi
  - LoadBalancerProbeConfig: Protocol parametresi için "Https" değeri desteği eklendi
* Yeni LoadBalancer alt kaynağı OutboundRule için yeni komutlar eklendi
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* PSNetworkInterface için yeni HostedWorkloads özelliği eklendi
* Özellik için yeni cmdlet'ler eklendi: ARM aracılığıyla Azure Güvenlik Duvarı
  - Get-AzureRmFirewall eklendi
  - Set-AzureRmFirewall eklendi
  - New-AzureRmFirewall eklendi
  - Remove-AzureRmFirewall eklendi
  - New-AzureRmFirewallApplicationRuleCollection eklendi
  - New-AzureRmFirewallApplicationRule eklendi
  - New-AzureRmFirewallNatRuleCollection eklendi
  - New-AzureRmFirewallNatRule eklendi
  - New-AzureRmFirewallNetworkRuleCollection eklendi
  - New-AzureRmFirewallNetworkRule eklendi
* Application Gateway'de Güvenilen Kök sertifika ve Otomatik ölçeklendirme yapılandırması desteği eklendi
  - Yeni cmdlet'ler eklendi:
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - Cmdlet'ler isteğe bağlı -TrustedRootCertificate parametresiyle güncelleştirildi
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - Cmdlet'ler isteğe bağlı -AutoscaleConfiguration parametresiyle güncelleştirildi
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* Arabirim Uç Noktası için Get-AzureInterfaceEndpoint cmdlet'i eklendi
* Bir alt ağda birden fazla adres ön eki için destek eklendi. Cmdlet'ler güncelleştirildi:
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* Alt ağ temsilcisi seçme cmdlet'leri eklendi.
  - New-AzureRmDelegation: Bir alt ağa eklenebilecek yeni bir temsilci oluşturur
  - Remove-AzureRmDelegation: Bir alt ağı alır ve belirtilen temsilci adını o alt ağdan kaldırır
  - Add-AzureRmDelegation: Bir alt ağı alır ve belirtilen hizmet adını o alt ağa temsilci olarak ekler
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Yönetilen disk desteği

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Insights bağımlılığı güncelleştirildi.

#### <a name="azurermresources"></a>AzureRM.Resources
* New-AzureRmResourceGroupDeployment cmdlet'i yeni RollbackAction parametresi eklenerek güncelleştirildi
    - Yeni parametreyle OnErrorDeployment desteği eklendi.
* İlke atamalarında yönetilen kimlik desteği eklendi.
* Varsayılan değerlere sahip parametrelerin artık 'New-AzureRmPolicyAssignment' ile ilke atama işlemi sırasında belirtilmesi zorunlu değil
* İlke diğer adlarını almak için yeni Get-AzureRmPolicyAlias cmdlet'i eklendi

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* 7161 numaralı sorun düzeltildi

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* SKU adları Free_F1 ve Standard_S1 olarak güncelleştirildi
* PSSignalRResource nesnesine sürüm alanı, PSSignalRKeys nesnesine de bağlantı dizesi eklendi.

#### <a name="azurermstorage"></a>AzureRM.Storage
* AzureRm.Storage için Değiştirilemezlik İlkesi desteği eklendi
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* İki yeni cmdlet eklendi: Get-AzureRmDeletedWebApp ve Restore-AzureRmDeletedWebApp
* Windows kapsayıcısı ile App Service planı oluşturmak için New-AzureRmAppServicePlan -HyperV anahtarı eklendi
* New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Windows kapsayıcı uygulaması oluşturmak ve yönetmek için yeni parametreler (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) eklendi

## <a name="681---august-2018"></a>6.8.1 - Ağustos 2018
#### <a name="general"></a>Genel
* Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.
* Ortak çalışma zamanı bütünleştirilmiş kodları güncelleştirildi

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.
* [https://github.com/Azure/azure-powershell/issues/6603](https://github.com/Azure/azure-powershell/issues/6603 ) sorunu düzeltildi
    - Import-AzureRmApiManagementApi ve *-AzureRmApiManagementCertificate cmdlet’leri artık göreli yolları işleyebiliyor
* [https://github.com/Azure/azure-powershell/issues/6879](https://github.com/Azure/azure-powershell/issues/6879 ) sorunu düzeltildi
    - CertificateInformation, Set-AzureRmApiManagement cmdlet’inin düzgün çalışmasını sağlayan, ayarlanabilir bir özelliktir. 4\.0.4-preview nuget’e yükselterek düzeltildi
* [https://github.com/Azure/azure-powershell/issues/6853](https://github.com/Azure/azure-powershell/issues/6853 ) sorunu düzeltildi
    - Odata filtresi Ürün üzerinde Ada Göre Arama için düzeltildi
* [https://github.com/Azure/azure-powershell/issues/6814](https://github.com/Azure/azure-powershell/issues/6814 ) sorunu düzeltildi
    - Odata filtresi API üzerinde Ada Göre Arama için düzeltildi
* Azure İzleyici günlükçüsüne yönelik destek eklendi


#### <a name="azurermcompute"></a>AzureRM.Compute
* Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.
* Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi
* Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.
* Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi

#### <a name="azurermnetwork"></a>AzureRM.Network
* Varsayılan cmdlet çıkış gösterimi, tablo görünümü olarak değiştirildi

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi


#### <a name="azurermresources"></a>AzureRM.Resources
* Market’ten yönetilen uygulama oluşturmayla ilgili sorun düzeltildi.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Düzeltilen sorunlar
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Çoklu değer yönlendirme yöntemi desteği eklendi
    - Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi
* Alt ağ yönlendirme yöntemi desteği eklendi
    - Uç noktalarda IP adresi aralıkları (alt ağları) desteği
* Profillerde Özel Üst Bilgi desteği eklendi
* Profillerde Beklenen durum kodu aralığı desteği eklendi
* Uç noktalarda Özel Üst Bilgi desteği eklendi

## <a name="680---august-2018"></a>6.8.0 - Ağustos 2018
#### <a name="general"></a>Genel
* Varsayılan kaynak gruplarının ayarlanmamasına neden olan sorun düzeltildi.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Connect-AzureRmAccount sırasında döndürülen belirteçlere sona erme özelliği eklendi

#### <a name="azurermcompute"></a>AzureRM.Compute
* Hata çıktısında hedefin eksik olmasına neden olan sorun düzeltildi.
* Yönetilen diske sahip VM için depolama hesabı türüyle ilgili sorun düzeltildi
* Azure Çin gibi diğer ortamlar için AEM Uzantı cmdlet'leri düzeltildi

#### <a name="azurermiothub"></a>AzureRM.IotHub
* New-AzureRmIotHubExportDevices ve New-AzureRmIotHubImportDevices için düzeltme örnekleri

#### <a name="azurermnetwork"></a>AzureRM.Network
* Varsayılan model gösterimi tablo görünümü olarak değiştirildi

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Duraklatılmış kapasite ölçeklendirilmeye çalışılırken Update-AzureRmPowerBIEmbeddedCapacity üzerindeki hata düzeltildi

#### <a name="azurermresources"></a>AzureRM.Resources
* Marketten yönetilen uygulamayla ilgili sorun düzeltildi.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Sorunlar için düzeltme
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Çoklu değer yönlendirme yöntemi desteği
    - Çoklu değer yönlendirme için yeni 'MaxReturn' parametresi
* Alt ağ yönlendirme yöntemi desteği
    - Uç noktalarda IP adresi aralıkları (alt ağları) desteği
* Profillerde Özel Üst Bilgi desteği
* Profillerde Beklenen durum kodu aralığı desteği
* Uç noktalarda Özel Üst Bilgi desteği

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Varsayılan kaynak gruplarının yanlış ayarlanmasına neden olan sorun düzeltildi.

## <a name="670---august-2018"></a>6.7.0 - Ağustos 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.
* Bağlam çakışmasını önlemek için varsayılan bağlam adına kullanıcı kimliği eklendi
    - https://github.com/Azure/azure-powershell/issues/6489
* Bağlam #6398 seçerken sorunlara neden olan Clear-AzureRmContext ile ilgili sorunlar giderildi
* 'Connect-AzureRmAccount' için kiracı etki alanının '-TenantId' parametresine geçirilmesi etkinleştirildi
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure Depolama
* Azure Dosya Paylaşımı kotasındaki 5 TB'lık sınır kaldırıldı
* Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermbatch"></a>AzureRM.Batch
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermbilling"></a>AzureRM.Billing
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.
* New-AzureRmVmssConfig’e EvictionPolicy parametresi eklendi
* Hiçbir konum belirtilmediyse New-AzureRmVm’nin DiskFileParameterSet parametresinde varsayılan konum kullanılıyor.
* Save-AzureRmVMImage cmdlet'inde parametre açıklaması düzeltildi
* Singlepass ile ilgili bazı senaryolarda Get-AzureRmVMDiskEncryptionStatus cmdlet’i düzeltildi

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* DebugPreference Powershell komut satırından ayarlandığında hata ayıklama düzeltildi
* Set-AzureRmDataLakeStoreItemAcl örneği güncelleştirildi
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.
* Set-AzureRmDataLakeStoreItemAclEntry örneği güncelleştirildi

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermdns"></a>AzureRM.Dns
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermmedia"></a>AzureRM.Media
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Set-AzureRmLocalNetworkGateway örneği eklendi
* Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey ve New-AzureRmVirtualNetworkGatewayConnection için örnek ve açıklamalar eklendi
* Remove-AzureRmVirtualNetworkGatewayIpConfig ve Reset-AzureRmVirtualNetworkGateway örnekleri eklendi
* Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi
* Set-AzureRmVirtualNetworkGatewayConnectionSharedKey örneği eklendi
* Set-AzureRmVirtualNetworkGatewayConnection örneği eklendi
* ApplicationSecurityGroup, RouteTable ve Usage için en son kod oluşturucu kullanılarak cmdlet’ler yeniden oluşturuldu
* Varolmayan bir alt ağ alma girişiminde bulunulduğunda Get-AzureRmVirtualNetworkSubnetConfig cmdlet'inin hata iletisi netleştirildi

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Get-AzureRmRecoveryServicesBackItem cmdlet’ine ilke filtresi eklendi. Komut, verilen ilke kimliği tarafından korunan yedekleme öğelerinin listesini döndürüyor.
* Microsoft.Azure.Management.RecoveryServices.Backup, sürüm 3.0.0 önizlemesine güncelleştirildi.
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.
* Restore-AzureRmRecoveryServicesBackupItem’e TargetResourceGroupName parametresi eklendi. Yönetilen disklerin geri yüklendiği kaynak grubu. Yönetilen disklerle yapılan VM yedeklemesi için geçerlidir.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermresources"></a>AzureRM.Resources
* Abonelik kapsamındaki şablon dağıtımı destekleniyor. Yeni Cmdlet’ler eklendi:
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Set-AzureRmResource’a bağlam geçirilirken hata oluşmasına neden olan sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/5705
* New-AzureRmResourceGroupDeployment cmdlet'indeki örnek düzeltildi
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermsql"></a>AzureRM.Sql
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermtags"></a>AzureRM.Tags
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Azure ClientRuntime'ın en son sürümüne güncelleştirildi.

## <a name="660---july-2018"></a>6.6.0 - Temmuz 2018
#### <a name="general"></a>Genel
* Tüm yardım dosyaları tam parametre türleriyle doğru giriş/çıkış türlerini içerecek şekilde güncelleştirildi.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Kaynağın geçerli yapılandırmasının hedef kaynakla uyumlu olduğunu doğrulayabilmek için Common.Strategy kitaplığı güncelleştirildi.
* Common.Storage'a ps1xml türleri eklendi

#### <a name="azurestorage"></a>Azure Depolama
* DefaultProfile’dan Depolama Bağlamı almak için destek eklendi
* Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* [https://github.com/Azure/azure-powershell/issues/6370](https://github.com/Azure/azure-powershell/issues/6370 ) sorunu düzeltildi
    - PsApiManagementApi'yi ApiContract'e çevirmek için Automapper hatası düzeltildi
* [https://github.com/Azure/azure-powershell/issues/6515](https://github.com/Azure/azure-powershell/issues/6515 ) sorunu düzeltildi
    - Kodlama Türü ile aşırı yüklemeyi önlemek için File.Save hatası düzeltildi
* [https://github.com/Azure/azure-powershell/issues/6560](https://github.com/Azure/azure-powershell/issues/6560 ) sorunu düzeltildi
    - apiId üzerindeki desen özel durumunu düzelten 4.0.3 Nuget sürümüne yükseltildi

#### <a name="azurermcompute"></a>AzureRM.Compute
* PremiumLRS depolama hesap türü yeniden adlandırması nedeniyle New-AzureRmVm'de DiskFileParameterSet kullanılarak sanal makine oluşturmanın başarısız olmasıyla ilgili hata düzeltildi.
* Invoke-AzureRmVMRunCommand cmdlet'i düzeltildi
* Abonelikteki tüm kullanılabilir kümelerin listelenebilmesi için Get-AzureRmAvailabilitySet güncelleştirildi.  (ResouceGroupName parametresi artık isteğe bağlı.)
* Uygun sanal makinelerde Hızlandırılmış Ağı etkinleştirmek için 'New-AzureRmVm' cmdlet'inin SimpleParameterSet öğesi güncelleştirildi.
* Kullanıcının belirttiği LB zaten mevcut olduğunda vmss oluşturmanın başarısız olması için New-AzureRmVmss basit parametre kümesi güncelleştirildi.
* New-AzureRmDisk örneği güncelleştirildi
* 'New-AzureRmVM' için örnek eklendi
* Set-AzureRmVMOSDisk açıklaması güncelleştirildi
* Yazımı ve ön eki düzeltmek amacıyla Set-AzureRmVMBginfoExtension için Örnek 1 güncelleştirildi.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK sürümü 1.1.0'a güncelleştirildi.
* Veri fabrikaları arasında paylaşılan şirket içinde barındırılan tümleştirme çalışma zamanı desteği.
     - Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine yeni -SharedIntegrationRuntimeResourceId parametresi eklendi.
     - Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet'ine isteğe bağlı yeni -LinkedDataFactoryName parametresi eklendi.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* DataPlane SDK'sı (Microsoft.Azure.DataLake.Store) sürümü 1.1.9'a güncelleştirildi

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi

#### <a name="azurerminsights"></a>AzureRM.Insights
* Yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi
* Microsoft.Azure.Management.Monitor SDK 0.19.1-preview kullanımı

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Set-AzureRmKeyVaultAccessPolicy'de yönlendirme sorunu düzeltildi

#### <a name="azurermnetwork"></a>AzureRM.Network
* LoadBalancerInboundNatPoolConfig cmdlet'leri için örnekler eklendi.

#### <a name="azurermresources"></a>AzureRM.Resources
* 'Get-AzureRmResource' için hem etiket adı hem de değer sağlama sorunu düzeltildi
    - https://github.com/Azure/azure-powershell/issues/6765
* 'Set-AzureRmResource' için yönlendirme senaryosu düzeltildi

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Kaldırma cmdlet'lerine InputObject ve ResourceId yöneltmesi güncelleştirildi
* birkaç sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Aşağıdaki cmdlet'lere Sunucu Gelişmiş Tehdit Koruması desteği ekleniyor:
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* Aşağıdaki cmdlet'lere Güvenlik Açığı Değerlendirme desteği ekleniyor:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Remove-AzureRmSqlServerFirewallRulecmdlet'indeki örnek düzeltildi
* Get-AzureSqlSyncGroupLog içinde ABD temelli olmayan kültürde yanlış tarih saat işlemesi düzeltildi

#### <a name="azurermstorage"></a>AzureRM.Storage
* Cmdlet'lerin çıkış türü özelliklerine Ps1XmlAttribute eklendi
* Tablo görünümünde StorageAccount cmdlet'i çıkışı gösteriliyor
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* Tag cmdlet'inin yardımında hatayı deyim kaldırıldı
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 - Temmuz 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* 'Get-AzureRmContextAutosaveSetting' için yardım güncelleştirildi

#### <a name="azurestorage"></a>Azure Depolama
* Salt yazılır Sas belirteciyle Karşıya Yükleme Blobu veya Dosyası desteği
* Set-AzureStorageBlobContent
* Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* AS'ye gerekli ResourceGroupName özelliği eklendi.

#### <a name="azurermautomation"></a>AzureRM.Automation
* 'New-AzureRMAutomationSchedule' için yardım güncelleştirildi ve örnek eklendi

#### <a name="azurermcompute"></a>AzureRM.Compute
* Update/New-AzureRmAvailabilitySet komutlarına -Tag parametresi eklendi
* 'Add-AzureRmVmssExtension' için örnek eklendi
* 'Remove-AzureRmVmssExtension' için örnek eklendi
* 'Set-AzureRmVMAccessExtension' için yardım güncelleştirildi
* New-AzureRmVmss için SimpleParameterSet güncelleştirilerek SinglePlacementGroup varsayılan olarak false değerine ayarlandı ve kullanıcının tek yerleşim grubunda VMSS oluşturmasına olanak tanıyan 'SinglePlacementGroup' geçiş parametresi eklendi.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* PSEventHubDRConfigurationAttributes sınıfına, çoğaltma işlemi devam ederken bekleyen çoğaltma işlemlerinin sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Set-AzureRmKeyVaultAccessPolicy için hata iletisi güncelleştirildi

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* New-AzureRmLogicApp’te "parametre kümesi çözümlenemedi" hatası düzeltildi

#### <a name="azurermnetwork"></a>AzureRM.Network
* Set/Add-AzureRmVirtualNetworkPeering için birden çok Kiracıdaki Sanal Makineler arasında eşleme etkinleştirildi
* Aşağıdaki cmdlet’ler Application Gateway için güncelleştirildi
    - New-AzureRmApplicationGateway: EnableFIPS bayrağı ve Bölgeler desteği eklendi
    - New-AzureRmApplicationGatewaySku: Yeni Standard_v2 ve WAF_v2 sku'ları eklendi
    - Set-AzureRmApplicationGatewaySku: Yeni Standard_v2 ve WAF_v2 sku'ları eklendi
* RouteTable cmdlet’leri en son oluşturucu sürümüyle yeniden oluşturuldu

#### <a name="azurermrelay"></a>AzureRM.Relay
* Markdown dosyaları güncelleştirildi, örnekteki parametre adı sorunu çözüldü

#### <a name="azurermresources"></a>AzureRM.Resources
* Roleassignment ve roledefinition cmdlet’leri güncelleştirildi:
    - Disk belleğinin parçası olarak yapılan ek roledefinition çağrıları kaldırıldı.
* Get-AzureRmRoleAssignment cmdlet’i düzeltildi
    - -ExpandPrincipalGroups komut parametresi işlevselliği düzeltildi
* '-ResourceType' parametresinin büyük/küçük harfe duyarlı olduğu 'Get-AzureRmResource' sorunu düzeltildi

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Liste cmdlet’lerine top ve skip parametreleri eklendi
* Standard'dan Premium NameSpace'e geçiş cmdlet’leri eklendi :
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* PSServiceBusDRConfigurationAttributes sınıfına, çoğaltma işlemi sürerken beklemede olan çoğaltma işlemi sayısını veren salt okunur 'PendingReplicationOperationsCount' özelliği eklendi

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* 'New-AzureRmServiceFabricCluster' için örnek güncelleştirildi

#### <a name="azurermsql"></a>AzureRM.Sql
* Müşterilerin Sql Server örneğine veya Yönetilen Örneğe TDE Sertifikası ekleyebilmeleri için yeni Management.Sql Cmdlet’leri eklendi
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Artık `Set-AzureRmWebApp -AssignIdentity` ve `Set-AzureRmWebAppSlot -AssignIdentity` false olarak ayarlandığında site object.Removing önizleme etiketinden Identity özelliğini kaldırıyor.
* `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` örneği güncelleştirildi
* `Set-AzureRmWebApp -PhpVersion` geçerli bir php sürümü off değerini destekliyor

## <a name="640---july-2018"></a>6.4.0 - Temmuz 2018
#### <a name="general"></a>Genel
* Modüllerin çoğu için yardım dosyalarındaki OutputType biçimlendirmesi düzeltildi

#### <a name="azurermprofile"></a>AzureRM.Profile
* Temel çıkış türlerine Ps1Xml özniteliği eklendi

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS için IP Etiketi özelliği
    - 'New-AzureRmVmssIpTagConfig' cmdlet'i eklendi
    - New-AzureRmVmssIpConfig cmdlet'ine IpTag parametresi eklendi
* VMSS için Otomatik İşletim Sistemi Geri Alma özelliği eklendi
    - New-AzureRmVmssConfig ve Update-AzureRmVmss cmdlet'lerine DisableAutoRollback parametreleri eklendi
* VMSS için İşletim Sistemi Yükseltme Geçmişi özelliği
    - Get-AzureRmVmss cmdlet'ine OSUpgradeHistory anahtarı parametresi eklendi

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Aşağıdaki komutlarla Katalog ACL'si için destek eklendi:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry ve Set-AzureRmDataLakeStoreItemAcl için iptal desteği ve ilerleme izleme özelliği eklendi
* Export-AzureRmDataLakeStoreChildItemProperties için iptal desteği eklendi
* Özyinelemeli işlemler gerçekleştiren cmdlet'ler için hata ayıklama iletilerinin boşaltılması hatası düzeltildi
* DataLake cmdlet'lerinin test konumu düzeltildi

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Get-AzureRmEventHub ve Get-AzureRmEventHubConsumerGroup Listeleme İşlemleri cmdlet'lerine İsteğe Bağlı MaxCount parametresi eklendi
* New-AzureRmEventHub cmdlet'inde yeni Olay Hub'ı oluşturma sırasında en az bir parametreye ihtiyaç duyma sorunu düzeltildi. Varsayılan Parametre kümesi sağlandı.
* Kullanıcının New-AzureRmEventHubKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Get-AzureRmKeyVault -Tag ile tüm kaynakların döndürülmesine neden olan sorun düzeltildi

#### <a name="azurermnetwork"></a>AzureRM.Network
* Zone-Redundant VirtualNetworkGateways için yeni SKU'lar kullanıma sunuldu
* Özellik için yeni komutlar eklendi: ARM aracılığıyla ExpressRoute İş Ortağı API’leri
    - Get-AzureRmExpressRouteCrossConnection eklendi
    - Set-AzureRmExpressRouteCrossConnection eklendi
    - Add-AzureRmExpressRouteCrossConnectionPeering eklendi
    - Get-AzureRmExpressRouteCrossConnectionPeering eklendi
    - Remove-AzureRmExpressRouteCrossConnectionPeering eklendi
    - Get-AzureRMExpressRouteCrossConnectionArpTable eklendi
    - Get-AzureRMExpressRouteCrossConnectionRouteTable eklendi
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary eklendi

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Get-AzureRmRecoveryServicesBackupStatus cmdlet'i eklendi. Bu cmdlet bir sanal makinenin kimliğini alır ve sanal makinenin abonelik içindeki kasaların koruması altında olup olmadığını denetler. Böyle bir kasa varsa cmdlet, bu kasanın ayrıntılarını belirtir.

#### <a name="azurermresources"></a>AzureRM.Resources
* Get-AzureRmPolicyAssignment cmdlet'leri güncelleştirildi:
    - Yönetim grubu düzeyinde -Scope değerlerini listeleme desteği eklendi
    - Yönetim grubu düzeyinde -Scope değerlerine sahip olan tek atamaları alma desteği eklendi
    - control parametresine -Effective ve -All anahtarları eklendi
* Get/New/Remove/Set-AzureRmPolicyDefinition cmdlet'leri güncelleştirildi
    - Belirli bir yönetim grubuna işlem uygulamayı sağlayan için -ManagementGroupName parametresi eklendi
    - Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi
* Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlet'leri güncelleştirildi
    - Belirli bir yönetim grubuna işlem uygulamayı sağlayan -ManagementGroupName parametresi eklendi
    - Belirli bir aboneliğe işlem uygulamayı sağlayan Add -SubscriptionId parametresi eklendi
* 'New-AzureRmResourceGroupDeployment' içinde 'TemplateParameterObject' kullanırken parametrelerde KeyVault gizli dizi başvurusu desteği eklendi
* 'New-AzureRmADAppCredential' için '-EndDate' parametresinin yoksayılmasına neden olan sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/6505
* 'Add-AzureRmADGroupMember' cmdlet'inin istekte bulunmak için yanlış URL'yi kullandığı sorun düzeltildi
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Kullanıcının New-AzureRmServiceBusKey cmdlet'ine KeyValue eklemesini sağlayan isteğe bağlı -KeyValue parametresi eklendi.

#### <a name="azurermsql"></a>AzureRM.Sql
* New-AzureRmSqlDatabaseRestorePoint yardımında Kullanıcı Tanımlı Geri Yükleme Noktaları netleştirildi
* Birden fazla cmdlet'te -ComputeGeneration parametresinin belgeleri güncelleştirildi

## <a name="630---june-2018"></a>6.3.0 - Haziran 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Enable-AzureRmContextAutoSave için hata iletileri güncelleştirildi
* 'Connect-AzureRmAccount' cmdlet'i eski bir bağlam olmadan çalıştırıldığında her abonelik için bir bağlam oluşturur

#### <a name="azurestorage"></a>Azure Depolama
* Yardım dosyalarına -Permissions parametresi hakkında daha fazla bilgi eklendi.

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'Get-AzureRmVmDiskEncryptionStatus' için veri diski bulunmayan VM'lerde karşılaşılan bir sorun düzeltildi
* Aşağıdaki cmdlet'leri düzeltmek için bilgisayar istemci kitaplığı sürümü güncelleştirildi
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* Aşağıdaki cmdlet'ler 'operation ID' ve 'operation status' bilgilerini doğru gösterecek şekilde düzeltildi:
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzureRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Gerekli olması halinde parametrelerin boş dizeyle değiştirilmesine izin vermek için Update-AzureRmEventGridSubscription cmdlet'i içindeki SubjectBeginsWith/SubjectEndsWith için ValidateNotNullOrEmpty doğrulama koşulları kaldırıldı.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Get-AzureRmKeyVault -Tag çalıştırıldığında etiket döndürülmeme sorunu düzeltildi

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Policy Insights cmdlet'leri genel kullanıma sunuldu
    - API 2018-04-04 sürümünü kullanın
    - PolicyDefinitionReferenceId, Get-AzureRmPolicyStateSummary sonuçlarına eklendi

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* RecoveryServices.Backup cmdlet'lerine -Vault parametresi eklendi. Bu parametre iletildiğinde Set-AzureRmRecoveryServicesContext cmdlet'ini geçersiz kılar.

#### <a name="azurermsql"></a>AzureRM.Sql
* Yardım dosyasındaki Get-AzureRmSqlDatabaseExpanded örneği güncelleştirildi

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Yardım dosyasındaki Add-AzureRmTrafficManagerEndpointConfig bölümü güncelleştirildi

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 'Set-AzureRmWebApp', -AssignIdentity kullanıldığında AppSettings verilerini geçersiz kılmayacak şekilde güncelleştirildi
* 'New-AzureRmWebAppSlot', isteğe bağlı parametre olarak AppServicePlan girişini kabul edecek şekilde güncelleştirildi

## <a name="621---june-2018"></a>6.2.1 - Haziran 2018
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* PSWorkspace modeli Network için tür parametresini kullanacak şekilde güncelleştirildi

## <a name="620---june-2018"></a>6.2.0 - Haziran 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Modülün içeri aktarılması sırasında Newtonsoft.Json 10.0.3 sürümünün yüklenmemesine ilişkin sorun düzeltildi

#### <a name="azurermcompute"></a>AzureRM.Compute
* VMSS VM Güncelleştirme özelliği
    - 'Update-AzureRmVmssVM' ve 'New-AzureRmVMDataDisk' cmdlet’leri eklendi
    - VMSS VM’sine veri diski eklemeyi desteklemek için 'Add-AzureRmVMDataDisk' cmdlet’ine VirtualMachineScaleSetVM parametresi eklendi.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.8.0-preview sürümüne güncelleştirildi:
    - Fabrika deposunu yapılandırma işlemi eklendi
    - QuickBooks LinkedService, consumerKey ve consumerSecret özelliklerini kullanıma sunmak üzere güncelleştirildi
    - SecretBase’ten Object’e birkaç model türü güncelleştirildi
    - Blob Etkinliklerini tetikleme eklendi

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Belgeler örnek çıktı ile güncelleştirildi

### <a name="azurermnetwork"></a>AzureRM.Network
* Ağ İzleyicisi cmdlet’leri üzerindeki Trafik Analizi parametreleri etkinleştirildi

#### <a name="azurermresources"></a>AzureRM.Resources
* 'Get-AzureRmResource' cmdlet’inden döndürülen 'PSResource' nesnesinin 'Properties' özelliğiyle ilgili bir sorun düzeltildi

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Güncelleştirilen ServiceBusQueueJob’ın yeni Kimlik Doğrulaması değerlerini ayarlamamasıyla ilgili bir sorun düzeltildi

### <a name="azurermsql"></a>AzureRM.Sql
* Şu cmdlet’ler isteğe bağlı LicenseType parametresiyle güncelleştirildi:
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 'New-AzureRMWebApp' Strategy kütüphanesindeki ortak algoritmaları kullanmak üzere güncelleştirildi.

## <a name="610---may-2018"></a>6.1.0 - Mayıs 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* 'Clear-AzureRmContext' komutunun çalıştırılmasının boş bir bağlamı önceki varsayılan bağlamın adıyla tutmasına ve böylece kullanıcının eski ad ile yeni bir bağlam oluşturamadığı bir sorun düzeltildi

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* AS’de Ağ geçidi ilişkilendirme/ilişkilendirme kaldırma işlemlerini etkinleştirin.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* ApiVersions, ApiReleases ve ApiRevisions desteği eklendi
* ServiceFabric Arka Ucu desteği eklendi
* Application Insights Günlükçüsü desteği eklendi
* ‘Temel’ sku’yu Api Yönetim hizmetinin geçerli sku’su olarak algılama desteği eklendi
* Özel CA tarafından Kök veya CA olarak yayınlanan Sertifikaları yükleme desteği eklendi
* Özel SSL sertifikalarını KeyVault ve Çoklu ara sunucu ana bilgisayar adlarıyla kabul etme desteği eklendi
* MSI kimliği desteği eklendi
* Url aracılığıyla İlkeleri kabul etmek için destek eklendi NOT: Aşağıdaki cmdlet’ler gelecek sürümde kullanım dışı bırakılacaktır
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Yeni Get-AzureBatchPoolNodeCounts cmdlet’ini yayınlama
* Yeni AzureBatchComputeNodeServiceLogUpload cmdlet’ini yayınlama

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Get-AzureRmConsumptionUsageDetail cmdlet’inde yeni Expand, ResourceGroup, InstanceName, InstanceId, Tags ve Top parametrelerini ekleme

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Export-AzureRmDataLakeStoreChildItemProperties için düzeltme örneği
* Set-AzureRmDataLakeStoreItemAclEntry komutunda Özyineleme durumu için null parametresi özel durumunu düzeltme
* Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry’ye yönelik yardım dosyalarını düzeltme

#### <a name="azurermnetwork"></a>AzureRM.Network
* Ağ SDK sürümünü 18.0.0-önizleme’den 19.0.0-önizlemeye yükseltme
* Protokol yapılandırması oluşturma cmdlet’i eklendi
    - New-AzureRmNetworkWatcherProtocolConfiguration
* Varolan express route bağlantı hattına yeni bir bağlantı hattı ekleme cmdlet’i eklendi.
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* Varolan express route bağlantı hattındaki bir bağlantı hattı bağlantısını kaldırma cmdlet’i eklendi.
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* Bağlantı hattı bağlantısı alma cmdlet’i eklendi
    - Add-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Oluşturulan sertifikalarla sunucu kimlik doğrulaması kullanımı düzeltildi (Sorun No. 5998)

#### <a name="azurermsql"></a>AzureRM.Sql
* AuditActions veya AuditActionGroups’un kaldırılmasını sağlamak üzere Denetim cmdlet’leri güncelleştirildi
* Yeni bir esnek saklama ilkesi ayarlarken komutun ‘Azure kurtarma hizmeti kasası ve ilkesiyle uzun süreli saklama ilkesini yapılandırma artık desteklenmiyor. Lütfen yeni esnek saklama ilkesi ile istek gönderin’ hatasını verdiği Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy komutuna ilişkin sorun düzeltildi.
* Ölçek ve katman ilişkili özelliklere yönelik Sku özelliğini destekleyen yeni Veritabanı API’sini kullanmak için tüm Azure SQL Veritabanı/ElasticPool Creation/Update cmdlet’lerini güncelleştirin.
* Güncelleştirilen cmlet’ler arasında şunlar yer almaktadır:
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* -Name parametresini kullanırken -ResourceGroupName parametresinin gerekli olması için 'Get-AzureRmTrafficManagerProfile'a yönelik parametreleri güncelleştirin.
