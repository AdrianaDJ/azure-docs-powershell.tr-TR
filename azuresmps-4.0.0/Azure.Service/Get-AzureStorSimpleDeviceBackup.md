---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106290"
---
# Get-AzureStorSimpleDeviceBackup

## SYNOPSIS
Bir cihazdan yedekleri alır.

## INDEKI

### Boş (varsayılan)
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyıd
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyobject
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorSimpleDeviceBackup** cmdlet 'i bir cihazdan yedekleri alır.
Yedekler için yedekleme ilkesi, hacim ve oluşturulma zamanını belirtebilirsiniz.

Bu cmdlet ilk sayfada maksimum 100 yedeği döndürebilir.
100 yedekleri varsa, *ilk* ve *Atla* parametrelerini kullanarak sonraki sayfaları alın.
*İlk* olarak *Atla* ve 50 için 100 değerini belirtirseniz, bu cmdlet ilk 100 sonucunu döndürmez.
Bu, atlan100 dıktan sonraki 50 sonuçlarının sonraki sonucunu verir.

## ÖRNEKLERDEN

### Örnek 1: aygıttaki tüm yedekleri alma
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

Bu komut, Contoso63-AppVm adlı cihazda bulunan tüm yedekleri alır.
İlk sayfa için izin verilen maksimum 100 yedeğinden daha fazlası varsa, *ilkini* kullanarak ek sonuçları görüntüleyin. *Skip*

### Örnek 2: iki tarih arasındaki yedekleri alma
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

Bu komut, 10/7/2014 tarihinde veya bu tarihten sonra veya 10/8/2014 tarihinde oluşturulan Contoso63-AppVm adlı cihazda yedeklemeler alır.
Bu cmdlet ilk sonucu atlar ve ilk iki sonucun ilk sonucunu döndürür.
*İlk* için değerleri değiştirin ve diğer sonuçları görüntülemek için *atlayın* .

### Örnek 3: yedekleme ilkesi KIMLIĞI için yedeklemeler alma
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

Bu komut, oluşturma Contoso63-AppVm belirtilen tarihte veya daha önce oluşturulan cihazda yedekleri alır.
Komut, belirtilen KIMLIĞE sahip yedekleme ilkesi kullanılarak oluşturulmuş yedekleri alır.
Bu komut *ilk* parametreyi belirtir, dolayısıyla yalnızca ilk 10 sonucu verir.

### Örnek 4: yedekleme ilkesi nesnesini yedekleme
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

Bu komut **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanarak bir **backuppolicydetails** nesnesi alır ve bu nesneyi ardışık düzen işlecini kullanarak geçerli cmdlet 'e iletir.
Bu cmdlet, komutun ilk bölümündeki yedekleme ilkesi kullanılarak oluşturulan Contoso63-AppVm adlı cihaz için yedeklemeler alır.
Komut, önceki örnekte olduğu gibi, belirtilen tarihte veya belirtilen tarihte oluşturulmuş yedekleri alır.
Bu komut yalnızca ilk 10 sonucu döndürür.

### Örnek 5: birim KIMLIĞI için yedekleme edinme
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

Bu komut, belirtilen örnek KIMLIĞINE sahip olan birimde oluşturulan cihazda bir yedekleme alır.
Bu komut *Birinci* parametreyi belirtir, dolayısıyla yalnızca ilk sonucu verir.

### Örnek 6: birim adı için yedekleme edinme
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

Bu komut, **Get-AzureStorSimpleDeviceVolume** cmdlet 'ini kullanarak bir **VirtualDisk** nesnesi alır ve bu nesneyi ardışık düzen işlecini kullanarak geçerli cmdlet 'e iletir.
Bu cmdlet, komutun ilk bölümünden birimde oluşturulan Contoso63-AppVm adlı cihaz için yedeklemeler alır.
Bu komut yalnızca ilk sonucu döndürür.

## PARAMETRELERINE

### -Yedeklemekuralı
**Backuppolicydetails** nesnesini belirtir.
Bu cmdlet, hangi yedeklemelerin alınacağını belirlemek için bu nesnenin **InstanceId** 'yi kullanır.
**Backuppolicydetails** nesnesini edinmek için **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanın.

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Backuppolicyıd
Yedekleme ilkesinin örnek KIMLIĞINI belirtir.
Bu cmdlet, bu parametrenin belirttiği ilkeye ait cihaz yedeklemelerini alır.

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

### -Aygıtadı
Yedeklemelerin alınacağı StorSimple aygıtının adını belirtir.

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
Bu cmdlet 'in aldığı yedeklemelerin başlangıç tarihini ve saatini belirtir.

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

### -To
Bu cmdlet 'in aldığı yedeklemelerin bitiş tarihini ve saatini belirtir.

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

### -Hacim
**VirtualDisk** nesnesini belirtir.
Bu cmdlet, yedeklemelerin olduğu birimi belirlemek için bu nesnenin **InstanceId** 'si kullanır.
**VirtualDisk** nesnesi edinmek için **Get-AzureStorSimpleDeviceVolume** parametresini kullanın.

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VolumeId
Yedeklemelerin olduğu birimin örnek KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: IdentifyById2
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

### BackupPolicyDetails, VirtualDisk
Bu cmdlet **Backuppolicydetails** ve **VirtualDisk** nesnelerini kabul eder.

## ÇıKıŞLAR

### 'Te\<Backup\>
Bu cmdlet, **yedekleme** nesnelerinin listesini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureStorSimpleDeviceBackup](./Remove-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)


