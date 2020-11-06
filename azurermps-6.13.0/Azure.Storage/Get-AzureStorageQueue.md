---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: 077d8139817c3998e27300d8c86c809b4da9e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589631"
---
# Get-AzureStorageQueue

## SYNOPSIS
Depolama sıralarını listeler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SıraAdı (varsayılan)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bir ad belirtir.
Ad belirtilmezse cmdlet, tüm sıraların listesini alır.
Tam veya kısmi ad belirtilirse cmdlet, Ad düzeniyle eşleşen tüm sıraları alır.

```yaml
Type: System.String
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
Type: System.String
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureStorageQueue](./New-AzureStorageQueue.md)

[Remove-AzureStorageQueue](./Remove-AzureStorageQueue.md)


