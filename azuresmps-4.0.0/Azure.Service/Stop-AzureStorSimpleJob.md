---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106012"
---
# Stop-AzureStorSimpleJob

## SYNOPSIS
StorSimple işini durdurur.

## INDEKI

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Stop-AzureStorSimpleJob** cmdlet 'i bir açık StorSimple işini durdurur.
Bir örnek KIMLIĞI veya bir iş adı sağlayarak bir iş belirtebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: bir cihazın işlerini durdurma
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

Bu komut, **Get-AzureStorSimpleJob** cmdlet 'Ini kullanarak Device07 adlı aygıtın işlerini alır.
Komut, ardışık düzen işlecini kullanarak işleri geçerli cmdlet 'e geçirir.
Geçerli cmdlet, komutun geçtiği tüm işleri durdurur.
Komut *Force* parametresini belirtir ve bu nedenle işi durdurmadan önce onaylamanız istemez.

### Örnek 2: belirli bir işi durdurma
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

Bu komut, belirtilen örnek KIMLIĞINE sahip olan işi durdurur.

## PARAMETRELERINE

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

### -InstanceId
Durdurulacak cihaz işinin KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### DeviceJobDetails
Bu cmdlet, bu cmdlet 'in durduğu **devicejob** ayrıntılarını alır.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


