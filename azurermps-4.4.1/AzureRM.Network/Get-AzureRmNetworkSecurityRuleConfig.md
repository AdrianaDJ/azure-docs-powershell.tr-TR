---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 903738f1cb2e816ce18c9e5e3c9b01cf3d4baa9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594627"
---
# Get-AzureRmNetworkSecurityRuleConfig

## SYNOPSIS
Ağ güvenlik grubunun ağ güvenlik kuralı yapılandırmasını alma.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmNetworkSecurityRuleConfig** cmdlet 'i, bir Azure ağ güvenlik grubu için ağ güvenlik kuralı yapılandırmasını alır.

## ÖRNEKLERDEN

### 1: ağ güvenlik kuralı yapılandırması alınıyor
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

Bu komut, "nsg1" kaynak grubundaki "Allowınternetoutbound" adlı Azure Network Security grubundan "RG1" adlı varsayılan kuralı alır

### 2: yalnızca adı kullanarak ağ güvenlik kuralı yapılandırması alma
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

Bu komut, "RG1" kaynak grubundaki "nsg1" adlı Azure Network Security grubundan "RDP-Rule" adlı Kullanıcı tanımlı kuralı alır

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

### -DefaultRules
Bu cmdlet 'in Kullanıcı tarafından oluşturulan bir kural yapılandırması mı yoksa varsayılan bir kural yapılandırması mı aldığını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Alınacak ağ güvenliği kuralı yapılandırmasının adını belirtir.

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

### -NetworkSecurityGroup
Alınacak ağ güvenliği kuralı yapılandırmasını içeren bir **Networksecuritygroup** nesnesi belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### PSNetworkSecurityGroup
' NetworkSecurityGroup ' parametresi ardışık düzenin ' PSNetworkSecurityGroup ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSSecurityRule

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureRmNetworkSecurityRuleConfig](./Add-AzureRmNetworkSecurityRuleConfig.md)

[Yeni-AzureRmNetworkSecurityRuleConfig](./New-AzureRmNetworkSecurityRuleConfig.md)

[Remove-AzureRmNetworkSecurityRuleConfig](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[Set-AzureRmNetworkSecurityRuleConfig](./Set-AzureRmNetworkSecurityRuleConfig.md)


