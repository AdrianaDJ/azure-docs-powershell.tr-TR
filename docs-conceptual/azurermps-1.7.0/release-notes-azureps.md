---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 9f31fe404cca1162d5e4898287261f1bcbfa0f3a
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821862"
---
# <a name="release-notes"></a>Sürüm notları

Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.

## <a name="version-170"></a>Sürüm 1.7.0

* **Tüm cmdlet’lerin -Force, –Confirm ve $ConfirmPreference parametreleri için davranış değişikliği. Bu uygulama PowerShell yönergelerine uygun olacak şekilde değiştirilmektedir. Çoğu cmdlet için bu durum Force parametresinin kaldırılması ve ShouldProcess isteminin atlanması anlamına gelir ve kullanıcıların ‘-Confirm:$false’ parametresini PowerShell betiklerine eklemesi gerekir.** Bu değişiklikler aşağıdaki sorunları ele alır:
  - –WhatIf işlevselliğinin doğru uygulanarak kullanıcının gerçek anlamda bir değişiklik yapmadan cmdlet veya betiğin etkisini belirlemesine olanak tanıması
  - Olası bir değişikliğin (Cmdlet’teki ConfirmImpact ayarıyla bildirilir) etkisine göre kullanıcının uyarılabilmesi için oturum genelinde bir $ConfirmPreference kullanılarak istem üzerinde denetim
  - –Confirm parametresi kullanılarak onay istemleri üzerinde cmdlet’e özel denetim
  - Değişikliklerin özel niteliği nedeniyle kullanıcıdan istem gereken eylemler (örneğin, gizli dosyaların silinmesi) için ShouldContinue ve –Force parametresinin cmdlet’lerde tutarlı kullanımı
  - Diğer cmdlet’lerden alınan PowerShell betik bilgisinin Azure PowerShell cmdlet’lerine hemen uygulanabilmesi için diğer PowerShell cmdlet’leriyle tutarlılık.

**Şu anda *Tüm Durumlarda tüm İstemleri otomatik atlamak* için Azure PowerShell cmdlet’lerinin kullanıcı tarafından iki parametre girilmesini gerektirdiğini unutmayın:**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Azure İşlem
  - Set-AzureRmVMADDomainExtension
  - Get-AzureRmVMADDomainExtension
  - Restart-AzureVM için -Redeploy parametresi
  - Move-AzureService, Move-AzureStorageAccount ve Move-AzureVirtualNetwork için -Validate parametresi
  - Uzantı cmdlet’leri için ad ve sürüm parametreleri daha önce olduğu gibi isteğe bağlıdır.
  - New-AzureVM, VM nesnesinden bir lisans türü alabilir.
* Azure Storage
  - Tags Parametresini Tag olarak değiştirin ve Tags parametre diğer adını ekleyin
    + New-AzureRmStorageAccount
    + Set-AzureRmStorageAccount
* Azure Ağı
  - Sanal Ağ Eşlemesi için yeni cmdlet eklendi
* Azure Redis Cache
  - Reset-AzureRmRedisCache için yeni cmdlet eklendi
  - Export-AzureRmRedisCache için yeni cmdlet eklendi
  - Import-AzureRmRedisCache için yeni cmdlet eklendi
  - New-AzureRmRedisCache cmdlet’i sanal ağ parametre değişikliğini içerecek şekilde değiştirildi
* Azure SQL DB Yedekleme/Geri Yükleme
  - LTR (Uzun Süreli Saklama) yedekleme özelliği cmdlet’leri
  - Get-AzureRmSqlServerBackupLongTermRetentionVault
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Set-AzureRmSqlServerBackupLongTermRetentionVault
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Restore-AzureRmSqlDatabase artık silinmiş veritabanının bir zaman noktasına geri yüklenmesini desteklemektedir
  - Restore-AzureRmSqlDatabase artık Uzun Süreli Saklama yedeklemesinden geri yüklemeyi desteklemektedir
* Azure LogicApp
  - LogicApp Tümleştirme hesapları cmdlet’leri eklendi.
  - Get-AzureRmIntegrationAccountAgreement
  - Get-AzureRmIntegrationAccountCallbackUrl
  - Get-AzureRmIntegrationAccountCertificate
  - Get-AzureRmIntegrationAccount
  - Get-AzureRmIntegrationAccountMap
  - Get-AzureRmIntegrationAccountPartner
  - Get-AzureRmIntegrationAccountSchema
  - New-AzureRmIntegrationAccountAgreement
  - New-AzureRmIntegrationAccountCertificate
  - New-AzureRmIntegrationAccount
  - New-AzureRmIntegrationAccountMap
  - New-AzureRmIntegrationAccountPartner
  - New-AzureRmIntegrationAccountSchema
  - Remove-AzureRmIntegrationAccountAgreement
  - Remove-AzureRmIntegrationAccountCertificate
  - Remove-AzureRmIntegrationAccount
  - Remove-AzureRmIntegrationAccountMap
  - Remove-AzureRmIntegrationAccountPartner
  - Remove-AzureRmIntegrationAccountSchema
  - Set-AzureRmIntegrationAccountAgreement
  - Set-AzureRmIntegrationAccountCertificate
  - Set-AzureRmIntegrationAccount
  - Set-AzureRmIntegrationAccountMap
  - Set-AzureRmIntegrationAccountPartner
  - Set-AzureRmIntegrationAccountSchema
* Azure Data Lake Store
  - Dosya ve klasörleri karşıya yükleme ve indirme performansı önemli ölçüde artırıldı.
  - Buna indirme parametresi adlarında küçük bir değişiklik ve karşıya yükleme için iki yeni parametrenin eklenmesi dahildir:
    + NumThreads -> PerFileThreadCount, tek bir dosyada kullanılacak iş parçacığı sayısını belirtmek için kullanılır
    + ConcurrentFileCount, klasörü karşıya yükleme/indirme işlemine paralel olarak karşıya yüklenecek/indirilecek dosya sayısını belirtmek için kullanılır.
  - Varsayılan iş parçacığı değerleri artık çoğu dosya boyutu için tamamen daha iyi bir aktarım hızı sağlamak için tasarlanmıştır. Performans istenen düzeyde değilse, yukarıdaki değerler gereksinimleri karşılayacak şekilde değiştirilebilir.
* Azure Data Lake Analytics
  - Get-AzureRMDataLakeAnalyticsDataSource artık bir bağımsız değişken olmadan çağrıldığında tüm veri kaynaklarını döndürmektedir.
  - Bu değişiklik, cmdlet’in veri kaynağı türü parametresini de kaldırır.
  - Bu değişiklik aşağıdaki özelliklerle liste işlemi için yeni bir nesnenin döndürülmesi ile sonuçlanır:
    + Tür, veri kaynağının türü
    + Ad, veri kaynağının adı
    + IsDefault, hesabın varsayılan veri kaynağı ise true olarak ayarlanır
  - submittedBefore ve submittedAfter ile filtrelenirken bazı tarih saat uzaklık değerleri için Get-AzureRMDataLakeAnalyticsJob düzeltildi.
* Web Apps
  - Düzenli takas ve önizleme ile tasar için Swap-AzureRmWebAppSlot cmdlet’i eklendi
  - Set-AzureRmWebAppSlot cmdlet’i otomatik takası destekleyecek şekilde genişletildi
* Azure API Management
  - AzureChinaCloud için Azure Api Management Dağıtımı cmdlet’leri düzeltildi.
  - Git Erişimi Varsayılan olarak etkin olduğundan Set-AzureRmApiManagementTenantGitAccess cmdlet’i kaldırıldı.
* Azure Kurtarma Hizmetleri Yedeklemesi
  - Azure SQL iş yükü için destek eklendi
  - Şifrelenmiş Azure VM’lerini yedeklemek ve geri yüklemek için destek eklendi
  - Backup-AzureRmRecoveryServicesBackupItem - Kurtarma noktaları için isteğe bağlı saklama süresi özelliği eklendi
  - Get-AzureRmRecoveryServicesBackupContainer ve Get-AzureRmRecoveryServicesBackupItem cmdlet’lerinde filtreyle ilgili küçük hata düzeltmeleri
* Azure Otomasyonu
  - Get-AzureRmAutomationHybridWorkerGroup eklendi
