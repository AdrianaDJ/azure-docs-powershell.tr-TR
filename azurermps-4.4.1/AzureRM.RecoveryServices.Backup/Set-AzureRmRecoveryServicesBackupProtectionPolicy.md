---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f17ce0a23c2b91cd00f2a12bb2451c4e235169ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594198"
---
# Set-AzureRmRecoveryServicesBackupProtectionPolicy

## SYNOPSIS
Yedekleme koruma ilkesini değiştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-AzureRmBackupProtectionPolicy** cmdlet 'i mevcut bir Azure yedekleme koruması ilkesini değiştirir.
Yedekleme zamanlaması ve bekletme ilkesi bileşenlerini değiştirebilirsiniz.

Yaptığınız tüm değişiklikler, ilkeyle ilişkili öğeleri yedeklemeyi ve bekletmesini etkiler.

Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: yedekleme koruma ilkesini değiştirme
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

İlk komut bir temel SchedulePolicy nesnesi alır ve $SchPol değişkeninde depolar.

İkinci komut $SchPol zamanlama ilkesindeki tüm zamanlanmış çalışma zamanlarını kaldırır.

Üçüncü komut, Get-Date cmdlet 'ini kullanarak geçerli tarih ve saati alır ve $DT değişkeninde depolar.

Dördüncü komut $DT tarih ve saati zamanlama ilkesinin çalışma zamanına göre ekler.

Beşinci komut bir temel bekletme ilkesi nesnesi alır ve $RetPol değişkeninde depolar.

Altıncı komut, bekletme süresini 365 güne ayarlar.

Yedinci komutu NewPolicy adındaki yedekleme koruma ilkesini alır ve $Pol değişkeninde depolar.

Son komutu, $SchPol zamanlama ilkesini ve $RetPol bekletme ilkesini kullanarak $Pol yedekleme koruma ilkesini değiştirir.

## PARAMETRELERINE

### -İlke
Bu cmdlet 'in değiştirdiği yedekleme koruması ilkesini belirtir.
**Backupprotectionpolicy** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Temel bekletme ilkesini belirtir.
**RetentionPolicy** nesnesi almak için Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchedulePolicy
Temel zamanlama İlkesi nesnesini belirtir.
**Schedulepolicy** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupSchedulePolicyObject nesnesini kullanın.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### PolicyBase
Parametre ' Ilke ', ardışık düzenin ' PolicyBase ' türünün değerini kabul eder

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. JobBase]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Get-AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[New-AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


