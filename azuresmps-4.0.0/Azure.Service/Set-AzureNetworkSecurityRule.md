---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105800"
---
# Set-AzureNetworkSecurityRule

## SYNOPSIS
Ağ güvenlik grubuna ağ güvenliği kuralı ekler veya değiştirir.

## INDEKI

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureNetworkSecurityRule** cmdlet 'i, bir ağ güvenlik grubunda bir Azure ağ güvenliği kuralı ekler veya değiştirir.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -Eylem
Ağ güvenlik kuralı eylemini belirtir.
Geçerli değerler: Izin ver ve Reddet.

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

### -DestinationAddressPrefix
Ağ güvenlik kuralı için hedef IP aralığının sınıfsız etki alanları arası yönlendirme (CıDR) adresini belirtir.
Yıldız işareti (*) herhangi bir IP adresini belirtir.

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

### -DestinationPortRange
Ağ güvenlik kuralı için bir hedef bağlantı noktası aralığı belirtir.
Geçerli değerler 0 ile 65535 arasında tamsayılar içerir.
Tek bir değer belirtebilir ya da bir aralığı, küçük harf-HigherNumber biçiminde belirtebilirsiniz.
Tire iki değeri birbirinden ayırır.

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
Bu cmdlet 'in eklediği veya değiştirdiği ağ güvenlik kuralının adını belirtir.

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

### -NetworkSecurityGroup
Bu cmdlet 'in değiştirdiği ağ güvenlik grubunu belirtir.
**Inetworksecuritygroup** nesnesi edinmek için Get-AzureNetworkSecurityGroup cmdlet 'ini kullanın.

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Öncelik
Ağ güvenlik kuralının önceliğini belirtir.
Geçerli değerler: 100 ile 4096 arasındaki tamsayılar.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir. Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

### -İletişim kuralı
Ağ güvenlik kuralı protokolünü belirtir.
Geçerli değerler: 

- TC 
- UDP 
- *

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

### -SourceAddressPrefix
Ağ güvenlik kuralı için kaynak IP aralığının CıDR adresini belirtir.
Yıldız işareti (*) herhangi bir IP adresini belirtir.

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

### -SourcePortRange
Ağ güvenlik kuralı için bir kaynak bağlantı noktası aralığı belirtir.
Geçerli değerler 0 ile 65535 arasında tamsayılar içerir.
Tek bir değer belirtebilir ya da bir aralığı, küçük harf-HigherNumber biçiminde belirtebilirsiniz.
Tire iki değeri birbirinden ayırır.

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

### -Tür
Ağ güvenlik kuralı için bağlantı türünü belirtir.
Geçerli değerler: gelen ve giden.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureNetworkSecurityRule](./Remove-AzureNetworkSecurityRule.md)


