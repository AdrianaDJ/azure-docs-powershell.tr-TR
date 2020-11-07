---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: fcf5bec22dffc18d6c4f9950d8dfb3e5b37332a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764528"
---
# Get-AzureRmRecoveryServicesBackupSchedulePolicyObject

## SYNOPSIS
Temel bir zamanlama İlkesi nesnesi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet 'ini bir temel **Azurermrecoveryservicesschedulepolicyobject** alır.
Bu nesne sistemde kalıcı değil.
Bu, yeni yedekleme koruma ilkesi oluşturmak için New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'i işleyebileceğiniz ve kullanabileceğiniz geçici bir nesnedir.

## ÖRNEKLERDEN

### Örnek 1: zamanlama frekansını haftalık olarak ayarlama
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

İlk komut bekletme ilkesi nesnesini alır ve $RetPol değişkeninde depolar.

İkinci komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.

Üçüncü komut zamanlama İlkesi sıklığını haftalık olarak değiştirir.

Son komut, güncelleştirilmiş zamanlamaya sahip yedek koruma ilkesi oluşturur.

### Örnek 2: yedekleme süresini ayarlama
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

İlk komut zamanlama İlkesi nesnesini alır ve $SchPol değişkeninde depolar.

İkinci komut $SchPol tüm zamanlanmış çalışma zamanlarını kaldırır.

Üçüncü komut geçerli tarih ve saati alır ve $DT değişkeninde depolar.

Dördüncü komut zamanlanmış çalışma saatlerini geçerli saat ile değiştirir.
Günde yalnızca bir kez AzureVM, yedekleme süresini sıfırlamak için özgün zamanlamayı değiştirmeniz gerekir.

Son komut yeni zamanlamayı kullanarak yedek koruma ilkesi oluşturur.

## PARAMETRELERINE

### -BackupManagementType
Yedekleme yönetim türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- AzureVM 
- Azuressqldatabase

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkloadType
İş yükü türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- AzureVM 
- Azuressqldatabase

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. SchedulePolicyBase

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Set-AzureRmRecoveryServicesBackupProtectionPolicy](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


