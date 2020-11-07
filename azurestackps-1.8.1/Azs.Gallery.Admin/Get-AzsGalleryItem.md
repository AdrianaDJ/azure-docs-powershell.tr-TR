---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fa95e34c6a220a496a79f7a72c65c222f1376f1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935161"
---
# Get-AzsGalleryItem

## SYNOPSIS
Galeri öğelerini listeler.

## INDEKI

### Liste (varsayılan)
```
Get-AzsGalleryItem [<CommonParameters>]
```

### Al
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## Tanım
Azure yığını marketi 'nde kullanılabilen Galeri öğelerinin listesini alma

## ÖRNEKLERDEN

### ÖRNEK 1
```
Get-AzsGalleryItem
```

Liste Galerisi öğeleri.

### ÖRNEK 2
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

Bir galeri öğesini ada göre alın.

## PARAMETRELERINE

### -Ad
Galeri öğesinin kimliği.
Publisher adını, öğe adını içerir ve süre karakteriyle ayrı sürüm içerebilir.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. AzureStack. Management. Gallery. admin. modeller. GALLERYITEM

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
