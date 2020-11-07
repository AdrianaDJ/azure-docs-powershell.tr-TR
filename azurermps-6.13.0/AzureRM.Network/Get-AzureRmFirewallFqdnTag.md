---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764618"
---
# Get-AzureRmFirewallFqdnTag

## SYNOPSIS
Kullanılabilir Azure Güvenlik Duvarı FQDN etiketlerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmFirewallFqdnTag** cmdlet 'ı, Azure Güvenlik Duvarı uygulama kuralları IÇIN kullanılabilen FQDN etiketlerinin listesini alır

## ÖRNEKLERDEN

### 1: kullanılabilir tüm FQDN etiketlerini alma
```
Get-AzureRmFirewallFqdnTag
```

Bu örnekte, kullanılabilir tüm FQDN etiketleri alınır.

### 2: uygulama kuralında kullanılabilir ilk FQDN etiketini kullanın
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

Bu örnekte, kullanılabilir ilk FQDN etiketini kullanan bir güvenlik duvarı uygulaması kuralı oluşturulur

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSAzureFirewallFqdnTag

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureRmFirewallApplicationRule](./New-AzureRmFirewallApplicationRule.md)

[Yeni-AzureRmFirewall](./New-AzureRmFirewall.md)
