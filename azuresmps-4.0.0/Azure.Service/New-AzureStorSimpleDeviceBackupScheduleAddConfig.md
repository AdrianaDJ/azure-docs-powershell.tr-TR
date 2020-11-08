---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105528"
---
# New-AzureStorSimpleDeviceBackupScheduleAddConfig

## SYNOPSIS
Yedekleme zamanlama yapılandırması nesnesi oluşturur.

## INDEKI

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet 'ı bir **backupschedulebase** yapılandırma nesnesi oluşturur.
**New-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanarak yeni yedekleme ilkesi oluşturmak için bu yapılandırma nesnesini kullanın.

## ÖRNEKLERDEN

### Örnek 1: yedek yapılandırma nesnesi oluşturma
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

Bu komut, bulut anlık görüntü yedekleri için yedekleme zamanlama taban nesnesi oluşturur.
Yedekleme her gün gerçekleşir ve yedeklemeler 100 gündür tutulur.
Bu zamanlama, geçerli saat olan varsayılan saatten etkinleştirilir.

## PARAMETRELERINE

### -BackupType
Yedekleme türünü belirtir.
Geçerli değerler: LocalSnapshot ve CloudSnapshot.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Özellikli
Yedekleme zamanlamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bir Azure profili belirtir.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurrenceType
Bu yedekleme zamanlaması için yinelenme türünü belirtir.
Geçerli değerler: 

- Dakika
- Dayanarak
- Mü
- Haftalık

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurrenceValue
Yedeklemenin ne sıklıkta yapılacağını belirtir.
Bu parametre, *RecurrenceType* parametresiyle belirtilen birimi kullanır.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionCount
Yedeklemenin tutulacağı gün sayısını belirtir.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Startfromdatetıme
Yedeklemelerin başlayacağı tarihi belirtir.
Varsayılan değer geçerli süredir.

```yaml
Type: String
Parameter Sets: (All)
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

### Yedeklemeschedulebase
Bu cmdlet bir **Backupschedulebase** nesnesi döndürür.
Yeni yedekleme ilkesi oluşturmak için **Backupschedulebase** kullanın.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorSimpleDeviceBackupScheduleUpdateConfig](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[New-AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)


