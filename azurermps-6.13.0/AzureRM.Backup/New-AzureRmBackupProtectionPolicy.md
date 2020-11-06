---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: ce4550d4b0b0206db3a28f11a58ac4384ecbac60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587303"
---
# New-AzureRmBackupProtectionPolicy

## SYNOPSIS
Yedekleme ilkesi oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### NoScheduleParamSet (varsayılan)
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DailyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyScheduleParamSet
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzureRmBackupProtectionPolicy** cmdlet 'ı Azure PowerShell nesnesi olarak bir Azure yedekleme ilkesi oluşturur.
Yedekleme ilkesi, yedeklemenin ne zaman ve ne sıklıkta yedekleme
Enable-AzureRmBackupProtection cmdlet 'i yedekleme İlkesi kullanır.

## ÖRNEKLERDEN

### Örnek 1: günlük ve aylık bekletme ile günlük yedekleme ilkesi oluşturma
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.
İkinci komut 30 günlük bekletmenin bir bekletme ilkesi oluşturur ve ardından $Daily değişkeninde depolar.
Üçüncü komut, on iki ay boyunca her ayın onuncu günü ve her ayın yirminleri boyunca yedeklemeyi tutan bekletme ilkesi oluşturur.
Komut, bekletme ilkesini $Monthly değişkeninde depolar.
Son komutu, $Vault 'de kasa için günlük yedekleme süresi 3:00 PM olan bir yedekleme ilkesi oluşturur.
Komut, $Daily ve $Monthly depolanan bekletme ilkelerini atar.
Komut sonucu $ProtectionPolicy değişkeninde depolar.

## PARAMETRELERINE

### -BackupTime
Yedekleme işlemi için günün saatini bir **TarihSaat** nesnesi olarak belirtir.
**TarihSaat** almak için Get-Date cmdlet 'ini kullanın.
**TarihSaat** nesneleri hakkında bilgi için, yazın `Get-Help Get-Date` .

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Günlük
Yedekleme işleminin günlük zamanlamada çalışacağını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 3
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
- Pazar *haftalık* parametresini belirtirseniz, bu parametreyi belirtin.

```yaml
Type: System.String[]
Parameter Sets: NoScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Ad
Yedekleme ilkesinin adını belirtir.
Kasada benzersiz bir ad seçin.

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
Yedekleme ilkesi için bir bekletme ilkeleri dizisi belirtir.
**AzureRmBackupRetentionPolicy** edinmek için New-AzureRmBackupRetentionPolicyObject cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tür
İlkenin uygulandığı yedekleme öğesinin türünü belirtir.
Şu anda desteklenen tek değer AzureVM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kasa
Yedekleme ilkesinin ait olduğu Azure Yedekleme Kasası 'nı belirtir.
**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Haftalık
Yedekleme ilkesinin haftanın bir veya birden çok günü haftalık olarak tetiklenmesini gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. DateTime

### System. String []

### Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupRetentionPolicy []

### Microsoft. Azure. Commands. AzureBackup. modeller. Azurermbackupkasası
Parametreler: kasa (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupProtectionPolicy

## NOTLARıNDA
* Yabilirsiniz

## ILGILI BAĞLANTıLAR

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[New-AzureRmBackupRetentionPolicyObject](./New-AzureRmBackupRetentionPolicyObject.md)

[Remove-AzureRmBackupProtectionPolicy](./Remove-AzureRmBackupProtectionPolicy.md)

[Set-AzureRmBackupProtectionPolicy](./Set-AzureRmBackupProtectionPolicy.md)


