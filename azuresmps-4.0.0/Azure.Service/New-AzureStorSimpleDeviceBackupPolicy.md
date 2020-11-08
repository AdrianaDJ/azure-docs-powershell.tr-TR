---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106208"
---
# New-AzureStorSimpleDeviceBackupPolicy

## SYNOPSIS
Yedekleme ilkesi oluşturur.

## INDEKI

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**New-AzureStorSimpleDeviceBackupPolicy** cmdlet 'i bir yedekleme ilkesi oluşturur.
Yedekleme ilkesi, bir veya daha fazla birimde çalıştırılabilecek bir veya daha fazla yedekleme zamanlaması içerir.
Yedekleme zamanlaması oluşturmak için, **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: yedekleme ilkesi oluşturma
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

İlk komut, **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet 'ini kullanarak bir yedekleme zamanlama yapılandırması nesnesi oluşturur ve bu nesneyi $Schedule 01 değişkeninde depolar.

İkinci komut, **New-AzureStorSimpleDeviceBackupScheduleAddConfig** kullanarak başka bir yedek yapılandırma nesnesi oluşturur ve bu nesneyi $Schedule 02 değişkeninde depolar.

Üçüncü komut, $ScheduleArray adlı boş bir dizi değişkeni oluşturur.
Sonraki iki komut $ScheduleArray için ilk iki komuttan oluşturulan nesneleri ekler.

Altıncı komut, **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'ini kullanarak Contoso63-AppVm adlı aygıtın birim kapsayıcısını alır ve bu kapsayıcı nesnesini $DeviceContainer değişkeninde depolar.

Yedinci komutu, **Get-AzureStorSimpleDeviceVolume** cmdlet 'ini kullanarak $DeviceContainer ilk üyesinde depolanan birim kapsayıcısının birimini alır ve bu birimi $Volume değişkeninde depolar.

Sekizinci komutu, $VolumeArray adlı boş bir dizi değişkeni oluşturur.
Next komutu $VolumeArray için bir birim KIMLIĞI ekler.
Bu değer, yedekleme ilkesinin çalıştığı $Volume depolanan birimi tanımlar.
$VolumeArray ek birim kimlikleri ekleyebilirsiniz.

Son komutu Contoso63-AppVm adlı cihaz için GeneralPolicy07 adlı yedekleme ilkesini oluşturur.
Komut, $ScheduleArray depolanan zamanlama yapılandırması nesnelerini belirtir.
Komut $VolumeArray ilkenin uygulanacağı birim veya birimleri belirtir.
**Get-AzureStorSimpleDeviceBackupPolicy** cmdlet 'ini kullanarak yedekleme ilkesini doğrulayabilirsiniz.

## PARAMETRELERINE

### -BackupPolicyName
Yedekleme ilkesinin adını belirtir.

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

### -BackupSchedulesToAdd
İlkeye eklenecek **Backupschedulebase** nesnelerinin dizisini belirtir.
Her nesne bir zamanlamayı temsil eder.
Yedekleme ilkesi, bir veya daha fazla zamanlama içerir.
**Backupschedulebase** nesnesi edinmek Için, **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet 'ini kullanın.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aygıtadı
Yedekleme ilkesinin oluşturulacağı StorSimple aygıtının adını belirtir.

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

### -Volumeıdstoadd
Yedekleme ilkesine eklenecek birimlerin kimliklerinin dizisini belirtir.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Yedeklemeilkesi
Bu cmdlet, yeni zamanlamaları ve birimleri içeren bir **Backuppolicy** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[New-AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


