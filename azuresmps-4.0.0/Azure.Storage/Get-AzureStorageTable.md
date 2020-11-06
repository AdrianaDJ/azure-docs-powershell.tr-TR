---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572342"
---
# Get-AzureStorageTable

## SYNOPSIS
Depolama tablolarını listeler.

## INDEKI

### TableName (varsayılan)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş depolama tablolarını listeler.

## ÖRNEKLERDEN

### Örnek 1: tüm Azure depolama tablolarını listeler
```
PS C:\>Get-AzureStorageTable
```

Bu komut, depolama hesabının tüm depolama tablolarını alır.

### Örnek 2: joker karakter kullanarak Azure depolama tablolarını listeleme
```
PS C:\>Get-AzureStorageTable -Name table*
```

Bu komut, adı tabloyla başlayan depolama tablolarını almak için joker karakter kullanır.

### Örnek 3: tablo adı önekini kullanarak Azure depolama tablolarını listeleme
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

Bu komut, adı tabloyla başlayan depolama tablolarını almak için *önek* parametresini kullanır.

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
Tablo adını belirtir.
Tablo adı boşsa, cmdlet tüm tabloları listeler.
Aksi takdirde, belirtilen ad veya normal Ad düzeniyle eşleşen tüm tablolar listelenir.

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Önek
Almak istediğiniz tablo veya tabloların adında kullanılan bir önek belirtir.
Tablo gibi aynı dizeyle başlayan tüm tabloları bulmak için bunu kullanabilirsiniz.

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
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

[New-AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


