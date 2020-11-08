---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F9C8D0AA-ED97-43E8-ADB1-5AE1A4517666
online version: ''
schema: 2.0.0
ms.openlocfilehash: c524bb90d84df6ad3e37b552b957dac2d75b6a6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105747"
---
# Start-AzureStorSimpleDeviceBackupRestoreJob

## SYNOPSIS
StorSimple cihazında yedeklemeyi geri yükleyen bir iş başlatır.

## INDEKI

### Boş (varsayılan)
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyıd
```
Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName <String> -BackupId <String> -SnapshotId <String>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Start-AzureStorSimpleDeviceBackupRestoreJob** cmdlet 'ı StorSimple cihazında yedeklemeyi geri yükleyen bir iş başlatır.
Yedekleme KIMLIĞI ve isteğe bağlı bir anlık görüntü KIMLIĞI belirtin.

## ÖRNEKLERDEN

### Örnek 1: bir yedeklemeyi geri yüklemek için bir iş başlatın
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -WaitForComplete
Confirm
Are you sure you want to restore the backup with backupId b3b50534-763c-4b05-9724-5ecf62bde721? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y


Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 217d0647-c001-4f43-9833-f8155a458e95
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e0aa2dcd2f197a8588c40a067fe0e519
```

Bu komut, Contoso63-AppVm adlı aygıtta belirtilen KIMLIĞE ve ilişkili anlık görüntülere sahip yedekleme nesnesini geri yükleyen bir iş başlatır.
Komut *Waitforcomplete* parametresini belirtir; böylece, cmdlet konsola denetimi göndermeden önce biter.

### Örnek 2: belirli bir anlık görüntüyü geri yüklemek için bir iş başlatın
```
PS C:\>Start-AzureStorSimpleDeviceBackupRestoreJob -DeviceName "Contoso63-AppVm" -BackupId "b3b50534-763c-4b05-9724-5ecf62bde721" -SnapshotId "2d0cfad7-46bf-4266-8859-96549646e947_0000000000000000" -Force

The start job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 9102ed9a-078f-4648-a
721-3cffbba31336 for tracking the job status
```

Bu komut, belirtilen KIMLIĞE sahip yedek anlık görüntüsünü geri yükleyen bir iş başlatır.
Komut, Contoso63-AppVm adlı cihazda KIMLIĞI belirtilen yedekleme nesnesini belirtir.
Komut *Force* parametresini belirtir, bu nedenle işi onaylamanızı istemeden başlatır.

## PARAMETRELERINE

### -BackupID
Geri yüklenecek yedeğin örnek KIMLIĞINI belirtir.

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

### -Aygıtadı
Yedeklemenin varolduğu StorSimple aygıtının adını belirtir.

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
Bu cmdlet 'in sizden onay istemez olmadığını gösterir.

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

### -Anlık anlık kimliği
Geri yüklenecek anlık görüntünün örnek KIMLIĞINI belirtir.

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

### Taskstatusınfo, TaskResponse
*Waitforcomplete* parametresini belirtirseniz, bu cmdlet bir **taskstatusınfo** nesnesi döndürür.
Bu parametreyi belirtmezseniz, bir **Taskresponse** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)

[Start-AzureStorSimpleDeviceBackupJob](./Start-AzureStorSimpleDeviceBackupJob.md)


