---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105474"
---
# Rename-AzureRemoteAppTemplateImage

## SYNOPSIS
Azure RemoteApp şablonu resmini yeniden adlandırır.

## INDEKI

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Rename-Azureremoteapptemplateımage** cmdlet 'ı Azure RemoteApp şablonu resmini yeniden adlandırır.

## ÖRNEKLERDEN

### Örnek 1: bir şablon resmini yeniden adlandırma
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

Bu komut, ContosoApps adındaki Azure RemoteApp şablonu resminin ContosoFinanceApps.

## PARAMETRELERINE

### -GörüntüAdı
Yeniden adlandırılacak bir Azure RemoteApp şablonu görüntüsünün adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NewName
Azure RemoteApp şablonu görüntüsü için yeni bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
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

[Get-Azureremoteapptemplateımage](./Get-AzureRemoteAppTemplateImage.md)

[Yeni-Azureremoteapptemplateımage](./New-AzureRemoteAppTemplateImage.md)

[Remove-Azureremoteapptemplateımage](./Remove-AzureRemoteAppTemplateImage.md)


