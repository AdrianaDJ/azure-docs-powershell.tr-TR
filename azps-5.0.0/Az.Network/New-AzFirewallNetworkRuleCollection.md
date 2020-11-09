---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 49a7484c0ca0b1a3dfa0feb82e09632d631333ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323806"
---
# New-AzFirewallNetworkRuleCollection

## SYNOPSIS
Ağ kuralları için bir Azure Güvenlik Duvarı ağ koleksiyonu oluşturur.

## INDEKI

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzFirewallNetworkRuleCollection** cmdlet 'ı, güvenlik duvarı ağ kuralları koleksiyonu oluşturur.

## ÖRNEKLERDEN

### Örnek 1: iki kuralla bir ağ koleksiyonu oluşturma
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

Bu örnek, iki kuralla eşleşen tüm trafiğe izin verecek bir koleksiyon oluşturur.
İlk kural tüm UDP trafiği içindir.
İkinci kural, 10.0.0.0 'den 60.1.5.0:4040 'e giden TCP trafiğine yöneliktir.
Aynı zamanda $rule 1 veya $rule 2 ' de tanımlanan trafikle eşleşen daha yüksek önceliğe sahip bir ağ kuralı koleksiyonu varsa, kural koleksiyonunun yüksek önceliğe sahip olan eylemi geçerli olacaktır. 

### Örnek 2: kural koleksiyonuna kural ekleme
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

Bu örnek, bir kuralla yeni bir ağ kuralı koleksiyonu oluşturur ve ardından kural koleksiyonu nesnesinde yöntem AddRule kullanarak kural koleksiyonuna ikinci bir kural ekler. Verilen bir kural koleksiyonundaki her kuralın adı benzersiz olmalıdır ve büyük/küçük harfe duyarlıdır.

### Örnek 3: kural koleksiyonundan kural alma
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

Bu örnek, bir kuralla yeni bir ağ kuralı koleksiyonu oluşturur ve kuralı adı, kural koleksiyonu nesnesinde GetRuleByName yöntemini arayan kuralı alır. GetRuleByName metodunun kural adı büyük/küçük harf duyarlı değildir.

### Örnek 4: kural koleksiyonundan kural kaldırma
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

Bu örnek, iki kural içeren yeni bir ağ kuralı koleksiyonu oluşturur ve ardından kural koleksiyonu nesnesinde yöntemi çağırarak kural koleksiyonundan ilk kuralı kaldırır. Yöntem için kural adı, büyük/küçük harf duyarlı değildir.

## PARAMETRELERINE

### -ActionType
Bu kuralın trafik eşleştirme koşullarıyla gerçekleştirilecek eylemi belirtir. Kabul edilen eylemler "Izin ver" veya "Reddet".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
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

### -Ad
Bu ağ kuralı koleksiyonunun adını belirtir. Ad tüm ağ kuralı koleksiyonunda benzersiz olmalıdır.

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
Bu kural koleksiyonunun önceliğini belirtir. Öncelik, 100 ve 65000 arasındaki bir sayıdır. Sayı ne kadar küçükse, öncelik o kadar yüksektir.

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kural
Bu koleksiyon altında Gruplanacak kuralların listesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRuleCollection

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzFirewallNetworkRule](./New-AzFirewallNetworkRule.md)

[New-AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)
