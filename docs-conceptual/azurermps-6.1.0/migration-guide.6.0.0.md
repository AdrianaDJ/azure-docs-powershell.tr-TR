---
title: Microsoft Azure PowerShell 6.0.0 için hataya neden olan değişiklikler
description: Bu geçiş kılavuzu, Azure PowerShell sürüm 6 yayınında yapılan ve hataya neden olan değişikliklerin bir listesini içerir.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: d73fbac10bc3876e722c564df283222f7f5b9824
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2018
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Microsoft Azure PowerShell 6.0.0 için hataya neden olan değişiklikler

Bu belge, Microsoft Azure PowerShell cmdlet’lerini kullananlar için hem bozucu değişiklik bildirimi hem de geçiş kılavuzu olarak sağlanır. Her bölümde hem bozucu değişikliğin yapılma nedeni hem de en kolay geçiş yolu açıklanır. Bağlamla ilgili daha ayrıntılı bilgi edinmek için lütfen her bir değişiklikle ilişkili çekme isteğine başvurun.

## <a name="table-of-contents"></a>İçindekiler

- [Hataya neden olan genel değişiklikler](#general-breaking-changes)
    - [Gereken en düşük PowerShell sürümü 5.0’a yükseldi](#minimum-powershell-version-required-bumped-to-50)
    - [Varsayılan olarak etkinleştirilen bağlam otomatik kaydı](#context-autosaved-enabled-by-default)
    - [Etiket diğer adlarının kaldırılması](#removal-of-tags-alias)
- [AzureRM.Compute cmdlet’lerinde hataya neden olan değişiklikler](#breaking-changes-to-azurermcompute-cmdlets)
- [AzureRM.DataLakeStore cmdlet’lerinde hataya neden olan değişiklikler](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [AzureRM.Dns cmdlet’lerinde hataya neden olan değişiklikler](#breaking-changes-to-azurermdns-cmdlets)
- [AzureRM.Insights cmdlet’lerinde hataya neden olan değişiklikler](#breaking-changes-to-azurerminsights-cmdlets)
- [AzureRM.KeyVault cmdlet’lerinde hataya neden olan değişiklikler](#breaking-changes-to-azurermkeyvault-cmdlets)
- [AzureRM.Network cmdlet’lerinde hataya neden olan değişiklikler](#breaking-changes-to-azurermnetwork-cmdlets)
- [AzureRM.RedisCache cmdlet’lerinde hataya neden olan değişiklikler](#breaking-changes-to-azurermrediscache-cmdlets)
- [AzureRM.Resources cmdlet’lerinde hataya neden olan değişiklikler](#breaking-changes-to-azurermresources-cmdlets)
- [AzureRM.Storage cmdlet’lerinde hataya neden olan değişiklikler](#breaking-changes-to-azurermstorage-cmdlets)
- [Kaldırılan modüller](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>Hataya neden olan genel değişiklikler

### <a name="minimum-powershell-version-required-bumped-to-50"></a>Gereken en düşük PowerShell sürümü 5.0’a yükseldi

Daha önce, Azure PowerShell’in herhangi bir cmdlet’i çalıştırması için _en az_ PowerShell 3.0 sürümü gerekliydi. Sonraları bu gereksinim PowerShell 5.0 sürümüne yükseltilecektir. PowerShell 5.0’a yükseltme yapma hakkında bilgi için lütfen [bu tabloya](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell) bakın.

### <a name="context-autosave-enabled-by-default"></a>Varsayılan olarak etkinleştirilen bağlam otomatik kaydı

Bağlam otomatik kaydı, yeni ve farklı PowerShell oturumları arasında kullanılabilen Azure oturum açma bilgilerinin depolanmasıdır. Bağlam otomatik kaydı hakkında daha fazla bilgi için lütfen [bu belgeye](https://docs.microsoft.com/en-us/powershell/azure/context-persistence) bakın.

Daha önce bağlam otomatik kaydı varsayılan olarak devre dışıydı. Diğer bir deyişle, Azure oturum açma bilgileri bağlam kalıcılığını etkinleştiren `Enable-AzureRmContextAutosave` cmdlet’i çalıştırılana kadar oturumlar arasında depolanmıyordu. Sonraları, bağlam otomatik kaydı varsayılan etkin duruma geldi ve _bağlam otomatik kaydı ayarları olmayan_ kullanıcıların bağlamları sonraki oturum açmada depolanmaya başladı. Kullanıcılar `Disable-AzureRmContextAutosave` cmdlet'ini kullanarak bu işlevselliği kullanmamayı seçebilir.

_Not_: Daha önce bağlam otomatik kaydını devre dışı bırakmış veya bağlam otomatik kaydı etkin olan kullanıcılar ve mevcut bağlamlar bu değişiklikten etkilenmeyecektir

### <a name="removal-of-tags-alias"></a>Etiket diğer adlarının kaldırılması

`Tag` parametresinin `Tags` diğer adı, çok sayıda cmdlet'ten kaldırıldı. Bu değişiklikten etkilenen modüllerin (ve karşılık gelen cmdlet'lerin) listesi aşağıda verilmiştir:

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>AzureRM.Compute cmdlet’lerinde hataya neden olan değişiklikler

**Çeşitli**
- `PSDisk` ve `PSSnapshot` türlerinde iç içe yerleştirilmiş sku name özelliğinin `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- `PSVirtualMachine`, `PSVirtualMachineScaleSet` ve `PSImage` türlerinde iç içe yerleştirilmiş storage account type özelliğinin `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- `StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**Add-AzureRmVMDataDisk**
- `StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**Add-AzureRmVmssDataDisk**
- `StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**New-AzureRmAvailabilitySet**
- `Managed` parametresi kaldırılarak `Sku` ile değiştirildi

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- `SkuName` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**New-AzureRmDiskUpdateConfig**
- `SkuName` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**New-AzureRmSnapshotConfig**
- `SkuName` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**New-AzureRmSnapshotUpdateConfig**
- `SkuName` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**Set-AzureRmImageOsDisk**
- `StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**Set-AzureRmVMAEMExtension**
- `DisableWAD` parametresi kaldırıldı
    -  Windows Azure Tanılama varsayılan olarak devre dışıdır

**Set-AzureRmVMDataDisk**
- `StorageAccountType` parametresinin kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**Set-AzureRmVMOSDisk**
- `StorageAccountType` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**Set-AzureRmVmssStorageProfile**
- `ManagedDisk` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

**Update-AzureRmVmss**
- `ManagedDiskStorageAccountType` parametresi için kabul edilen `StandardLRS` ve `PremiumLRS` değerleri sırasıyla `Standard_LRS` ve `Premium_LRS` değerleriyle değiştirildi

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>AzureRM.DataLakeStore cmdlet’lerinde hataya neden olan değişiklikler

**Export-AzureRmDataLakeStoreItem**
- `PerFileThreadCount` ve `ConcurrentFileCount` parametreleri kaldırıldı. Lütfen bundan sonra `Concurrency` parametresini kullanın

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- `PerFileThreadCount` ve `ConcurrentFileCount` parametreleri kaldırıldı. Lütfen bundan sonra `Concurrency` parametresini kullanın

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- `Clean` parametresi kaldırıldı

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>AzureRM.Dns cmdlet’lerinde hataya neden olan değişiklikler

**New-AzureRmDnsRecordSet**
- `Force` parametresi kaldırıldı

**Remove-AzureRmDnsRecordSet**
- `Force` parametresi kaldırıldı

**Remove-AzureRmDnsZone**
- `Force` parametresi kaldırıldı

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>AzureRM.Insights cmdlet’lerinde hataya neden olan değişiklikler

**Add-AzureRmAutoscaleSetting**
- `AutoscaleProfiles` ve `Notifications` parametre diğer adları kaldırıldı

**Add-AzureRmLogProfile**
- `Categories` ve `Locations` parametre diğer adları kaldırıldı

**Add-AzureRmMetricAlertRule**
- `Actions` parametre diğer adı kaldırıldı

**Add-AzureRmWebtestAlertRule**
- `Actions` parametre diğer adı kaldırıldı

**Get-AzureRmLog**
- `MaxRecords` ve `MaxEvents` parametre diğer adları kaldırıldı

**Get-AzureRmMetricDefinition**
- `MetricNames` parametre diğer adı kaldırıldı

**New-AzureRmAlertRuleEmail**
- `CustomEmails` ve `SendToServiceOwners` parametre diğer adları kaldırıldı

**New-AzureRmAlertRuleWebhook**
- `Properties` parametre diğer adı kaldırıldı

**New-AzureRmAutoscaleNotification**
- `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` ve `Webhooks` parametre diğer adları kaldırıldı

**New-AzureRmAutoscaleProfile**
- `Rules`, `ScheduleDays`, `ScheduleHours` ve `ScheduleMinutes` parametre diğer adları kaldırıldı

**New-AzureRmAutoscaleWebhook**
- `Properties` parametre diğer adı kaldırıldı

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>AzureRM.KeyVault cmdlet’lerinde hataya neden olan değişiklikler

**Add-AzureKeyVaultCertificate**
- `Certificate` parametresi zorunlu hale geldi.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- Cmdlet artık erişim belirtecini oluşturan tek parametreleri kabul etmez; bunun yerine cmdlet, `Service` veya `Permissions` gibi açık belirteç parametrelerini, başka bir yerde tanımlanmış örnek bir erişim belirtecine karşılık gelen genel bir `TemplateUri` parametresi ile değiştirir (büyük olasılıkla Depolama PowerShell cmdlet’lerini kullanarak veya Depolama belgelerine uygun şekilde el ile oluşturarak.) Cmdlet `ValidityPeriod` parametresini korur.

Azure Depolama için paylaşılan erişim belirteçleri oluşturma hakkında daha fazla bilgi için lütfen belgeler sayfasına sırasıyla bakın:
- [Hizmet SAS oluşturma] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)
- [Hesap SAS oluşturma] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- `IssuerProvider` parametresi zorunlu hale geldi.

**Undo-AzureKeyVaultCertificateRemoval**
- Bu cmdlet’in `CertificateBundle` olan çıktısı `PSKeyVaultCertificate` olarak değiştirildi.

**Undo-AzureRmKeyVaultRemoval**
- `ResourceGroupName`, `InputObject` parametre kümesinden kaldırıldı ve onun yerine `InputObject` parametresinin `ResourceId` özelliği elde edildi.

**Set-AzureRmKeyVaultAccessPolicy**
- `all` izni `PermissionsToKeys`, `PermissionsToSecrets` ve `PermissionsToCertificates` içinden kaldırıldı.

**Genel**
- `ValueFromPipelineByPropertyName` özelliği, `InputObject` ile kanal oluşturmanın etkin olduğu tüm cmdlet'lerden kaldırıldı.  Etkilenen cmdlet'ler şunlardır:
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- `ConfirmImpact` düzeyleri tüm cmdlet'lerden kaldırıldı.  Etkilenen cmdlet'ler şunlardır:
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- `IKeyVaultDataServiceClient`, tüm Certificate işlemleri SDK türleri yerine PSTypes döndürecek şekilde güncelleştirildi. Buna aşağıdakiler dahildir:
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>AzureRM.Network cmdlet’lerinde hataya neden olan değişiklikler


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- `ProbeEnabled` parametresi kaldırıldı

**Add-AzureRmVirtualNetworkPeering**
- `AlloowGatewayTransit` parametre diğer adı kaldırıldı

**New-AzureRmApplicationGatewayBackendHttpSettings**
- `ProbeEnabled` parametresi kaldırıldı

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- `ProbeEnabled` parametresi kaldırıldı

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>AzureRM.RedisCache cmdlet’lerinde hataya neden olan değişiklikler

**New-AzureRmRedisCache**
- `Subnet` ve `VirtualNetwork` parametreleri kaldırılarak `SubnetId` ile değiştirildi
- `RedisVersion` parametresi kaldırıldı
- `MaxMemoryPolicy` parametresi kaldırılarak `RedisConfiguration` ile değiştirildi

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- `MaxMemoryPolicy` parametresi kaldırılarak `RedisConfiguration` ile değiştirildi

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>AzureRM.Resources cmdlet’lerinde hataya neden olan değişiklikler

**Find-AzureRmResource**
- Bu cmdlet kaldırıldı ve işlevsellik `Get-AzureRmResource` içine taşındı

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- Bu cmdlet kaldırıldı ve işlevsellik `Get-AzureRmResourceGroup` içine taşındı

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- `AtScopeAndBelow` parametresi kaldırıldı.

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>AzureRM.Storage cmdlet’lerinde hataya neden olan değişiklikler

**New-AzureRmStorageAccount**
- `EnableEncryptionService` parametresi kaldırıldı

**Set-AzureRmStorageAccount**
- `EnableEncryptionService` ve `DisableEncryptionService` parametreleri kaldırıldı

## <a name="removed-modules"></a>Kaldırılan modüller

### `AzureRM.ServerManagement`

Sunucu Yönetim Araçları hizmeti [geçen yıl kullanımdan kaldırıldı](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/) ve sonuç olarak SMT için karşılık gelen `AzureRM.ServerManagement` modülü, `AzureRM` içinden kaldırıldı ve bundan sonra gönderilmeyecek.

### `AzureRM.SiteRecovery`

`AzureRM.SiteRecovery` modülünün yerini, `AzureRM.SiteRecovery` modülünün işlevsel bir alt kümesi olup eşdeğer cmdlet’lerden oluşan yeni bir küme içeren `AzureRM.RecoveryServices.SiteRecovery` alacak. Eski ve yeni cmdlet'lerin eşlemelerini içeren tam liste aşağıda bulunabilir:

| Kullanım dışı bırakılan cmdlet                                        | Eşdeğer cmdlet                                                | Diğer adlar                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |