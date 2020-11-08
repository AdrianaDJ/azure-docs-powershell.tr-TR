---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106335"
---
# Get-AzureMediaServicesAccount

## SYNOPSIS
Kullanılabilir Azure Media Services hesaplarını alır.

**Not:** Bu sürüm kullanımdan kalktı, lütfen [daha yeni sürüme](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)bakın.

## INDEKI

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

Tüm hesapları listelemek için `Get-AzureMediaServicesAccount` cmdlet 'i kullanın.
Belirli bir hesap hakkında daha ayrıntılı bilgi edinmek için `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet 'i kullanın.

## ÖRNEKLERDEN

### Örnek 1: tüm medya hizmetleri hesaplarını listeler
```
PS C:\> Get-AzureMediaServicesAccount
```

Bu komut, kullanılabilir tüm medya hizmetleri hesaplarını listeler.

### Örnek 2: Medya Hizmetleri hesabı hakkında ayrıntılı bilgi alma
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

Bu komut, bir medya Hizmetleri hesabının özelliklerini görüntüler.

## PARAMETRELERINE

### -Ad
Medya Hizmetleri hesap adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

[Medya Hizmetleri için Azure PowerShell kullanma](https://go.microsoft.com/fwlink/?LinkId=324179)


