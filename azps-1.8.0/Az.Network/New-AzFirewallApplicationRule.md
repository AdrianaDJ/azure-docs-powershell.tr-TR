---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: 6aad78a873b1eb24f1534c9b8c0b38d1567ee2ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760344"
---
# New-AzFirewallApplicationRule

## SYNOPSIS
Güvenlik duvarı uygulaması kuralı oluşturur.

## INDEKI

### TargetFqdn (varsayılan)
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FqdnTag
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzFirewallApplicationRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir uygulama kuralı oluşturur.

## ÖRNEKLERDEN

### 1:10.0.0.0 'tan tüm HTTPS trafiğine izin veren bir kural oluşturma
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

Bu örnek, bağlantı noktası 443 üzerindeki HTTPS trafiğinin 10.0.0.0 'den izin verecek bir kural oluşturur.

### 2:10.0.0.0/24 alt ağı için WindowsUpdate 'e izin veren bir kural oluşturma
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

Bu örnek, 10.0.0.0/24 etki alanı için Windows güncelleştirmelerinde trafiğe izin verecek bir kural oluşturur.

## PARAMETRELERINE

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
Bu kural için isteğe bağlı bir açıklama belirtin.

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

### -FqdnTag
Bu kural için FQDN etiketlerinin listesini belirtir. Kullanılabilir Etiketler [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet 'i kullanılarak alınabilir.

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu uygulama kuralının adını belirtir. Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.

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

### -İletişim kuralı
Bu kurala göre filtre uygulanacak trafik türünü belirtir. Biçim <protocol type> : <port> . Örneğin, "http: 80" veya "https: 443".
TargetFqdn kullanıldığında protokol zorunludur, ancak FqdnTag ile kullanılamaz. Desteklenen protokoller HTTP ve HTTPS 'DIR.

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
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
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFqdn
Bu kurala göre filtrelenmiş etki alanı adlarının listesini belirtir.
' ' Yıldız karakteri, *yalnızca listedeki BIR FQDN 'nin ilk karakteri olarak kabul edilir. Kullanıldığında, yıldız karakteri herhangi bir sayıda karakterle eşleşir. (örneğin, '* msn.com ', msn.com ve tüm alt etki alanlarına eşleşir)

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSAzureFirewallApplicationRule

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzFirewallApplicationRuleCollection](./New-AzFirewallApplicationRuleCollection.md)

[New-AzFirewall](./New-AzFirewall.md)

[Get-AzFirewall](./Get-AzFirewall.md)

[Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md)
