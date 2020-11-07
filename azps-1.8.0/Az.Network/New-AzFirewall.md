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
# <span data-ttu-id="684fa-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="684fa-101">New-AzFirewall</span></span>

## <span data-ttu-id="684fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="684fa-102">SYNOPSIS</span></span>
<span data-ttu-id="684fa-103">Kaynak grubunda yeni bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="684fa-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="684fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="684fa-104">SYNTAX</span></span>

### <span data-ttu-id="684fa-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="684fa-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="684fa-106">Ipconfigurationparametervalues değerleri</span><span class="sxs-lookup"><span data-stu-id="684fa-106">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="684fa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="684fa-107">DESCRIPTION</span></span>
<span data-ttu-id="684fa-108">**New-AzFirewall** cmdlet 'ı bir Azure Güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="684fa-108">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="684fa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="684fa-109">EXAMPLES</span></span>

### <span data-ttu-id="684fa-110">1: sanal ağa bağlı bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="684fa-110">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="684fa-111">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="684fa-111">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="684fa-112">Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).</span><span class="sxs-lookup"><span data-stu-id="684fa-112">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="684fa-113">Ayrıca, Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda da çalışır.</span><span class="sxs-lookup"><span data-stu-id="684fa-113">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="684fa-114">2: tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturun</span><span class="sxs-lookup"><span data-stu-id="684fa-114">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="684fa-115">Bu örnek, bağlantı noktası 443 ' de tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="684fa-115">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="684fa-116">Intel, kötü amaçlı trafiğin günlüğe kaydedilmesini, ancak reddedilemeyecek anlamına gelen varsayılan modda çalışır.</span><span class="sxs-lookup"><span data-stu-id="684fa-116">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="684fa-117">3: VSEÇNAT-10.1.2.3 adresine yönlendirilen trafiği yeniden yönlendir: 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="684fa-117">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="684fa-118">Bu örnek, 10.1.2.3 adresine giden tüm paketlerin hedef IP ve bağlantı noktasını çeviren bir güvenlik duvarı oluşturmuştur, bu örnekte 10.2.3.4:8080 tehdit Intel kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="684fa-118">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="684fa-119">4: kural olmadan ve sorun durumunda Intel ile güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="684fa-119">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

<span data-ttu-id="684fa-120">Bu örnek, tüm trafiği (varsayılan davranış) engelleyen ve uyarı modunda çalışan tehdit Intel 'e sahip bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="684fa-120">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="684fa-121">Bu, diğer kuralların uygulanması (Bu örnekte yalnızca varsayılan kural) uygulanmadan önce kötü amaçlı trafik için uyarı günlüklerinin Yayınlanma anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="684fa-121">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="684fa-122">5: bağlantı noktası 8080 ' da tüm HTTP trafiğine izin veren ancak tehdit Intel tarafından tanımlanan kötü amaçlı etki alanlarını engeller</span><span class="sxs-lookup"><span data-stu-id="684fa-122">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="684fa-123">Bu örnek, 8080 iş parçacığı tarafından kötü niyetli olarak kabul edilmedikçe, bağlantı noktası üzerindeki tüm HTTP trafiğinin güvenlik duvarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="684fa-123">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="684fa-124">Engelleme modunda çalışırken, uyarıdan farklı olarak, tehdit ile kötü amaçlı olan trafik yalnızca günlüğe kaydedilmez, ancak engellenmiş olur.</span><span class="sxs-lookup"><span data-stu-id="684fa-124">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

## <span data-ttu-id="684fa-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="684fa-125">PARAMETERS</span></span>

### <span data-ttu-id="684fa-126">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="684fa-126">-ApplicationRuleCollection</span></span>
<span data-ttu-id="684fa-127">Yeni güvenlik duvarının uygulama kuralları koleksiyonlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="684fa-127">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="684fa-128">-Iş</span><span class="sxs-lookup"><span data-stu-id="684fa-128">-AsJob</span></span>
<span data-ttu-id="684fa-129">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="684fa-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="684fa-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684fa-130">-DefaultProfile</span></span>
<span data-ttu-id="684fa-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="684fa-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="684fa-132">-Force</span><span class="sxs-lookup"><span data-stu-id="684fa-132">-Force</span></span>
<span data-ttu-id="684fa-133">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="684fa-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="684fa-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="684fa-134">-Location</span></span>
<span data-ttu-id="684fa-135">Güvenlik duvarının bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="684fa-135">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="684fa-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="684fa-136">-Name</span></span>
<span data-ttu-id="684fa-137">Bu cmdlet 'in oluşturduğu Azure Güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="684fa-137">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="684fa-138">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="684fa-138">-NatRuleCollection</span></span>
<span data-ttu-id="684fa-139">AzureFirewallNatRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="684fa-139">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="684fa-140">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="684fa-140">-NetworkRuleCollection</span></span>
<span data-ttu-id="684fa-141">AzureFirewallNetworkRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="684fa-141">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="684fa-142">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="684fa-142">-PublicIpName</span></span>
<span data-ttu-id="684fa-143">Genel IP adı.</span><span class="sxs-lookup"><span data-stu-id="684fa-143">Public Ip Name.</span></span> <span data-ttu-id="684fa-144">Genel IP standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="684fa-144">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="684fa-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684fa-145">-ResourceGroupName</span></span>
<span data-ttu-id="684fa-146">Güvenlik duvarını içerecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="684fa-146">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="684fa-147">Etiketli</span><span class="sxs-lookup"><span data-stu-id="684fa-147">-Tag</span></span>
<span data-ttu-id="684fa-148">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="684fa-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="684fa-149">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="684fa-149">For example:</span></span>

<span data-ttu-id="684fa-150">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="684fa-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="684fa-151">-Threatıntelmodu</span><span class="sxs-lookup"><span data-stu-id="684fa-151">-ThreatIntelMode</span></span>
<span data-ttu-id="684fa-152">Tehdit yönetim bilgileri için işlem modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="684fa-152">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="684fa-153">Varsayılan mod, kapalı değil uyarıdır.</span><span class="sxs-lookup"><span data-stu-id="684fa-153">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="684fa-154">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="684fa-154">-VirtualNetworkName</span></span>
<span data-ttu-id="684fa-155">Güvenlik duvarının dağıtılacağı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="684fa-155">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="684fa-156">Sanal ağ ve güvenlik duvarı aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="684fa-156">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="684fa-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="684fa-157">-Confirm</span></span>
<span data-ttu-id="684fa-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="684fa-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="684fa-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="684fa-159">-WhatIf</span></span>
<span data-ttu-id="684fa-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="684fa-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="684fa-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="684fa-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="684fa-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684fa-162">CommonParameters</span></span>
<span data-ttu-id="684fa-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="684fa-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684fa-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="684fa-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684fa-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="684fa-165">INPUTS</span></span>

### <span data-ttu-id="684fa-166">System. String</span><span class="sxs-lookup"><span data-stu-id="684fa-166">System.String</span></span>

### <span data-ttu-id="684fa-167">Microsoft. Azure. Commands. Network. model. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="684fa-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="684fa-168">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="684fa-168">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="684fa-169">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="684fa-169">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="684fa-170">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="684fa-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="684fa-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="684fa-171">OUTPUTS</span></span>

### <span data-ttu-id="684fa-172">Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="684fa-172">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="684fa-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="684fa-173">NOTES</span></span>

## <span data-ttu-id="684fa-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="684fa-174">RELATED LINKS</span></span>

[<span data-ttu-id="684fa-175">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="684fa-175">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="684fa-176">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="684fa-176">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="684fa-177">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="684fa-177">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="684fa-178">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="684fa-178">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="684fa-179">Yeni-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="684fa-179">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="684fa-180">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="684fa-180">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
