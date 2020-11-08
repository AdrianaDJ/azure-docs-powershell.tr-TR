---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106571"
---
# Get-AzureRemoteAppVM

## SYNOPSIS
Bir Azure RemoteApp koleksiyonundaki sanal makineleri alır.

## INDEKI

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureRemoteAppVM** cmdlet 'i oturum barındırma Için bir Azure RemoteApp koleksiyonu altında oluşturulmuş sanal makineleri alır.

## ÖRNEKLERDEN

### Örnek 1: bir koleksiyonda sanal makineleri görüntüleme
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

Bu komut, contoso adlı bir Azure RemoteApp koleksiyonunda oturum barındırma için kullanılan sanal makineleri görüntüler.

## PARAMETRELERINE

### -CollectionName
Azure RemoteApp koleksiyonunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Restart-AzureRemoteAppVM](./Restart-AzureRemoteAppVM.md)


