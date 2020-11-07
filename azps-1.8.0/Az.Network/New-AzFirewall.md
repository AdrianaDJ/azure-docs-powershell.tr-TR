---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760345"
---
# New-AzFirewall

## SYNOPSIS
Kaynak grubunda yeni bir güvenlik duvarı oluşturur.

## INDEKI

### Varsayılan (varsayılan)
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Ipconfigurationparametervalues değerleri
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarı oluşturur.

## ÖRNEKLERDEN

### 1: sanal ağa bağlı bir güvenlik duvarı oluşturma
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.
Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).
Ayrıca, Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda da çalışır.

### 2: tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturun
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

Bu örnek, bağlantı noktası 443 ' de tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturur.
Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda çalışır.

### 3: VSEÇNAT-10.1.2.3 adresine yönlendirilen trafiği yeniden yönlendir: 10.2.3.4:8080
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

Bu örnek, 10.1.2.3 adresine giden tüm paketlerin hedef IP ve bağlantı noktasını çeviren bir güvenlik duvarı oluşturmuştur, bu örnekte 10.2.3.4:8080 tehdit Intel kapalıdır.

### 4: kural olmadan ve sorun durumunda Intel ile güvenlik duvarı oluşturma
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

Bu örnek, tüm trafiği (varsayılan davranış) engelleyen ve uyarı modunda çalışan tehdit Intel 'e sahip bir güvenlik duvarı oluşturur.
Bu, diğer kuralların uygulanması (Bu örnekte yalnızca varsayılan kural) uygulanmadan önce kötü amaçlı trafik için uyarı günlüklerinin Yayınlanma anlamına gelir.

### 5: bağlantı noktası 8080 ' da tüm HTTP trafiğine izin veren ancak tehdit Intel tarafından tanımlanan kötü amaçlı etki alanlarını engeller
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

Bu örnek, 8080 iş parçacığı tarafından kötü niyetli olarak kabul edilmedikçe, bağlantı noktası üzerindeki tüm HTTP trafiğinin güvenlik duvarını oluşturur.
Engelleme modunda çalışırken, uyarıdan farklı olarak, tehdit ile kötü amaçlı olan trafik yalnızca günlüğe kaydedilmez, ancak engellenmiş olur.

## PARAMETRELERINE

### -ApplicationRuleCollection
Yeni güvenlik duvarının uygulama kuralları koleksiyonlarını belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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

### -Konum
Güvenlik duvarının bölgesini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in oluşturduğu Azure Güvenlik duvarının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NatRuleCollection
AzureFirewallNatRuleCollections listesi

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleCollection
AzureFirewallNetworkRuleCollections listesi

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpName
Genel IP adı. Genel IP standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Güvenlik duvarını içerecek kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin:

@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Threatıntelmodu
Tehdit yönetim bilgileri için işlem modunu belirtir. Varsayılan mod, kapalı değil uyarıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkName
Güvenlik duvarının dağıtılacağı sanal ağın adını belirtir. Sanal ağ ve güvenlik duvarı aynı kaynak grubuna ait olmalıdır.

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

### Microsoft. Azure. Commands. Network. model. PSAzureFirewallApplicationRuleCollection []

### Microsoft. Azure. Commands. Network. model. PSAzureFirewallNatRuleCollection []

### Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRuleCollection []

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzFirewall](./Get-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)

[Set-AzFirewall](./Set-AzFirewall.md)

[New-AzFirewallApplicationRuleCollection](./New-AzFirewallApplicationRuleCollection.md)

[Yeni-AzFirewallNatRuleCollection](./New-AzFirewallNatRuleCollection.md)

[New-AzFirewallNetworkRuleCollection](./New-AzFirewallNetworkRuleCollection.md)
