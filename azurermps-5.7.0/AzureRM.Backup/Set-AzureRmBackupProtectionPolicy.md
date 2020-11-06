---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592943"
---
# Set-AzureRmBackupProtectionPolicy

## SYNOPSIS
Var olan koruma ilkesini değiştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### NoScheduleParamSet (varsayılan)
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Set-AzureRmBackupProtectionPolicy** cmdlet 'ı Azure Backup 'ta var olan koruma ilkesini değiştirir.
Aşağıdaki koruma ilkesi bileşenlerini değiştirebilirsiniz: 

- Adlandır
- Yedekleme zamanlaması
- Bekletme ilkeleri

Herhangi bir değişiklik, ilkeyle ilişkili öğelerin yedekleme ve tutma etkilerini etkileyebilir.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -BackupTime
İlkenin yeni yedekleme saatini, bir **Tarih saat** nesnesi olarak ilke için belirtir.
**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.
**TarihSaat** nesneleri hakkında bilgi için, yazın `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Günlük
Yedekleme işleminin günlük zamanlamada çalışacağını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Daysofya
Haftanın bir günü dizisini belirtir.
Bu ilke, yedekleri bu parametre tarafından belirtilen günlerde çalıştırır.
Bu parametre için kabul edilebilir değerler şunlardır:

- Den 
- Salı 
- Günü 
- Per 
- Cuma 
- Günü 
- Gününü

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
İlkenin yeni adını belirtir.
Bu ad kasada benzersiz olmalıdır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionPolicy
Bu cmdlet 'in değiştirdiği koruma ilkesini belirtir.
**Azurermbackupprotectionpolicy** nesnesi almak için Get-AzureRmBackupProtectionPolicy cmdlet 'ini kullanın.

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Yedekleme ilkesi için bir bekletme ilkeleri dizisi belirtir.
**AzureRmBackupRetentionPolicy** nesnelerini edinmek için New-AzureRmBackupRetentionPolicyObject cmdlet 'ini kullanın.

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Haftalık
Yedekleme işleminin haftalık zamanlamada çalışacağını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### AzureRmBackupProtectionPolicy

## ÇıKıŞLAR

### Yabilirsiniz

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


