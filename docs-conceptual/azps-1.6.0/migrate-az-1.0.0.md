---
title: Microsoft Azure PowerShell Az 1.0.0 için yeni değişiklikler
description: Bu geçiş kılavuzu, Azure PowerShell Az sürüm 1 yayınında yapılan yeni değişikliklerin listesini içerir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475678"
---
# <a name="migration-guide-for-az-100"></a>Az 1.0.0 için Geçiş Kılavuzu

Bu belgede AzureRM’nin 6.x sürümleri ile Az 1.0.0 sürümü arasındaki değişiklikler açıklanır.

## <a name="table-of-contents"></a>İçindekiler
- [Hataya neden olan genel değişiklikler](#general-breaking-changes)
  - [Cmdlet İsim Öneki Değişiklikleri](#cmdlet-noun-prefix-changes)
  - [Modül adı değişiklikleri](#module-name-changes)
  - [Kaldırılan modüller](#removed-modules)
  - [Windows PowerShell 5.1 ve .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [PSCredential ile Kullanıcı oturumu açmanın geçici olarak kaldırılması](#temporary-removal-of-user-login-using-pscredential)
  - [Web Tarayıcısı istemi yerine varsayılan Cihaz Kodu ile oturum açma](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [Modüldeki yeni değişiklikler](#module-breaking-changes)
  - [Az.ApiManagement (eski adıyla AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (eski adıyla AzureRM.Billing, AzureRM.Consumption ve AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (eski adıyla AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (eski adıyla AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (eski adıyla AzureRM.DataFactories ve AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (eski adıyla AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (eski adıyla AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (eski adıyla AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (eski adıyla AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (eski adıyla AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (eski adıyla AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (eski adıyla AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (eski adıyla AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup ve AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (eski adıyla AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (eski adıyla AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (eski adıyla AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (eski adıyla Azure.Storage and AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (eski adıyla AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>Hataya neden olan genel değişiklikler
### <a name="cmdlet-noun-prefix-changes"></a>Cmdlet İsim Öneki Değişiklikleri
AzureRM’de cmdlet’ler ya 'AzureRM' ya da 'Azure' isim önekini kullanıyordu.  Az ile birlikte cmdlet adları basitleştirilip normalleştirilerek tüm cmdlet’lerin isim öneki olarak 'Az' kullanılacak. Örnek:
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

Şuna dönüştü:
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

Bu yeni cmdlet adlarına geçişi kolaylaştırmak için Az ile birlikte iki yeni cmdlet sunuluyor: ```Enable-AzureRmAlias``` ve ```Disable-AzureRmAlias```.  ```Enable-AzureRmAlias```, AzureRM’deki eski cmdlet adlarından yeni Az cmdlet adlarına diğer adlar oluşturur.  Bu cmdlet, geçerli oturumda ya da tüm oturumlarda kullanıcı veya makine profilinizi değiştirerek diğer ad oluşturmanıza imkan tanır. 

Örneğin, şu AzureRM betiği:
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

```Enable-AzureRmAlias``` kullanılarak küçük değişikliklerle çalıştırılabilir:
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

```Enable-AzureRmAlias -Scope CurrentUser``` çalıştırıldığında açtığınız tüm powershell oturumları için diğer adları etkinleştireceğinden, bu cmdlet’i çalıştırdıktan sonra şunun gibi bir betiğin hiç değiştirilmesi gerekmez:
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Diğer ad cmdlet’lerinin kullanımıyla ilgili tüm ayrıntıları öğrenmek için powershell isteminden şunu yürütün: ```Get-Help -Online Enable-AzureRmAlias```.

```Disable-AzureRmAlias```, ```Enable-AzureRmAlias``` tarafından oluşturulan AzureRM cmdlet diğer adlarını kaldırır.  Tüm ayrıntıları öğrenmek için powershell isteminden şunu yürütün: ```Get-Help -Online Disable-AzureRmAlias```.

### <a name="module-name-changes"></a>Modül Adı Değişiklikleri
- Aşağıdaki modüller dışında, önceden `AzureRM.*` olan modül adları `Az.*` olarak değiştirildi:
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

Modül adlarındaki değişiklikler nedeniyle, belirli modülleri yüklemek için ```#Requires``` ve ```Import-Module``` deyimlerini kullanan tüm betiklerin yeni modülü kullanacak şekilde güncelleştirilmesi gerekir.

#### <a name="migrating-requires-statements"></a>#Requires Deyimlerini Geçirme
AzureRM modüllerine bağımlılığı bildirmek için #Requires deyimini kullanan betikler yeni modül adlarını kullanacak şekilde güncelleştirilmelidir
```powershell
#Requires -Module AzureRM.Compute
```

Şöyle değiştirilmelidir:
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a>Import-Module Deyimlerini Geçirme
AzureRM modüllerini yüklemek için ```Import-Module``` deyimini kullanan betikler yeni modül adlarını yansıtacak şekilde güncelleştirilmelidir.
```powershell
Import-Module -Name AzureRM.Compute
```

Şöyle değiştirilmelidir:
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Tam Olarak Nitelenen Cmdlet Çağrılarını Geçirme
Şunun gibi modül adıyla nitelenen cmdlet çağrılarını kullanan betikler:
```powershell
AzureRM.Compute\Get-AzureRmVM
```

Yeni modülü ve cmdlet adlarını kullanacak şekilde değiştirilmelidir
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Modül Bildirimi Bağımlılıklarını Geçirme
Bir modül bildirimi (.psd1) dosyası aracılığıyla AzureRM modüllerine bağımlılığı ifade eden modüllerin 'RequiredModules' bölümünde güncelleştirilmiş modül adları olmalıdır

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Şöyle değiştirilmelidir:

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Kaldırılan modüller
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Bu hizmetlere yönelik araçlar artık etkin bir şekilde desteklenmemektedir.  Müşterilerin uygun olan en yakın zamanda alternatif hizmetlere geçmesi önerilir.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 ve .NET 4.7.2
- Windows PowerShell 5.1 ile Az kullanımı, .NET 4.7.2 sürümünün yüklenmesini gerektirir. Bununla birlikte, PowerShell Core ile Az kullanımı için .NET 4.7.2 gerekmez. 

### <a name="temporary-removal-of-user-login-using-pscredential"></a>PSCredential ile Kullanıcı oturumu açmanın geçici olarak kaldırılması
- .NET Standard kimlik doğrulama akışındaki değişiklikler nedeniyle, PSCredential üzerinden kullanıcı oturumu açmayı geçici olarak kaldırıyoruz. Bu özellik, Windows PowerShell 5.1’in 15.01.2019 tarihli yayınında yeniden kullanıma sunulacaktır. Bu konu, [bu sorunda](https://github.com/Azure/azure-powershell/issues/7430) ayrıntılı olarak ele alınmıştır.

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Web Tarayıcısı istemi yerine varsayılan Cihaz Kodu ile oturum açma
- .NET Standard kimlik doğrulama akışındaki değişiklikler nedeniyle, etkileşimli oturum açma sırasında varsayılan oturum açma akışı olarak cihazla oturum açmayı kullanıyoruz. Web tarayıcısı tabanlı oturum açma, Windows PowerShell 5.1 için 15.01.2019 tarihli yayınla birlikte yeniden varsayılan seçenek olarak kullanıma sunulacaktır. İlgili tarihte, kullanıcılar bir Switch parametresini kullanarak cihaz oturumunu seçebilecek.

## <a name="module-breaking-changes"></a>Modüldeki yeni değişiklikler

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (eski adıyla AzureRM.ApiManagement)
- Şu cmdlet’ler kaldırılıyor:
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Bu özellikleri ayarlamak için bunun yerine **Set-AzApiManagement** cmdlet’ini kullanın
- Aşağıdaki özellikler kaldırıldı
  - `PsApiManagementContext` öğesinden `PsApiManagementHostnameConfiguration` türündeki `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` ve `ScmHostnameConfiguration` özelliği kaldırıldı. Bunun yerine `PsApiManagementCustomHostNameConfiguration` türündeki `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` ve `ScmCustomHostnameConfiguration` özelliğini kullanın.
  - PsApiManagementContext öğesinden `StaticIPs` özelliği kaldırıldı. Özellik `PublicIPAddresses` ve `PrivateIPAddresses` olarak bölündü.
  - New-AzureApiManagementVirtualNetwork cmdlet’inden gerekli olan `Location` özelliği kaldırıldı.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (eski adıyla AzureRM.Billing, AzureRM.Consumption ve AzureRM.UsageAggregates)
- `Get-AzConsumptionUsageDetail` cmdlet’inden `InvoiceName` parametresi kaldırıldı.  Fatura için betiklerin diğer kimlik parametrelerini kullanması gerekir.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (eski adıyla AzureRM.CognitiveServices)
- `Get-AzCognitiveServicesAccountSkus` cmdlet’inden `GetSkusWithAccountParamSetName` parametre kümesi kaldırıldı.  ResourceGroupName ve Hesap Adı parametrelerini kullanmak yerine Sku’ları Hesap Türüne ve Konuma göre almalısınız.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (eski adıyla AzureRM.Compute)
- `PSVirtualMachine` ve `PSVirtualMachineScaleSet` nesnelerinde `Identity` özelliğinden `IdentityIds` kaldırıldı Betikler artık işleme kararları vermek için bu alanın değerini kullanmamalıdır.
- `PSVirtualMachineScaleSetVM` nesnesinin `InstanceView` özelliğinin `VirtualMachineInstanceView` olan türü `VirtualMachineScaleSetVMInstanceView` olarak değiştirildi
- `UpgradePolicy` özelliğinden `AutoOSUpgradePolicy` ve `AutomaticOSUpgrade` özelliği kaldırıldı
- `PSSnapshotUpdate` nesnesindeki `Sku` özelliğinin `DiskSku` olan türü `SnapshotSku` olarak değiştirildi
- `Add-AzVMDataDisk` cmdlet’inden `VmScaleSetVMParameterSet` kaldırıldı, artık tek bir ScaleSet sanal makinesine veri diski ekleyemezsiniz.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (eski adıyla AzureRM.DataFactories ve AzureRM.DataFactoryV2)
- `New-AzDataFactoryEncryptValue` cmdlet’inde `GatewayName` parametresi zorunlu hale geldi
- `New-AzDataFactoryGatewayKey` cmdlet'i kaldırıldı
- `Get-AzDataFactoryV2ActivityRun` cmdlet’inden `LinkedServiceName` parametresi kaldırıldı Betikler artık işleme kararları vermek için bu alanın değerini kullanmamalıdır.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (eski adıyla AzureRM.DataLakeAnalytics)
- Kullanım dışı cmdlet’ler kaldırıldı: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` ve `Set-AzDataLakeAnalyticsCatalogSecret`

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (eski adıyla AzureRM.DataLakeStore)
- Aşağıdaki cmdlet’lerin `Encoding` parametresinin `FileSystemCmdletProviderEncoding` olan türü `System.Text.Encoding` olarak değişti. Bu değişiklikle birlikte `String` ve `Oem` kodlama değerleri kaldırılıyor. Önceki diğer tüm kodlama değerleri olduğu gibi kaldı.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- `New-AzDataLakeStoreAccount` ve `Set-AzDataLakeStoreAccount` cmdlet’inden kullanım dışı `Tags` özellik diğer adı kaldırıldı

  Şunları kullanan betikler:
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  Şöyle değiştirilmelidir:
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- ```PSDataLakeStoreAccountBasic``` nesnesinden kullanım dışı ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` özelliği kaldırıldı.  ```Get-AzDataLakeStoreAccount``` cmdlet’inden döndürülen ```PSDatalakeStoreAccount``` özelliğini kullanan hiçbir betik bu özelliklere başvurmamalıdır.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (eski adıyla AzureRM.KeyVault)
- `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` ve `PSKeyVaultSecretAttributes` nesnesinden `PurgeDisabled` özelliği kaldırıldı Betikler artık işleme kararları vermek için ```PurgeDisabled``` özelliğine başvurmamalıdır.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (eski adıyla AzureRM.Media)
- `New-AzMediaService` cmdlet’inden kullanım dışı `Tags` özelliği diğer adı kaldırıldı Şunları kullanan betikler:
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  Şöyle değiştirilmelidir:
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (eski adıyla AzureRM.Insights)
- `Set-AzDiagnosticSetting` cmdlet’inden alınan tekil parametre adları tercih edilerek çoğul ad `Categories` ve `Timegrains` parametresi kaldırıldı Şunları kullanan betikler:
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  Şöyle değiştirilmelidir:
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (eski adıyla AzureRM.Network)
- `Get-AzServiceEndpointPolicyDefinition` cmdlet’inden kullanım dışı `ResourceId` parametresi kaldırıldı
- `PSVirtualNetwork` nesnesinden kullanım dışı `EnableVmProtection` özelliği kaldırıldı
- Kullanım dışı `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet’i kaldırıldı
  
Betikler artık bu alanların değerlerini temel alan işleme kararları almamalıdır.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (eski adıyla AzureRM.OperationalInsights)
- `Get-AzOperationalInsightsDataSource` için varsayılan parametre kümesi kaldırıldı, varsayılan parametre kümesi `ByWorkspaceNameByKind` oldu

  Veri kaynaklarını şunu kullanarak listeleyen betikler:
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  Bir Tür belirtecek şekilde değiştirilmelidir
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (eski adıyla AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup ve AzureRM.RecoveryServices.SiteRecovery)
- `New/Set-AzRecoveryServicesAsrPolicy` cmdlet’inden `Encryption` parametresi kaldırıldı
- Artık `Restore-AzRecoveryServicesBackupItem` cmdlet'indeki yönetilen disk geri yükleme işlemleri için `TargetStorageAccountName` parametresi zorunludur
- `Restore-AzRecoveryServicesBackupItem` cmdlet’inden `StorageAccountName` ve `StorageAccountResourceGroupName` parametresi kaldırıldı
- `Get-AzRecoveryServicesBackupContainer` cmdlet’inden `Name` parametresi kaldırıldı

### <a name="azresources-previously-azurermresources"></a>Az.Resources (eski adıyla AzureRM.Resources)
- `New/Set-AzPolicyAssignment` cmdlet’inden `Sku` parametresi kaldırıldı
- `New-AzADServicePrincipal` ve `New-AzADSpCredential` cmdlet’inden `Password` parametresi kaldırıldı Parolalar otomatik olarak oluşturulduğundan, daha önce parolayı sağlayan betikler:
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Parolayı çıktıdan alacak şekilde değiştirilmelidir:
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (eski adıyla AzureRM.ServiceFabric)
- Aşağıdaki cmdlet dönüş türleri değişmiştir:
  - `ApplicationHealthPolicy` türündeki `SerivceTypeHealthPolicies` özelliği kaldırıldı.
  - `ClusterUpgradeDeltaHealthPolicy` türündeki `ApplicationHealthPolicies` özelliği kaldırıldı.
  - `ClusterUpgradePolicy` türündeki `OverrideUserUpgradePolicy` özelliği kaldırıldı.
  - Bu değişikliklerden aşağıdaki cmdlet’ler etkilenir:
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql (eski adıyla AzureRM.Sql)
- `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet’inden `State` ve `ResourceId` parametresi kaldırıldı
- Kullanım dışı cmdlet’ler kaldırıldı: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`
- `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet’inden kullanım dışı `Current` parametresi kaldırıldı
- `Get-AzSqlServerServiceObjective` cmdlet’inden kullanım dışı `DatabaseName` parametresi kaldırıldı
- `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet’inden kullanım dışı `PrivilegedLogin` parametresi kaldırıldı

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (eski adıyla Azure.Storage and AzureRM.Storage)
- Yalnızca depolama hesabı adıyla bir Oauth depolama bağlamı oluşturulmasının desteklenmesi için varsayılan parametre kümesi `OAuthParameterSet` olarak değiştirildi
  - Örnek: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- `Get-AzStorageUsage` cmdlet’inde `Location` parametresi zorunlu hale geldi
- Depolama API’si metotları artık zaman uyumlu API çağrıları yerine Görev Tabanlı Zaman Uyumsuz Düzeni (TAP) kullanıyor.
#### <a name="1-blob-snapshot"></a>1. Blob Anlık Görüntüsü
##### <a name="before"></a>Önce:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a>Sonra:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a>2. Anlık Görüntüyü Paylaş
##### <a name="before"></a>Önce:
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a>Sonra:
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a>3. Geçici silme işlemini geri alma
##### <a name="before"></a>Önce:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a>Sonra:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a>4. Blob Katmanını Ayarla
##### <a name="before"></a>Önce:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a>Sonra:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (eski adıyla AzureRM.Websites)
- `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` ve `PSSite` nesnesinden kullanım dışı özellikler kaldırıldı