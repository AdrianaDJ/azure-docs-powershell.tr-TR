---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107352"
---
# Get-WAPackVMOSDisk

## SYNOPSIS
Sanal makinelerin işletim sistemi disk nesnelerini alır.

## INDEKI

### Boş (varsayılan)
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Get-Wapackvmosdısk** cmdlet 'i sanal makinelerin işletim sistemi disk nesnelerini alır.

## ÖRNEKLERDEN

### Örnek 1: bir ad kullanarak işletim sistemi diski edinme
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

Bu komut, ContosoOSDisk adlı bir işletim sistemi diskini alır.

### Örnek 2: bir KIMLIK kullanarak işletim sistemi diski edinme
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

Bu komut, belirtilen KIMLIĞE sahip işletim sistemi diskini alır.

### Örnek 3: tüm işletim sistemi disklerini alma
```
PS C:\> Get-WAPackVMOSDisk
```

Bu komut, tüm işletim sistemi disklerini alır.

## PARAMETRELERINE

### -ID
İşletim sistemi diskinin benzersiz KIMLIĞINI belirtir.

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
İşletim sistemi diskinin adını belirtir.

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


