---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106375"
---
# Enable-AzureTrafficManagerProfile

## SYNOPSIS
Traffic Manager profili etkinleştirilir.

## INDEKI

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Enable-AzureTrafficManagerProfile** cmdlet 'ı bir Microsoft Azure Traffic Manager profili sağlar.
İşlemin başarılı olup olmadığını göstermek için *geçiş parametresini belirtin* .

## ÖRNEKLERDEN

### Örnek 1: Traffic Manager profilini etkinleştirme
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

Bu komut Myprofıle adlı Traffic Manager profilini etkinleştirmiştir.

### Örnek 2: Traffic Manager profilini etkinleştirme ve sonuçları görüntüleme
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Bu komut Myprofıle adlı Traffic Manager profilini ve komutun başarılı olup olmadığını görüntüler.

## PARAMETRELERINE

### -Ad
Etkinleştirilecek Traffic Manager profilinin adını belirtir.

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

### -Geçiş
İşlem başarılı olursa $True döndürür; Aksi takdirde $False.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

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
Bu cmdlet 'in okuduğu Azure profilini belirtir. Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### System. Boolean
Bu cmdlet $True veya $False oluşturur.
İşlem başarılı olursa ve *geçiş parametresini belirtirseniz, bu* cmdlet bir $true değeri döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


