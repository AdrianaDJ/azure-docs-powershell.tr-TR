---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935138"
---
# Test-AzsNameAvailability

## SYNOPSIS
Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir

## INDEKI

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## Tanım
Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

Belirtilen abonelikler kaynak türünün ve adının kullanılabilirlik düzeyini verir

## PARAMETRELERINE

### -Ad
Doğrulanacak kaynak adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Doğrulanacak kaynak türü.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. AzureStack. Management. abonelikler. admin. modeller. Checknamekullanılabilirliği Bilityresponse

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

