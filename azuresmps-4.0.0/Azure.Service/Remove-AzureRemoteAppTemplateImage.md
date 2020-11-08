---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106149"
---
# Remove-AzureRemoteAppTemplateImage

## SYNOPSIS
Azure RemoteApp şablonu resmini siler.

## INDEKI

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Remove-Azureremoteapptemplateımage** cmdlet 'ı bir Azure RemoteApp şablonu resmini siler.
Bir şablon görüntüsü yalnızca herhangi bir Azure RemoteApp koleksiyonuna bağlı değilse silinebilir.

## ÖRNEKLERDEN

### Örnek 1: şablon görüntüsü silme
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

Bu komut, ContosoApps adlı şablon resmini siler.

## PARAMETRELERINE

### -GörüntüAdı
RemoteApp şablonu görüntüsünün adını belirtir.

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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

[Rename-Azureremoteapptemplateımage](./Rename-AzureRemoteAppTemplateImage.md)


