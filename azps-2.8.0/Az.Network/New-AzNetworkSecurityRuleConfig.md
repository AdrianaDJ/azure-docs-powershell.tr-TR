---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: e3afa3ee5809af2760225be674990827c117bdfa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918231"
---
# <span data-ttu-id="859a4-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="859a4-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="859a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="859a4-102">SYNOPSIS</span></span>
<span data-ttu-id="859a4-103">Ağ güvenlik kuralı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="859a4-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="859a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="859a4-104">SYNTAX</span></span>

### <span data-ttu-id="859a4-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="859a4-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="859a4-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="859a4-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="859a4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="859a4-107">DESCRIPTION</span></span>
<span data-ttu-id="859a4-108">**Yeni-Azağsecurityruleconfig** cmdlet 'i, bir ağ güvenlik grubu Için bir Azure ağ güvenlik kuralı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="859a4-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="859a4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="859a4-109">EXAMPLES</span></span>

### <span data-ttu-id="859a4-110">1: RDP 'ye izin veren ağ güvenlik kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="859a4-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="859a4-111">Bu komut Internet 'ten bağlantı noktası 3389 'e erişim izni veren bir güvenlik kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="859a4-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="859a4-112">2: HTTP 'ye izin veren ağ güvenlik kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="859a4-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="859a4-113">Bu komut Internet 'ten bağlantı noktası 80 'e erişim izni veren bir güvenlik kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="859a4-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="859a4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="859a4-114">PARAMETERS</span></span>

### <span data-ttu-id="859a4-115">-Access</span><span class="sxs-lookup"><span data-stu-id="859a4-115">-Access</span></span>
<span data-ttu-id="859a4-116">Ağ trafiğine izin verilip verilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="859a4-117">Bu parametre için kabul edilebilir değerler: Izin ver ve Reddet.</span><span class="sxs-lookup"><span data-stu-id="859a4-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859a4-118">-DefaultProfile</span></span>
<span data-ttu-id="859a4-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="859a4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="859a4-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="859a4-120">-Description</span></span>
<span data-ttu-id="859a4-121">Oluşturulacak ağ güvenliği kuralı yapılandırmasının açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="859a4-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="859a4-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="859a4-123">Hedef adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="859a4-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="859a4-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="859a4-125">Sınıfsız Etki alanları arası yönlendirme (CıDR) adresi</span><span class="sxs-lookup"><span data-stu-id="859a4-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="859a4-126">Hedef IP adresi aralığı</span><span class="sxs-lookup"><span data-stu-id="859a4-126">A destination IP address range</span></span> 
- <span data-ttu-id="859a4-127">Herhangi bir IP adresiyle eşleşen bir joker karakter (\*), VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="859a4-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="859a4-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="859a4-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="859a4-129">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="859a4-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="859a4-130">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="859a4-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a4-131">-Destinationapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="859a4-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="859a4-132">Kural için hedef olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="859a4-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="859a4-133">' DestinationAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="859a4-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a4-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="859a4-134">-DestinationPortRange</span></span>
<span data-ttu-id="859a4-135">Hedef bir bağlantı noktası veya aralığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="859a4-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="859a4-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="859a4-137">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="859a4-137">An integer</span></span>
- <span data-ttu-id="859a4-138">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="859a4-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="859a4-139">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="859a4-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="859a4-140">-Yön</span><span class="sxs-lookup"><span data-stu-id="859a4-140">-Direction</span></span>
<span data-ttu-id="859a4-141">Kuralın gelen veya giden trafikte değerlendirilip değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="859a4-142">Bu parametre için kabul edilebilir değerler: gelen ve giden.</span><span class="sxs-lookup"><span data-stu-id="859a4-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a4-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="859a4-143">-Name</span></span>
<span data-ttu-id="859a4-144">Bu cmdlet 'in oluşturduğu ağ güvenlik kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a4-145">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="859a4-145">-Priority</span></span>
<span data-ttu-id="859a4-146">Kural yapılandırmasının önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="859a4-147">Bu parametre için kabul edilebilir değerler şunlardır: 100 ile 4096 arasında bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="859a4-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="859a4-148">Öncelikteki her kural için öncelik numarası benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="859a4-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="859a4-149">Öncelik numarası düşükse, kuralın önceliği o kadar yüksek olur.</span><span class="sxs-lookup"><span data-stu-id="859a4-149">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a4-150">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="859a4-150">-Protocol</span></span>
<span data-ttu-id="859a4-151">Yeni bir kural yapılandırmasının uygulandığı ağ protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="859a4-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="859a4-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="859a4-153">TC</span><span class="sxs-lookup"><span data-stu-id="859a4-153">Tcp</span></span>
- <span data-ttu-id="859a4-154">UDP</span><span class="sxs-lookup"><span data-stu-id="859a4-154">Udp</span></span>
- <span data-ttu-id="859a4-155">joker karakter (\*) ile eşleşir.</span><span class="sxs-lookup"><span data-stu-id="859a4-155">wildcard character (\*) to match both.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a4-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="859a4-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="859a4-157">Kaynak adres önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="859a4-158">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="859a4-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="859a4-159">CıDR</span><span class="sxs-lookup"><span data-stu-id="859a4-159">A CIDR</span></span>
- <span data-ttu-id="859a4-160">Kaynak IP aralığı</span><span class="sxs-lookup"><span data-stu-id="859a4-160">A source IP range</span></span>
- <span data-ttu-id="859a4-161">Herhangi bir IP adresiyle eşleşen joker karakter (\*).</span><span class="sxs-lookup"><span data-stu-id="859a4-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="859a4-162">VirtualNetwork, AzureLoadBalancer ve Internet gibi etiketleri de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="859a4-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="859a4-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="859a4-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="859a4-164">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="859a4-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="859a4-165">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="859a4-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a4-166">-Sourceapplicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="859a4-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="859a4-167">Kural için kaynak olarak ayarlanan uygulama güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="859a4-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="859a4-168">' SourceAddressPrefix ' parametresiyle kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="859a4-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859a4-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="859a4-169">-SourcePortRange</span></span>
<span data-ttu-id="859a4-170">Kaynak bağlantı noktasını veya aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="859a4-170">Specifies the source port or range.</span></span>
<span data-ttu-id="859a4-171">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="859a4-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="859a4-172">Bir tamsayı</span><span class="sxs-lookup"><span data-stu-id="859a4-172">An integer</span></span>
- <span data-ttu-id="859a4-173">0 ile 65535 arasında bir tamsayı aralığı</span><span class="sxs-lookup"><span data-stu-id="859a4-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="859a4-174">Herhangi bir bağlantı noktası ile eşleşen bir joker karakter (\*)</span><span class="sxs-lookup"><span data-stu-id="859a4-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="859a4-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859a4-175">CommonParameters</span></span>
<span data-ttu-id="859a4-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="859a4-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859a4-177">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="859a4-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859a4-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="859a4-178">INPUTS</span></span>

### <span data-ttu-id="859a4-179">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="859a4-179">None</span></span>

## <span data-ttu-id="859a4-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="859a4-180">OUTPUTS</span></span>

### <span data-ttu-id="859a4-181">Microsoft. Azure. Commands. Network. modeller. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="859a4-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="859a4-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="859a4-182">NOTES</span></span>

## <span data-ttu-id="859a4-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="859a4-183">RELATED LINKS</span></span>

[<span data-ttu-id="859a4-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="859a4-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="859a4-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="859a4-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="859a4-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="859a4-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="859a4-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="859a4-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


