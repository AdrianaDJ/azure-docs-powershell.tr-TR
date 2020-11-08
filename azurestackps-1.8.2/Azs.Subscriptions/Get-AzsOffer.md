---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106761"
---
# Get-AzsOffer

## SYNOPSIS
Genel teklifler listesini edinin.

## INDEKI

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## Tanım
Genel teklifler listesini edinin.

## ÖRNEKLERDEN

### ÖRNEK 1
```
Get-AzsOffer | fl
```

Genel teklifler listesini edinin.

## PARAMETRELERINE

### -Atla
Parametre değerinde belirtilen ilk N öğeyi atlayın.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Üst
Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.
-Skip parametresinden sonra uygulanır.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sağlayıcı
Temsilci sağlayıcı adını belirtmek için isteğe bağlı parametre. Bu parametre kullanılmıyor ve gelecekte kullanım dışı olacak.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. AzureStack. Management. Subscription. modeller.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
