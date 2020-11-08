---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280073"
---
# Get-AzMigrateJob

## SYNOPSIS
Bir Azure geçiş işinin durumunu alır.

## INDEKI

### ListByName (varsayılan)
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Liste
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Tanım
Get-AzMigrateJob cmdlet 'i, bir Azure geçiş işinin durumunu alır.

## ÖRNEKLERDEN

### Örnek 1: Iş kimliğine göre alma
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Bu, bir işi kimliğiyle alır.

### Örnek 2: kaynak grubuna ve projeye göre liste
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Bu, projedeki tüm işleri alır.

### Örnek 3: kaynak grubuna, projeye ve iş adına göre alma
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Bu belirli bir iş alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filtre
OData filtre seçenekleri.

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Çoğaltma sunucusunun iş nesnesini belirtir.
Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Ayrıntıların alınması gereken iş kimliğini belirtir.

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
İş tanımlayıcısı

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectID
Sunucularda çoğaltma yapan Azure geçiş projesini belirtir.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectName
Proje geçirme adı.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcegroupıd
Geçerli abonelikteki Azure geçiş projesi kaynak grubunu belirtir.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kurtarma Hizmetleri kasasındaki kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Azure abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıjob

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <IJob> : Çoğaltma sunucusunun iş nesnesini belirtir.
  - `[Location <String>]`: Kaynak konumu
  - `[ActivityId <String>]`: Etkinlik kimliği.
  - `[AllowedAction <String[]>]`: İşe Izin verilen eylem.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Kaynak sunucu, kaynak bulut, hedef sunucu, hedef bulut gibi etkilenen nesne özellikleri iş akışı nesnesi ayrıntılarına göre.
    - `[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.
  - `[EndTime <DateTime?>]`: Bitiş saati.
  - `[Error <IJobErrorDetails[]>]`: Hatalar.
    - `[CreationTime <DateTime?>]`: İş hatasının oluşturulma zamanı.
    - `[ErrorLevel <String>]`: Hata düzeyi hata.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: Hata kodu.
    - `[ProviderErrorDetailErrorId <String>]`: Sağlayıcı hata kimliği.
    - `[ProviderErrorDetailErrorMessage <String>]`: Hata iletisi.
    - `[ProviderErrorDetailPossibleCaus <String>]`: Hatanın olası nedenleri.
    - `[ProviderErrorDetailRecommendedAction <String>]`: Hatayı çözmek için önerilen eylem.
    - `[ServiceErrorDetailActivityId <String>]`: Etkinlik kimliği.
    - `[ServiceErrorDetailCode <String>]`: Hata kodu.
    - `[ServiceErrorDetailMessage <String>]`: Hata iletisi.
    - `[ServiceErrorDetailPossibleCaus <String>]`: Hatanın olası nedenleri.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Hatayı çözmek için önerilen eylem.
    - `[TaskId <String>]`: Görevin kimliği.
  - `[FriendlyName <String>]`: DisplayName.
  - `[ScenarioName <String>]`: ScenarioName.
  - `[StartTime <DateTime?>]`: Başlangıç saati.
  - `[State <String>]`: Işin durumu. Bu değerlerden biri-NotStarted, InProgress, başarılı, başarısız, Iptal edildi, askıya alınmış veya diğer değerlerinden biridir.
  - `[StateDescription <String>]`: Işin durumunun açıklaması. Örneğin, tamamlandı durumu için, açıklama tamamlanabilir, PartiallySucceeded, Completedwithınformation veya atlandı.
  - `[TargetInstanceType <String>]`: {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType} sınıfının etkilenen nesnesinin türü.
  - `[TargetObjectId <String>]`: Etkilenen nesne kimliği.
  - `[TargetObjectName <String>]`: Etkilenen nesnenin adı.
  - `[Task <IAsrTask[]>]`: Görevler.
    - `[AllowedAction <String[]>]`: Bu görevde uygulanabilir durum/eylemler.
    - `[CustomDetailInstanceType <String>]`: Görev ayrıntılarının türü.
    - `[EndTime <DateTime?>]`: Bitiş saati.
    - `[Error <IJobErrorDetails[]>]`: Görev hata ayrıntıları.
    - `[FriendlyName <String>]`: Ad.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Alt görevler.
    - `[GroupTaskCustomDetailInstanceType <String>]`: Görev ayrıntılarının türü.
    - `[Name <String>]`: Benzersiz görev adı.
    - `[StartTime <DateTime?>]`: Başlangıç saati.
    - `[State <String>]`: Eyalet. Bu değerlerden biri-NotStarted, InProgress, başarılı, başarısız, Iptal edildi, askıya alınmış veya diğer değerlerinden biridir.
    - `[StateDescription <String>]`: Görev durumunun açıklaması. Örneğin, başarılı durum Için, açıklama tamamlanabilir, PartiallySucceeded, Completedwithınformation veya atlandı.
    - `[TaskId <String>]`: Kimlik.
    - `[TaskType <String>]`: Görevin türü. CustomDetails özelliğindeki Ayrıntılar bu türe bağlıdır.

## ILGILI BAĞLANTıLAR

