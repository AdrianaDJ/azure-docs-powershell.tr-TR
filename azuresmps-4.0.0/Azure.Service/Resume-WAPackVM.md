---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5E85F58B-7C70-4F4A-B218-08F9AF512B76
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8aba9c72e3911f59db88e9be4262ee90ea460a5c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107395"
---
# Resume-WAPackVM

## SYNOPSIS
Duraklatılan sanal makineleri sürdürür.

## INDEKI

```
Resume-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Özgeçmiş-WAPackVM** cmdlet 'i duraklatılan sanal makineleri sürdürür.

## ÖRNEKLERDEN

### Örnek 1: sanal makineyi sürdürme
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Resume-WAPackVM -VM $VirtualMachine
```

İlk komut ContosoV126 adındaki sanal makineyi **Get-WAPackVM** cmdlet 'ini kullanarak alır ve bu nesneyi $VirtualMachine değişkeninde depolar.

İkinci komut $VirtualMachine depolanan sanal makineyi sürdürür.

## PARAMETRELERINE

### -Geçiş
Çalıştığınız öğeyi temsil eden bir nesne döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -VM
Bir sanal makine belirtir.
Sanal makine edinmek için **Get-WAPackVM** cmdlet 'ini kullanın.

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-WAPackVM](./Get-WAPackVM.md)

[Yeni-WAPackVM](./New-WAPackVM.md)

[Remove-WAPackVM](./Remove-WAPackVM.md)

[Restart-WAPackVM](./Restart-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Başlangıç-WAPackVM](./Start-WAPackVM.md)

[Dur-WAPackVM](./Stop-WAPackVM.md)

[Askıya al-WAPackVM](./Suspend-WAPackVM.md)


