---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107391"
---
# Get-WAPackVMTemplate

## SYNOPSIS
Sanal makine şablonlarını alır.

## INDEKI

### Boş (varsayılan)
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Get-WAPackVMTemplate** cmdlet 'i sanal makine şablonlarını alır.

## ÖRNEKLERDEN

### Örnek 1: ad kullanarak sanal makine şablonu alma
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

Bu komut, ContosoTemplate04 adlı sanal makine şablonunu alır.

### Örnek 2: KIMLIK kullanarak sanal makine şablonu alma
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

Bu komut belirtilen KIMLIĞE sahip sanal makine şablonunu alır.

### Örnek 3: tüm sanal makine şablonlarını edinin
```
PS C:\> Get-WAPackVMTemplate
```

Bu komut, tüm sanal makine şablonlarını alır.

## PARAMETRELERINE

### -ID
Şablonun benzersiz KIMLIĞINI belirtir.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Şablonun adını belirtir.

```yaml
Type: String
Parameter Sets: FromName
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

[Get-WAPackVM](./Get-WAPackVM.md)


