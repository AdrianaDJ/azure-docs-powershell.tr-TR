---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588467"
---
# New-AzureRmFirewallNetworkRule

## SYNOPSIS
Güvenlik Duvarı ağ kuralı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzureRmFirewallNetworkRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir ağ kuralı oluşturur.

## ÖRNEKLERDEN

### 1: tüm TCP trafiği için bir kural oluşturma
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

Bu örnekte tüm TCP trafiği için bir kural oluşturulur. Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.

### 2:10.0.0.0 ile 60.1.5.0 arasında tüm TCP trafiği için bir kural oluşturun: 4040
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

Bu örnekte, 10.0.0.0 ile 60.1.5.0:4040 arasındaki tüm TCP trafiği için bir kural oluşturulur. Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.

### 3: herhangi bir kaynaktan 10.0.0.0/16 adresine giden tüm TCP ve ıCMP trafiği için bir kural oluşturun
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

Bu örnekte, 10.0.0.0 ile 60.1.5.0:4040 arasındaki tüm TCP trafiği için bir kural oluşturulur. Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Açıklama
Bu kural için isteğe bağlı bir açıklama belirtin.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddress
Kuralın hedef adresleri

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPort
Kuralın hedef bağlantı noktaları

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu ağ kuralının adını belirtir. Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.

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

### -İletişim kuralı
Bu kurala göre filtre uygulanacak trafik türünü belirtir. Olası değerler TCP, UDP, ıCMP ve Any değerleridir.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddress
Kuralın kaynak adresleri

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSFirewallNetworkRule

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureRmFirewallNetworkRuleCollection](./New-AzureRmFirewallNetworkRuleCollection.md)

[Yeni-AzureRmFirewall](./New-AzureRmFirewall.md)

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)
