---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 987793101e89a7f628f575bf7353994756edaeae
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934922"
---
# Move-AzsSubscription

## SYNOPSIS
Abonelikleri temsilci sağlayıcı teklifleri arasında taşıyın.

## INDEKI

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## Tanım
Abonelikleri temsilci sağlayıcı teklifleri arasında taşıyın.
Bu süreç yalnızca bir yeniden markalama işlemi yapacak, temeldeki teklif, planlar, aboneliklerin kotaları değiştirilmeyecektir.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
Move user subscriptions to a delegated provider offer.
```

Move-AzsSubscription \` -destinationdelegatevseçproviderteklifini "/Subscriptions/45ec4d39-8dea-4D26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/RO1"-RESOURCEID "/Subscriptions/45ec4d39-8dea-4D26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6", "/Subscriptions/45ec4d39-8dea-4D26-a373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4E73-abfc-169512576f7d"

### --------------------------ÖRNEK 2--------------------------
```
Move user subscriptions from a delegated provider to the Default Provider.
```

$resourceIds = Get-AzsUserSubscription-Filter "offerName EQ ' O1 '" | WHERE {$ _. Delegatevseçprovidersubscriptionıd-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select-ExpandProperty ID Move-AzsSubscription-RESOURCEID $resourceIds

## PARAMETRELERINE

### -Iş
Taşıma işleminin iş olarak yürütülüp yürütülmeyeceğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destinationdelegatevseçproviderteklifini
Bu cmdlet 'in abonelikleri taşıdıkları tam nitelikli sağlayıcı teklifini belirtir.
Abonelikler varsayılan sağlayıcıya geri taşındıysa NULL.

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

### -RESOURCEID
Bu cmdlet 'in hareket ettiği tam bir abonelik kaynak tanımlayıcılarının dizisini belirtir.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

