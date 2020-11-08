---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105693"
---
# Disable-AzureTrafficManagerProfile

## SYNOPSIS
Traffic Manager profilini devre dışı bırakır.

## INDEKI

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Disable-AzureTrafficManagerProfile** cmdlet 'ı bir Microsoft Azure Traffic Manager profilini devre dışı bırakır.
İşlemin başarılı olup olmadığını görüntülemek için *geçiş parametresini kullanabilirsiniz* .

## ÖRNEKLERDEN

### Örnek 1: Traffic Manager profilini devre dışı bırakma ve sonuçları görüntüleme
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Bu komut Myprofıle adlı Traffic Manager profilini devre dışı bırakır.
Komut, komutun başarılı olup olmadığını göstermek için *geçiş parametresini belirtir* .

### Örnek 2: Traffic Manager profilini devre dışı bırakma ve sonuç görüntüleme
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

Bu komut Myprofıle adlı Traffic Manager profilini devre dışı bırakır ancak komutun başarılı olup olmadığını görüntülemez.

## PARAMETRELERINE

### -Ad
Devre dışı bırakmak için Traffic Manager profili adını belirtir.

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
İşlem başarılıysa ve *geçiş parametresini belirtirseniz, bu* cmdlet bir $true değeri döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


