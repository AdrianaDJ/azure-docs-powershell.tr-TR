---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 3b4014b56a36228fe53221430ffe79a43118f8fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937227"
---
# <span data-ttu-id="fb573-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fb573-101">New-AzFirewall</span></span>

## <span data-ttu-id="fb573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb573-102">SYNOPSIS</span></span>
<span data-ttu-id="fb573-103">Kaynak grubunda yeni bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="fb573-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb573-104">SYNTAX</span></span>

### <span data-ttu-id="fb573-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb573-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb573-106">Oldıda Configurationparametervalues</span><span class="sxs-lookup"><span data-stu-id="fb573-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb573-107">Ipconfigurationparametervalues değerleri</span><span class="sxs-lookup"><span data-stu-id="fb573-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb573-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb573-108">DESCRIPTION</span></span>
<span data-ttu-id="fb573-109">**New-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="fb573-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb573-110">EXAMPLES</span></span>

### <span data-ttu-id="fb573-111">1: sanal ağa bağlı bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb573-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="fb573-112">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="fb573-113">Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).</span><span class="sxs-lookup"><span data-stu-id="fb573-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="fb573-114">Ayrıca, Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda da çalışır.</span><span class="sxs-lookup"><span data-stu-id="fb573-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="fb573-115">2: tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturun</span><span class="sxs-lookup"><span data-stu-id="fb573-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="fb573-116">Bu örnek, bağlantı noktası 443 ' de tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="fb573-117">Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda çalışır.</span><span class="sxs-lookup"><span data-stu-id="fb573-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="fb573-118">3: VSEÇNAT-10.1.2.3 adresine yönlendirilen trafiği yeniden yönlendir: 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="fb573-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="fb573-119">Bu örnek, 10.1.2.3 adresine giden tüm paketlerin hedef IP ve bağlantı noktasını çeviren bir güvenlik duvarı oluşturmuştur, bu örnekte 10.2.3.4:8080 tehdit Intel kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="fb573-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="fb573-120">4: kural olmadan ve sorun durumunda Intel ile güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb573-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="fb573-121">Bu örnek, tüm trafiği (varsayılan davranış) engelleyen ve uyarı modunda çalışan tehdit Intel 'e sahip bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="fb573-122">Bu, diğer kuralların uygulanması (Bu örnekte yalnızca varsayılan kural) uygulanmadan önce kötü amaçlı trafik için uyarı günlüklerinin Yayınlanma anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="fb573-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="fb573-123">5: bağlantı noktası 8080 ' da tüm HTTP trafiğine izin veren ancak tehdit Intel tarafından tanımlanan kötü amaçlı etki alanlarını engeller</span><span class="sxs-lookup"><span data-stu-id="fb573-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="fb573-124">Bu örnek, 8080 iş parçacığı tarafından kötü niyetli olarak kabul edilmedikçe, bağlantı noktası üzerindeki tüm HTTP trafiğinin güvenlik duvarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="fb573-125">Engelleme modunda çalışırken, uyarıdan farklı olarak, tehdit ile kötü amaçlı olan trafik yalnızca günlüğe kaydedilmez, ancak engellenmiş olur.</span><span class="sxs-lookup"><span data-stu-id="fb573-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="fb573-126">6: kural olmadan ve kullanılabilirlik bölgeleriyle güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb573-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="fb573-127">Bu örnekte, kullanılabilir tüm kullanılabilirlik bölgeleri içeren bir güvenlik duvarı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fb573-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="fb573-128">7: iki veya daha çok ortak IP adresi içeren bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb573-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="fb573-129">Bu örnek, iki genel IP adresi olan "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="fb573-130">8: belirli SQL veritabanıyla MSSQL trafiğine izin veren bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb573-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="fb573-131">Bu örnek, 1433 için standart bağlantı noktası MSSQL trafiğine izin veren bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="fb573-132">9: sanal hub 'a bağlı bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb573-132">9:  Create a Firewall attached to a virtual hub</span></span>
```
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="fb573-133">Bu örnek, "vHub" sanal hub 'ına bağlı bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="fb573-134">Güvenlik duvarına bir güvenlik duvarı ilkesi $fp eklenir.</span><span class="sxs-lookup"><span data-stu-id="fb573-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="fb573-135">Bu güvenlik duvarı, güvenlik duvarı $fp ilkesinde belirtilen kurallara dayalı olarak trafiğe izin verir/reddeder.</span><span class="sxs-lookup"><span data-stu-id="fb573-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="fb573-136">Sanal hub ve güvenlik duvarı aynı bölgede olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fb573-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="fb573-137">10: tehdit zek</span><span class="sxs-lookup"><span data-stu-id="fb573-137">10: Create a Firewall with threat intelligence whitelist setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="fb573-138">Bu örnek, tehdit zekkarşı "www.microsoft.com" ve "8.8.8.8" gibi beyaz bir liste oluşturur</span><span class="sxs-lookup"><span data-stu-id="fb573-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="fb573-139">11: özelleştirilmiş özel Aralık kurulumuyla bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb573-139">11: Create a Firewall with customized private range setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="fb573-140">Bu örnekte, "99.99.99.0/24" ve "66.66.0.0/16" özel IP aralığı olarak ele</span><span class="sxs-lookup"><span data-stu-id="fb573-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="fb573-141">12: Yönetim alt ağı ve genel IP adresiyle güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb573-141">12:  Create a Firewall with a management subnet and Public IP address</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="fb573-142">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="fb573-143">Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).</span><span class="sxs-lookup"><span data-stu-id="fb573-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="fb573-144">Ayrıca, Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda da çalışır.</span><span class="sxs-lookup"><span data-stu-id="fb573-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="fb573-145">"Zorunlu tünel" senaryolarını desteklemek için, bu güvenlik duvarı "AzureFirewallManagementSubnet" alt ağını ve yönetim trafiği için yönetim genel IP adresini kullanır</span><span class="sxs-lookup"><span data-stu-id="fb573-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="fb573-146">13: sanal ağa güvenlik duvarı Ilkesiyle ilişkili bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb573-146">13:  Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="fb573-147">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb573-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="fb573-148">Güvenlik duvarına uygulanacak kurallar ve tehdit bilgileri güvenlik duvarı ilkesinden alınır</span><span class="sxs-lookup"><span data-stu-id="fb573-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

## <span data-ttu-id="fb573-149">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb573-149">PARAMETERS</span></span>

### <span data-ttu-id="fb573-150">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fb573-150">-ApplicationRuleCollection</span></span>
<span data-ttu-id="fb573-151">Yeni güvenlik duvarının uygulama kuralları koleksiyonlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb573-151">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="fb573-152">-Iş</span><span class="sxs-lookup"><span data-stu-id="fb573-152">-AsJob</span></span>
<span data-ttu-id="fb573-153">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fb573-153">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb573-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb573-154">-DefaultProfile</span></span>
<span data-ttu-id="fb573-155">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb573-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb573-156">-Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="fb573-156">-FirewallPolicyId</span></span>
<span data-ttu-id="fb573-157">Güvenlik duvarına bağlı güvenlik duvarı ilkesi</span><span class="sxs-lookup"><span data-stu-id="fb573-157">The firewall policy attached to the firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-158">-Force</span><span class="sxs-lookup"><span data-stu-id="fb573-158">-Force</span></span>
<span data-ttu-id="fb573-159">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fb573-159">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb573-160">-Konum</span><span class="sxs-lookup"><span data-stu-id="fb573-160">-Location</span></span>
<span data-ttu-id="fb573-161">Güvenlik duvarının bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb573-161">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="fb573-162">-Managementpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="fb573-162">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="fb573-163">Yönetim trafiği için kullanılacak bir veya birden çok ortak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="fb573-163">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="fb573-164">Genel IP adresleri standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fb573-164">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-165">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb573-165">-Name</span></span>
<span data-ttu-id="fb573-166">Bu cmdlet 'in oluşturduğu Azure Güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb573-166">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fb573-167">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fb573-167">-NatRuleCollection</span></span>
<span data-ttu-id="fb573-168">AzureFirewallNatRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="fb573-168">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="fb573-169">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fb573-169">-NetworkRuleCollection</span></span>
<span data-ttu-id="fb573-170">AzureFirewallNetworkRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="fb573-170">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="fb573-171">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="fb573-171">-PrivateRange</span></span>
<span data-ttu-id="fb573-172">Trafiğin eşitlenmeyeceği özel IP aralıkları</span><span class="sxs-lookup"><span data-stu-id="fb573-172">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="fb573-173">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="fb573-173">-PublicIpAddress</span></span>
<span data-ttu-id="fb573-174">Bir veya daha fazla ortak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="fb573-174">One or more Public IP Addresses.</span></span> <span data-ttu-id="fb573-175">Genel IP adresleri standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fb573-175">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-176">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="fb573-176">-PublicIpName</span></span>
<span data-ttu-id="fb573-177">Genel IP adı.</span><span class="sxs-lookup"><span data-stu-id="fb573-177">Public Ip Name.</span></span> <span data-ttu-id="fb573-178">Genel IP standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fb573-178">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb573-179">-ResourceGroupName</span></span>
<span data-ttu-id="fb573-180">Güvenlik duvarını içerecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb573-180">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="fb573-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="fb573-181">-Sku</span></span>
<span data-ttu-id="fb573-182">Güvenlik Duvarı için SKU türü</span><span class="sxs-lookup"><span data-stu-id="fb573-182">The sku type for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-183">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fb573-183">-Tag</span></span>
<span data-ttu-id="fb573-184">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="fb573-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fb573-185">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="fb573-185">For example:</span></span>

<span data-ttu-id="fb573-186">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="fb573-186">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fb573-187">-Threatıntelmodu</span><span class="sxs-lookup"><span data-stu-id="fb573-187">-ThreatIntelMode</span></span>
<span data-ttu-id="fb573-188">Tehdit yönetim bilgileri için işlem modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb573-188">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="fb573-189">Varsayılan mod, kapalı değil uyarıdır.</span><span class="sxs-lookup"><span data-stu-id="fb573-189">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-190">-Threatıntelwhitelist</span><span class="sxs-lookup"><span data-stu-id="fb573-190">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="fb573-191">Tehdit yönetim bilgileri için beyaz liste</span><span class="sxs-lookup"><span data-stu-id="fb573-191">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-192">-Virtualhubıd</span><span class="sxs-lookup"><span data-stu-id="fb573-192">-VirtualHubId</span></span>
<span data-ttu-id="fb573-193">Güvenlik duvarının bağlı olduğu sanal hub</span><span class="sxs-lookup"><span data-stu-id="fb573-193">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-194">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb573-194">-VirtualNetwork</span></span>
<span data-ttu-id="fb573-195">Sanal ağ</span><span class="sxs-lookup"><span data-stu-id="fb573-195">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-196">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fb573-196">-VirtualNetworkName</span></span>
<span data-ttu-id="fb573-197">Güvenlik duvarının dağıtılacağı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb573-197">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="fb573-198">Sanal ağ ve güvenlik duvarı aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fb573-198">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb573-199">-Bölge</span><span class="sxs-lookup"><span data-stu-id="fb573-199">-Zone</span></span>
<span data-ttu-id="fb573-200">Güvenlik duvarının nereden gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="fb573-200">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="fb573-201">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb573-201">-Confirm</span></span>
<span data-ttu-id="fb573-202">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb573-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb573-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb573-203">-WhatIf</span></span>
<span data-ttu-id="fb573-204">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb573-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb573-205">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb573-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb573-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb573-206">CommonParameters</span></span>
<span data-ttu-id="fb573-207">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb573-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb573-208">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb573-208">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb573-209">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb573-209">INPUTS</span></span>

### <span data-ttu-id="fb573-210">System. String</span><span class="sxs-lookup"><span data-stu-id="fb573-210">System.String</span></span>

### <span data-ttu-id="fb573-211">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fb573-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="fb573-212">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress []</span><span class="sxs-lookup"><span data-stu-id="fb573-212">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="fb573-213">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="fb573-213">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="fb573-214">Microsoft. Azure. Commands. Network. model. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="fb573-214">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="fb573-215">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="fb573-215">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="fb573-216">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="fb573-216">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="fb573-217">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb573-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fb573-218">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb573-218">OUTPUTS</span></span>

### <span data-ttu-id="fb573-219">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fb573-219">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="fb573-220">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb573-220">NOTES</span></span>

## <span data-ttu-id="fb573-221">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb573-221">RELATED LINKS</span></span>

[<span data-ttu-id="fb573-222">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fb573-222">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="fb573-223">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fb573-223">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="fb573-224">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="fb573-224">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="fb573-225">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fb573-225">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="fb573-226">Yeni-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fb573-226">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="fb573-227">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fb573-227">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
