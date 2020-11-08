---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105524"
---
# New-AzureStorSimpleDeviceBackupScheduleUpdateConfig

## SYNOPSIS
Yedekleme zamanlama güncelleştirmesi yapılandırma nesnesi oluşturur.

## INDEKI

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet 'ı bir **Backupscheduleupdaterequest** yapılandırma nesnesi oluşturur.
**Set-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanarak yedekleme ilkesini güncelleştirmek için bu yapılandırma nesnesini kullanın.

## ÖRNEKLERDEN

### Örnek 1: zamanlama güncelleştirme isteği oluşturma
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

Bu komut zamanlama için belirtilen KIMLIĞE sahip bir yedekleme zamanlama güncelleştirme isteği oluşturur.
İstek, zamanlamayı her saat yinelenirse bir bulut anlık görüntü yedeklemesi yapmak.
Yedeklemeler 50 gündür.
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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Güncelleştirilecek yedekleme zamanlamasının örnek KIMLIĞINI belirtir.

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

### Yedeklemescheduleupdaterequest
Bu cmdlet, güncelleştirilmiş yedekleme zamanlamaları hakkında bilgi içeren bir **Backupscheduleupdaterequest** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)


