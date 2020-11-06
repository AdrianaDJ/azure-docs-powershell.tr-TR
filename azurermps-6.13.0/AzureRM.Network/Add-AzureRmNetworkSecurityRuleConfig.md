---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 051a46fe9c6dc6a4178dac2ccb69dc58a1031b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594882"
---
# Add-AzureRmNetworkSecurityRuleConfig

## SYNOPSIS
Ağ güvenlik grubuna ağ güvenlik kuralı yapılandırması ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SetByResource (varsayılan)
```
Add-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Setbyresourceıd
```
Add-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-AzureRmNetworkSecurityRuleConfig** cmdlet 'ı bir Azure ağ güvenlik grubuna ağ güvenlik kuralı yapılandırması ekler.

## ÖRNEKLERDEN

### 1: ağ güvenlik grubu ekleme
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzureRmNetworkSecurityGroup
```

İlk komut, "RG1" kaynak grubundan "nsg1" adlı bir Azure ağ güvenlik grubunu alır. İkinci komut "RDP-Rule" adlı bir ağ güvenlik kuralı ekler; bağlantı 3389 noktası Değiştirilmiş Azure Network Security grubunu devam ettirir.

### 2: uygulama güvenlik gruplarıyla yeni bir güvenlik kuralı ekleme
```
$srcAsg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzureRmNetworkSecurityGroup
```

İlk olarak iki yeni uygulama güvenlik grubu oluşturduk. Ardından, "RG1" kaynak grubundan "nsg1" adlı bir Azure ağ güvenlik grubunu aldık. ve buna "RDP-Rule" adlı bir ağ güvenliği kuralı ekleyin. Kural, "srcAsg" uygulama güvenlik grubundaki tüm IP yapılandırmalarından gelen trafiğe, bağlantı noktası 3389 "destAsg" uygulamasındaki tüm IP yapılandırmalarına izin verir. Kuralı ekledikten sonra, değiştirilmiş Azure ağ güvenlik grubunu devam ediyoruz.

## PARAMETRELERINE

### -Access
Ağ trafiğine izin verilip verilmediğini belirtir.
Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Açıklama
Ağ güvenlik kuralı yapılandırmasının açıklamasını belirtir.

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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yön
Kuralın gelen veya giden trafikte değerlendirilip değerlendirilmeyeceğini belirtir.
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
Ağ güvenlik kuralı yapılandırmasının adını belirtir.

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
Bir **Networksecuritygroup** nesnesini belirtir.
Bu cmdlet, bu parametrenin belirttiği nesneye ağ güvenlik kuralı yapılandırması ekler.

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
Bu parametre için kabul edilebilir değerler şunlardır:
- TC
- UDP
- İkisi ile eşleşen joker karakter (*)

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
- Herhangi bir IP adresiyle eşleşen joker karakter (*).
VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
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
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Kaynak bağlantı noktası veya aralığını belirtir.
Bu değer bir tamsayı olarak, 0 ile 65535 arasındaki bir Aralık veya herhangi bir kaynak bağlantı noktası ile eşleşen bir joker karakter (*) olarak ifade edilir.

```yaml
Type: System.Collections.Generic.List`1[System.String]
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

### Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup
Parametreler: NetworkSecurityGroup (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmNetworkSecurityRuleConfig](./Get-AzureRmNetworkSecurityRuleConfig.md)

[Yeni-AzureRmNetworkSecurityRuleConfig](./New-AzureRmNetworkSecurityRuleConfig.md)

[Remove-AzureRmNetworkSecurityRuleConfig](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[Set-AzureRmNetworkSecurityRuleConfig](./Set-AzureRmNetworkSecurityRuleConfig.md)


