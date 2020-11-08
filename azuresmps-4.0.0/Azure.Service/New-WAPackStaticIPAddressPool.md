---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107381"
---
# New-WAPackStaticIPAddressPool

## SYNOPSIS
Statik IP adresi havuzu oluşturur.

## INDEKI

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Yeni-Wapackstaticıpaddresspool** cmdlet 'ı statik IP adresi havuzu oluşturur.

## ÖRNEKLERDEN

### Örnek 1: statik IP adresi havuzu oluşturma
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

İlk komut öncelikle, statik IP adresi havuzu eklemek istediğimiz sanal makine ağını alır.
Bu sanal makine ağının adı ContosoVNet01.

İkinci komut, statik IP adresi havuzunu eklemek istediğimiz ContosoVMSubnet01 adlı sanal makine alt ağını almak için daha önce alınan sanal makine ağını kullanır.

Son komut, ad ContosoStaticIpAddressPool01 ile yeni bir statik IP adresi havuzu oluşturur ve bir aralığı Başlat 192.168.1.0 ve bir Aralık uç 192.168.1.10.

## PARAMETRELERINE

### -IPAddressRangeEnd
Statik IP adresi havuzu için bir IP adresi aralığı sonu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ipaddressrangestart
Statik IP adresi havuzu için bir IP adresi aralığı başlangıcını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Statik IP adresi havuzu için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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
Statik IP adresi havuzuyla ilişkili bir VMSubnet belirtir.

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

[Get-Wapackstaticıpaddresspool](./Get-WAPackStaticIPAddressPool.md)

[Remove-Wapackstaticıpaddresspool](./Remove-WAPackStaticIPAddressPool.md)


