---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107406"
---
# Remove-WAPackVNet

## SYNOPSIS
Sanal ağ nesnelerini kaldırır.

## INDEKI

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Remove-WAPackVNet** cmdlet 'i sanal ağ nesnelerini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: sanallaştırılmış bir ağı kaldırma
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

İlk komut ContosoVNet01 adlı sanallaştırılmış ağı **Get-WAPackVNet** cmdlet 'ini kullanarak alır ve bu nesneyi $VNET değişkeninde depolar.
İkinci komut $VNet 'da depolanan sanallaştırılmış ağı kaldırır.
Komut sizden onaylamanızı ister.

### Örnek 2: bir sanallaştırılmış ağı onaysız kaldırma
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

İlk komut **Get-WAPackVNet** cmdlet 'Ini kullanarak ContosoVNet02 adındaki bulut hizmetini alır ve bu nesneyi $VNET değişkeninde depolar.
İkinci komut $VNet 'da depolanan sanallaştırılmış ağı kaldırır.
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

### -VNet
Sanallaştırılmış bir ağ belirtir.
Sanallaştırılmış bir ağ edinmek için **Get-WAPackVNet** cmdlet 'ini kullanın.

```yaml
Type: VMNetwork
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

[Get-WAPackVNet](./Get-WAPackVNet.md)

[Yeni-WAPackVNet](./New-WAPackVNet.md)


