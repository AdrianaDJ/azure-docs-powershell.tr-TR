---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273799"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
Depolama hesabını geri yüklemek için blob Aralık nesnesi oluşturur.

## INDEKI

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-AzStorageBlobRangeToRestore** cmdlet 'i restore-AzStorageBlobRange 'de kullanılabilen bir blob Aralık nesnesi oluşturur.

## ÖRNEKLERDEN

### Örnek 1: geri yüklenecek blob aralığı oluşturur
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Bu komut geri yüklemek için container1/blob1 (Include) ve Container2/blob2 (exclude) ile biten bir blob aralığı oluşturur.

### Örnek 2: ilk Blobun ilk blob 'dan belirli bir blob 'a geri yüklenecek bir blob aralığı oluşturur (Dışla)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Bu komut, alfabetik sıranın ilk blosonra belirli bir blob container2/blob2 (hariç tut) geri yüklenecek bir blob aralığı oluşturur

### Örnek 3: belirli bir Blobun (Include) en son blob 'u alfabetik sırada geri yüklenecek bir blob aralığı oluşturur
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Bu komut, belirli bir blob container1/blob1 (include) en son blob 'a alfabetik sırada geri yüklenecek bir blob aralığı oluşturur.

### Örnek 4: tüm blob 'ları geri yüklenecek blob aralığı oluşturur
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Bu komut, tüm blob 'ları geri yüklenecek blob aralığı oluşturur.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRange
Blob geri yükleme bitiş aralığını belirtin.
Son Aralık geri yükleme bloblarını dışarıda bırakılacak.
Sonuna geri dönmek için boş bir stri olarak ayarlayın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartRange
Blob geri yükleme başlangıç aralığını belirtin.
Başlangıç aralığı geri yükleme bloblarını içerir.
Başlangıçtan geri yüklemek için boş dize olarak ayarlayın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Management. Storage. model. PSBlobRestoreRange

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
