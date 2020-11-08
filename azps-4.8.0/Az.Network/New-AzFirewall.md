---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: a7c38a264860ad4a8458dbdb3555980279a33ff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274861"
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
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Oldıda Configurationparametervalues
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Ipconfigurationparametervalues değerleri
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**New-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: sanal ağa bağlı bir güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.
Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).
Ayrıca, Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda da çalışır.

### Örnek 2: tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

Bu örnek, bağlantı noktası 443 ' de tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturur.
Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda çalışır.

### Örnek 3: VSEÇNAT-10.1.2.3 'e yönlendirilen trafiği yeniden yönlendir: 10.2.3.4:8080
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

Bu örnek, 10.1.2.3 adresine giden tüm paketlerin hedef IP ve bağlantı noktasını çeviren bir güvenlik duvarı oluşturmuştur, bu örnekte 10.2.3.4:8080 tehdit Intel kapalıdır.

### Örnek 4: kural olmadan ve iş arkadaşlarınızla Intel uyarı modunda güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

Bu örnek, tüm trafiği (varsayılan davranış) engelleyen ve uyarı modunda çalışan tehdit Intel 'e sahip bir güvenlik duvarı oluşturur.
Bu, diğer kuralların uygulanması (Bu örnekte yalnızca varsayılan kural) uygulanmadan önce kötü amaçlı trafik için uyarı günlüklerinin Yayınlanma anlamına gelir.

### Örnek 5: bağlantı noktası 8080 ' da tüm HTTP trafiğine izin veren ancak tehdit Intel tarafından tanımlanan kötü amaçlı etki alanlarını engeller
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

Bu örnek, 8080 iş parçacığı tarafından kötü niyetli olarak kabul edilmedikçe, bağlantı noktası üzerindeki tüm HTTP trafiğinin güvenlik duvarını oluşturur.
Engelleme modunda çalışırken, uyarıdan farklı olarak, tehdit ile kötü amaçlı olan trafik yalnızca günlüğe kaydedilmez, ancak engellenmiş olur.

### Örnek 6: kural olmadan ve kullanılabilirlik bölgeleriyle güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

Bu örnekte, kullanılabilir tüm kullanılabilirlik bölgeleri içeren bir güvenlik duvarı oluşturulur.

### Örnek 7: iki veya daha çok ortak IP adresi içeren bir güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

Bu örnek, iki genel IP adresi olan "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.

### Örnek 8: belirli SQL veritabanıyla MSSQL trafiğine izin veren bir güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

Bu örnek, 1433 için standart bağlantı noktası MSSQL trafiğine izin veren bir güvenlik duvarı oluşturur.

### Örnek 9: sanal hub 'a bağlı bir güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

Bu örnek, "vHub" sanal hub 'ına bağlı bir güvenlik duvarı oluşturur. Güvenlik duvarına bir güvenlik duvarı ilkesi $fp eklenir. Bu güvenlik duvarı, güvenlik duvarı $fp ilkesinde belirtilen kurallara dayalı olarak trafiğe izin verir/reddeder. Sanal hub ve güvenlik duvarı aynı bölgede olmalıdır.

### Örnek 10: tehdit zek
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

Bu örnek, tehdit zekkarşı "www.microsoft.com" ve "8.8.8.8" gibi beyaz bir liste oluşturur

### Örnek 11: özelleştirilmiş özel Aralık kurulumuyla bir güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

Bu örnekte, "99.99.99.0/24" ve "66.66.0.0/16" özel IP aralığı olarak ele

### Örnek 12: Yönetim alt ağı ve genel IP adresiyle güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.
Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).
Ayrıca, Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda da çalışır.

"Zorunlu tünel" senaryolarını desteklemek için, bu güvenlik duvarı "AzureFirewallManagementSubnet" alt ağını ve yönetim trafiği için yönetim genel IP adresini kullanır

### Örnek 13: sanal ağa güvenlik duvarı Ilkesiyle ilişkili bir güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.
Güvenlik duvarına uygulanacak kurallar ve tehdit bilgileri güvenlik duvarı ilkesinden alınır

### Örnek 14: DNS proxy 'Si ve DNS sunucularıyla güvenlik duvarı oluşturma
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.
DNS proxy bu güvenlik duvarı için etkinleştirildi ve 2 DNS sunucusu sağlanır. Ayrıca ağ kuralları için DNS proxy ıste, FQDN içeren ağ kuralları varsa, DNS proxy 'si de kullanılır.

### Örnek 15: birden çok IP içeren bir güvenlik duvarı oluşturun. Güvenlik Duvarı sanal hub ile ilişkilendirilebilir
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -Sku AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

Bu örnekte, güvenlik duvarıyla aynı kaynak grubunda sanal hub 'a bağlı bir güvenlik duvarı oluşturulur.
Güvenlik duvarına, örtük olarak oluşturulan 2 genel IP 'Ler atanır.

### 16: etkin FTP 'ye Izin veren bir güvenlik duvarı oluşturun.
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

Bu örnek, etkin FTP bayrağı olan bir güvenlik duvarı oluşturur.

## PARAMETRELERINE

### -ApplicationRuleCollection
Yeni güvenlik duvarının uygulama kuralları koleksiyonlarını belirtir.

```yaml
Type: PSAzureFirewallApplicationRuleCollection[]
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
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsProxyNotRequiredForNetworkRule
Ağ kuralları içinde FQDN 'Ler için DNS proxy işlevleri gerekir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsServer
DNS çözümlemesi için kullanılacak DNS sunucularının listesi

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDnsProxy
DNS proxy 'yi etkinleştirin. Varsayılan olarak devre dışıdır.


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowActiveFTP
Güvenlik duvarında etkin FTP 'ye izin verir. Varsayılan olarak devre dışıdır.


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Firewallpolicyıd
Güvenlik duvarına bağlı güvenlik duvarı ilkesi

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hubıpaddresses
Sanal hub 'a bağlı güvenlik duvarının IP adresleri

```yaml
Type: PSAzureFirewallHubIpAddresses
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
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Managementpublicıpaddress
Yönetim trafiği için kullanılacak bir veya birden çok ortak IP adresi. Genel IP adresleri standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.

```yaml
Type: PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in oluşturduğu Azure Güvenlik duvarının adını belirtir.

```yaml
Type: String
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
Type: PSAzureFirewallNatRuleCollection[]
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
Type: PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateRange
Trafiğin eşitlenmeyeceği özel IP aralıkları

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publicıpaddress
Bir veya daha fazla ortak IP adresi. Genel IP adresleri standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.

```yaml
Type: PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpName
Genel IP adı. Genel IP standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
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
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Güvenlik Duvarı için SKU türü

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin:

@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: Hashtable
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
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Threatıntelwhitelist
Tehdit yönetim bilgileri için beyaz liste

```yaml
Type: PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Virtualhubıd
Güvenlik duvarının bağlı olduğu sanal hub

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Sanal ağ

```yaml
Type: PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Güvenlik duvarının dağıtılacağı sanal ağın adını belirtir. Sanal ağ ve güvenlik duvarı aynı kaynak grubuna ait olmalıdır.

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bölge
Güvenlik duvarının nereden gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork

### Microsoft. Azure. Commands. Network. model. Pspublicıpaddress []

### Microsoft. Azure. Commands. Network. model. Pspublicıpaddress

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
