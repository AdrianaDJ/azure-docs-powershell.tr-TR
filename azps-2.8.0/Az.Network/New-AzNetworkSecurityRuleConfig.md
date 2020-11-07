---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: e3afa3ee5809af2760225be674990827c117bdfa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918231"
---
# New-AzNetworkSecurityRuleConfig

## SYNOPSIS
Ağ güvenlik kuralı yapılandırması oluşturur.

## INDEKI

### SetByResource (varsayılan)
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Setbyresourceıd
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-Azağsecurityruleconfig** cmdlet 'i, bir ağ güvenlik grubu Için bir Azure ağ güvenlik kuralı yapılandırması oluşturur.

## ÖRNEKLERDEN

### 1: RDP 'ye izin veren ağ güvenlik kuralı oluşturma
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

Bu komut Internet 'ten bağlantı noktası 3389 'e erişim izni veren bir güvenlik kuralı oluşturur

### 2: HTTP 'ye izin veren ağ güvenlik kuralı oluşturma
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

Bu komut Internet 'ten bağlantı noktası 80 'e erişim izni veren bir güvenlik kuralı oluşturur

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
Oluşturulacak ağ güvenliği kuralı yapılandırmasının açıklamasını belirtir.

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
Bu cmdlet 'in oluşturduğu ağ güvenlik kuralı yapılandırmasının adını belirtir.

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
Yeni bir kural yapılandırmasının uygulandığı ağ protokolünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- TC
- UDP
- joker karakter (*) ile eşleşir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSSecurityRule

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


