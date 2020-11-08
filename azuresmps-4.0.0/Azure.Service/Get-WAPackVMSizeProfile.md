---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107430"
---
# Get-WAPackVMSizeProfile

## SYNOPSIS
Boyut profili nesnelerini alır.

## INDEKI

### Boş (varsayılan)
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Get-WAPackVMSizeProfile** cmdlet 'i sanal makinelerin boyut profili nesnelerini alır.

## ÖRNEKLERDEN

### Örnek 1: ad kullanarak boyut profili alma
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

Bu komut, ContosoSizeProfile07 adlı boyut profilini alır.

### Örnek 2: bir KIMLIK kullanarak boyut profili alma
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

Bu komut belirtilen KIMLIĞE sahip olan boyut profilini alır.

### Örnek 3: tüm boyut profillerini alma
```
PS C:\> Get-WAPackVMSizeProfile
```

Bu komut, tüm boyut profillerini alır.

## PARAMETRELERINE

### -ID
Boyut profilinin benzersiz KIMLIĞINI belirtir.

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
Boyut profilinin adını belirtir.

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


