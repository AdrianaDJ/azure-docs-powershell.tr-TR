---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572193"
---
# New-AzureStorageTable

## SYNOPSIS
Depolama tablosu oluşturur.

## INDEKI

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Tanım
**New-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş bir depolama tablosu oluşturur.

## ÖRNEKLERDEN

### Örnek 1: Azure depolama tablosu oluşturma
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

Bu komut, tableabc adında bir depolama tablosu oluşturur.

### Örnek 2: birden çok Azure depolama tablosu oluşturma
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

Bu komut birden çok tablo oluşturur.
.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.

## PARAMETRELERINE

### -Context
Depolama bağlamını belirtir.
Bunu oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Ad
Yeni tablo için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorageTable](./Get-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


