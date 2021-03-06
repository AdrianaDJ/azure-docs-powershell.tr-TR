---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572370"
---
# Get-AzureStorageQueue

## SYNOPSIS
Depolama sıralarını listeler.

## INDEKI

### SıraAdı (varsayılan)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorageQueue** cmdlet 'ı bir Azure depolama hesabıyla ilişkilendirilmiş depolama sıralarını listeler.

## ÖRNEKLERDEN

### Örnek 1: tüm Azure depolama sıralarını listeler
```
PS C:\>Get-AzureStorageQueue
```

Bu komut, geçerli depolama hesabının tüm depolama sıralarının listesini alır.

### Örnek 2: joker karakter kullanarak Azure depolama sıralarını listeleme
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

Bu komut, adı sırayla başlayan depolama sıralarının listesini almak için joker karakter kullanır.

### Örnek 3: sıra adı önekini kullanarak Azure depolama sıralarını listeleme
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

Bu örnekte, adı sırayla başlayan depolama sıralarının listesini almak için *önek* parametresi kullanılır.

## PARAMETRELERINE

### -Context
Azure depolama bağlamını belirtir.
Bunu **New-AzureStorageContext** cmdlet 'i kullanarak oluşturabilirsiniz.

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
Bir ad belirtir.
Ad belirtilmezse cmdlet, tüm sıraların listesini alır.
Tam veya kısmi ad belirtilirse cmdlet, Ad düzeniyle eşleşen tüm sıraları alır.

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Önek
Almak istediğiniz sıraların adında kullanılan bir önek belirtir.

```yaml
Type: String
Parameter Sets: QueuePrefix
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

[Yeni-AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


