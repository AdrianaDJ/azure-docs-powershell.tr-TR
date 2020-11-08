---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106696"
---
# Get-AzsComputeQuota

## SYNOPSIS
İşlem nesnelerinin kota sınırlarını belirten kotalar döndürür.

## INDEKI

### Liste (varsayılan)
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### Al
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## Tanım
Var olan kotaların listesini alma.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
Get-AzsComputeQuota -Location 'local'
```

Tüm işlem kotalarını belirtilen konumda edinin.

### --------------------------ÖRNEK 2--------------------------
```
Get-AzsComputeQuota 'Default Quota'
```

Belirli bir işlem kotası edinin.

## PARAMETRELERINE

### -Konum
{{Dolgu konumu açıklaması}}

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Kotanın adı.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### ComputeQuotaObject

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

