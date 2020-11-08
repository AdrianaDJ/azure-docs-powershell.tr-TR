---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105558"
---
# Get-AzureStorSimpleJob

## SYNOPSIS
StorSimple işlerini alır.

## INDEKI

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureStorSimpleJob** cmdlet 'ı Azure StorSimple işlerini alır.
Belirli bir iş almak için bir örnek KIMLIĞI belirtin.
Bu cmdlet 'in aldığı işleri sınırlandırmak için diğer parametreleri belirtin.

Bu cmdlet en çok 200 işi döndürür.
200 'den fazla işi varsa, *ilk* ve *Atla* parametrelerini kullanarak kalan işleri alın.
*İlk* olarak *Atla* ve 50 için 100 değerini belirtirseniz, bu cmdlet ilk 100 sonucunu döndürmez.
Bu, atlan100 dıktan sonraki 50 sonuçlarının sonraki sonucunu verir.

## ÖRNEKLERDEN

### Örnek 1: KIMLIK kullanarak iş alma
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

Bu komut, belirtilen KIMLIĞE sahip olan iş için bilgi alır.

### Örnek 2: bir cihaz adı kullanarak işleri alma
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

Bu komut, 8600-Bravo 001 adlı aygıttaki işlerle ilgili bilgileri alır.
Komut, aygıtın ilk iki işini alır.

### Örnek 3: tamamlanan işleri alma
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

Bu komut tamamlanmış işleri alır.
Komut ilk on işi atladıktan sonra yalnızca ilk iki işi alır.

### Örnek 4: elle yedekleme işleri edinme
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

Bu komut, el ile yedekleme türündeki işleri alır.

### Örnek 5: belirtilen saatler arasındaki işleri alma
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

İlk iki komut Get-Date cmdlet 'ini kullanarak **DateTime** nesneleri oluşturur.
Komutlar $StartTime ve $EndTime değişkenlerinde yeni zamanları depolar.
Daha fazla bilgi için yazın `Get-Help Get-Date` .

Son komutu, $StartTime ve $EndTime depolanan saatler arasında bulunan Device07 adlı cihaz için işler alır.

## PARAMETRELERINE

### -Aygıtadı
StorSimple aygıtının adını belirtir.

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

### -Önce
Yalnızca belirtilen sayıda nesneyi alır.
Alınacak nesne sayısını girin.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### 'Den
Bu cmdlet 'in aldığı işlerin başlangıç tarihini ve saatini belirtir.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Alınacak işin KIMLIĞINI belirtir.

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

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### -Atla
Belirtilen sayıda nesneyi yoksayar ve kalan nesneleri alır.
Atlanacak nesne sayısını girin.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Durum
Durumu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Çalışması
- Tamamladığı
- İptal
- Erişilemedi
- İşleminin
- Completederrors

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

### -To
Bu cmdlet 'in aldığı işlerin bitiş tarihini ve saatini belirtir.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tür
İş türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Yedeğinin
- ManualBackup
- Kurtarma
- CloneWorkflow
- DeviceRestore
- Güncelleştiremedi
- Destek paketi
- Virtualappliancesağlamasını

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
Bu cmdlet 'e giriş kanalı oluşturamazsınız.

## ÇıKıŞLAR

### IList \<DeviceJobDetails\> , devicejobdetails
Bu cmdlet iş ayrıntıları nesnelerinin listesini döndürür veya *InstanceId* parametresini belirtirseniz, tek bir iş ayrıntı nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Stop-AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)


