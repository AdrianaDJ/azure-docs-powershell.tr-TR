---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106329"
---
# Get-AzureRemoteAppCollection

## SYNOPSIS
Azure RemoteApp koleksiyonu hakkında bilgi alır.

## INDEKI

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureRemoteAppCollection** cmdlet 'ı, Microsoft Azure 'Daki Azure RemoteApp koleksiyonlarıyla ilgili bilgileri getirir.
Belirli bir koleksiyonda bilgi içeren bir nesne veya geçerli abonelikteki tüm koleksiyonlar için hiçbir koleksiyon belirtilmemişse bir nesne döndürür.

## ÖRNEKLERDEN

### Örnek 1: tüm koleksiyonların listesini alma
```
PS C:\> Get-AzureRemoteAppCollection
```

Bu komut, abonelikteki tüm Azure RemoteApp koleksiyonlarının bir listesini döndürür.

### Örnek 2: belirtilen koleksiyon hakkında bilgi alma
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

Bu komut, ContosoApps adlı Azure RemoteApp koleksiyonu hakkındaki bilgileri döndürür.

### Örnek 3: joker karakter kullanarak koleksiyonların listesini alma
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

Bu komut, finans * ile eşleşen tüm Azure RemoteApp koleksiyonlarının bir listesini döndürür.

## PARAMETRELERINE

### -CollectionName
Azure RemoteApp koleksiyonunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
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

[New-AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


