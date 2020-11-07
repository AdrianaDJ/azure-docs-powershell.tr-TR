---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 6d0935b0b2c5296a5d45d25c56cd7feb9e269a55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917912"
---
# Set-AzFirewall

## SYNOPSIS
Değiştirilmiş Güvenlik duvarını kaydeder.

## INDEKI

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarını güncelleştirir.

## ÖRNEKLERDEN

### 1: güvenlik duvarı uygulaması kuralı koleksiyonunun güncelleştirme önceliği
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

Bu örnekte, bir Azure Güvenlik duvarının varolan kural koleksiyonunun önceliği güncelleştirilir.
"AzureFirewall" kaynak grubunda Azure Güvenlik duvarının "RG" olarak kabul edil, "RG" adlı bir uygulama kuralı koleksiyonu içeriyor Set-AzFirewall komutu olmadan, yerel $azFw nesnesinde gerçekleştirilen tüm işlemler sunucuya yansıtılmaz.

### 2: Azure Güvenlik Duvarı oluşturma ve uygulama kuralı koleksiyonunu daha sonra ayarlama
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

Bu örnekte, uygulama kuralı koleksiyonları olmadan önce bir güvenlik duvarı oluşturulur. Ardından uygulama kuralı ve uygulama kuralı koleksiyonu oluşturulur, bulutta gerçek yapılandırma etkilenmeksizin güvenlik duvarı nesnesi bellekte değiştirilir. Değişikliklerin bulutta yansıtılması için Set-AzFirewall çağrılmalıdır.

### 3: Azure Güvenlik duvarının tehdit Intel işlem modunu güncelleştirin
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

Bu örnekte, "RG" kaynak grubundaki "AzureFirewall" Azure Güvenlik duvarının tehdit Intel çalışma modu güncelleştirilir.
Set-AzFirewall komutu olmadan, yerel $azFw nesnesinde gerçekleştirilen tüm işlemler sunucuya yansıtılmaz.

### 4: güvenlik duvarını ayırma ve tahsis etme
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```

Bu örnek bir güvenlik duvarı alır, güvenlik duvarını ayırır ve kaydeder. Serbest bırakma komutu, çalışan hizmeti kaldırır ancak güvenlik duvarının yapılandırmasını korur. Değişikliklerin bulutta yansıtılması için Set-AzFirewall çağrılmalıdır.
Kullanıcı Hizmeti yeniden başlatmak istiyorsa, ayırma yöntemi güvenlik duvarında çağrılmalıdır.
Yeni VNet ve genel IP, güvenlik duvarıyla aynı kaynak grubunda olmalıdır. Değişikliklerin bulutta yansıtılması için, Set-AzFirewall çağrılmalıdır.

### 5: Azure Güvenlik duvarına ortak IP adresi ekleme
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Bu örnekte, "azFwPublicIp1" genel IP adresi güvenlik duvarına bağlıdır.

### 6: Azure güvenlik duvarından genel IP adresini kaldırma
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Bu örnekte, "azFwPublicIp1" genel IP adresi güvenlik duvarından ayrılır.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın

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

### -AzureFirewall
AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
