---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106210"
---
# New-AzureStorSimpleAccessControlRecord

## SYNOPSIS
Bir erişim denetimi kaydı oluşturur.

## INDEKI

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**New-AzureStorSimpleAccessControlRecord** cmdlet 'i bir erişim denetimi kaydı oluşturur.
Birimleri yapılandırmak için bir **Accesscontrolrecord** nesnesi kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: bir erişim Controlaccess denetim kaydı oluşturma ve resultaccess denetimini bekleme
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

Bu komut, Iqn10 adındaki Iscsı başlatıcısı için Acr10 adında bir erişim denetimi kaydı oluşturur.
Bu komut, *waitforcomplete* parametresini belirtir ve bu nedenle, komut işlem tamamlanana kadar bekler ve ardından **taskstatusınfo** nesnesini döndürür.

### Örnek 2: bir erişim denetimi oluşturma
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

Bu komut, Iqn11 adındaki Iscsı başlatıcısı için Acr11 adında bir erişim denetimi kaydı oluşturur.
Bu komut *Waitforcomplete* parametresini belirtmez ve bu nedenle komut görevi başlatır ve ardından bir **taskresponse** nesnesi döndürür.
Görevin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.

## PARAMETRELERINE

### -ACRName
Erişim denetimi kaydı için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Iqninitiatorname
Bu cmdlet 'in birime erişim sağladığı Iscsı başlatıcısının tam adını (ıQN) belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

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

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


