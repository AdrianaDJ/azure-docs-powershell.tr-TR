---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572014"
---
# New-AzureStorageQueue

## SYNOPSIS
Depolama kuyruğu oluşturur.

## INDEKI

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Tanım
**New-AzureStorageQueue** cmdlet 'i Azure 'da bir depolama sırası oluşturur.

## ÖRNEKLERDEN

### Örnek 1: Azure depolama sırası oluşturma
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

Bu örnek, queueabc adlı bir depolama sırası oluşturur.

### Örnek 2: birden çok Azure depolama kuyruğu oluşturma
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

Bu örnek, birden çok depolama sırası oluşturur.
.NET String sınıfının bölme yöntemini kullanır ve sonra da ardışık düzene geçirir.

## PARAMETRELERINE

### -Context
Azure depolama bağlamını belirtir.
Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.

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
Sıra için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

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

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


