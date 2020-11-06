---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93571033"
---
# Save-AzureRmContext

## SYNOPSIS
Geçerli kimlik doğrulama bilgilerini diğer PowerShell oturumlarında kullanılmak üzere kaydeder.

## INDEKI

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## Tanım
Save-AzureRmContext cmdlet 'i diğer PowerShell oturumlarında kullanılacak geçerli kimlik doğrulama bilgilerini kaydeder.

## ÖRNEKLERDEN

### Örnek 1: geçerli oturumun içeriği kaydediliyor
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

Bu örnek, geçerli oturumun Azure bağlamını sağlanan JSON dosyasına kaydeder.

### Örnek 2: verilen bağlamı kaydetme
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

Bu örnek, sağlanan JSON dosyasına cmdlet 'e geçirilen Azure bağlamını kaydeder.

## PARAMETRELERINE

### -Force
Varsa, verilen dosyanın üzerine yaz

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yol
Kimlik doğrulama bilgilerinin kaydedileceği dosyanın yolunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure bağlamını belirtir.
Bağlam belirtmezseniz, bu cmdlet yerel varsayılan içerikten okur.

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRMProfile

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Profile. modeller. PSAzureProfile

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

