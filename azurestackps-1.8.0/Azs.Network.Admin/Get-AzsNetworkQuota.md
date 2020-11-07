---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934797"
---
# Get-AzsNetworkQuota

## SYNOPSIS
Tüm kotaları listeler.

## INDEKI

### Liste (varsayılan)
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### Al
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## Tanım
Tüm kotaları listeler.
Adı veya filtreyi geçirerek listeyi sınırlayın.

## ÖRNEKLERDEN

### ÖRNEK 1
```
Get-AzsNetworkQuota
```

Tüm ağ kotalarını listeler.

### ÖRNEK 2
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

Belirtilen ağ kotasını alır.

## PARAMETRELERINE

### -Ad
Ağ kotası kaynak adı.

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

### -Konum
Kaynağın konumu.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. AzureStack. Management. Network. admin. modeller. Quota

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
