---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105748"
---
# Start-AzureStorSimpleBackupCloneJob

## SYNOPSIS
Bir cihazda yedeklemeyi klonuygulayan bir iş başlatır.

## INDEKI

### Boş (varsayılan)
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyname
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyıd
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Start-AzureStorSimpleBackupCloneJob** cmdlet 'ı StorSimple cihazında var olan bir yedeği klonuygulayan bir iş başlatır.

## ÖRNEKLERDEN

### Örnek 1: cihaz adlarını kullanarak yedeği farklı bir birime kopyalama
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

İlk komut **Get-AzureStorSimpleDeviceBackup** cmdlet 'Ini kullanarak ContosoDev07 adlı aygıtın ilk yedeklemesini alır.
Komut bu yedeği $Backup değişkeninde depolar.

İkinci komut **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanarak erişim denetimi kayıtlarını alır.
Komut sonucu $Acrs değişkeninde depolar.

Son komut, bir birimdeki bir birimin belirtilen yedeğini aynı cihazdaki farklı bir birime klonuygulayan bir iş başlatır.
Bu örnek, cihazı adıyla belirtir.
Komut, $Backup ve $Acrs depolanan değerleri kullanır.
Komut işin KIMLIĞINI döndürür.

### Örnek 2: cihaz kimliklerini kullanarak yedeği farklı bir birime kopyalama
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

İlk komut **Get-AzureStorSimpleDeviceBackup** cmdlet 'Ini kullanarak ContosoDev07 adlı aygıtın ilk yedeklemesini alır.
Komut bu yedeği $Backup değişkeninde depolar.

İkinci komut **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanarak erişim denetimi kayıtlarını alır.
Komut sonucu $Acrs değişkeninde depolar.

Son komut, bir birimdeki bir birimin belirtilen yedeğini aynı cihazdaki farklı bir birime klonuygulayan bir iş başlatır.
Bu örnekte cihazı cihaz KIMLIĞIYLE belirtilir.
Komut, $Backup ve $Acrs depolanan değerleri kullanır.
Komut işin KIMLIĞINI döndürür.

### Örnek 3: cihaz adlarını kullanarak yedeği farklı bir cihazda bir birime kopyalama
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

İlk komut **Get-AzureStorSimpleDeviceBackup** cmdlet 'Ini kullanarak ContosoDev07 adlı aygıtın ilk yedeklemesini alır.
Komut bu yedeği $Backup değişkeninde depolar.

İkinci komut **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanarak erişim denetimi kayıtlarını alır.
Komut sonucu $Acrs değişkeninde depolar.

Son komutu, bir birimdeki bir birimin belirtilen yedeğini farklı bir aygıttaki birime klonuygulayan bir iş başlatır.
Bu örnekte, cihazlar ada göre belirtilir.
Komut, $Backup ve $Acrs depolanan değerleri kullanır.
Komut işin KIMLIĞINI döndürür.

### Örnek 4: cihaz adlarını ve ardışık düzen işlecini kullanarak yedeği farklı bir birime kopyalama
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

İlk komut **Get-AzureStorSimpleDeviceBackup** cmdlet 'Ini kullanarak ContosoDev07 adlı aygıtın ilk yedeklemesini alır.
Komut bu yedeği $Backup değişkeninde depolar.

İkinci komut **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanarak erişim denetimi kayıtlarını alır.
Komut sonuçları ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.
Geçerli cmdlet, bir aygıttaki bir birimin belirtilen yedeğini aynı cihazdaki farklı bir birime klonuygulayan bir iş başlatır.
Bu örnek, cihazı adıyla belirtir.
Komutta $Backup depolanan değer kullanılır.
Komut, ardışık düzenin *Targetaccesscontrolrecords* parametresinin değerini alır.
Komut işin KIMLIĞINI döndürür.

## PARAMETRELERINE

### -BackupID
Kopya oluşturulacak yedeğin örnek KIMLIĞINI belirtir.

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

### -CloneVolumeName
Hedef aygıttaki yeni kopyalanmış birimin adını belirtir.

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

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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

### -Anlık görüntü
Bu cmdlet 'in klonkullandığı anlık görüntü nesnesini belirtir.

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Sourcedeviceıd
Kaynak aygıtın örnek KIMLIĞINI belirtir.
Bu cmdlet, kaynak cihazdan geri döner.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sourceaygıtadı
Kaynak aygıtın adını belirtir.
Bu cmdlet, kaynak cihazdan geri döner.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAccessControlRecords
Erişim denetimi kayıtlarını belirtir.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Targetdeviceıd
Hedef aygıtın örnek KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Targetaygıtadı
Bu cmdlet 'in yedeği klondıkları aygıtın adını belirtir.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Anlık görüntü, AccessControlRecord listesi
**Anlık görüntü** nesnelerini veya **accesscontrolrecord** nesnelerinin listesini bu cmdlet 'e boru yapabilirsiniz.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


