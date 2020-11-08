---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274260"
---
# New-AzRecoveryServicesBackupProtectionPolicy

## SYNOPSIS
Yedek koruma ilkesi oluşturur.

## INDEKI

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzRecoveryServicesBackupProtectionPolicy** cmdlet 'Inde bir yedek koruma ilkesi oluşturur.
Koruma ilkesi en az bir bekletme ilkesiyle ilişkilendirilmiştir.
Bekletme ilkesi, bir kurtarma noktasının Azure Backup ile ne kadar tutulacağını tanımlar.
Varsayılan bekletme ilkesini almak için Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanabilirsiniz.
Ayrıca, varsayılan zamanlama ilkesini almak için Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet 'ini kullanabilirsiniz.
**Schedulepolicy** ve **RetentionPolicy** nesneleri, **Yeni-AzRecoveryServicesBackupProtectionPolicy** cmdlet 'ine giriş olarak kullanılır.
Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: yedekleme koruma ilkesi oluşturma
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

İlk komut bir temel **Schedulepolicyobject** alır ve $SchPol değişkeninde depolar.
İkinci komut $SchPol zamanlama ilkesindeki tüm zamanlanmış çalışma zamanlarını kaldırır.
Üçüncü komut, geçerli tarih ve saati almak için Get-Date cmdlet 'ini kullanır.
Dördüncü komut, zamanlama ilkesine zamanlanan çalışma süresi olarak $Dt geçerli tarihi ve saati ekler.
Beşinci komut bir temel **RetentionPolicy** nesnesi alır ve $RetPol değişkeninde depolar.
Altıncı komut, bekletme süresi ilkesini 365 gün olarak ayarlar.
Son komutu, önceki komutlar tarafından oluşturulan zamanlama ve bekletme ilkelerine dayalı bir **Backupprotectionpolicy** nesnesi oluşturur.

### Örnek 2

Yedek koruma ilkesi oluşturur. oluşturulmuş

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## PARAMETRELERINE

### -BackupManagementType
Korunan kaynakların sınıfı. Bu parametre için kabul edilebilir değerler şunlardır:
- AzureVM 
- AzureStorage
- AzureWorkload

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
İlkenin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionPolicy
Temel **RetentionPolicy** nesnesini belirtir.
**RetentionPolicy** nesnesi almak için Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet 'ini kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SchedulePolicy
Temel **Schedulepolicy** nesnesini belirtir.
**Schedulepolicy** nesnesini almak için Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet 'ini kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultId
Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkloadType
Kaynağın iş yükü türü. Bu parametre için kabul edilebilir değerler şunlardır:
- AzureVM 
- AzureFiles
- KLASÖRÜNÜN

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. WorkloadType

### System. Nullable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. Yedeklememanagementtype, Microsoft. Azure. PowerShell. cmdlet. RecoveryServices. Backup. model, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. RetentionPolicyBase

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. SchedulePolicyBase

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Enable-AzRecoveryServicesBackupProtection](./Enable-AzRecoveryServicesBackupProtection.md)

[Get-AzRecoveryServicesBackupProtectionPolicy](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[Get-AzRecoveryServicesBackupRetentionPolicyObject](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[Get-AzRecoveryServicesBackupSchedulePolicyObject](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[Remove-AzRecoveryServicesBackupProtectionPolicy](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


