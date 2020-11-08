---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106506"
---
# Get-AzureWebsiteLog

## SYNOPSIS
Belirtilen Web sitesi için günlükleri alır.

## INDEKI

### Dolgusunu
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ListPath
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

Belirtilen Web sitesi için günlük alır.

## ÖRNEKLERDEN

### Örnek 1: günlük akışını başlatma
```
PS C:\> Get-AzureWebsiteLog -Tail
```

Bu örnek, tüm uygulama günlükleri için günlük akışını başlatır.

### Örnek 2: http günlükleri için günlük akışını başlatma
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

Bu örnek http günlükleri için günlük akışını başlatır.

### Örnek 3: hata günlükleri için günlük akışını başlatma
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

Bu örnek yalnızca akış akışını ve yalnızca hata günlüklerini göstermeyi başlatır.

### Örnek 4: kullanılabilir günlükleri görüntüleme
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

Bu örnek, Web sitesindeki kullanılabilir tüm günlük yollarını listeler.

## PARAMETRELERINE

### -ListPath
Günlük yollarının listeedilip edilmeyeceğini gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -İleti
Günlük iletisini filtrelemek için kullanılacak bir dize belirtir.
Yalnızca bu dizeyi içeren Günlükler alınır.

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Web sitesinin adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
Günlüğün alınacağı yol.
Varsayılan olarak bu, tüm yolları içermek anlamına gelir.

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Yuvalı
Yuva adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Kuyruklu
Günlüklerin kaydedilip kaydedilmeyeceğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureWebsite](./Get-AzureWebsite.md)

[New-AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)


