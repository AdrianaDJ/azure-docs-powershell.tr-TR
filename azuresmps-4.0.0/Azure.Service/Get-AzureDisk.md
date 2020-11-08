---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106354"
---
# Get-AzureDisk

## SYNOPSIS
Azure disk deposundaki diskler hakkında bilgi alır.

## INDEKI

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Get-AzureDisk** cmdlet 'i, geçerli abonelik için Azure disk deposunda depolanan diskler hakkında bilgi alır.
Bu cmdlet, depodaki tüm diskler için bir bilgi listesi döndürür.
Belirli bir diskle ilgili bilgileri görüntülemek için diskin adını belirtin.

## ÖRNEKLERDEN

### Örnek 1: diskle ilgili bilgileri alma
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

Bu komut, disk deposundaki ContosoDataDisk adlı diskle ilgili bilgi verilerini alır.

### Örnek 2: tüm disklerle ilgili bilgileri alma
```
PS C:\> Get-AzureDisk
```

Bu komut, disk deposundaki tüm diskler hakkında bilgi alır.

### Örnek 3: diskle ilgili bilgileri alma
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

Bu komut, şu anda sanal makineye eklenmemiş olan disk deposundaki tüm disklere yönelik verileri alır.
Komut tüm diskler hakkında bilgi alır ve her nesneyi **WHERE-nesne** cmdlet 'ine geçirir.
Bu cmdlet, **AttachedTo** özelliği için $null değeri olmayan tüm diskleri bırakır.
Komut, **Biçim-Tablo** cmdlet 'ini kullanarak listeyi tablo olarak biçimlendirir.

## PARAMETRELERINE

### -DiskName
Bu cmdlet 'in bilgi aldığı disk deposundaki diskin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureDisk](./Add-AzureDisk.md)

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Güncelleştirme-AzureDisk](./Update-AzureDisk.md)


