---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764616"
---
# New-AzureRmFirewallApplicationRule

## SYNOPSIS
Güvenlik duvarı uygulaması kuralı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### TargetFqdn (varsayılan)
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FqdnTag
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzureRmFirewallApplicationRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir uygulama kuralı oluşturur.

## ÖRNEKLERDEN

### 1:10.0.0.0 'tan tüm HTTPS trafiğine izin veren bir kural oluşturma
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

Bu örnek, bağlantı noktası 443 üzerindeki HTTPS trafiğinin 10.0.0.0 'den izin verecek bir kural oluşturur.

### 2:10.0.0.0/24 alt ağı için WindowsUpdate 'e izin veren bir kural oluşturma
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

Bu örnek, 10.0.0.0/24 etki alanı için Windows güncelleştirmelerinde trafiğe izin verecek bir kural oluşturur.

## PARAMETRELERINE

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
Bu kural için FQDN etiketlerinin listesini belirtir. Kullanılabilir Etiketler [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet 'i kullanılarak alınabilir.

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[System.String]
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
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSFirewallApplicationRule

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureRmFirewallApplicationRuleCollection](./New-AzureRmFirewallApplicationRuleCollection.md)

[Yeni-AzureRmFirewall](./New-AzureRmFirewall.md)

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)

[Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md)
