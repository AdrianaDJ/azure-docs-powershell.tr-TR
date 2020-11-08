---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106579"
---
# Get-AzureRemoteAppTemplateImage

## SYNOPSIS
Azure RemoteApp şablonu görüntüleriyle ilgili bilgileri getirir.

## INDEKI

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-Azureremoteapptemplateımage** cmdlet 'ı, Azure RemoteApp şablonu görüntüleriyle Ilgili bilgileri Microsoft Azure 'da alır.
Bu cmdlet, belirli bir şablon görüntüsü hakkında bilgi içeren bir nesne döndürür.
Şablon görüntüsü belirtilmemişse, geçerli abonelikteki tüm şablon resimlerinde yer alan bilgiler görüntülenir.

## ÖRNEKLERDEN

### Örnek 1: tüm şablon görüntülerinin listesini alma
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

Bu komut, tüm şablon görüntülerinin listesini döndürür.

### Örnek 2: belirtilen şablon görüntüsü hakkında bilgi alma
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

Bu komut, ContosoApps adındaki şablon görüntüsü hakkında bilgi alır.

## PARAMETRELERINE

### -GörüntüAdı
Azure RemoteApp şablonu görüntüsünün adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


