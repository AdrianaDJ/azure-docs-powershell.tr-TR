---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 740077def0ba0eccb1d962b88317fadb3c5c897c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587302"
---
# New-AzureRmBackupRetentionPolicyObject

## SYNOPSIS
Yedekleme bekletme ilkesi oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### DailyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WeeklyRetentionParamSet
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MonthlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInDailyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### YearlyRetentionInWeeklyFormatParamSet
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**New-AzureRmBackupRetentionPolicyObject** cmdlet 'ı bir Azure yedekleme bekletme ilkesi oluşturur.
Bekletme ilkesi yedeklemenin bir kurtarma noktası olmasını sağlar.
Bekletme türleri şunlardır: 
- Mü 
- Haftalık 
- Aylık 
- Yılda kullanmayı düşündüğünüz her bir bekletme türü için bir bekletme ilkesi oluşturun.
Yedekleme ilkesi en az bir bekletme ilkesiyle ilişkilendirilmiştir.
Yedekleme ilkesi oluşturmak için New-AzureRmBackupProtectionPolicy cmdlet 'ini kullanın.
Bunun yerine Enable-AzureRmBackupProtection cmdlet 'e bir bekletme ilkesi sağlayabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: günlük tutma için bekletme ilkesi oluşturma
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

İlk komut 30 günlük bekletmenin bir bekletme ilkesi oluşturur ve ardından $Daily değişkeninde depolar.
İkinci komut $Daily içeriğini görüntüler.

### Örnek 2: aylık bir bekletme ilkesi oluşturma
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

İlk komut, on iki ay boyunca her ayın onuncu günü ve her ayın yirminleri boyunca yedeklemeyi tutan bekletme ilkesi oluşturur.
Komut, bekletme ilkesini $Monthly değişkeninde depolar.
İkinci komut $Monthly içeriğini görüntüler.

## PARAMETRELERINE

### -Günlüktutma
Bu cmdlet 'in günlük bekletme ilkesi oluşturduğunu gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Daysofay
Hangi kurtarma noktalarının yedeğine ve ne kadar süreyle saklanacağını tanımlayan ay günlerini belirtir.
Bu parametre için kabul edilebilir değerler: 1 ila 28 ve son tamsayılar.
*Dailyalımı* , *MonthlyRetentionInDailyFormat* ve *YearlyRetentionInDailyFormat* parametrelerini belirtmeniz durumunda bu parametreyi belirtin.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases:
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Daysofya
Haftanın bir günü dizisini belirtir.
Bu cmdlet 'in hangi kurtarma noktalarının saklanacağını ve ne süreyle kaldığını tanımlayan günler.
Bu parametre için kabul edilebilir değerler şunlardır:
- Den 
- Salı 
- Günü 
- Per 
- Cuma 
- Günü 
- Pazar, *Weeklyalıkoyma* , *MonthlyRetentionInWeeklyFormat* ve *YearlyRetentionInWeeklyFormat* parametrelerini belirtirseniz, bu parametreyi belirtin.
Yedekleme ve bekletme için seçtiğiniz hafta günlerinin hizalandığından emin olun.
Örneğin, yedeğiniz Cumartesi günleri ayarlanmışsa, bekletme ilkelerinin da Cumartesi kullanması gerekir.

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -MonthlyRetentionInDailyFormat
Bu cmdlet 'in günlük biçimde bir aylık ilke oluşturduğunu gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthlyRetentionInWeeklyFormat
Bu cmdlet 'in haftalık biçimde bir aylık ilke oluşturduğunu gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonthsOfYear
Hangi ayların yedekleme 'nin yıllık olarak sakladığı kurtarma noktalarına sahip olduğunu belirtir.
Bu parametre için kabul edilebilir değerler: ay, Ocak veya Şubat gibi değerlerdir.

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekletme
Yedekleme bir yedekleme noktasını saklayan saklama süresini gün, ay veya yıl olarak belirtir.
Birim, bu cmdlet 'in günlük, aylık veya yıllık bekletme seçeneğini seçdiğine bağlıdır.
Örneğin, *Dailyalıkoyma* parametresini belirtirseniz cmdlet, geçerli parametreyi gün sayısı olarak yorumlar.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Weeklyalımesi
Bu cmdlet 'in haftalık bekletme ilkesi oluşturduğunu gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Haftanumarası
Hangi kurtarma noktalarının yedeğine ve ne kadar süreyle saklanacağını tanımlayan ayın haftasını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Eklemelisiniz 
- İden 
- Üç 
- Dördüncü 
- Soya

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInDailyFormat
Bu cmdlet 'in günlük biçimde bir yıllık bekletme ilkesi oluşturduğunu gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -YearlyRetentionInWeeklyFormat
Bu cmdlet 'in haftalık biçimde bir yıllık bekletme ilkesi oluşturduğunu gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupRetentionPolicy

## NOTLARıNDA
* Yabilirsiniz

## ILGILI BAĞLANTıLAR

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Yeni-AzureRmBackupProtectionPolicy](./New-AzureRmBackupProtectionPolicy.md)


