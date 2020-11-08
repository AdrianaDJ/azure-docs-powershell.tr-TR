---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 047C5FBD-CB0D-47BF-AE03-4DF32B4FAD87
online version: ''
schema: 2.0.0
ms.openlocfilehash: a546c9fdb066aaf1203055fd62d8eb01258569c8
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107356"
---
# Get-WAPackVM

## SYNOPSIS
Sanal makine nesnelerini alır.

## INDEKI

### Boş (varsayılan)
```
Get-WAPackVM [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVM [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVM [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Get-WAPackVM** cmdlet 'i sanal makine nesnelerini alır.

## ÖRNEKLERDEN

### Örnek 1: ad kullanarak sanal makine alma
```
PS C:\> Get-WAPackVM -Name "ContosoV126"
```

Bu komut, ContosoV126 adındaki sanal makineyi alır.

### Örnek 2: KIMLIK kullanarak sanal makine edinme
```
PS C:\> Get-WAPackVM -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

Bu komut belirtilen KIMLIĞE sahip sanal makineyi alır.

### Örnek 3: tüm sanal makineleri edinme
```
PS C:\> Get-WAPackVM
```

Bu komut tüm sanal makineleri alır.

## PARAMETRELERINE

### -ID
Sanal makinenin benzersiz KIMLIĞINI belirtir.

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
Sanal makinenin adını belirtir.

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

[Yeni-WAPackVM](./New-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Restart-WAPackVM](./Restart-WAPackVM.md)

[Özgeçmiş-WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Başlangıç-WAPackVM](./Start-WAPackVM.md)

[Dur-WAPackVM](./Stop-WAPackVM.md)

[Askıya al-WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


