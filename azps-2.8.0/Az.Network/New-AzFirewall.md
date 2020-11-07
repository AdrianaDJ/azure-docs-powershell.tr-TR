---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918296"
---
# <span data-ttu-id="93e1c-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="93e1c-101">New-AzFirewall</span></span>

## <span data-ttu-id="93e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="93e1c-103">Kaynak grubunda yeni bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="93e1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93e1c-104">SYNTAX</span></span>

### <span data-ttu-id="93e1c-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="93e1c-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93e1c-106">Oldıda Configurationparametervalues</span><span class="sxs-lookup"><span data-stu-id="93e1c-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93e1c-107">Ipconfigurationparametervalues değerleri</span><span class="sxs-lookup"><span data-stu-id="93e1c-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93e1c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="93e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="93e1c-109">**New-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="93e1c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="93e1c-111">1: sanal ağa bağlı bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="93e1c-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="93e1c-112">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="93e1c-113">Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).</span><span class="sxs-lookup"><span data-stu-id="93e1c-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="93e1c-114">Ayrıca, Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda da çalışır.</span><span class="sxs-lookup"><span data-stu-id="93e1c-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="93e1c-115">2: tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturun</span><span class="sxs-lookup"><span data-stu-id="93e1c-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="93e1c-116">Bu örnek, bağlantı noktası 443 ' de tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="93e1c-117">Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda çalışır.</span><span class="sxs-lookup"><span data-stu-id="93e1c-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="93e1c-118">3: VSEÇNAT-10.1.2.3 adresine yönlendirilen trafiği yeniden yönlendir: 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="93e1c-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="93e1c-119">Bu örnek, 10.1.2.3 adresine giden tüm paketlerin hedef IP ve bağlantı noktasını çeviren bir güvenlik duvarı oluşturmuştur, bu örnekte 10.2.3.4:8080 tehdit Intel kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="93e1c-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="93e1c-120">4: kural olmadan ve sorun durumunda Intel ile güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="93e1c-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="93e1c-121">Bu örnek, tüm trafiği (varsayılan davranış) engelleyen ve uyarı modunda çalışan tehdit Intel 'e sahip bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="93e1c-122">Bu, diğer kuralların uygulanması (Bu örnekte yalnızca varsayılan kural) uygulanmadan önce kötü amaçlı trafik için uyarı günlüklerinin Yayınlanma anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="93e1c-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="93e1c-123">5: bağlantı noktası 8080 ' da tüm HTTP trafiğine izin veren ancak tehdit Intel tarafından tanımlanan kötü amaçlı etki alanlarını engeller</span><span class="sxs-lookup"><span data-stu-id="93e1c-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="93e1c-124">Bu örnek, 8080 iş parçacığı tarafından kötü niyetli olarak kabul edilmedikçe, bağlantı noktası üzerindeki tüm HTTP trafiğinin güvenlik duvarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="93e1c-125">Engelleme modunda çalışırken, uyarıdan farklı olarak, tehdit ile kötü amaçlı olan trafik yalnızca günlüğe kaydedilmez, ancak engellenmiş olur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="93e1c-126">6: kural olmadan ve kullanılabilirlik bölgeleriyle güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="93e1c-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="93e1c-127">Bu örnekte, kullanılabilir tüm kullanılabilirlik bölgeleri içeren bir güvenlik duvarı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="93e1c-128">7: iki veya daha çok ortak IP adresi içeren bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="93e1c-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="93e1c-129">Bu örnek, iki genel IP adresi olan "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="93e1c-130">8: belirli SQL veritabanıyla MSSQL trafiğine izin veren bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="93e1c-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="93e1c-131">Bu örnek, 1433 için standart bağlantı noktası MSSQL trafiğine izin veren bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="93e1c-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="93e1c-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93e1c-132">PARAMETERS</span></span>

### <span data-ttu-id="93e1c-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="93e1c-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="93e1c-134">Yeni güvenlik duvarının uygulama kuralları koleksiyonlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e1c-134">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="93e1c-135">-Iş</span><span class="sxs-lookup"><span data-stu-id="93e1c-135">-AsJob</span></span>
<span data-ttu-id="93e1c-136">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="93e1c-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93e1c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e1c-137">-DefaultProfile</span></span>
<span data-ttu-id="93e1c-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93e1c-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93e1c-139">-Force</span><span class="sxs-lookup"><span data-stu-id="93e1c-139">-Force</span></span>
<span data-ttu-id="93e1c-140">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="93e1c-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93e1c-141">-Konum</span><span class="sxs-lookup"><span data-stu-id="93e1c-141">-Location</span></span>
<span data-ttu-id="93e1c-142">Güvenlik duvarının bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e1c-142">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="93e1c-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="93e1c-143">-Name</span></span>
<span data-ttu-id="93e1c-144">Bu cmdlet 'in oluşturduğu Azure Güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e1c-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="93e1c-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="93e1c-145">-NatRuleCollection</span></span>
<span data-ttu-id="93e1c-146">AzureFirewallNatRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="93e1c-146">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="93e1c-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="93e1c-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="93e1c-148">AzureFirewallNetworkRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="93e1c-148">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="93e1c-149">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="93e1c-149">-PublicIpAddress</span></span>
<span data-ttu-id="93e1c-150">Bir veya daha fazla ortak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="93e1c-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="93e1c-151">Genel IP adresleri standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="93e1c-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="93e1c-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="93e1c-152">-PublicIpName</span></span>
<span data-ttu-id="93e1c-153">Genel IP adı.</span><span class="sxs-lookup"><span data-stu-id="93e1c-153">Public Ip Name.</span></span> <span data-ttu-id="93e1c-154">Genel IP standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="93e1c-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="93e1c-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e1c-155">-ResourceGroupName</span></span>
<span data-ttu-id="93e1c-156">Güvenlik duvarını içerecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e1c-156">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="93e1c-157">-Bölge</span><span class="sxs-lookup"><span data-stu-id="93e1c-157">-Zone</span></span>
<span data-ttu-id="93e1c-158">Güvenlik duvarının nereden gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="93e1c-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="93e1c-159">Etiketli</span><span class="sxs-lookup"><span data-stu-id="93e1c-159">-Tag</span></span>
<span data-ttu-id="93e1c-160">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="93e1c-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="93e1c-161">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="93e1c-161">For example:</span></span>

<span data-ttu-id="93e1c-162">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="93e1c-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="93e1c-163">-Threatıntelmodu</span><span class="sxs-lookup"><span data-stu-id="93e1c-163">-ThreatIntelMode</span></span>
<span data-ttu-id="93e1c-164">Tehdit yönetim bilgileri için işlem modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e1c-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="93e1c-165">Varsayılan mod, kapalı değil uyarıdır.</span><span class="sxs-lookup"><span data-stu-id="93e1c-165">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="93e1c-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="93e1c-166">-VirtualNetwork</span></span>
<span data-ttu-id="93e1c-167">Sanal ağ</span><span class="sxs-lookup"><span data-stu-id="93e1c-167">Virtual Network</span></span>

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

### <span data-ttu-id="93e1c-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="93e1c-168">-VirtualNetworkName</span></span>
<span data-ttu-id="93e1c-169">Güvenlik duvarının dağıtılacağı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="93e1c-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="93e1c-170">Sanal ağ ve güvenlik duvarı aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="93e1c-170">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="93e1c-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="93e1c-171">-Confirm</span></span>
<span data-ttu-id="93e1c-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="93e1c-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e1c-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e1c-173">-WhatIf</span></span>
<span data-ttu-id="93e1c-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="93e1c-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e1c-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="93e1c-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e1c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e1c-176">CommonParameters</span></span>
<span data-ttu-id="93e1c-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93e1c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e1c-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e1c-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e1c-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93e1c-179">INPUTS</span></span>

### <span data-ttu-id="93e1c-180">System. String</span><span class="sxs-lookup"><span data-stu-id="93e1c-180">System.String</span></span>

### <span data-ttu-id="93e1c-181">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="93e1c-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="93e1c-182">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress []</span><span class="sxs-lookup"><span data-stu-id="93e1c-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="93e1c-183">Microsoft. Azure. Commands. Network. model. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="93e1c-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="93e1c-184">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="93e1c-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="93e1c-185">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="93e1c-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="93e1c-186">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="93e1c-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="93e1c-187">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93e1c-187">OUTPUTS</span></span>

### <span data-ttu-id="93e1c-188">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="93e1c-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="93e1c-189">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93e1c-189">NOTES</span></span>

## <span data-ttu-id="93e1c-190">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93e1c-190">RELATED LINKS</span></span>

[<span data-ttu-id="93e1c-191">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="93e1c-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="93e1c-192">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="93e1c-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="93e1c-193">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="93e1c-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="93e1c-194">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="93e1c-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="93e1c-195">Yeni-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="93e1c-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="93e1c-196">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="93e1c-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
