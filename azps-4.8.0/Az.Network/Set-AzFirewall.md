---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274777"
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

### 5: Zorlamalı tünel senaryoları için bir yönetim genel IP adresiyle tahsis edin
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
Bu örnek güvenlik duvarını, Zorlamalı tünel senaryoları için genel bir genel IP adresi ve alt ağ ile ayırır. VNet, "AzureFirewallManagementSubnet" adlı bir alt ağ içermelidir.

### 6: Azure Güvenlik duvarına ortak IP adresi ekleme
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Bu örnekte, "azFwPublicIp1" genel IP adresi güvenlik duvarına bağlıdır.

### 7: Azure güvenlik duvarından genel IP adresini kaldırma
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

Bu örnekte, "azFwPublicIp1" genel IP adresi güvenlik duvarından ayrılır.

### 8: Azure Güvenlik duvarında Yönetim genel IP adresini değiştirme
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

Bu örnekte, güvenlik duvarının genel genel IP adresi "AzFwMgmtPublicIp2" olarak değiştirilir

### 9: Azure Güvenlik duvarına DNS yapılandırması ekleme
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

Bu örnekte, DNS proxy ve DNS sunucusu yapılandırması güvenlik duvarına eklenir.

### 10: güvenlik duvarı uygulama kuralı koleksiyonunda var olan bir kuralın hedefini güncelleştirme
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

Bu örnekte, bir Azure Güvenlik duvarının kural koleksiyonundaki mevcut bir kuralın hedefi güncelleştirilir. Bu, IP adresleri dinamik olarak değiştiğinde kurallarınızı otomatik olarak güncelleştirmenize olanak tanır.

### 11: Azure Güvenlik duvarında Active FTP 'ye izin verme
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

Bu örnekte, güvenlik duvarında Active FTP 'ye izin verilir.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
