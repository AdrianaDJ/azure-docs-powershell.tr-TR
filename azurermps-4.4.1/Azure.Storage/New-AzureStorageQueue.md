---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f6a9aff40d2cff62e683439b3f28f9e782b2de05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595053"
---
# New-AzureStorageQueue

## SYNOPSIS
Depolama kuyruğu oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

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

### Istoragecontext

' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder

### Dizisi

' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


