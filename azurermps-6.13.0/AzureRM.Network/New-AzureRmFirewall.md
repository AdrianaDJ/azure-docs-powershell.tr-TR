---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewall.md
ms.openlocfilehash: 6486c7db87e8c71b0703b90a765fa30287b82769
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594378"
---
# <span data-ttu-id="e870c-101">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e870c-101">New-AzureRmFirewall</span></span>

## <span data-ttu-id="e870c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e870c-102">SYNOPSIS</span></span>
<span data-ttu-id="e870c-103">Kaynak grubunda yeni bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e870c-103">Creates a new Firewall in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e870c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e870c-104">SYNTAX</span></span>

```
New-AzureRmFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-VirtualNetworkName <String>] [-PublicIpName <String>]
 [-ApplicationRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]>]
 [-NatRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]>]
 [-NetworkRuleCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e870c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e870c-105">DESCRIPTION</span></span>
<span data-ttu-id="e870c-106">**Yeni-AzureRmFirewall** cmdlet 'ı bir Azure Güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e870c-106">The **New-AzureRmFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="e870c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e870c-107">EXAMPLES</span></span>

### <span data-ttu-id="e870c-108">1: sanal ağa bağlı bir güvenlik duvarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e870c-108">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="e870c-109">Bu örnek, güvenlik duvarıyla aynı kaynak grubundaki "VNET" sanal ağına eklenmiş bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e870c-109">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="e870c-110">Kural belirtilmediğinden, güvenlik duvarı tüm trafiği engeller (varsayılan davranış).</span><span class="sxs-lookup"><span data-stu-id="e870c-110">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>

### <span data-ttu-id="e870c-111">2: tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturun</span><span class="sxs-lookup"><span data-stu-id="e870c-111">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="e870c-112">Bu örnek, bağlantı noktası 443 ' de tüm HTTPS trafiğine izin veren bir güvenlik duvarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e870c-112">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>

### <span data-ttu-id="e870c-113">3: VSEÇNAT-10.1.2.3 adresine yönlendirilen trafiği yeniden yönlendir: 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="e870c-113">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection
```

<span data-ttu-id="e870c-114">Bu örnek, 10.1.2.3 adresine gelen tüm paketlerin hedef IP ve bağlantı noktasını çeviren bir güvenlik duvarı oluşturmuştur, 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="e870c-114">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>

## <span data-ttu-id="e870c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e870c-115">PARAMETERS</span></span>

### <span data-ttu-id="e870c-116">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e870c-116">-ApplicationRuleCollection</span></span>
<span data-ttu-id="e870c-117">Yeni güvenlik duvarının uygulama kuralları koleksiyonlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e870c-117">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e870c-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="e870c-118">-AsJob</span></span>
<span data-ttu-id="e870c-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e870c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e870c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e870c-120">-DefaultProfile</span></span>
<span data-ttu-id="e870c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e870c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e870c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e870c-122">-Force</span></span>
<span data-ttu-id="e870c-123">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e870c-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e870c-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="e870c-124">-Location</span></span>
<span data-ttu-id="e870c-125">Güvenlik duvarının bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e870c-125">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="e870c-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="e870c-126">-Name</span></span>
<span data-ttu-id="e870c-127">Bu cmdlet 'in oluşturduğu Azure Güvenlik duvarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e870c-127">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e870c-128">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e870c-128">-NatRuleCollection</span></span>
<span data-ttu-id="e870c-129">AzureFirewallNatRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="e870c-129">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e870c-130">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e870c-130">-NetworkRuleCollection</span></span>
<span data-ttu-id="e870c-131">AzureFirewallNetworkRuleCollections listesi</span><span class="sxs-lookup"><span data-stu-id="e870c-131">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e870c-132">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="e870c-132">-PublicIpName</span></span>
<span data-ttu-id="e870c-133">Genel IP adı.</span><span class="sxs-lookup"><span data-stu-id="e870c-133">Public Ip Name.</span></span> <span data-ttu-id="e870c-134">Genel IP standart SKU 'YU kullanmalıdır ve güvenlik duvarıyla aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e870c-134">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="e870c-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e870c-135">-ResourceGroupName</span></span>
<span data-ttu-id="e870c-136">Güvenlik duvarını içerecek kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e870c-136">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="e870c-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e870c-137">-Tag</span></span>
<span data-ttu-id="e870c-138">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e870c-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e870c-139">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="e870c-139">For example:</span></span>

<span data-ttu-id="e870c-140">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e870c-140">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e870c-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e870c-141">-VirtualNetworkName</span></span>
<span data-ttu-id="e870c-142">Güvenlik duvarının dağıtılacağı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e870c-142">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="e870c-143">Sanal ağ ve güvenlik duvarı aynı kaynak grubuna ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e870c-143">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="e870c-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="e870c-144">-Confirm</span></span>
<span data-ttu-id="e870c-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e870c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e870c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e870c-146">-WhatIf</span></span>
<span data-ttu-id="e870c-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e870c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e870c-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e870c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e870c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e870c-149">CommonParameters</span></span>
<span data-ttu-id="e870c-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e870c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e870c-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e870c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e870c-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e870c-152">INPUTS</span></span>

### <span data-ttu-id="e870c-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e870c-153">None</span></span>
<span data-ttu-id="e870c-154">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e870c-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e870c-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e870c-155">OUTPUTS</span></span>

### <span data-ttu-id="e870c-156">Microsoft. Azure. Commands. Network. modeller. PSFirewall</span><span class="sxs-lookup"><span data-stu-id="e870c-156">Microsoft.Azure.Commands.Network.Models.PSFirewall</span></span>

## <span data-ttu-id="e870c-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e870c-157">NOTES</span></span>

## <span data-ttu-id="e870c-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e870c-158">RELATED LINKS</span></span>

[<span data-ttu-id="e870c-159">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e870c-159">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="e870c-160">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e870c-160">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="e870c-161">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e870c-161">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)

[<span data-ttu-id="e870c-162">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e870c-162">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="e870c-163">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e870c-163">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="e870c-164">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e870c-164">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)
