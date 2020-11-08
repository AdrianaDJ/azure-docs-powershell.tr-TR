---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274148"
---
# Get-AzFirewallFqdnTag

## SYNOPSIS
Kullanılabilir Azure Güvenlik Duvarı FQDN etiketlerini alır.

## INDEKI

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzFirewallFqdnTag** cmdlet 'ı, Azure Güvenlik Duvarı uygulama kuralları IÇIN kullanılabilen FQDN etiketlerinin listesini alır

## ÖRNEKLERDEN

### 1: kullanılabilir tüm FQDN etiketlerini alma
```
Get-AzFirewallFqdnTag
```

Bu örnekte, kullanılabilir tüm FQDN etiketleri alınır.

### 2: uygulama kuralında kullanılabilir ilk FQDN etiketini kullanın
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

Bu örnekte, kullanılabilir ilk FQDN etiketini kullanan bir güvenlik duvarı uygulaması kuralı oluşturulur

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallFqdnTag

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. cmdlet. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[New-AzFirewall](./New-AzFirewall.md)
