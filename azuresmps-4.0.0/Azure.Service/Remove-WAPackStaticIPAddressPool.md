---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107412"
---
# Remove-WAPackStaticIPAddressPool

## SYNOPSIS
Statik IP adresi havuzu nesnelerini kaldırır.

## INDEKI

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Remove-Wapackstaticıpaddresspool** cmdlet 'ı statik IP adresi havuzu nesnelerini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: statik IP adresi havuzunu kaldırma
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

İlk komut ContosoStaticIPAddressPool01 adlı statik IP adresi havuzunu **Get-Wapackstaticıpaddresspool** cmdlet 'ini kullanarak alır ve bu nesneyi $StaticIPAddressPool değişkeninde depolar.

İkinci komut $StaticIPAddressPool depolanan statik IP adresi havuzunu kaldırır.
Komut sizden onaylamanızı ister.

### Örnek 2: onay olmadan statik IP adresi havuzunu kaldırma
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

İlk komut ContosoStaticIPAddressPool02 adlı statik IP adresi havuzunu **Get-Wapackstaticıpaddresspool** cmdlet 'ini kullanarak alır ve bu nesneyi $ staticıpaddresspool değişkeninde depolar.

İkinci komut $StaticIPAddressPool depolanan statik IP adresi havuzunu kaldırır.
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

### -Staticıpaddresspool
Bir Staticıpaddresspool belirtir.
Statik IP adresi havuzu edinmek için **Get-Wapackstaticıpaddresspool** cmdlet 'ini kullanın.

```yaml
Type: StaticIPAddressPool
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

[Get-Wapackstaticıpaddresspool](./Get-WAPackStaticIPAddressPool.md)

[Remove-Wapackstaticıpaddresspool](./Remove-WAPackStaticIPAddressPool.md)


