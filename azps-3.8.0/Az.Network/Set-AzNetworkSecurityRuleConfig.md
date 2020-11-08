---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: cff46867b92010969118ced67f53f5bd94c8337f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097961"
---
# Set-AzNetworkSecurityRuleConfig

## SYNOPSIS
Ağ güvenlik grubu için ağ güvenliği kuralı yapılandırmasını güncelleştirir.

## INDEKI

### SetByResource (varsayılan)
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Setbyresourceıd
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Set-Azağsecurityruleconfig** cmdlet 'i, ağ güvenlik grubu için bir ağ güvenliği kuralı yapılandırmasını güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1: ağ güvenlik kuralında erişim yapılandırmasını değiştirme
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

İlk komut NSG-ön uç adlı ağ güvenlik grubunu alır ve bunu değişken $nsg depolar.
İkinci komut, RDP kuralı adlı güvenlik kuralı yapılandırmasını alan ve Get-AzNetworkSecurityRuleConfig öğesine $nsg güvenlik grubuna geçirmek için ardışık düzen işlecini kullanır.
Üçüncü komut, RDP kuralının erişim yapılandırmasını reddedecek şekilde değiştirir.

## PARAMETRELERINE

### -Access
Ağ trafiğine izin verilip verilmediğini belirtir. Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Açıklama
Kural yapılandırmasının açıklamasını belirtir.
Boyut üst sınırı 140 karakterdir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
Hedef adres önekini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi 
- Hedef IP adresi aralığı 
- Herhangi bir IP adresiyle eşleşen bir joker karakter (*), VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
Kural için hedef olarak ayarlanan uygulama güvenlik grubu. ' DestinationAddressPrefix ' parametresiyle kullanılamaz.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destinationapplicationsecuritygroupıd
Kural için hedef olarak ayarlanan uygulama güvenlik grubu. ' DestinationAddressPrefix ' parametresiyle kullanılamaz.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
Hedef bir bağlantı noktası veya aralığı belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Bir tamsayı 
- 0 ile 65535 arasında bir tamsayı aralığı
- Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (*)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yön
Kuralın gelen veya giden trafik için değerlendirilip değerlendirilmeyeceğini belirtir.
Bu parametre için kabul edilebilir değerler: gelen ve giden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in ayarladığı ağ güvenlik kuralı yapılandırmasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
Ayarlanacak ağ güvenlik kuralı yapılandırmasını içeren **Networksecuritygroup** nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Öncelik
Kural yapılandırmasının önceliğini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.
Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.
Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -İletişim kuralı
Kural yapılandırmasının uygulandığı ağ protokolünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:-TCP
- UDP
- Her ikisiyle eşleşen bir joker karakter (*)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Kaynak adres önekini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- CıDR
- Kaynak IP aralığı
- Herhangi bir IP adresiyle eşleşen bir joker karakter (*), VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
Kural için kaynak olarak ayarlanan uygulama güvenlik grubu. ' SourceAddressPrefix ' parametresiyle kullanılamaz.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sourceapplicationsecuritygroupıd
Kural için kaynak olarak ayarlanan uygulama güvenlik grubu. ' SourceAddressPrefix ' parametresiyle kullanılamaz.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Kaynak bağlantı noktasını veya aralığını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Bir tamsayı
- 0 ile 65535 arasında bir tamsayı aralığı
- Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (*)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


