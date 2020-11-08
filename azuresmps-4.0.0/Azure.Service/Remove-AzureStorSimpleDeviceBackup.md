---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106467"
---
# Remove-AzureStorSimpleDeviceBackup

## SYNOPSIS
Yedekleme nesnesini siler.

## INDEKI

### Identifybyıd (varsayılan)
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyobject
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Remove-AzureStorSimpleDeviceBackup** cmdlet 'i tek bir yedekleme nesnesini siler.
Zaten silinmiş olan bir yedeği silmeye çalışırsanız, bu cmdlet hata döndürür.

## ÖRNEKLERDEN

### Örnek 1: bir cihazın yedeklemesini kaldırma
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

Bu komut, Contoso63-AppVm adlı cihaz için belirtilen KIMLIĞE sahip olan yedeği kaldırır.
Komut, **yedekleme** nesnesini kaldıran işlemi başlatır ve ardından bir **taskresponse** nesnesi döndürür.
Görevin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.

### Örnek 2: bir aygıtın KIMLIĞINI kullanarak ilk yedeklemeyi kaldırma
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

İlk komut Contoso63-AppVm adlı cihaz için yedekleri alır ve $Backup değişkeninde depolar.

İkinci komut, Contoso63-AppVm adlı cihazdan bir yedeği siler.
Komut, $Backup dizisinin ilk öğesinin **InstanceId** özelliğine başvuruda bulunmak için standart nokta gösterimini kullanır.
Bu komut, *waitforcomplete* parametresini belirtir ve bu nedenle, komut işlem tamamlanana kadar bekler ve ardından **taskstatusınfo** nesnesini döndürür.

### Örnek 3: ardışık düzeni kullanarak bir cihazın ilk yedeklemesini kaldırma
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

İlk komut Contoso63-AppVm adlı cihaz için yedekleri alır ve $Backup değişkeninde depolar.

İkinci komut $Backup dizisinde depolanan ilk nesneyi geçerli cmdlet 'e geçirir.
Bu cmdlet, Contoso63-AppVm adlı cihazdan bu yedeği siler.
Bu komut, *waitforcomplete* parametresini belirtir ve bu nedenle, komut işlem tamamlanana kadar bekler ve ardından **taskstatusınfo** nesnesini döndürür.

## PARAMETRELERINE

### -Yedekleme
Silinecek **yedekleme** nesnesini belirtir.
**Yedekleme** nesnesi edinmek için **Get-AzureStorSimpleDeviceBackup** cmdlet 'ini kullanın.

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupID
Silinecek yedeğin örnek KIMLIĞINI belirtir.

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
Yedeklemenin silineceği StorSimple aygıtının adını belirtir.

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

### Yedeğinin

## ÇıKıŞLAR

### Taskstatusınfo, TaskResponse
Bu cmdlet, bu parametreyi belirtmezseniz, *Waitforcomplete* parametresini belirtirseniz **, bir** **taskresponse** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)


