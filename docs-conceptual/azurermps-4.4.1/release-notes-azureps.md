---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 07/26/2017
ms.openlocfilehash: 563f84c3af98de066611dd80102e552b31f12883
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56154061"
---
# <a name="release-notes"></a>Sürüm notları

Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.

## <a name="20170925---version-440"></a>2017.09.25 - Sürüm 4.4.0
* AnalysisServices
  * Veritabanlarının okuma-yazma örneğinden salt okunur örneklere eşitlenmesine olanak tanıyan yeni bir dataplane komutu eklendi
    - Komut için yardım dosyası eklendi
    - Bellek içi testler ve bir senaryo testi (yalnızca canlı) eklendi
  * Add-AzureAsAccount komutundaki hatalar düzeltildi
* Otomasyon
  * Önceki sürümde düzeltilen cmdlet'ler için yardım belgeleri düzeltildi.
  * DSC düğüm yapılandırmalarının aşamalı piyasaya çıkışını desteklemek için 4 yeni cmdlet eklendi.
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * Bilişsel Hizmetler Yönetim SDK’sı sürüm 2.0.0 ile tümleştirme.
  * Get-AzureRmCognitiveServicesAccount artık sayfalamayı doğru şekilde destekleyebiliyor.
* İşlem
  * Çalıştır Komutu özelliği:
    - Yeni cmdlet: 'Invoke-AzureRmVMRunCommand' bir VM üzerinde çalıştırma komutunu çağırır
    - Yeni cmdlet: 'Get-AzureRmVMRunCommandDocument' kullanılabilir çalıştırma komutu belgelerini gösterir
  * 'StorageAccountType' parametresi Set-AzureRmDataDisk’e eklendi
  * Sanal makine, VM ölçek kümesi ve disk için Kullanılabilirlik Alanı desteği
    - Yeni parametre: 'Bölge' New-AzureRmVM, New-AzureRmVMConfig, New-AzureRmVmssConfig, New-AzureRmDiskConfig’e eklenir
  * VM ölçek kümesi sıralı yükseltme özelliği:
    - Yeni cmdlet: 'Start-AzureRmVmssRollingOSUpgrade', VM ölçek kümesinin işletim sistemi sıralı yükseltmesini çağırır
    - Yeni cmdlet: 'Set-AzureRmVmssRollingUpgradePolicy', VM ölçek kümesi sıralı yükseltmesi için yükseltme ilkesini ayarlar.
    - Yeni cmdlet: 'Stop-AzureRmVmssRollingUpgrade', VM ölçek kümesinin sıralı yükseltmesini iptal eder
    - Yeni cmdlet: 'Get-AzureRmVmssRollingUpgrade', VM ölçek kümesi sıralı yükseltmesinin durumunu gösterir.
  * Sistem tarafından atanan kimlik için AssignIdentity anahtar parametresi kullanılma sunuldu.
    - Yeni parametre: 'AssignIdentity' New-AzureRmVMConfig, New-AzureRmVmssConfig ve Update-AzureRmVM’ye eklendi
  * Vmss disk şifreleme özelliği:
    - Yeni cmdlet: 'Set-AzureRmVmssDiskEncryptionExtension', VM ölçek kümesinde disk şifrelemeyi etkinleştirir
    - Yeni cmdlet: 'Disable-AzureRmVmssDiskEncryption', VM ölçek kümesinde disk şifrelemeyi devre dışı bırakır
    - Yeni cmdlet: 'Get-AzureRmVmssDiskEncryptionStatus', bir VM ölçek kümesinin disk şifreleme durumunu gösterir
    - Yeni cmdlet: 'Get-AzureRmVmssVMDiskEncryptionStatus', bir VM ölçek kümesindeki VM’lerin disk şifreleme durumunu gösterir
* ContainerInstance
  * Azure Container Örneği için PowerShell cmdlet'leri eklendi
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* Insights
  * Yeni Disable-AzureRmActivityLogAlert cmdlet’i
    - Mevcut bir etkinlik günlüğü uyarısını devre dışı bırakmaya yönelik yeni cmdlet.
    - İsteğe bağlı olarak, Etiketler de bu cmdlet ile ayarlanabilir.
  * Yeni Enable-AzureRmActivityLogAlert cmdlet’i
    - Mevcut bir etkinlik günlüğü uyarısını etkinleştirmeye yönelik yeni cmdlet.
    - İsteğe bağlı olarak, Etiketler de bu cmdlet ile ayarlanabilir.
  * Yeni Get-AzureRmActivityLogAlert cmdlet’i
    - Bir veya daha fazla etkinlik günlüğü uyarısını almaya yönelik yeni cmdlet.
    - Uyarılar ad, kaynak grubu veya aboneliğe göre alınabilir.
  * Yeni New-AzureRmActionGroup cmdlet’i
    - Bellekte bir ActionGroup nesnesi oluşturmaya yönelik yeni cmdlet (istek yapılmaz.)
  * Yeni New-AzureRmActivityLogAlertCondition cmdlet’i
    - Bellekte bir etkinlik günlüğü uyarısı yaprak koşulu nesnesi oluşturmaya yönelik yeni cmdlet (istek yapılmaz.)
  * Yeni Set-AzureRmActivityLogAlert cmdlet’i
    - Bir etkinlik günlüğü uyarısı oluşturmaya veya güncelleştirmeye yönelik yeni cmdlet.
  * Yeni Remove-AzureRmActivityLogAlert cmdlet’i
    - Bir etkinlik günlüğü uyarısını kaldırmaya yönelik yeni cmdlet.
  * Yeni Set-AzureRmActionGroup cmdlet’i
    - Yeni bir eylem grubu oluşturmaya ya da var olan bir eylem grubunu güncelleştirmeye yönelik yeni cmdlet.
  * Yeni Get-AzureRmActionGroup cmdlet’i
    - Bir veya daha fazla eylem grubunu almaya yönelik yeni cmdlet.
    - Eylem grupları ad, kaynak grubu veya aboneliğe göre alınabilir.
  * Yeni Remove-AzureRmActionGroup cmdlet’i
    - Bir eylem grubunu kaldırmaya yönelik yeni cmdlet.
  * Yeni New-AzureRmActionGroupReceiver cmdlet’i
    - Bellekte yeni bir eylem grubu alıcısı oluşturmaya yönelik yeni cmdlet.
* KeyVault
  * KeyVault sertifikaları için geçici silmeyi destekleyen yeni/güncelleştirilmiş cmdlet’ler
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* Ağ
  * Sanal Ağ Alt Ağlarına uç nokta hizmetleri desteği eklendi
    - Add-AzureRmVirtualSubnetConfig güncelleştirildi: İsteğe bağlı - ServiceEndpoint parametresi eklendi
    - New-AzureRmVirtualSubnetConfig güncelleştirildi: İsteğe bağlı - ServiceEndpoint parametresi eklendi
    - Set-AzureRmVirtualSubnetConfig güncelleştirildi: İsteğe bağlı - ServiceEndpoint parametresi eklendi
  * Konumda mevcut olan uç nokta hizmetlerini listeleyen cmdlet eklendi
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * Aşağıdaki komutlara dış yarıçap tabanlı P2S kimlik doğrulamasını yapılandırma becerisi eklendi
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * Dış yarıçap tabanlı P2S için VpnProfiles oluşturmaya izin veren cmdlet eklendi
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * Genel IP Adresleri ve Load Balancer için SKU parametre desteği eklendi
    - New-AzureRMLoadBalancer güncelleştirildi: İsteğe bağlı -Sku parametresi eklendi
    - New-AzureRMPublicIpAddress güncelleştirildi: İsteğe bağlı -Sku parametresi eklendi
  * Load Balancer Kurallarına DisableOutboundSNAT desteği eklendi
    - New-AzureRMLoadBalancerRuleConfig güncelleştirildi: İsteğe bağlı DisableOutboundSNAT parametresi eklendi
    - Add-AzureRMLoadBalancerRuleConfig güncelleştirildi: İsteğe bağlı DisableOutboundSNAT parametresi eklendi
    - Set-AzureRMLoadBalancerRuleConfig güncelleştirildi: İsteğe bağlı DisableOutboundSNAT parametresi eklendi
  * IkeV2 P2S desteği eklendi
    - New-AzureRmVirtualNetworkGateway güncelleştirildi: İsteğe bağlı -VpnClientProtocol parametresi eklendi, varsayılan değer [ "SSTP", "IkeV2" ]
    - Set-AzureRmVirtualNetworkGateway güncelleştirildi: İsteğe bağlı -VpnClientProtocol parametresi eklendi
  * Ağ Güvenlik Kuralları ve Etkili Ağ Güvenliği Kuralları’na MultiValued kural desteği eklendi
    - Add-AzureRmNetworkSecurityRuleConfig güncelleştirildi: SourcePortRange, DestinationPortRange, SourceAddressPrefix parametreleri bir dize listesi kabul edecek şekilde güncelleştirildi
    - New-AzureRmNetworkSecurityRuleConfig güncelleştirildi: SourcePortRange, DestinationPortRange, SourceAddressPrefix parametresi bir dize listesi kabul edecek şekilde güncelleştirildi
    - Set-AzureRmNetworkSecurityRuleConfig güncelleştirildi: SourcePortRange, DestinationPortRange, SourceAddressPrefix parametresi bir dize listesi kabul edecek şekilde güncelleştirildi
    - Add-AzureRmNetworkSecurityRuleConfig güncelleştirildi: SourcePortRange, DestinationPortRange, SourceAddressPrefix parametresi bir dize listesi kabul edecek şekilde güncelleştirildi
    - New-AzureRmNetworkSecurityGroup güncelleştirildi: SecurityRules parametresi, PSSecurityRule nesnesinde dize listesi olan SourcePortRange, DestinationPortRange, SourceAddressPrefix parametrelerini kabul edecek şekilde güncelleştirildi
    - Get-AzureRmEffectiveNetworkSecurityGroup güncelleştirildi: TagMap parametresi eklendi
    - Get-AzureRmEffectiveNetworkSecurityGroup güncelleştirildi: Döndürülen PSEffectiveSecurityRule nesnesi, dize listesi olan SourcePortRange, DestinationPortRange, SourceAddressPrefix parametreleri ile güncelleştirildi.
  * Sanal ağlar için DDoS koruması desteği eklendi
    - New-AzureRmVirtualNetwork güncelleştirildi: EnableDDoSProtection ve EnableVmProtection anahtar parametreleri eklendi
    - PSVirtualNetwork nesnesine EnableDDoSProtection ve EnableVmProtection özellikleri eklendi
  * Yüksek Oranda Kullanılabilir İç Load Balancer desteği eklendi
    - Add-AzureRmLoadBalancerRuleConfig güncelleştirildi: Protocol parametresi için kabul edilebilir bir değer olarak All eklendi
    - New-AzureRmLoadBalancerRuleConfig güncelleştirildi: Protocol parametresi için kabul edilebilir bir değer olarak All eklendi
    - Set-AzureRmLoadBalancerRuleConfig güncelleştirildi: Protocol parametresi için kabul edilebilir bir değer olarak All eklendi
  * Uygulama Güvenliği Grupları desteği eklendi
    - New-AzureRmApplicationSecurityGroup eklendi
    - Get-AzureRmApplicationSecurityGroup eklendi
    - Remove-AzureRmApplicationSecurityGroup eklendi
    - New-AzureRmNetworkInterface güncelleştirildi: İsteğe bağlı ApplicationSecurityGroup ve ApplicationSecurityGroupId parametreleri eklendi
    - New-AzureRmNetworkInterfaceIpConfig güncelleştirildi: İsteğe bağlı ApplicationSecurityGroup ve ApplicationSecurityGroupId parametreleri eklendi
    - Add-AzureRmNetworkInterfaceIpConfig güncelleştirildi: İsteğe bağlı ApplicationSecurityGroup ve ApplicationSecurityGroupId parametreleri eklendi
    - Set-AzureRmNetworkInterfaceIpConfig güncelleştirildi: İsteğe bağlı ApplicationSecurityGroup ve ApplicationSecurityGroupId parametreleri eklendi
    - New-AzureRmNetworkSecurityRuleConfig güncelleştirildi: SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup ve DestinationApplicationSecurityGroupId isteğe bağlı parametreleri eklendi
    - Add-AzureRmNetworkSecurityRuleConfig güncelleştirildi: SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup ve DestinationApplicationSecurityGroupId isteğe bağlı parametreleri eklendi
    - Set-AzureRmNetworkSecurityRuleConfig güncelleştirildi: SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup ve DestinationApplicationSecurityGroupId isteğe bağlı parametreleri eklendi
  * VpnDeviceConfiguration Betikleri için yeni komutlar eklendi
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* Profil
  * AzureRm cmdlet'leri için Start-Job desteği.
    * Tüm AzureRmCmdlets bir bağlam kabul edebilen -AzureRmContext parametresini kabul eder (Context cmdlet’inin bir çıktısı).
      - Bağlam kalıcılığı DISABLED: `Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)` olan işler için ortak desen
      - Bağlam kalıcılığı ENABLED: `Start-Job {New-AzureRmVM [... other parameters]}` olan işler için ortak desen
  * Oturum açma bilgilerini oturumlarda sürdürme, yeni cmdlet'ler:
    - Enable-AzureRmContextAutosave - Oturumlar arasında kimlik bilgilerinin kalıcılığını etkinleştirme.
    - Disable-AzureRmContextAutosave - Oturumlar arasında kimlik bilgilerinin kalıcılığını devre dışı bırakma.
  * Bağlam bilgilerini yönetme, yeni cmdlet’ler
    - Select-AzureRmContext - Etkin adlandırılmış bağlamı seçme.
    - Rename-AzureRmContext - Daha kolay başvuru için mevcut bir bağlamı yeniden adlandırma.
    - Remove-AzureRmContext - Mevcut bir bağlamı kaldırma.
    - Remove-AzureRmAccount - Bir hesapla ilişkili tüm kimlik bilgilerini, abonelikleri ve kiracıları kaldırma.
  * Bağlam bilgilerini yönetme, cmdlet değişiklikleri:
    - Kimlik bilgilerini değiştiren tüm cmdlet’lere Scope = (Process | CurrentUser) eklendi
    - Get-AzureRmContext - Tüm kayıtlı bağlamları listelemek için ListAvailable parametresi eklendi
* Kaynaklar
  * PolicySetDefinition cmdlet’leri eklendi
    - Bir ilke kümesi tanımı oluşturmaya yönelik New-AzureRmPolicySetDefinition cmdlet’i
    - Tüm ilke kümesi tanımlarını listelemeye veya belirli bir ilke kümesi tanımı almaya yönelik Get-AzureRmPolicySetDefinition cmdlet’i
    - Bir ilke kümesi tanımını silmeye yönelik Remove-AzureRmPolicySetDefinition cmdlet’i
    - Var olan bir ilke kümesi tanımını güncelleştirmeye yönelik Set-AzureRmPolicySetDefinition cmdlet’i
  * -PolicySetDefinition, -Sku ve -NotScope parametreleri New-AzureRmPolicyAssignment ve Set-AzureRmPolicyAssignment cmdlet’lerine eklendi
  * New-AzureRmPolicyDefinition ve Set-AzureRmPolicyDefinition cmdlet’lerine ilke url’sini geçirme desteği eklendi
  * -Mode parametresi New-AzureRmPolicyDefinition cmdlet’ine eklendi
  * PSRoleAssignment nesnesi kullanılarak rol atamasını kaldırma desteği eklendi
    - Kullanıcılar artık PSRoleassignmnet giriş nesnesini Remove-AzureRMRoleAssignment komutuyla birlikte kullanarak rol atamasını kaldırabilir.
  * ManagedApplication cmdlet'leri eklendi
    - Yönetilen bir uygulama oluşturmaya yönelik New-AzureRmManagedApplication cmdlet’i
    - Bir abonelik altındaki tüm yönetilen uygulamaları listelemeye veya belirli bir yönetilen uygulamayı almaya yönelik Get-AzureRmManagedApplication cmdlet’i
    - Yönetilen bir uygulamayı silmeye yönelik Remove-AzureRmManagedApplication cmdlet’i
    - Mevcut bir yönetilen uygulamayı güncelleştirmeye yönelik Set-AzureRmManagedApplication cmdlet’i
  * ManagedApplicationDefinition cmdlet'leri eklendi
    - Bir zip dosyası uri’si veya mainTemplate ve createUiDefinition json dosyaları kullanılarak yönetilen bir uygulama tanımı oluşturmaya yönelik New-AzureRmManagedApplicationDefinition cmdlet’i
    - Bir kaynak grubu altındaki tüm yönetilen uygulama tanımlarını listelemeye veya belirli bir yönetilen uygulama tanımını almaya yönelik Get-AzureRmManagedApplicationDefinition cmdlet’i
    - Yönetilen bir uygulama tanımını silmeye yönelik Remove-AzureRmManagedApplicationDefinition cmdlet’i
    - Mevcut bir yönetilen uygulama tanımını güncelleştirmeye yönelik Set-AzureRmManagedApplicationDefinition cmdlet’i
* Sql
  * Sanal Ağ Kuralları desteği ekleme
    - Belirli bir kural adına veya bir Azure Sql sunucusundaki sanal ağ kuralları listesine göre sanal ağ kurallarını alan Get-AzureRmSqlServerVirtualNetworkRule cmdlet’ini ekleme.
    - Kuralın işaret ettiği sanal ağı değiştiren Set-AzureRmSqlServerVirtualNetworkRule cmdlet’ini ekleme.
    - Bir Azure Sql sunucusu için sanal ağ kuralı kaldıran Remove-AzureRmSqlServerVirtualNetworkRule cmdlet’ini ekleme.
    - Bir Azure Sql sunucusu için yeni bir sanal ağ kuralı oluşturan New-AzureRmSqlServerVirtualNetworkRule cmdlet’ini ekleme.
* Web Siteleri
  * App Service Planları için PremiumV2 Katmanı eklendi
* Azure Depolama
  * Azure Depolama İstemci Kitaplığı 8.4.0 ve Azure DataMovement Kitaplığı 0.6.1 sürümüne yükseltildi
  * Karşıya Yükleme ve Kopyalama Blob API’sine PremiumPageBlobTier Desteği eklendi
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * AzureStorageContainer, AzureStorageBlob, AzureStorageQueue, AzureStorageTable Konsol Çıktı Biçimi iyileştirildi
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>2017.08.10 - Sürüm 4.3.1
  * Bütünleştirilmiş kod imzalama sorununu düzeltmek için güncelleştirin

## <a name="20170807---version-430"></a>2017.08.07 - Sürüm 4.3.0
* AnalysisServices
  * Set-AzureRmAnalysisServciesServer içinde bir hata düzeltildi
    - Yönetici sağlanmadığında, yönetici kaldırılır.
  * New-AzureRmAnalysisServicesServer ve Set-AzureRmAnalysisServicesServer içine BackupBlobContainerUri eklendi
    - Azure Analysis Services Server’ı yedeklemek/geri yüklemek için yedekleme blob kapsayıcısını ayarlama/devre dışı bırakma etkinleştirildi
  * New-AzureRmAnalysisServicesServer ve Set-AzureRmAnalysisServicesServer içinde güncelleştirilmiş SKU arama
    - Sabit kodlanmış SKU, dinamik arama olarak değiştirildi.
  * Hizmet Sorumlusu ile oturum açmayı desteklemek için Add-AzureAnalysisServicesAccount
* Otomasyon
  * 100’den fazla kayıt çekmek için AutomationDSC* cmdlet’lerinde değişiklikler yapıldı
  * Ayrıntılı akışların bazı Otomasyon cmdlet’leri (örneğin Get-AzureRmAutomationVariable, Get-AzureRmAutomationJob) çağrıldıktan sonra çalışmayı durdurması sorunu çözüldü.
  * StartAzureAutomationDscCompilationJob ve ImportAzureAutomationDscNodeConfiguration içinde NodeConfiguration Derleme sürümü oluşturma desteği eklendi
  * Mevcut sorunlar için hata düzeltmeleri - #3775 içindeki diğer ad ve HybridWorkers için runOn diğer adı ve desteği sorunu düzeltildi.
* İşlem
  * Set-AzureRmVMAEMExtension: Yeni Premium Disk boyutları için destek eklendi
  * Set-AzureRmVMAEMExtension: M serisi için destek eklendi
  * Add-AzureRmVmssExtension öğesine ForceUpdateTag parametresi ekleme
  * New-AzureRmVmssIpConfig öğesine Primary parametresi ekleme
  * Add-AzureRmVmssNetworkInterfaceConfig öğesine EnableAcceleratedNetworking parametresi ekleme
  * Set-AzureRmVmss öğesine InstanceId ekleme
  * Get-AzureRmVM -Status çıkışını almak için MaintenanceRedeployStatus öğesini kullanıma sunma
  * Get-AzureRmComputeResourceSku öğesinin tablo biçimine yönelik Restriction ve Capability öğelerini kullanıma sunma
* DataLakeStore
  * Şu sorun düzeltildi: https://github.com/Azure/azure-powershell/issues/4323
* EventHub
  * NamespaceAttributes öğesine ResourceGroup özelliği eklendi
    - 'ResourceGroup', Ad Alanının bulunduğu kaynak grubunun adını alır
  * cmdlet’ler AuthorizationRule işlemine yönelik Namespace ve EventHub için Parametersets ile güncelleştirildi
    - New-AzureRmEventHubAuthorizationRule - Mevcut NameSpace veya EventHub öğesine yeni bir AuthorizationRule ekler.
    - Get-AzureRmEventHubAuthorizationRule - Mevcut NameSpace veya EventHub öğesinin AuthorizationRule / AuthorizationRules Listesini alır.
    - Set-AzureRmEventHubAuthorizationRule - EventHub NameSpace için mevcut AuthorizationRule özelliklerini güncelleştirir.
    - Remove-AzureRmEventHubAuthorizationRule - Mevcut NameSpace veya EventHub için mevcut AuthorizationRule öğesini siler.
    - New-AzureRmEventHubKey - Mevcut NameSpace veya EventHub için AuthorizationRule öğesine yönelik yeni bir Birincil/İkincil Anahtar oluşturur.
    - Get-AzureRmEventHubKey - Mevcut NameSpace veya EventHub için AuthorizationRule öğesine yönelik Birincil/İkincil Anahtarı alır.
* Ağ
    * IPv6 desteği ve isteğe bağlı yeni bir parametre (PeerAddressType) eklendi
      * New-AzureRmExpressRouteCircuitPeeringConfig:
      * Set-AzureRmExpressRouteCircuitPeeringConfig: IPv6 desteği eklendi. İsteğe bağlı yeni bir parametre eklendi
      * Remove-AzureRmExpressRouteCircuitPeeringConfig: IPv6 desteği eklendi. İsteğe bağlı yeni bir parametre eklendi
    * -ProbeEnabled parametresi eski olarak işaretlendi
      - Add-AzureRmApplicationGatewayBackendHttpSettings
      - New-AzureRmApplicationGatewayBackendHttpSettings
      - Set-AzureRmApplicationGatewayBackendHttpSettings
* Profil
    * Veri toplama varsayılan olarak etkinleştirildi. Kullanım verileri, kullanıcı deneyimini geliştirmek için Microsoft tarafından toplanır. Veriler anonimdir ve komut satırı bağımsız değişkeni değerlerini içermez.
      - Özelliği kapatmak için Disable-AzureRmDataCollection cmdlet’ini kullanın
      - Özelliği açmak için Enable-AzureRmDataCollection cmdlet’ini kullanın
* Kaynaklar
    * İstek ARM’ye gönderilmeden önce aşağıdaki roledefinition ve roleassignment commandlet’leri için kapsam doğrulama desteği ekleme
      - Get-AzureRMRoleAssignment
      - New-AzureRMRoleAssignment
      - Remove-AzureRMRoleAssignment
      - Get-AzureRMRoleDefinition
      - New-AzureRMRoleDefinition
      - Remove-AzureRMRoleDefinition
      - Set-AzureRMRoleDefinition
* ServiceBus
  * NameSpace, Queue ve Topic için AuthorizationRules öğesine yönelik aşağıdaki yeni commandlet’ler eklendi. Yetkilendirme kuralı işlemleri, ayarlanan parametreye göre uygulanır.
    - New-AzureRmServiceBusAuthorizationRule - Mevcut ServiceBus NameSpace/Queue/Topic için yeni bir AuthorizationRule ekler.
    - Get-AzureRmServiceBusAuthorizationRule - Mevcut ServiceBus NameSpace/Queue/Topic için AuthorizationRule / AuthorizationRules Listesini alır.
    - Set-AzureRmServiceBusAuthorizationRule - Servicebus NameSpace/Queue/Topic için mevcut AuthorizationRule özelliklerini güncelleştirir.
    - New-AzureRmServiceBusKey - Mevcut ServiceBus NameSpace/Queue/Topic için AuthorizationRule öğesine yönelik yeni bir Birincil/İkincil Anahtar oluşturur.
    - Get-AzureRmServiceBusKey - Mevcut ServiceBus NameSpace/Queue/Topic için AuthorizationRule öğesinin Birincil/İkincil Anahtarını alır.
    - Remove-AzureRmServiceBusNamespaceAuthorizationRule - ServiceBus NameSpace/Queue/Topic için mevcut AuthorizationRule öğesini siler.
  * NamespceAttributes öğesine Kaynak Grubu özelliği eklendi

* Sql
    * Set-AzureRmSqlServerTransparentDataEncryptionProtector, Şifreleme Koruyucu Türü AzureKeyVault olarak ayarlandığında bir uyarı görüntülemek ve onay gerektirmek üzere güncelleştiriliyor
    * Denetim ayarları için yeni güncelleştirilmiş cmdlet’ler ekleniyor
      - Bir Azure SQL veritabanının denetim ayarlarını alan Get-AzureRmSqlDatabaseAuditing cmdlet’i.
      - Bir Azure SQL sunucusunun denetim ayarlarını alan Get-AzureRmSqlServerAuditing cmdlet’i.
      - Bir Azure SQL veritabanının denetim ayarlarını değiştiren Set-AzureRmSqlDatabaseAuditing cmdlet’i.
      - Bir Azure SQL sunucusunun denetim ayarlarını değiştiren Set-AzureRmSqlServerAuditing cmdlet’i.
    * Mevcut Denetim ilkesi cmdlet’leri kullanım dışı bırakılıyor
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * Update-AzureRmSqlSyncGroup için şema dosyası ayrıştırma işlemi artık büyük/küçük harfe duyarlı değildir.
* Depolama
    * Kaynak modu depolama hesabı cmdlet’lerine NeworkRule desteği eklendi
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>2017.07.17 - Sürüm 4.2.1
* İşlem
  - VM Diskleri ve VM Diski anlık görüntüleri için oluşturma ve güncelleştirme cmdlet’leri ile ilgili sorun çözüldü (bağlantı)[<https://github.com/azure/azure-powershell/issues/4309>]
    - New-AzureRmDisk
    - New-AzureRmSnapshot
    - Update-AzureRmDisk
    - Update-AzureRmSnapshot
* Profil
  - RDFE’de etkileşimli olmayan kullanıcı kimlik doğrulaması ile ilgili sorun düzeltildi (bağlantı)[<https://github.com/Azure/azure-powershell/issues/4299>]

* ServiceManagement
  - Etkileşimli olmayan kullanıcı kimlik doğrulaması ile ilgili sorun düzeltildi (bağlantı)[<https://github.com/Azure/azure-powershell/issues/4299>]

## <a name="2017711---version-420"></a>2017.7.11 - Sürüm 4.2.0
* AnalysisServices
    * Yeni veri düzlemi API’si ekleme
        - Analysis Services sunucu günlüğünü getirmeye yönelik Export-AzureAnalysisServicesInstanceLog API’si kullanıma sunuldu
* Otomasyon
    * New-AzureRmAutomationSchedule için Haftalık ve Aylık zamanlamalarda TimeZone değerini doğru ayarlama
        - Bu sorunla ilgili daha fazla bilgi bulabilirsiniz: https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - Yeni Get-AzureBatchJobPreparationAndReleaseTaskStatus cmdlet’i eklendi.
    - Get-AzureBatchNodeFileContent parametrelerine bayt aralığı başlangıcı ve bitişi eklendi.
* CognitiveServices
    * Bilişsel Hizmetler Yönetim SDK’sı sürüm 1.0.0 ile tümleştirme.
    * Hesap adı uzunluğu denetleme hatası düzeltildi.
* İşlem
    * Görüntü diski için depolama hesabı türü desteği:
        - Set-AzureRmImageOsDisk ve Add-AzureRmImageDataDisk’e 'StorageAccountType' parametresi eklendi
    * Vmss Ip Yapılandırması içindeki PrivateIP ve PublicIP özelliği:
        - New-AzureRmVmssIpConfig’e 'PrivateIPAddressVersion', 'PublicIPAddressConfigurationName', 'PublicIPAddressConfigurationIdleTimeoutInMinutes', 'DnsSetting' adları eklendi
        - New-AzureRmVmssIpConfig’e IPv4 veya IPv6 belirtmeye yönelik 'PrivateIPAddressVersion' parametresi eklendi
    * Performans Bakımı özelliği:
        - Restart-AzureRmVM’ye 'PerformMaintenance' anahtar parametresi eklendi.
        - Get-AzureRmVM -Status, belirli bir VM’nin performans bilgilerini gösteriyor
    * Sanal Makine Kimliği özelliği:
        - New-AzureRmVMConfig ve UpdateAzureRmVM’ye 'IdentityType' parametresi eklendi
        - Get-AzureRmVM, belirli bir VM’nin kimlik bilgilerini gösteriyor
    * Vmss Kimliği özelliği:
        - New-AzureRmVmssConfig’e 'IdentityType' parametresi eklendi
        - Get-AzureRmVmss, belirli bir Vmss’nin kimlik bilgilerini gösteriyor
    * Vmss Önyükleme Tanılaması özelliği:
        - Vmss nesnesinin önyükleme tanılamasını ayarlamaya yönelik yeni cmdlet: Set-AzureRmVmssBootDiagnostics
        - New-AzureRmVmssConfig’e 'BootDiagnostic' parametresi eklendi
    * Vmss LicenseType özelliği:
        - New-AzureRmVmssConfig’e 'LicenseType' parametresi eklendi
    * RecoveryPolicyMode desteği:
        - New-AzureRmVmssConfig’e 'RecoveryPolicyMode' parametresi eklendi
    * İşlem Kaynağı Sku’su özelliği:
        - Yeni 'Get-AzureRmComputeResourceSku' cmdlet’i tüm işlem kaynağı sku’larını listeler
* DataFactories
    * New-AzureRmDataFactoryGatewayKey kullanımdan kaldırıldı
    * New-AzureRmDataFactoryGatewayAuthKey ve Get-AzureRmDataFactoryGatewayAuthKey eklenerek ağ geçidi kimlik doğrulama anahtarı özelliği kullanıma sunuldu
* DataLakeAnalytics
    * Aşağıdaki komutlarla İşlem İlkesi CRUD’si için destek eklendi:
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * Yinelenen işlerde ve iş işlem hatlarında yardım için iş ilişkisi meta veri desteği eklendi. Aşağıdaki komutlar güncelleştirildi veya eklendi:
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * İş ve katalog API’lerinde belirteç hedef kitlesi, Azure Resource hedef kitlesi yerine Data Lake’e özel olan doğru hedef kitleyi kullanacak şekilde güncelleştirildi.
* DataLakeStore
    * Set-AzureRMDataLakeStoreAccount cmdlet’inde kullanıcı tarafından yönetilen KeyVault anahtar dönüşleri için destek eklendi
    * Kullanıcı tarafından yönetilen bir KeyVault eklendiğinde veya bir anahtar döndürüldüğünde `enableKeyVault` çağrısını otomatik olarak tetiklemek üzere bir yaşam kalitesi güncelleştirmesi eklendi.
    * İş ve katalog API’lerinde belirteç hedef kitlesi, Azure Resource hedef kitlesi yerine Data Lake’e özel olan doğru hedef kitleyi kullanacak şekilde güncelleştirildi.
    * Aşağıdaki cmdlet’ler kullanılarak oluşturulan/eklenen dosyaların boyutunu sınırlayan bir hata düzeltildi:
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* Dns
    * Get-AzureRmDnsZone için kanal oluşturma senaryosundaki hata düzeltildi
        - Buradan daha fazla bilgi bulabilirsiniz: https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * Operations Management Suite’i (OMS) etkinleştirme/devre dışı bırakma desteği eklendi
    * Yeni cmdlet’ler
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * Spark özel yapılandırmalarını ayarlamak için Add-AzureRmHDInsightConfigValues’a yeni parametreler eklendi
        - Spark 1.6 için SparkDefaults ve SparkThriftConf parametreleri
        - Spark 2.0 için Spark2Defaults ve Spark2ThriftConf parametreleri
* Insights
    * Sorun 4215 (değişiklik isteği), Get-AzureRmLog cmdlet’inin zaman penceresindeki 15 günlük sınır ortadan kaldırıldı. Ayrıca birim testi adlarında küçük değişiklikler yapıldı.
    * Get-AzureRmLog için Sorun 3957 çözüldü
        - Sorun 1: Arka uç, her birinde 200 kayıt olup sonraki sayfaya devam belirteci ile bağlanan sayfalar halinde kayıtlar döndürüyor. Müşteriler daha fazlası olduğunu bildikleri durumlarda cmdlet’in yalnızca 200 kayıt döndürdüğünü görüyordu. Bu durum, MaxEvents için ayarladıkları ve 200’den az olmayan değerden bağımsız olarak gerçekleşiyordu.
        - Sorun 2: Belgeler bu cmdlet hakkında yanlış veriler içeriyordu. Örn. varsayılan zaman penceresi 1 saatti.
        - Düzeltme 1: Cmdlet artık MaxEvents değerine veya küme sonuna ulaşana kadar arka uç tarafından döndürülen devam belirtecini takip etmektedir.<br>MaxEvents için varsayılan değer 1000 ve en büyük değer 100000’dir. 1’den küçük tüm MaxEvents değerleri yok sayılmakta ve yerine varsayılan değer kullanılmaktadır. Bu değerler ve davranış değişmemiştir, ancak şu anda doğru şekilde belgelenmektedir.<br>Cmdlet adı artık olaylar hakkında değil, yalnızca Günlükler hakkında bilgi verdiği için, MaxEvents’e ilişkin bir diğer ad eklendi.
        - Düzeltme 2: Belgeler doğru ve daha ayrıntılı bilgiler içeriyor: yeni diğer ad, doğru zaman penceresi, doğru varsayılan değer, en küçük ve en büyük değerler.
* KeyVault
    * Set-AzureRMKeyVaultAccessPolicy ve Remove-AzureRMKeyVaultAccessPolicy cmdlet’lerinde -UserPrincipalName belirtildiğinde, dizin sorgusundan e-posta adresi kaldırılıyor.
      - Her iki Cmdlet de artık e-posta adresinin uygun olup olmadığı sorgulanırken -UserPrincipalName parametresi yerine kullanılabilecek bir -EmailAddress parametresine sahiptir.  Dizinde birden çok eşleşen e-posta adresi varsa, Cmdlet başarısız olur.
* Ağ
    * New-AzureRmIpsecPolicy: SALifeTimeSeconds ve SADataSizeKilobytes artık zorunlu parametreler değildir
        - SALifeTimeSeconds varsayılan değeri 27000 saniyedir
        - SADataSizeKilobytes varsayılan değeri 102400000 KB’dir
    * Ssl ilkesi kullanıp Application Gateway’de tüm ssl seçeneklerini listeleyen özel şifre paketi yapılandırması için destek eklendi
        - İsteğe bağlı -PolicyType, -PolicyName, -MinProtocolVersion, -Ciphersuite parametresi eklendi
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - Get-AzureRmApplicationGatewayAvailableSslOptions eklendi (Diğer ad: List-AzureRmApplicationGatewayAvailableSslOptions)
        - Get-AzureRmApplicationGatewaySslPredefinedPolicy eklendi (Diğer ad: List-AzureRmApplicationGatewaySslPredefinedPolicy)
    * Application Gateway’de yeniden yönlendirme desteği eklendi
        - Add-AzureRmApplicationGatewayRedirectConfiguration eklendi
        - Get-AzureRmApplicationGatewayRedirectConfiguration eklendi
        - New-AzureRmApplicationGatewayRedirectConfiguration eklendi
        - Remove-AzureRmApplicationGatewayRedirectConfiguration eklendi
        - Set-AzureRmApplicationGatewayRedirectConfiguration eklendi
        - İsteğe bağlı -RedirectConfiguration parametresi eklendi
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - İsteğe bağlı -DefaultRedirectConfiguration parametresi eklendi
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - İsteğe bağlı -RedirectConfiguration parametresi eklendi
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - İsteğe bağlı -RedirectConfigurations parametresi eklendi
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Application Gateway’de Azure web siteleri desteği eklendi
        - New-AzureRmApplicationGatewayProbeHealthResponseMatch eklendi
        - İsteğe bağlı -PickHostNameFromBackendHttpSettings, -MinServers, -Match parametreleri eklendi
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - İsteğe bağlı -PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled, -Path parametreleri eklendi
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * VM Ölçek Kümesi aracılığıyla oluşturulan publicipaddress kaynaklarını almak için Get-AzureRmPublicIPaddress güncelleştirildi
    * Sanal ağın geçerli kullanımını almak için cmdlet eklendi
        - Get-AzureRmVirtualNetworkUsageList
* Profil
    * Import-AzureRmContext veya Save-AzureRmContext kullanılırken karşılaşılan hata düzeltildi
        - Bu sorunla ilgili daha fazla bilgi bulabilirsiniz: https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * Azure Site Recovery işlemleri için yeni bir modül kullanıma sunuluyor.
        - Tüm cmdlet’ler AzureRmRecoveryServicesAsr* ile başlar
* Sql
    * AzureRM.Sql’e Veri Senkronizasyonu PowerShell Cmdlet’leri eklendi
    * Sunucu oluştururken zaman aşımlarını önleyen yeni REST API’sini kullanmak üzere AzureRmSqlServer cmdlet’leri güncelleştirildi.
    * Eski sunucu sürümü (2.0) artık mevcut olmadığı için sunucu yükseltme cmdlet’leri kullanımdan kaldırıldı.
    * SQL sunucusu kaynağı için bir kaynak kimliği sağlamayı desteklemek üzere New-AzureRmSqlServer ve Set-AzureRmSqlServer cmdlet’lerine yeni isteğe bağlı "AssignIdentity" parametresi eklendi
    * ResourceGroupName parametresi Get-AzureRmSqlServer için artık isteğe bağlıdır
        - Aşağıdaki sorunla ilgili daha fazla bilgi bulabilirsiniz: https://github.com/Azure/azure-powershell/issues/635
* ExpressRoute için ServiceManagement:
    * New-AzureBgpPeering cmdlet’i aşağıdaki yeni seçenekleri içerecek şekilde güncelleştirildi:
        - PeerAddressType : İlgili adres ailesi türünün BGP Eşliğini oluşturmak için "IPv4" veya "IPv6" değerleri belirtilebilir
    * Set-AzureBgpPeering cmdlet’i aşağıdaki yeni seçenekleri içerecek şekilde güncelleştirildi:
        - PeerAddressType : İlgili adres ailesi türünün BGP Eşliğini güncelleştirmek için "IPv4" veya "IPv6" değerleri belirtilebilir
    * Remove-AzureBgpPeering cmdlet’i aşağıdaki yeni seçenekleri içerecek şekilde güncelleştirildi:
        - PeerAddressType : İlgili adres ailesi türünün veya tümünün BGP Eşliğini kaldırmak için "IPv4" veya "IPv6" ya da Tümü değerleri belirtilebilir

## <a name="20170607---version-410"></a>2017.06.07 - Sürüm 4.1.0
* AnalysisServices
    * Yeni SKU’lar eklendi: B1, B2, S0
    * Ölçek artırma/azaltma desteği eklendi
* CognitiveServices
    * Bilişsel Hizmetler kaynakları oluşturulurken lisans sözleşmelerinin ayrıntılı görüntüsü güncelleştirildi
* İşlem
    * Birden fazla yönetilen disk içeren sanal makineler için Test-AzureRmVMAEMExtension düzeltildi
    * Set-AzureRmVMAEMExtension güncelleştirildi: Premium yönetilen diskler için önbelleğe alma bilgileri eklendi
    * Add-AzureRmVhd: Vhd üzerindeki boyut sınırı 4 TB’ye yükseltildi.
    * Stop-AzureRmVM: STayProvisioned parametresinin belgeleri netleştirildi
    * New-AzureRmDiskUpdateConfig
      * CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId parametreleri kullanımdan kaldırıldı
    * Set-AzureRmDiskUpdateImageReference: Kullanım dışı bırakılan cmdlet
    * New-AzureRmSnapshotUpdateConfig
      * CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId parametreleri kullanımdan kaldırıldı
    * Set-AzureRmSnapshotUpdateImageReference: Kullanım Dışı Bırakılan Cmdlet
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * Bir DataLake Deposu için KeyVault ile yönetilen şifreleme etkinleştirildi
* DevTestLabs
    * Cmdlet’ler geçerli ve güncelleştirilmiş DevTest Labs API sürümü ile çalışacak şekilde güncelleştirildi.
* IotHub
    * IoTHub cmdlet’leri için Yönlendirme desteği eklendi
* KeyVault
  * KeyVault ile Yönetilen Depolama Hesabı Anahtarlarını destekleyen yeni Cmdlet’ler
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* Ağ
    * Get-AzureRmNetworkUsage: Ağ kullanımını ve kapasite bilgilerini gösteren yeni cmdlet
    * VirtualNetworkGateways için yeni GatewaySku seçenekleri eklendi
        * Vpn ağ geçitleri için yeni VpnGw1, VpnGw2, VpnGw3 Sku’ları eklendi
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * Düzeltilen yardım örnekleri
* NotificationHubs
    * Yeni API için NotificationHubs cmdlet’lerinde Saydam Güncelleştirme
* Profil
    * Resolve-AzureRmError
      * Sunucu isteği/yanıt verileri dahil olmak üzere cmdlet’ler tarafından oluşturulan hata ve özel durumların ayrıntılarını gösteren yeni cmdlet
    * Send-Feedback
      * Oturum açmadan geri bildirim gönderme etkinleştirildi
    * Get-AzureRmSubscription
      * CSP aboneliklerini alma hatası düzeltildi
* Kaynaklar
    * Rol atama sayısının 1000’den fazla olması durumunda Get-AzureRMRoleAssignment cmdlet’inin Hatalı İstek ile sonuçlandığı sorun düzeltildi
        * Kullanıcılar bundan böyle döndürülen rol atamaları sayısı 1000’den fazla olsa bile Get-AzureRMRoleAssignment cmdlet’ini kullanabilir
* Sql
    * Restore-AzureRmSqlDatabase: Belge örneği güncelleştirildi
* Depolama
    * Kaynak modu depolama hesabı cmdlet’lerine AssignIdentity ayarlama desteği eklendi
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * Kaynak modu depolama hesabı cmdlet’lerine Müşteri Anahtarı Desteği eklendi
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * Yeni 'MonitorIntervalInSeconds', 'MonitorTimeoutInSeconds', 'MonitorToleratedNumberOfFailures' İzleyici ayarları
    * Yeni 'TCP' İzleyici protokolü
* ServiceManagement
    * Add-AzureVhd: Vhd üzerindeki boyut sınırı 4 TB’ye yükseltildi.
    * New-AzureBGPPeering: LegacyMode desteği
* Azure Depolama
    * Joker karakterleri kabul eden parametrelere ilişkin yardım ve StorageContext türü güncelleştirildi

## <a name="20170523---version-402"></a>2017.05.23 - Sürüm 4.0.2
* Profil
    * Add-AzureRmAccount
      * AzureRM.profile 2.x sürümleriyle geri dönük uyumluluk için `-EnvironmentName` parametre diğer adı eklendi

## <a name="20170512---version-401"></a>2017.05.12 - Sürüm 4.0.1
 * Çevrimdışı senaryolarda New-AzureStorageContext ile ilgili senaryo düzeltildi: https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>2017.05.10 - Sürüm 4.0.0


* Bu sürüm önemli değişiklikler içerir. Değişikliklerle ilgili ayrıntılar ve var olan betikler üzerindeki etkileri için lütfen [geçiş kılavuzuna](https://aka.ms/azps-migration-guide) bakın.
* ApiManagement
  - New-AzureRmApiManagementGroup cmdlet'inde harici grupların yapılandırılması için destek eklendi.
* Faturalandırma
  - Yeni Get-AzureRmBillingPeriod
    + cmdlet'i ile aboneliğin Azure faturalandırma dönemlerini alabilirsiniz.
  - Get-AzureRmBillingInvoice cmdlet'i güncelleştirildi
  - Yeni özellik: BillingPeriodNames
  - Liste görünümünde çıktı
* İşlem
  - Set-AzureRmVMAEMExtension ve Test-AzureRmVMAEMExtension cmdlet'leri Premium yönetilen diskleri destekleyecek şekilde güncelleştirildi
  - IaaS VM'leri için şifreleme ayarlarının yedeklenmesi ve hata durumunda geri yüklenmesi
  - ChefServiceInterval seçeneğinin adı ChefDaemonInterval olarak değiştirildi. Ancak eskisi de çalışmaya devam ediyor.
  - PS VM nesnesinden yinelenen DataDiskNames ve NetworkInterfaceIDs özellikleri kaldırıldı.
  - Remove-AzureRmVMDataDisk ve Remove-AzureRmVMNetworkInterface cmdlet'lerindeki Make DataDiskNames ve NetworkInterfaceIDs parametreleri isteğe bağlı hale getirildi.
  - Get cmdlet'leri liste nesnesi döndürdüğünde karşılaşılan kanal sorunu düzeltildi.
  - RDFE cmdlet'leriyle çakışan cmdlet'ler yeniden adlandırıldı. Daha ayrıntılı bilgi için https://github.com/Azure/azure-powershell/issues/2917 sorununa bakın
    + `New-AzureVMSqlServerAutoBackupConfig`, `New-AzureRmVMSqlServerAutoBackupConfig` olarak yeniden adlandırıldı
    + `New-AzureVMSqlServerAutoPatchingConfig`, `New-AzureRmVMSqlServerAutoPatchingConfig` olarak yeniden adlandırıldı
    + `New-AzureVMSqlServerKeyVaultCredentialConfig`, `New-AzureRmVMSqlServerKeyVaultCredentialConfig` olarak yeniden adlandırıldı
* Tüketim
  - Yeni cmdlet: Get-AzureRmConsumptionUsageDetail
    + Abonelik kullanım ayrıntılarını alma cmdlet'i.
* ContainerRegistry
  - Azure Container Registry için PowerShell cmdlet'leri eklendi
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - Katalog paketleri için alma ve listeleme desteği eklendi
  - Aşağıdaki katalog öğeleri için daha üst öğelerden listeleme desteği eklendi:
    + Tablo
    + TVF
    + Görünüm
    + İstatistikler
* DataLakeStore
  - Performansı artırmak için `Import-AzureRMDataLakeStoreItem` ve `Export-AzureRMDataLakeStoreItem` için izleme günlüğü varsayılan olarak devre dışı bırakıldı. İzleme günlüğünden faydalanmak isterseniz lütfen `-DiagnosticLogLevel` ve `-DiagnosticLogPath` parametrelerini kullanın
  - Bazen ADLS'ye çok sayıda küçük dosya yüklerken PowerShell'in çökmesine neden olan bir hata düzeltildi.
* EventHub
  - Hata düzeltmesi:
    + Set-AzureRmEventHubNamespace cmdlet'inin "Tier" null olamaz, "SkuName" olmalı hatası için düzeltme
    + Set-AzureRmEventHub - EventHub güncelleştirilirken karşılaşılan "Nesne başvurusu bir nesnenin örneğine ayarlanmadı" hatası düzeltildi
* Insights
  - Add-AzureRm*AlertRule
    + Tek bir nesne döndürür: newResource, statusCode, requestId
  - Get-AzureRmAlertRule
    + Çıktı artık tek bir nesne yerine numaralandırılmış alan şeklinde. Türü değişmedi, yine bir liste.
  - Remove-AzureRmAlertRule
    + statusCode, istek tarafından döndürülen durum kodunu takip ediyor, önceden sürekli Tamam şeklindeydi.
  - Add-AzureRmAutoscaleSetting
    + Artık statusCode, requestId ve yeni oluşturulan/güncelleştirilen kaynağı içeren tek bir nesne (eskisi gibi liste değil) döndürüyor.
    + Durum kodu istek tarafından döndürülen durumu takip ediyor, önceden sürekli Tamam şeklindeydi.
  - New-AzureRmAutoscaleRule
    + ScaleActionType parametresi genişletildi, artık şu değerleri alıyor: ChangeCount, PercentChangeCount, ExactCount.
  - Remove-AzureRmAutoscaleSetting
    + Çıktıdaki statusCode, istek tarafından döndürülen statusCode değerini takip ediyor. Önceden sürekli Tamam şeklindeydi.
  - Get-AzureRMLogProfile
    + Çıktı artık numaralandırılmış alan şeklinde. Önceden tek bir nesne olarak kabul ediliyordu. Çıktı türü, daha önce olduğu gibi liste olarak kalıyor.
  - Remove-AzureRmLogProfile
    + PassThru paremetresi uygulandı.
  - Ölçüm API'si
    + SDK artık ölçümleri MDM'den alıyor.
  - Get-AzureRmMetricDefinition
    + Çıktı hala bir liste, ancak liste yapısı değiştirildi.
  - Get-AzureRmMetric
    + Çağrı değiştirildi. Yeni sözdizimi şu şekildedir: Get-AzureRmMetric ResourceId [ÖlçümAdları [ZamanDilimi] [ToplamaTürü] [BaşlangıçZamanı] [BitişZamanı]] [AyrıntılıÇıktı]
    + Çıktı bir liste, ancak öğelerinin yapısı değiştirildi.
* KeyVault
  - KeyVault gizli dizileri için yedekleme/geri yükleme desteği eklendi
    + Gizli diziler yedeklenip geri yüklenebilir, Anahtarlar için desteklenen işlevlerle birlikte kullanılabilir

  - Anahtarlar ve Gizli Diziler için yedekleme cmdlet'leri artık giriş parametresi için karşılık gelen bir nesneyi kabul ediyor
    + Çağıran, alma ve yedekleme işlemlerini birbirine zincirleyebilir: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - Yedekleme cmdlet'i artık var olan bir dosyanın üzerine yazmak için -Force anahtarı kullanılmasını destekliyor
    + Var olan dosyanın üzerine yazma girişiminin artık işlemi sonlandırmayacağını, kullanıcıya nasıl devam etmek istediğinin sorulacağını unutmayın.
* LogicApp
  - Değişim Denetim Numarası olağanüstü durum kurtarma cmdlet'leri için yeni parametreler:
    + İlgili kontrol numaralarını belirtmek için isteğe bağlı -AgreementType parametresi ("X12" veya "Edifact")
* MachineLearning
  - Yeni Azure Machine Learning .Net SDK'sı sürümü kullanılıyor ve yeni bir cmdlet eklendi
    + Add-AzureRmMlWebServiceRegionalProperty
  - Yardım metninde küçük metin düzeltmeleri yapıldı.
* Ağ
  - Test-AzureRmNetworkWatcherConnectivity cmdlet'i eklendi
    + Belirtilen kaynak VM ve hedef için bağlantı durumu bilgilerini döndürür
    + Kaynak ve hedef arasında bağlantı kurulamazsa cmdlet sorunla ilgili ayrıntıları döndürür
* Profil
  - "Send-Feedback" cmdlet'i eklendi: Kullanıcının Azure PowerShell ekibine geri bildirim gönderen komut dizisi başlatmasını sağlar.
  - Azure modülündeki var olan cmdlet adlarıyla çakıştığından aşağıdaki diğer adlar kaldırıldı:
    + `Enable-AzureDataCollection` (destekleyen: `Enable-AzureRmDataCollection`)
    + `Disable-AzureDataCollection` (destekleyen: `Disable-AzureRmDataCollection`)
* Geçiş
  - Kullanıcıların Azure Geçişi kaynakları oluşturmasını ve yönetmesini sağlayan Azure Geçişi cmdlet'leri eklendi.
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* Kaynaklar
  - New-AzureRmResourceGroupDeployment için kaynak grupları arası dağıtım desteği eklendi
    + Kullanıcılar artık farklı kaynak gruplarında dağıtım yapmak için iç içe geçmiş dağıtımlar kullanabilir.
* ServiceBus

  - Hata Düzeltmesi: ServiceBus Kuyruğu nesnesi özellik değerleri null olarak belirlenmişti, nesne Kuyruğu güncelleştirmek için Set-AzureRmServiceBusQueue cmdlet'inde giriş parametresi olarak kullanılıyor.
    - Etkilenen özellikler: LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount ve MessageCount
* ServiceFabric

  - Service Fabric için cmdlet'ler eklendi
    + Add-AzureRmServiceFabricApplicationCertificate       Uygulama sertifikası olarak kullanılacak bir sertifika ekler
    + Add-AzureRmServiceFabricClientCertificate       Küme ayarlarına istemci kimlik doğrulaması için ortak ad veya parmak izi ekler
    + Add-AzureRmServiceFabricClusterCertificate       Var olan sertifikaya geçmek için kümeye ikincil küme sertifikası ekler
    + Add-AzureRmServiceFabricNodes       Bir kümeye belirli bir düğüm türünde düğümler/VM'ler ekler
    + Add-AzureRmServiceFabricNodeType       Var olan bir kümeye düğüm türü/VM'ler ekler
    + Get-AzureRmServiceFabricCluster       Küme kaynağının ayrıntılarını döndürür
    + New-AzureRmServiceFabricCluster Yeni bir ServiceFabric kümesi oluşturur. Bu komut farklı senaryoları kapsayacak şekilde kullanılabilir
    + Remove-AzureRmServiceFabricClientCertificate       Bir kümeye erişmek için kullanılan bir istemci sertifikasını engeller
    + Remove-AzureRmServiceFabricClusterCertificate       Bir kümenin güvenliği için kullanılan bir küme sertifikasını kaldırır
    + Remove-AzureRmServiceFabricNodes       Bir kümede yer alan belirli türdeki düğümleri kaldırır
    + Remove-AzureRmServiceFabricNodeType       Bir kümedeki düğüm türünü kaldırır
    + Remove-AzureRmServiceFabricSettings       Bir kümeden bir veya daha fazla ServiceFabric ayarını kaldırır
    + Set-AzureRmServiceFabricSettings       Bir kümeye bir veya daha fazla ServiceFabric ayarı ekler veya var olan ayarları güncelleştirir
    + Set-AzureRmServiceFabricUpgradeType       Bir kümenin ServiceFabric yükseltme türünü değiştirir
    + Update-AzureRmServiceFabricDurability       Bir kümenin dayanıklılık katmanını değiştirir
    + Update-AzureRmServiceFabricReliability       Bir kümenin güvenilirlik katmanını değiştirir
* Sql
  - New-AzureRmSqlDatabase cmdlet'ine Added -SampleName parametresi eklendi
  - Yük Devretme Grubu cmdlet'leri güncelleştirildi
  - "Etiket" parametreleri kaldırıldı
  - Remove-AzureRmSqlDatabaseFailoverGroup cmdlet'inden "PartnerResourceGroupName" ve "PartnerServerName" parametreleri kaldırıldı
  - New- ve Set- cmdlet'lerine "GracePeriodWithDataLossHours" paremetresi eklendi, "GracePeriodWithDataLossHour" parametresinin yerini alması planlanıyor
  - Belgeler gözden geçirildi ve güncelleştirildi
  - Geri döndürülen nesnelerin biçimi değiştirildi ve alanların doldurulmadığı bazı hatalar düzeltildi
  - Yük Devretme Grubu nesnesine "DatabaseNames" ve "PartnerLocation" özellikleri eklendi
  - Switch- cmdlet'inin işlemin tamamlanmasını beklemek yerine hemen sonuç döndürmesine neden olan hata düzeltildi
  - Yüksek yetkisiz kullanım süresi değerleri kullanıldığında ortaya çıkan tamsayı taşma hatası düzeltildi
  - Daha düşük bir değer girildiğinde yetkisiz kullanım süresi en az 1 saat olacak şekilde ayarlandı
  - Set-AzureRmSqlDatabaseThreatDetectionPolicy ve Set-AzureRmSqlServerThreatDetectionPolicy cmdlet'lerinin "ExcludedDetectionType" parametresinin kabul edilen değerlerinden "Usage_Anomaly" kaldırıldı.
* Depolama
  - SRP SDK'sı 6.3.0 sürümüne yükseltildi
  - New/Set-AzureRmStorageAccount: EnableHttpsTrafficOnly desteği için yeni bir parametre eklendi
  - New/Set/Get-AzureRmStorageAccount: Döndürülen Depolama Hesabı artık yeni EnableHttpsTrafficOnly özniteliğini içeriyor
* Azure Depolama
  - Azure Depolama İstemci Kitaplığı 8.1.1 ve Azure Depolama Veri Taşıma Kitaplığı 0.5.1 sürümüne yükseltildi
  - Blob Artımlı Kopya özelliğini desteklemek için yeni bir cmdlet eklendi
