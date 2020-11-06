---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 14f42ae951fe25f7594eb6e314ac65bb678e29c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587362"
---
# New-AzureStorageTable

## SYNOPSIS
Depolama tablosu oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
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
Yeni tablo için bir ad belirtir.

```yaml
Type: System.String
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

### System. String

### Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageTable

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorageTable](./Get-AzureStorageTable.md)

[Remove-AzureStorageTable](./Remove-AzureStorageTable.md)


