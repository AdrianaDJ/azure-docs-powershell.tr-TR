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
# <span data-ttu-id="ed5c3-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ed5c3-101">New-AzFirewall</span></span>

## <span data-ttu-id="ed5c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5c3-103">Kaynak grubunda yeni bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="ed5c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed5c3-104">SYNTAX</span></span>

### <span data-ttu-id="ed5c3-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed5c3-105">Default (Default)</span></span>
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

### <span data-ttu-id="ed5c3-106">Oldıda Configurationparametervalues</span><span class="sxs-lookup"><span data-stu-id="ed5c3-106">OldIpConfigurationParameterValues</span></span>
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

### <span data-ttu-id="ed5c3-107">Ipconfigurationparametervalues değerleri</span><span class="sxs-lookup"><span data-stu-id="ed5c3-107">IpConfigurationParameterValues</span></span>
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

## <span data-ttu-id="ed5c3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed5c3-108">DESCRIPTION</span></span>
<span data-ttu-id="ed5c3-109">**New-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="ed5c3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed5c3-110">EXAMPLES</span></span>

### <span data-ttu-id="ed5c3-111">Örnek 1: sanal ağa bağlı bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="ed5c3-112">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ed5c3-113">Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).</span><span class="sxs-lookup"><span data-stu-id="ed5c3-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="ed5c3-114">Ayrıca, Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda da çalışır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="ed5c3-115">Örnek 2: tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="ed5c3-116">Bu örnek, bağlantı noktası 443 ' de tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="ed5c3-117">Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda çalışır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="ed5c3-118">Örnek 3: VSEÇNAT-10.1.2.3 'e yönlendirilen trafiği yeniden yönlendir: 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="ed5c3-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="ed5c3-119">Bu örnek, 10.1.2.3 adresine giden tüm paketlerin hedef IP ve bağlantı noktasını çeviren bir güvenlik duvarı oluşturmuştur, bu örnekte 10.2.3.4:8080 tehdit Intel kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="ed5c3-120">Örnek 4: kural olmadan ve iş arkadaşlarınızla Intel uyarı modunda güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="ed5c3-121">Bu örnek, tüm trafiği (varsayılan davranış) engelleyen ve uyarı modunda çalışan tehdit Intel 'e sahip bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="ed5c3-122">Bu, diğer kuralların uygulanması (Bu örnekte yalnızca varsayılan kural) uygulanmadan önce kötü amaçlı trafik için uyarı günlüklerinin Yayınlanma anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="ed5c3-123">Örnek 5: bağlantı noktası 8080 ' da tüm HTTP trafiğine izin veren ancak tehdit Intel tarafından tanımlanan kötü amaçlı etki alanlarını engeller</span><span class="sxs-lookup"><span data-stu-id="ed5c3-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="ed5c3-124">Bu örnek, 8080 iş parçacığı tarafından kötü niyetli olarak kabul edilmedikçe, bağlantı noktası üzerindeki tüm HTTP trafiğinin güvenlik duvarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="ed5c3-125">Engelleme modunda çalışırken, uyarıdan farklı olarak, tehdit ile kötü amaçlı olan trafik yalnızca günlüğe kaydedilmez, ancak engellenmiş olur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="ed5c3-126">Örnek 6: kural olmadan ve kullanılabilirlik bölgeleriyle güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="ed5c3-127">Bu örnekte, kullanılabilir tüm kullanılabilirlik bölgeleri içeren bir güvenlik duvarı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="ed5c3-128">Örnek 7: iki veya daha çok ortak IP adresi içeren bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="ed5c3-129">Bu örnek, iki genel IP adresi olan "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="ed5c3-130">Örnek 8: belirli SQL veritabanıyla MSSQL trafiğine izin veren bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="ed5c3-131">Bu örnek, 1433 için standart bağlantı noktası MSSQL trafiğine izin veren bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="ed5c3-132">Örnek 9: sanal hub 'a bağlı bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="ed5c3-133">Bu örnek, "vHub" sanal hub 'ına bağlı bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="ed5c3-134">Güvenlik duvarına bir güvenlik duvarı ilkesi $fp eklenir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="ed5c3-135">Bu güvenlik duvarı, güvenlik duvarı $fp ilkesinde belirtilen kurallara dayalı olarak trafiğe izin verir/reddeder.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="ed5c3-136">Sanal hub ve güvenlik duvarı aynı bölgede olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="ed5c3-137">Örnek 10: tehdit zek</span><span class="sxs-lookup"><span data-stu-id="ed5c3-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="ed5c3-138">Bu örnek, tehdit zekkarşı "www.microsoft.com" ve "8.8.8.8" gibi beyaz bir liste oluşturur</span><span class="sxs-lookup"><span data-stu-id="ed5c3-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="ed5c3-139">Örnek 11: özelleştirilmiş özel Aralık kurulumuyla bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="ed5c3-140">Bu örnekte, "99.99.99.0/24" ve "66.66.0.0/16" özel IP aralığı olarak ele</span><span class="sxs-lookup"><span data-stu-id="ed5c3-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="ed5c3-141">Örnek 12: Yönetim alt ağı ve genel IP adresiyle güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="ed5c3-142">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ed5c3-143">Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).</span><span class="sxs-lookup"><span data-stu-id="ed5c3-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="ed5c3-144">Ayrıca, Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda da çalışır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="ed5c3-145">"Zorunlu tünel" senaryolarını desteklemek için, bu güvenlik duvarı "AzureFirewallManagementSubnet" alt ağını ve yönetim trafiği için yönetim genel IP adresini kullanır</span><span class="sxs-lookup"><span data-stu-id="ed5c3-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="ed5c3-146">Örnek 13: sanal ağa güvenlik duvarı Ilkesiyle ilişkili bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="ed5c3-147">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ed5c3-148">Güvenlik duvarına uygulanacak kurallar ve tehdit bilgileri güvenlik duvarı ilkesinden alınır</span><span class="sxs-lookup"><span data-stu-id="ed5c3-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="ed5c3-149">Örnek 14: DNS proxy 'Si ve DNS sunucularıyla güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ed5c3-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="ed5c3-150">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ed5c3-151">DNS proxy bu güvenlik duvarı için etkinleştirildi ve 2 DNS sunucusu sağlanır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="ed5c3-152">Ayrıca ağ kuralları için DNS proxy ıste, FQDN içeren ağ kuralları varsa, DNS proxy 'si de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="ed5c3-153">Örnek 15: birden çok IP içeren bir güvenlik duvarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="ed5c3-154">Güvenlik Duvarı sanal hub ile ilişkilendirilebilir</span><span class="sxs-lookup"><span data-stu-id="ed5c3-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -Sku AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="ed5c3-155">Bu örnekte, güvenlik duvarıyla aynı kaynak grubunda sanal hub 'a bağlı bir güvenlik duvarı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ed5c3-156">Güvenlik duvarına, örtük olarak oluşturulan 2 genel IP 'Ler atanır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="ed5c3-157">16: etkin FTP 'ye Izin veren bir güvenlik duvarı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="ed5c3-158">Bu örnek, etkin FTP bayrağı olan bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="ed5c3-159">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed5c3-159">PARAMETERS</span></span>

### <span data-ttu-id="ed5c3-160">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ed5c3-160">-ApplicationRuleCollection</span></span>
<span data-ttu-id="ed5c3-161">Yeni güvenlik duvarının uygulama kuralları koleksiyonlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-161">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="ed5c3-162">-Iş</span><span class="sxs-lookup"><span data-stu-id="ed5c3-162">-AsJob</span></span>
<span data-ttu-id="ed5c3-163">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ed5c3-163">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed5c3-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5c3-164">-DefaultProfile</span></span>
<span data-ttu-id="ed5c3-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed5c3-166">-DnsProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ed5c3-166">-DnsProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="ed5c3-167">Ağ kuralları içinde FQDN 'Ler için DNS proxy işlevleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-167">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>

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

### <span data-ttu-id="ed5c3-168">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="ed5c3-168">-DnsServer</span></span>
<span data-ttu-id="ed5c3-169">DNS çözümlemesi için kullanılacak DNS sunucularının listesi</span><span class="sxs-lookup"><span data-stu-id="ed5c3-169">The list of DNS Servers to be used for DNS resolution,</span></span>

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

### <span data-ttu-id="ed5c3-170">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="ed5c3-170">-EnableDnsProxy</span></span>
<span data-ttu-id="ed5c3-171">DNS proxy 'yi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-171">Enable DNS Proxy.</span></span> <span data-ttu-id="ed5c3-172">Varsayılan olarak devre dışıdır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-172">By default it is disabled.</span></span>


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

### <span data-ttu-id="ed5c3-173">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="ed5c3-173">-AllowActiveFTP</span></span>
<span data-ttu-id="ed5c3-174">Güvenlik duvarında etkin FTP 'ye izin verir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-174">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="ed5c3-175">Varsayılan olarak devre dışıdır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-175">By default it is disabled.</span></span>


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

### <span data-ttu-id="ed5c3-176">-Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="ed5c3-176">-FirewallPolicyId</span></span>
<span data-ttu-id="ed5c3-177">Güvenlik duvarına bağlı güvenlik duvarı ilkesi</span><span class="sxs-lookup"><span data-stu-id="ed5c3-177">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="ed5c3-178">-Force</span><span class="sxs-lookup"><span data-stu-id="ed5c3-178">-Force</span></span>
<span data-ttu-id="ed5c3-179">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-179">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed5c3-180">-Hubıpaddresses</span><span class="sxs-lookup"><span data-stu-id="ed5c3-180">-HubIPAddresses</span></span>
<span data-ttu-id="ed5c3-181">Sanal hub 'a bağlı güvenlik duvarının IP adresleri</span><span class="sxs-lookup"><span data-stu-id="ed5c3-181">The ip addresses for the firewall attached to a virtual hub</span></span>

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

### <span data-ttu-id="ed5c3-182">-Konum</span><span class="sxs-lookup"><span data-stu-id="ed5c3-182">-Location</span></span>
<span data-ttu-id="ed5c3-183">Güvenlik duvarının bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-183">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="ed5c3-184">-Managementpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ed5c3-184">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="ed5c3-185">Yönetim trafiği için kullanılacak bir veya birden çok ortak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-185">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="ed5c3-186">Genel IP adresleri standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-186">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="ed5c3-187">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed5c3-187">-Name</span></span>
<span data-ttu-id="ed5c3-188">Bu cmdlet 'in oluşturduğu Azure Güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-188">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ed5c3-189">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ed5c3-189">-NatRuleCollection</span></span>
<span data-ttu-id="ed5c3-190">AzureFirewallNatRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="ed5c3-190">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="ed5c3-191">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ed5c3-191">-NetworkRuleCollection</span></span>
<span data-ttu-id="ed5c3-192">AzureFirewallNetworkRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="ed5c3-192">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="ed5c3-193">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="ed5c3-193">-PrivateRange</span></span>
<span data-ttu-id="ed5c3-194">Trafiğin eşitlenmeyeceği özel IP aralıkları</span><span class="sxs-lookup"><span data-stu-id="ed5c3-194">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="ed5c3-195">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ed5c3-195">-PublicIpAddress</span></span>
<span data-ttu-id="ed5c3-196">Bir veya daha fazla ortak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-196">One or more Public IP Addresses.</span></span> <span data-ttu-id="ed5c3-197">Genel IP adresleri standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-197">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="ed5c3-198">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="ed5c3-198">-PublicIpName</span></span>
<span data-ttu-id="ed5c3-199">Genel IP adı.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-199">Public Ip Name.</span></span> <span data-ttu-id="ed5c3-200">Genel IP standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-200">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="ed5c3-201">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5c3-201">-ResourceGroupName</span></span>
<span data-ttu-id="ed5c3-202">Güvenlik duvarını içerecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-202">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="ed5c3-203">-SKU</span><span class="sxs-lookup"><span data-stu-id="ed5c3-203">-Sku</span></span>
<span data-ttu-id="ed5c3-204">Güvenlik Duvarı için SKU türü</span><span class="sxs-lookup"><span data-stu-id="ed5c3-204">The sku type for firewall</span></span>

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

### <span data-ttu-id="ed5c3-205">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ed5c3-205">-Tag</span></span>
<span data-ttu-id="ed5c3-206">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ed5c3-207">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="ed5c3-207">For example:</span></span>

<span data-ttu-id="ed5c3-208">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="ed5c3-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ed5c3-209">-Threatıntelmodu</span><span class="sxs-lookup"><span data-stu-id="ed5c3-209">-ThreatIntelMode</span></span>
<span data-ttu-id="ed5c3-210">Tehdit yönetim bilgileri için işlem modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="ed5c3-211">Varsayılan mod, kapalı değil uyarıdır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-211">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="ed5c3-212">-Threatıntelwhitelist</span><span class="sxs-lookup"><span data-stu-id="ed5c3-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="ed5c3-213">Tehdit yönetim bilgileri için beyaz liste</span><span class="sxs-lookup"><span data-stu-id="ed5c3-213">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="ed5c3-214">-Virtualhubıd</span><span class="sxs-lookup"><span data-stu-id="ed5c3-214">-VirtualHubId</span></span>
<span data-ttu-id="ed5c3-215">Güvenlik duvarının bağlı olduğu sanal hub</span><span class="sxs-lookup"><span data-stu-id="ed5c3-215">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="ed5c3-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed5c3-216">-VirtualNetwork</span></span>
<span data-ttu-id="ed5c3-217">Sanal ağ</span><span class="sxs-lookup"><span data-stu-id="ed5c3-217">Virtual Network</span></span>

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

### <span data-ttu-id="ed5c3-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ed5c3-218">-VirtualNetworkName</span></span>
<span data-ttu-id="ed5c3-219">Güvenlik duvarının dağıtılacağı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="ed5c3-220">Sanal ağ ve güvenlik duvarı aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-220">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="ed5c3-221">-Bölge</span><span class="sxs-lookup"><span data-stu-id="ed5c3-221">-Zone</span></span>
<span data-ttu-id="ed5c3-222">Güvenlik duvarının nereden gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="ed5c3-223">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed5c3-223">-Confirm</span></span>
<span data-ttu-id="ed5c3-224">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5c3-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5c3-225">-WhatIf</span></span>
<span data-ttu-id="ed5c3-226">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed5c3-227">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed5c3-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5c3-228">CommonParameters</span></span>
<span data-ttu-id="ed5c3-229">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5c3-230">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed5c3-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5c3-231">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed5c3-231">INPUTS</span></span>

### <span data-ttu-id="ed5c3-232">System. String</span><span class="sxs-lookup"><span data-stu-id="ed5c3-232">System.String</span></span>

### <span data-ttu-id="ed5c3-233">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ed5c3-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="ed5c3-234">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress []</span><span class="sxs-lookup"><span data-stu-id="ed5c3-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="ed5c3-235">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="ed5c3-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="ed5c3-236">Microsoft. Azure. Commands. Network. model. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="ed5c3-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="ed5c3-237">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="ed5c3-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="ed5c3-238">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="ed5c3-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="ed5c3-239">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ed5c3-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ed5c3-240">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed5c3-240">OUTPUTS</span></span>

### <span data-ttu-id="ed5c3-241">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ed5c3-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="ed5c3-242">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed5c3-242">NOTES</span></span>

## <span data-ttu-id="ed5c3-243">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed5c3-243">RELATED LINKS</span></span>

[<span data-ttu-id="ed5c3-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ed5c3-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="ed5c3-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ed5c3-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="ed5c3-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ed5c3-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="ed5c3-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ed5c3-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="ed5c3-248">Yeni-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ed5c3-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="ed5c3-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ed5c3-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
