---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9374f8a55beca561afd9ed4bca4320b685349798
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93940263"
---
# Get-AzsAzureBridgeActivation

## SYNOPSIS
Azure Köprüsü etkinleştirme 'yi döndürür.

## INDEKI

### Liste (varsayılan)
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### Al
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### Içermiyor
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## Tanım
Azure yığını kaydedildikten sonra, etkinleştirme nesnesi Azure 'daki kayda bir Azure yığın dağıtımını bağlayan bilgileri (örneğin, kayıt son kullanım tarihi, ad vb.) içerir.

## ÖRNEKLERDEN

### ÖRNEK 1
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

"ActivationRG" kaynak grubunun altındaki Azure Bridge etkinleştirmeleri listesini alma

### ÖRNEK 2
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

' ActivationRG ' altında ' Myacsyon ' adlı bir Azure köprü etkinleştirme

## PARAMETRELERINE

### -Ad
Etkinleştirme adı.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure yığınının kaydı sırasında kullanılan kaynak grubu; Ayrıca, portalda kaynak grubu adlarını da görüntüleyebilirsiniz.

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Kaynak kimliği.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Atla
Parametre değerinde belirtilen ilk N öğeyi atlayın.

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -Üst
Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.
-Skip parametresinden sonra uygulanır.

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. AzureStack. Management. AzureBridge. admin. modeller. ActivationResource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
