---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106273"
---
# Get-AzureWebsiteJob

## SYNOPSIS
Web sitesiyle ilişkilendirilmiş Web işlerini alır.

## INDEKI

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Web sitesiyle ilişkilendirilmiş Web işlerini alır.

## ÖRNEKLERDEN

### Örnek 1: belirli Web işi bilgilerini alma
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

MyWebsite üretim yuvasından MyWebJob adlı bir Web işini alır.

### Örnek 2: Web sitesi için tüm Web işlerini alma
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

MyWebsite üretim yuvalı tüm Web işlerini alır.

### Örnek 3: tüm tetiklenen web işlerini alın
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

MyWebsite 'in aşamalandırma yuvasından tüm tetiklenen web işlerini alır.

## PARAMETRELERINE

### -JobName
Web işi adı

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

### -JobType
Web işi türü.
Bu parametre için kabul edilebilir değerler şunlardır:

- Tetiklenen
- Eğri

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

### -Ad
Azure Web sitesinin adı.

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
Azure Web sitesinin yuva adı.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureWebsite](./Get-AzureWebsite.md)

[New-AzureWebsiteJob](./New-AzureWebsiteJob.md)

[Remove-AzureWebsiteJob](./Remove-AzureWebsiteJob.md)

[Start-AzureWebsiteJob](./Start-AzureWebsiteJob.md)

[Stop-AzureWebsiteJob](./Stop-AzureWebsiteJob.md)


