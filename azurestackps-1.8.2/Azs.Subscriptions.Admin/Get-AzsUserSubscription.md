---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106985"
---
# Get-AzsUserSubscription

## SYNOPSIS
Kullanıcı abonelikleri listesini yönetici olarak alın.

## INDEKI

### Liste (varsayılan)
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### Al
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## Tanım
Kullanıcı abonelikleri listesini yönetici olarak alın.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
Get-AzsUserSubscription
```

Kullanıcı abonelikleri listesini yönetici olarak alın.

## PARAMETRELERINE

### -Filtre
OData filtre parametresi.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Abonelik kimliği parametresi.

```yaml
Type: Guid
Parameter Sets: Get
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

### Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

