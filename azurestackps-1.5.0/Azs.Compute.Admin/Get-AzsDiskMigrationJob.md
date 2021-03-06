---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571738"
---
# Get-AzsDiskMigrationJob

## SYNOPSIS
Yönetilen disk geçiş işlerinin listesini döndürür.

## INDEKI

### Liste (varsayılan)
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### Al
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## Tanım
Disk geçiş işlerinin listesini döndürür.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

Belirli bir yönetilen disk geçiş işi edinin.

### --------------------------ÖRNEK 2--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local
```

Yerel konumda yönetilen disk geçiş işlerinin listesini döndürür.

## PARAMETRELERINE

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

### -Ad
Geçiş işi GUID adı.

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

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
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Durum
Disk geçiş işinin parametreleri.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. AzureStack. Management. COMPUTE. admin. modeller. DiskMigrationJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

