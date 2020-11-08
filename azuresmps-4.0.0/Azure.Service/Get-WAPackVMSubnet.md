---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107355"
---
# Get-WAPackVMSubnet

## SYNOPSIS
Sanal makine alt ağ nesnelerini alır.

## INDEKI

### FromVMNetworkObject (varsayılan)
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Get-WAPackVMSubnet** cmdlet 'i sanal makine alt ağ nesnelerini alır.

## ÖRNEKLERDEN

### Örnek 1: ad kullanarak sanal makine alt ağını alma
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

Bu komut, ContosoSubnet01 adındaki sanal makine alt ağını alır.

### Örnek 2: KIMLIK kullanarak sanal makine alt ağını alma
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

Bu komut, belirtilen KIMLIĞE sahip sanal makine alt ağını alır.

### Örnek 3: verilen sanallaştırılmış ağlardan tüm sanal makine alt ağlarını alma
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

Bu komut, belirli bir sanallaştırılmış ağın tüm sanal makine alt ağlarını alır.

## PARAMETRELERINE

### -ID
Sanal makine alt ağının benzersiz KIMLIĞINI belirtir.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Sanal makine alt ağının adını belirtir.

```yaml
Type: String
Parameter Sets: FromName
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

### -VNet
Sanal makine alt ağıyla ilişkili VNet belirtir.

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

[Yeni-WAPackVMSubnet](./New-WAPackVMSubnet.md)

[Remove-WAPackVMSubnet](./Remove-WAPackVMSubnet.md)


