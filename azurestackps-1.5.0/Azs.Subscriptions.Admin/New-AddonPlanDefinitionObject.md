---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7074752cda5997bba0536cf891675f59e734e509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572297"
---
# New-AddonPlanDefinitionObject

## SYNOPSIS
Bir teklifin bağlanacağı veya bağlantısının istendiği istenen planın adını içerir.

## INDEKI

```
New-AddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## Tanım
Bir teklifin bağlanacağı veya bağlantısının istendiği istenen planın adını içerir.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
New-AddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

Belirtilen plan için 500 alma sınırı ile yeni bir plan tanımı nesnesi oluşturun.

## PARAMETRELERINE

### -Maxtanışan
Tek bir abonelikle edinildiği en fazla örnek sayısı.
Belirtilmemişse, kabul edilen değer 1 ' dir.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plankimliği
Plan tanımlayıcısı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

