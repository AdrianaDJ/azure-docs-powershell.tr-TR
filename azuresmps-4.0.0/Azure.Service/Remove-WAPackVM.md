---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107408"
---
# Remove-WAPackVM

## SYNOPSIS
Sanal makine nesnelerini kaldırır.

## INDEKI

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Remove-WAPackVM** cmdlet 'i sanal makine nesnelerini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: sanal makineyi kaldırma
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

İlk komut ContosoV126 adındaki sanal makineyi **Get-WAPackVM** cmdlet 'ini kullanarak alır ve bu nesneyi $VirtualMachine değişkeninde depolar.

İkinci komut, $VirtualMachine depolanan sanal makineyi kaldırır.
Komut sizden onaylamanızı ister.

### Örnek 2: onaysız sanal makineyi kaldırma
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

İlk komut ContosoV126 adındaki sanal makineyi **Get-WAPackVM** cmdlet 'ini kullanarak alır ve bu nesneyi $VirtualMachine değişkeninde depolar.

İkinci komut, $VirtualMachine depolanan sanal makineyi kaldırır.
Bu komut *Force* parametresini içerir.
Komut sizden onay istemez.

## PARAMETRELERINE

### -Force
Cmdlet 'in bir sanal makineyi onaylamanızı istemeden kaldırmadığını gösterir.

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

### -Geçiş
Cmdlet 'in Boole değeri döndürdüğü anlamına gelir.
İşlem başarılı olursa cmdlet $True değeri döndürür.
Aksi takdirde, bir $False değeri döndürür.
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

[Get-WAPackVM](./Get-WAPackVM.md)

[Yeni-WAPackVM](./New-WAPackVM.md)

[Restart-WAPackVM](./Restart-WAPackVM.md)

[Özgeçmiş-WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[Başlangıç-WAPackVM](./Start-WAPackVM.md)

[Dur-WAPackVM](./Stop-WAPackVM.md)

[Askıya al-WAPackVM](./Suspend-WAPackVM.md)


