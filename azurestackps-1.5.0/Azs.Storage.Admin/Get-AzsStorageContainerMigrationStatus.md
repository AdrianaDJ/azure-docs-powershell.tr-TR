---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0207d9d2353954fc1997f5752ac6dad26dbdfa13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761746"
---
# Get-AzsStorageContainerMigrationStatus

## SYNOPSIS
Kapsayıcı geçiş işinin durumunu döndürür.

## INDEKI

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## Tanım
Kapsayıcı geçiş işinin durumunu döndürür.

## ÖRNEKLERDEN

### --------------------------ÖRNEK 1--------------------------
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

Kapsayıcı geçiş işinin durumunu edinin.

## PARAMETRELERINE

### -FarmName
Grup kimliği.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
İşlem kimliği.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. AzureStack. Management. Storage. admin. modeller. MigrationResult

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

