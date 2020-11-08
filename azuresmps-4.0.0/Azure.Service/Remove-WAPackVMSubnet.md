---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107407"
---
# Remove-WAPackVMSubnet

## SYNOPSIS
Sanal makine alt ağ nesnelerini kaldırır.

## INDEKI

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Remove-WAPackVMSubnet** cmdlet 'i sanal makine alt ağ nesnelerini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: sanal makine alt ağını kaldırma
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

İlk komut ContosoVMSubnet01 adındaki sanal makine alt ağını **Get-WAPackVMSubnet** cmdlet 'ini kullanarak alır ve bu nesneyi $VMSubnet değişkeninde depolar.

İkinci komut, $VMSubnet depolanan sanal makine alt ağını kaldırır.
Komut sizden onaylamanızı ister.

### Örnek 2: onaysız sanal makineyi kaldırma
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

İlk komut **Get-WAPackVMSubnet** cmdlet 'Ini kullanarak ContosoVMSubnet02 adındaki bulut hizmetini alır ve bu nesneyi $VMSubnet değişkeninde depolar.

İkinci komut, $VMSubnet depolanan sanal makine alt ağını kaldırır.
Bu komut *Force* parametresini içerir.
Komut sizden onay istemez.

## PARAMETRELERINE

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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

### -VMSubnet
Bir sanal makine alt ağını belirtir.
Sanal makine alt ağı edinmek için **Get-WAPackVMSubnet** cmdlet 'ini kullanın.

```yaml
Type: VMSubnet
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

[Get-WAPackVMSubnet](./Get-WAPackVMSubnet.md)

[Yeni-WAPackVMSubnet](./New-WAPackVMSubnet.md)


