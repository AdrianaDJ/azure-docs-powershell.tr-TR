---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107090"
---
# Get-AzsDelegatedProvider

## SYNOPSIS
Temsilci sağlayıcıların listesini alın.

## INDEKI

### Liste (varsayılan)
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### Al
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## Tanım
Temsilci sağlayıcıların listesini alın.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
Get-AzsDelegatedProvider
```

Temsilci sağlayıcıların bir listesini alın.

### --------------------------ÖRNEK 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

Belirli bir temsilci sağlayıcı edinin.

## PARAMETRELERINE

### -Delegatevseçproviderıd
{{Fill Delegateıd açıklama}}

```yaml
Type: Guid
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

### Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

