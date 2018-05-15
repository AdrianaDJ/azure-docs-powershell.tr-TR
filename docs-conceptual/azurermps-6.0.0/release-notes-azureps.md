---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Sürüm notları

Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.

---

## <a name="600---may-2018"></a>6.0.0 - Mayıs 2018

### <a name="general"></a>Genel
* Modüllerin PowerShell 5.0’a en düşük bağımlılığını ayarlama

### <a name="azurestorage"></a>Azure Depolama
* Depolama blob kapsayıcı adı olarak destek
    - New-AzureStorageBlobContainer
    - Remove-AzureStorageBlobContainer
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* Bazı Depolama cmdlet’lerinin hata çıktısının ayrıntılı hata bilgilerini içermediği sorun düzeltildi

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Birden çok hataya neden olan değişiklik eklendi
    - Daha fazla bilgi için lütfen geçiş kılavuzuna bakın

### <a name="azurermautomation"></a>AzureRM.Automation
* Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı
    - 'Set-AzureRmAutomationRunbook'

### <a name="azurermbatch"></a>AzureRM.Batch
* New-AzureBatchPool belgeleri kullanım dışı örneği kaldırmak üzere güncelleştirildi

### <a name="azurermcdn"></a>AzureRM.Cdn
* Birden çok hataya neden olan değişiklik eklendi
    - Daha fazla bilgi için lütfen geçiş kılavuzuna bakın

### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVm' ve 'New-AzureRmVmss', parametrelerin ayrıntılı çıktısını destekler
* 'New-AzureRmVm' ve 'New-AzureRmVmss' (tek parametre kümesi), sanal makinelere kullanıcı tanımlı ve(veya) sistem tanımlı kimlikler atamayı destekler.
* VMSS Redeploy ve PerformMaintenance özelliği
    -  Yeni -Redeploy ve -PerformMaintenance anahtar parametresi 'Set-AzureRmVmss' ve 'Set-AzureRmVmssVM' içine eklendi
* DisableVMAgent anahtar parametresi 'Set-AzureRmVMOperatingSystem' cmdlet’ine eklendi
* 'New-AzureRmVm' ve 'New-AzureRmVmss' (basit parametre kümesi) bir 'Win10' görüntüsünü destekler.
* 'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet’i eklendi.
* Birden çok hataya neden olan değişiklik eklendi
    - Daha ayrıntılı bilgi için lütfen geçiş kılavuzuna bakın
* 'Set-AzureRmVmDiskEncryptionExtension', AAD parametrelerini isteğe bağlı yapar

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* ADF .Net SDK sürümü, aşağıdaki değişiklikleri içeren 0.7.0-preview sürümüne güncelleştirildi:
    - ExecuteSSISPackage Etkinliğine yürütme parametreleri ve connection managers özelliği eklendi
    - PostgreSql, MySql bağlı hizmeti, sunucu, veritabanı, şema, kullanıcı ve parola yerine tam bağlantı dizesini kullanacak şekilde güncelleştirildi
    - Şemaya DB2 bağlı hizmetinden kaldırdı
    - Schema özelliği Teradata bağlı hizmetinden kaldırıldı
    - Responsys için LinkedService, Dataset, CopySource eklendi

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı
    - 'New-AzureRmDataLakeAnalyticsAccount'
    - 'Set-AzureRmDataLakeAnalyticsAccount'

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Özyinelemeli yeni Acl Değişikliği özelliği Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl cmdlet’lerine eklendi
* Bir dizin altındaki içerik özetini almak için yeni cmdlet eklendi
* Disk kullanımı ve Acl yedek kopyasını almak için yeni cmdlet eklendi
* Set-AzureRmDataLakeStoreItemAcl bool değerinin dönüş türü IEnumerable<DataLakeStoreItemAce> olarak düzeltildi
* Set-AzureRmDataLakeStoreItemAclEntry bool değerinin dönüş türü IEnumerable<DataLakeStoreItemAce> olarak düzeltildi
* Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem cmdlet’lerinde hataya neden olan değişiklikler

### <a name="azurermdns"></a>AzureRM.Dns
* Birden çok hataya neden olan değişiklik eklendi
    - Daha fazla bilgi için lütfen geçiş kılavuzuna bakın

### <a name="azurermeventhub"></a>AzureRM.EventHub
* Cmdlet Yardımı, eksik örneklerle güncelleştirildi

### <a name="azurerminsights"></a>AzureRM.Insights
* Birden çok hataya neden olan değişiklik eklendi
    - Daha fazla bilgi için lütfen geçiş kılavuzuna bakın

### <a name="azurermiothub"></a>AzureRM.IotHub
* IotHub’da etiketler ve Temel Sku etkinleştirildi

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Kanal oluşturma senaryolarını desteklemek amacıyla hataya neden olan değişiklikler
* Yeni cmdlet’ler eklendi: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval ve Undo-AzureKeyVaultManagedStorageAccountRemoval

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* Kullanım dışı 'Tags' diğer adı cmdlet’lerden kaldırıldı
    - 'Set-AzureRmMediaService'

### <a name="azurermnetwork"></a>AzureRM.Network
* DDoS koruması plan kaynağı için destek eklendi
* Birden çok hataya neden olan değişiklik eklendi
    - Daha fazla bilgi için lütfen geçiş kılavuzuna bakın

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Birden çok hataya neden olan değişiklik eklendi
    - Daha fazla bilgi için lütfen geçiş kılavuzuna bakın

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Birden çok hataya neden olan değişiklik eklendi
    - Daha fazla bilgi için lütfen geçiş kılavuzuna bakın

### <a name="azurermprofile"></a>AzureRM.Profile
* Bağlam otomatik kaydı varsayılan olarak etkinleştirildi
* Azure US Gov ortamına USGovernmentOperationalInsightsEndpoint ve USGovernmentOperationalInsightsEndpointResourceId özellikleri eklendi.

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* SiteRecovery senaryolarında Kimlik Doğrulama Üst Bilgisi düzeltildi

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Birden çok hataya neden olan değişiklik eklendi
    - Daha fazla bilgi için lütfen geçiş kılavuzuna bakın

### <a name="azurermresources"></a>AzureRM.Resources
* Geçersiz -AtScopeAndBelow parametresi Get-AzureRmRoledefinition çağrısından kaldırıldı
* Silinen USers/Groups/ServicePrincipals atamaları Get-AzureRmRoleAssignment sonucuna eklendi
* Scope ve ResourceType için Tab tamamlayıcıları eklendi
* ServicePrincipals oluşturmak için kolaylık cmdlet’i eklendi
* Get- ve Find- işlevselliği Get-AzureRmResource içinde birleştirildi
* AD Cmdlet’leri eklendi:
  - Remove-AzureRmADGroupMember
  - Get-AzureRmADGroup
  - New-AzureRmADGroup
  - Remove-AzureRmADGroup
  - Remove-AzureRmADUser
  - Update-AzureRmADApplication
  - Update-AzureRmADServicePrincipal
  - Update-AzureRmADUser

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Varsayılan Linux görüntü sürümü sku’su güncelleştirildi
  - NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku güncelleştirmesi

### <a name="azurermstorage"></a>AzureRM.Storage
* Birden çok hataya neden olan değişiklik eklendi
    - Daha fazla bilgi için lütfen geçiş kılavuzuna bakın

### <a name="azurermwebsites"></a>AzureRM.Websites
* Web Siteleri SDK'sının en son sürümüne yükseltildi
* Set-AzureRmWebApp ve Set-AzureRmWebAppSlot için -AssignIdentity ve -Httpsonly özellikleri eklendi
* İki yeni cmdlet eklendi: Get-AzureRmWebAppSnapshots ve Restore-AzureRmWebAppSnapshot
