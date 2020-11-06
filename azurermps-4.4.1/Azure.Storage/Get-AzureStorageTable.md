---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587069"
---
# Get-AzureStorageTable

## SYNOPSIS
Depolama tablolarını listeler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

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
Accept wildcard characters: True
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

### Istoragecontext

' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder

### Dizisi

' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageTable

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorageTable](./New-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


